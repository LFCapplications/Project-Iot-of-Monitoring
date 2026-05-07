# Project-Iot-of-Monitoring
Project Iot of Monitoring

  This is a project Iot with a cloud-based system utilizing the Microsoft Azure, speccificaly the services Iot Hub, Event hub and a little of Azure Functions.

  The data architectury is: an Arduino-microcontroller -> Node Red -> (Microsoft Azure) Hub Iot -> Event Hub -> App Mobile (take the data in the endpoint). 

  The arduino collects data of temperature and umidity in real-time with a temperature sensor. Before, this data is post in a sever mqtt(pc1). 
A second machine assigns the Topics "Temperature" and "Umidity" and send this data, formatting using two functions in the Node-RED, to Azure. In the Azure, the Hub Iot send this informations 
for the Event Hub. This service is the responsible to notify users of updates via App mobile, using an endpoint that allows you to connect Azure to App. In the app, the single requeriment to 
see the data in real time is a connection with wifi.

