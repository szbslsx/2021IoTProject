Note:
1. All dependencies packages must be installed in the same python version folder. (exp, pip3 matches pyhton3. Use the same version across the board. No pip2 then pyhton3.) Check and make sure defacult pip and python shell command are pointed toward the same version by using 'which python' and 'which pip' command. If they don't a match, it has to be fixed beforehand. 

Current Progress: 
- Could not access bluetooth interface/shell on cloud VM. 
- Used homebrew to install bluetooth shell on mac.
- Used bluetooth shell to connect Mac to Windows machine
- Install Mosquitto MQTT on mac through homebrew shell
- Mosquitto on local machine -- Mosquitto borker launched. Mosquitto subscribed. Mosquitto helloworld successful. (All on the same machine) https://www.digikey.com/en/maker/projects/send-and-receive-messages-to-your-iot-devices-using-mqtt/39ed5690cc46473abe8904c8f960341f
https://subscription.packtpub.com/book/application-development/9781787287815/1/ch01lvl1sec12/installing-a-mosquitto-broker-on-macos
OKay, bluetooth does not work for mqtt as mqtt has to run over TCP/IP (wifi)?? Is it?
- Created In/Outgoing bluetooth ports on PC.
IoT Hub? Gateway?
- /PyBlueZ-master/examples/simple/inquiry is working on Mac.
- Python environment has to be fixed -- Multiple Python versions mixing up in the shell command cause dependencies to be scattered into different versions thus not working.
- /PyBlueZ-master/examples/simple/rfccom-server is not working: “Could not retrieve an available service channel”
- /PyBlueZ-master/examples/simple/l2pserver is not working: “protocal not supported”
- /Test is not working: “Could not retrieve an available service channel”

Proposal/final goal:
- Gather data from a wearable health sensor like Fitbit and present tracked data in a dashboard at local device. Then pass the data to cloud server to train a machine learning model to predict activity’s contribution to sleep quality. 
- Data was collected from sensor by local device through Bluetooth. The sensor was simulated on a local machine and data was pre-installed to simulate output. PyBlueZ was used in Python to set up the Master - Sub connection between local device and sensor. 
- Data was transferred from local device to cloud server through MQTT protocol, which used RabbitMQ in Python to set up the sensor as publisher, local device as broker, and cloud server as subscriber. The server was hosted on Azure Cloud Virtual Machine running Ubuntu. 
- The data was normalized into dataframe through Pandas. Sklearn and Statsmodel were used for multiple regression and performance evaluation, which was based on confusion matrix and n-fold cross-validation. 
- Packaged code into Docker images for deployment.

