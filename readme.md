# Opis projektu
Celem naszego projektu było opracowanie **skalowalnego systemu do monitorowania liczby butli nurkowych na łodziach**.

Nurkowanie staje się coraz popularniejszym sportem, w związku z czym coraz dynamiczniej rozwijają się i rozbudowują centra nurkowe odpowiedzialne za organizowanie podwodnych przygód. Jedną z form wyjazdów nurkowych są safari, czyli jedno lub wielodniowe wycieczki łodziami. Przy dużej liczbie nurków na łodzi, załoga może się pomylić przy liczeniu osób, co może skutkować np. zostawieniem nurków w wodzie.

Rozwiązanie klasyczne: Liczenie osób wchodzących do wody i wychodzących z niej.
Rozwiązanie IoT: Wykrywanie obecności butli i automatyczna weryfikacja ich liczby.

# Technologie
- **Raspberry Pi 0 W** (jako slave) do przetwarzania danych z paneli z czujnikami i przesyłania ich do głównej jednostki na łodzi
- **Raspberry Pi 4** jako główna jednostka na łodzi oraz jako serwer w siedzibie administratora
- **FastAPI** do obsługi RESTful API w celu przesyłania danych na serwer poprzez żądania HTTP
- **Python** do obsługi Raspberry Pi oraz serwera, a także zapisywania danych z łodzi
- **Flutter** do aplikacji webowej służącej do wizualizacji danych

# Instrukcja instalacji

1. Klonowanie repozytorium
```
git clone https://github.com/wojtekbakun/Butlometr-RPi4-server
```

2. Przejście do folderu z wirtualnym środowiskiem
```
cd serwer_RPi4
```

3. Aktywacja wirtualnego środowiska
```
source vSRPi4/bin/activate
```

4. Przejście do folderu głównego
```
cd vSRPi4
```

5. Instalacja niezbędnych bibliotek
```
pip install -r requirements.txt
```

## Requirements.txt
```
fastapi
uvicorn[standard]
faker
firebase_admin
```

# Przewodnik użytkowania

## Uruchomienie serwera na RPi 0
```
uvicorn main:app --reload --host 0.0.0.0
```

# Przykład użytkowania

