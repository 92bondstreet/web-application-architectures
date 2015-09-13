# Exercice 6

> Rental modification

Some users want to modify the dates/distance for a given rental.

## New dates and distance

* Drivy computes the amount that was already paid by (or given to) each actor
* Using the new dates/distance, drivy re-computes the price of the rental, the "deductible reduction" amount, the commission, ...
* Drivy compute the delta amount [1] that must be debited/credited for each actor
* Each actor receives a debit/credit payment to settle his debt

What is the delta amounts for each actor?

[1] the delta amount is basically the difference between:
- the amount the actor owes (or is owed) *after* the modification
- the amount the actor has already paid (or been given) *before* the modification

```js
{
  "rentalModifications": [
    {
      "id": 1,
      "rentalId": "1-pb-92",
      "actions": [
        {
          "who": "driver",
          "type": ?,
          "amount": ?
        },
        {
          "who": "owner",
          "type": ?,
          "amount": ?
        },
        {
          "who": "insurance",
          "type": ?,
          "amount": ?
        },
        {
          "who": "assistance",
          "type": ?,
          "amount": ?
        },
        {
          "who": "drivy",
          "type": ?,
          "amount": ?
        }
      ]
    },
    {
      "id": 2,
      "rentalId": "3-sa-92",
      "actions": [
        {
          "who": "driver",
          "type": ?,
          "amount": ?
        },
        {
          "who": "owner",
          "type": ?,
          "amount": ?
        },
        {
          "who": "insurance",
          "type": ?,
          "amount": ?
        },
        {
          "who": "assistance",
          "type": ?,
          "amount": ?
        },
        {
          "who": "drivy",
          "type": ?,
          "amount": ?
        }
      ]
    }
  ]
}
```
