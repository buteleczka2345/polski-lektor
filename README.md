# Lektor Multilanguage

**Lektor do Chrome — zamienia napisy w filmach i serialach na głos. Wersja 3.0.6**

Rozszerzenie do przeglądarki, które odczytuje tekst z napisów na strumieniach
i wypowiada go syntetycznym głosem. Wszystko dzieje się **na Twoim komputerze** —
bez serwera, bez Pythona, bez chmury.

## W punktach

### Co to jest
- Rozszerzenie Chrome (**Manifest V3**), gotowe do wgrania w trybie deweloperskim
- Czyta napisy odtwarzacza i zamienia je na mowę
- Obsługiwane serwisy: **Netflix, YouTube, Prime Video, Amazon Video, iQ / iQIYI, Dailymotion, Rumble**
- Panel sterowania na stronie filmu: **prędkość czytania** i **kalibracja opóźnienia** (offset w ms)

### Silnik i głosy
- Wbudowany silnik **sherpa-onnx** (ONNX Runtime) skompilowany do **WebAssembly** — synteza leci w przeglądarce
- Katalog **236 modeli głosowych w 51 językach**: VITS (229), Matcha (4), Kokoro (3)
- W pakiecie **wbudowany polski głos męski**: VITS-Piper `pl_PL-meski_wg_glos`
- Pozostałe modele w katalogu do pobrania na żądanie (uprawnienie `downloads`)

### Prywatność
- Nic nie wychodzi na zewnątrz — zero serwera, zero chmury
- Działa offline, po jednorazowym pobraniu modelu
- Uprawnienia: `activeTab`, `storage`, `offscreen` (audio), `downloads` — żadnych „kontaktów” z serwerem firmy

### Instalacja
1. Rozpakuj pobrany ZIP (ok. 229 MB)
2. W Chrome wejdź na `chrome://extensions` i włącz **Tryb deweloperski**
3. Kliknij **Wczytaj rozpakowane** i wskaż folder `Lektor Multilanguage`
4. Przypnij ikonę lektora i włącz go na stronie z filmem

### Rozmiar
- ZIP: ok. **229 MB**
- Po rozpakowaniu: ok. **301 MB** (WASM silnika ok. 11 MB + modele + dane wymowy espeak)
- Wymaga przeglądarki opartej na Chromium (Manifest V3 + WASM)

## Moja ocena

- **Największa zaleta: cały TTS w przeglądarce.** Po instalacji działa sam,
  także bez internetu. To odróżnia to rozszerzenie od typowych „czytników”,
  które wołają chmurę i wnoszą opóźnienie do każdego zdania.
- **Katalog 236 modeli w 51 językach** to poważny zakres — przy czym pojedynczy
  głos waży od kilkudziesięciu do kilkuset MB, więc paczka jest celowo duża
  (stąd dystrybucja przez Release, a nie przez zwykłe repo).
- **Regulacja prędkości i opóźnienia** rozwiązuje najczęstszy problem lektorów:
  mowa musi trafiać w moment, kiedy tekst pojawia się na ekranie. Suwak pozwala
  dostroić to w milisekundach.
- **Do czego się przyda:** nauka języków (głos w danym języku + oryginalne napisy),
  dostępność, oglądanie bez dźwięku, walidacja tłumaczeń i instrukcji głosowych.
- **Uwaga praktyczna:** pierwsze wypowiedzenie po zmianie modelu potrafi potrwać
  sekundę–dwie (rozruch silnika WASM), więc warto dać lektorowi chwilę na start.

## Pobieranie

Wersja v1.0 — plik `Lektor-Multilanguage.zip` w sekcji **Assets** poniżej.
