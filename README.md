# exp1
import Adafruit_DHT
import time
DHT_SENSOR = Adafruit_DHT.DHT11
DHT_PIN = 4
while True:
    humidity,temperature=Adafruit_DHT.read(DHT_SENSOR,DHT_PIN)
    if temperature is not None and humidity is not None:
      print("Temp={0:0.1f}c Humidity={0:1.0f}%".format(temperature,humidity));
     else:
      print("sensor failure.check wiring");
      time.sleep(1); 
