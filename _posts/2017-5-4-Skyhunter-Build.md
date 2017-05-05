---
layout: post
title: Skyhunter Build
published: true
---
## To Do List

1.Mount GPS in the wing
2.Mount Dragonlink Receiver in the opposite wing

|Channel|Output   |
|1      |Motor/ESC|
|2      |         |
|3      |Elevator |
|4      |L Aileron|
|5      |R Aileron|
|6      |Rudder   |

Skyhunter Nano (no rudder)

mixer CUSTOMAIRPLANE
mmix reset
mmix 0 1.000 0.000 0.000 0.000
smix reset
smix 0 3 0 -100 0 0 100 
smix 1 4 0 -100 0 0 100 
smix 2 2 1 -100 0 0 100 
