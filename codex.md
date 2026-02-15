# Codex.md

Praktický průvodce projektem pro člověka i LLM.

## 1) Co tento projekt dělá

- Jednostránková kalkulačka v HTML.
- Přepočítává objem `m³` na cenu.
- `1 m³ = 9 775 Kč` (bez DPH).
- `DPH = 21 %` (dopočet ceny s DPH).

## 2) Kde co je

- `kalkulacka.html`: celý projekt (HTML + CSS + JavaScript v jednom souboru).
- `codex.md`: tento orientační dokument.

## 3) Klíčové chování aplikace

- Vstup `Velikost v m³` přijímá český i anglický desetinný zápis (`2,5` i `2.5`).
- Tlačítka `+` a `−` mění hodnotu po `10 m³`.
- Hodnota nikdy nejde pod `0`.
- Výstupy se přepočítávají okamžitě.
- `Výsledek bez DPH`.
- `DPH + 21 %`.
- Částky se formátují jako měna `CZK`.

## 4) Důležité konstanty (v JS)

V souboru `kalkulacka.html`:

- `RATE = 9775`
- `VAT_MULTIPLIER = 1.21`
- `STEP = 10`

Pokud měníš obchodní logiku, upravuj tyto konstanty jako první.

## 5) Jak projekt upravovat bezpečně

1. Zachovej dva výstupy: bez DPH a s DPH.
2. Zachovej formátování měny pro české prostředí (`cs-CZ`, `CZK`).
3. Zachovej podporu desetinné čárky.
4. Otestuj ruční zadání hodnoty (např. `2,5`).
5. Otestuj klikání na `+` a `−`.
6. Otestuj hraniční stav `0`.

## 6) Rychlé testovací hodnoty

- `1 m³` -> bez DPH `9 775 Kč`, s DPH `11 827,75 Kč`
- `10 m³` -> bez DPH `97 750 Kč`, s DPH `118 277,50 Kč`

## 7) Doporučení pro další rozvoj

- Přidat tlačítko `Vymazat`.
- Přidat dlouhý stisk `+`/`−` pro rychlé přičítání.
- Oddělit CSS a JS do samostatných souborů při větším rozsahu.
