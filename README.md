Smart Gates & Safety Buffers (SGSB) — v1.7.3-71826R4 (Couldnt Get it right) Hotfix
"The House That Code Built"

A Note from the Developer
    This project is dedicated to the glory of God. Every mile driven and every line of code written is an expression of gratitude for the journey. May this mod bring a little more order, peace, and grace to the virtual highways we all travel. This is our first mod ever, so please extend us some grace!

The Problem: "Gate Lag"
	After years of long-haul trucking in American Truck Simulator, we know that immersion is everything. Nothing kills the flow of a delivery faster than "gate lag"—that frustrating moment when you are at the yard threshold, waiting for a barrier to crawl open while your multi-ton rig is already stalled out.
The Solution: Smart Gates & Safety Buffers

SGSB is the definitive logic overhaul for gate operations. We have stripped away the inconsistent, immersion-breaking triggers of the base game and replaced them with a standardized, high-performance logic set.

Whether you are hauling heavy cargo into a Phoenix warehouse or navigating a tight depot in the Midwest, your gates will now respond with the reliable precision a professional driver expects. Built by a driver, for drivers.

Quick Reference Specs
    SGSB Trigger Distance: 49.0m for yard entries (Up from the vanilla 15m–25m. Values of 50m+ break the engine logic).
    SGSB Orientation Tolerance: 45° – 47° (Up from vanilla 30°) to catch your approach angle early.
    Accidental Trigger Prevention: Depot warehouse storage doors are kept tight at 30° to prevent nearby external lane traffic from accidentally opening them.
    
Official Release Information

    Current Version: v1.7.3-71826R4 (Stable Hotfix 71926)
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
  
	v1.1 – v1.1.1 [Completed]: Expanded gate opening range to 48.5m, cleaned up old comments, and resolved edge-case depot clipping in newer map expansions (e.g., South Dakota).
    v1.2 – v1.3 [Completed]: Increased gate triggers to 48.7m, optimized orientation to 60°–75°, and executed a complete overhaul of lane-specific toll booth logic.
    v1.5 – v1.6 [Completed]: Added missing asset sound profiles, implemented total trailer tracking protection, refined gate sensor cones, and fine-tuned lane offsets.
   v1.7 [Current Release]: Re-integrated native automatic rest distances and standardized the structural pointer schema naming conventions across all sliding variants.
    Future Updates & Maintenance [In Progress]: Continuous tracking and integration of any new gate or toll structures added by SCS Software, ongoing .sii def file maintenance, and diving into Blender to learn asset-level gate speed adjustments.
    2.0 Standardization of Code. 1.7 is pretty much a test base.
    Cleaned up mod_description to clean up warnings in long. No code change. I will be working on a Github link for full changelogs in the coming days.



Compatibility & Load Order
    Convoy-Ready: Fully optimized file layout ensures seamless synchronization during multiplayer convoy sessions with zero mod-mismatch errors.
    Map Compatibility: Clean, definition-only architecture guarantees absolute stability and pristine game logs alongside major map expansions like ProMods Canada, Reforma, and global traffic AI mods.

Recommended Load Order

To ensure the custom safety buffer parameters take priority over world geometry data, organize your mod manager as follows:

    Smart Gates and Safety Buffers (SGSB) (Place Right Here)
    Global Traffic & AI Density Mods
    Map Expansion Mods (ProMods, Reforma, etc.)

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
