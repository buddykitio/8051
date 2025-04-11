# Buddy51 Mini - 8051 Development Board

![Board Image](https://github.com/buddykitio/Buddy51mini/blob/main/Hardware/Image/Buddy51mini.jpg)

A compact, beginner-friendly 8051 development board with micro USB programming, designed for embedded systems education.

## 📌 Features
- **8051 Microcontroller** (W78E52D)
- **Micro USB Programming** (No external programmer needed)
- **Inbuilt LED** for GPIO testing
- **Breadboard-friendly** design
- **USB-powered** (5V) with voltage regulation
- **USB UART support** for serial communication
- **SDCC compatible** (Open-source toolchain)
- **Low-cost** student-friendly design


## 🚀 Quick Start Guide

## 🛠 Hardware Setup
### 1. Connections
- Connect via Micro USB to PC
- Detects as COM port (check Device Manager)
- USB-powered (no external supply needed)

### 2.Basic Program (Blink LED)
```c
#include <8051.h>
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

## ⚙️ Compilation & Flashing
For complete compilation workflow and project templates, see our dedicated repository:
[Buddy51-Project](https://github.com/buddykitio/Buddy51-Project)

## 📚 Learning Resources
- **SDCC Documentation**: 
  - [Official Manual](http://sdcc.sourceforge.net/doc/sdccman.pdf)
  - [8051 Specific Guide](https://sdcc.sourceforge.net/doc/8051.html)
- **Hardware Reference**:
  - [W78E52D Datasheet](https://www.nuvoton.com/products/microcontrollers/8bit-8051-mcus/industrial-8051-series/w78e52d/)
  - [CH340 Datasheet](https://www.wch-ic.com/products/CH340.html)

## 🔧 Troubleshooting
| Symptom | Solution |
|---------|----------|
| Board not recognized | Install CH340 drivers |
| SDCC compilation errors | Check `#include` paths for  headers |
| Flashing fails | Ensure proper COM port selection in Nuvoton tool |

## 🤝 Contributing
We welcome contributions! Please follow these steps:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## 📧 Support
For technical support or collaboration inquiries:
- Email: buddykit@sakthicontroller.com
- Website: [buddykit.io](https://buddykit.io)
- GitHub Issues: [Report bugs/requests](https://github.com/buddykitio/Buddy51mini/issues)

## 📜 License
Open-source under MIT License - Free for educational and personal use
