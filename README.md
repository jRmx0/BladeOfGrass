# BladeOfGrass

BladeOfGrass is a DIY robotic lawn mower project aimed at building a fully autonomous mowing system using off-the-shelf hardware parts and custom software developed on the ESP-IDF framework.

## Overview

The hardware is built using easily available parts to create a reliable, affordable mower that’s easy to maintain and upgrade. The design focuses on durability and long-term use.

The software architecture follows a modular design approach, implementing clear separation of concerns across three distinct modules:

1. Modem (Research Phase)
2. Controller (Active Development - [GitHub Repository](https://github.com/jRmx0/BladeOfGrass-mower)) 
3. NTRIP Client (Operational - [GitHub Repository](https://github.com/jRmx0/BladeOfGrass-NTRIP-client)) 

### Module functionality

**Modem Module:** Manages internet connectivity and serves as the main communication link to the outside world. It oversees other modules and monitors critical system parameters. A backup power supply and dedicated GPS antenna enable it to send alerts in case of theft or major system failures.

**Controller Module:** Functions as the central processing hub, collecting and processing data from all subsystems to determine and execute mowing operations. This module coordinates the overall system behavior based on inputs from various sensors and subsystems.

**NTRIP Client Module:** Handles communication with RTK correction services, enabling the UM980 GNSS module to establish and maintain RTK fixed positioning for precise navigation.

## Future plans

The current implementation uses the ThingsBoard Cloud platform, which offers convenience but also imposes certain limitations. To build a fully customized and self-sufficient system, the following components are planned:

1. **On-premise server** – to serve as the system's database and backend, providing greater control and flexibility.
2. **Mobile app** – to enhance user experience through real-time interaction, control, and monitoring.

These additions will support a more robust, scalable, and user-friendly solution.

