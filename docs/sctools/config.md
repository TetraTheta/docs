# SC Tools Config

SC Tools uses configuration files to change some of its behavior.

## auto_god_map.txt { #auto_god_map }

[NPC Auto GodMode](feature.md#auto-godmode) will only be activated in maps defined in `auto_god_map.txt`.

??? abstract "Default content of `auto_god_map.txt`"
    
    ``` plaintext title="auto_god_map.txt"
    # Part of the 'NPC Auto GodMode' configuration. 'NPC Auto GodMode' will only be triggered on these maps.
    # You can add a comment using '#'.
    # '#' can be either the start of the line or the middle of the line. Any character after '#' will be ignored.
    # Half-Life 2
    d1_trainstation_01
    d1_trainstation_02
    d1_trainstation_03
    d1_trainstation_04
    d1_trainstation_05
    d1_trainstation_06
    d1_canals_01
    d1_canals_01a
    d1_canals_02
    d1_canals_03
    d1_canals_05
    d1_canals_06
    d1_canals_07
    d1_canals_08
    d1_canals_09
    d1_canals_10
    d1_canals_11
    d1_canals_12
    d1_canals_13
    d1_eli_01
    d1_eli_02
    d1_town_01
    d1_town_01a
    d1_town_02
    d1_town_02a
    d1_town_03
    d1_town_04
    d1_town_05
    d2_coast_01
    d2_coast_03
    d2_coast_04
    d2_coast_05
    d2_coast_07
    d2_coast_08
    d2_coast_09
    d2_coast_10
    d2_coast_11
    d2_coast_12
    d2_prison_01
    d2_prison_02
    d2_prison_03
    d2_prison_04
    d2_prison_05
    d2_prison_06
    d2_prison_07
    d2_prison_08
    d3_c17_01
    d3_c17_02
    d3_c17_03
    d3_c17_04
    d3_c17_05
    d3_c17_06a
    d3_c17_06b
    d3_c17_07
    d3_c17_08
    d3_c17_09
    d3_c17_10a
    d3_c17_10b
    d3_c17_11
    d3_c17_12
    d3_c17_12b
    d3_c17_13
    d3_citadel_01
    d3_citadel_02
    d3_citadel_03
    d3_citadel_04
    d3_citadel_05
    d3_breen_01
    # Half-Life 2: Episode 1
    ep1_citadel_00
    ep1_citadel_01
    ep1_citadel_02
    ep1_citadel_02b
    ep1_citadel_03
    ep1_citadel_04
    ep1_c17_00
    ep1_c17_00a
    ep1_c17_01
    ep1_c17_01a
    ep1_c17_02
    ep1_c17_02b
    ep1_c17_02a
    ep1_c17_05
    ep1_c17_06
    # Half-Life 2: Episode 2
    ep2_outland_01
    ep2_outland_01a
    ep2_outland_02
    ep2_outland_03
    ep2_outland_04
    ep2_outland_05
    ep2_outland_06
    ep2_outland_06a
    ep2_outland_07
    ep2_outland_08
    ep2_outland_09
    ep2_outland_10
    ep2_outland_10a
    ep2_outland_11
    ep2_outland_11a
    ep2_outland_11b
    ep2_outland_12
    ep2_outland_12a
    # Half-Life 2: Lost Coast
    d2_lostcoast
    ```

<h3>See also</h3>

* [Feature 'Auto GodMode'](feature.md#auto-godmode)

## auto_god_npc.txt { #auto_god_npc }

[NPC Auto GodMode](feature.md#auto-godmode) will only be activated for NPCs defined in `auto_god_npc.txt`.

You can get a list of classes for NPCs in the [Valve Developer Community](https://developer.valvesoftware.com/wiki/Category:NPCs).

??? abstract "Default content of `auto_god_npc.txt`"
    
    ``` plaintext title="auto_god_npc.txt"
    # Part of the 'NPC Auto God Mode' configuration. 'NPC Auto God Mode' will only be triggered on these NPCs.
    # You can add a comment using '#'.
    # '#' can be either the start of the line or the middle of the line. Any character after '#' will be ignored.
    # Don't add 'npc_citizen' in here! Colonel Odessa Cubbage will be handled automatically.
    # NPCs will only be set to 'god mode' if they are not hostile to the player. But if they become hostile to the player during midgame, you must attack them first to remove their god mode.
    npc_alyx
    npc_barney
    npc_eli
    npc_kleiner
    npc_magnusson
    npc_monk
    npc_mossman
    npc_vortigaunt
    ```

<h3>See also</h3>

* [Feature 'Auto GodMode'](feature.md#auto-godmode)

## npc_disable_input.txt { #npc_disable_input }

When SC Tools removes the NPC, it will pass a few inputs to the NPC to stop what it is doing, like shooting players.

You can get a list of classes for NPCs in the [Valve Developer Community](https://developer.valvesoftware.com/wiki/Category:NPCs) and find out valid inputs for NPCs.

??? abstract "Default content of `npc_disable_input.txt`"
    
    ``` plaintext title="npc_disable_input.txt"
    # You can add a comment using '#'.
    # '#' can be either the start of the line or the middle of the line. Any character after '#' will be ignored.
    # entity_class|input_name_1:input_name_2 param:...
    combine_mine|Disarm
    npc_alyx|HolsterWeapon
    npc_antlion|DisableJump:StopFightToPosition
    npc_antlionguard|ClearChargeTarget:DisableBark:DisablePreferPhysicsAttack:StopInvestigating
    npc_apcdriver|StopFiring:Stop
    npc_barnacle|LetGo
    npc_barney|HolsterWeapon
    npc_breen|HolsterWeapon
    npc_citizen|HolsterWeapon
    npc_clawscanner|ClearFollowTarget:DisableSpotlight
    npc_combine_camera|Disable:SetIdle
    npc_combine_s|HolsterWeapon:StopPatrolling
    npc_combinedropship|StopPatrol:SetGunRange 1
    npc_combinegunship|BlindfireOff:OmniscientOff:StopPatrol
    npc_cscanner|ClearFollowTarget:DisableSpotlight
    npc_eli|HolsterWeapon
    npc_fisherman|HolsterWeapon
    npc_gman|HolsterWeapon
    npc_helicopter|DisableDeadlyShooting:GunOff:MissileOff:StopPatrol
    npc_hunter|Crouch:DisableShooting
    npc_kleiner|HolsterWeapon
    npc_magnusson|HolsterWeapon
    npc_manhack|InteractivePowerDown
    npc_metropolice|HolsterWeapon
    npc_missiledefense|HolsterWeapon
    npc_monk|HolsterWeapon
    npc_mossman|HolsterWeapon
    npc_rollermine|InteractivePowerDown:TurnOff
    npc_sniper|DisableSniper:StopSweeping
    npc_stalker|HolsterWeapon
    npc_strider|DisableAggressiveBehavior:StopPatrol
    npc_turret_ceiling|Disable
    npc_turret_floor|Disable
    npc_turret_ground|Disable:InteractivePowerDown
    npc_vehicledriver|StopFiring:Stop
    npc_vortigaunt|HolsterWeapon
    ```

<h3>See also</h3>

* [Command `sc_remove`](command.md#sc_remove)

## small_model.txt { #small_model }

Props with these models will be considered ['small objects'](feature.md#small-objects).

??? abstract "Default content of `small_model.txt`"
    
    ``` plaintext title="small_model.txt"
    # You can add a comment using '#'.
    # '#' can be either the start of the line or the middle of the line. Any character after '#' will be ignored.
    models/combine_apc_destroyed_gib02.mdl
    models/combine_apc_destroyed_gib03.mdl
    models/combine_apc_destroyed_gib04.mdl
    models/combine_apc_destroyed_gib05.mdl
    models/combine_apc_destroyed_gib06.mdl
    models/props_c17/chair02a.mdl
    models/props_c17/tools_pliers01a.mdl
    models/props_c17/tools_wrench01a.mdl
    models/props_junk/garbage_metalcan001a.mdl
    models/props_junk/garbage_metalcan002a.mdl
    models/props_junk/garbage_milkcarton001a.mdl
    models/props_junk/garbage_milkcarton002a.mdl
    models/props_junk/garbage_newspaper001a.mdl
    models/props_junk/garbage_plasticbottle001a.mdl
    models/props_junk/garbage_plasticbottle002a.mdl
    models/props_junk/garbage_plasticbottle003a.mdl
    models/props_junk/garbage_takeoutcarton001a.mdl
    models/props_junk/metal_paintcan001a.mdl
    models/props_junk/metal_paintcan001b.mdl
    models/props_junk/popcan01a.mdl
    models/props_junk/shoe001a.mdl
    models/props_lab/binderblue.mdl
    models/props_lab/binderbluelabel.mdl
    models/props_lab/bindergraylabel01a.mdl
    models/props_lab/bindergraylabel01b.mdl
    models/props_lab/bindergreen.mdl
    models/props_lab/bindergreenlabel.mdl
    models/props_lab/binderredlabel.mdl
    models/props_lab/box01a.mdl
    models/props_lab/box01b.mdl
    models/props_lab/clipboard.mdl
    models/props_lab/jar01a.mdl
    models/props_wasteland/cafeteria_table001a.mdl
    models/props_wasteland/controlroom_chair001a.mdl
    models/props/cs_office/cardboard_box01.mdl
    models/props/cs_office/cardboard_box02.mdl
    models/props/cs_office/cardboard_box03.mdl
    models/props/cs_office/file_box_p1.mdl
    models/props/cs_office/file_box_p2.mdl
    models/props/cs_office/plant01_p1.mdl
    models/props/cs_office/trash_can_p1.mdl
    models/props/cs_office/trash_can_p2.mdl
    models/props/cs_office/trash_can_p3.mdl
    models/props/cs_office/trash_can_p4.mdl
    models/props/cs_office/trash_can_p5.mdl
    models/props/cs_office/trash_can_p6.mdl
    models/props/cs_office/trash_can_p7.mdl
    models/props/cs_office/trash_can_p8.mdl
    models/props/cs_office/water_bottle.mdl
    ```

## small_model_dir.txt { #small_model_dir }

Props with these models under these paths will be considered ['small objects'](feature.md#small-objects).

??? abstract "Default content of `small_model_dir.txt`"
    
    ``` plaintext title="small_model_dir.txt"
    # You can add a comment using '#'.
    # '#' can be either the start of the line or the middle of the line. Any character after '#' will be ignored.
    # Directory path must ends with '/'.
    models/gibs/
    models/humans/
    ```
