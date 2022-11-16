## Controlling AC Loads through Voice Commands on Pi:

At idle conditions, the raspberry pi keeps on checking for the phrase which triggers the code. In our case, our triggering phrase will be “hello”. We wrote our code in such a way that when the user speaks the triggering phrase- hello, it triggers the remaining part of the code. The program will further run, which deals with the listening of the audio and executing the commands (which turns on/off the lights depending on the commands it listens to).

# Code

from subprocess import call
import speech_recognition as sr
import serial
import RPi.GPIO as GPIO      
import os, time
r= sr.Recognizer()
led=27
text = {}
text1 = {}
GPIO.setwarnings(False)
GPIO.setmode(GPIO.BCM)
GPIO.setup(led, GPIO.OUT)
def listen1():
    with sr.Microphone(device_index = 2) as source:
               r.adjust_for_ambient_noise(source)
               print("Say Something");
               audio = r.listen(source)
               print("got it");
    return audio
def voice(audio1):
       try: 
         text1 = r.recognize_google(audio1) 
##         call('espeak '+text, shell=True) 
         print ("you said: " + text1);
         return text1; 
       except sr.UnknownValueError: 
          call(["espeak", "-s140  -ven+18 -z" , "Google Speech Recognition could not understand"])
          print("Google Speech Recognition could not understand") 
          return 0
       except sr.RequestError as e: 
          print("Could not request results from Google")
          return 0

