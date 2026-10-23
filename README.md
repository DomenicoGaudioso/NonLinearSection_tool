# NonLinearSection_tool

Sito demo / landing page di **[SectionTool](https://github.com/DomenicoGaudioso/SectionTool)** (StrutturaNL) — il motore per l'analisi **non lineare** di sezioni in calcestruzzo armato, c.a. precompresso, acciaio e miste.

👉 **[Guarda la Demo Interattiva Web](https://domenicogaudioso.github.io/NonLinearSection_tool/)** 👈

La pagina presenta il tool di verifica delle sezioni in continuità con il [sito personale](https://domenicogaudioso.github.io/DomenicoGaudioso/): prima una sezione calcolata dal motore, poi la parte tecnica.

## Contenuti del sito

- **Esploratore interattivo**: sezione, dominio N-M e curva momento-curvatura di un pilastro 400 x 600 (C30/37, B450C, NTC 2018) calcolati con il motore dell'app per 13 valori dello sforzo normale; i dati sono incorporati in `index.html`.
- **Parte tecnica**: convenzioni, materiali, sezione e input, verifiche SLU con i riferimenti normativi, esercizio, elaborazioni, relazione Word, integrazioni (feagent, IA, API) e modi per ottenere l'app.

## Funzionalità del motore (SectionTool / StrutturaNL)

- **Legami costitutivi non lineari**: parabola-rettangolo EC2 e DIN 1045 (valori medi o di progetto), acciaio con incrudimento, leggi lineari elastiche.
- **Multi-materiale e getti successivi**: ogni getto ha geometria e legge propria, con predeformazioni (Vordehnung); trefoli di precompressione e barre con legge indipendente.
- **Fessurazione e viscosità**: tension stiffening (Mitwirkung) e viscosità semplificata con φ.
- **Analisi uniassiale e biassiale**: curva M-χ, dominio N-M, superficie N-Mx-My, verifica del punto.
- **UI Streamlit** (`strutturanl/ui/app.py`) con import delle sezioni da file; grafici matplotlib/plotly.

## Struttura

- `index.html` — pagina autoconsistente (CSS e JavaScript inline, grafici SVG disegnati dallo script), nessuna build richiesta.
- `assets/` — icone di CivilBox e feagent.

## Sorgente

Tutto il calcolo vive in **[DomenicoGaudioso/SectionTool](https://github.com/DomenicoGaudioso/SectionTool)** (`strutturanl/`: analisi, materiali, sezioni, grafici, telaio, ui).
