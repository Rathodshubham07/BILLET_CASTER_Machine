## 2.4. Field Sensor & Instrument:

Billet casting machine contains following field sensors & instruments

- Clamp proximity
- De-clamp proximity
- Saw motor assembly home position proximity
- Saw motor assembly end position proximity
- Limit switch
- Photo sensor
- Cylinder A+ (Reed Switch)
- Cylinder A- (Reed Switch)
- Cylinder B+(Reed Switch)
- Cylinder F- (Reed Switch)
- Cylinder B- (Reed Switch)
- Cylinder C+ (Reed Switch)
- Cylinder C- (Reed Switch)
- Cylinder D+ (Reed Switch)
- Cylinder D- (Reed Switch)
- Cylinder E+ (Reed Switch)
- Cylinder E- (Reed Switch)
- Cylinder F+ (Reed Switch)

### 2.4.2. Working Philosophy:

For starting the machine the healthy condition are as follows:

- All emergency released.
- Temperature level of the furnace.
- Water level for cooling water pump.
- Saw motor table assembly at home position.

If all these condition is satisfied then and then only machine can be started.

For starting the machine operation we have to press the Main Start push button from  push button station 1 and there is also a Main Stop push button on PB station 1 this button will off the total machine operation. On push button station 1 a toggle switch is present which will be used for switchon and switchoff the control voltage of the drive motor. For controlling the speed of the drive motor there is a Potentiometer from which operator can adjust the speed of drive motor. This drive motor is used for conveying the BILLET in forward direction.

When machine started first time at the first start-up of machine, traction bar is present in the machine this will holds the billet and moves in forward direction. There are two traction rollers present and the gap between these two traction rollers is adjusted by using spring return selector switch which is present on push button station 3. After that traction bar is removed from the billet manually. When billet is on first conveyer the water pump will be start and this operation is done by operator manually.

After this point the machine can be operated in two modes i.e. Auto mode and Manual mode. And this mode selection is done by auto/manual button which is present on push button station 4.

### 2.4.3. Machine in Auto mode:

When operator select the Auto mode all the operation is done by machine is automatically.

There are two field instrument i.e. Limit switch and Photo sensor present on the machine for calculating the length of the billet. The limit switch is 1.2 meter distance away from billet cutting saw and photo senor is 1.8 meter distance away from billet cutting saw. As per requirement of the billet length any of these field instruments gives feedback to the PLC which is used in the program for further operation. When we get the feedback the sequence of operation is performed.

The sequences of operations are as per given bellow:

**Clamping:** In this process the two mechanical arms are connected to the billet. There are two proximity switches present on that mechanical arm from which we can identify that clamping is done or not.

**Saw motor operation:** As soon as clamping is done saw motor is turn on. Saw motor moves in only one direction.

**Saw motor head operation:** After saw motor on the head of the saw motor is lowered. Normally head of the saw motor is in raise condition.

**Saw motor head assembly motion**: when saw motor head is lowered the saw motor head assembly is starting to move from operator side to drive side. This operation is controlled by pneumatically with chain arrangement. For identifying the location of the saw motor head assembly there are two proximity switches present on the machine.( Home position proximity and End position proximity)

When saw motor head assembly reach to the end of the billet the end position proximity is activated and gives feedback signal to the PLC. When PLC get the signal from end position proximity it will take the appropriate action on it i.e. head of the saw motor raised to its normal position and saw motor head assembly starts moving from drive side to operator side by using that pneumatically with chain arrangement. When saw motor head assembly is came back to its normal position this will activate the home position proximity and saw motor head assembly motion is stopped.

**De-clamping:** When saw motor head assembly came back to its original home position the de-clamping of that mechanical arm is done. Due to this de-clamping process the saw motor table is detached from the billet. As soon as de-clamping is done the saw motor is turned off.

**Saw motor table operation:** When clamping is done the saw motor table is moving in forward direction along with the billet. Due to this for next cycle we have saw motor table at its home position. That’s why when de-clamping is done the saw motor table moves to its home position. There is one proximity switch for identifying the table home position.

This whole cycle repeated continuously from clamping the billet to saw motor table return back to its home position.

### 2.4.3 Machine in Manual mode:

When manual mode from push button station 4 is selected following operation performed independently with each other.

**Saw raise (PB):** Saw raisepush button is used toraise the saw motor head. This will activate one of the solenoid valve from solenoid valve bank.

**Saw lower (PB):** Saw lowerpush button is used for lower the saw motor head. This will activate one of the solenoid valve from solenoid valve bank.

**Saw forward (PB):** Saw motor head is moved from operator side to drive side.

**Saw return (PB):** Saw motor head is moved from driver side to operator side.

Saw motor on (PB): Saw motor on push button will turn on the saw motor.

**Saw motor off (PB):** Saw motor off push button will turn off the saw motor.

**Clamp (PB):** Clamp push button will clamp the mechanical arm to the forward moving billet due to this the whole saw motor table assembly moves forward with the billet.

**De-clamp (PB):** De-clamp push button will de-clamp the mechanical arm from the forward moving billet. Afterde-clamping saw motor assembly is detached from forward moving billet.

**Eject raise (PB):** Eject raise push button will raise the eject assembly.

**Eject lower (PB):** Eject lower push button will lower the eject assembly.

**Table return (PB):** Table return push button will moves the saw motor table in forward direction with the billet.

**Table release (PB**): Table release push button will release the saw motor table and table came back to its home position.

After cutting the billet of 1.2 meter or 1.8 meter billet is moved to the next process by using conveyer motor. The operation of conveyer motor is handled manually by using DOL starter push button station.

Then this billet is given to the billet cutting motor. This section contains 3 DOL motors. And these motors are controlled manually by using DOL starter push button station.

### 2.4.4. **Input and output list:**

Following inputs are considered in this project.

| **SR.NO.** | **DESCRIPTION** | **FIELD INSTRUMENT** |
| --- | --- | --- |
| 1 | MACHINE START | PUSH BUTTON |
| 2 | MACHINE STOP | PUSH BUTTON |
| 3 | AUTO MODE | SPSS |
| 4 | MANUAL MODE | SPSS |
| 5 | EMERGENCY STOP | MPB |
| 6 | TRACTION DRIVE MOTOR | CONTACTOR TRIP FEEDBACK |
| 7 | SAW MOTOR TRIP | CONTACTOR TRIP FEEDBACK |
| 8 | CONTROL VOLTAGE ON/OFF | TOGGEL SWITCH |
| 9 | SAW MOTOR ON | PUSH BUTTON |
| 10 | SAW MOTOR OFF | PUSH BUTTON |
| 11 | CLAMP | PUSH BUTTON |
| 12 | CLAMP | REED SWITCH |
| 13 | CLAMP | PROXIMITY |
| 14 | DE-CLAMP | PUSH BUTTON |
| 15 | DE-CLAMP | REED SWITCH |
| 16 | SAW MOTOR HEAD UP | PUSH BUTTON |
| 17 | SAW MOTOR HEAD DOWN | PUSH BUTTON |
| 18 | SAW MOTOR HEAD UP | REED SWITCH |
| 19 | SAW MOTOR HEAD DOWN | REED SWITCH |
| 20 | SAW MOTOR HEAD FORWARD | PUSH BUTTON |
| 21 | SAW MOTOR HEAD REVERSE | PUSH BUTTON |
| 22 | SAW MOTOR HEAD AT HOME POSITION | PROXIMITY |
| 23 | SAW MOTOR HEAD AT END POSITION | PROXIMITY |
| 24 | SAW MOTOR TABLE FORWARD | PUSH BUTTON |
| 25 | SAW MOTOR TABLE REVERSE | PUSH BUTTON |
| 26 | BILLET PRESENT (1.8M) | PHOTOSENSOR |
| 27 | BILLET PRESENT (1.2M) | LIMIT SWITCH |

\

Following outputs are considered in this project.

| **SR.NO.** | **DESCRIPTION** | **FIELD INSTRUMENT** |
| --- | --- | --- |
| 1 | TRACTION DRIVE MOTOR ON COMMAND | CONTACTOR ON COMMAND |
| 2 | SAW MOTOR ON COMMAND | CONTACTOR ON COMMAND |
| 3 | CLAMP | SOV. A+ |
| 4 | DE-CLAMP | SOV. A- |
| 5 | SAW MOTOR HEAD UP | SOV. B+ |
| 6 | SAW MOTOR HEAD DOWN | SOV. B- |
| 7 | SAW MOTOR HEAD FORWARD | SOV. C+ |
| 8 | SAW MOTOR HEAD REVERSE | SOV. C- |
| 9 | SAW MOTOR TABLE HOME POSITION | SOV. D+ |
|  |  |  |

These are all input and output considered in this project.

All Emergency push button are kept in series. Any emergency push button is pressed it will stop the whole machine operation.
