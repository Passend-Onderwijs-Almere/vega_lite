### Aantal leerlingen per schooljaar

Onderstaande Vega‑Lite visualisatie toont het **aantal leerlingen per schooljaar**.  
Op de x-as staat het schooljaar en op de y-as het totaal aantal leerlingen, berekend als een **count** van het leerlingnummer.

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
