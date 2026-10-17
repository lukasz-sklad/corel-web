# Corel Web (VectorCraft)

Nowoczesny, webowy edytor grafiki wektorowej działający w przeglądarce, stworzony w czystym Rust (WebAssembly + WebGPU / WebGL2 + egui) na bazie silnika **VectorCraft**.

## Główne cechy

- 🎨 **Domyślny ciemny motyw (Dark Mode):** Wygodna praca z grafiką i precyzyjnymi krzywymi bez męczenia wzroku.
- 🇵🇱 **Interfejs w języku polskim:** Pełne wsparcie dla polskiego interfejsu użytkownika.
- 🎯 **Udoskonalona obsługa formatów CorelDRAW (CDR):**
  - **CDR wersje 1 do X3 (legacy binarne):** Natywny import klasycznych plików CDR z pełnym odczytem geometrii, kolorów i krzywych.
  - **CDR wersje X4 i nowsze (nowoczesne archiwa ZIP/XML/CPNG):** Płynny odczyt i parsowanie nowoczesnych struktur CorelDRAW.
  - Znakomita wydajność i stabilność importu bezpośrednio w przeglądarce bez przesyłania plików na zewnętrzne serwery (100% przetwarzania po stronie klienta).
- 📐 **Szeroka kompatybilność formatów wektorowych:** Obsługa SVG, PDF, Adobe Illustrator (AI), TIFF, EPS oraz formatu natywnego VectorCraft.

## Dostęp online

Aplikacja jest dostępna publicznie pod adresami:
- **[https://corel.lmk.one/](https://corel.lmk.one/)** (Domena produkcyjna zoptymalizowana przez Cloudflare CDN)
- Kopia GitHub Pages: **[https://lukasz-sklad.github.io/corel-web/](https://lukasz-sklad.github.io/corel-web/)**
- Przekierowanie z bloga: **[https://lmk.one/corel](https://lmk.one/corel)**

## Architektura i hosting

- **Silnik:** Rust `wasm32-unknown-unknown`, zoptymalizowany pod kątem minimalnego rozmiaru i maksymalnej wydajności za pomocą `wasm-opt -Oz`.
- **Hosting:** GitHub Pages + Cloudflare Proxy CDN (rekord CNAME `corel.lmk.one` wskazujący na `lukasz-sklad.github.io`).
- **Kompresja:** Pre-generowane zasoby Gzip (`.wasm.gz`, `.js.gz`) gwarantujące błyskawiczne ładowanie.
