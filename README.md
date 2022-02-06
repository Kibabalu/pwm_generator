# PWM power output generator

PWM power output generator for utilization in training arangements.

Generates a 0 to 100% duty cycle to the load at the output. The dyty cycle can be controlled by an potentiometer. Operating voltage 12VDC. Max. current 3A. In addition it features Inverse supply voltage protection and over-voltage protection. The board fits into a Hammond 1593K enclosure.

Most of PWM generator designs are based on 555 ICs. But I haven't found a circuit that covers up the full range from 0 to 100% duty cycle. Thus I used a more basic design: A combination of a Schmitt trigger and a Integrator, both implemented with two opamps (TLV2372), is feeding a comparator (TLV2372). The duty cycle of the resulting PWM signal is determind by the switching voltage comming from a potentiometer. A complementary driver, made by a NPN (BC817) and a PNP (BC807) transistor, drives a MOSFET (TSM900n06CW) for the load.

![schematic](pwm_generator.png)

![Enclosure](1593K.png)

![PCB](pwm_driver.png)

![Photo](IMG_0087.jpeg)
