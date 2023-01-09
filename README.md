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

# Usługa anty-phisingowa

## Wymagania funkcjonalne

## Wymagania bezpieczeństwa

## Wymagania wydajnościowe

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

## Wymagania bezpieczeństwa

## Wymagania wydajnościowe


