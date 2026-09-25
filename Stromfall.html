<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
<title>Project Stormfall - Battle Royale</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    background: #0a0a0f;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    overflow: hidden;
    width: 100vw;
    height: 100vh;
    color: #fff;
    user-select: none;
    -webkit-user-select: none;
  }
  canvas { display: block; }
  #gameCanvas {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
  }

  /* Start Screen */
  #startScreen {
    position: absolute; top: 0; left: 0;
    width: 100%; height: 100%;
    background: linear-gradient(135deg, #0d1117 0%, #161b22 50%, #0d1117 100%);
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    z-index: 100;
    transition: opacity 0.5s;
  }
  #startScreen.hidden { opacity: 0; pointer-events: none; }

  .title-container {
    text-align: center;
    margin-bottom: 30px;
    animation: titlePulse 3s ease-in-out infinite;
  }
  @keyframes titlePulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.02); }
  }
  .game-title {
    font-size: clamp(28px, 6vw, 56px);
    font-weight: 900;
    background: linear-gradient(135deg, #ff6b35, #f7c948, #ff6b35);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-transform: uppercase;
    letter-spacing: 4px;
    text-shadow: 0 0 40px rgba(255, 107, 53, 0.3);
  }
  .game-subtitle {
    font-size: clamp(12px, 2.5vw, 18px);
    color: #8b949e;
    letter-spacing: 8px;
    text-transform: uppercase;
    margin-top: 5px;
  }

  .character-select {
    display: flex; gap: 15px;
    margin: 20px 0;
    flex-wrap: wrap;
    justify-content: center;
    padding: 0 10px;
  }
  .char-card {
    background: rgba(255,255,255,0.05);
    border: 2px solid rgba(255,255,255,0.1);
    border-radius: 12px;
    padding: 15px;
    width: clamp(100px, 20vw, 140px);
    text-align: center;
    cursor: pointer;
    transition: all 0.3s;
  }
  .char-card:hover { border-color: #ff6b35; transform: translateY(-3px); }
  .char-card.selected {
    border-color: #ff6b35;
    background: rgba(255, 107, 53, 0.15);
    box-shadow: 0 0 20px rgba(255, 107, 53, 0.2);
  }
  .char-icon {
    font-size: 36px;
    margin-bottom: 8px;
    display: block;
  }
  .char-name {
    font-size: 13px;
    font-weight: 700;
    color: #e6edf3;
  }
  .char-ability {
    font-size: 10px;
    color: #8b949e;
    margin-top: 4px;
  }

  .mode-select {
    display: flex; gap: 10px;
    margin: 15px 0;
  }
  .mode-btn {
    background: rgba(255,255,255,0.05);
    border: 2px solid rgba(255,255,255,0.1);
    border-radius: 8px;
    padding: 10px 20px;
    color: #e6edf3;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
  }
  .mode-btn:hover { border-color: #58a6ff; }
  .mode-btn.selected {
    border-color: #58a6ff;
    background: rgba(88, 166, 255, 0.15);
  }

  .play-btn {
    background: linear-gradient(135deg, #ff6b35, #e85d26);
    border: none;
    border-radius: 12px;
    padding: 16px 60px;
    color: #fff;
    font-size: 18px;
    font-weight: 800;
    cursor: pointer;
    text-transform: uppercase;
    letter-spacing: 3px;
    margin-top: 20px;
    transition: all 0.3s;
    box-shadow: 0 4px 20px rgba(255, 107, 53, 0.4);
  }
  .play-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 30px rgba(255, 107, 53, 0.6);
  }

  /* Drop Phase */
  #dropScreen {
    position: absolute; top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.85);
    display: none;
    flex-direction: column;
    align-items: center; justify-content: center;
    z-index: 90;
  }
  #dropScreen.visible { display: flex; }
  .drop-text {
    font-size: 24px;
    font-weight: 700;
    color: #ff6b35;
    animation: dropPulse 1.5s ease-in-out infinite;
  }
  @keyframes dropPulse {
    0%, 100% { opacity: 0.6; }
    50% { opacity: 1; }
  }
  .drop-hint {
    font-size: 14px;
    color: #8b949e;
    margin-top: 10px;
  }

  /* HUD */
  #hud {
    position: absolute; top: 0; left: 0;
    width: 100%; height: 100%;
    pointer-events: none;
    z-index: 50;
    display: none;
  }
  #hud.visible { display: block; }

  .hud-top {
    position: absolute; top: 10px; left: 50%;
    transform: translateX(-50%);
    display: flex; gap: 15px;
    align-items: center;
  }
  .alive-count {
    background: rgba(0,0,0,0.6);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 8px;
    padding: 6px 16px;
    font-size: 14px;
    font-weight: 700;
  }
  .alive-count span { color: #ff6b35; }
  .zone-timer {
    background: rgba(0,0,0,0.6);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 8px;
    padding: 6px 16px;
    font-size: 12px;
    color: #f7c948;
  }

  .hud-left {
    position: absolute; bottom: 20px; left: 15px;
    display: flex; flex-direction: column; gap: 6px;
  }
  .health-bar-container, .armor-bar-container {
    width: 200px;
    height: 22px;
    background: rgba(0,0,0,0.6);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 6px;
    overflow: hidden;
    position: relative;
  }
  .health-bar {
    height: 100%;
    background: linear-gradient(90deg, #e74c3c, #2ecc71);
    transition: width 0.3s;
    border-radius: 5px;
  }
  .armor-bar {
    height: 100%;
    background: linear-gradient(90deg, #3498db, #5dade2);
    transition: width 0.3s;
    border-radius: 5px;
  }
  .bar-text {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    font-size: 11px;
    font-weight: 700;
    text-shadow: 1px 1px 2px rgba(0,0,0,0.8);
  }

  .hud-right {
    position: absolute; bottom: 20px; right: 15px;
    text-align: right;
  }
  .weapon-info {
    background: rgba(0,0,0,0.6);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 8px;
    padding: 8px 14px;
    margin-bottom: 6px;
  }
  .weapon-name {
    font-size: 14px;
    font-weight: 700;
    color: #e6edf3;
  }
  .ammo-count {
    font-size: 20px;
    font-weight: 800;
    color: #f7c948;
  }
  .ammo-count .ammo-sep { color: #8b949e; margin: 0 2px; }
  .kills-display {
    background: rgba(0,0,0,0.6);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 8px;
    padding: 6px 14px;
    font-size: 13px;
    font-weight: 700;
  }
  .kills-display span { color: #e74c3c; }

  .hud-bottom-center {
    position: absolute; bottom: 15px; left: 50%;
    transform: translateX(-50%);
    display: flex; gap: 6px;
    pointer-events: auto;
  }
  .inv-slot {
    width: 50px; height: 50px;
    background: rgba(0,0,0,0.6);
    border: 2px solid rgba(255,255,255,0.15);
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 20px;
    cursor: pointer;
    transition: all 0.2s;
    position: relative;
  }
  .inv-slot.active {
    border-color: #ff6b35;
    background: rgba(255, 107, 53, 0.2);
    box-shadow: 0 0 10px rgba(255, 107, 53, 0.3);
  }
  .inv-slot .slot-key {
    position: absolute; top: 2px; left: 4px;
    font-size: 9px; color: #8b949e;
  }

  /* Minimap */
  .minimap-container {
    position: absolute; top: 10px; right: 10px;
    width: clamp(100px, 15vw, 150px);
    height: clamp(100px, 15vw, 150px);
    background: rgba(0,0,0,0.7);
    border: 2px solid rgba(255,255,255,0.2);
    border-radius: 8px;
    overflow: hidden;
  }
  #minimapCanvas {
    width: 100%; height: 100%;
  }

  /* Kill Feed */
  .kill-feed {
    position: absolute; top: 50px; left: 15px;
    display: flex; flex-direction: column; gap: 4px;
    max-height: 200px;
    overflow: hidden;
  }
  .kill-msg {
    background: rgba(0,0,0,0.6);
    padding: 4px 10px;
    border-radius: 4px;
    font-size: 11px;
    color: #e6edf3;
    animation: fadeSlide 0.3s ease-out;
    white-space: nowrap;
  }
  @keyframes fadeSlide {
    from { opacity: 0; transform: translateX(-20px); }
    to { opacity: 1; transform: translateX(0); }
  }
  .kill-msg .killer { color: #ff6b35; font-weight: 700; }
  .kill-msg .victim { color: #e74c3c; font-weight: 700; }

  /* Ability Cooldown */
  .ability-container {
    position: absolute; bottom: 80px; right: 15px;
    pointer-events: auto;
  }
  .ability-btn {
    width: 50px; height: 50px;
    background: rgba(0,0,0,0.6);
    border: 2px solid rgba(139, 92, 246, 0.5);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 22px;
    cursor: pointer;
    position: relative;
    overflow: hidden;
  }
  .ability-btn.on-cooldown { opacity: 0.5; }
  .ability-cd-overlay {
    position: absolute; bottom: 0; left: 0;
    width: 100%;
    background: rgba(0,0,0,0.7);
    transition: height 0.1s linear;
  }
  .ability-cd-text {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    font-size: 12px;
    font-weight: 700;
    z-index: 2;
  }

  /* Game Over */
  #gameOver {
    position: absolute; top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.85);
    display: none;
    flex-direction: column;
    align-items: center; justify-content: center;
    z-index: 100;
  }
  #gameOver.visible { display: flex; }
  .result-text {
    font-size: clamp(32px, 8vw, 60px);
    font-weight: 900;
    margin-bottom: 10px;
  }
  .result-text.win {
    background: linear-gradient(135deg, #f7c948, #ff6b35);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .result-text.lose { color: #e74c3c; }
  .result-stats {
    display: flex; gap: 30px;
    margin: 20px 0;
  }
  .stat-item {
    text-align: center;
  }
  .stat-value {
    font-size: 28px;
    font-weight: 800;
    color: #ff6b35;
  }
  .stat-label {
    font-size: 12px;
    color: #8b949e;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  .play-again-btn {
    background: linear-gradient(135deg, #ff6b35, #e85d26);
    border: none;
    border-radius: 10px;
    padding: 14px 50px;
    color: #fff;
    font-size: 16px;
    font-weight: 700;
    cursor: pointer;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-top: 15px;
    transition: all 0.3s;
    pointer-events: auto;
  }
  .play-again-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 20px rgba(255, 107, 53, 0.5);
  }

  /* Damage Indicator */
  .damage-overlay {
    position: absolute; top: 0; left: 0;
    width: 100%; height: 100%;
    pointer-events: none;
    z-index: 45;
  }
  .damage-flash {
    position: absolute; top: 0; left: 0;
    width: 100%; height: 100%;
    border: 4px solid transparent;
    border-radius: 0;
    opacity: 0;
    transition: opacity 0.15s;
  }
  .damage-flash.active {
    border-color: rgba(231, 76, 60, 0.6);
    opacity: 1;
  }

  /* Mobile Controls */
  .mobile-controls {
    display: none;
    position: absolute; bottom: 0; left: 0;
    width: 100%; height: 50%;
    pointer-events: none;
    z-index: 55;
  }
  .mobile-controls.visible { display: block; }
  .joystick-area {
    position: absolute;
    bottom: 20px;
    width: 120px; height: 120px;
    pointer-events: auto;
  }
  .joystick-left { left: 20px; }
  .joystick-right { right: 20px; }
  .joystick-base {
    width: 100%; height: 100%;
    background: rgba(255,255,255,0.1);
    border: 2px solid rgba(255,255,255,0.2);
    border-radius: 50%;
    position: relative;
  }
  .joystick-knob {
    width: 50px; height: 50px;
    background: rgba(255,255,255,0.3);
    border: 2px solid rgba(255,255,255,0.4);
    border-radius: 50%;
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
  }
  .mobile-shoot-btn {
    position: absolute;
    bottom: 160px; right: 30px;
    width: 65px; height: 65px;
    background: rgba(255, 107, 53, 0.4);
    border: 2px solid rgba(255, 107, 53, 0.6);
    border-radius: 50%;
    pointer-events: auto;
    display: flex; align-items: center; justify-content: center;
    font-size: 14px; font-weight: 700;
  }
  .mobile-action-btns {
    position: absolute;
    bottom: 160px; left: 30px;
    display: flex; flex-direction: column; gap: 8px;
    pointer-events: auto;
  }
  .mob-btn {
    width: 45px; height: 45px;
    background: rgba(255,255,255,0.1);
    border: 1px solid rgba(255,255,255,0.2);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 11px;
    color: #e6edf3;
    font-weight: 600;
  }

  /* Loot popup */
  .loot-popup {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    background: rgba(0,0,0,0.8);
    border: 1px solid rgba(255,255,255,0.2);
    border-radius: 10px;
    padding: 15px;
    min-width: 200px;
    display: none;
    z-index: 60;
    pointer-events: auto;
  }
  .loot-popup.visible { display: block; }
  .loot-title {
    font-size: 14px;
    font-weight: 700;
    color: #f7c948;
    margin-bottom: 10px;
    text-align: center;
  }
  .loot-item {
    display: flex; align-items: center; gap: 10px;
    padding: 8px;
    border-radius: 6px;
    cursor: pointer;
    transition: background 0.2s;
  }
  .loot-item:hover { background: rgba(255,255,255,0.1); }
  .loot-item-icon { font-size: 20px; }
  .loot-item-info {
    flex: 1;
  }
  .loot-item-name {
    font-size: 12px; font-weight: 600;
  }
  .loot-item-desc {
    font-size: 10px; color: #8b949e;
  }

  /* Hit marker */
  .hit-marker {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    font-size: 18px;
    font-weight: 800;
    color: #f7c948;
    pointer-events: none;
    z-index: 48;
    opacity: 0;
    transition: all 0.3s;
  }
  .hit-marker.active {
    opacity: 1;
    transform: translate(-50%, -80%);
  }

  /* Crosshair */
  .crosshair {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    pointer-events: none;
    z-index: 47;
  }

  /* Interact prompt */
  .interact-prompt {
    position: absolute;
    bottom: 120px; left: 50%;
    transform: translateX(-50%);
    background: rgba(0,0,0,0.7);
    border: 1px solid rgba(255,255,255,0.2);
    border-radius: 6px;
    padding: 6px 14px;
    font-size: 12px;
    color: #f7c948;
    display: none;
    z-index: 52;
    white-space: nowrap;
  }
  .interact-prompt.visible { display: block; }
</style>
</head>
<body>

<canvas id="gameCanvas"></canvas>

<!-- Start Screen -->
<div id="startScreen">
  <div class="title-container">
    <div class="game-title">Project Stormfall</div>
    <div class="game-subtitle">Battle Royale</div>
  </div>

  <div style="font-size:13px; color:#8b949e; margin-bottom:10px; text-transform:uppercase; letter-spacing:2px;">Choose Your Operative</div>
  <div class="character-select" id="charSelect"></div>

  <div style="font-size:13px; color:#8b949e; margin-bottom:10px; text-transform:uppercase; letter-spacing:2px;">Select Mode</div>
  <div class="mode-select">
    <div class="mode-btn selected" data-mode="solo" onclick="selectMode(this)">Solo</div>
    <div class="mode-btn" data-mode="duo" onclick="selectMode(this)">Duo</div>
    <div class="mode-btn" data-mode="squad" onclick="selectMode(this)">Squad</div>
  </div>

  <button class="play-btn" onclick="startGame()">Deploy</button>

  <div style="margin-top:20px; font-size:11px; color:#484f58; text-align:center; max-width:400px; line-height:1.5;">
    WASD to move • Mouse to aim & shoot • E to interact • R to reload • 1-5 for weapons • Q for ability • Space to dash
  </div>
</div>

<!-- Drop Screen -->
<div id="dropScreen">
  <div class="drop-text">⬆ CLICK TO DROP ⬆</div>
  <div class="drop-hint">Choose your landing spot wisely</div>
  <canvas id="dropMapCanvas" width="400" height="400" style="margin-top:15px; border-radius:8px; border:2px solid rgba(255,255,255,0.15); cursor:pointer;"></canvas>
</div>

<!-- HUD -->
<div id="hud">
  <div class="hud-top">
    <div class="alive-count">⚔ <span id="aliveCount">30</span> Alive</div>
    <div class="zone-timer" id="zoneTimer">Zone shrinking in 60s</div>
  </div>

  <div class="minimap-container">
    <canvas id="minimapCanvas"></canvas>
  </div>

  <div class="kill-feed" id="killFeed"></div>

  <div class="hud-left">
    <div class="health-bar-container">
      <div class="health-bar" id="healthBar" style="width:100%"></div>
      <div class="bar-text" id="healthText">100</div>
    </div>
    <div class="armor-bar-container">
      <div class="armor-bar" id="armorBar" style="width:0%"></div>
      <div class="bar-text" id="armorText">0</div>
    </div>
  </div>

  <div class="hud-right">
    <div class="weapon-info">
      <div class="weapon-name" id="weaponName">Pistol</div>
      <div class="ammo-count">
        <span id="ammoCurrent">12</span><span class="ammo-sep">/</span><span id="ammoReserve">48</span>
      </div>
    </div>
    <div class="kills-display">☠ <span id="killCount">0</span> Eliminations</div>
  </div>

  <div class="hud-bottom-center" id="weaponSlots"></div>

  <div class="ability-container">
    <div class="ability-btn" id="abilityBtn" onclick="useAbility()">
      <div class="ability-cd-overlay" id="abilityCdOverlay" style="height:0%"></div>
      <span class="ability-cd-text" id="abilityCdText"></span>
      <span id="abilityIcon">⚡</span>
    </div>
  </div>

  <div class="interact-prompt" id="interactPrompt">Press E to pick up</div>

  <div class="hit-marker" id="hitMarker">✕</div>

  <div class="damage-overlay">
    <div class="damage-flash" id="damageFlash"></div>
  </div>

  <!-- Mobile Controls -->
  <div class="mobile-controls" id="mobileControls">
    <div class="joystick-area joystick-left" id="joystickLeft">
      <div class="joystick-base"><div class="joystick-knob" id="joystickKnobL"></div></div>
    </div>
    <div class="joystick-area joystick-right" id="joystickRight">
      <div class="joystick-base"><div class="joystick-knob" id="joystickKnobR"></div></div>
    </div>
    <div class="mobile-shoot-btn" id="mobileShoot">FIRE</div>
    <div class="mobile-action-btns">
      <div class="mob-btn" onclick="reloadWeapon()">R</div>
      <div class="mob-btn" onclick="interact()">E</div>
    </div>
  </div>
</div>

<!-- Game Over -->
<div id="gameOver">
  <div class="result-text" id="resultText">ELIMINATED</div>
  <div style="font-size:14px; color:#8b949e;" id="placementText">Placement: #5</div>
  <div class="result-stats">
    <div class="stat-item">
      <div class="stat-value" id="finalKills">0</div>
      <div class="stat-label">Eliminations</div>
    </div>
    <div class="stat-item">
      <div class="stat-value" id="finalDamage">0</div>
      <div class="stat-label">Damage</div>
    </div>
    <div class="stat-item">
      <div class="stat-value" id="finalSurvival">0:00</div>
      <div class="stat-label">Survived</div>
    </div>
  </div>
  <button class="play-again-btn" onclick="location.reload()">Play Again</button>
</div>

<script>
// ============ AUDIO ENGINE ============
const AudioCtx = window.AudioContext || window.webkitAudioContext;
let audioCtx;
function initAudio() {
  if (!audioCtx) audioCtx = new AudioCtx();
}
function playSound(freq, dur, type = 'square', vol = 0.15) {
  if (!audioCtx) return;
  const osc = audioCtx.createOscillator();
  const gain = audioCtx.createGain();
  osc.type = type;
  osc.frequency.setValueAtTime(freq, audioCtx.currentTime);
  gain.gain.setValueAtTime(vol, audioCtx.currentTime);
  gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + dur);
  osc.connect(gain);
  gain.connect(audioCtx.destination);
  osc.start();
  osc.stop(audioCtx.currentTime + dur);
}
function playShoot(type) {
  if (type === 'shotgun') { playSound(120, 0.15, 'sawtooth', 0.25); playSound(80, 0.2, 'square', 0.2); }
  else if (type === 'sniper') { playSound(200, 0.3, 'sawtooth', 0.3); playSound(100, 0.4, 'square', 0.15); }
  else if (type === 'smg') { playSound(300, 0.08, 'square', 0.12); }
  else if (type === 'ar') { playSound(250, 0.12, 'sawtooth', 0.18); }
  else { playSound(400, 0.1, 'square', 0.1); }
}
function playHit() { playSound(800, 0.08, 'sine', 0.2); }
function playPickup() { playSound(600, 0.1, 'sine', 0.15); playSound(900, 0.15, 'sine', 0.1); }
function playDeath() { playSound(200, 0.5, 'sawtooth', 0.2); playSound(150, 0.7, 'square', 0.15); }
function playExplosion() { playSound(60, 0.6, 'sawtooth', 0.4); playSound(40, 0.8, 'square', 0.3); }
function playDash() { playSound(500, 0.15, 'sine', 0.1); }

// ============ CHARACTERS ============
const CHARACTERS = [
  { id: 'ghost', name: 'Ghost', icon: '👻', ability: 'Invisible 3s', abilityIcon: '👻', color: '#a78bfa',
    passive: 'Silent footsteps', abilityCd: 20000, useAbility(g) { g.player.invisTimer = 3000; playSound(400, 0.2, 'sine', 0.1); } },
  { id: 'surge', name: 'Surge', icon: '⚡', ability: 'Speed Boost 4s', abilityIcon: '⚡', color: '#f7c948',
    passive: 'Faster sprint', abilityCd: 15000, useAbility(g) { g.player.speedBoost = 4000; playDash(); } },
  { id: 'fortress', name: 'Fortress', icon: '🛡', ability: 'Shield 100hp', abilityIcon: '🛡', color: '#5dade2',
    passive: 'Armor +25', abilityCd: 25000, useAbility(g) { g.player.armor = Math.min(150, g.player.armor + 50); playSound(300, 0.3, 'sine', 0.15); } },
  { id: 'viper', name: 'Viper', icon: '🐍', ability: 'Poison Cloud', abilityIcon: '☠', color: '#2ecc71',
    passive: 'Faster heal', abilityCd: 18000, useAbility(g) { g.poisonZones.push({x:g.player.x, y:g.player.y, r:120, dur:5000, owner:g.player.id}); playSound(200, 0.3, 'sawtooth', 0.1); } },
  { id: 'hawk', name: 'Hawk', icon: '🦅', ability: 'Scan Area', abilityIcon: '📡', color: '#e74c3c',
    passive: 'See farther', abilityCd: 22000, useAbility(g) { g.scanTimer = 5000; playSound(1000, 0.3, 'sine', 0.15); } },
  { id: 'medic', name: 'Medic', icon: '💉', ability: 'Heal Burst', abilityIcon: '💚', color: '#1abc9c',
    passive: 'Heal +50%', abilityCd: 20000, useAbility(g) { g.player.hp = Math.min(100, g.player.hp + 40); playSound(500, 0.3, 'sine', 0.15); playSound(700, 0.2, 'sine', 0.1); } }
];

// ============ WEAPONS ============
const WEAPON_DEFS = {
  pistol: { name: 'Pistol', icon: '🔫', type: 'pistol', damage: 18, fireRate: 250, mag: 12, spread: 0.06, range: 350, reloadTime: 1200, speed: 14, bulletSize: 3, auto: false, color: '#aaa' },
  smg: { name: 'SMG', icon: '🔫', type: 'smg', damage: 14, fireRate: 80, mag: 30, spread: 0.1, range: 280, reloadTime: 1500, speed: 15, bulletSize: 2.5, auto: true, color: '#3498db' },
  ar: { name: 'Assault Rifle', icon: '🔫', type: 'ar', damage: 22, fireRate: 120, mag: 30, spread: 0.07, range: 420, reloadTime: 1800, speed: 16, bulletSize: 3, auto: true, color: '#e67e22' },
  shotgun: { name: 'Shotgun', icon: '🔫', type: 'shotgun', damage: 12, fireRate: 600, mag: 6, spread: 0.25, range: 180, reloadTime: 2000, speed: 12, bulletSize: 3, auto: false, pellets: 6, color: '#e74c3c' },
  sniper: { name: 'Sniper', icon: '🔫', type: 'sniper', damage: 75, fireRate: 1200, mag: 5, spread: 0.01, range: 700, reloadTime: 2500, speed: 22, bulletSize: 4, auto: false, color: '#9b59b6' },
  dmr: { name: 'DMR', icon: '🔫', type: 'dmr', damage: 35, fireRate: 300, mag: 10, spread: 0.04, range: 500, reloadTime: 2000, speed: 18, bulletSize: 3.5, auto: false, color: '#f39c12' }
};

// ============ LOOT TABLES ============
const LOOT_TABLE = [
  { type: 'weapon', id: 'pistol', weight: 25, icon: '🔫', name: 'Pistol' },
  { type: 'weapon', id: 'smg', weight: 18, icon: '🔫', name: 'SMG' },
  { type: 'weapon', id: 'ar', weight: 15, icon: '🔫', name: 'Assault Rifle' },
  { type: 'weapon', id: 'shotgun', weight: 15, icon: '🔫', name: 'Shotgun' },
  { type: 'weapon', id: 'dmr', weight: 10, icon: '🔫', name: 'DMR' },
  { type: 'weapon', id: 'sniper', weight: 7, icon: '🔫', name: 'Sniper' },
  { type: 'ammo', amount: 30, weight: 20, icon: '🔵', name: 'Ammo' },
  { type: 'health', amount: 30, weight: 15, icon: '❤️', name: 'Med Kit' },
  { type: 'armor', amount: 50, weight: 10, icon: '🛡️', name: 'Armor Plate' },
  { type: 'grenade', weight: 10, icon: '💣', name: 'Grenade' }
];

// ============ MAP GENERATION ============
const MAP_SIZE = 3000;
const TILE = 40;

function generateMap() {
  const buildings = [];
  const zones = [
    { name: 'Stormfall City', cx: 1500, cy: 1500, count: 25, type: 'city' },
    { name: 'Riverside Village', cx: 400, cy: 500, count: 10, type: 'village' },
    { name: 'Industrial Zone', cx: 2500, cy: 400, count: 15, type: 'factory' },
    { name: 'Military Base', cx: 500, cy: 2400, count: 12, type: 'military' },
    { name: 'Airport', cx: 2400, cy: 2500, count: 14, type: 'airport' },
    { name: 'Forest Camp', cx: 1500, cy: 400, count: 8, type: 'forest' },
    { name: 'Research Lab', cx: 800, cy: 1500, count: 10, type: 'lab' },
    { name: 'Hilltop Outpost', cx: 2200, cy: 1200, count: 8, type: 'outpost' },
    { name: 'Beach Resort', cx: 400, cy: 1200, count: 8, type: 'beach' },
    { name: 'Underground Bunker', cx: 1800, cy: 2200, count: 6, type: 'bunker' }
  ];
  zones.forEach(zone => {
    for (let i = 0; i < zone.count; i++) {
      const w = 40 + Math.random() * 80;
      const h = 40 + Math.random() * 60;
      const x = zone.cx + (Math.random() - 0.5) * 500;
      const y = zone.cy + (Math.random() - 0.5) * 500;
      const color = zone.type === 'city' ? '#3a3f4b' : zone.type === 'factory' ? '#5a4a3a' :
                    zone.type === 'military' ? '#4a5a4a' : zone.type === 'lab' ? '#3a4a5a' :
                    zone.type === 'airport' ? '#4a4a5a' : '#4a3a3a';
      buildings.push({ x, y, w, h, color, zone: zone.name, loot: generateLoot() });
    }
  });
  // Add cover objects
  for (let i = 0; i < 120; i++) {
    buildings.push({
      x: Math.random() * MAP_SIZE, y: Math.random() * MAP_SIZE,
      w: 15 + Math.random() * 25, h: 15 + Math.random() * 25,
      color: '#2d333b', zone: 'wild', loot: Math.random() < 0.3 ? generateLoot() : []
    });
  }
  return { buildings, zones };
}

function generateLoot() {
  const items = [];
  const count = Math.floor(Math.random() * 3) + 1;
  for (let i = 0; i < count; i++) {
    const totalWeight = LOOT_TABLE.reduce((s, l) => s + l.weight, 0);
    let r = Math.random() * totalWeight;
    for (const l of LOOT_TABLE) {
      r -= l.weight;
      if (r <= 0) { items.push({ ...l }); break; }
    }
  }
  return items;
}

// ============ BOT AI ============
function createBot(id, x, y) {
  const charIdx = Math.floor(Math.random() * CHARACTERS.length);
  const weapons = ['pistol', 'smg', 'ar', 'shotgun'];
  const weaponId = weapons[Math.floor(Math.random() * weapons.length)];
  return {
    id, x, y, hp: 100, armor: Math.random() < 0.4 ? 30 + Math.random() * 40 : 0,
    angle: Math.random() * Math.PI * 2, speed: 2 + Math.random(),
    weapon: { ...WEAPON_DEFS[weaponId], ammo: WEAPON_DEFS[weaponId].mag },
    char: CHARACTERS[charIdx],
    state: 'wander', targetX: x, targetY: y,
    lastShot: 0, alive: true, name: `Bot_${id}`,
    wanderTimer: 0, shootAcc: 0.08 + Math.random() * 0.12,
    spotted: false, hpItems: Math.floor(Math.random() * 3)
  };
}

// ============ MAIN GAME ============
let game = null;
const canvas = document.getElementById('gameCanvas');
const ctx = canvas.getContext('2d');

function resizeCanvas() {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
}
window.addEventListener('resize', resizeCanvas);
resizeCanvas();

// Character Selection
let selectedChar = 0;
let selectedMode = 'solo';
function initCharSelect() {
  const container = document.getElementById('charSelect');
  CHARACTERS.forEach((c, i) => {
    const card = document.createElement('div');
    card.className = 'char-card' + (i === 0 ? ' selected' : '');
    card.innerHTML = `<span class="char-icon">${c.icon}</span><div class="char-name">${c.name}</div><div class="char-ability">${c.ability}</div>`;
    card.onclick = () => {
      document.querySelectorAll('.char-card').forEach(el => el.classList.remove('selected'));
      card.classList.add('selected');
      selectedChar = i;
    };
    container.appendChild(card);
  });
}
initCharSelect();

function selectMode(el) {
  document.querySelectorAll('.mode-btn').forEach(b => b.classList.remove('selected'));
  el.classList.add('selected');
  selectedMode = el.dataset.mode;
}

// Drop Phase
function showDropPhase() {
  const dropScreen = document.getElementById('dropScreen');
  dropScreen.classList.add('visible');
  const dc = document.getElementById('dropMapCanvas');
  const dctx = dc.getContext('2d');
  const mapData = generateMap();

  function drawDropMap() {
    dctx.fillStyle = '#1a2332';
    dctx.fillRect(0, 0, 400, 400);
    // Draw zones
    mapData.zones.forEach(z => {
      const sx = (z.cx / MAP_SIZE) * 400;
      const sy = (z.cy / MAP_SIZE) * 400;
      dctx.fillStyle = 'rgba(255,255,255,0.05)';
      dctx.fillRect(sx - 30, sy - 30, 60, 60);
      dctx.fillStyle = '#8b949e';
      dctx.font = '8px sans-serif';
      dctx.textAlign = 'center';
      dctx.fillText(z.name, sx, sy + 40);
    });
    // Draw buildings as dots
    mapData.buildings.forEach(b => {
      const sx = (b.x / MAP_SIZE) * 400;
      const sy = (b.y / MAP_SIZE) * 400;
      dctx.fillStyle = 'rgba(255,255,255,0.15)';
      dctx.fillRect(sx, sy, 3, 2);
    });
    // Flight path
    dctx.strokeStyle = 'rgba(255, 107, 53, 0.5)';
    dctx.lineWidth = 2;
    dctx.setLineDash([5, 5]);
    dctx.beginPath();
    dctx.moveTo(50, 350);
    dctx.lineTo(350, 50);
    dctx.stroke();
    dctx.setLineDash([]);
  }
  drawDropMap();

  dc.onclick = (e) => {
    const rect = dc.getBoundingClientRect();
    const mx = ((e.clientX - rect.left) / rect.width) * MAP_SIZE;
    const my = ((e.clientY - rect.top) / rect.height) * MAP_SIZE;
    dropScreen.classList.remove('visible');
    initGame(mapData, mx, my);
  };
}

// ============ INIT GAME ============
function initGame(mapData, dropX, dropY) {
  initAudio();
  const hud = document.getElementById('hud');
  hud.classList.add('visible');

  // Check if mobile
  const isMobile = 'ontouchstart' in window || navigator.maxTouchPoints > 0;
  if (isMobile) document.getElementById('mobileControls').classList.add('visible');

  const BOT_COUNT = selectedMode === 'solo' ? 29 : selectedMode === 'duo' ? 28 : 27;
  const teamSize = selectedMode === 'solo' ? 1 : selectedMode === 'duo' ? 2 : 4;

  // Create player
  const player = {
    x: dropX || MAP_SIZE / 2, y: dropY || MAP_SIZE / 2,
    hp: 100, armor: selectedChar === 2 ? 75 : 50, // Fortress bonus
    angle: 0, speed: 3.5, radius: 12,
    weapons: [{ ...WEAPON_DEFS.pistol, ammo: WEAPON_DEFS.pistol.mag }],
    currentWeapon: 0,
    alive: true, kills: 0, totalDamage: 0,
    char: CHARACTERS[selectedChar],
    abilityCdLeft: 0, invisTimer: 0, speedBoost: 0,
    lastShot: 0, reloading: false, reloadStart: 0,
    grenades: 2, hpItems: 0,
    dashCd: 0, dashing: false, dashTimer: 0,
    vx: 0, vy: 0
  };

  // Create bots
  const bots = [];
  for (let i = 0; i < BOT_COUNT; i++) {
    let bx, by;
    do {
      bx = 100 + Math.random() * (MAP_SIZE - 200);
      by = 100 + Math.random() * (MAP_SIZE - 200);
    } while (Math.hypot(bx - player.x, by - player.y) < 200);
    bots.push(createBot(i, bx, by));
  }

  // Create floor loot
  const floorLoot = [];
  mapData.buildings.forEach(b => {
    b.loot.forEach(item => {
      floorLoot.push({
        ...item,
        x: b.x + Math.random() * b.w,
        y: b.y + Math.random() * b.h,
        picked: false
      });
    });
  });
  // Extra random loot
  for (let i = 0; i < 80; i++) {
    const totalWeight = LOOT_TABLE.reduce((s, l) => s + l.weight, 0);
    let r = Math.random() * totalWeight;
    for (const l of LOOT_TABLE) {
      r -= l.weight;
      if (r <= 0) {
        floorLoot.push({ ...l, x: Math.random() * MAP_SIZE, y: Math.random() * MAP_SIZE, picked: false });
        break;
      }
    }
  }

  // Safe zone
  const zone = {
    x: MAP_SIZE / 2, y: MAP_SIZE / 2, r: MAP_SIZE * 0.5,
    targetX: MAP_SIZE / 2, targetY: MAP_SIZE / 2, targetR: MAP_SIZE * 0.5,
    phase: 0, timer: 45000, shrinkSpeed: 0,
    damage: 1, nextShrink: 45000
  };

  // Supply drops
  const supplyDrops = [];
  const supplyDropTimer = 60000;

  // Poison zones
  const poisonZones = [];

  // Particles
  const particles = [];

  // Bullets
  const bullets = [];

  // Projectiles (grenades)
  const projectiles = [];

  // Camera
  const camera = { x: 0, y: 0 };

  // Input
  const keys = {};
  let mouseX = 0, mouseY = 0, mouseDown = false;
  let worldMouseX = 0, worldMouseY = 0;

  // Scan
  let scanTimer = 0;

  // Mobile joystick
  let leftJoyX = 0, leftJoyY = 0, rightJoyX = 0, rightJoyY = 0;
  let mobileFiring = false;

  game = {
    mapData, player, bots, floorLoot, bullets, projectiles,
    particles, zone, camera, poisonZones, supplyDrops,
    keys, mouseX, mouseY, mouseDown, worldMouseX, worldMouseY,
    aliveCount: BOT_COUNT + 1, startTime: Date.now(),
    supplyDropTimer, scanTimer, gameOver: false,
    killFeed: [], leftJoyX, leftJoyY, rightJoyX, rightJoyY, mobileFiring,
    isMobile, teamSize, nearestLoot: null
  };

  // Input handlers
  document.addEventListener('keydown', e => {
    keys[e.key.toLowerCase()] = true;
    if (e.key >= '1' && e.key <= '6') switchWeapon(parseInt(e.key) - 1);
    if (e.key.toLowerCase() === 'e') interact();
    if (e.key.toLowerCase() === 'r') reloadWeapon();
    if (e.key.toLowerCase() === 'q') useAbility();
    if (e.key === ' ') { e.preventDefault(); tryDash(); }
    if (e.key.toLowerCase() === 'g') throwGrenade();
  });
  document.addEventListener('keyup', e => { keys[e.key.toLowerCase()] = false; });
  canvas.addEventListener('mousemove', e => { mouseX = e.clientX; mouseY = e.clientY; });
  canvas.addEventListener('mousedown', e => { mouseDown = true; });
  canvas.addEventListener('mouseup', e => { mouseDown = false; });
  canvas.addEventListener('contextmenu', e => e.preventDefault());

  // Mobile joystick
  if (isMobile) {
    setupMobileJoystick();
  }

  // Create weapon slots UI
  createWeaponSlots();

  // Start game loop
  requestAnimationFrame(gameLoop);
}

// ============ MOBILE JOYSTICK ============
function setupMobileJoystick() {
  const g = game;
  const leftArea = document.getElementById('joystickLeft');
  const rightArea = document.getElementById('joystickRight');
  const knobL = document.getElementById('joystickKnobL');
  const knobR = document.getElementById('joystickKnobR');
  const shootBtn = document.getElementById('mobileShoot');

  function handleJoystick(e, area, knob, callback) {
    e.preventDefault();
    const touch = e.touches[0];
    const rect = area.getBoundingClientRect();
    const cx = rect.left + rect.width / 2;
    const cy = rect.top + rect.height / 2;
    let dx = touch.clientX - cx;
    let dy = touch.clientY - cy;
    const dist = Math.hypot(dx, dy);
    const maxDist = rect.width / 2 - 25;
    if (dist > maxDist) { dx = dx / dist * maxDist; dy = dy / dist * maxDist; }
    knob.style.transform = `translate(calc(-50% + ${dx}px), calc(-50% + ${dy}px))`;
    callback(dx / maxDist, dy / maxDist);
  }

  leftArea.addEventListener('touchstart', e => handleJoystick(e, leftArea, knobL, (x, y) => { g.leftJoyX = x; g.leftJoyY = y; }));
  leftArea.addEventListener('touchmove', e => handleJoystick(e, leftArea, knobL, (x, y) => { g.leftJoyX = x; g.leftJoyY = y; }));
  leftArea.addEventListener('touchend', () => { g.leftJoyX = 0; g.leftJoyY = 0; knobL.style.transform = 'translate(-50%, -50%)'; });

  rightArea.addEventListener('touchstart', e => handleJoystick(e, rightArea, knobR, (x, y) => { g.rightJoyX = x; g.rightJoyY = y; }));
  rightArea.addEventListener('touchmove', e => handleJoystick(e, rightArea, knobR, (x, y) => { g.rightJoyX = x; g.rightJoyY = y; }));
  rightArea.addEventListener('touchend', () => { g.rightJoyX = 0; g.rightJoyY = 0; knobR.style.transform = 'translate(-50%, -50%)'; });

  shootBtn.addEventListener('touchstart', e => { e.preventDefault(); g.mobileFiring = true; });
  shootBtn.addEventListener('touchend', () => { g.mobileFiring = false; });
}

// ============ WEAPON SLOTS ============
function createWeaponSlots() {
  const container = document.getElementById('weaponSlots');
  container.innerHTML = '';
  const keys = ['1', '2', '3', '4', '5'];
  keys.forEach((k, i) => {
    const slot = document.createElement('div');
    slot.className = 'inv-slot' + (i === 0 ? ' active' : '');
    slot.innerHTML = `<span class="slot-key">${k}</span><span id="slotIcon${i}"></span>`;
    slot.onclick = () => switchWeapon(i);
    container.appendChild(slot);
  });
}

function switchWeapon(idx) {
  if (!game || !game.player.alive) return;
  const p = game.player;
  if (idx < p.weapons.length) {
    p.currentWeapon = idx;
    p.reloading = false;
    document.querySelectorAll('.inv-slot').forEach((s, i) => {
      s.classList.toggle('active', i === idx);
    });
    updateWeaponUI();
  }
}

function updateWeaponUI() {
  if (!game) return;
  const p = game.player;
  const w = p.weapons[p.currentWeapon];
  if (w) {
    document.getElementById('weaponName').textContent = w.name;
    document.getElementById('ammoCurrent').textContent = w.ammo;
    document.getElementById('ammoReserve').textContent = w.mag * 3;
  }
  // Update slots
  p.weapons.forEach((w, i) => {
    const el = document.getElementById(`slotIcon${i}`);
    if (el) el.textContent = w.icon || '🔫';
  });
}

// ============ INTERACT / LOOT ============
function interact() {
  if (!game || !game.player.alive) return;
  const p = game.player;
  const nearestLoot = game.nearestLoot;
  if (nearestLoot && nearestLoot.dist < 50) {
    pickupItem(nearestLoot.item);
  }
}

function pickupItem(item) {
  if (!game) return;
  const p = game.player;
  if (item.type === 'weapon') {
    if (p.weapons.length < 5) {
      p.weapons.push({ ...WEAPON_DEFS[item.id], ammo: WEAPON_DEFS[item.id].mag });
      switchWeapon(p.weapons.length - 1);
    } else {
      p.weapons[p.currentWeapon] = { ...WEAPON_DEFS[item.id], ammo: WEAPON_DEFS[item.id].mag };
    }
    playPickup();
  } else if (item.type === 'ammo') {
    const w = p.weapons[p.currentWeapon];
    if (w) w.ammo = Math.min(w.ammo + item.amount, w.mag);
    playPickup();
  } else if (item.type === 'health') {
    p.hp = Math.min(100, p.hp + item.amount);
    playPickup();
  } else if (item.type === 'armor') {
    p.armor = Math.min(100, p.armor + item.amount);
    playPickup();
  } else if (item.type === 'grenade') {
    p.grenades = Math.min(5, p.grenades + 1);
    playPickup();
  }
  item.picked = true;
  updateWeaponUI();
  updateHUD();
}

// ============ RELOAD ============
function reloadWeapon() {
  if (!game || !game.player.alive) return;
  const p = game.player;
  const w = p.weapons[p.currentWeapon];
  if (w && w.ammo < w.mag && !p.reloading) {
    p.reloading = true;
    p.reloadStart = Date.now();
    playSound(300, 0.2, 'square', 0.1);
  }
}

// ============ ABILITY ============
function useAbility() {
  if (!game || !game.player.alive) return;
  const p = game.player;
  if (p.abilityCdLeft > 0) return;
  p.char.useAbility(game);
  p.abilityCdLeft = p.char.abilityCd;
}

// ============ DASH ============
function tryDash() {
  if (!game || !game.player.alive) return;
  const p = game.player;
  if (p.dashCd > 0 || p.dashing) return;
  p.dashing = true;
  p.dashTimer = 200;
  p.dashCd = 2000;
  playDash();
}

// ============ GRENADE ============
function throwGrenade() {
  if (!game || !game.player.alive || game.player.grenades <= 0) return;
  const p = game.player;
  p.grenades--;
  game.projectiles.push({
    x: p.x, y: p.y,
    vx: Math.cos(p.angle) * 8, vy: Math.sin(p.angle) * 8,
    timer: 1500, owner: p.id, type: 'grenade'
  });
  playSound(400, 0.15, 'sine', 0.1);
}

// ============ SHOOTING ============
function tryShoot(entity, isBot = false) {
  const now = Date.now();
  const w = entity.weapon || entity.weapons[entity.currentWeapon];
  if (!w) return;
  if (entity.reloading) return;
  if (now - entity.lastShot < w.fireRate) return;
  if (w.ammo <= 0) {
    if (!isBot) reloadWeapon();
    return;
  }

  entity.lastShot = now;
  w.ammo--;

  const pellets = w.pellets || 1;
  for (let i = 0; i < pellets; i++) {
    const spread = (isBot ? entity.shootAcc : w.spread) * (Math.random() - 0.5) * 2;
    const angle = entity.angle + spread;
    game.bullets.push({
      x: entity.x + Math.cos(entity.angle) * 15,
      y: entity.y + Math.sin(entity.angle) * 15,
      vx: Math.cos(angle) * w.speed,
      vy: Math.sin(angle) * w.speed,
      damage: w.damage, range: w.range,
      dist: 0, owner: entity.id, size: w.bulletSize,
      color: w.color
    });
  }

  if (!isBot) playShoot(w.type);
  // Muzzle flash
  game.particles.push({
    x: entity.x + Math.cos(entity.angle) * 18,
    y: entity.y + Math.sin(entity.angle) * 18,
    vx: 0, vy: 0, life: 80, maxLife: 80,
    size: 8, color: '#f7c948', type: 'flash'
  });

  if (!isBot) updateWeaponUI();
}

// ============ BOT AI UPDATE ============
function updateBot(bot, dt) {
  if (!bot.alive) return;

  const p = game.player;
  const distToPlayer = Math.hypot(bot.x - p.x, bot.y - p.y);

  // Simple AI states
  bot.wanderTimer -= dt;

  // Check for nearby enemies (other bots or player)
  let nearestEnemy = null;
  let nearestDist = Infinity;

  // Check player
  if (p.alive && distToPlayer < 400) {
    nearestEnemy = p;
    nearestDist = distToPlayer;
  }

  // Check other bots
  game.bots.forEach(other => {
    if (other === bot || !other.alive) return;
    const d = Math.hypot(bot.x - other.x, bot.y - other.y);
    if (d < 300 && d < nearestDist) {
      nearestEnemy = other;
      nearestDist = d;
    }
  });

  // Zone check - move toward safe zone if outside
  const distToZone = Math.hypot(bot.x - game.zone.x, bot.y - game.zone.y);
  const inZone = distToZone < game.zone.r;

  if (!inZone) {
    // Move toward zone center
    const angle = Math.atan2(game.zone.y - bot.y, game.zone.x - bot.x);
    bot.x += Math.cos(angle) * bot.speed * 1.2;
    bot.y += Math.sin(angle) * bot.speed * 1.2;
    bot.angle = angle;
  } else if (nearestEnemy && nearestDist < 350) {
    // Combat mode
    const angle = Math.atan2(nearestEnemy.y - bot.y, nearestEnemy.x - bot.x);
    bot.angle = angle;

    // Shoot
    if (nearestDist < 300 && Math.random() < 0.6) {
      tryShoot(bot, true);
    }

    // Strafe
    const strafeAngle = angle + (Math.random() < 0.5 ? Math.PI / 2 : -Math.PI / 2);
    bot.x += Math.cos(strafeAngle) * bot.speed * 0.5;
    bot.y += Math.sin(strafeAngle) * bot.speed * 0.5;

    // Keep distance
    if (nearestDist < 100) {
      bot.x -= Math.cos(angle) * bot.speed;
      bot.y -= Math.sin(angle) * bot.speed;
    }
  } else {
    // Wander
    if (bot.wanderTimer <= 0) {
      bot.targetX = bot.x + (Math.random() - 0.5) * 400;
      bot.targetY = bot.y + (Math.random() - 0.5) * 400;
      bot.targetX = Math.max(50, Math.min(MAP_SIZE - 50, bot.targetX));
      bot.targetY = Math.max(50, Math.min(MAP_SIZE - 50, bot.targetY));
      bot.wanderTimer = 2000 + Math.random() * 3000;
    }
    const angle = Math.atan2(bot.targetY - bot.y, bot.targetX - bot.x);
    bot.x += Math.cos(angle) * bot.speed * 0.6;
    bot.y += Math.sin(angle) * bot.speed * 0.6;
    bot.angle = angle;
  }

  // Pickup loot
  game.floorLoot.forEach(item => {
    if (item.picked) return;
    if (Math.hypot(bot.x - item.x, bot.y - item.y) < 30) {
      if (item.type === 'weapon' && Math.random() < 0.3) {
        bot.weapon = { ...WEAPON_DEFS[item.id], ammo: WEAPON_DEFS[item.id].mag };
        item.picked = true;
      } else if (item.type === 'health' && bot.hp < 60) {
        bot.hp = Math.min(100, bot.hp + item.amount);
        item.picked = true;
      }
    }
  });

  // Clamp to map
  bot.x = Math.max(10, Math.min(MAP_SIZE - 10, bot.x));
  bot.y = Math.max(10, Math.min(MAP_SIZE - 10, bot.y));

  // Zone damage
  if (!inZone) {
    bot.hp -= game.zone.damage * dt / 1000;
    if (bot.hp <= 0) {
      eliminateBot(bot, null, 'zone');
    }
  }
}

function eliminateBot(bot, killer, cause) {
  if (!bot.alive) return;
  bot.alive = false;
  game.aliveCount--;

  playDeath();

  // Death particles
  for (let i = 0; i < 15; i++) {
    game.particles.push({
      x: bot.x, y: bot.y,
      vx: (Math.random() - 0.5) * 5, vy: (Math.random() - 0.5) * 5,
      life: 500 + Math.random() * 500, maxLife: 1000,
      size: 3 + Math.random() * 3, color: '#e74c3c', type: 'particle'
    });
  }

  // Drop loot
  const weapons = ['smg', 'ar', 'shotgun', 'dmr'];
  const wid = weapons[Math.floor(Math.random() * weapons.length)];
  game.floorLoot.push({
    type: 'weapon', id: wid, icon: '🔫', name: WEAPON_DEFS[wid].name,
    x: bot.x, y: bot.y, picked: false
  });
  game.floorLoot.push({
    type: 'ammo', amount: 30, icon: '🔵', name: 'Ammo',
    x: bot.x + 15, y: bot.y, picked: false
  });

  // Kill feed
  const killerName = killer ? (killer === game.player ? 'You' : killer.name) : 'Zone';
  addKillFeed(killerName, bot.name, cause);

  if (killer === game.player) {
    game.player.kills++;
    game.player.totalDamage += 100;
    document.getElementById('killCount').textContent = game.player.kills;
  }

  updateAliveCount();
  checkGameOver();
}

function addKillFeed(killer, victim, cause) {
  const feed = document.getElementById('killFeed');
  const msg = document.createElement('div');
  msg.className = 'kill-msg';
  if (cause === 'zone') {
    msg.innerHTML = `<span class="victim">${victim}</span> died to the storm`;
  } else if (cause === 'explosion') {
    msg.innerHTML = `<span class="killer">${killer}</span> 💥 <span class="victim">${victim}</span>`;
  } else {
    msg.innerHTML = `<span class="killer">${killer}</span> ☠ <span class="victim">${victim}</span>`;
  }
  feed.prepend(msg);
  if (feed.children.length > 5) feed.removeChild(feed.lastChild);
  setTimeout(() => { if (msg.parentNode) msg.remove(); }, 5000);
}

function updateAliveCount() {
  document.getElementById('aliveCount').textContent = game.aliveCount;
}

function checkGameOver() {
  const p = game.player;
  if (!p.alive) {
    endGame(false);
  } else if (game.aliveCount <= 1) {
    endGame(true);
  }
}

function endGame(won) {
  game.gameOver = true;
  const go = document.getElementById('gameOver');
  go.classList.add('visible');

  const rt = document.getElementById('resultText');
  if (won) {
    rt.textContent = '🏆 VICTORY ROYALE 🏆';
    rt.className = 'result-text win';
  } else {
    rt.textContent = 'ELIMINATED';
    rt.className = 'result-text lose';
  }

  const placement = won ? 1 : Math.max(1, game.aliveCount);
  document.getElementById('placementText').textContent = `Placement: #${placement}`;
  document.getElementById('finalKills').textContent = game.player.kills;
  document.getElementById('finalDamage').textContent = Math.round(game.player.totalDamage);

  const elapsed = Math.floor((Date.now() - game.startTime) / 1000);
  const mins = Math.floor(elapsed / 60);
  const secs = elapsed % 60;
  document.getElementById('finalSurvival').textContent = `${mins}:${secs.toString().padStart(2, '0')}`;
}

// ============ GAME LOOP ============
let lastTime = 0;
function gameLoop(timestamp) {
  if (!game || game.gameOver) return;
  const dt = Math.min(timestamp - (lastTime || timestamp), 50);
  lastTime = timestamp;

  update(dt);
  render();
  requestAnimationFrame(gameLoop);
}

function update(dt) {
  const g = game;
  const p = g.player;
  if (!p.alive) return;

  // Player movement
  let mx = 0, my = 0;
  if (g.isMobile) {
    mx = g.leftJoyX;
    my = g.leftJoyY;
  } else {
    if (g.keys['w'] || g.keys['arrowup']) my -= 1;
    if (g.keys['s'] || g.keys['arrowdown']) my += 1;
    if (g.keys['a'] || g.keys['arrowleft']) mx -= 1;
    if (g.keys['d'] || g.keys['arrowright']) mx += 1;
  }

  // Normalize
  const mlen = Math.hypot(mx, my);
  if (mlen > 0) { mx /= mlen; my /= mlen; }

  let speed = p.speed;
  if (g.keys['shift'] || p.speedBoost > 0) speed *= 1.5;

  if (p.dashing) {
    speed *= 3;
    p.dashTimer -= dt;
    if (p.dashTimer <= 0) p.dashing = false;
  }

  p.vx = mx * speed;
  p.vy = my * speed;
  p.x += p.vx;
  p.y += p.vy;

  // Clamp
  p.x = Math.max(10, Math.min(MAP_SIZE - 10, p.x));
  p.y = Math.max(10, Math.min(MAP_SIZE - 10, p.y));

  // Collision with buildings
  g.mapData.buildings.forEach(b => {
    const cx = Math.max(b.x, Math.min(b.x + b.w, p.x));
    const cy = Math.max(b.y, Math.min(b.y + b.h, p.y));
    const dist = Math.hypot(p.x - cx, p.y - cy);
    if (dist < p.radius) {
      const angle = Math.atan2(p.y - cy, p.x - cx);
      p.x = cx + Math.cos(angle) * p.radius;
      p.y = cy + Math.sin(angle) * p.radius;
    }
  });

  // Camera
  g.camera.x = p.x - canvas.width / 2;
  g.camera.y = p.y - canvas.height / 2;

  // Player angle
  if (g.isMobile) {
    if (Math.abs(g.rightJoyX) > 0.1 || Math.abs(g.rightJoyY) > 0.1) {
      p.angle = Math.atan2(g.rightJoyY, g.rightJoyX);
    }
  } else {
    g.worldMouseX = mouseX + g.camera.x;
    g.worldMouseY = mouseY + g.camera.y;
    p.angle = Math.atan2(g.worldMouseY - p.y, g.worldMouseX - p.x);
  }

  // Shooting
  const shooting = g.mouseDown || g.mobileFiring;
  if (shooting && !p.reloading) {
    const w = p.weapons[p.currentWeapon];
    if (w) {
      if (w.auto || (!w.auto && !g._lastMouseDown)) {
        tryShoot(p, false);
      }
    }
  }
  g._lastMouseDown = shooting;

  // Reload
  if (p.reloading) {
    const w = p.weapons[p.currentWeapon];
    if (w && Date.now() - p.reloadStart >= w.reloadTime) {
      w.ammo = w.mag;
      p.reloading = false;
      updateWeaponUI();
      playSound(500, 0.1, 'sine', 0.1);
    }
  }

  // Timers
  if (p.invisTimer > 0) p.invisTimer -= dt;
  if (p.speedBoost > 0) p.speedBoost -= dt;
  if (p.abilityCdLeft > 0) p.abilityCdLeft -= dt;
  if (p.dashCd > 0) p.dashCd -= dt;

  // Ability UI
  const abilityPct = Math.max(0, p.abilityCdLeft / p.char.abilityCd) * 100;
  document.getElementById('abilityCdOverlay').style.height = abilityPct + '%';
  document.getElementById('abilityCdText').textContent = p.abilityCdLeft > 0 ? Math.ceil(p.abilityCdLeft / 1000) : '';

  // Find nearest loot
  g.nearestLoot = null;
  let nearestDist = 60;
  g.floorLoot.forEach(item => {
    if (item.picked) return;
    const d = Math.hypot(p.x - item.x, p.y - item.y);
    if (d < nearestDist) {
      nearestDist = d;
      g.nearestLoot = { item, dist: d };
    }
  });

  // Interact prompt
  const prompt = document.getElementById('interactPrompt');
  if (g.nearestLoot) {
    prompt.classList.add('visible');
    const item = g.nearestLoot.item;
    prompt.textContent = `Press E: ${item.name || item.id}`;
  } else {
    prompt.classList.remove('visible');
  }

  // Safe zone
  g.zone.timer -= dt;
  if (g.zone.timer <= 0) {
    g.zone.phase++;
    g.zone.timer = Math.max(15000, 45000 - g.zone.phase * 8000);
    g.zone.targetR = Math.max(80, g.zone.r * 0.65);
    g.zone.targetX = g.zone.x + (Math.random() - 0.5) * 200;
    g.zone.targetY = g.zone.y + (Math.random() - 0.5) * 200;
    g.zone.targetX = Math.max(g.zone.targetR, Math.min(MAP_SIZE - g.zone.targetR, g.zone.targetX));
    g.zone.targetY = Math.max(g.zone.targetR, Math.min(MAP_SIZE - g.zone.targetR, g.zone.targetY));
    g.zone.damage = Math.min(10, 1 + g.zone.phase * 2);
  }

  // Shrink zone
  const z = g.zone;
  const shrinkSpeed = 0.02 * dt / 16;
  z.x += (z.targetX - z.x) * shrinkSpeed;
  z.y += (z.targetY - z.y) * shrinkSpeed;
  z.r += (z.targetR - z.r) * shrinkSpeed;

  // Zone damage to player
  const playerDistToZone = Math.hypot(p.x - z.x, p.y - z.y);
  if (playerDistToZone > z.r) {
    p.hp -= z.damage * dt / 1000;
    if (p.hp <= 0) {
      p.alive = false;
      p.hp = 0;
      game.aliveCount--;
      addKillFeed('Zone', 'You', 'zone');
      checkGameOver();
    }
    updateHUD();
  }

  // Zone timer UI
  document.getElementById('zoneTimer').textContent = `Zone: ${Math.ceil(z.timer / 1000)}s | Phase ${z.phase + 1}`;

  // Update bullets
  for (let i = g.bullets.length - 1; i >= 0; i--) {
    const b = g.bullets[i];
    b.x += b.vx;
    b.y += b.vy;
    b.dist += Math.hypot(b.vx, b.vy);

    if (b.dist > b.range || b.x < 0 || b.x > MAP_SIZE || b.y < 0 || b.y > MAP_SIZE) {
      g.bullets.splice(i, 1);
      continue;
    }

    // Check building collision
    let hitBuilding = false;
    g.mapData.buildings.forEach(bld => {
      if (b.x > bld.x && b.x < bld.x + bld.w && b.y > bld.y && b.y < bld.y + bld.h) {
        hitBuilding = true;
      }
    });
    if (hitBuilding) {
      g.bullets.splice(i, 1);
      continue;
    }

    // Hit player
    if (b.owner !== p.id && p.alive && p.invisTimer <= 0) {
      if (Math.hypot(b.x - p.x, b.y - p.y) < p.radius + b.size) {
        let dmg = b.damage;
        if (p.armor > 0) {
          const armorAbsorb = Math.min(p.armor, dmg * 0.6);
          p.armor -= armorAbsorb;
          dmg -= armorAbsorb;
        }
        p.hp -= dmg;
        g.bullets.splice(i, 1);
        playHit();
        showDamageFlash();

        // Find shooter
        const shooter = g.bots.find(bot => bot.id === b.owner);
        if (shooter) {
          p.totalDamage += b.damage;
        }

        if (p.hp <= 0) {
          p.alive = false;
          p.hp = 0;
          game.aliveCount--;
          if (shooter) {
            shooter.hp = Math.min(100, shooter.hp + 20);
            addKillFeed(shooter.name, 'You', 'bullet');
          }
          checkGameOver();
        }
        updateHUD();
        continue;
      }
    }

    // Hit bots
    let hitBot = false;
    for (const bot of g.bots) {
      if (!bot.alive || bot.id === b.owner) continue;
      if (Math.hypot(b.x - bot.x, b.y - bot.y) < 12 + b.size) {
        let dmg = b.damage;
        if (bot.armor > 0) {
          const armorAbsorb = Math.min(bot.armor, dmg * 0.6);
          bot.armor -= armorAbsorb;
          dmg -= armorAbsorb;
        }
        bot.hp -= dmg;

        if (b.owner === p.id) {
          p.totalDamage += b.damage;
          showHitMarker();
        }

        if (bot.hp <= 0) {
          const killer = b.owner === p.id ? p : g.bots.find(bb => bb.id === b.owner);
          eliminateBot(bot, killer, 'bullet');
        }
        hitBot = true;
        g.bullets.splice(i, 1);
        break;
      }
    }
    if (hitBot) continue;
  }

  // Update projectiles (grenades)
  for (let i = g.projectiles.length - 1; i >= 0; i--) {
    const proj = g.projectiles[i];
    proj.x += proj.vx;
    proj.y += proj.vy;
    proj.vx *= 0.98;
    proj.vy *= 0.98;
    proj.timer -= dt;

    if (proj.timer <= 0) {
      // Explode
      playExplosion();
      for (let j = 0; j < 20; j++) {
        g.particles.push({
          x: proj.x, y: proj.y,
          vx: (Math.random() - 0.5) * 8, vy: (Math.random() - 0.5) * 8,
          life: 400 + Math.random() * 400, maxLife: 800,
          size: 4 + Math.random() * 4, color: '#ff6b35', type: 'particle'
        });
      }

      // Damage
      const radius = 100;
      if (proj.owner === p.id || proj.owner !== p.id) {
        if (Math.hypot(proj.x - p.x, proj.y - p.y) < radius && p.alive) {
          const dmg = 60 * (1 - Math.hypot(proj.x - p.x, proj.y - p.y) / radius);
          p.hp -= dmg;
          showDamageFlash();
          if (p.hp <= 0) {
            p.alive = false; p.hp = 0; game.aliveCount--;
            addKillFeed('Explosion', 'You', 'explosion');
            checkGameOver();
          }
          updateHUD();
        }
      }
      g.bots.forEach(bot => {
        if (!bot.alive) return;
        if (Math.hypot(proj.x - bot.x, proj.y - bot.y) < radius) {
          const dmg = 60 * (1 - Math.hypot(proj.x - bot.x, proj.y - bot.y) / radius);
          bot.hp -= dmg;
          if (bot.hp <= 0) {
            const killer = proj.owner === p.id ? p : g.bots.find(bb => bb.id === proj.owner);
            eliminateBot(bot, killer, 'explosion');
          }
        }
      });

      g.projectiles.splice(i, 1);
    }
  }

  // Update bots
  g.bots.forEach(bot => updateBot(bot, dt));

  // Bot vs bot zone damage already handled in updateBot

  // Particles
  for (let i = g.particles.length - 1; i >= 0; i--) {
    const part = g.particles[i];
    part.x += part.vx;
    part.y += part.vy;
    part.vx *= 0.95;
    part.vy *= 0.95;
    part.life -= dt;
    if (part.life <= 0) g.particles.splice(i, 1);
  }

  // Poison zones
  for (let i = g.poisonZones.length - 1; i >= 0; i--) {
    const pz = g.poisonZones[i];
    pz.dur -= dt;
    if (pz.dur <= 0) { g.poisonZones.splice(i, 1); continue; }
    // Damage bots in zone
    g.bots.forEach(bot => {
      if (!bot.alive) return;
      if (Math.hypot(bot.x - pz.x, bot.y - pz.y) < pz.r) {
        bot.hp -= 5 * dt / 1000;
        if (bot.hp <= 0) {
          const killer = pz.owner === p.id ? p : null;
          eliminateBot(bot, killer, 'poison');
        }
      }
    });
    // Damage player
    if (Math.hypot(p.x - pz.x, p.y - pz.y) < pz.r && pz.owner !== p.id) {
      p.hp -= 5 * dt / 1000;
      if (p.hp <= 0) {
        p.alive = false; p.hp = 0; game.aliveCount--;
        checkGameOver();
      }
      updateHUD();
    }
  }

  // Scan timer
  if (g.scanTimer > 0) g.scanTimer -= dt;

  // Supply drops
  g.supplyDropTimer -= dt;
  if (g.supplyDropTimer <= 0) {
    g.supplyDropTimer = 40000 + Math.random() * 20000;
    g.supplyDrops.push({
      x: 200 + Math.random() * (MAP_SIZE - 400),
      y: 200 + Math.random() * (MAP_SIZE - 400),
      opened: false
    });
  }

  // Pickup supply drops
  g.supplyDrops.forEach(drop => {
    if (drop.opened) return;
    if (Math.hypot(p.x - drop.x, p.y - drop.y) < 35) {
      drop.opened = true;
      // Give good loot
      if (p.weapons.length < 5) {
        const goodWeapons = ['ar', 'sniper', 'dmr'];
        const wid = goodWeapons[Math.floor(Math.random() * goodWeapons.length)];
        p.weapons.push({ ...WEAPON_DEFS[wid], ammo: WEAPON_DEFS[wid].mag });
      }
      p.armor = Math.min(100, p.armor + 50);
      p.hp = Math.min(100, p.hp + 30);
      playPickup();
      playPickup();
      updateWeaponUI();
      updateHUD();
    }
  });

  // Auto pickup for bots
  g.bots.forEach(bot => {
    if (!bot.alive) return;
    g.supplyDrops.forEach(drop => {
      if (drop.opened) return;
      if (Math.hypot(bot.x - drop.x, bot.y - drop.y) < 35) {
        drop.opened = true;
        bot.hp = Math.min(100, bot.hp + 30);
        bot.armor = Math.min(100, bot.armor + 30);
      }
    });
  });

  updateHUD();
}

function updateHUD() {
  if (!game) return;
  const p = game.player;
  document.getElementById('healthBar').style.width = Math.max(0, p.hp) + '%';
  document.getElementById('healthText').textContent = Math.max(0, Math.round(p.hp));
  document.getElementById('armorBar').style.width = Math.max(0, p.armor) + '%';
  document.getElementById('armorText').textContent = Math.max(0, Math.round(p.armor));

  const w = p.weapons[p.currentWeapon];
  if (w) {
    document.getElementById('ammoCurrent').textContent = w.ammo;
  }
}

function showDamageFlash() {
  const flash = document.getElementById('damageFlash');
  flash.classList.add('active');
  setTimeout(() => flash.classList.remove('active'), 200);
}

function showHitMarker() {
  const marker = document.getElementById('hitMarker');
  marker.classList.add('active');
  playHit();
  setTimeout(() => marker.classList.remove('active'), 150);
}

// ============ RENDER ============
function render() {
  if (!game) return;
  const g = game;
  const p = g.player;
  const cam = g.camera;

  ctx.clearRect(0, 0, canvas.width, canvas.height);

  // Background
  ctx.fillStyle = '#1a2332';
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  // Grid
  ctx.strokeStyle = 'rgba(255,255,255,0.03)';
  ctx.lineWidth = 1;
  const gridSize = 100;
  const startX = -(cam.x % gridSize);
  const startY = -(cam.y % gridSize);
  for (let x = startX; x < canvas.width; x += gridSize) {
    ctx.beginPath(); ctx.moveTo(x, 0); ctx.lineTo(x, canvas.height); ctx.stroke();
  }
  for (let y = startY; y < canvas.height; y += gridSize) {
    ctx.beginPath(); ctx.moveTo(0, y); ctx.lineTo(canvas.width, y); ctx.stroke();
  }

  // Safe zone
  ctx.save();
  ctx.translate(-cam.x, -cam.y);

  // Draw zone border (outside is danger)
  ctx.beginPath();
  ctx.rect(-500, -500, MAP_SIZE + 1000, MAP_SIZE + 1000);
  ctx.arc(g.zone.x, g.zone.y, g.zone.r, 0, Math.PI * 2, true);
  ctx.fillStyle = 'rgba(231, 76, 60, 0.15)';
  ctx.fill();

  // Zone circle border
  ctx.beginPath();
  ctx.arc(g.zone.x, g.zone.y, g.zone.r, 0, Math.PI * 2);
  ctx.strokeStyle = '#3498db';
  ctx.lineWidth = 3;
  ctx.stroke();

  // Next zone
  ctx.beginPath();
  ctx.arc(g.zone.targetX, g.zone.targetY, g.zone.targetR, 0, Math.PI * 2);
  ctx.strokeStyle = 'rgba(255,255,255,0.2)';
  ctx.lineWidth = 2;
  ctx.setLineDash([8, 8]);
  ctx.stroke();
  ctx.setLineDash([]);

  // Poison zones
  g.poisonZones.forEach(pz => {
    ctx.beginPath();
    ctx.arc(pz.x, pz.y, pz.r, 0, Math.PI * 2);
    ctx.fillStyle = 'rgba(46, 204, 113, 0.2)';
    ctx.fill();
    ctx.strokeStyle = 'rgba(46, 204, 113, 0.5)';
    ctx.lineWidth = 2;
    ctx.stroke();
  });

  // Buildings
  g.mapData.buildings.forEach(b => {
    if (b.x + b.w < cam.x - 50 || b.x > cam.x + canvas.width + 50 ||
        b.y + b.h < cam.y - 50 || b.y > cam.y + canvas.height + 50) return;

    ctx.fillStyle = b.color;
    ctx.fillRect(b.x, b.y, b.w, b.h);
    ctx.strokeStyle = 'rgba(255,255,255,0.1)';
    ctx.lineWidth = 1;
    ctx.strokeRect(b.x, b.y, b.w, b.h);

    // Windows
    ctx.fillStyle = 'rgba(135, 206, 250, 0.2)';
    for (let wx = b.x + 10; wx < b.x + b.w - 10; wx += 20) {
      ctx.fillRect(wx, b.y + 5, 8, 6);
    }
  });

  // Floor loot
  g.floorLoot.forEach(item => {
    if (item.picked) return;
    if (item.x < cam.x - 30 || item.x > cam.x + canvas.width + 30 ||
        item.y < cam.y - 30 || item.y > cam.y + canvas.height + 30) return;

    ctx.beginPath();
    ctx.arc(item.x, item.y, 6, 0, Math.PI * 2);
    const rarityColor = item.type === 'weapon' ? (['sniper', 'dmr'].includes(item.id) ? '#9b59b6' : '#3498db') :
                        item.type === 'health' ? '#2ecc71' :
                        item.type === 'armor' ? '#5dade2' : '#f7c948';
    ctx.fillStyle = rarityColor;
    ctx.fill();
    ctx.strokeStyle = '#fff';
    ctx.lineWidth = 1;
    ctx.stroke();

    // Glow
    ctx.beginPath();
    ctx.arc(item.x, item.y, 10, 0, Math.PI * 2);
    ctx.fillStyle = rarityColor.replace(')', ', 0.15)').replace('rgb', 'rgba');
    ctx.fill();
  });

  // Supply drops
  g.supplyDrops.forEach(drop => {
    if (drop.opened) return;
    if (drop.x < cam.x - 30 || drop.x > cam.x + canvas.width + 30 ||
        drop.y < cam.y - 30 || drop.y > cam.y + canvas.height + 30) return;

    ctx.beginPath();
    ctx.arc(drop.x, drop.y, 12, 0, Math.PI * 2);
    ctx.fillStyle = '#f7c948';
    ctx.fill();
    ctx.strokeStyle = '#fff';
    ctx.lineWidth = 2;
    ctx.stroke();

    // Parachute icon
    ctx.font = '14px sans-serif';
    ctx.textAlign = 'center';
    ctx.fillText('📦', drop.x, drop.y + 5);

    // Pulse
    ctx.beginPath();
    ctx.arc(drop.x, drop.y, 18 + Math.sin(Date.now() / 300) * 4, 0, Math.PI * 2);
    ctx.strokeStyle = 'rgba(247, 201, 72, 0.3)';
    ctx.lineWidth = 2;
    ctx.stroke();
  });

  // Particles
  g.particles.forEach(part => {
    if (part.x < cam.x - 20 || part.x > cam.x + canvas.width + 20 ||
        part.y < cam.y - 20 || part.y > cam.y + canvas.height + 20) return;

    const alpha = part.life / part.maxLife;
    ctx.globalAlpha = alpha;
    ctx.beginPath();
    ctx.arc(part.x, part.y, part.size * alpha, 0, Math.PI * 2);
    ctx.fillStyle = part.color;
    ctx.fill();
    ctx.globalAlpha = 1;
  });

  // Bullets
  g.bullets.forEach(b => {
    if (b.x < cam.x - 10 || b.x > cam.x + canvas.width + 10 ||
        b.y < cam.y - 10 || b.y > cam.y + canvas.height + 10) return;

    ctx.beginPath();
    ctx.arc(b.x, b.y, b.size, 0, Math.PI * 2);
    ctx.fillStyle = b.color || '#f7c948';
    ctx.fill();

    // Trail
    ctx.beginPath();
    ctx.moveTo(b.x, b.y);
    ctx.lineTo(b.x - b.vx * 2, b.y - b.vy * 2);
    ctx.strokeStyle = 'rgba(247, 201, 72, 0.4)';
    ctx.lineWidth = 1.5;
    ctx.stroke();
  });

  // Projectiles
  g.projectiles.forEach(proj => {
    ctx.beginPath();
    ctx.arc(proj.x, proj.y, 5, 0, Math.PI * 2);
    ctx.fillStyle = '#e74c3c';
    ctx.fill();
  });

  // Bots
  g.bots.forEach(bot => {
    if (!bot.alive) return;
    if (bot.x < cam.x - 50 || bot.x > cam.x + canvas.width + 50 ||
        bot.y < cam.y - 50 || bot.y > cam.y + canvas.height + 50) return;

    // During scan, show all bots
    if (g.scanTimer > 0) {
      ctx.beginPath();
      ctx.arc(bot.x, bot.y, 18, 0, Math.PI * 2);
      ctx.strokeStyle = 'rgba(231, 76, 60, 0.5)';
      ctx.lineWidth = 1;
      ctx.stroke();
    }

    drawCharacter(ctx, bot, bot.char.color, cam);
  });

  // Player
  if (p.alive) {
    if (p.invisTimer > 0) {
      ctx.globalAlpha = 0.3;
    }
    drawCharacter(ctx, p, p.char.color, cam);
    ctx.globalAlpha = 1;
  }

  // Crosshair
  if (!g.isMobile && p.alive) {
    const cx = mouseX;
    const cy = mouseY;
    ctx.strokeStyle = 'rgba(255,255,255,0.7)';
    ctx.lineWidth = 1.5;
    ctx.beginPath();
    ctx.moveTo(cx - 10, cy); ctx.lineTo(cx - 4, cy);
    ctx.moveTo(cx + 4, cy); ctx.lineTo(cx + 10, cy);
    ctx.moveTo(cx, cy - 10); ctx.lineTo(cx, cy - 4);
    ctx.moveTo(cx, cy + 4); ctx.lineTo(cx, cy + 10);
    ctx.stroke();

    ctx.beginPath();
    ctx.arc(cx, cy, 2, 0, Math.PI * 2);
    ctx.fillStyle = 'rgba(255,255,255,0.5)';
    ctx.fill();
  }

  ctx.restore();

  // Render minimap
  renderMinimap();
}

function drawCharacter(ctx, entity, color, cam) {
  const x = entity.x;
  const y = entity.y;

  // Body
  ctx.beginPath();
  ctx.arc(x, y, 12, 0, Math.PI * 2);
  ctx.fillStyle = color;
  ctx.fill();
  ctx.strokeStyle = '#fff';
  ctx.lineWidth = 2;
  ctx.stroke();

  // Direction indicator / weapon
  ctx.save();
  ctx.translate(x, y);
  ctx.rotate(entity.angle);
  ctx.fillStyle = '#888';
  ctx.fillRect(8, -2, 12, 4);
  ctx.restore();

  // HP bar
  ctx.fillStyle = 'rgba(0,0,0,0.5)';
  ctx.fillRect(x - 14, y - 22, 28, 4);
  const hpPct = Math.max(0, entity.hp / 100);
  ctx.fillStyle = hpPct > 0.5 ? '#2ecc71' : hpPct > 0.25 ? '#f7c948' : '#e74c3c';
  ctx.fillRect(x - 14, y - 22, 28 * hpPct, 4);

  // Armor bar
  if (entity.armor > 0) {
    ctx.fillStyle = 'rgba(0,0,0,0.5)';
    ctx.fillRect(x - 14, y - 27, 28, 3);
    ctx.fillStyle = '#5dade2';
    ctx.fillRect(x - 14, y - 27, 28 * Math.min(1, entity.armor / 100), 3);
  }

  // Name
  ctx.font = '9px sans-serif';
  ctx.textAlign = 'center';
  ctx.fillStyle = '#ccc';
  ctx.fillText(entity.name || entity.char?.name || '', x, y - 30);
}

function renderMinimap() {
  if (!game) return;
  const mc = document.getElementById('minimapCanvas');
  const mctx = mc.getContext('2d');
  const size = mc.width = mc.offsetWidth;
  mc.height = size;

  mctx.fillStyle = '#0d1117';
  mctx.fillRect(0, 0, size, size);

  const scale = size / MAP_SIZE;

  // Zone
  mctx.beginPath();
  mctx.arc(game.zone.x * scale, game.zone.y * scale, game.zone.r * scale, 0, Math.PI * 2);
  mctx.strokeStyle = '#3498db';
  mctx.lineWidth = 1.5;
  mctx.stroke();

  // Buildings
  mctx.fillStyle = 'rgba(255,255,255,0.1)';
  game.mapData.buildings.forEach(b => {
    if (b.zone === 'wild') return;
    mctx.fillRect(b.x * scale, b.y * scale, Math.max(2, b.w * scale), Math.max(1, b.h * scale));
  });

  // Bots as dots (only during scan)
  if (game.scanTimer > 0) {
    mctx.fillStyle = 'rgba(231, 76, 60, 0.7)';
    game.bots.forEach(bot => {
      if (!bot.alive) return;
      mctx.fillRect(bot.x * scale - 1.5, bot.y * scale - 1.5, 3, 3);
    });
  }

  // Player
  mctx.fillStyle = '#2ecc71';
  mctx.beginPath();
  mctx.arc(game.player.x * scale, game.player.y * scale, 3, 0, Math.PI * 2);
  mctx.fill();

  // Direction
  mctx.strokeStyle = '#2ecc71';
  mctx.lineWidth = 1;
  mctx.beginPath();
  mctx.moveTo(game.player.x * scale, game.player.y * scale);
  mctx.lineTo(
    game.player.x * scale + Math.cos(game.player.angle) * 8,
    game.player.y * scale + Math.sin(game.player.angle) * 8
  );
  mctx.stroke();
}

// ============ START ============
document.getElementById('startScreen').classList.remove('hidden');

function startGame() {
  document.getElementById('startScreen').classList.add('hidden');
  showDropPhase();
}
</script>
</body>
</html>
