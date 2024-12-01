# midi_guesture

a gesture-controlled MIDI device

a gesture-controlled MIDI device

## prototype v1.0

![image](https://github.com/user-attachments/assets/b6e907ae-41b0-477b-be2e-bad63831c19e)


this device acts as a midi-device when connected via micro-usb to a USB HOST

it sends cc values on midi channel 0 to the following cc channels:

cc channel | device

### ldr controls x4

there are 4 seperate controls for sending midi cc with light dependant resistors and a rgb led for feedback

each channel has a ldr jack, an upper and lower button and offset knob.

these grouping can be seen on the circuit board in green (with there corrosponding cc channel below them)

![image](https://github.com/user-attachments/assets/b61ffcb8-c77e-4848-89a7-0c1032219365)


### operation of each ldr channel

the cc values on the ldr channel depends on how much light falls on the ldr. midi cc ranges between 0 and 127. 

- if the midi cc value reaches __max__ value of 127 the led turns red
- if the midi cc value reaches __min__ value of 0 the led turns blue
- a single press of the __upper button__ sets the current ldr level as maximum
- a single press of the __lower button__ sets the current ldr level as minimum
- a double press of the __upper button__ resets the upper limit
- a double press of the __lower button__ resets the lower limit
- turning the knob offset adds/subtracts values to the midi cc

### operation of the gyro unit

additionally to the ldr control there is a gyro module that can control cc channels 5 and 6

![image](https://github.com/user-attachments/assets/572d9313-6f1f-4bed-b947-1afbab8962fb)


- the middle button of left enables the x axis to send midi on channel 5 (led shows white when channel is enalbed)
- the middle button of right enables the y axis to send midi on channel 6 (led shows white when channel is enalbed)
- similar to ldr stage the top button sets the upper limit with single press and resets it with double press (red led indicates upper bound reached and blue led indicates lower bound reaches)
- similar to tdr stage the bottom buttom sets the upper limit with single press and resets it with double press (red led indicates upper bound reached and blue led indicates lower bound reaches)
