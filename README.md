Note:
1. All packages must be installed in the same python folder. (exp, pip3-pyhton3)

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
