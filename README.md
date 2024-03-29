# Anty-Phishing
### *W ramach przedmiotu "Zarządzanie projektami informatycznymi"*

Głównym celem projektu jest stworzenie filtra anty-phishingowego, który będzie chronił użytkowników przed atakiem typu  "Phishing" oraz złośliwym oprogramowaniem. Jego zadanie to zapewnienie większego bezpieczeństwa sieci. Dzięki tej funkcji przeglądarka będzie wyświetlać ostrzeżenia podczas odwiedzin strony phishingowej, czyli zgłoszonej jako oszustwo internetowe, podszywającej się pod prawdziwą witrynę, a także strony będącej źródłem niechcianego oprogramowania.

## Korzyści wynikające z używania filtra
- Uniknięcie kosztownych strat w firmie
- Wzmożona ochrona w odpowiedzi na stale zwiększającą się liczbę ataków
- Pewność, że przetwarzane dane są bezpieczne
- Bezpieczna korespondecja 
- Automatyczna segregacja wiadomości

## Skład projektu

| Sefffciu | Pentester | Piłkarz |

## Założenia funkcjonalne usługi
- Nieprzerwana ochrona korespondencji
- Odrzucanie szkodliwych wiadomości
- Odfiltrowywanie spamu
- Analiza załączników 
- Automatyczne aktualizowanie kampanii phishingowych
- Stałe łącze internetowe
- Możliwość przywrócenia "odrzuconych" wiadomości
- Zarządzanie filtrem z dowolnego miejsca

# Schemat architektury

![Alt text here](schemat-filtra.png)


# Usługa anty-phisingowa

## Wymagania funkcjonalne
Użytkownik powinien posiadać możliwość ciągłego korzystania z usługi. Wiadomości otrzymane przez użytkownika powinny być analizowane przez filtr w śrowisku sand-boxowym w celu uniknięcia ewentualnych zagrożeń. Następnie zweryfikowane wiadomości trafiają do użytkownika, który w tym momencie posiada pewność, że jest ona bezpieczna. Jest to główny cel produktu, którym jest filtr anty-phisingowy. Istotnym elementem jest czas, ponieważ przewidujemy, że filtr będzie dział nieprzerwanie i przeanalizowane przez filtr wiadomości będą dostarczane do użytkownika na bieżąco. 
## Wymagania bezpieczeństwa
W kontekście bezpiecznego funkcjonowania filtru konieczne jest stworzenie polityki bezpieczeństwa w celu uzyskania zbioru spójnych, precyzyjnych reguł i procedur, według których nasza organizacja będzie budować dane, dokumenty i zasoby informatyczne, zarządzać nimi oraz je udostępniać. Określać one będzie także, które zasoby i w jaki sposób mają być chronione. 
## Wymagania wydajnościowe
Głównym założeniem filtra antyphisingowego jest sprawdzanie każdej odwiedzanej strony i porównywanie jej z listami znanych niebezpiecznych stron, również tych oferujących niechciane oprogramowanie. Listy te będą regularnie aktualizowane w określonych ramach czasowych. W przypadku próby wejścia na niebezpieczną stronę lub pobrania groźnego oprogramowania, filtr będzie blokował tego rodzaju działania.
# Usługa przywracania usuniętych wiadomości
Moduł ten odpowiada za przywrócenie usuniętych przez filtr wiadomości ponownie do użytkownika.

## Wymagania funkcjonalne
W wyniku błędnie zinterpretowanych przez system wiadomości, użytkownik posiada możliwość zgłoszenia administratorowi informacji o błędnym usunięciu wiadomości. W takim wypadku zarządzający platformą ma możliwość przywrócenia z serwera "kosza" usuniętej wiadomości na skrzynkę pocztową użytkownika. Proces przywracania charakteryzuje się ponownym przejściem procesu analizy wiadomości pod kątem możliwości wystąpienia phishingu pod okiem administratora. W przypadku poprawnego przejścia testu wiadomość trafia do docelowego odbiorcy.
## Wymagania bezpieczeństwa
W celu poprawnego działania modułu należy nawiązać współpracę z twórcami czarnych list domen, które zostały określone jako złośliwe w sieci.  

## Wymagania wydajnościowe
Do poprawnego działania tego modułu wymagane jest wprowadzenie do usługi dodatkowego serwera "kosza" z którym serwer główny będzie połączony, w którym przetrzymywane będą przez określony czas wiadomości zweryfikowane jako negatywne. Dostęp do kosza musi zostać zapewniony przez cały czas pracy filtra dla poprawnego działania usługi. Zarządzanie tym elementem przypisane jest tylko i wyłącznie administratorom usługi. Dodatkową formą mającą znaczący wpływ na poprawną weryfikacje jest stosowanie środowiska sandbox, w którym uruchamiane będą załączniki dołączone do treści wiadomości.
## Usługa raportowania

## Wymagania funkcjonalne
W usłudze raportowania jest możliwość wybrania gotowego szablonu i nazwy raportu oraz przydzielenie go do odpowiedniej grupy raportów . Możliwość korzystania z narzędzi do analizy oraz przedstawienia danych.Sprawdzenie i porównywanie danych raportowych w celu podjęcia na ich podstawie ważnych decyzji biznesowych.Dowolność w podjęciu decyzji o udostępnieniu wygenerowanego raportu.

## Wymagania bezpieczeństwa
Zapisywanie wygenerwoanych raportów w chmurze.Utrzymywanie usuniętych raportów w odpowiednim folderze z możliwością przywrócenia przez pewien czas.

## Wymagania wydajnościowe
Możliwie szybkie wygenerowanie raportu.


