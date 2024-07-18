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
