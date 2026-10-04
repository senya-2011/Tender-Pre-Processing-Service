# Tender Pre-Processing Service — ТЗ (Typst + Mermaid)

Требуется: `typst` и `mmdc` (mermaid-cli).

    make diagrams   # diagrams/*.mmd -> build/diagrams/*.svg
    make pdf        # диаграммы + typst compile -> build/spec.pdf
    make watch      # typst watch (диаграммы пересобирайте командой make diagrams)
    make clean

Структура: `main.typ` — документ, `diagrams/` — исходники Mermaid, `mermaid-config.json` — настройки
(`htmlLabels: false` обязателен, иначе Typst теряет подписи в SVG).
