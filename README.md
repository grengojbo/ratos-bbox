# ratos-bbox
Custom configuration RatOS


## List STATES

RatOS - SAVE_GCODE_STATE

  - PAUSE_state
  - prime_line_state
  - prime_blob_state
  - unload_state
  - load_state
  - start_print_state
  - end_print_state
  - probe_for_priming_state
  - probe_current_position_state
  - screws_tilt_state
  - STATE_G32
  - probe_calibrate

Klipper State ?

  - STATUS_READY
	- STATUS_OFF
	- STATUS_BUSY
	- STATUS_HEATING
	- STATUS_LEVELING
	- STATUS_HOMING
	- STATUS_CLEANING
	- STATUS_MESHING
	- STATUS_CALIBRATING_Z

# With additional macros for basic control:

  - SET_NOZZLE_LEDS_ON
  - SET_LOGO_LEDS_OFF
  - SET_NOZZLE_LEDS_OFF

Ecample set state:

```
SAVE_GCODE_STATE name=probe_calibrate
STOW_PROBE
RESTORE_GCODE_STATE name=probe_calibrate MOVE=1 MOVE_SPEED={RatOS.macro_travel_speed|float}
```