![FineMotionLogo8bit](https://user-images.githubusercontent.com/15166740/219030593-b4450e05-8ab3-4bbc-aa22-df6a7a366d92.png)

# SlimeVR Based Full-Body Tracker

ESP8266 Motion Capture Devices for SlimeVR Ecosystem

Thinnest SlimeVR Tracker!

Full SMT PCB operating in MPU-6500 6DoF mode

Operate with all 5V chargers, including C to C PD chargers.

You can use it simply by ordering it from the fabricator

![.](https://media.discordapp.net/attachments/1035468061580460032/1035468374693662740/unknown.png)
<!--![FBT_Round_2022-Feb-21_12-32-22AM-000_CustomizedView14755583882_png - 복사본](https://user-images.githubusercontent.com/15166740/161261406-e853b4be-313f-4721-82e6-cb6b48a9e55c.png)
![KakaoTalk_20220223_222725417_01](https://user-images.githubusercontent.com/15166740/161364606-c8e09892-575d-4725-931e-a6b7f6b5f61f.jpg)
![KakaoTalk_20220223_222725417](https://user-images.githubusercontent.com/15166740/161364617-89621510-34f0-4919-be8a-b33350d9140c.jpg)
![image](https://user-images.githubusercontent.com/15166740/161454675-0740d4ca-4264-4b6e-8f56-9f29aa31817a.png)
![image](https://user-images.githubusercontent.com/15166740/161454916-a54c4693-e9c1-454c-85dc-dd0a7822720e.png)
![KakaoTalk_20220420_084354356_01](https://user-images.githubusercontent.com/15166740/164119670-261c3e02-e0fe-4508-9886-2ccc19d5d1fd.jpg)
![KakaoTalk_20220726_093847052](https://user-images.githubusercontent.com/15166740/180898132-acec5d8d-918e-4d9e-ad32-58ac35cc4740.png)-->
![image](https://user-images.githubusercontent.com/15166740/209420772-763fcecc-921f-4fd3-a2c7-cabfb2675628.png)
![image](https://user-images.githubusercontent.com/15166740/209420777-812ca429-9d7b-4f0d-8604-7bc034dd56ba.png)
![image](https://user-images.githubusercontent.com/15166740/209420814-63488cd2-4e08-49c9-aa34-135fa9019e34.png)
![image](https://user-images.githubusercontent.com/15166740/209420816-57d1c694-6230-49aa-a3e7-25622dffc013.png)
![KakaoTalk_20221224_130624400_03](https://user-images.githubusercontent.com/15166740/209420863-f9336a47-574b-4c65-8325-b619993901eb.jpg)
![KakaoTalk_20221224_130624400_07](https://user-images.githubusercontent.com/15166740/209420867-e5448ab0-63b1-4d20-9ddd-20a08a36494b.jpg)

## Why should that tracker be able to be detached from the strap?

It is because of the start-up calibration of the MPU-6000 series.

When the MPU first powers up, the DMP measures the static noise, but this needs to be done on every boot. In other words, to reboot the tracker in-game, you must detach it from your body. Not only does this strap adapter help make it very convenient, but it is also a great help in tracker maintenance!

It only takes 10 seconds for you to assemble the tracker sensor and adapter, and less than 30 seconds to assemble all the trackers to your body \:P

It is eco-friendly to save the life of Velcro straps and easily replace broken adapters.



## Specification

- Power Rating: 500mA@5V (TProg: 2.4KOhm)
- Wi-Fi: 802.11bgn 2.4GHz (20.5mW@2dBi)
- Protection Circuit: Depend on battery
- IMU: Invensense MPU-6500 6DoF Attitude detection sensor
- The radio wave safety of this product has been verified by a nationally recognized testing agency.

## Prerequirements

- PCB: [This Repo!](/PCBs)
- 3D Model: [This Repo!](/3D%20Models)
- Belt Strap: https://aliexpress.com/item/1005003002833146.html, or any 50mm width Strap
- Battery: https://aliexpress.com/item/1005004165245143.html, or any 702050 Cell
- USB Cable: https://aliexpress.com/item/1005004409330904.html, or any Type-C cables

## How do I make it?

1. [Order PCB!](/PCBs)
2. Order Belt, Battery!
3. [Print Shell!](/3D%20Models)
4. Go to SteamVR...

## defines.h
```cpp
#define FineMotion_v5
#define IMU IMU_MPU6500
#define IMU_ROTATION DEG_0
#define BOARD BOARD_NODEMCU
#define SECOND_IMU IMU
#define SECOND_IMU_ROTATION IMU_ROTATION
#define BATTERY_MONITOR 1
#define BATTERY_SHIELD_RESISTANCE 0
#define BATTERY_SHIELD_R1 12
#define BATTERY_SHIELD_R2 47
#define PIN_IMU_SDA 4
#define PIN_IMU_SCL 5
#define PIN_IMU_INT 0xFF
#define PIN_IMU_INT_2 0xFF
#define PIN_BATTERY_LEVEL 17
```

## Why do trackers have to be thin?

![image](https://user-images.githubusercontent.com/15166740/216480616-5468ac55-ce28-4b37-8486-5be85c9a62f6.png)

![image](https://user-images.githubusercontent.com/15166740/216480622-75ee1430-e2c8-4386-a897-92c558b35838.png)

The thinner the tracker, the closer the IMU is to the bone and the better the tracking accuracy. It is less affected by inertial force in fast movements.. Above all, it is comfortable when lying on the bed facing the tracker!

## License
**This hardware is licensed under the CERN-OHL-P v2 license**, which is a permissive,
non-viral and non-reciprocal open hardware license. Unlike software licenses like
MIT and Apache 2.0, it better handles the nuances of hardware and protects both
the licensor and licensee from patent lawsuits.

**Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this work by you, shall be licensed as above, without any
additional terms or conditions.**

### Conveying notice of License
Note that as part of the CERN-OHL-P v2 license, recipients of manufactured
hardware must also receive notice of the above license. One such
method of conveying the notice is to include a link to the original source repo,
or printing "Licensed under CERN-OHL-P v2" on the PCB silkscreen. For more info,
see [here](https://ohwr.org/project/cernohl/wikis/Documents/CERN-OHL-version-2).

This is conceptually similar to the MIT/Apache 2.0 Licenses, where the original
license must still be included as a notice even when the source is modified and
subsequently relicensed under different terms.

