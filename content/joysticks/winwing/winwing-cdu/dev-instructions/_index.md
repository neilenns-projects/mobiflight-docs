---
title: Developer instructions
weight: 70
---

## General concept

For each supported plane a python script will be shipped with MobiFlight. The python script fetches the data from the plane interface and pushes it to the MobiFlight websocket interface. Everyone can contribute those python scripts and after an evaluation, we might add them. For questions ask in the MobiFlight discord using the "development channel".

The currently provided scripts can be found in the MobiFlight installation folder in `\Scripts\Winwing`. For example `\Scripts\Winwing\fenix_winwing_cdu.py`

Please try to minimize the use of extra python packages. Use the same packages as already used in other existing scripts. For example "websockets" or "gql" in the fenix example. Also put everything in one python file.

MobiFlight websocket Interface:

```text
ws://localhost:8320/winwing/cdu-captain
ws://localhost:8320/winwing/cdu-co-pilot
ws://localhost:8320/winwing/cdu-observer
```

## Data format to be send

Json structure with a list of 336 elements in the Data section for the 336 possible chars on the CDU.

- Each list element is a triplet.
    1. The character to be shown as UTF-8 string
    2. The color as UTF-8 string
    3. The size as a number (0 large, 1 small).
- For empty character "SPACE", also an empty list element [] can be used, instead of [" ", "w", 0].

## Color identifiers

```text
"a" // amber
"w" // white          
"c" // cyan        
"g" // green            
"m" // magenta          
"r" // red            
"y" // yellow            
"o" // brown
"e" // grey 
"k" // kahki
```

## Special chars

For special chars like <- or -> use the unicode syntax. For example in python:

```python
'\u2610'  # ballot box
'\u2191'  # up arrow
'\u2193'  # down arrow
'\u2192'  # right arrow
'\u2190'  # left arrow
'\u0394'  # greek delta for overfly
```

## Example json

```json
{
    "Target": "Display",
    "Data": [ [], [], [], [], [], [], [], ["M", "w", 0], ["C", "w", 0], ["D", "w", 0], ["U", "w", 0], ... ]
}
```

**Full example:**

```json
{"Target": "Display", 
 "Data": [[], [], [], [], [], [], [], ["M", "w", 0], ["C", "w", 0], ["D", "w", 0], ["U", "w", 0], [], ["M", "w", 0], ["E", "w", 0], ["N", "w", 0], 
  ["U", "w", 0], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], 
  ["<", "g", 0], ["F", "g", 0], ["M", "g", 0], ["G", "g", 0], ["C", "g", 0], [], [], [], [], [], [], [], [], [], [], [], [], ["C", "w", 0], 
  ["O", "w", 0], ["N", "w", 0], ["F", "w", 0], ["I", "w", 0], ["G", "w", 0], [">", "w", 0], [], [], [], [], [], [], [], [], [], [], [], [], [], [], 
  [], [], [], [], [], [], [], [], [], [], ["<", "w", 0], ["A", "w", 0], ["T", "w", 0], ["S", "w", 0], ["U", "w", 0], [], [], [], [], [], [], [], [], 
  [], [], [], [], [], ["M", "w", 0], ["A", "w", 0], ["I", "w", 0], ["N", "w", 0], ["T", "w", 0], [">", "w", 0], [], [], [], [], [], [], [], [], [], 
  [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], 
  [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], 
  [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], 
  [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], 
  [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], [], 
  ["S", "w", 0], ["E", "w", 0], ["L", "w", 0], ["E", "w", 0], ["C", "w", 0], ["T", "w", 0], [], ["D", "w", 0], ["E", "w", 0], ["S", "w", 0], 
  ["I", "w", 0], ["R", "w", 0], ["E", "w", 0], ["D", "w", 0], [], ["S", "w", 0], ["Y", "w", 0], ["S", "w", 0], ["T", "w", 0], ["E", "w", 0], 
  ["M", "w", 0], [], [], []]}
```
