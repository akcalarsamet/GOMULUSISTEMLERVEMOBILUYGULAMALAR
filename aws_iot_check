#!/usr/bin/env python
from AWSIoTPythonSDK.MQTTLib import AWSIoTMQTTShadowClient
import time
import RPi.GPIO as GPIO
from mfrc522 import SimpleMFRC522
import mysql.connector
import Adafruit_CharLCD as LCD
import logging
import json

db = mysql.connector.connect(
  host="localhost",
  user="attendanceadmin",
  passwd="sametakcalar34",
  database="attendancesystem"
)

class shadowCallbackContainer:
    def __init__(self, deviceShadowInstance):
        self.deviceShadowInstance = deviceShadowInstance

    # Custom Shadow callback
    def customShadowCallback_Delta(self, payload, responseStatus, token):
        # payload is a JSON string ready to be parsed using json.loads(...)
        # in both Py2.x and Py3.x
        global LEDPIN=responseStatus
        payloadDict = json.loads(payload)
        isLEDOn=payloadDict["state"]["isLEDOn"]
        deltaMessage = json.dumps(payloadDict["state"])
        #print(deltaMessage)
        if isLEDOn == "true":
            print("Gecerli Kart")
            GPIO.output(LEDPIN, GPIO.HIGH) # Turn on
        else:
            print("Turn off LED")
            GPIO.output(LEDPIN, GPIO.LOW) # Turn on    
        #print("Request to update the reported state...")
        newPayload = '{"state":{"reported":' + deltaMessage + '}}'
        self.deviceShadowInstance.shadowUpdate(newPayload, None, 5)


clientId="mypythoncodeled"
thingName="rfid"
myAWSIoTMQTTShadowClient = AWSIoTMQTTShadowClient(clientId)
myAWSIoTMQTTShadowClient.configureEndpoint("asfbv2rxqx300-ats.iot.us-east-2.amazonaws.com", 8883)
myAWSIoTMQTTShadowClient.configureCredentials("root-CA.pem", "LED-private.pem.key", "LED.pem.crt")


# Connect to AWS IoT
myAWSIoTMQTTShadowClient.connect()

deviceShadowHandler = myAWSIoTMQTTShadowClient.createShadowHandlerWithName(thingName, True)
shadowCallbackContainer_Bot = shadowCallbackContainer(deviceShadowHandler)

# Listen on deltas
deviceShadowHandler.shadowRegisterDeltaCallback(shadowCallbackContainer_Bot.customShadowCallback_Delta)

cursor = db.cursor()
reader = SimpleMFRC522()

lcd = LCD.Adafruit_CharLCD(4, 24, 23, 17, 18, 22, 16, 2, 4);

try:
  while True:
    lcd.clear()
    lcd.message('Kartinizi OKutun\n')
    id, text = reader.read()
    bool cardState
    cursor.execute("Select id, name FROM users WHERE rfid_uid="+str(id))
     if isLEDOn == True
            print("Gecerli Kart")
            GPIO.output(LEDPIN, GPIO.HIGH) # Turn on
            customShadowCallback_Delta(self,payload,)
        else:
            print("Turn off LED")
            GPIO.output(LEDPIN, GPIO.LOW) # Turn on    
    result = cursor.fetchone()

    lcd.clear()

    if cursor.rowcount >= 1:
      lcd.message("Hos Geldiniz\n" + result[1])
      cursor.execute("INSERT INTO attendance (user_id) VALUES (%s)", (result[0],) )
      db.commit()
    else:
      lcd.message("Gecis Yok")
    time.sleep(2)
finally:
  GPIO.cleanup()
