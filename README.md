# MMM-DHT22 Module for MagicMirror

The MMM-DHT22 module displays temperature and humidity data from a DHT22 sensor on your MagicMirror.

Examples:

![screenshot_01](https://github.com/J0n4e/MMM-DHT22/assets/25276418/0d85cc54-2cb8-4f64-b31f-2e00e5c2e0b5)

![screenshot_02](https://github.com/J0n4e/MMM-DHT22/assets/25276418/9881f059-bf93-4138-94ea-4e267863c68b)

![screenshot_03](https://github.com/J0n4e/MMM-DHT22/assets/25276418/3aada7c4-041d-4a9b-8ed0-98fb95902fb1)

## Installation

1. Navigate to your MagicMirror's `modules` directory using the terminal:
````
cd ~/MagicMirror/modules
````

1. Clone this repository:
````
git clone https://github.com/J0n4e/MMM-DHT22.git
````

3. Install required dependencies:
````
npm install
````

4. Install Adafruit DHT Library:
````
sudo apt-get update
sudo apt-get install python3-dev python3-pip
git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT
sudo python3 setup.py install
````

5. Test the Library (Optional):
````
cd examples
python3 AdafruitDHT.py 22 <GPIO_PIN>
````
   
Configuration
To use this module, add it to the modules array in the config/config.js file of your MagicMirror installation:

````
modules: [
  {
    module: 'MMM-DHT22',
    position: 'top_right',
    config: {
      // Configuration options here
    }
  }
]
````


Configuration Options
* gpioPin: GPIO pin number for the DHT22 sensor.
* fontSize: Font size for module text.
* fontFamily: Font family for module text.
* showThermometerIcon: Set to true to show the thermometer icon.
* showDropletIcon: Set to true to show the droplet icon.
* showTemperatureText: Set to true to show the temperature text.
* showHumidityText: Set to true to show the humidity text.
* headerText: The header text to be displayed above the values.
* updateInterval: Update interval in seconds for fetching sensor data.

Example Configuration
Here's an example configuration for the MMM-DHT22 module:

````
modules: [
  {
    module: 'MMM-DHT22',
    position: 'top_right',
    config: {
      headerText: 'Local Environment',
      gpioPin: 6,
      updateInterval: 120,
      fontSize: '16px',
      fontFamily: 'Arial',
      showThermometerIcon: true,
      showDropletIcon: true,
      showTemperatureText: true,
      showHumidityText: true   
    }
  }
]
````
License:

This project is licensed under the MIT License. See the LICENSE file for details.

Support and Contributions:

If you encounter any issues or have suggestions for improvements, please open an issue on the GitHub repository.

Acknowledgments:

Special thanks to the MagicMirror community and contributors.
