
# pygeolocate
 
`pip install -U pygeolocate` or `python -m pip install -U pygeolocate`
|  |  |
|--|--|
| <img align="center" src="https://i.imgur.com/g3Euo2M.png" height="128" width="128"/> | <img align="center" src="https://img.shields.io/pypi/dm/pygeolocate?style=for-the-badge"/><img align="center" src="https://img.shields.io/github/license/scrumpyy/pygeolocate?style=for-the-badge"/><img align="center" src="https://img.shields.io/github/issues/scrumpyy/pygeolocate?style=for-the-badge"/><br><img align="center" src="https://img.shields.io/github/stars/scrumpyy/pygeolocate?style=for-the-badge"/><img align="center" src="https://img.shields.io/pypi/v/pygeolocate?style=for-the-badge"/><img align="center" src="https://img.shields.io/pypi/pyversions/pygeolocate?style=for-the-badge"/> |

Support server: <a href="https://discord.gg/v9Y8Yq2k5D" target="_blank">
  <img draggable="false" style="width:119xp;height:20xp;" src="https://discord.com/api/guilds/1103834986194415637/embed.png">
</a>

## What is pygeolocate?
Pygeolocate is a simple Python module that allows for developers to get the longitude and latitude coordinates of the geographical center of a country based on Googles dataset.

Pygeolocate also allows for developers to search for countries based on their country code (and vice versa) as well as search for partial country names.

## Get a country by its full name
```python
# pygeolocate/examples/get_country_by_full_name.py
import pygeolocate

united_kingdom = pygeolocate.locate_by_name("united kingdom")[0]

print(united_kingdom)
print(united_kingdom.name)
print(united_kingdom.coordinates)
print(united_kingdom.coordinates[0])
print(united_kingdom.coordinates['long'])
```

## Get a country by part of its name
```python
# pygeolocate/examples/get_country_by_partial_name.py

import pygeolocate

for country in pygeolocate.locate_by_name("united"):
    print(country)
    print(country.name)
    print(country.coordinates)
    print(country.coordinates[0])
    print(country.coordinates['long'])
```
