
# AR Share Template (GLB + USDZ)

To repo/zip pozwala szybko udostępnić model 3D w AR przez link. Działa na iPhonie (USDZ/Quick Look) i Androidzie (GLB/Scene Viewer).

## Co zrobić krok po kroku
1) Wyeksportuj z Blendera:
   - Android: **model.glb** (glTF 2.0, najlepiej z kompresją Draco).
   - iOS: **model.usdz** (np. przez Apple Reality Converter lub inny konwerter).
2) W tym folderze:
   - Podmień pliki `model.glb`, `model.usdz` i opcjonalnie `poster.png` (miniatura).
3) Opublikuj online przez HTTPS, np. **GitHub Pages**:
   - Utwórz nowe repo, wrzuć pliki (ten index.html i modele).
   - W ustawieniach repo włącz **Pages** dla gałęzi `main` i katalogu `/`.
   - Otwórz udostępniony adres URL (np. `https://twoja-nazwa.github.io/ar-demo/`).
4) Wyślij link odbiorcy. Na telefonie zobaczy przycisk „Wyświetl w AR”.

## Alternatywa: Bez własnego hostingu
- **Sketchfab**: wgraj GLB/FBX, ustaw **Unlisted** i wyślij link (ma wbudowany przycisk AR dla iOS/Android).
- **iOS tylko AR**: wyślij bezpośredni link do `model.usdz` w HTTPS — Safari otworzy Quick Look z AR.
- **Android tylko AR**: link bezpośredni do Scene Viewer:
  ```
  https://arvr.google.com/scene-viewer/1.0?file=FULL_HTTPS_URL_TO/model.glb&mode=ar_preferred&title=Model
  ```

## Wskazówki
- Skala: 1 jednostka = 1 metr. Ustaw origin na spód modelu i zastosuj skalę (Ctrl+A).
- Tekstury: PBR (BaseColor/MetallicRoughness/Normal/AO). Bake’uj proceduralne node’y.
- Wydajność mobilna: 50–200k trójkątów, tekstury 1–4K.
- Jeśli iOS nie pokazuje AR, sprawdź, czy masz **USDZ** i że link działa po HTTPS.
