# [WORK IN PROGRESS] Embedded C development WITHOUT IDE but using Makefile and VIM (Or any Text editor you want) and CMSIS Library.
This repository contains all the resources that I used to learn how to develop
 on micro controller.
I explain all choices made to build my project (Why and How).

"I hear and I forget,
 I see and I remember,
 I do and I understand."
 Confucius

## Equipment:

### Why buy a STM32F3 device?
Because it's funnier to actually use an embedded device to program.
But you still can use a processor emulator like QEMU (not covered here) if you
can't afford one.
- STM32F303VC Discovery
https://fr.farnell.com/stmicroelectronics/stm32f3discovery/evaluation-f3-cortex-m4-discovery/dp/2215108

### Why buy Mini USB cable ?
Because you need one to connect your computer to your microcontroler (USB or ST link).
And another one if you plan to use FTDI component for UART (RS232) communication
betweeen your computer and your device.
- 2x Mini USB cable:
https://www.amazon.fr/gp/product/B00P0GI68M?ref=ppx_pt2_dt_b_prod_image

### Why buy a bluetooth peripheral ?
If you plan to communicate throught bluetooth between your computer and your
device.
- Bluetooth 2.0:
https://www.amazon.fr/gp/product/B074GMQ6G3?ref=ppx_pt2_dt_b_prod_image

### Why buy a FTDI peripheral ?
If you plan to use UART communication (RS232) 
between your computer and your device. Don't forget to buy
a Mini USB cable for this as mentioned earlier.
- FTDI:
https://www.amazon.fr/gp/product/B06ZZ65R3H/ref=ppx_od_dt_b_asin_title_s00?ie=UTF8&psc=1

### Why buy wiring ?
We need this to connect FTDI (UART), Bluetooth (UART), ITM peripheral (ITM)
and everything you could need later.
- Male/Male, Male/Female, Female/Female wiring:
https://www.amazon.fr/dp/B00OR3LWLM/ref=pe_3044141_189395771_TE_3p_dp_1

## Documentation
We will rely on this documentation to develop our software.
It covers your device in detail. 
See Documentation repository or link in the "ressources" part.

## Why make another embedded development resource ?
Because a lot of resources use an IDE/Library which hide the complexity and
logic behind embedded development. Of course those tools are really usefull and
you will probably use them in a professionnal environment. But for a learning
purpose I think it's better to learn and understand what your IDE and your
library do at the lowest level (for a software developer).
Because I wanted to understand Why and How?
Because you can learn software development on embedded system only using
Makefile and text editor (with of course an appropriate tool chain). You don't
NEED anything else.
Because I wanted to make my work useful for people like me :).

## Why use CMSIS Library ?
CMSIS stands for ARM Cortex Microcontroller Software Interface Standard.
More specifically we use the CMSIS library provided in the STM32 CubeMX 
package.
https://www.st.com/en/embedded-software/stm32cubef3.html
In this package we have all the CMSIS library plus an additionnal header file 
from stm32 suited for our devices. This header file is useful because we want 
to avoid any mistake from bad bit manipulation.
We need those files to build our own library.

## Is there everything I need to know for embedded development on this "tutorial" ?
No.
Just what i think is mandatory to know/understand to be comfortable.
No electronics skills are needed and i don't cover this part (yet).

## How is your project build ?
A readme.md file explains all choices made for each subject/file.
I tell what I'm doing and why. Sometimes (or usually) I add a lot of other 
sources to read, to go further/deeply. I won't write everything on this 
tutorial because there are a lot of good resources on the internet to learn a 
particular notion.

## Is there an order for reading ?
No. Each little project is independent and can work alone. You can cherry pick
or mix project if you want to.
But if it's your only learning material (and I hope it's not) I encourage you
 to follow the suggested order.

## Why there is no picture from documentation in your readme files ?
Because an essential skill you need in software development is knowing how to 
RTFM (Read The F__king Manual). You HAVE to kno how to find information in your
device documentation and how to use it. It's important to get conmfortable with
the official documentation. At the begining it's annoying but then you will 
find what you need easily.

## Something else ?
If you need more information about a part of this resources, just ask me.
If something in here helped you in some way, let me know :).

Enjoy your embedded development journey :D

## Resources

USER MANUAL:
https://www.st.com/content/ccc/resource/technical/document/user_manual/8a/56/97/63/8d/56/41/73/DM00063382.pdf/files/DM00063382.pdf/jcr:content/translations/en.DM00063382.pdf

DATA SHEET:
https://www.st.com/resource/en/datasheet/stm32f303vc.pdf

REFERENCE MANUAL:
https://www.st.com/content/ccc/resource/technical/document/reference_manual/4a/19/6e/18/9d/92/43/32/DM00043574.pdf/files/DM00043574.pdf/jcr:content/translations/en.DM00043574.pdf

ECOMPASS MODULE: 3D ACCELEROMETER AND 3D MAGNETOMETER:
https://www.st.com/resource/en/datasheet/lsm303dlhc.pdf

3-AXIS DIGITAL OUTPUT GYROSCOPE:
https://www.st.com/content/ccc/resource/technical/document/application_note/2c/d9/a7/f8/43/48/48/64/DM00119036.pdf/files/DM00119036.pdf/jcr:content/translations/en.DM00119036.pdf

## One particularly good resources i started with
https://docs.rust-embedded.org/discovery/index.html
It's in Rust because i wanted to learn Embedded developement and Rust at the 
same time (bad idea).
It's a well written tutorial you can refer too even if it's not in C.
But there is just one thing missing:
"I've taken care of initializing everything" => This is the part covered here.
