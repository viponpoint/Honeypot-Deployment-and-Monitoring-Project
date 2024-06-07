# Honeypot-Deployment-and-Monitoring-Project

## Objective

The primary objective of setting up this honeypot project using T-Pot on Digital Ocean is to create a sophisticated environment for detecting, monitoring, and analyzing malicious network activities. Honeypot is something that is easily accessible and attractive, this can be data services or systems, and the objective here is to detect unauthorized activity or to learn more about an attacker or simply distract them.

This setup serves several key purposes:

1. **Threat Detection and Analysis**:
   - **Capture Malicious Traffic**: Attract and capture various forms of cyber attacks in a controlled environment.
   - **Analyze Attack Patterns**: Study the techniques, tactics, and procedures (TTPs) used by attackers.
   - **Identify Vulnerabilities**: Discover common vulnerabilities exploited by attackers, which can inform security improvements.

2. **Improving Incident Response**:
   - **Real-Time Monitoring**: Utilize tools like Kibana and Attack Map to visualize and monitor malicious activities in real-time.
   - **Enhanced Response Capabilities**: Improve the ability to respond swiftly and effectively to detected threats.

3. **Security Automation and Integration**:
   - **Automate Threat Detection**: Implement automated processes for detecting and responding to attacks.
   - **Integrate with Security Tools**: Integrate the honeypot with other security tools and platforms to enhance overall security posture.

### Key Components of the Project

1. **Digital Ocean**:
   - **Cloud Infrastructure**: Utilize Digital Ocean's cloud platform to host the T-Pot honeypot environment, ensuring scalability and reliability.

2. **T-Pot Honeypot Framework**:
   - **Comprehensive Honeypot**: Deploy T-Pot, a multi-honeypot platform that includes various types of honeypots to attract different attack vectors.
   - **Data Collection**: Gather detailed information on attacks for analysis and research.

3. **Kibana**:
   - **Data Visualization**: Use Kibana to create dashboards that visualize honeypot data, making it easier to monitor and analyze attacks.
   - **Real-Time Monitoring**: Enable real-time monitoring and alerting based on honeypot activity.

4. **Attack Map**:
   - **Geographical Visualization**: Provide a visual representation of attack sources and targets on a world map.
   - **Insight into Attack Trends**: Offer insights into the geographical distribution and trends of cyber attacks.

By achieving these objectives, the project aims to significantly enhance the understanding of cyber threats, improve security measures, and contribute valuable insights to my cybersecurity knowledge.

### Skills Learned

- Understanding and applying best practices for securing cloud environments, including firewall configurations, access controls, and network security.
- Installation of T-Pot! Proficiency in deploying and configuring the T-Pot honeypot framework, including initial setup, customization, and optimization.
- Managing multiple honeypot sensors within the T-Pot framework, each designed to attract different types of cyber attacks.
- Analyzing network traffic to detect malicious activities and understand attack patterns.
- Implementing real-time monitoring and alerting based on honeypot activity, using Kibana and other visualization tools.
- Creating and customizing dashboards in Kibana to visualize data collected from the honeypot.
- Identifying and categorizing different types of cyber attacks based on the data collected from the honeypot.

### Tools Used

- Droplets: Digital Ocean's virtual private servers used to host the T-Pot honeypot environment.
- Networking Tools: Digital Ocean's networking features such as VPC, floating IPs, and firewalls to secure and manage the infrastructure.
- T-Pot 24.04.0 Framework: An all-in-one honeypot solution that includes various honeypot sensors and tools for capturing and analyzing attacks.
- Data Visualization: Kibana is used to create dashboards and visualizations of the data collected by T-Pot, providing insights into attack patterns and trends.
- Geographical Visualization: Attack Map is used to visually represent the geographical origins and targets of cyber attacks captured by the honeypot.
- Dionaea: Captures malware samples and exploits.
- Cowrie: Simulates an SSH and Telnet service to capture brute force attacks and shell interaction.
- Elasticpot: A honeypot for simulating Elasticsearch services.
- Conpot: Simulates industrial control systems (ICS/SCADA) to capture specific attacks targeting these environments.
- Honeytrap: Captures and analyzes network-based attacks.


## Steps

#### 1. **Create a Digital Ocean Account**
   - If you don’t already have an account, sign up on [Digital Ocean](https://www.digitalocean.com/).

#### 2. **Create a New Droplet**
   - Log in to your Digital Ocean account.
   - Click on “Create Droplet”.
   - Choose an image: Select **Ubuntu 22.04** as the operating system.
   - Select a plan: Choose a plan with sufficient resources. T-Pot recommends at least 4GB of RAM and 2 CPUs.
   - Add block storage if needed.
   - Choose a data center region that is closest to your location for better performance.
   - Enter your prefered password.

#### 3. **Initial Setup of the Droplet**
   - Once the droplet is created, note the IP address.
   - Connect to your droplet via SSH:
     You can use Putty
     ssh root@your_droplet_ip
     ```
   - Update the package lists and upgrade the existing packages:
     ```sh
     apt update && apt upgrade -y
     ```

#### 4. **Install Docker**
   - Install Docker, which is required for running T-Pot:
     ```sh
     apt install docker.io -y
     systemctl start docker
     systemctl enable docker
     ```

#### 5. **Install Docker Compose**
   - Install Docker Compose for managing the multi-container Docker applications:
     ```sh
     apt install docker-compose -y
     ```

#### 6. **Download and Install T-Pot**
   - Clone the T-Pot repository:
     ```sh
     git clone https://github.com/telekom-security/tpotce
     cd tpotce/iso/installer/
     ```
   - Run the T-Pot installer:
     ```sh
     ./install.sh --type=user
     ```
   - Follow the on-screen instructions to complete the installation.
     
#### 7. **Configure T-Pot**
   - Once the installation is complete, T-Pot will automatically start its services. You can access the T-Pot web interface by navigating to `https://your_droplet_ip:64297` in a web    
     browser.
   - Log in using your credentials that you must have created during the installation.

#### 8. **Accessing Kibana and Attack Map**
   - Access Kibana for log analysis and visualization at `https://your_droplet_ip:64297/kibana` or click on the GUI link leading to Kibana
   - View the Attack Map at `https://your_droplet_ip:64297/map` or also click the GUI link.

#### 9. **Set Up Monitoring and Alerts**
   - Configure Kibana to create dashboards for visualizing attack data.
   - Set up alerts in Kibana for specific events or attack patterns.

#### 10. **Enhance Security**
   - Enable firewalls and security groups on Digital Ocean to restrict access to the honeypot.
   - Implement network monitoring and intrusion detection systems if necessary.

### Summary

By following these steps, you can set up a fully functional T-Pot honeypot on Digital Ocean, allowing you to monitor, analyze, and visualize cyber attacks in real-time. This project not only helps me in understanding attack patterns from all over the world, but also in enhancing overall cybersecurity measures.

##Images from the project

![Screenshot 2024-06-07 150250](https://github.com/viponpoint/Honeypot-Deployment-and-Monitoring-Project/blob/main/Everywhere.png)   
After 24 hours of the setup, attacks are coming from all over the world as shown on the map.

Images from the lap to follow soon!
