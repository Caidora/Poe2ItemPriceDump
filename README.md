# Poe2ItemPriceDump

A comprehensive dataset containing historical price logs collected by [poe2scout.com](https://poe2scout.com) through the 0.1.0 Standard and Hardcore Leagues.

## Data Description

The data is stored in `hardcore_logs.csv` and `standard_logs.csv` and contains detailed price tracking information for items in Path of Exile 2.

### Fields Explanation

- **price**: The raw price value of the item
- **currency_string_id**: The currency type used for the price (e.g., "exalted", "divine")
- **nominal_price**: Normalized price converted to equivalent exalted orb value at the time of logging
  - Example: If an item costs 50 Divine Orbs, the nominal_price would be the equivalent value in Exalted Orbs based on the exchange rate at that time
  - Note: Some early logs may be missing this normalization

### League Identifiers
- **pbestandard1**: Standard League data
- **pbehardcore1**: Hardcore League data

### Quantity Data
The quantity field indicates relative item scarcity over time. While useful for tracking trends in item availability, the absolute values should not be taken as exact representations, especially for non-currency items. This metric will be improved in future leagues.

## Notes
- All data is collected through poe2scout's price logging system
- Historical price trends can be analyzed across both Standard and Hardcore leagues
- Early logs may have incomplete normalization data
