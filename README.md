# Medical_OCR


- Quick setup
    1. get administrator permission
    2. download devcon.exe
    3. update the disk id
    4. update the device id

- Setting
    - OverView
        |     Feature Name     |     Range     |                            Note                                 |
        |:--------------------:|:-------------:|:---------------------------------------------------------------:|
        |    Camera Height     | 17cm ~ 45cm   |   Defaultly 30cm, counting from platform to ultrasonic module   |
        |    Illumination      |    1 ~ 6      |                       Defaultly 1.3                             |
        |    Lens Exposure     |  1.8 ~ 16     |                             N/A                                 |
        |    Lens Focus        |      N/A      |                   Defaultly focus on 30cm                       |
        |    Holder Thickness  |      N/A      |  Defaultly 1.5cm, call DDRA00 if thickness is greater than 3cm  |

    - Arduino(UNO) / UltraSonic Module(UNO-Hc-SR04):
        | Ultrasonic Module | Arduino |
        |:-----------------:|:-------:|
        |        vcc        |    5v   |
        |        GND        |   GND   |
        |        Trig       | pin 13  |
        |        Echo       | pin 12  |

    - Camera(acA4024 - 29uc) (this will be set by programme)
        |     Feature Name    |     Range     |  Value In Programme  |
        |:-------------------:|:-------------:|:--------------------:|
        |      Resolution     |  4024 * 3036  |          N/A         |
        |    exposure_time    |   0 ~ 999999  |        44565.0       |
        |         gain        |    0 ~ 27     |          10          |
        |        gamma        |    0 ~ 3.9    |           1          |
        |  balance_ratio_red  |    0 ~ 15     |        2.31592       |
        |  balance_ratio_green|    0 ~ 15     |           1          |
        |  balance_ratio_blue |    0 ~ 15     |        2.0549        |
        
    - Error Code:
        |          Error Name         |     Code     |
        |:---------------------------:|:------------:|
        |   LogFileOpenError          |     1000     |
        |   PreviousFileNameError     |     1001     |
        |   USBHubError               |     2000     |
        |   CameraError               |     2001     |
        |   FocusModuleError          |     2002     |
        |   ArduinoError              |     2003     |
        |   LEDError                  |     2004     |
        |   AdminError                |     3000     |
        |   DiskError                 |     3001     |
        |   UnknownError              |     7000     |
        |   OCRError                  |     7001     |
        |   StickerNumberError        |     7002     |
        |   RedTapeNumberError        |     7003     |
        |   RedTapeSignError          |     7004     |
        |   ConnectorNumberError      |     7005     |
        |   ConnectorDirectionError   |     7006     |