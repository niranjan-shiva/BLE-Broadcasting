**Basic Bluetooth Broadcasting**

This code initializes the Bluetooth Serial library and sets the device name to "ESP32-WROOM-32E". In the setup() function:

It initializes the serial communication at a baud rate of 115200.
It starts the Bluetooth serial communication with the device name.
It waits for 5 seconds to allow the Bluetooth device to start.
It prints a message to the serial console indicating that the device is ready to pair with Bluetooth.

In the loop() function:
It checks if the device is connected to a Bluetooth device using the connected() method.
If connected, it prints a message to the serial console indicating that it's connected.
If not connected, it prints a message indicating that it's not connected.
It waits for 1 second before checking again.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Broadcasting Environmental Sensing Data**

This code uses the Adafruit BME280 library to read temperature, humidity, and pressure data from the sensor. It then broadcasts this data over Bluetooth using the sendData() function.

Key components:
sensor_data_t struct: This struct holds the sensor data, including temperature, humidity, pressure, and two boolean flags (updated and simulate).
sensorTask() function: This function reads the sensor data from the BME280 sensor and updates the sensorData struct. If the sensor is not found, it enables data simulation.
sendData() function: This function broadcasts the sensor data over Bluetooth using the SerialBT object.
loop() function: This function calls the sensorTask() function to read the sensor data and checks if the data has been updated. If updated, it calls the sendData() function to broadcast the data.

