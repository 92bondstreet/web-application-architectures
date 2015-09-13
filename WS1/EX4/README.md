# Exercice 4

> The famous deductible

In case of an accident, drivy applies a 800€ euros deductible.

The driver can reduce the deductible amount from 800€ to 150€ with a `deductible option` for a few more euros per day.

## The deductible

The driver is charged an additional 4€/day when he chooses the "deductible reduction" option.

**The additional charge goes to drivy, not to the car owner.**

```js
{
  "rentals": [
    {
      "id": "paul-bismuth",
      "price": ?,
      "commission": {
        "insurance": ?,
        "assistance": ?,
        "drivy": ?
      },
      "options":{
        "deductibleReduction": ?
      }
    },
    {
      "id": "rebecca-solanas",
      "price": ?,
      "commission": {
        "insurance": ?,
        "assistance": ?,
        "drivy": ?
      },
      "options":{
        "deductibleReduction": ?
      }
    },
    {
      "id": "sami-ameziane",
      "price": ?,
      "commission": {
        "insurance": ?,
        "assistance": ?,
        "drivy": ?
      },
      "options":{
        "deductibleReduction": ?
      }
    }
  ]
}
```
