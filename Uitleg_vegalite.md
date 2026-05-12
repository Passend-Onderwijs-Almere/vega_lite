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

