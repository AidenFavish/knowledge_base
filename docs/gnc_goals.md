# GNC Goals

## Mission Timeline
The timeline of everything GNC should be thinking about for a mission.

1. Power the drone, power the router, turn on the GCS

2. GCS application should automatically connect to FC and Jetson

3. Run through the checklist (vehicle type, calibrations, peripheral checks, input waypoints, arm script)

4. Arm from remote controller to initiate script

5. Takeoff to 165 ft (~50 m) - 200 ft (~60 m) depending on vehicle to avoid 150 ft minimum altutude floor

6. Do maximum number of waypoint laps we can while still being able to RTL (monitor range, time, and have consistent and predictable soc drain function for scanning, dropping and mapping)

7. Scan the search area

8. Fly to nearest target (manequin or tent) and drop corresponding payload (bottle or beacon respectively)

9. Repeat #8

10. Map the rest of the search area

11. RTL

## Big Ideas

- Build a user friendly and intuitive GCS that can do everything from power on to final landing neccessary (commercial product level)

- Efficient flying, the more optimized path planning, the better

- Aggressive automated real time unit tests to simulate the judges scrutiny on rules

- Safe, predictable, consistent, easy missions

## Quarterly Plan

### Fall Quarter
- Competition ready quadcopter flight script

- Finished GCS (supporting quadcopter flight)

- Automated mission rules validation tests

### Winter Quarter

- Well-polished GCS that can support both quadcopter and fixed wing missions

- Basic fixed wing mission script (regular ArduPlane)

- Find and set up a physics enabled simulation for fixed wing control testing (preferably interfacing with SITL)

### Spring Quarter

- Well-tuned fixed wing mission script (forked modded ArduPlane firmware)

- Improve fixed wing control, consistency and reliability
