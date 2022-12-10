# F1Project : For MAD2502
## Weekend Compiler Dataframe guide
### Notes on Packages:
weekendCompiler uses fastf1 api for data scraping, pd for dataframe manipulation, datetime for date changing, and dfply for data cleaning.

For those unaware, dfply is a package that mimics the "dplyr" package from R. I used this because I'm most familiar with cleaning data using R, but I wanted to keep everything in python.

### Meaning for each dataframe variable (ripped from fastf1 documentation):
1. Index: unnecessary but I can't remove it
2. Driver (str): Driver number
3. LapTime (pandas.Timedelta): Lap time of the last finished lap (the lap in this row)
4. NumberOfLaps (int): Number of laps driven by this driver including the lap in this row
5. NumberOfPitStops (int): Number of pit stops of this driver
6. Sector1/2/3Time (pandas.Timedelta): Sector times (one column for each sector time)
7. SpeedI1/I2/FL/ST: Speed trap speeds; FL is speed at the finish line; I1 and I2 are speed traps in sector 1 and 2 respectively; ST maybe a speed trap on the longest straight
8. Compound (str): Tire compound
9. New: New (bool): Whether the tire was new when fitted
10. AirTemp (float): Air temperature [°C]
11. Humidity (float): Relative humidity [%]
12. Pressure (float): Air pressure [mbar]
13. Rainfall (bool): Shows if there is rainfall
14. TrackTemp (float): Track temperature [°C]
15. WindSpeed (float): Wind speed [km/h]
16. Practice (int): Which practice session lap took place in
17. Grand Prix: Which grand prix entry corresponds too

Note that Qualifying prefix references the data during the driver's best qualifying lap.

