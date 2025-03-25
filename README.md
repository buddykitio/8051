


# 8051 Development Board with Micro USB Programming

![Board Image](https://via.placeholder.com/400x250) *(Replace with actual image)*

A compact, beginner-friendly 8051 development board with micro USB programming and inbuilt LED, designed for embedded systems learning. Fully compatible with Keil µVision IDE.

## 📌 Features
- **8051 Microcontroller** (W78E52D)
- **Micro USB Programming** (No external programmer needed)
- **Inbuilt LED** for GPIO testing
- **Breadboard-friendly** design
- **USB-powered** (5V) with voltage regulation
- **Reset button** for debugging
- **UART support** for serial communication
- **Keil µVision IDE** compatible
- **Low-cost** student-friendly design

## 🛠 Hardware Setup
### 1. Connections
- Connect via Micro USB to PC
- Detects as COM port (check Device Manager)
- USB-powered (no external supply needed)

### 2. Required Software
- [Keil µVision IDE](https://www.keil.com/)
- USB-to-Serial drivers (CH340/CP2102 if needed)
- [Novoton](https://www.nuvoton.com/resource-download.jsp?tp_GUID=SW1720200221181328))

## 💻 Keil µVision Setup
### 1. Install Keil C51
1. Download from [keil.com](https://www.keil.com/)
2. Install C51 compiler (free version has 2KB limit)

### 2. Create New Project
1. Project → New µVision Project
2. Select your 8051 variant (e.g. W78E52D)
3. Add startup file (usually auto-added)

### 3. Build and Flash
1. Write code in `.c` file
2. Build (F7) to generate `.hex`
3. Flash using Novoton

## 👨‍💻 Example Code (Blink LED)
```c
#include <W78E52D.H>
#define LED P1_1

void delay(unsigned int ms) {
    unsigned int i, j;
    for(i=0; i<ms; i++)
        for(j=0; j<1275; j++);
}

void main() {
    while(1) {
        LED = 0;    
        delay(500);
        LED = 1;    
        delay(500);
    }
}
```

### Steps to Run:
1. Create new Keil project
2. Add this code to `main.c`
3. Build (F7) → generates `.hex`
4. Flash using Novoton

## 📚 Learning Resources
- [Keil 8051 Tutorial](https://www.keil.com/support/man/docs/c51/)
- [8051 Embedded C Guide](https://www.electronicshub.org/8051-tutorials/)
- [ Novoton](https://www.nuvoton.com/tool-and-software/debugger-and-programmer/1-to-1-debugger-and-programmer/nu-link2-pro/?index=5)

## 🔧 Troubleshooting
| Issue | Solution |
|-------|----------|
| Board not detected | Install CH340/CP2102 drivers |
| Hex not flashing | Check COM port/baud rate |

## 📜 License
 Open source for educational use

## 🤝 Contributing
Contributions welcome! Please:
1. Fork the project
2. Create your feature branch
3. Submit a pull request

## 📧 Contact
- Email: mailemail@example.com
- Website: [your-website.com](https://your-website.com)

