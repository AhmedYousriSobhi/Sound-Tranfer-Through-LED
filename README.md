# Sound-Tranfer-Through-LED
# About:
In This Project, just like the title said, We transfer sound, audio or music from device like your smartphone to headphones or speaker through LED.
This project is divided into two distinct sections: audio transmission and reception via hardware. The transmission media is unguided. The main objective of this project was primarily to realize a transmission-reception system to transfer sound via Laser without a guiding medium, using Intensity Modulation with little quality loss.
![IMG-20201106-WA0009](https://user-images.githubusercontent.com/66730765/98439590-8da1bf80-20fb-11eb-9742-c8e192adb977.jpg)

# Details:
This project consists of Two Main parts, The Transmitter circuit and The Reciever circuit.
## components:
### 1-LED:
It stands for Light Emitted Diode. It can be used as a replacement of the laser . it do the same function as the laser .it cosume low power than the laser , but the range of the LED is smaller than the range of the laser.
![1200px-LEDs](https://user-images.githubusercontent.com/66730765/98441661-71584f80-2108-11eb-9e6a-fa28438a9a88.jpg)
### 2-Laser:
The laser stands for “light amplification by stimulated emission of radiation.” Lasers work as a result of resonant effects. The output of a laser is a coherent electromagnetic field. In a coherent beam of electromagnetic energy, all the waves have the same frequency and phase. The laser transmit the information exactly the same as it get it.

![mini-laser-module-diode-red-dot-650nm-5v-dc-5mw-500x500](https://user-images.githubusercontent.com/66730765/98441620-2f2f0e00-2108-11eb-9db8-6398a5ae9b7a.jpg)
### 3-Transistor 2N2222:
It’s a BJT transistor. Its used to make a common emitter amplifier ( it will be explained in transmitter section).

![1](https://user-images.githubusercontent.com/66730765/98441699-a5337500-2108-11eb-99b8-7aa8fcb68f8b.png)
### 4-LM386 audio amplifier:
An Op-Amp is used to make an amplifier. It will be explained in receiving section.

![lm386-pin-arrangement](https://user-images.githubusercontent.com/66730765/98441722-d01dc900-2108-11eb-90f3-b45412ad1e1f.jpg)
### 5-Capcaitors.
### 6-Resistors and Potentiometer.
### 7-9V Battery.
### 8- Wires

##Schematic of Project on Proteus simulation:
![schemit](https://user-images.githubusercontent.com/66730765/98443325-37407b00-2113-11eb-83fe-e9ee6ed55f0a.jpg)

## The Transmitter Circuit V1 Schematic schetch:
![DSC_0002](https://user-images.githubusercontent.com/66730765/98441227-a0b98d00-2105-11eb-8502-44b6a0376194.jpg)

## The Reciever Circuit V1 Schematic schetch:
![DSC_0003](https://user-images.githubusercontent.com/66730765/98441243-be86f200-2105-11eb-8682-6d297871511b.jpg)

## The Transmitter circuit Explanation:
The audio is fed to the circuit through a standard 3.5mm audio jack through the input Vin shown in the Circuit Diagram . Simply connect an audio source (such as a mobile phone or laptop) to the mono jack and turn on the laser / LED . The modulations of current produced by the audio device causes the laser to modulate accordingly. It will get slightly dimmer and brighter, depending on the music. However, this is very difficult to detect by the human eye.
The audio jack presented the input to a feedback BJT transistor amplifier of n- type (common emitter) which has a gain of about 25 , but with a phase shift 180 degree . A capacitor of 1uF which is used as dc blocking to block any dc signal comes suddenly from the input . the amplifier is with a bias of 12 v . Another capacitor of 1uF works also as dc blocking capacitor . we have 3 kΩ resistor to have the ouput amplified voltage across it . sure there will be small loses on the 5 ohm resistance which is series to the 3k ohm but it will be neglected and from the voltage divider the 3k ohm will take all the voltage, but we put it just to saperate the ground from the 3k ohm resistance because as u can see the negative terminal of the resistance is connected parallel to the positive terminal 9 volt battery . we have Zout which is very large and presented the input impedance in the common collector . but in common collector configuration (2N2222) , we consider it as buffer as it just maintains voltage gain and have a great input impedance so the input voltage on it will be on the input impedance and a small volt will be absorbed on the internal resistance of the input  , and small output impedance of the buffer which is important point in this configuration to prevent making a great drop on it if it is great and the  , in the same time to send most of the gain from the common emitter to the output (laser here or led ) 9 v battery for the aim of biasing . Finally the output signal (light) from the laser/LED will be sent to the receiver circuit .

![13140756_912790628866473_2118212339_n](https://user-images.githubusercontent.com/66730765/98443842-cb601180-2116-11eb-80e0-e834534d9f6f.png)
![13161275_912790685533134_770548571_o](https://user-images.githubusercontent.com/66730765/98443844-d024c580-2116-11eb-8110-87259d04137f.png)
![13161515_912789648866571_194956494_o](https://user-images.githubusercontent.com/66730765/98443846-d155f280-2116-11eb-89d6-f7d710cf8f44.png)
### Experimental Results:
The input voltage from the mobile vary from 0.05 to 0.07 volt rms AC
The input voltage from the laptop vary from 0.09 to 0.12 volt rms AC
The output volt of the common emitter amplifier vary from 0.7 to 1 volt rms AC
The volt on the laser/ led is 3.7 volt DC and vary from 0.9 to 1.6 volt rms AC
Q point:
Vce=5.7volt dc max       icq=60uA rms              Vbc=5.6volt  dc       Veb=0.63 volt dc              
Note This values will differ from a song to another , and vary as you increase the volume of the song on the smartphone or decrease it , and for sure this reading will differ from one smartphone to another because not all the phones have the same output value of a song .

## The Reciever circuit Explanation:
The voltage variation in photo resistance is amplified by a low voltage audio power amplifier LM386 and reproduced by speaker. The maximum output of audio amplifier LM386 is 1 watt, while its voltage gain is 20 to 200. Here laser diode with maximum operating voltage 2.6Volt and maximum operating current 45mA is used to transmit the audio signal.
First of all , we have a photo resistor to receive the signal from the transmitting circuit which its value changes as the laser or light approach it. a battery of 9v is used in parallel with the photo resistor as photo resistor is a passive element doesn’t produce voltage .so, we put a battery 9 v to produce a current which will change proportionally with  the variable value of the resistor and produces a variable voltage as we need !. a capacitor of 1 uF Working as a dc blocking to block any dc signal just permit audio signal pass .In addition , a variable resistor of maximum value of 10kΩ which works as a volume control for the audio signal (simply acts as attenuator ) To make the LM386 a more flexible audio amplifier .the main pivotal component in our circuit if LM386 IC , it is the amplification component in the circuit , contains 8 pins each one has its unique function in the component . in our circuit we connect pins 1 and 8 together with capacitor between them with a value of 10 uF to vary the gain of audio power amplifier LM386 IC .Also a capacitor of 1 uF to block dc signals . Another capacitor (1nF) works as a filter which prevents high frequency signals from the amplifier ( harmonics) .  a series RC are placed on which have the the values of 10Ω and 10 nF respectively .Moreover , we can compensate poor speaker bass using them . a battery of 9 v is used connecting to pins number 6 to be the supply of vcc of the circuit and a bias for the circuit to make the junctions work . finally we have a 8 Ω speaker (stereo) to receive the amplifying  output signal . 
Note that: we can use LDR or solar cell instead of photo resistor .. all of them doesn’t need a 9 v source to get a voltage as they are active elements produce voltage as they were hit by light or laser.  
The volt of the op amp amplifier is from 0.8 to 1.6 volt rms AC 

# Updated Circuits:
I tried to update the circuits to reduce the number of batteries and be easier to connect for kids to do on their own.

## The Transmitter Circuit V2 Schematic schetch:
![DSC_3704](https://user-images.githubusercontent.com/66730765/98440460-84b3ec80-2101-11eb-8464-96aa61555a99.jpg)

## The Reciever Circuit V2 Schematic schetch:
![DSC_3703](https://user-images.githubusercontent.com/66730765/98440498-b7f67b80-2101-11eb-964d-5a7bcf1faea5.jpg)

## Full V2 Schematic schetch:
![DSC_3707](https://user-images.githubusercontent.com/66730765/98441511-7ff23700-2107-11eb-98d4-2d93fc7a8492.jpg)

## Hardware Connection on BreadBoard:
![DSC_3712](https://user-images.githubusercontent.com/66730765/98441313-250c1000-2106-11eb-9a05-ed37baee31ea.jpg)

## The Transmitter Circuit V2 on BreadBoard:
![DSC_3708](https://user-images.githubusercontent.com/66730765/98441343-4ff66400-2106-11eb-8f4b-3434b8e6b342.jpg)

## The Reciever Circuit V2 on BreadBoard:
![DSC_3710](https://user-images.githubusercontent.com/66730765/98441358-66042480-2106-11eb-90c6-ef8c4b5dd7a4.jpg)

## Full Circuit Connection:
![IMG-20201106-WA0010](https://user-images.githubusercontent.com/66730765/98441375-80d69900-2106-11eb-9c2d-438ee0ebbe3b.jpg)

# Life Photos of the Project:
### LED emitted light is directed toward the LDR:
![DSC_3699](https://user-images.githubusercontent.com/66730765/98441396-a663a280-2106-11eb-955e-36d74d2ee43c.jpg)
### LED emitted light is not directed toward the LDR:
![DSC_3700](https://user-images.githubusercontent.com/66730765/98441398-a82d6600-2106-11eb-953f-276cd8b42be1.jpg)

# Conclusion 
• A circuit for sound transmission using laser was designed and developed. 
• The transmitter and receiver circuit were designed separately to perform the required function. 
• An optical source, Laser, was used on which the audio signal was successfully modulated and transmitted. Finally the optical signal was received by the solar panel.
• The complete hardware circuit was successful in performing the desired function i.e. transfers of sound from the transmitter circuit to the receiver’s circuit loudspeaker via unguided media.


# References:
• What are lasers - http://whatis.techtarget.com/definition/laser
• Transmitting Audio Wirelessly Through Light-http://treehouseprojects.ca/audiolight/
• Light and Optics - http://sci-toys.com/scitoys/scitoys/light/light.html

# Special thanks to all the people we meet who had helped us a lot in our project . 
