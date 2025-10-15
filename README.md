# LLM-Driven Synthetic Sensor Traffic Generation for 6G Networks in Smart Homes

By leveraging Large Language Models (LLMs) or other generative approaches to synthesize both realistic normal and controlled malicious 6G traffic, researchers can obtain a critical tool for evaluating physical layer security (PLS) mechanisms. In the absence of real 6G infrastructures, synthetic traffic enables systematic testing of PLS algorithms against statistical variability, extreme scenarios, and hidden or perturbed patterns. Synthetic datasets: 

- Provide large-scale, labeled data without privacy risks, thereby facilitating the training and cross-comparison of machine learning–based PLS techniques (e.g., physical-layer authentication, anomaly detection).

- Allow controlled replication of specific attack scenarios such as spoofing, replay, denial-of-service (DoS), jamming, eavesdropping, and novel threats related to THz or reconfigurable intelligent surface (RIS) channels.

- Ensure reproducible and shareable evaluation pipelines that increase the reliability of security assessments.

Moreover, the AI-driven, multi-layer, and space–air–ground integrated architecture of 6G will inevitably introduce new attack surfaces; beyond conventional threats (e.g., spoofing, replay, DDoS, jamming, passive eavesdropping), adversarial manipulations targeting RIS configurations or THz propagation are also anticipated. Therefore, evaluating PLS solutions under both benign and adversarial synthetic traffic is indispensable. Ultimately, LLM-driven, scenario-specific traffic generation offers a practical pathway to bridge the gap between theory and implementation in PLS research, enabling early-stage measurement and improvement of the trustworthiness and resilience of future 6G networks.


# Smart Home Devices (Current and Future 6G-Enabled Ecosystem) and Room Topology

To simulate realistic Internet of Things (IoT) communication and device interaction, we designed a smart home environment represented by a 3D-rendered apartment layout. 
The apartment consists of two bedrooms, one living room, one kitchen, and one bathroom, arranged in a compact, efficient structure suitable for residential IoT experiments.

Each room is equipped with embedded smart devices (e.g., smart speakers, motion sensors, lighting controllers, and environmental monitors), interconnected through a wireless network architecture. 
The living room serves as the central hub, hosting a smart television, an automation control tablet, and several IoT access points responsible for managing the communication with peripheral devices distributed across the apartment. 
The kitchen and bathroom include smart utility components such as connected water and energy sensors, while the bedrooms integrate smart lighting and climate control systems.

This virtual environment provides a controlled yet realistic setting for testing smart home communication protocols, data collection mechanisms, and anomaly detection algorithms. 
Its modular design allows easy adaptation to various experimental conditions, including the introduction of network attacks, device failures, or behavioral automation scenarios.

![smart_home](https://github.com/nkelesoglu/6G-Synthetic-Traffic-Generation/blob/main/room_topology.png)

We assume smart home devices relevant for data-driven simulation and attack detection at the physical layer, thus include: Smart lock systems, Window or glass-break sensors,  Smart thermostats and air-quality monitors, Intelligent HVAC controllers, Robotic vacuum cleaners, Smart lighting and curtain systems, Smart refrigerator, oven, washing machine, and dishwasher, Smart coffee maker, 6G smart gateway.


These devices collectively represent sensor-rich, low-latency communication nodes that align well with the study’s goal of producing synthetic yet physically plausible 6G traffic for studying attack detection and trustworthiness mechanisms at the physical layer.


Table 1 presents the distribution of smart devices deployed in the simulated 6G-enabled apartment environment. The simulated home consists of two bedrooms, a living room, a kitchen, and a bathroom. Each room hosts a set of devices representing realistic usage scenarios observed in contemporary and emerging smart homes.

For instance, bedrooms include smart locks, environmental sensors, lighting systems, and robotic vacuum cleaners, reflecting a typical low-latency, sensor-rich communication setup. 
The living room contains a higher concentration of interconnected devices, including smart lighting, HVAC controllers, and entertainment-related appliances such as smart TVs and plug systems, which together produce diverse data traffic patterns. 
The kitchen features multiple IoT-enabled appliances—smart refrigerator, oven, coffee maker, and air-quality monitor—emphasizing machine-to-machine communication relevant to energy optimization and automation. 
The bathroom setup includes environmental and humidity sensors for health and safety monitoring.

A single 6G smart gateway acts as the central hub that coordinates communication between all devices, manages the local network, and links the home infrastructure to the external 6G network core. 
This setup allows a realistic simulation of intra-home communication, data aggregation, and potential attack detection mechanisms at the physical layer.

Overall, the configuration offers a compact yet representative smart home environment for evaluating 6G-based sensor data generation, physical-layer attack modeling, and security testing.

**Table 1.** Distribution of 6G-enabled smart home devices across rooms in a simulated apartment environment, including device type and unique identifiers.

| **Room** | **Device Type** | **Unit** | **Device ID** | **Description** |
|-----------|------------------|-----------|----------------|-----------------|
| **Living Room** | Smart Thermostat | 1 | 0xst001 | Controls temperature and humidity; <br> connected to HVAC system |
|  | Smart Air Quality Monitor | 1 | 0xsaq001 | Measures CO₂, VOCs, and humidity levels |
|  | Smart Lighting (Ceiling) | 2 | 0xsl001, 0xsl002 | Dimmable LED light with motion <br> and brightness control |
|  | Smart Curtain System | 2 | 0xsm001, 0xsm002 | Automatically adjusts curtains <br> based on sunlight and time of day |
|  | Smart Plug (TV Unit) | 2 | 0xsmp001, 0xsmp002 | Monitors and controls energy consumption <br> of entertainment unit |
|  | Motion Sensor | 1 | 0xmos001 | Detects human presence for lighting <br> and security automation |
| **Bedroom #1** | Smart Light Bulb (Ceiling) | 2 | 0xsl003, 0xsl004 | Adjustable white/color temperature <br> for ambient comfort |
|  | Smart Plug (Desk) | 4 | 0xsmp003, 0xsmp004, 0xsmp005, 0xsmp006 | Power monitoring and remote control <br> for electronics |
|  | Smart Lock (Room Door) | 1 | 0xsmal001 | Secure access management for private space |
|  | Temperature Sensor | 1 | 0xtemp001 | Provides local room temperature readings <br> for HVAC optimization |
| **Bedroom #2** | Smart Light Bulb (Ceiling) | 2 | 0xsl005, 0xsl006 | Ambient lighting with adaptive brightness control |
|  | Smart Plug | 4 | 0xsmp007, 0xsmp008, 0xsmp009, 0xsmp010 | Power control for bedside devices |
|  | Motion Sensor | 1 | 0xmos002 | Detects occupant presence and automates lighting |
| **Kitchen** | Smart Light Bulb (Ceiling) | 2 | 0xsl007, 0xsl008 | Ambient lighting with adaptive brightness control |
|  | Smart Refrigerator | 1 | 0xsref001 | Tracks temperature, humidity, and power usage |
|  | Smart Oven | 1 | 0xsov001 | Provides temperature telemetry and cooking status |
|  | Smart Dishwasher | 1 | 0xsdis001 | Sends cycle completion and water usage data |
|  | Smart Coffee Maker | 1 | 0xscof001 | Automated brewing schedule and power control |
|  | Smart Plug | 6 | 0xsmp011, 0xsmp012, 0xsmp013, 0xsmp014 | Measures energy consumption of small appliances |
| **Bathroom** | Smart Light Bulb (Ceiling) | 1 | 0xsl009 | Ambient lighting with adaptive brightness control |
|  | Smart Humidity Sensor | 1 | 0xshum001 | Detects steam and humidity for ventilation control |
|  | Smart Lighting | 2 | 0xsl010, 0xsl011 | Automated lighting via motion detection |
|  | Smart Water Leak Sensor | 1 | 0xswat001 | Detects water leakage and alerts the system |
| **Core Network** | Smart Gateway (6G Home Hub) | 1 | 0xgw001 | Central hub for device communication and traffic routing |
|  | Smart Energy Meter | 1 | 0xsem001 | Monitors total home energy usage and reports to gateway |
| **All Rooms** | Intelligent HVAC Controller | 5 | 0xhvac01, 0xhvac02, 0xhvac03, 0xhvac04, 0xhvac05 | Manages heating, cooling, and airflow across rooms |
| **Total** |  | **48** |  |  |
