# Ørion — osobisty asystent AI dla Windows

[![Windows 10/11](https://img.shields.io/badge/Windows-10%20%7C%2011-14b8a6?style=flat-square&logo=windows)](https://github.com/DolilDev/Orion/releases)
[![Beta](https://img.shields.io/badge/status-publiczna%20beta-f5b942?style=flat-square)](https://github.com/DolilDev/Orion/releases)
[![Issues](https://img.shields.io/github/issues/DolilDev/Orion?style=flat-square)](https://github.com/DolilDev/Orion/issues)

## Pobierz najnowszego Øriona

[![Pobierz Ørion 0.20.0 beta 56](https://img.shields.io/badge/Pobierz-Ørion%200.20.0%20beta%2056-14b8a6?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/DolilDev/Orion/releases/tag/app-v0.20.0-beta.56)

**[Przejdź do wydania i pobierz instalator dla Windows →](https://github.com/DolilDev/Orion/releases/tag/app-v0.20.0-beta.56)**

> Najnowsza wersja: **0.20.0 beta 56**. Poprzednie i techniczne wydania
> rozszerzeń pozostają dostępne w pełnym [katalogu Releases](https://github.com/DolilDev/Orion/releases).

Beta 56 ogranicza przypadkowe reakcje na ciszę i dźwięki tła. Dokładniej
potwierdza hasło „Orion”, odrzuca typowe błędne transkrypcje i wymaga
jednoznacznego polecenia przed wyłączeniem lub restartem komputera.

Ørion to natywna aplikacja dla Windows, która łączy rozmowę z AI ze sterowaniem
komputerem, organizacją dnia, lokalną wiedzą i opcjonalnymi rozszerzeniami.
Możesz pisać, mówić albo wywołać małe okno nad dowolną aplikacją skrótem
`Shift+Alt+Spacja`. `Ctrl+Alt+Spacja` otwiera główne okno Øriona.

To nie jest wyłącznie chatbot. Ørion potrafi wykonywać kontrolowane działania:
otwierać aplikacje, zarządzać oknami i dźwiękiem, tworzyć przypomnienia,
przeszukiwać wskazane dokumenty, prowadzić notatki, rejestrować spotkania czy
śledzić cele i treningi. Działania zmieniające system respektują ustawienia
uprawnień, pokazują podgląd i trafiają do historii aktywności.

> [!IMPORTANT]
> Ørion jest obecnie publiczną wersją beta. Przed wykonaniem ważnej operacji
> sprawdź podgląd działania. Błędy i pomysły możesz zgłaszać w
> [GitHub Issues](https://github.com/DolilDev/Orion/issues).

## Pobieranie i instalacja

1. Otwórz stronę [Releases](https://github.com/DolilDev/Orion/releases).
2. Pobierz najnowszy plik `Orion-Setup-*.exe`.
3. Uruchom instalator i przejdź przez pierwszą konfigurację.
4. Wklej klucz wybranego dostawcy AI albo wybierz lokalną Ollamę.

Wymagania:

- Windows 10 lub Windows 11 w wersji 64-bitowej;
- połączenie z internetem dla modeli chmurowych i pobierania rozszerzeń;
- klucz API wybranego dostawcy albo uruchomiona lokalnie Ollama;
- mikrofon tylko wtedy, gdy chcesz korzystać z głosu lub ØrionMeet.

Aktualizacje są pobierane i weryfikowane wewnątrz Øriona. Opcjonalny automat
sprawdza rozmiar i sumę SHA-256, tworzy kopię danych, instaluje nową wersję
w bezpiecznym momencie, a potem uruchamia aplikację ponownie. Instalator beta
nie jest jeszcze podpisany certyfikatem,
dlatego Windows SmartScreen może wyświetlić ostrzeżenie. Pobieraj pliki wyłącznie
z oficjalnych wydań w tym repozytorium.

Powiadomienie o dostępnej aktualizacji pozostaje na dzwonku aż do jej
zainstalowania. W ostatniej sekcji Ustawień można również odinstalować Øriona,
wybierając zachowanie wszystkich danych i kluczy albo ich całkowite usunięcie.

## Darmowe AI — co wybrać?

| Wariant | Koszt na start | Gdzie działa model | Najlepszy wybór, gdy… |
|---|---:|---|---|
| **Groq** | bezpłatny plan z limitami | chmura | chcesz zacząć szybko i bez pobierania modeli |
| **NVIDIA NIM** | darmowe endpointy developerskie z limitami | chmura NVIDIA | chcesz testować różne otwarte modele i modele wizyjne |
| **Ollama** | bez opłat za API | Twój komputer | prywatność jest ważniejsza od szybkości i masz miejsce na model |

Limity, dostępne modele i zasady bezpłatnych planów ustalają ich dostawcy i mogą
się zmieniać. Ørion nie dolicza własnej opłaty do wykorzystania API.

### Groq — najprostszy start

1. Załóż konto w [Groq Console](https://console.groq.com/).
2. Otwórz [API Keys](https://console.groq.com/keys) i wybierz utworzenie klucza.
3. Skopiuj klucz zaczynający się zwykle od `gsk_`.
4. W pierwszej konfiguracji Øriona wybierz **Groq** i wklej klucz. Później możesz
   zrobić to przez **Ustawienia → AI → Dodaj klucz API**.
5. Wybierz model i zapisz konfigurację.

Groq udostępnia plan Free z limitami liczby zapytań i tokenów. Aktualne wartości
znajdziesz w [oficjalnej tabeli limitów](https://console.groq.com/docs/rate-limits).
Do zwykłej rozmowy i prostych poleceń jest to rekomendowany sposób rozpoczęcia.

### NVIDIA NIM — darmowe endpointy do developmentu

Do korzystania z hostowanego API NVIDIA **nie potrzebujesz karty NVIDIA** — model
działa w chmurze. Karta graficzna ma znaczenie dopiero przy modelach uruchamianych
lokalnie.

1. Zaloguj się lub utwórz konto w [NVIDIA API Catalog](https://build.nvidia.com/explore).
2. Otwórz wybrany model oznaczony jako **Free Endpoint**.
3. Kliknij **Get API Key** albo przejdź do
   [ustawień kluczy](https://build.nvidia.com/settings/api-keys).
4. Dołącz do NVIDIA Developer Program, jeśli kreator o to poprosi.
5. Skopiuj klucz zaczynający się zwykle od `nvapi-`.
6. W Ørionie wybierz **NVIDIA NIM**, wklej klucz i zapisz konfigurację.

NVIDIA opisuje te endpointy jako bezpłatne API serwerowe do developmentu.
Poszczególne modele mogą mieć inne limity lub warunki licencyjne — sprawdź kartę
modelu przed użyciem go komercyjnie. Instrukcję tworzenia klucza opisuje także
[oficjalny quickstart NVIDIA](https://docs.api.nvidia.com/nim/docs/api-quickstart).

### Ollama — całkowicie lokalnie, bez klucza API

1. Pobierz [Ollama dla Windows](https://ollama.com/download/windows).
2. Zainstaluj ją i pozostaw uruchomioną w tle.
3. W Ørionie wybierz **Użyj Ollama lokalnie**.
4. Jeżeli brakuje modelu, Ørion pokaże jego dokładny rozmiar i poprosi o zgodę
   przed pobraniem.

Ollama udostępnia lokalne API pod adresem `http://localhost:11434`. Działa na CPU,
a zgodna karta NVIDIA lub AMD może znacznie przyspieszyć odpowiedzi. Sama
instalacja Ollamy wymaga według jej dokumentacji co najmniej około 4 GB miejsca,
a modele potrzebują dodatkowej przestrzeni. Więcej informacji znajduje się w
[oficjalnej dokumentacji Ollama dla Windows](https://docs.ollama.com/windows).

## Klucze i prywatność

- Klucze API i tokeny logowania trafiają do **Windows Credential Manager**, a nie
  do zwykłego pliku ustawień.
- Ørion rozpoznaje dostawcę po formacie klucza lokalnie.
- Lokalna wiedza indeksuje tylko foldery jawnie wskazane przez użytkownika.
- ØrionMeet może nagrywać i transkrybować spotkania lokalnie.
- Historię, pamięć i dane rozszerzeń można usunąć bez kasowania kluczy API.
- Nigdy nie wklejaj klucza API, tokenu OAuth ani prywatnego dokumentu do Issues.

Modele chmurowe otrzymują treść potrzebną do odpowiedzi. Dla prywatnych danych
wybierz Ollamę albo profil korzystający z modelu lokalnego.

## Przykładowe rzeczy, o które możesz poprosić

To tylko pomysły — część wymaga odpowiedniego rozszerzenia lub połączonej usługi.

```text
Co jest teraz na moim ekranie i na co powinienem zwrócić uwagę?
```

```text
O 17:30 przypomnij mi, żebym wysłał podsumowanie sprintu.
```

```text
Ustaw głośność Spotify na 25%, włącz Deep Focus i otwórz projekt Sprintly.
```

```text
Z tej wypowiedzi zrób uporządkowaną notatkę z nagłówkami i checklistą.
```

```text
Przeszukaj moje PDF-y z folderu Studia i podaj źródło każdego wniosku.
```

```text
Uruchom trzy agenty Pi korzystające z mojego zalogowanego Codexa w workspace Sprintly.
```

```text
Dodaj do celu Siłownia 1 godzinę i zapisz check-in 5/5: dobry trening.
```

```text
Zapisz w ØrionFit 4 serie po 8 powtórzeń wyciskania z ciężarem 80 kg.
```

```text
Nagraj spotkanie z mikrofonu i dźwięku systemowego, a potem zapisz transkrypcję.
```

```text
Gdy podłączę słuchawki, włącz Deep Focus, ustaw głośność na 30% i otwórz Spotify.
```

## Pełna tabela funkcji

| Obszar | Co potrafi Ørion | Dostępność / wymagania |
|---|---|---|
| Rozmowa | Chat tekstowy, odpowiedzi strumieniowe, załączniki i wspólny kontekst akcji | Wbudowane; wymaga modelu AI |
| Szybkie akcje | Małe okno nad każdą aplikacją, domyślnie `Ctrl+Alt+Spacja`; skrót można zmienić | Wbudowane |
| Głos | Dyktowanie, wake word, lokalny lub chmurowy STT i odpowiedzi TTS | Wbudowane; mikrofon, opcjonalnie model mowy |
| Przerywanie mowy | „Ørion stop”, przycisk zatrzymania albo wysłanie nowej wiadomości przerywa wypowiedź | Wbudowane |
| Ekran i wizja | Zrzuty ekranów, pytania „co jest na ekranie?” i analiza obrazu | Wbudowane; model obsługujący obrazy |
| Schowek i zaznaczenie | Odczyt tekstu, plików i obrazów ze schowka, analiza zaznaczonego tekstu, zapis wyniku do schowka | Wbudowane |
| Aplikacje i strony | Wyszukiwanie, otwieranie i bezpieczne zamykanie aplikacji; otwieranie stron i wyszukiwanie w sieci | Wbudowane |
| Własne skróty | Zapisywanie i uruchamianie skrótów do aplikacji, stron, plików i folderów | Wbudowane |
| Dźwięk | Odczyt i zmiana głośności głównej, wyciszenie oraz głośność konkretnej aplikacji | Wbudowane; Windows Core Audio |
| Multimedia | Odtwarzanie/pauza, następny, poprzedni i stop dla aktywnego odtwarzacza Windows | Wbudowane; bez logowania do Apple Music |
| Okna i monitory | Lista okien i monitorów, fokus, minimalizacja, maksymalizacja, przywracanie, przenoszenie i zamykanie | Wbudowane |
| Karty przeglądarki | Lista, aktywacja, zamykanie i przywracanie kart Chrome, Edge lub Brave przez tryb CDP | Wbudowane; pełna lista kart wymaga uruchomienia CDP |
| Planer | Lokalne przypomnienia, wydarzenia i zadania w widokach miesiąca, tygodnia, dnia i listy; przeciąganie, skróty, cofanie oraz kolejka offline | Wbudowane; działa w tle |
| Minutniki | Minutniki działające również po schowaniu aplikacji do zasobnika | Wbudowane |
| Centrum powiadomień | Pominięte przypomnienia i wydarzenia, błędy integracji oraz trwałe informacje o oczekujących aktualizacjach | Wbudowane |
| Deep Focus | Czasowe wyciszenie Øriona i ograniczenie rozpraszaczy z przywróceniem poprzedniego stanu | Wbudowane |
| Nie przeszkadzać | Wstrzymanie wake word, TTS i wyskakujących powiadomień | Wbudowane |
| Pamięć | Zapamiętywanie, wyszukiwanie i usuwanie faktów oraz jawny profil użytkownika | Wbudowane; lokalny zapis |
| Profil współpracy | Preferowany ton, styl odpowiedzi i poziom samodzielności Øriona | Wbudowane; lokalny zapis |
| Profile kontekstowe | Osobne profile Prywatne, Praca i Nauka z własnym modelem, pamięcią, folderami, stylem i automatyzacjami | Wbudowane; konfigurowane również przez chat |
| Router modeli | Dobór szybkiego, lokalnego lub mocniejszego modelu zależnie od zadania; historia wyboru, tokeny i koszt | Wbudowane; opcjonalne |
| Wielu dostawców AI | Groq, NVIDIA NIM, Ollama, Google Gemini, OpenRouter, OpenAI, Anthropic, xAI, Mistral AI i DeepSeek | Wbudowane; zależnie od dostawcy wymagany klucz |
| Uprawnienia | Dla każdej akcji: zawsze pozwalaj, pytaj przed użyciem albo zablokuj | Wbudowane |
| Podgląd działania | Przed ryzykowną operacją Ørion pokazuje nazwę akcji i jej argumenty | Wbudowane |
| Cofanie | Centrum odwracalnych operacji z bieżącej sesji i cofnięcie wybranego wpisu, m.in. zmian w ØrionNotes i danych rozszerzeń | Wbudowane; tylko dla operacji z bezpieczną akcją odwrotną |
| Historia aktywności | Rejestr wykonanych, odrzuconych i błędnych akcji wraz z rezultatem | Wbudowane; lokalna baza |
| Operacje systemowe | Przygotowanie restartu, wyłączenia lub wylogowania z osobnym etapem potwierdzenia | Wbudowane; zawsze wymaga potwierdzenia |
| Lokalna wiedza | Indeks wybranych folderów, PDF-ów, dokumentów, plików tekstowych i notatek; odpowiedzi ze źródłami | Wbudowane; konfiguracja przez chat |
| Gmail | Odczyt nagłówków, wysyłanie wiadomości i powiadomienia o nowych mailach | Opcjonalna integracja Google |
| Google Calendar | Lista kalendarzy i wydarzeń, dodawanie, edycja, usuwanie oraz powiadomienia | Opcjonalna integracja Google |
| Google Tasks | Listy zadań, dodawanie, edycja, ukończenie i usuwanie zadań | Opcjonalna integracja Google |
| Spotify | Wyszukiwanie utworów i sterowanie aktywnym odtwarzaczem | Opcjonalne OAuth; część funkcji może wymagać Spotify Premium |
| SoundCloud | Wyszukiwanie odtwarzalnych utworów | Opcjonalne OAuth |
| Leki | Lista leków, dawki, harmonogramy i historia przyjęcia | Wbudowane; dane lokalne |
| Pogoda | Bieżące warunki oraz prognoza dzienna i godzinowa dla podanej lub zapisanej lokalizacji | Wbudowane; wymaga internetu |
| Orion Doctor | Test kondycji Ollamy, modeli, dźwięku, głosu, kluczy, integracji, aktualizacji, rozszerzeń i danych; dostępny również przez pytanie „czy wszystko działa?” | Wbudowane; test tylko do odczytu |
| Samonaprawa | Uruchomienie Ollamy, instalacja po zgodzie i pobranie modelu po pokazaniu rozmiaru | Wbudowane; każda instalacja wymaga zgody |
| Aktualizacje | Ręczne lub automatyczne pobieranie, SHA-256, harmonogram instalacji, zweryfikowany backup, historia i przywracanie danych | Wbudowane; GitHub Releases |
| Kontrolowana proaktywność | Lokalne sugestie ważnych spraw z regulowanym dziennym limitem, bez wykonywania działań | Opcjonalna; domyślnie wyłączona |
| Odinstalowanie | Usunięcie aplikacji z wyborem: zachowaj wszystkie dane i klucze albo usuń je całkowicie | Wbudowane; ostatnia sekcja Ustawień |
| Rozszerzenia | Katalog możliwości, pobieranie osobnej paczki zweryfikowanej sumą SHA-256, kontrola manifestu, włączanie, wyłączanie i usuwanie | Funkcje są pobierane dopiero podczas instalacji |
| Praca w tle | Zasobnik systemowy, przypomnienia i monitory integracji bez otwartego głównego okna | Wbudowane |
| Jedna instancja | Kolejne uruchomienie aktywuje działającego Øriona zamiast otwierać następny proces aplikacji | Wbudowane |
| Autoprezentacja | Bezpieczny pokaz najważniejszych obszarów aplikacji bez wykonywania zmian | Wbudowane |

### Rozszerzenia

| Rozszerzenie | Funkcje | Dane i wymagania |
|---|---|---|
| **ØrionCode** | Wiele agentów Pi, nazwy sesji, wspólny workspace, odpinane panele i wysyłanie poleceń do konkretnego agenta | Lokalne Pi korzystające z zalogowanego Codexa; nie ma osobnego trybu PowerShell ani innych agentów |
| **ØrionNotes** | Notatki, tagi, gwiazdki, wyszukiwanie, edycja głosem, notatka z dłuższej wypowiedzi i formatowanie przez AI | Dane lokalne; akcje dostępne również z głównego chatu |
| **ØrionRhythm** | Cele dzienne i wielodniowe, kilka liczników naraz, check-iny, kalendarz, import danych, statystyki i panel Start | Dane lokalne; cele są oddzielone od zadań i przypomnień |
| **ØrionFlow** | Rutyny opisane naturalnym językiem, podgląd kroków, próba bez zmian i wyzwalacze: czas, aplikacja, audio, lokalizacja, wiadomość, kalendarz lub głos | Każdy krok przechodzi przez uprawnienia i audyt |
| **ØrionMeet** | Nagrywanie mikrofonu i/lub dźwięku systemowego, lokalna transkrypcja, podsumowanie, decyzje, działania, edycja i eksport TXT | Mikrofon/dźwięk systemowy; użytkownik odpowiada za zgodę uczestników |
| **ØrionFit** | Plany treningowe, serie, powtórzenia, ciężar, objętość, rekordy, historia, pomiary sylwetki i wykres postępu | Dane lokalne; oddzielone od ØrionRhythm |

## Bezpieczeństwo działań

Ørion nie powinien wykonywać operacji systemowych „w ciemno”. Akcje pochodzą z
jawnej listy, argumenty są walidowane, a wynik jest sprawdzany po wykonaniu.
Usuwanie, wysyłanie wiadomości, zamykanie programu i inne ryzykowne działania
mogą wymagać potwierdzenia — zależnie od ustawionej przez Ciebie reguły.

AI może się pomylić. Nie używaj Øriona jako jedynego źródła porad medycznych,
prawnych lub finansowych i zawsze sprawdzaj działania mające poważne skutki.

## Aktualizacje i rozszerzenia

Publiczne repozytorium służy obecnie do dystrybucji instalatora, pakietów
rozszerzeń i obsługi zgłoszeń. Kod źródłowy pozostaje prywatny.

Ørion pobiera aplikację i oficjalne rozszerzenia wyłącznie z wydań
`DolilDev/Orion`. Przed instalacją sprawdza adres zasobu, rozmiar, SHA-256 oraz —
w przypadku rozszerzeń — zawartość manifestu i sumy poszczególnych plików.

## Zgłaszanie błędów i pomysłów

W Orion Doctor wybierz **Zgłoś problem**, aby utworzyć lokalną paczkę z
opcjonalnymi logami po usunięciu sekretów i otworzyć gotowy, jeszcze niewysłany
formularz. Możesz też przejść bezpośrednio do
[GitHub Issues](https://github.com/DolilDev/Orion/issues/new). Podaj:

- wersję Øriona i Windows;
- kroki prowadzące do problemu;
- oczekiwany i rzeczywisty rezultat;
- bezpieczny zrzut ekranu, jeśli pomaga odtworzyć błąd.

Przed wysłaniem usuń ze zrzutów i logów klucze API, tokeny, prywatne ścieżki,
adresy e-mail oraz treść dokumentów.

---

Ørion powstaje jako jedno miejsce do rozmowy, organizacji i bezpiecznego
sterowania Windowsem — bez konieczności otwierania osobnej aplikacji do każdej
drobnej czynności.
