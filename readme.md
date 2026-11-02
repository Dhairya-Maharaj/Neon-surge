📖 The Journey From Start to Finish
🔹 Version 1.0 — Initial Prototype
Basic 3-lane Three.js endless runner with keyboard & swipe controls.
Procedural track chunks, basic box-based obstacles, and collectible gold coins.
Web Audio API procedural sound effects (jump, slide, coin chime, crash, background music) without external audio file dependencies.
Upgrade shop and local storage persistence.
🔹 Version 1.5 — Collision & Solvability Pass
Issue: Track generation was spawning impossible roadblock walls right at chunk seams, and obstacles were blending into pitch-black fog.
Fix: Implemented solvability guarantees (at least 1 open lane at every segment slice). Reduced fog density and added street lamps so obstacles could be seen 100+ meters away.
🔹 Version 1.8 — Hitbox & Alignment Overhaul
Issue: Players were dying while sliding under red lasers; the 3rd lane on the right was clipping outside the rails.
Fix: Re-centered the 3-lane grid (-2.6, 0.0, +2.6). Reworked the red laser collision check to an explicit coordinate window (Y = 1.35 to 2.35). When sliding, the player's collision height drops to Y = 0.25, guaranteeing safe passage under every laser.
🔹 Version 2.0 — Running Man Model
Addition: Replaced the primitive block character with an athletic Running Man rig inspired by the Poly Pizza runner (84URB-weoAu), featuring an athletic cap, runner torso, and dynamically swinging arms and legs.
🔹 Version 2.1 — Ghost Obstacle Purge
Issue: When restarting after a crash, hurdles from where you previously died remained frozen at the start line and came at the player immediately.
Fix: Diagnosed and resolved memory leakage where obstacle meshes weren't being unhooked from the Three.js scene. Added a complete purge (scene.remove) of all obstacles, coins, and particles on restart.
🔹 Version 2.2 — Pacing & Train Ramps
Issue: The startup delay was too long, and gameplay was too slow.
Addition: Added climbable yellow train ramps (75% of trains). Players can sprint up ramps onto train roofs to collect rooftop coin trails. Reduced startup delay to a tight 50-meter buffer and boosted base speed to a snappy 22 (accelerating to 54).
🔹 Version 2.3 — Diwali Festival Mode
Addition: Added a dedicated Diwali Festival Mode toggle featuring midnight purple skies, overhead starburst fireworks with crackle audio, glowing clay Diyas lining the tracks, festive toran arches, and a celebratory saffron kurta & turban avatar.
🔹 Version 2.4 — Admin Panel & Settings
Addition: Secret Admin Hack Terminal protected by a passkey (God Mode, Perma-Jetpack, Ultra Magnet, Moon Jump, Speed Controls, Currency Injection).
Addition: Settings Panel (Audio toggles, Graphics quality presets, Camera FOV, Swipe sensitivity).
Addition: Harsh Restart option to factory reset all coins, characters, and upgrades.
Fix: Cross button (✕) and "RETURN TO MENU" navigation now cleanly take you back to the Main Menu.
🎮 Quick Reference Guide
Category	Controls / Details
Move Lanes	A / D or Arrow Left / Right or Swipe Left / Right
Jump	W / Space / Arrow Up / Swipe Up
Slide Under Lasers	S / Arrow Down / Swipe Down
Admin Terminal Key	~ (Tilde / Backquote) or Click ADMIN HACKS 🛠️
Diwali Mode Toggle	Click MODE: DIWALI FESTIVAL 🪔 on the Main Menu
Climbing Trains	Run directly up the yellow ramps in front of monorails
