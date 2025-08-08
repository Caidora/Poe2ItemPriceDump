
# Poe2ItemPriceDump

A comprehensive dataset containing historical price logs collected by [poe2scout.com](https://poe2scout.com).

## Data Description

The data is stored in `hardcore_logs.csv` and `standard_logs.csv`. These files contain detailed price tracking information for items in Path of Exile 2.

### Fields Explained

Data logs are formatted differently based on the league they were collected in.

#### **poe2_league1**

- **price**: The raw price value of the item.
- **currency_string_id**: The currency type used for the price (e.g., "exalted", "divine").
- **nominal_price**: The normalized price converted to the equivalent value in **Exalted Orbs** at the time of logging.
  - *Example:* If an item cost 50 Divine Orbs, the `nominal_price` would be the equivalent value in Exalted Orbs based on the exchange rate at that time.
  - *Note:* Some early logs may be missing this normalization.

#### **poe2_dawnOfTheHunt**

- **price**: The value of the item, presented in **Exalted Orbs**.

## Notes for each league

### **poe2_league1**

This league's early logs may have incomplete normalization data.

### **poe2_dawnOfTheHunt**

This league saw a change in the data schema. The format is different from previous leagues but will be more consistent going forward.

---
## Quantity Data

The `quantity` field indicates an item's relative scarcity over time. While useful for tracking trends in availability, the absolute values should not be considered exact representations, especially for non-currency items.