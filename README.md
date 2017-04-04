# Hadoop1
Hadoop1


This project aim is to  build mapper and reducer scripts which analyzes data from file stored in  /data/nyc/nyc-traffic.csv.

**Run the following commands in order to run the program:**<br>
1)Clone the program : git clone https://github.uc.edu/suggusi/Hadoop1/tree/master <br>
2)Run the below command in order to retrieve the log: <br>
hadoop jar /opt/hadoop-2.7.1/share/hadoop/tools/lib/hadoop-streaming-2.7.1.jar -file /home/suggusi/mapper.py    -mapper /home/suggusi/mapper.py -file /home/suggusi/reducer.py   -reducer /home/suggusi/reducer.py -input /data/nyc/nyc-traffic.csv  -output /user/suggusi/homework4

3)Run the following program to see the output: <br>
hadoop fs -cat /user/suggusi/homework4/*

**OUTPUT OBTAINED:**<br>
AMBULANCE 3713<br>
BICYCLE 24153 <br>
BUS     25871<br>
FIRE TRUCK      1333<br>
LARGE COM VEH(6 OR MORE TIRES)  27981<br>
LIVERY VEHICLE  17775<br>
MOTORCYCLE      10029<br>
OTHER   51360 <br>
PASSENGER VEHICLE       1005161 <br>
PEDICAB 123<br>
PICK-UP TRUCK   26281<br>
SCOOTER 534<br>
SMALL COM VEH(4 TIRES)  30048 <br>
SPORT UTILITY / STATION WAGON   363210 <br>
TAXI    63892 <br>
UNKNOWN 105481 <br>
VAN     51666 <br>

This dataser contains 1.01 M rows and 29 columns.
The columns which we consider for this project is:
1)VEHICLE TYPE CODE 1
2)VEHICLE TYPE CODE 2
3)VEHICLE TYPE CODE 3
4)VEHICLE TYPE CODE 4
5)VEHICLE TYPE CODE 5

From the above columns, we yield summary counts for each vehicle that describe the total count, per vehicle type, that the vehicle type was involved in an incident. If the same  type of vehicle was involved more than once in an incident, we count the vehicle twice for the purpose of the summary statistic.



