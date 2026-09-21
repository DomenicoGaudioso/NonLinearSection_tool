# NonLinearSection_tool# NonLinear Section

Il framework definitivo per l'analisi e la verifica non lineare di sezioni in Calcestruzzo Armato (CA), Acciaio e Miste.

👉 **[Guarda la Demo Interattiva Web](https://domenicogaudioso.github.io/NonLinearSection_tool/)** 👈

## Funzionalità
- **Legami Costitutivi Non Lineari**: Modelli parabola-rettangolo, Mander (confinamento) ed elasto-plastico incrudente.
- **Dominio M-N 3D e 2D**: Generazione automatica di domini di interazione per pressoflessione deviata e retta.
- **Analisi Momento-Curvatura (M-χ)**: Calcolo della duttilità e della curvatura ultima.
- **CLI Integrata**: Scripting e automazione per verifiche massive.

## Installazione
```bash
npm install -g nonlinear-section
nls init --project "capannone-industriale"
nls add-concrete --grade C30/37 --model mander
nls add-rebar --type B450C --cover 40mm
nls run analysis --type m-curvature --target-ductility 4
