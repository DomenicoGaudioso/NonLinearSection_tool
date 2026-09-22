# NonLinearSection_tool

Sito demo / landing page di **[SectionTool](https://github.com/DomenicoGaudioso/SectionTool)** (StrutturaNL) — il motore per l'analisi **non lineare** di sezioni in calcestruzzo armato, c.a. precompresso, acciaio e miste.

👉 **[Guarda la Demo Interattiva Web](https://domenicogaudioso.github.io/NonLinearSection_tool/)** 👈

Il sito racconta, con simulazioni animate live (stile feagent), il funzionamento del tool di verifica delle sezioni.

## Contenuti del sito

- **CASE 01 · Sezione & materiali** — geometria arbitraria (poligoni con fori, cerchi/anelli, gruppi di barre, trefoli, getti successivi) e legami σ-ε non lineari: parabola-rettangolo EC2/DIN 1045, acciaio elastoplastico con incrudimento, tension stiffening.
- **CASE 02 · Momento-curvatura** — piano delle deformazioni ε = ε₀ + κ·y in equilibrio con (N, M): curva M-χ con fessurazione, snervamento, ramo ultimo e curvatura ultima per la duttilità.
- **CASE 03 · Domini di interazione** — dominio N-M allo SLU con diagramma limite EC2, superficie biassiale N-Mx-My, verifica del punto con Grenzdehnungen.
- Flusso di calcolo (geometria → materiali → equilibrio → output), feature grid e guida all'installazione.

## Funzionalità del motore (SectionTool / StrutturaNL)

- **Legami costitutivi non lineari**: parabola-rettangolo EC2 e DIN 1045 (valori medi o di progetto), acciaio con incrudimento, leggi lineari elastiche.
- **Multi-materiale e getti successivi**: ogni getto ha geometria e legge propria, con predeformazioni (Vordehnung); trefoli di precompressione e barre con legge indipendente.
- **Fessurazione e viscosità**: tension stiffening (Mitwirkung) e viscosità semplificata con φ.
- **Analisi uniassiale e biassiale**: curva M-χ, dominio N-M, superficie N-Mx-My, verifica del punto.
- **UI Streamlit** (`strutturanl/ui/app.py`) con import delle sezioni da file; grafici matplotlib/plotly.

## Struttura

- `index.html` — pagina completa e autoconsistente (CSS + JS inline, animazioni canvas 2D + vista 3D three.js), nessuna build richiesta.

## Sorgente

Tutto il calcolo vive in **[DomenicoGaudioso/SectionTool](https://github.com/DomenicoGaudioso/SectionTool)** (`strutturanl/`: analisi, materiali, sezioni, grafici, telaio, ui).
