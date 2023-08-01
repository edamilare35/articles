---
title: "IoT Part 2: Connect an IoT device to Azure Raspberry Pi"
datePublished: Sat Jul 15 2023 12:50:28 GMT+0000 (Coordinated Universal Time)
cuid: clkrj5vcz000009muay5qaeet
slug: iot-part-2-connect-an-iot-device-to-azure-raspberry-pi
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1690847556497/28198081-cba0-4752-a32d-b7676953aa5e.jpeg
tags: azure, cloud-computing

---

To connect an IoT device to the Azure Raspberry Pi simulator, you can follow these steps:

1.	Set up an Azure IoT Hub:
a. Go to the Azure portal and create a new IoT Hub resource.
![Hub](https://cdn.hashnode.com/res/hashnode/image/upload/v1690847544476/0157798c-f3f0-4373-80d3-a5330e5fac0e.png)
b. Configure the settings for your IoT Hub, such as name, subscription, resource group, and region.
![Configurations](https://cdn.hashnode.com/res/hashnode/image/upload/v1690847546351/3eae6edb-f7ac-4370-90f9-2f166ef53a57.png)
c. 
Once the IoT Hub is created, go to its “Shared access policies” section and create a new policy with sufficient permissions (e.g., “registryRead”, “registryWrite”, “serviceConnect”, “deviceConnect”).
d. Take note of the “Connection string - primary key” value; you’ll need it later.
![primaryconnectionkey](https://cdn.hashnode.com/res/hashnode/image/upload/v1690847548325/a2aa35a9-c284-4771-9533-4dc45eb0143c.jpeg)

2. Open your web browser and search for azure raspberry pi simulator.

3.	Run the Raspberry Pi simulator:
![RPS](https://cdn.hashnode.com/res/hashnode/image/upload/v1690847550341/248bfab5-495e-432a-82c0-c859ad2ab6c8.jpeg)
a. Input your code, add logic to start the device simulation and send telemetry data at regular intervals. Input primary connection key on line 15 of the code script.
![PCS](https://cdn.hashnode.com/res/hashnode/image/upload/v1690847552268/bca960b7-b757-4217-ba99-2a1c054e8649.jpeg)
b. Test the simulator on your local machine to make sure it’s functioning correctly.
	
4.	Monitor device telemetry in Azure IoT Hub:
a. In the Azure portal, navigate to your IoT Hub resource.
b. Open the “IoT devices” section and verify that your simulated device is listed.
c. Monitor the incoming telemetry data and device events in the “Messages” and “Events” sections.
![ME](https://cdn.hashnode.com/res/hashnode/image/upload/v1690847554369/c17a7b40-e73b-4f65-b4d0-8b99f4201ee5.jpeg)

That’s it! You have now connected your IoT device (Raspberry Pi simulator) to Azure IoT Hub. You can explore additional features such as device management, data visualization, and alerts using Azure services like Azure Stream Analytics, Azure Functions, or Azure Logic Apps.