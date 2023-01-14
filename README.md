

# :pushpin: Robot-Rc-Car-ZK-2



<p align="center">
  <img src="https://i.postimg.cc/tRZw0xQ4/logo-removebg-preview.png" alt="robotika smkn1 kotabekasi logo"/ style="height:350px;" "width: 350px;">
</p>


[![Version](https://img.shields.io/badge/VENOM-1.0.17-brightgreen.svg?maxAge=259200)]()
[![Stage](https://img.shields.io/badge/Release-Stable-brightgreen.svg)]()
![licence](https://img.shields.io/badge/license-GPLv3-brightgreen.svg)
[![Arduino Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-alpine.svg?left_text=Alpine%20Linux%20Build)](##Link##)
[![Kali Linux Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-kali.svg?left_text=Kali%20Linux%20Build)](##Link##)
[![Armel Kali Linux Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-armel.svg?left_text=Armel%20Kali%20Linux%20Build)](##Link##)
[![Armhf Kali Linux Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-armhf.svg?left_text=Armhf%20Kali%20Linux%20Build)](##Link##)
[![DragonFly BSD Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-dfly.svg?left_text=DragonFly%20Build)](##Link##)
[![FreeBSD 11 Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-fbsd-11.svg?left_text=FreeBSD%2011%20Build)](##Link##)
[![FreeBSD 12 Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-fbsd-12.svg?left_text=FreeBSD%2012%20Build)](##Link##)
[![OpenBSD 6 Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-obsd.svg?left_text=OpenBSD%20Build)](##Link##)
[![NetBSD 8.1 Build Status](https://buildbot.aircrack-ng.org/badges/aircrack-ng-netbsd81.svg?left_text=NetBSD%20Build)](##Link##)
[![Coverity Scan Build Status](https://scan.coverity.com/projects/aircrack-ng/badge.svg)](##Link##)



## :inbox_tray: Media Social Instagram

To keep this collection up-to-date need contributors who can add more Program Arduino scripts
||
|--------------|
|:mailbox_with_mail: [artha_sa_](https://www.instagram.com/artha_sa_/)
|:mailbox_with_mail: [dicky_asqaelani26](https://www.instagram.com/dicky_asqaelani26/)
|:mailbox_with_mail: [rahmatnurraya](https://www.instagram.com/rahmatnurraya990/)
|:mailbox_with_mail: [applepi_fthur](https://www.instagram.com/applepi_fthur/)
|:mailbox_with_mail: [robotika-smkn1](https://www.instagram.com/robotika.smkn1kotabekasi/)


# :moneybag: [Donate](https://saweria.co/arthasyarif)


# :briefcase: Barang & Bahan
- Arduino Uno
- l293d motor driver
- hc 05 bluetooth module
- Dinamo dc gearbox robot mobil 4X
- Saklar On/Off
- Kabel Male & Female
- Plat Akrilik Sasis Mobil 2X
- Batre Awt 40A,3300mAh
- Tempat Dudukan Batre Awt


# :mag: Ilustrasi Arduino

<p align="center">
  <img src="https://i.postimg.cc/CMZVG8c7/cietj.webp" style="height:205px;" "width:205px;"/>
</p>


# :inbox_tray: Download Libary [ AFmotor ](https://drive.google.com/file/d/1lWQe0IQlVc9-mDP6qdFGbbAMht38LXMc/view?usp=share_link) 


# :clipboard: Source Code

```bash

/*
 * 
 * All the resources for this project: smkn1kotabekasi.sch.id
 * Modified by Robotika smkn1 kotabekasi
 * 
 * Created by Robotika smkn1 kotabekasi
 * 
 */
 
 #include <AFMotor.h>
AF_DCMotor motor1(1);
AF_DCMotor motor2(2);
AF_DCMotor motor3(3);
AF_DCMotor motor4(4);
 
int Speed = 230;
char value;
void setup() {
  Serial.begin(9600);
  motor1.setSpeed(Speed);
  motor2.setSpeed(Speed);
  motor3.setSpeed(Speed);
  motor4.setSpeed(Speed);
}
 
void loop() {
  if (Serial.available() > 0) {
    value = Serial.read();
  }
  if (value == 'F') {
    motor1.run(FORWARD);
    motor2.run(FORWARD);
    motor3.run(FORWARD);
    motor4.run(FORWARD);
  } else if (value == 'B') {
    motor1.run(BACKWARD);
    motor2.run(BACKWARD);
    motor3.run(BACKWARD);
    motor4.run(BACKWARD);
  } else if (value == 'L') {
    motor1.run(BACKWARD);
    motor2.run(FORWARD);
    motor3.run(FORWARD);
    motor4.run(BACKWARD);
  } else if (value == 'R') {
    motor1.run(FORWARD);
    motor2.run(BACKWARD);
    motor3.run(BACKWARD);
    motor4.run(FORWARD);
  } else {
    motor1.run(RELEASE);
    motor2.run(RELEASE);
    motor3.run(RELEASE);
    motor4.run(RELEASE);
  }
}

 

```
