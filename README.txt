QUICKBITE FOOD DELIVERY INSIGHT — SYNTHETIC DATASET

These five CSVs are synthetic and generated for practice with the Food Delivery Insight assessment. They are not real QuickBite or Zomato records.

FILES / KEYS
- orders.csv: order details. Key: order_id.
- riders.csv: rider master data. Key: rider_id.
- routes.csv: distance, traffic, zone, weather_id. Join orders on order_id.
- weather.csv: weather observations. Join routes on weather_id.
- delivery.csv: pickup/delivery timestamps, status and rider_id. Join orders on order_id and riders on rider_id.

ROW COUNTS
- orders.csv: 2,012 (2,000 orders + 12 intentional duplicate rows)
- routes.csv: 2,000
- weather.csv: 2,000
- delivery.csv: 2,000
- riders.csv: 120 (each rider can serve multiple orders)

QUALITY ISSUES INTENTIONALLY INCLUDED
- Duplicate order records in orders.csv
- Inconsistent zone capitalization/spelling
- Missing pickup timestamps and missing weather readings
- Missing delivered timestamps for cancelled/failed orders
- A few negative timestamp durations

SUGGESTED JOINS
1. Deduplicate orders by order_id.
2. orders.order_id = routes.order_id
3. routes.weather_id = weather.weather_id
4. orders.order_id = delivery.order_id
5. delivery.rider_id = riders.rider_id

FEATURES TO ENGINEER
- pickup_duration_min = pickup_timestamp - order_timestamp
- delivery_duration_min = delivered_timestamp - pickup_timestamp
- order_to_delivery_min = delivered_timestamp - order_timestamp
- order_hour / peak_period from order_timestamp

Do not treat missing timestamps or negative durations as valid. Decide and document a consistent cleaning rule before analysis.
