# Tapo P100
Tapo P100 is a Python library for controlling the Tp-link Tapo P100/P105/P110 plugs and L510E bulbs.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install PyP100.

```bash
pip3 install PyP100
```

## Usage
```python
from PyP100 import PyP100

p100 = PyP100.P100("192.168.X.X", "email@gmail.com", "Password123") #Creating a P100 plug object

p100.handshake() #Creates the cookies required for further methods
p100.login() #Sends credentials to the plug and creates AES Key and IV for further methods

p100.turnOn() #Sends the turn on request
p100.setBrightness(100) #Sends the set brightness request
p100.turnOff() #Sends the turn off request
p100.getDeviceInfo() #Returns dict with all the device info
```

```python
from PyP100 import PyP110

p110 = PyP110.P110("192.168.X.X", "email@gmail.com", "Password123") #Creating a P110 plug object

p110.handshake() #Creates the cookies required for further methods
p110.login() #Sends credentials to the plug and creates AES Key and IV for further methods

#PyP110 has all PyP100 functions and additionally allows to query energy usage infos
p110.getEnergyUsage() #Returns dict with all the energy usage
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Contributers
[K4CZP3R](https://github.com/K4CZP3R)\
[Sonic74](https://github.com/sonic74)

## License
[MIT](https://choosealicense.com/licenses/mit/)
