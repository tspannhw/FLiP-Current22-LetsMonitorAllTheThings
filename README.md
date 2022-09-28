## FLiP-Current22-LetsMonitorAllTheThings

<img src="https://raw.githubusercontent.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/main/monitor.jpeg" width="366" height="206" />

### Let's Monitor The Conditions at the Conference

#### Session Time:  11:15 am - 12:00 pm 

#### Session Date:  Wednesday, 5 October 2022 

#### Session Type:  In-Person 

#### Location:  Ballroom G


#### Session Description:

At home, I monitor the temperature, humidity, gas levels, ozone, air quality, and other features around my desk. Let's bring this to the different spots around the conference including lunch tables, vendor booths, hotel rooms, and more. I need to know about these readings now, not when I get back home from the conference. We need to get these sensor readings immediately in case we need to turn on a fan or move to another area. We will also see if my talk produces a lot of hot air!? My setup is pretty simple, a raspberry pi, a breakout garden sensor mount, and as many sensors as I am willing to fly to Austin. The software stack is Python and Java, Apache Pulsar, MQTT, HTML, JQuery, and Apache Kafka.


#### 0️⃣  How to Monitor a Conference (Or Anywhere Really)

Here is your menu of tasty monitoring items, some need devices, add-ons, antennas, sensors and some just some code.   I bounce around between Python, Java, SQL, JavaScript, CSS and Low Code with Apache NiFi.   Pick any 3 for mega monitoring.



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

##### 2️⃣  Weather

Let's use Apache NiFi to read all the US weather and sent it to Pulsar.

* https://medium.com/@tspann/parsing-weather-feeds-to-add-to-real-time-streams-ec5ecc2849fb
* https://github.com/tspannhw/pulsar-weather-function

![weather](https://user-images.githubusercontent.com/18673814/192903489-9f15c4cf-4c98-4048-a2d5-b44f6c8e2bf3.png)



##### 3️⃣ Temperature, Barometric Pressure, Humidity Near My Shirt

Let's Monitor Temperature, Barometric Pressure and Humidity very local via small sensor and sent out via MQTT 

https://github.com/tspannhw/pulsar-adafruit-funhouse

<img src="https://raw.githubusercontent.com/tspannhw/pulsar-adafruit-funhouse/main/IMG-6527.jpg" width="300" height="300" />


##### 4️⃣ Local Air Quality

With a more powerful Raspberry Pi, I can monitor even more local items.

* https://github.com/tspannhw/FLiP-Pi-DeltaLake-Thermal
* https://medium.com/@tspann/apache-pulsar-edge-iot-applications-with-python-for-tvoc-2424a79a8ada


##### 5️⃣  Let's consume all the conference tweets


##### 6️⃣  Planes, Trains and Autos.... Actually just planes.

ADSB-Y transponders from planes can be read with a simple USB adapter and antenna attached to a Raspberry Pi.

* https://dzone.com/articles/tracking-aircraft-in-real-time-with-apache-pulsar
* https://github.com/tspannhw/FLiP-Py-ADS-B
* https://github.com/tspannhw/pulsar-adsb-function
* https://medium.com/@tspann/tracking-aircraft-in-real-time-with-open-source-554124125011



#### 7️⃣  Let's Monitor the Electric We Use Today

Required:   HS-110 TP-Link Monitoring Device, Python 3, Apache Pulsar
Optional:   Apache Spark SQL, Trino, Apache Flink SQL, Pulsar Functions, InfluxDB

* https://github.com/tspannhw/FLiP-Py-Energy
* https://medium.com/@tspann/lets-monitor-our-own-energy-usage-e8feefd5a3b1

![EnergizeMe](https://github.com/tspannhw/FLiP-Py-Energy/raw/main/flinkeletricmax.png)

![FriendsAreElectric](https://github.com/tspannhw/FLiP-Py-Energy/blob/main/dashboard.png)


##### 8️⃣  We could also monitor with ease:

* Transit Feeds https://github.com/tspannhw/FLiP-Transit
* Subways, Trains and Buses
* Live Traffic Cameras

##### 9️⃣ Display Live Streaming Data The Easy Open Source Way

**Required:  WebSockets, Plain HTML, CSS, JavaScript, Apache Pulsar, Topics of Data**

* https://medium.com/@tspann/using-apache-pulsar-websockets-for-real-time-messaging-in-front-end-applications-cf0ac2d80d10




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

