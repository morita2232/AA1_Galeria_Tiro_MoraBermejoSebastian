# Unreal Engine Audio Integration – AA2 Assignment

This project was completed as part of the AA2 audio integration assignment for Unreal Engine 5.4.  
**Important:** All required audio features were implemented only in the branch `AA2-Unreal-Integration`.  
Please ignore other branches, as they do not contain the updated audio work.

---

## Implemented Requirements and Where They Were Applied

### 1. 12+ Audio Sources and 12+ Unique Audio Files
**Where:** Entire map  
**How:**  
- 3 randomized gunshot sounds via MetaSound  
- 1 casing drop sound  
- 4 ambient looped effects (wind, vent, hum, electric buzz)  
- Footsteps  
- Door open sound  
- 2 additional ambient sources placed in the environment  

---

### 2. Spatialization Setup (attenuation, curves, low-pass filter)
**Where:** All ambient and interactive sounds  
**How:**  
- Applied `Ambience_Attenuation` asset  
- Set falloff distances (Inner Radius: 400, Falloff: 750)  
- Enabled spatialization and panning  
- Reverb send enabled based on distance  

---

### 3. Soundscape Quality
**Where:** All level areas  
**How:**  
- More than 6 spatial ambient sources placed throughout the scene  
- Carefully balanced volume and placement  
- Sounds create a layered, immersive experience  

---

### 4. MetaSounds (random pitch/sample/volume)
**Where:** Gunshots  
**How:**  
- MetaSound uses `Random Get`, `Random (Float)`, and pitch/volume modifiers  
- 3 gunshot samples selected at random  
- Blended through a Mono Mixer  

---

### 5. Keyframe-Based Sound
**Where:** FirstPerson_AnimBP  
**How:**  
- Added an animation notify called `PlayCasingSound`  
- Triggers casing sound after each gunshot based on animation timing  

---

### 6. Collision-Based Sound
**Where:** Footsteps  
**How:**  
- Sound triggered by movement or ground contact  
- Tied to character collision or animation states  

---

### 7. Mixing Control (Submix Routing)
**Where:** All sound sources  
**How:**  
- Created and used submixes: `Master_Submix`, `SFX_Submix`, and `Ambience_Submix`  
- Assigned each sound manually in their respective settings  
- Verified routing through the Sound Cue and asset details  

---

### 8. Submix Effects (Reverb)
**Where:** SFX Submix  
**How:**  
- Applied a Reverb Effect preset  
- Configured parameters such as decay, density, gain  
- Active only on SFX submix with moderate wet level  

---

### 9. Audio Volumes
**Where:** Indoor area  
**How:**  
- Placed an `Audio Volume` in the scene  
- Enabled reverb and assigned `ReverbEffect`  
- Fade Time set to 0.3, Volume set to 0.5  
- Reverb activates on player entry  

---

### 10. Overall Audio Quality
**Where:** Entire project  
**How:**  
- All sounds volume-balanced and non-intrusive  
- Ambient audio looped smoothly  
- No overlaps or audio glitches  
- Efficient use of looping, attenuation, and submixes  

---

## Submission Notes

- Project Name: Galería de Tiro
- Engine Version: Unreal Engine 5.4.4
- Submission Branch: `AA2-Unreal-Integration`

Please check only the `AA2-Unreal-Integration` branch. Other branches are not part of the submission.
