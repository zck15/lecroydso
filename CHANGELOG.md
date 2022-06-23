# Changelog

All notable changes to the original package [**TeledyneLeCroy/lecroydso**](https://github.com/TeledyneLeCroy/lecroydso) will be documented in this file.

## 2022-06-23
### Added
- For class `LeCroyVISA` in `lecroyvisa.py`, save the `pyvisa.ResourceManager` to `self._rm` in method `__init__()`. Thus the visa resource manage can be closed manually.

### Changed

- In methods `reconnect()` and `disconnect()` of class `LeCroyVISA` in `lecroyvisa.py`, close the resource manager.
- In method `__init__()` of class `LeCroyVISA` in `lecroyvisa.py`, close the resource manager if failed to make a LeCroyVISA connection.
- In method `__init__()` of class `LeCroyVISA` in `lecroyvisa.py`, save the `connection_string` to `self.connection_string` no matter connection succeed or not. Thus we can call `reconnect()` to try to connect again.

