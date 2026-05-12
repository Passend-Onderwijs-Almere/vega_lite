### Uitleg van de Vega‑Lite visualisatie

**Mark**  
De `mark` geeft aan welk type grafiek wordt gebruikt.  
In deze code is `mark: "bar"` gekozen, wat betekent dat de data wordt weergegeven als een **staafdiagram**.

**Encoding**  
De `encoding` beschrijft hoe de data wordt gekoppeld aan visuele onderdelen van de grafiek, zoals de assen.  
Hier worden de x‑ en y‑as gedefinieerd op basis van velden uit de dataset.

**X-as**  
De x‑as gebruikt het veld `schooljaar` met het type `nominal`.  
Dit zorgt ervoor dat elk schooljaar als een **categorie** apart op de horizontale as wordt weergegeven.

**Y-as**  
De y‑as telt (`aggregate: "count"`) het aantal waarden van `lokaal_leerlingnummer`.  
Het type is `quantitative`, omdat het resultaat een **numerieke waarde** is.  
Elke staaf laat zo zien hoeveel leerlingen er per schooljaar zijn.

```json
{
  "$schema": "https://vega.github.io/schema/vega-lite/v5.json",
  "data": { "name": "dataset" },
  "mark": "bar",
  "encoding": {
    "x": {
      "field": "schooljaar",
      "type": "nominal"
    },
    "y": {
      "aggregate": "count",
      "field": "lokaal_leerlingnummer",
      "type": "quantitative"
    }
  }
}
