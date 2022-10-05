## FLiP-Current22-LetsMonitorAllTheThings

<img src="https://raw.githubusercontent.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/main/monitor.jpeg" width="366" height="206" />

### Let's Monitor The Conditions at the Conference

#### Session Time:  11:15 am - 12:00 pm 

#### Session Date:  Wednesday, 5 October 2022 

#### Session Type:  In-Person 

#### Location:  Ballroom G


#### Session Description:

At home, I monitor the temperature, humidity, gas levels, ozone, air quality, and other features around my desk. Let's bring this to the different spots around the conference including lunch tables, vendor booths, hotel rooms, and more. I need to know about these readings now, not when I get back home from the conference. We need to get these sensor readings immediately in case we need to turn on a fan or move to another area. We will also see if my talk produces a lot of hot air!? My setup is pretty simple, a raspberry pi, a breakout garden sensor mount, and as many sensors as I am willing to fly to Austin. The software stack is Python and Java, Apache Pulsar, MQTT, HTML, JQuery, and Apache Kafka.

![Easy?](https://github.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/blob/main/lookatmeter.jpg?raw=true)


#### 0️⃣  How to Monitor a Conference (Or Anywhere Really)

Here is your menu of tasty monitoring items, some need devices, add-ons, antennas, sensors and some just some code.   I bounce around between Python, Java, SQL, JavaScript, CSS and Low Code with Apache NiFi.   Pick any 3 for mega monitoring.

It worked in San Francisco....  It can work in Austin.

<img src="https://raw.githubusercontent.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/main/2022-08-18_12-09-27_912.jpeg" width="586" height="439">

You do not need some giant cluster to get started.   You can have a Raspberry Pi, a Laptop, a Jetson Nano or some old Linux machine.

![Server](https://user-images.githubusercontent.com/18673814/192906050-1b095050-d599-41dd-8991-b1e5d53e0028.png)




##### 1️⃣  Air Quality

Let's use the new Spring to read a ton of Air Quality data for the area.  Send to Pulsar via All the Protocols?~!!  
This is a REST feed, no extra equipment needed.

* https://github.com/tspannhw/spring-pulsar-airquality
* https://github.com/tspannhw/airquality
* https://github.com/tspannhw/airquality-kafka-consumer
* https://github.com/tspannhw/airquality-mqtt-consumer
* https://github.com/tspannhw/FLiPN-AirQuality-REST
* https://medium.com/@tspann/timeplus-plus-pulsar-is-pure-perfection-a1a4d253031f
* https://github.com/tspannhw/pulsar-airquality-timeplus
* https://github.com/tspannhw/FLiPN-AirQuality-Checks
* https://github.com/tspannhw/airquality-datastore
* https://github.com/tspannhw/airquality-amqp-consumer

![Protocols](https://github.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/blob/main/catallthepulsars.jpg?raw=true)



##### 2️⃣  Weather

Let's use Apache NiFi to read all the US weather and sent it to Pulsar.

* https://medium.com/@tspann/parsing-weather-feeds-to-add-to-real-time-streams-ec5ecc2849fb
* https://github.com/tspannhw/pulsar-weather-function
* https://www.youtube.com/watch?v=2PO15zb7irg

![weather](https://user-images.githubusercontent.com/18673814/192903489-9f15c4cf-4c98-4048-a2d5-b44f6c8e2bf3.png)



##### 3️⃣ Temperature, Barometric Pressure, Humidity Near My Shirt

Let's Monitor Temperature, Barometric Pressure and Humidity very local via small sensor and sent out via MQTT 

https://github.com/tspannhw/pulsar-adafruit-funhouse

<img src="https://raw.githubusercontent.com/tspannhw/pulsar-adafruit-funhouse/main/IMG-6527.jpg" width="300" height="300" />




##### 4️⃣ Local Air Quality

With a more powerful Raspberry Pi, I can monitor even more local items.

* https://github.com/tspannhw/FLiP-Pi-DeltaLake-Thermal
* https://medium.com/@tspann/apache-pulsar-edge-iot-applications-with-python-for-tvoc-2424a79a8ada

<img src="https://raw.githubusercontent.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/main/2022-09-14_10-56-20_079.jpeg" width="586" height="498">




##### 5️⃣  Let's consume all the conference tweets

I am looking at the new Twitter Java SDK v2 to sent to pulsar.

* https://community.cloudera.com/t5/Community-Articles/Parsing-Any-Document-with-Apache-NiFi-1-5-with-Apache-Tika/ta-p/247672
* https://www.datainmotion.dev/2020/04/streaming-data-with-cloudera-data-flow.html

Twitter Terms:    #Current22 #KafkaSummit

````
Twitter API v2 - setup a rule

curl "https://api.twitter.com/2/tweets/search/stream/rules" -H "Authorization: Bearer $BEARER_TOKEN"
{"data":[{"id":"1575560079515983872","value":" #kafkasummit OR #current22  OR retweets_of:PaasDev","tag":"conferencetags"}],"meta":{"sent":"2022-09-30T16:13:12.528Z","result_count":1}}
````



##### 6️⃣  Planes, Trains and Autos.... Actually just planes.

ADSB-Y transponders from planes can be read with a simple USB adapter and antenna attached to a Raspberry Pi.

* https://dzone.com/articles/tracking-aircraft-in-real-time-with-apache-pulsar
* https://github.com/tspannhw/FLiP-Py-ADS-B
* https://github.com/tspannhw/pulsar-adsb-function
* https://medium.com/@tspann/tracking-aircraft-in-real-time-with-open-source-554124125011

![Planes](https://github.com/tspannhw/FLiP-Py-ADS-B/raw/main/airmap.png)



#### 7️⃣  Let's Monitor the Electric We Use Today

Required:   HS-110 TP-Link Monitoring Device, Python 3, Apache Pulsar
Optional:   Apache Spark SQL, Trino, Apache Flink SQL, Pulsar Functions, InfluxDB

* https://github.com/tspannhw/FLiP-Py-Energy
* https://medium.com/@tspann/lets-monitor-our-own-energy-usage-e8feefd5a3b1

![EnergizeMe](https://github.com/tspannhw/FLiP-Py-Energy/raw/main/flinkeletricmax.png)

![FriendsAreElectric](https://github.com/tspannhw/FLiP-Py-Energy/blob/main/dashboard.png)




##### 8️⃣  I have also monitored these data sources:

![AllTheThings](https://github.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/blob/main/monitorallthethings.jpg?raw=true)

* Transit Feeds https://github.com/tspannhw/FLiP-Transit
* Subways, Trains and Buses
* Live Traffic Cameras
* Local Cameras
* Thermal Camera
* License Plates
* GPS Data
* NFTs
* BitCoin, Cryptocurrency
* Stock Data
* Any data, any time, many protocols, really fast



##### 9️⃣ Display Live Streaming Data The Easy Open Source Way

**Required:  WebSockets, Plain HTML, CSS, JavaScript, Apache Pulsar, Topics of Data**

* https://medium.com/@tspann/using-apache-pulsar-websockets-for-real-time-messaging-in-front-end-applications-cf0ac2d80d10



#### 1️⃣0️⃣ Join the Streams!!!!

With Flink SQL it's easy.

* https://github.com/tspannhw/FLiP-Py-ADS-B/blob/main/join.md
* https://github.com/tspannhw/pulsar-weather-function


````
CREATE CATALOG pulsar WITH (
   'type' = 'pulsar',
   'service-url' = 'pulsar://pulsar1:6650',
   'admin-url' = 'http://pulsar1:8080',
   'format' = 'json'
);


select COALESCE(location,station_id,'?') || ' ' || cast(lat as string) || ',' || cast(lon as string) as PlaneLocation, 
       cast(latitude  as string)|| ',' || cast(longitude as string) as WeatherLocation,
       COALESCE(flight,'-','-') || ' * ' || COALESCE(hex, '-','-') as FlightNum, 
       cast(alt_baro  as string) || ' / ' ||  cast(alt_geom as string) as Altitude, 
       gs as Speed,
       temperature_string || weather as Weather, 
       mach, pressure_string, dewpoint_string, heat_index_string, wind_string, baro_rate,
       NOW() as now
FROM aircraft /*+ OPTIONS('scan.startup.mode' = 'earliest') */,
aircraftweather /*+ OPTIONS('scan.startup.mode' = 'earliest') */ 
WHERE (aircraft.lat > aircraftweather.latitude - 0.1) 
and (aircraft.lat < aircraftweather.latitude + 0.1)
and (aircraft.lon < aircraftweather.longitude + 0.1) 
and (aircraft.lon > aircraftweather.longitude - 0.1);


````

![SQL](https://github.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/blob/main/ghostbusters.jpg?raw=true)

We can run lots of queries with Pulsar SQL (Trino/Presto) or Spark SQL as well.

![SQL](https://github.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/blob/main/queryingpulsar.jpg?raw=true)

You can do a lot of different SQL against Pulsar since we have schemas on our data.

````
select avg(`current`) as AvgCurrent, 
       max(voltage) as MaxVoltage,
       max(`power`) as MaxPower,
       model
from electric
group by model;

select max(alt_baro) as MaxAltitudeFeet, min(alt_baro) as MinAltitudeFeet, avg(alt_baro) as AvgAltitudeFeet,
       max(alt_geom) as MaxGAltitudeFeet, min(alt_geom) as MinGAltitudeFeet, avg(alt_geom) as AvgGAltitudeFeet,
       max(gs) as MaxGroundSpeed, min(gs) as MinGroundSpeed, avg(gs) as AvgGroundSpeed, 
       count(alt_baro) as RowCount, 
       hex as ICAO, flight as IDENT
from aircraft 
group by flight, hex;

````




##



### See Me in Person and Walk Through the Code

Real-Time Data Streaming Meetup with Aerospike

Mon, Oct 3, 2022, 6:30 PM | Meetup

https://www.meetup.com/new-york-city-apache-pulsar-meetup/events/288501432/

Inside the Current Event 2022 Conference.  Stop by booth G8 to learn more about Pulsar features 


### References

* https://2022.currentevent.io/website/39543/speakers/
* https://2022.currentevent.io/website/39543/agenda/
* https://github.com/tspannhw/FLiPStackWeekly
* https://github.com/tspannhw/FLiPN-DEVNEXUS-2022
* https://www.flipstack.dev/
* https://dzone.com/users/297029/bunkertor.html
* https://github.com/riferrei/is-using-kop-a-good-idea

### See Me For Some Stickers That Are Both About Data and Cats

![Cats](https://github.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/blob/main/dataAndCat.jpg?raw=true)
