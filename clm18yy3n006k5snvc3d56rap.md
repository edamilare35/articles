---
title: "IoT Part 2: Connect an IoT device to Azure Raspberry Pi"
datePublished: Sat Jul 15 2023 12:50:28 GMT+0000 (Coordinated Universal Time)
cuid: clm18yy3n006k5snvc3d56rap
slug: iot-part-2-connect-an-iot-device-to-azure-raspberry-pi-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693612188823/77547852-bc80-4348-bc08-1f673918a533.jpeg

---

To connect an IoT device to the Azure Raspberry Pi simulator, you can follow these steps:

1.	Set up an Azure IoT Hub:
a. Go to the Azure portal and create a new IoT Hub resource.
![Hub](https://cdn.hashnode.com/res/hashnode/image/upload/v1693612179768/47a6562f-8287-46ee-813c-483018b3e6cd.png)
b. Configure the settings for your IoT Hub, such as name, subscription, resource group, and region.
![Configurations](https://cdn.hashnode.com/res/hashnode/image/upload/v1693612181120/c08845af-326b-49b3-bf70-2c678e9bbed1.png)
c. 
Once the IoT Hub is created, go to its “Shared access policies” section and create a new policy with sufficient permissions (e.g., “registryRead”, “registryWrite”, “serviceConnect”, “deviceConnect”).
d. Take note of the “Connection string - primary key” value; you’ll need it later.
![primaryconnectionkey](https://cdn.hashnode.com/res/hashnode/image/upload/v1693612182737/185408b9-16ba-4f54-b76d-e9bf19f3aee2.jpeg)

2. Open your web browser and search for azure raspberry pi simulator.

3.	Run the Raspberry Pi simulator:
![RPS](https://cdn.hashnode.com/res/hashnode/image/upload/v1693612184083/ff79ad1d-eac3-458c-aa62-d953e340fb21.jpeg)
a. Input your code, add logic to start the device simulation and send telemetry data at regular intervals. Input primary connection key on line 15 of the code script.
![PCS](https://cdn.hashnode.com/res/hashnode/image/upload/v1693612186038/fa8c9d90-e94c-4cbd-a006-d2d16d08cc7d.jpeg)
b. Test the simulator on your local machine to make sure it’s functioning correctly.
	
4.	Monitor device telemetry in Azure IoT Hub:
a. In the Azure portal, navigate to your IoT Hub resource.
b. Open the “IoT devices” section and verify that your simulated device is listed.
c. Monitor the incoming telemetry data and device events in the “Messages” and “Events” sections.
![ME](https://cdn.hashnode.com/res/hashnode/image/upload/v1693612187604/5cc8c935-d5d8-4a29-b147-e6064f85f9c6.jpeg)

That’s it! You have now connected your IoT device (Raspberry Pi simulator) to Azure IoT Hub. You can explore additional features such as device management, data visualization, and alerts using Azure services like Azure Stream Analytics, Azure Functions, or Azure Logic Apps.