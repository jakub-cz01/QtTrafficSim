# QtTrafficSim

**QtTrafficSim** (wewnętrznie znany jako *EasyRider*) to interaktywny symulator ruchu ulicznego napisany w języku C++ z wykorzystaniem frameworka Qt. Aplikacja pozwala na wizualizację i sterowanie parametrami ruchu drogowego w czasie rzeczywistym, symulując zachowania pojazdów, sygnalizację świetlną oraz interakcje między uczestnikami ruchu.

## Spis treści
1. [Opis projektu](#opis-projektu)
2. [Funkcjonalności](#funkcjonalności)
3. [Technologie](#technologie)
4. [Zrzuty ekranu](#zrzuty-ekranu)
5. [Instalacja i kompilacja](#instalacja-i-kompilacja)
6. [Struktura projektu](#struktura-projektu)

## Opis projektu

Celem projektu jest symulacja prostego systemu drogowego. Aplikacja zarządza cyklem życia pojazdów, ich poruszaniem się po wyznaczonej mapie drogowej (grafie ulic i skrzyżowań) oraz reakcją na otoczenie, takie jak inne pojazdy czy światła drogowe. Użytkownik ma możliwość wpływania na przebieg symulacji za pomocą panelu sterowania.

## Funkcjonalności

*   **Symulacja w czasie rzeczywistym:** Płynne odwzorowanie ruchu pojazdów.
*   **System sterowania ruchem:** Obsługa skrzyżowań oraz sygnalizacji świetlnej (klasa `TrafficLight`).
*   **Inteligentne zachowanie pojazdów:**
    *   Wykrywanie kolizji i zachowanie bezpiecznego odstępu.
    *   Stany pojazdów: Jazda (`DrivingState`), Zatrzymanie (`StoppedState`), Podążanie za innym pojazdem (`FollowingState`).
*   **Panel kontrolny GUI:**
    *   Start/Pauza symulacji.
    *   Suwak limitu pojazdów na mapie.
    *   Suwak częstotliwości pojawiania się nowych aut (Spawn Rate).
    *   Suwak prędkości symulacji.
*   **Zarządzanie mapą:** System oparty na węzłach (`StreetMapNode`) i ulicach (`StraightStreet`), tworzący spójną sieć drogową.

## Technologie

Projekt został zrealizowany przy użyciu następujących technologii:

*   **Język:** C++17
*   **Framework GUI:** Qt (Qt5 / Qt6 - Widgets)
*   **System budowania:** CMake (minimalna wersja 3.5)

## Zrzuty ekranu

<img width="1002" height="739" alt="image" src="https://github.com/user-attachments/assets/0b085884-f77d-458b-8b0c-498ab0f33a03" />
*Widok główny symulacji*

## Instalacja i kompilacja

Aby skompilować i uruchomić projekt, potrzebujesz kompilatora C++, CMake oraz bibliotek Qt.

### Wymagania wstępne
*   C++ Compiler (GCC, Clang, MSVC) wspierający C++17
*   CMake
*   Qt 5 lub Qt 6 (moduł `Widgets`)

### Kroki instalacji

1.  **Sklonuj repozytorium:**
    ```bash
    git clone https://github.com/jakub-cz01/QtTrafficSim.git
    cd QtTrafficSim
    ```

2.  **Utwórz katalog budowania:**
    ```bash
    mkdir build
    cd build
    ```

3.  **Skonfiguruj projekt za pomocą CMake:**
    ```bash
    cmake ..
    ```

4.  **Skompiluj projekt:**
    ```bash
    cmake --build .
    ```

5.  **Uruchom aplikację:**
    Na systemie Linux/macOS:
    ```bash
    ./EasyRider
    ```
    Na systemie Windows:
    ```bash
    Debug\EasyRider.exe
    ```

## Struktura projektu

Główne pliki i klasy w projekcie:

*   **`main.cpp`**: Punkt wejścia aplikacji.
*   **`mainwindow.cpp/h`**: Obsługa głównego okna i interfejsu użytkownika.
*   **`simulationloop.cpp/h`**: Główna pętla sterująca logiką symulacji (wzorzec Singleton).
*   **`vehicle.cpp/h`**: Klasa reprezentująca pojazd.
*   **`vehiclemanager.cpp/h`**: Zarządzanie tworzeniem i usuwaniem pojazdów.
*   **`trafficlight.cpp/h`**: Logika sygnalizacji świetlnej.
*   **`streetmap.cpp/h`**: Reprezentacja mapy drogowej.
*   **`*.ui`**: Pliki interfejsu użytkownika Qt Designer.

---
Autor: [jakub-cz01](https://github.com/jakub-cz01)
