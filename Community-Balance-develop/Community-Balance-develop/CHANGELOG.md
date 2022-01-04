# CHANGELOG

IDs can be cross referenced with the [balance spreadsheet](https://docs.google.com/spreadsheets/d/13tNI8PFfEiwCAUHOaHBhuule5bAcmYr37FjSdI8NggE).

## Unreleased

### Balance

#### Air

- ID21: Hummingbird
  - `max_health` reduced from 150 to 120
- ID21: Phoenix
  - `max_health` reduced from 300 to 240
- ID23: Hornet
  - `max_health` increased from 200 to 600
  - `build_metal_cost` increased from 1500 to 3200
  - `rate_of_fire` increased from 0.25 to 0.5
  - `max_range` increased from 180 to 190
  - `max_velocity` for missiles increased from 80 to 160
  - `move_speed` reduced from 40 to 30
- ID24: Zeus
  - `max_health` increased from 10,000 to 12,000
  - `rate_of_fire` increased from 0.5 to 0.55 shots/sec
  - `ammo_demand` increased from 5000 to 5500 energy/sec
- ID39: Icarus
  - `target_priorities` changed:
    - Fabber
    - AirDefense
    - Mobile & (Land | Naval)
- ID52: Kestrel
  - `max_health` reduced from 300 to 250
  - `max_range` reduced from 80 to 60
  - `damage` increased from 15 to 20

#### Land

- ID1: Dox
  - `move_speed` increased from 19 to 20
  - `acceleration` reduced from 190 to 50
- ID1: Stryker
  - `move_speed` reduced from 18 to 17
  - `max_range` reduced from 80 to 75
- ID2: Spark
  - `max_range` reduced from 70 to 65
- ID4: Ant
  - `rate_of_fire` increased from 0.5 to 0.55 shots/sec
- ID5: Drifter
  - `damage` reduced from 125 to 120
  - `max_range` reduced from 115 to 110
- ID6: Grenadier
  - `firing_standard_deviation` increased from 1 to 1.5
  - `splash_damage` removed
  - `splash_radius` removed
  - `full_damage_splash_radius` removed
- ID8: Advanced Laser Tower
  - `range` increased from 120 to 130
  - `rate_of_fire` increased from 3 to 5 shots/sec
- ID9: Lob
  - `rate_of_fire` increased from 3 to 4.5 shots/sec
  - `ammo_demand` reduced from 15 to 13 metal/sec
  - `ammo_capacity` decreased from 500 to 432
  - `ammo_per_shot` decreased from 60 to 50
- ID10: Colonel
  - `build_metal_cost` reduced from 7000 to 6000
  - `max_health` reduced from 8000 to 6000
  - `max_range` on build arm increased from 20 to 30
- ID11/ID43: Manhattan
  - `move_speed` increased from 7 to 10
  - `turn_speed` increased from 45 to 60
  - `turn_accel` increased from 15 to 30
- ID12: Vanguard
  - `max_range` increased from 30 to 50
  - `rate_of_fire` increased from 0.5 to 1 shot/sec
  - `damage` reduced from 2000 to 1000
  - `splash_damage` reduced from 2000 to 1000
- ID13: Mend
  - `max_health` increased from 150 to 350
- ID15: Slammer
  - `rate_of_fire` for torpedo increased from 0.25 to 0.75 shots/sec
- ID20: Stinger
  - `move_speed` increased from 12 to 16
- ID25: Atlas
  - `max_health` increased from 40,000 to 60,000
- ID26: Ares
  - `max_health` reduced from 80,000 to 50,000
  - `tools` close range stomp attack removed
- ID27: Unit Cannon
  - `unit_types` UNITTYPE_CannonBuildable added to Storm
  - `build_metal_cost` reduced from 10,000 to 6800
  - `spawn_layers` changed from WL_LandHorizontal to WL_AnyHorizontalGroundOrWaterSurface
- ID28: Advanced Metal Extractor
  - `max_health` reduced from 5000 to 3000
  - `production` `metal` increased from 16 to 18
  - `build_metal_cost` reduced from 2000 to 1800
- ID31: Energy Storage
  - `storage` `energy` increased from 100,000 to 300,000
- ID37: Single Laser Tower
  - `max_health` increased from 350 to 400
  - `yaw_rate` increased from 60 to 90
  - `damage` increased from 40 to 60
- ID47: Leveler
  - `max_range` reduced from 140 to 130

#### Naval

- ID15: Barnacle
  - `move_speed` increased from 10 to 12
- ID15: Barracuda
  - `ignore_radar` removed
  - `description` updated (THIS IS USING AN OLD TRANSLATION STILL IN THE GAME)
- ID15: Narwhal
  - `tools` torpedo weapon added
    - `rate_of_fire` 0.4 shots/sec
    - `max_range` 150
    - `damage` 250
  - strategic icon updated
  - build bar icon updated
  - DESCRIPTION MENTIONS SEA TARGETS BUT NOT UNDERSEA BUT WAS LEFT AS IS TO AVOID TRANSLATION IMPACT - RECOMMEND UPDATING ENGLISH TRANSLATION FOR ACCURACY
- ID15: Orca
  - `tools` torpedo weapon removed
  - strategic icon updated
  - build bar icon updated
  - `description` updated (BREAKS EXISTING TRANSLATIONS - ALTERNATE OPTION IS RETAINING ORIGINAL DESCRIPTION BUT UPDATING ENGLISH TRANSLATION FOR ACCURACY)
- ID15: Piranha
  - `max_range` reduced from 120 to 105
- ID19: Stingray
  - `target_layers` for tactical missile changed to include WL_Air
  - `target_priorities` for tactical missile changed:
    - "Air & (Tactical | Heavy)",
    - "Mobile - Air",
    - "Structure - Wall",
    - "Mobile & Air",
    - "Wall"

#### Orbital

- ID29: Jig
  - `storage` removed
  - `production` `energy` reduced from 7000 to 3750
  - `armor_damage_map` updated to prevent damage to mobile units by death explosion
- ID30: Solar Array
  - `production` `energy` increased from 2500 to 3200
- ID34: Omega
  - `damage` on side guns reduced from 65 to 30 (NOTE THAT orbital_battleship_tool_weapon.json `ammo_id` WAS CHANGED TO THE NEW FILE orbital_battleship_ammo.json TO ALLOW FOR THIS)
  - `rate_of_fire` on side guns increased from 1 to 2 shots/sec
  - `target_layers` on side guns changed:
    - WL_Orbital
    - WL_Air
    - WL_LandHorizontal
    - WL_WaterSurface
  - `pitch_range` on side guns increased from 60 to 180

### Bugfix

- ID8: Advanced Laser Tower can no longer be shot over the top of walls by direct fire units
  - `mesh_bounds` height reduced from 23 to 19
- ID23: Gil-E delay in intercepting missiles corrected
  - `idle_aim_delay` reduced from 0.1 to 0
  - `nearby_target_tick_update_interval` reduced from 15 to 2
- ID38: Galata can damage Astraeus again
  - `armor_damage_map` AT_Orbital removed
- ID38: Storm can damage Astraeus again
  - `armor_damage_map` AT_Orbital removed
- ID45: Colonel turns changed to avoid them getting stuck
  - `turn_in_place` set to true
  - `turn_speed` increased from 90 to 180
- ID45: Commander turns changed to avoid them getting stuck
  - `turn_in_place` set to true
  - `turn_speed` increased from 90 to 180
- ID52: Kestrel guards properly
  - `guard_layer` changed from WL_Anysurface to WL_AnySurface
