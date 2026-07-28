Smart Gates & Safety Buffers (SGSB) — v3.0.3-72826(Heavy Fruit Hotfix)
"The House That Code Built"

A Note from the Developer
  This project is dedicated to the glory of God. Every mile driven and every line of code written is an expression of gratitude for the journey. May this mod bring a little more order, peace, and grace to the virtual highways we all travel. This is our first mod ever, so please extend us some grace!

Full Release Log
https://github.com/insanity35/Smart-Gates-Tolls-and-Safety-Buffers

**NOTICE Because it seems SOME DLC gates lack definition files, you cannot target them by adding code to a definition list. So i have to manually unpack state DLC files to look for gate codes. These will come in future updates like the massive 3.0 update. But some gates at yards and areas are hard coded and there is nothing I can do. **

The Problem: "Gate Lag"
	After years of long-haul trucking in American Truck Simulator, we know that immersion is everything. Nothing kills the flow of a delivery faster than "gate lag"—that frustrating moment when you are at the yard threshold, waiting for a barrier to crawl open while your multi-ton rig is already stalled out.
The Solution: Smart Gates & Safety Buffers

SGSB is the definitive logic overhaul for gate operations. We have stripped away the inconsistent, immersion-breaking triggers of the base game and replaced them with a standardized, high-performance logic set.

Whether you are hauling heavy cargo into a Phoenix warehouse or navigating a tight depot in the Midwest, your gates will now respond with the reliable precision a professional driver expects. Built by a driver, for drivers.

Quick Reference
	Logistics Master Triggers: 55.0m for industrial yards and sliding gates.
  	Orientation Tolerance: Optimized to 60° to catch your approach angle early on tight compound turns.
  	Toll Plazas (Precision Lanes): Tuned to 10.0m for a smoother, more forgiving clearance window.
  	Toll Plazas (Standard Lanes): Left untouched at 23.0m.  
  	Depot Storage Doors: Set to 20.0m to completely eliminate slow-opening bay snags and trailer clipping.
  	
Official Release Information
    Current Version: v3.0.3-72826(Heavy Fruit Hotfix)(Stable)
    Official Launch Date (v1.0): Tuesday, July 14, 2026
    ATS Compatibility: v1.60.* branch (Until SCS breaks the core gate code)
    Development Environment: Ubuntu 26.04 LTS via Linux
    Architecture: Pure definition-only (.sii) layout

Complete Mod Genesis & Release History
The Early Development Phase

    June 2026 [Alpha Phase: Extraction & Mapping]: Natively developed on Ubuntu 26.04. Utilized the sk-zk Extractor tool to dissect def.scs and base.scs. Performed a deep-dive code analysis to map game logic specifically within animated_gate blocks and identify critical trigger/reset dependencies.

    July 10–11, 2026 [Beta Testing: Stress Testing the Framework]: Field-tested across high-density industrial hubs in Phoenix and Stockton. Confirmed 100% Convoy-ready multiplayer compatibility with zero "mod-mismatch" errors.

    July 11–14, 2026 [Release Candidate 1.0: Real-World Discoveries]: Implemented a standardized 47m trigger distance for all industrial yard gates to ensure full clearance for double and triple trailer combinations. Discovered during a vacation road trip that the engine handles rest distances automatically now; native reset code remains commented out until v1.7.

    July 14, 2026 [Version 1.0.0: Public Launch]: Initial public release. Successfully moved gate trigger zones significantly further away from the physical frames.

Version History & Changelog Evolution
	
	v3.0.3-72826(Heavy Fruit)
			Depot & Warehouse Doors: Tuned to 50m–60m for clean dock backing without highway false triggers.
			Precision Tolls: Locked cash booths to 14m.
			Parser Fix: Corrected Oregon Storage to gate.metal_01.
			Heavy Yards & Map Mods: Maintained at 85m–100m for smooth momentum.
			Dual-Path Ready: Verified for both def/world/ and unit/hookup/.
			Clean Layout: Added high-visibility headers across all 50 groups.

	v3.0.2-72826(HEAVY FRUIT Hotfix)
    Dual-Directory Sync: This exact code serves as the unified blueprint for both the def/world/ (editor-placed gates) and unit/hookup/ (prefab-spawned gates) directories, ensuring 100% map coverage.
    Trigger Bump: Logistics Master (Section 03) trigger_distance increased to 90.0m for all three gate variants to fully accommodate long-nose setups.
    Engine Compliance: Filename standardized to the engine-hardcoded animated_gate.sii to force the game to overwrite vanilla baseline stats.
    Toll Integrity: Zero changes to toll barriers or border checks; all parameters remain strictly locked to baseline.
    
	   v3.0.0-72726(PROJECT HEAVY FRUIT)
		Everything from 2.1
		Smart Gates & Safety Buffers (SGSB) — v3.0.0 [PROJECT HEAVY FRUIT]
	Master Change Manifest: Complete Record of All Additions & Adjustments
	The following is the exhaustive, definitive accounting of every single change, addition, and parameter optimization integrated into the v3.0 master build (animated_gate.sgsb.sii) for American Truck Simulator (ATS v1.60)
	
	Part 1: All Core Parameter Changes (The Smoothness & Long-Nose Calibration)
	To eliminate truck nose-clipping (such as with long-nose configurations like the Kenworth W900) and prevent raycasting lag at highway speeds, every existing parameter block was systematically scaled up:
	Trigger Distances (trigger_distance): Uniformly bumped across all tiers by +3m to +10m to grant the physics engine predictive lead time:
	Standard Tolls (E-ZPass): Increased from 28.0m to 32.0m
	Precision Tolls (Cash Booths): Increased from 13.0m to 15.0m
	Logistics & Slide Gates: Increased from 75.0m to 85.0m
	Heavy Industrial & Ports: Scaled up to 100.0m
	Angular Tolerances (orientation_tolerance): Widened by +5° to +15° to catch wide-swinging turns and diagonal yard entries without dropping trigger states:
	Tolls: Expanded from 35.0° to 40.0°
	Logistics Masters: Expanded from 70.0° to 80.0°
	Maritime & Ferry Ports: Scaled up to 120.0°
	Lateral Offsets (trigger_offset): Fine-tuned across multi-lane prefabs to +/-3.5m through +/-4.5m to reliably catch vehicles hugging either side of wide entry lanes.
	
	Part 2: All Newly Added DLC Prefabs & Specialized Yards (Groups 22–35)
	The master index was expanded to incorporate specialized corporate, regional, and state DLC assets:
	[Group 22] Retail Car Lots (gate.car_dealership_01): Suburban automotive display and security gates.
	[Group 23] Agricultural Co-Ops (gate.ag_coop_01): Midwest grain elevator and farm supply access points.
	[Group 24] Historic Waypoints (gate.historic_park_01): Route 66 and state park decorative wood/stone-pillar pivot barriers.
	[Group 25] River Locks & Barges (gate.river_lock_01): Commercial waterway lock gates and barge terminals.
	[Group 26] Heavy Rolling Freight Yards (gate.heavy_rolling_01): Intermodal container terminal rolling gates.
	[Group 27] Multi-Bay Freight Docks (gate.multibay_freight_01): High-throughput warehouse drop-off docks with electric actuation.
	[Group 28] Municipal City Yards (gate.muni_service_01): Local public works and service department security gates.
	[Group 29] Inland River Ports (gate.river_port_01): Heavy shipping terminal gates linking water and highway logistics.
	[Group 30] Aerospace Facilities (gate.aero_sec_01): High-security defense and manufacturing compound gates (TX/WA).
	[Group 31] Livestock Auctions (gate.livestock_01): Specialized ranch and livestock transport yards (WY/NE/KS).
	[Group 32] Quarry & Mine Booms (gate.quarry_boom_01): Aggregate extraction site pneumatic check-booms (CO/MT).
	[Group 33] Oil & Gas Drill Sites (gate.oil_site_01): Remote energy extraction security barriers (TX/OK).
	[Group 34] Sawmill Pivots (gate.sawmill_01): Regional timber and lumber processing mill gates (AR/PNW).
	[Group 35] Midwest Manufacturing (gate.ethanol_plt_01 & gate.meat_pack_01): Dedicated ethanol processing plants and industrial meatpacking facilities (MO/IA).
	
	Part 3: All Map Mod Integration Layers Added (Groups 36–40)
	Native configuration bindings were built directly into Tier 3 to eliminate the need for separate sub-mod compatibility patches:
	[Group 36] Reforma Expansion (gate.ref_toll01 to gate.ref_farm_01): Calibrated parameters for Mexican/Central American highway toll plazas (casetas), customs border control (garitas), and ranch gates.
	[Group 37] ProMods Canada (gate.pm_border1 to gate.pm_timber01): Profiled for Canadian Border Services Agency (CBSA) inspection lanes, BC ferry terminals, and northern timber logging trails.
	[Group 38] Sierra Nevada (gate.sn_ag_check01 & gate.atx_intermodal_01): Configured for California Department of Food and Agriculture (CDFA) agricultural check stations and regional intermodal rail yards.
	[Group 39] Coast to Coast (C2C) Hubs (gate.c2c_toll_01 & gate.c2c_yard_01): Mapped custom C2C highway toll barrier prefabs and freight yard gates.
	[Group 40] Great America Industrial (gate.ga_wide_01): Integrated oversized industrial security gates profiled specifically for wide-layout prefabs in the Great America map mod.
	
	Part 4: Structural & Architectural Overhauls
	Sequential 40-Group Master Index: Completely restructured the configuration from legacy naming into a clean, strictly sequential numbering scheme (01 to 40) across three distinct tiers to eliminate load-order conflicts.
	ATS v1.61 Engine Alignment: Vetted against experimental physics updates to ensure zero frame stutter or desynchronization during rapid proximity raycasts.
	
	Part 5: Illinois & Louisiana DLC Expansion Nodes (Groups 36–38)
	[Group 36] Gulf Coast Maritime (LA) (gate.shipyard_01, gate.lng_terminal_01, gate.salt_mine_01): Integrated specialized heavy iron and pneumatic security barriers for Port Fourchon shipyards, LNG export terminals, and regional salt mining infrastructure.
	[Group 37] Great Lakes Heavy Industrial (IL) (gate.chi_intermodal_01, gate.const_equip_01, gate.marina_sec_01): Configured wide-layout access gates for Chicago intermodal rail hubs, heavy construction equipment manufacturing plants, and regional waterfront security points.
	[Group 38] Federal & Energy Security (NM/TX/AR) (gate.military_base_01, gate.energy_sec_01): Mapped high-clearance military reservation gates and critical energy infrastructure power plant barriers.
	
	Part 6: National Parks, Research Facilities & Hidden Landmarks (Groups 39–45)
	[Group 39] National Parks & Air Cargo (gate.nat_park_01, gate.air_cargo_01): Calibrated wood-framed ranger entrance booths and high-throughput airport cargo facility gates.
	[Group 40] Vanilla California Ag Border (gate.ca_ag_check01): Optimized pneumatic inspection barriers for classic California agricultural quarantine stations.
	[Group 41] PACCAR Test Track (WA) (gate.paccar_sec_01): Profiled high-security test facility gates.
	[Group 42] Hydroelectric Dam Security (NV/AZ/WA) (gate.dam_sec_01): Mapped heavy blast-resistant security gates across major regional dam complexes.
	[Group 43] Research & Black Sites (NM/ID) (gate.lab_black_01): Configured extended-range proximity triggers for isolated federal research compounds.
	[Group 44] Resorts & VIP Studios (NV/CA/CO) (gate.resort_vip_01): Tailored fast-acting electric gates for luxury hotel and studio access points.
	[Group 45] Hidden Road Racetracks (AZ/TX) (gate.hidden_track_01): Tuned access barriers for hidden motorsports and test circuit shortcuts.
	
	Part 7: Re-indexed Community Map Overhauls (Groups 46–50)
	Sequential Tier 3 Shift: Community map integration layers originally mapped to groups 36–40 were safely re-indexed upward to Groups 46 through 50 (Reforma, ProMods Canada, Sierra Nevada, Coast to Coast, and Great America) to preserve strict numerical continuity across the 50-group master build.
	
INTERNAL CODE AND TEST VERSION NEVER RELEASED!! 
  v2.1.0-***SGSB (Tolls, And DLC Gates)
  	Oregon Metal_01 gate
  	Namespace Standardization: Renamed definition file to animated_gate.sgsb.sii for improved load order hierarchy and mod compatibility.
  	Toll Plaza Tuning:Section 1A (Standard): Shifted orientation_tolerance to 47.0° to better clear high-speed highway plaza approaches.
  	Section 1A Audio: Added missing sound_path: "/sound/world/gate_pneumatic.soundref" hooks to prevent silent barrier animations and engine log warnings.
  	Section 1B (Precision 13M): Standardized orientation_tolerance to 35.0° for tight, single-lane toll booths.Compound-Curve Expansion: 
  	Extended Logistics Master & Sliding Gates (Sections 2 & 2C) to 75.0° yaw tolerance to accommodate sharp, off-angle depot approaches without trigger drops.

  v2.0.0-72226(Evolution)
	Unified Architecture: New "Global Logic" groups make the mod faster and easier to maintain.
	Engine-Native Cleanse: Removed legacy code to ensure zero-log-error performance.
	Logistics Master Triggers: 55.0m for industrial yards and sliding gates.
  	Orientation Tolerance: Optimized to 60° to catch your approach angle early on tight compound turns.
  	Toll Plazas (Precision Lanes): Tuned to 10.0m for a smoother, more forgiving clearance window.
  	Toll Plazas (Standard Lanes): Left untouched at 23.0m.  
  	Depot Storage Doors: Set to 20.0m to completely eliminate slow-opening bay snags and trailer clipping.

  v1.7.3-71826R4(Feeling Hot Hot Hot) Hotfix-71926
    Deprecated trailer code causing some gates/tolls to not trigger at a distance.
    Cleaned up mod_description to clean up warnings in long. No code change. I will be working on a Github link for full changelogs in the coming days.
  
  v1.7.2-71826R3 (Couldnt Get it right) Hotfix
    Fixed AI Traffic Jams: Resolved an issue where gates would occasionally stay closed too long, causing AI trucks to get stuck at depot entrances.
    Smoother Animations: Fine-tuned gate movement to eliminate stuttering or "shivering" when pulling up to a gate in a long-nose truck.
    Refined Sound Quality: Optimized in-cab audio to better muffle gate operation, making the experience more immersive from the driver's seat.
    Improved Lane Intelligence: Enhanced the gate's ability to ignore traffic in adjacent lanes, preventing "ghost triggers" from opening your gate when it shouldn't.
    General Performance: Minor backend cleanup to improve frame stability when passing through gate collision zones.
    Trigger Distance bumped 49m!

   v1.7.1-71826R2 Hotfix "The House Thats Code Built" (Current Version)
    No More Crushed Trailers: Fixed a bug where warehouse roll-up doors would accidentally close on your trailer while you were trying to back into tight docks.
    Better Sensors for Long-Nose Trucks: Fine-tuned the trigger zones at toll booths and left-side gates so long conventional trucks open them more reliably without having to scrape the mirrors.
    Cleaner Game Logs: Fixed some internal file names to clear out map-node warnings and keep your game.log.txt clean.
    Under-the-Hood Polish: Updated the background code to perfectly match the newest ATS v1.60+ engine standards for better stability.

   v1.7.0-71826 — "The House That Code Built" (Current Version)
        Engine Rest Restoration: Fully integrated native 1.60+ automatic rest distance mechanics across all definitions. Extraneous engine-level overrides have been safely scrubbed to let the base code handle drop-in/drop-out scaling perfectly without micro-stutters.
        Global Pointer Audit: Standardized identifier parsing across complex automated sub-variants. Fixed an inherited naming syntax bug in Section 2C where gate.ani_slide_3f mismatched its structural family (gate.an_slide_f3f), completely eliminating map-node registration failures and dead assets.
        Left-Hand Toll Offset Calibration: Refined left-hand mirror variants (gate.anim_gate3l) to match inverse axis geometry. Shuffled the bounding boxes relative to the node origin to stop long-nose conventionals from having to pull up too deep into left-side manual cash slots.
        Added missing gates!!!

    v1.6.0-71626 — "Fight Fire with Code"
        EZ-Pass Lanes: Fine-tuned to a 23m trigger distance and a 4m trigger offset. This maintains your perfect 19m entry approach while tightening the exit zone to 27m to block tailgating AI traffic from slipping through on your green light.
        Manual Cash Lanes: Retained the highly stable 5m trigger and -3m offset layout with full trailer tracking enabled for heavy-haul safety.
        Border Customs: Programmed with a 25m trigger distance and realistic pneumatic lock sounds.
        Traditional Toll Gates: Standardized at a 5m trigger with active trailer tracking.
        Sliding & Automated Gates: Synchronized yard assets to a 48.9m trigger distance and a 47° orientation tolerance for seamless depot access. Applied progressive electric, metal, and wooden sound profiles based on asset styles.

    v1.5.0-71626 — "For Whom the Code Tolls"
        Total Trailer Protection: Added trailer_activation: true to every single gate block. Tolls, border checkpoints, and logistics yards now track your entire rig—no more barriers dropping early on long 53ft trailers, flatbeds, or double/triple setups.
        Expanded Yard Buffers: Increased yard gate trigger distance to 48.9m (up from 48.7m) for a wider safety margin at busy depots.
        Smart Sensor Tuning: Tightened yard gate opening angles back down to 45° (from 60°/75°). Gates will no longer swing open falsely when you are simply maneuvering or backing into an adjacent dock.
        Refined Soundsets: Toll plazas remain silent to match vanilla plastic barriers, while logistics yards and border checkpoints enforce heavy, realistic iron gate clanks.
        Animation Fix: Resolved a broken pathing bug on the Sliding Yard Gate (gate.ani_slide_3), restoring full opening and closing visuals.

    v1.3.0-71526 — "And Justice for Tolls"
        EZ-Pass Lanes (Left Gates): Increased trigger to 15m for smooth, slow-roll tracking without stopping.
        Cash Lanes (Right Gates): Kept tight at 5m for realistic stop-and-pay action.
        Legacy Tolls (Single Gates): Standardized at 5m to preserve old-school realism.
        Border Crossings: Increased to 25m so heavy gates clear long-nose rigs early.
    
    v1.2.0-71526 — "Logic Overhaul"
        Angle Adjustments: Widened the orientation_tolerance cones up to 60° and 75° so gates recognize your truck earlier when swinging into a yard from sharp, tight angles. Bumped trigger range to 48.7m.

    v1.1.0-71426 — "The Distance Baseline"
        Range Bump: Expanded trigger distance baseline to 48.5m. Removed old alpha phase reset trigger comments from the active code base.

Project Roadmap
    Continued the streamlined process of adding new gates, service areas etc and re-bases as needed.


Compatibility & Load Order
    Convoy-Ready: Fully optimized file layout ensures seamless synchronization during multiplayer convoy sessions with zero mod-mismatch errors.
    Map Compatibility: Clean, definition-only architecture guarantees absolute stability and pristine game logs alongside major map expansions like ProMods Canada, Reforma, and global traffic AI mods.

Recommended Load Order

To ensure the custom safety buffer parameters take priority over world geometry data, organize your mod manager as follows:

Top - SoundFixes
    Smart Gates and Safety Buffers (SGSB) (Place Right Here)(Needs to be high)
    Global Traffic & AI Density Mods
Bottom - Map Expansion Mods (ProMods, Reforma, etc.)

Support, Feedback & Conflict Notices
    Conflict Notice: This is a standalone global logic override. It will conflict with other mods that attempt to modify the same global gate animation or trigger definitions (animated_gate blocks).

Depot Reporting Protocol
If you encounter a specific yard, toll plaza, or logistics depot anywhere on the map that still feels "off" or doesn't trigger correctly, please drop the City and Company Name in the comments section. Feedback will be logged and prioritized for our upcoming maintenance hotfixes.
Credits & Technical Acknowledgments

    Development Group: Smoke Show Studios & Smoke Show Creations
    Lead Developer & Tester: meanshadows35
    Co-Developer: mrh368
    Technical Consultant: Overdrive

A massive shout-out to our three-person team for pulling this together, and special thanks to the entire trucking community for the incredible passion and feedback that keeps our virtual roads moving forward. We pray this turns into an excellent long-term resource for the community!

    Developed natively on Ubuntu 26.04 LTS
    Mod testing powered by thezk sk-zk Extractor tool (https://github.com/sk-/Extractor)
    Built using the official SCS Uploader tool running under Proton
    Thank you to SCS Software for the robust modding ecosystem

Glory To God — Soli Deo Gloria

    Trucky Mods: SGSB (Smart Gates, Tolls & Safety Buffers)
    Steam Workshop: SGSB (Smart Gates, Tolls & Safety Buffers)
