
# 8051 Development Board with Micro USB Programming

![Board Image](https://via.placeholder.com/400x250) *(Replace with actual image)*

A compact, beginner-friendly 8051 development board with micro USB programming and inbuilt LED, designed for embedded systems learning. Uses SDCC (Small Device C Compiler) for open-source development.

## 📌 Features
- **8051 Microcontroller** (W78E52D)
- **Micro USB Programming** (No external programmer needed)
- **Inbuilt LED** for GPIO testing
- **Breadboard-friendly** design
- **USB-powered** (5V) with voltage regulation
- **Reset button** for debugging
- **UART support** for serial communication
- **SDCC compatible** (Open-source toolchain)
- **Low-cost** student-friendly design

## 🛠 Hardware Setup
### 1. Connections
- Connect via Micro USB to PC
- Detects as COM port (check Device Manager)
- USB-powered (no external supply needed)

### 2. Required Software
- [SDCC Compiler](https://sdcc.sourceforge.net/)
- USB-to-Serial drivers (CH340/CP2102 if needed)
- [Flash Tool](https://www.nuvoton.com/tool-and-software/) (Nuvoton programmer)

## 💻 SDCC Setup
### 1. Install SDCC
#### Windows:
Download installer from [SDCC website](https://sdcc.sourceforge.net/)

#### Linux (Debian/Ubuntu):
```bash
sudo apt install sdcc
```

#### macOS:
```bash
brew install sdcc
```

### 2. Compile and Flash
1. Write your code in `.c` file
2. Compile:
```bash
sdcc main.c
```
3. Generate HEX file:
```bash
packihx main.ihx > main.hex
```
4. Flash using Nuvoton programmer

## 👨‍💻 Example Code (Blink LED)
```c
#include <W78E52D.h>
#define LED P1_1

void delay(unsigned int ms) {
    unsigned int i, j;
    for(i=0; i<ms; i++)
        for(j=0; j<1275; j++);
}

void main() {
    while(1) {
        LED = 0;    // LED ON
        delay(500);
        LED = 1;    // LED OFF
        delay(500);
    }
}
```

### Steps to Run:
1. Save as `main.c`
2. Compile: `sdcc main.c`
3. Generate HEX: `packihx main.ihx > main.hex`
4. Flash using Nuvoton tool

## 📚 Learning Resources
- [SDCC Manual](http://sdcc.sourceforge.net/doc/sdccman.pdf)
- [8051 with SDCC Guide](https://electronics.stackexchange.com/questions/tagged/sdcc+8051)
- [Nuvoton Programming Tools](https://www.nuvoton.com/tool-and-software/)

## 🔧 Troubleshooting
| Issue | Solution |
|-------|----------|
| SDCC not found | Add to PATH or reinstall |
| "packihx not found" | Install SDCC completely |
| Board not detected | Check USB drivers |

## 📜 License
Open source for educational use

## 🤝 Contributing
1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📧 Contact
- Email: buddykit@sakthicontroller.com
- Website: [buddykit.io](https://buddykit.io)


Would you like me to add any specific SDCC-related details like:
- Makefile examples for automated builds
- Advanced SDCC compiler flags
- Debugging with SDCC
- Specific W78E52D header file configurations?
