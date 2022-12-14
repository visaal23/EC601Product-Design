# EC601Product-Design
 
# EC601Product-Design

## Raspberry Pi Speech Recognition Program :
We begin by importing the speech recognition modules and other needed
modules, which are used to convert speech to text and text to speech. After
importing these modules, we have to import the GPIO module, which controls the
pins of the raspberry pi.

```
from subprocess import call
import speech_recognition as sr
import serial
import RPi.GPIO as GPIO
```

The code given below is a function, which deals with the listening of the phrases
that we speak. This program waits until the user gives input (speech). When the
user says something, it stores that information in the “audio” variable and returns
that information.
```

def listen1():
  with sr.Microphone(device_index = 2) as source:
               r.adjust_for_ambient_noise(source)
               print("Say Something");
               audio = r.listen(source)
               print("got it");
  return audio
```


The below code is a function that accepts the audio1 variable. It recognizes our
voice using google speech API and then prints our speech in string format on
the screen.

```
def voice(audio1):
    try:
      text1 = r.recognize_google(audio1)
      call('espeak '+text, shell=True)
      print ("you said: " + text1);
      return text1;
    except sr.UnknownValueError:
       call(["espeak", "-s140 -ven+18 -z" , "Google Speech Recognition
       could not understand"])
       print("Google Speech Recognition could not understand")
       return 0
    except sr.RequestError as e:
       print("Could not request results from Google")
       return 0
```

The code which is written in the main function is used to deal with the listening of
the phrases, which is then converted to text using speech to text module, and
then gives feedback using Espeak.

```
def main(text):
   audio1 = listen1()
   text = voice(audio1);
   text = {}
```

The if and elseif conditions given below are used to check whether the string in
the text variable is either “light on” or “light off”. If the string inside the text
variable is light on, then the if function gets satisfied.

The code inside if function is used to send high value to the pin name led (PIN
27). After sending the high value to the pin, we use espeak that transfers text to
speech, which is used as feedback. If the string inside the text variable is light off,
then if condition will not be satisfied leading the program to check for the elseif
condition. If the elseif condition gets satisfied (if the string inside the variable
“text” is light off), the program enters the code which is written inside the elseif
condition. The code inside the elseif function is used to send low value to the pin
named led (PIN 27). This pin is connected to a relay to control any required AC
load.

```
if 'light on' in text:
        GPIO.output(led , 1)
        call(["espeak", "-s140 -ven+18 -z" , "okay Sir, Switching ON the
Lights"])
        print ("Lights on");
     elif 'light off' in text:
        GPIO.output(led , 0)
        call(["espeak", "-s140 -ven+18 -z" , "okay Sir, Switching off the
Lights"])
        print ("Lights Off");
       text = {}
```

The code given below is the one that runs first. When the python interpreter is
running the module, it sets the __name__ variable to a value “ __main__”. The
below code deals with listening and comparing the “text” variable. The code is
given below acts as the code to keep the main program in standby mode until the
raspberry pi listens to the triggering phrase. When the raspberry pi captures the
triggering phrase, it allows the program to enter the main code, which is defined
in another function named main().

```
if __name__ == '__main__':
   while(1):
       audio1 = listen1()
       text = voice(audio1)
   if text == 'hello':
       text = {}
       call(["espeak", "-s140 -ven+18 -z" ," Okay master, waiting for your
command"])
       main(text)
     else:
        call(["espeak", "-s140 -ven+18 -z" , " Please repeat"])
```






 
