Guishushu Traffic Light Control System - UML Statechart Diagram
=====================================================

This README file provides an overview of the Guishushu traffic light control system modeled in the UML Statechart Diagram. The diagram represents an intersection with four directions: North, South, East, and West, where each direction takes turns displaying green and yellow lights to manage traffic flow safely and effectively.

Components
----------

1. **Initial State**:
   - The system starts with all lights set to red, allowing no vehicles to pass from any direction.

2. **Directional States**:
   - The system has four primary states, one for each direction:
     - **North Direction**
     - **South Direction**
     - **East Direction**
     - **West Direction**
   - Each direction has a:
     - **Green Phase**: The specified direction displays a green light, allowing vehicles to pass while all other directions remain red.
     - **Yellow Phase**: After the green phase, the light turns yellow for a short duration, signaling vehicles to prepare to stop.

3. **Transitions**:
   - The diagram shows state transitions based on timing events:
     - **Green Duration Ends**: Transitions the active direction from green to yellow.
     - **Yellow Duration Ends**: Transitions the active direction from yellow to red, moving to the "All Directions Red" state before the next direction.
   - Example transitions:
     - **North Direction**: "North Green, Others Red" → "North Yellow, Others Red" → "All Directions Red"
     - **East Direction**: "East Green, Others Red" → "East Yellow, Others Red" → "All Directions Red"
     - **South and West Directions** follow the same pattern.

4. **Cycle Restart**:
   - After all four directions (North, East, South, and West) complete their green-yellow sequence, the system briefly returns to "All Directions Red" before restarting the cycle.

5. **Loop Structure**:
   - The traffic light control system loops through each direction in sequence. After each directional state completes, the next direction takes its turn with a green light, followed by yellow, and back to red.

Purpose of the Diagram
----------------------
This UML Statechart Diagram models a structured, time-based sequence to control traffic lights at an intersection, ensuring only one direction shows a green light at any time. This design prevents collisions and provides an orderly flow of vehicles through the intersection.

Usage
-----
This model can serve as a reference for implementing traffic light control systems in real-world intersections, where precise timing manages the green and yellow phases for each direction.
