# Relay Control System

This project allows you to control relays over a web interface, using a serial communication protocol. The relays can be toggled on or off from the web browser or via API and the system ensures that only authenticated users can access the control interface.

## Instruction
1. Pull the project
2. Update the config.xml, ensure it match the total relays associated to the board. For instance, the product https://denkovi.com/usb-eight-channel-relay-board-for-automation have 8 relays, so a total of 8 relay slots on config.xml
3. Ensure the board is powered on and connected to the PC or raspberry PI.
4. run the program
```
chmod +x ftdicontroller
./ftdicontroller
```
5. Open localhost:8080 to login and test the control or you try postman: http://localhost:8080/control?slot=3&state=true, supply the basic auth on the request, ensure it matcht he config.xml


## AI Integration
You can use function calling to control the relay remotely but before that happens you need to expose your home IP to the internet or you can use Ngrok tunneling service to expose speficific port to handle the request.

## Notes
1. COM3 is windowsbased while /dev/ttyUSB0< is linux based, u need to update the config.xml correctly.
