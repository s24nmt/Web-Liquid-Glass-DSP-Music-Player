# No need to install various Music player apps, no platform limitations, Just Fun.

# Web-Liquid-Glass-DSP-Music-Player
This is a self-contained single-file web application (Liquid Glass DSP Music Player) built with HTML5, CSS3, and vanilla JavaScript. It works like a portable active crossover, parametric equalizer, and stereo/echo processor right in the browser, using the Web Audio API to process local audio files in real time.
# 1. Visual Design & Responsive Layout
Mobile-First + Desktop Studio Rack:
Below 960px, it uses a bottom navigation bar (Player, Sub & X-Over, Live EQ, Space FX) so only one view is active at a time, All volume, crossover, EQ, and FX faders use vertical orientation.
# Desktop Layout
<img width="800" height="504" alt="PC Layout" src="https://github.com/user-attachments/assets/8838ac77-0cfd-4fcf-95d1-f08052d37d7f" />

# Mobile Layout
<img width="400" height="718" alt="Mobile Layout" src="https://github.com/user-attachments/assets/02979352-4cf2-4dd0-8150-a354559e00cd" />


# 2. Web Audio API Signal Chain,
4-Band Parametric EQ (eqNodes):
Low-Mid (peaking, default 250 Hz, range 120–600 Hz)
Vocal / Mid (peaking, default 1000 Hz, range 600–2500 Hz)
Presence (peaking, default 3500 Hz, range 2500–7000 Hz)
Air / Highs (highshelf, default 10000 Hz, range 6000–16000 Hz)
Active Crossover & Subwoofer Path,
Sub path: High-pass Subsonic HPF (15–45 Hz) to filter out ultra-low rumble, two cascaded low-pass stages (subLpf1, subLpf2), a Punch peaking boost (subPunchFilter), Phase invert (0° or 180°), optional Sub Mono summing (subMonoNode set to channelCount = 1), and Sub Level gain (-15 dB to +12 dB).
Tops path: Two cascaded high-pass stages (topsHpf1, topsHpf2) for the highs/mids above the crossover point, followed by the Space FX chain.
Master Volume & Metering

# 3. Local Media, Metadata & Persistence
File & Folder Loading: Supports picking individual audio files, Offline Cover Art 

# 4. Seven Visualizer Modes
1- Liquid Bars, 2- Winamp Bands, 3- Waveform Flow, 4- Geometric Cascade, 5- Radial Spectrum Ring, 6- Particle Pulse Field, 7- 3D Terrain Wave
