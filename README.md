## FLiP-Current22-LetsMonitorAllTheThings

<img src="https://raw.githubusercontent.com/tspannhw/FLiP-Current22-LetsMonitorAllTheThings/main/monitor.jpeg" width="366" height="206" />

### Let's Monitor The Conditions at the Conference

#### Session Time:  11:15 am - 12:00 pm 

#### Session Date:  Wednesday, 5 October 2022 

#### Session Type:  In-Person 

#### Location:  Ballroom G


#### Session Description:

At home, I monitor the temperature, humidity, gas levels, ozone, air quality, and other features around my desk. Let's bring this to the different spots around the conference including lunch tables, vendor booths, hotel rooms, and more. I need to know about these readings now, not when I get back home from the conference. We need to get these sensor readings immediately in case we need to turn on a fan or move to another area. We will also see if my talk produces a lot of hot air!? My setup is pretty simple, a raspberry pi, a breakout garden sensor mount, and as many sensors as I am willing to fly to Austin. The software stack is Python and Java, Apache Pulsar, MQTT, HTML, JQuery, and Apache Kafka.


#### How to Monitor a Conference (Or Anywhere Really)

Here is your menu of tasty monitoring items, some need devices, add-ons, antennas, sensors and some just some code.   I bounce around between Python, Java, SQL, JavaScript, CSS and Low Code with Apache NiFi.   Pick any 3 for mega monitoring.



##### [1] Let's use the new Spring to read a ton of Air Quality data for the area.  Send to Pulsar via All the Protocols?~!!

* https://github.com/tspannhw/spring-pulsar-airquality
* https://github.com/tspannhw/airquality-kafka-consumer
* https://github.com/tspannhw/airquality-mqtt-consumer
* https://github.com/tspannhw/FLiPN-AirQuality-REST
* https://medium.com/@tspann/timeplus-plus-pulsar-is-pure-perfection-a1a4d253031f

##### Let's use Apache NiFi to read all the US weather and sent to Pulsar.

* https://medium.com/@tspann/parsing-weather-feeds-to-add-to-real-time-streams-ec5ecc2849fb
* https://github.com/tspannhw/FLiP-Pi-Weather
* https://github.com/tspannhw/pulsar-weather-function


##### Let's Monitor Temperature and Humidity via MQTT 

https://github.com/tspannhw/pulsar-adafruit-funhouse

<img src="https://raw.githubusercontent.com/tspannhw/pulsar-adafruit-funhouse/main/IMG-6527.jpg" width="300" height="300" />


##### Let's consume all the conference tweets

##### Let's monitor all planes nearby

* https://dzone.com/articles/tracking-aircraft-in-real-time-with-apache-pulsar
* https://github.com/tspannhw/FLiP-Py-ADS-B


#### Let's Monitor the Electric We Use Today

Required:   HS-110 TP-Link Monitoring Device, Python 3, Apache Pulsar
Optional:   Apache Spark SQL, Trino, Apache Flink SQL, Pulsar Functions, InfluxDB

* https://github.com/tspannhw/FLiP-Py-Energy

![EnergizeMe](https://github.com/tspannhw/FLiP-Py-Energy/raw/main/flinkeletricmax.png)


##### Display Live Streaming Data The Easy Open Source Way

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

