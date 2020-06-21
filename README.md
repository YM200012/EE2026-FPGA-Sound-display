# EE2026 Design Project
NUS EE2026 final project: Sound Display and digital piano. An FPGA project written by NUS Electrical Engineering Undergraduates Yi Ming and Jiang Weixi
<br/>

## Hardware Requiremants
* Basys 3<sup>TM</sup> FPGA Board
* PmodMIC3
* PmodOLEDrgb
<br/>

## Software Environment
* Vivado Design Suite - HLx Editions - V2018.2
<br/>

## Features
* real-time audio volume indicator
<br/>Show the led and the 7-segment display
Smooth source data to ensure volume reading is stable
* graphical visualization and configurations
<br/>When the switch is 1<br/>
SW15: 1-pixel border<br/>
SW14: 3-pixel border<br/>
SW13: show/hide the volume bar<br/>
BTNC: reset

* The digital piano visualizer
<br/>When the switch is on, the OLED will change the color of a particular space to simulate the press of the keyboard<br/>
When some certain switch is on, the OLED will present the name of a particular chord<br/>
C: 12 8 5<br/>Cm: 12 9 5<br/>D: 10 6 3
<br/>Dm: 10 7 3
<br/>E: 8 4 1
<br/>Em: 8 5 1
<br/>

## Detailed description
In the first part real-time audio volume indicator, the led and the 7-segment display are used to display the volume of the captured audio. The 7-segment display will indicate the peak volume from 0 to 15. 
In this graphical visualization and configurations part, two switches are designed to control two kind of borders. By controlling the switches separately, the OLED will display borders with one or three pixels on width. After that, with the audio signal captured by the real time audio volume indicator, the signal is converted to the volume bar which represented by different colors. The high volume is represented by red, and the low volume is represented by green.  

The additional feature is a small digital piano which have 7 white keys and five black keys. When users do operations on different switches, the OLED screen will change the color of the keys to show which musical note he or she wants to play. Meanwhile, the white key will change from white to yellow, the black key will change from red to pink. The character ‘e-piano’ will be present under the OLED keyboard. At the same time, if the user plays a chord like C (do mi so), the OLED will present the name of the chord to let the user know which chord has played. This feature only contains a few of the chord, it does not support chords with four keys. 

The whole project is about the audio capture and show, also a mini keyboard. It is very proper to use the 96*64 OLED to present a keyboard. Something not so good is have not so much contact between the audio capture and the additional feature. A possible improvement is combining the volume bar with the keyboard or detect the frequency of the voice and give its tone. 
