# ECP

To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in

**AIM**
- To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in
keil.

**APPARATUS REQUIRED**

- Keil.
- Personal Computer
- Keil μVision Software
- Serial Transfer of Single Byte / Character using 8051 (Keil)


**PROGRAM**
(i) Serial Port Transfer a Single Character
```C
#include<reg51.h>
void main(void)
{
TMOD=0X20;
TH1=0XFA;
SCON=0X50;
TR1=1;
SBUF='A';
while (T1==0);
T1=0;
while(1);
}
```
(ii) Serial Port to Transfer a Message
```C
#include <reg51.h>
void main(void)
{
unsigned char msg[] = "RAVEENDRANATH";
unsigned char i;
TMOD = 0x20; // Timer1 Mode2
TH1 = 0xFD; // 9600 baud rate
SCON = 0x50; // Serial mode1
TR1 = 1; // Start Timer1
for(i = 0; msg[i] != '\0'; i++)
{
SBUF = msg[i];
while(TI == 0);
TI = 0;
}
while(1);
}
```
**OUTPUT**
(i) Serial Port Transfer a Single Character

<img width="752" height="533" alt="image" src="https://github.com/user-attachments/assets/24cd54b6-8899-4b5b-9037-85d901c4f1da" />

---

<img width="959" height="563" alt="image" src="https://github.com/user-attachments/assets/46fb9856-3ec3-4998-a5f4-b3b81fb2faa2" />

---

<img width="570" height="254" alt="image" src="https://github.com/user-attachments/assets/5e44671e-b0eb-453b-9111-690334664cfb" />


(ii) Serial Port to Transfer a Message

<img width="959" height="563" alt="image" src="https://github.com/user-attachments/assets/c24a3b89-6c8c-4a31-a2bc-8025f563a93f" />

---

<img width="957" height="563" alt="image" src="https://github.com/user-attachments/assets/0baea9fe-4369-4b14-af0e-a23dba10c193" />

--- 

<img width="568" height="236" alt="image" src="https://github.com/user-attachments/assets/d19a3a24-385b-4c24-932f-25b57e9ce890" />





**RESULT**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
