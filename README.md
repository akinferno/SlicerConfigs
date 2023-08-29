# SlicerConfigs
A place to keep track of my slicer profiles.

I include skirts as a variable to eliminate the purge if the skirt has more than 1 ring on my Ender.

Gcode sample for Superslicer:
PRINT_START EXTRUDER_TEMP={first_layer_temperature[initial_extruder] + extruder_temperature_offset[initial_extruder]} BED_TEMP={first_layer_bed_temperature} CHAMBER={chamber_temperature} EXTRUDE_RATE={100 * extrusion_multiplier} SKIRT={skirts}

Gcode sample for Prusa Slicer (Not tested yet):
PRINT_START EXTRUDER_TEMP={first_layer_temperature[initial_extruder]} BED_TEMP=[first_layer_bed_temperature] EXTRUDE_RATE=[extrusion_multiplier] SKIRT={skirts}

Gcode sample for Cura slicer:
PRINT_START BED_TEMP={material_bed_temperature_layer_0} EXTRUDER_TEMP={material_print_temperature_layer_0} EXTRUDE_RATE={material_flow_layer_0} CHAMBER={build_volume_temperature} 

Gcode sample for OrcaSlicer:
PRINT_START EXTRUDER_TEMP=[nozzle_temperature_initial_layer] BED_TEMP=[bed_temperature_initial_layer_single] CHAMBER=[chamber_temperature] EXTRUDE_RATE=[filament_flow_ratio]  SKIRT=[skirt_loops]
