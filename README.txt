
# AR Share Template (GLB + USDZ)

To repo/zip pozwala szybko udostępnić model 3D w AR przez link. Działa na iPhonie (USDZ/Quick Look) i Androidzie (GLB/Scene Viewer).

## Co zrobić krok po kroku
   - Android: **model.glb** (glTF 2.0, najlepiej z kompresją Draco).
   - iOS: **model.usdz** (np. przez Apple Reality Converter lub inny konwerter).
   - Podmień pliki `model.glb`, `model.usdz` i opcjonalnie `poster.png` (miniatura).
   - Utwórz nowe repo, wrzuć pliki (ten index.html i modele).
   - W ustawieniach repo włącz **Pages** dla gałęzi `main` i katalogu `/`.
   - Otwórz udostępniony adres URL (np. `https://twoja-nazwa.github.io/ar-demo/`).
Wyślij link odbiorcy. Na telefonie zobaczy przycisk „Wyświetl w AR”.

## Wskazówki
- Skala: 1 jednostka = 1 metr. Ustaw origin na spód modelu i zastosuj skalę (Ctrl+A).
- Tekstury: PBR (BaseColor/MetallicRoughness/Normal/AO). Bake’uj proceduralne node’y.
- Wydajność mobilna: 50–200k trójkątów, tekstury 1–4K.
- Jeśli iOS nie pokazuje AR, sprawdź, czy masz **USDZ** i że link działa po HTTPS.
