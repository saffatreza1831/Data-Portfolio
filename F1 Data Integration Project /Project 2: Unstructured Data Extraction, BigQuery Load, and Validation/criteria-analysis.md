## Criteria 1
OpenF1, Ergast, Historical Car, Wikipedia (of each race track)

## Criteria 2
Wikipedia pages were converted to pdf form for each race track for the 2023 and 2024 season.

## Critera 3
drivers_openf1, ergast_drivers, ergast_lap_times, eragast_races, laps, meetings, pit, qualifying_results, race_results, sessions, historical_cars, and racerpedia.

## Criteria 4
Info across datasets has functional dependency. For example, race info is consistent, whether it includes driver, location, date, time, etc. If one row says the Spanish Grand Prix has a country code of ESP, this will be conistent within the dataset as well as the other tables. This applies to all of the data. The data is not randomly generated and is pulled from multiple reputable APIs and datasets.

## Criteria 5
Date information should be DATETIME or DATE format but only works as STRING. These columns will require adjusting later.

## Critera 6
drivers_openf1 table has null values. Other tables also have null values.

## Criteria 7
ergast_races has date and time in one column and the other ergast data has them separated. We want to separate that column to match the other ergast data for easier analysis

## Criteria 8
laps table columns segments_sector_1, segments_sector_2, segments_sector_3 all have list values in them. These indicate 'mini-sectors' and the values are mapped to a certain value

## Criteria 9
Ergast data and openf1 have very similar data but different identifier systems. For example, drivers_openf1 uses driver_number as the primary key while ergast_drivers uses driver_id as the primary key. Both tables are necessary for other tables to make sense in our ERD.

## Criteria 10
Many tables carry the meeting_key, however, this is unnecessary since the meetings table is connected to sessions which has a session_key. This session_key is more unique for the other tables, therefore making it redundant to have both meeting_key and session_key in all of the tables that use session_key.
