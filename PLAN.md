# RETRO TERMINAL 90s REDESIGN — Plan transformacji orzech.me

## Wizja

Strona ma wyglądać jak terminal/konsola z lat 90., z klimatem wczesnego internetu —
ale pod spodem ma być w pełni nowoczesna, responsywna, z dopracowanymi animacjami.
Efekt "wow" dla nostalgików, a jednocześnie perfekcyjna obsługa mobile.

---

## 1. TYPOGRAFIA I FONTY

**Obecny stan:** Poppins (nowoczesny sans-serif)

**Propozycja:**
- Font główny: **VT323** (Google Fonts) — pikselowy monospace, idealny terminal look
- Font alternatywny: **Press Start 2P** do nagłówków/tytułu (opcjonalnie)
- Fallback: `"Courier New", monospace`
- Efekt "typewriter" — tekst tytułu wpisywany litera po literze z migającym kursorem `█`

---

## 2. KOLORYSTYKA

**Obecny stan:** Subtelne gradienty blue/gray, jasny/ciemny motyw

**Propozycja — paleta retro terminala:**
- **Tło:** Czarne (`#0a0a0a`) z subtlenym CRT scanline overlay
- **Tekst główny:** Zielony fosforyzujący (`#00ff41`) — klasyczny "Matrix green"
- **Tekst alternatywny:** Amber/pomarańczowy (`#ffb000`) — styl IBM terminal
- **Akcenty:** Cyan (`#00ffff`), Magenta (`#ff00ff`), Żółty (`#ffff00`)
- **Linki:** Cyan z podkreśleniem (jak w Lynx browser)
- **Hover:** Inwersja kolorów (czarny tekst na zielonym tle) — klasyczny terminal selection

**Motywy (zamiast light/dark):**
1. **Green Phosphor** — zielony na czarnym (domyślny)
2. **Amber Monitor** — pomarańczowy na czarnym
3. **Hacker Mode** — Matrix-style z "deszczem kodu"
4. **90s Web** — kolorowy jak GeoCities (teal tło, żółty tekst, gifowe separatory)

---

## 3. EFEKTY CRT / TERMINAL

**Propozycja efektów wizualnych:**
- **CRT Scanlines** — półprzezroczyste linie co 2-4px nałożone na cały ekran
- **CRT Curvature** — lekkie zaokrąglenie krawędzi ekranu (CSS border-radius + box-shadow)
- **Screen flicker** — subtelne migotanie luminancji (0.97-1.0 opacity, losowe interwały)
- **Chromatic aberration** — lekkie przesunięcie RGB na krawędziach tekstu (text-shadow)
- **Glow effect** — zielone/amber świecenie tekstu (text-shadow z blur)
- **Vignette** — przyciemnienie rogów ekranu
- **"Boot sequence"** — na wejście strona "bootuje się" jak stary komputer:
  ```
  BIOS v1.0 ... OK
  RAM check: 640K ... OK
  Loading ORZECH.ME v2.0 ...
  C:\> _
  ```

---

## 4. LAYOUT I STRUKTURA

**Obecny stan:** Centrowany card z przyciskami

**Propozycja:**
- Cała strona wygląda jak okno terminala/konsoli
- **Ramka "okna"** — nagłówek z paskiem tytułowym:
  ```
  ┌─────────────────────────────────────────┐
  │ ORZECH.ME Terminal v2.0          [-][□][×] │
  ├─────────────────────────────────────────┤
  │ C:\ORZECH> dir                            │
  │                                            │
  │  PAULINA.EXE    PAWEL.EXE                 │
  │  BLOG.LNK      KONTAKT.DAT               │
  │                                            │
  │ C:\ORZECH> _                               │
  └─────────────────────────────────────────┘
  ```
- Na mobile: pełnoekranowy terminal, bez ramki (oszczędność miejsca)
- Scrollowalny "output" z komendami

**Interaktywny element:**
- Pseudo-komendowa linia — użytkownik "widzi" jak komendy się wpisują
- Nawigacja jako komendy: `> open blog.lnk`, `> mail pawel@orzech.me`

---

## 5. ANIMACJE I EFEKTY

### 5a. Boot Sequence (na wejściu)
- Tekst pojawia się linia po linii jak w terminalu
- Efekt typewriter (litera po literze) na kluczowych komendach
- Migający kursor `█` podczas "wpisywania"
- Progressbar ASCII: `[████████░░░░░░] 56%`
- Po "załadowaniu" — reveal głównej treści

### 5b. Animacje ciągłe
- **Migający kursor** — klasyczne `█` co 530ms
- **Scanlines** — ruch scanline overlay (subtle)
- **Matrix rain** — w tle (opcjonalnie, w trybie "Hacker Mode")
- **Glitch effect** — losowe krótkie "glitche" tekstu co kilka sekund
- **Pulsujący glow** tekstu

### 5c. Animacje interakcji
- **Hover na linkach:** Inwersja kolorów z krótkim "glitch"
- **Click effect:** Krótki flash ekranu
- **Przejścia między motywami:** "Static/snow" TV effect na 300ms
- **Zmiana języka:** Tekst "się kasuje" i wpisuje na nowo

### 5d. Easter eggs
- Konami code → specjalny efekt
- Kliknięcie na 🌰 → ASCII art orzecha w terminalu
- Sekretna komenda w terminalu

---

## 6. MOBILE

**Propozycja:**
- Terminal zajmuje 100% ekranu (full-bleed)
- Ramka okna uproszczona do paska tytułowego
- Font size dobrany do czytelności na mobile (min 14px monospace)
- Touch-friendly: duże obszary klikalne (min 44x44px)
- Swipe do zmiany motywów
- Boot sequence skrócona na mobile (szybsza)
- Scanlines i CRT effects zoptymalizowane (mniejsza intensywność na mobile, GPU-friendly)
- Landscape mode: dwa "okna terminala" obok siebie

---

## 7. ELEMENTY 90s WEB

**Propozycja dodatkowych elementów retro:**
- **Visitor counter:** `You are visitor #001337` (ASCII art counter)
- **"Under construction" GIF** przy Stronie Pauliny (klasyczny żółto-czarny)
- **ASCII art** w tle lub jako separatory:
  ```
       _   _   _   _   _
      / \ / \ / \ / \ / \
     ( O | R | Z | E | C | H )
      \_/ \_/ \_/ \_/ \_/
  ```
- **Marquee effect** — scrollujący tekst u góry/dołu (CSS animation, nie `<marquee>`)
- **Blinking text** na ważnych elementach (z umiarem)
- **"Best viewed in Netscape Navigator"** badge w footerze
- **Guestbook** odwołanie (link do Mastodon jako "nowoczesna księga gości")
- **Hit counter** stylizowany na retro
- **Separator** z ASCII: `═══════════════════════`

---

## 8. DŹWIĘK (opcjonalnie)

- Klik klawiatury przy typewriter effect (Web Audio API, domyślnie wyłączony)
- "Dial-up modem" sound na boot sequence (opcjonalnie)
- Mute/unmute przycisk stylizowany na retro

---

## 9. ARCHITEKTURA TECHNICZNA

**Podejście:** Zostajemy przy single-file HTML (zero build tools) — to pasuje do retro vibe.

- Tailwind CSS (CDN) — zostaje jako utility framework
- Vanilla JS — żadnych frameworków, czysty retro
- CSS custom properties do motywów
- `@keyframes` dla wszystkich animacji
- `requestAnimationFrame` dla płynnych animacji
- Intersection Observer do lazy animations
- `prefers-reduced-motion` — wyłączenie animacji dla użytkowników z ustawieniem systemowym
- CSS `will-change` i `transform: translateZ(0)` dla GPU acceleration

---

## 10. PLAN PRACY — AGENTY

Implementacja rozdzielona na niezależnych agentów pracujących równolegle:

### Agent 1: CRT & Visual Effects
- Scanlines overlay (CSS)
- CRT curvature effect
- Vignette effect
- Screen flicker
- Chromatic aberration (text-shadow)
- Glow effects

### Agent 2: Boot Sequence & Typewriter
- Animacja bootowania
- Typewriter effect z kursorem
- ASCII progress bar
- Sekwencja "ładowania" systemu
- Reveal głównej treści po boot

### Agent 3: Layout & Terminal Window
- Ramka okna terminala (ASCII borders)
- Pasek tytułowy z przyciskami
- Responsywny layout terminala
- Pseudo-command line
- Nawigacja jako komendy
- Mobile adaptacja

### Agent 4: Kolorystyka & Motywy
- System motywów (Green/Amber/Hacker/90s Web)
- CSS custom properties
- Przejścia między motywami (static/snow effect)
- Przycisk przełączania motywów (retro style)

### Agent 5: Retro Elements & Easter Eggs
- Visitor counter
- "Under construction" element
- ASCII art
- Marquee text
- "Best viewed in..." badge
- Konami code easter egg
- 🌰 ASCII art easter egg

### Agent 6: Mobile & Performance
- Mobile-first responsive adjustments
- Touch interactions (swipe motywy)
- Performance optimization (will-change, GPU)
- `prefers-reduced-motion` support
- Testowanie na różnych rozmiarach ekranu
- Landscape mode support

---

## 11. KOLEJNOŚĆ IMPLEMENTACJI

1. **Faza 1:** Layout terminala + fonty + kolorystyka bazowa (Agent 3 + Agent 4)
2. **Faza 2:** CRT effects + boot sequence (Agent 1 + Agent 2)
3. **Faza 3:** Retro elements + easter eggs (Agent 5)
4. **Faza 4:** Mobile optimization + performance (Agent 6)
5. **Faza 5:** Polish & QA — wszystko dopięte na ostatni guzik

---

## 12. CO ZACHOWUJEMY

- Dwujęzyczność PL/EN
- Linki do emaili, bloga, strony Pauliny
- Feed z Mastodona
- Zegar z emoji
- Orzeszek 🌰 w footerze
- Link do GitHub
- SEO meta tags
- Accessibility (ARIA, semantic HTML)
- localStorage dla preferencji

---

## PODSUMOWANIE

Transformacja z eleganckiego minimalizmu w retro-terminalowy klimat lat 90. z:
- 4 motywami kolorystycznymi (zamiast light/dark)
- Efektami CRT (scanlines, curvature, flicker, glow)
- Boot sequence na wejściu
- Typewriter animations
- Interaktywną pseudo-konsolą
- Elementami retro web (visitor counter, under construction, marquee)
- Easter eggs
- Perfekcyjną obsługą mobile
- Pełną dostępnością i wydajnością
