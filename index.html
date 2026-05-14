<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta
    name="viewport"
    content="width=device-width, initial-scale=1.0, viewport-fit=cover"
  />
  <title>White Neumorphic Spiral Visualizer</title>

  <style>
    :root {
      --bg: #f5f7fb;
      --bg-2: #eef2f8;
      --surface: #f8faff;
      --surface-2: #f2f5fb;
      --ink: #243046;
      --muted: #6e7890;
      --accent: #7cd7ff;
      --accent-2: #b6a2ff;
      --accent-3: #89b8ff;
      --line: rgba(36, 48, 70, 0.08);
      --success: #1aa26b;
      --danger: #cf547d;

      --radius-xl: 30px;
      --radius-lg: 22px;
      --radius-md: 18px;
      --transition: 700ms cubic-bezier(.2, .8, .2, 1);

      --shadow-raised:
        18px 18px 40px rgba(190, 198, 212, 0.72),
        -18px -18px 40px rgba(255, 255, 255, 0.98);
      --shadow-soft:
        10px 10px 24px rgba(194, 202, 216, 0.62),
        -10px -10px 24px rgba(255, 255, 255, 0.96);
      --shadow-inset:
        inset 8px 8px 16px rgba(210, 217, 229, 0.7),
        inset -8px -8px 16px rgba(255, 255, 255, 0.95);

      --visual-size: 140vmax;
    }

    * {
      box-sizing: border-box;
    }

    html,
    body {
      margin: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      background: var(--bg);
      color: var(--ink);
    }

    body {
      position: relative;
      -webkit-tap-highlight-color: transparent;
    }

    .screen {
      position: absolute;
      inset: 0;
      opacity: 0;
      pointer-events: none;
      transform: scale(1.02);
      filter: blur(10px);
      transition:
        opacity var(--transition),
        transform var(--transition),
        filter var(--transition);
    }

    .screen.active {
      opacity: 1;
      pointer-events: auto;
      transform: scale(1);
      filter: blur(0);
    }

    /* -----------------------------
       Setup screen
    ----------------------------- */
    #setupScreen {
      display: grid;
      place-items: center;
      padding: clamp(14px, 3vw, 32px);
      background:
        radial-gradient(circle at 16% 18%, rgba(124, 215, 255, 0.35), transparent 24%),
        radial-gradient(circle at 82% 20%, rgba(182, 162, 255, 0.24), transparent 26%),
        radial-gradient(circle at 52% 88%, rgba(137, 184, 255, 0.24), transparent 28%),
        linear-gradient(145deg, #fbfcff 0%, #f2f5fb 48%, #edf1f8 100%);
    }

    .panel {
      width: min(1120px, 100%);
      max-height: min(94vh, 980px);
      overflow: auto;
      padding: clamp(18px, 2.5vw, 30px);
      border-radius: var(--radius-xl);
      background: linear-gradient(145deg, #f9fbff, #eff3f9);
      box-shadow: var(--shadow-raised);
      border: 1px solid rgba(255,255,255,0.8);
    }

    .hero {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 16px;
      flex-wrap: wrap;
      margin-bottom: 20px;
    }

    .hero h1 {
      margin: 0 0 10px;
      font-size: clamp(28px, 5vw, 52px);
      line-height: 0.97;
      letter-spacing: -0.04em;
      font-weight: 850;
      color: #1f2a3e;
    }

    .hero p {
      margin: 0;
      max-width: 760px;
      font-size: clamp(14px, 1.8vw, 16px);
      line-height: 1.55;
      color: var(--muted);
    }

    .heroTag {
      padding: 10px 14px;
      border-radius: 999px;
      background: linear-gradient(145deg, #f7faff, #edf2f8);
      box-shadow: var(--shadow-soft);
      color: #45526c;
      font-size: 12px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      white-space: nowrap;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 18px;
    }

    .card {
      padding: 18px;
      border-radius: var(--radius-lg);
      background: linear-gradient(145deg, #f8fbff, #eef2f8);
      box-shadow: var(--shadow-soft);
      border: 1px solid rgba(255,255,255,0.85);
    }

    .card h2 {
      margin: 0 0 14px;
      font-size: 15px;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: #3d4a65;
      font-weight: 800;
    }

    .uploadBox,
    .controls {
      display: grid;
      gap: 14px;
    }

    .fileWrap {
      display: grid;
      gap: 10px;
      position: relative;
    }

    .fileButton {
      position: relative;
      min-height: 112px;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 16px;
      border-radius: var(--radius-md);
      text-align: center;
      cursor: pointer;
      background: linear-gradient(145deg, #f9fbff, #eef2f8);
      box-shadow: var(--shadow-inset);
      border: 1px solid rgba(255,255,255,0.8);
      transition: transform 220ms ease, box-shadow 220ms ease;
    }

    .fileButton:hover {
      transform: translateY(-1px);
      box-shadow:
        inset 6px 6px 12px rgba(210, 217, 229, 0.62),
        inset -6px -6px 12px rgba(255, 255, 255, 0.95),
        0 8px 20px rgba(124, 215, 255, 0.12);
    }

    .fileButton input {
      position: absolute;
      inset: 0;
      opacity: 0;
      cursor: pointer;
    }

    .fileMeta {
      min-height: 18px;
      display: flex;
      justify-content: space-between;
      gap: 12px;
      font-size: 12px;
      color: var(--muted);
    }

    .ok {
      color: var(--success);
      font-weight: 700;
    }

    .row {
      display: grid;
      gap: 8px;
    }

    .row.inline2 {
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 12px;
    }

    .labelLine {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
      font-size: 13px;
      color: #3a4761;
    }

    .value {
      color: #3f8eff;
      font-variant-numeric: tabular-nums;
      font-weight: 700;
    }

    input[type="range"] {
      width: 100%;
      appearance: none;
      height: 12px;
      border-radius: 999px;
      background: linear-gradient(145deg, #eef3f8, #fbfdff);
      box-shadow: var(--shadow-inset);
      outline: none;
    }

    input[type="range"]::-webkit-slider-thumb {
      appearance: none;
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background: linear-gradient(145deg, #ffffff, #e8eef8);
      box-shadow:
        6px 6px 14px rgba(193, 201, 214, 0.72),
        -6px -6px 14px rgba(255,255,255,0.98);
      border: 1px solid rgba(255,255,255,0.92);
      cursor: pointer;
    }

    input[type="range"]::-moz-range-thumb {
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background: linear-gradient(145deg, #ffffff, #e8eef8);
      box-shadow:
        6px 6px 14px rgba(193, 201, 214, 0.72),
        -6px -6px 14px rgba(255,255,255,0.98);
      border: 1px solid rgba(255,255,255,0.92);
      cursor: pointer;
    }

    input[type="color"] {
      width: 100%;
      min-height: 52px;
      border-radius: 16px;
      border: 1px solid rgba(255,255,255,0.9);
      background: linear-gradient(145deg, #f9fbff, #edf2f8);
      box-shadow: var(--shadow-soft);
      cursor: pointer;
    }

    .toggle {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 14px;
      padding: 12px 14px;
      border-radius: 18px;
      background: linear-gradient(145deg, #f9fbff, #edf2f8);
      box-shadow: var(--shadow-soft);
      border: 1px solid rgba(255,255,255,0.84);
    }

    .switch {
      position: relative;
      width: 58px;
      height: 32px;
      flex: 0 0 auto;
    }

    .switch input {
      position: absolute;
      inset: 0;
      opacity: 0;
      cursor: pointer;
    }

    .switch span {
      position: absolute;
      inset: 0;
      border-radius: 999px;
      background: linear-gradient(145deg, #eef3f8, #fbfdff);
      box-shadow: var(--shadow-inset);
      transition: 240ms ease;
    }

    .switch span::after {
      content: "";
      position: absolute;
      top: 4px;
      left: 4px;
      width: 24px;
      height: 24px;
      border-radius: 50%;
      background: linear-gradient(145deg, #ffffff, #e8eef8);
      box-shadow:
        6px 6px 12px rgba(193, 201, 214, 0.6),
        -6px -6px 12px rgba(255,255,255,0.98);
      transition: transform 240ms ease;
    }

    .switch input:checked + span::after {
      transform: translateX(26px);
    }

    .status {
      min-height: 20px;
      margin-top: 12px;
      text-align: center;
      color: var(--danger);
      font-size: 13px;
    }

    .footer {
      display: flex;
      justify-content: center;
      padding-top: 18px;
    }

    .submitBtn {
      min-width: min(320px, 100%);
      padding: 17px 26px;
      border: 0;
      border-radius: 999px;
      cursor: pointer;
      font-weight: 900;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: #2d3950;
      background: linear-gradient(145deg, #f9fbff, #e9eef7);
      box-shadow:
        14px 14px 28px rgba(193, 201, 214, 0.64),
        -14px -14px 28px rgba(255,255,255,0.98);
      transition: transform 220ms ease, box-shadow 220ms ease;
    }

    .submitBtn:hover {
      transform: translateY(-2px);
      box-shadow:
        18px 18px 36px rgba(193, 201, 214, 0.66),
        -18px -18px 36px rgba(255,255,255,0.98),
        0 8px 20px rgba(124, 215, 255, 0.14);
    }

    .submitBtn:active {
      transform: translateY(0);
    }

    /* -----------------------------
       Visualizer screen
    ----------------------------- */
    #visualizerScreen {
      overflow: hidden;
      background: linear-gradient(145deg, #f9fbff, #edf2f8);
    }

    .visualBg {
      position: absolute;
      inset: -10%;
      background:
        radial-gradient(circle at 18% 18%, rgba(124, 215, 255, 0.30), transparent 24%),
        radial-gradient(circle at 80% 24%, rgba(182, 162, 255, 0.22), transparent 28%),
        radial-gradient(circle at 50% 82%, rgba(137, 184, 255, 0.26), transparent 28%),
        linear-gradient(145deg, #fbfcff, #eef2f8 50%, #f7f9fd 100%);
      transition: background 1000ms ease;
      filter: saturate(110%);
      transform: scale(1.08);
    }

    .visualOverlay {
      position: absolute;
      inset: 0;
      pointer-events: none;
      background:
        radial-gradient(circle at 50% 50%, rgba(255,255,255,0.55), transparent 26%),
        radial-gradient(circle at 50% 50%, rgba(124, 215, 255, 0.10), transparent 40%);
      mix-blend-mode: screen;
    }

    #particleCanvas {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      opacity: 0.9;
    }

    #scene {
      position: absolute;
      left: 50%;
      top: 50%;
      width: 0;
      height: 0;
      z-index: 2;
    }

    .sprite {
      position: absolute;
      width: var(--visual-size);
      height: var(--visual-size);
      will-change: transform;
      transform-style: preserve-3d;
    }

    .sprite img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      user-select: none;
      -webkit-user-drag: none;
      transform-origin: 50% 50%;
      will-change: transform, opacity, filter;
      filter:
        drop-shadow(0 0 18px rgba(124, 215, 255, 0.10))
        drop-shadow(0 0 30px rgba(182, 162, 255, 0.10));
    }

    .fullscreenBtn {
      position: absolute;
      top: max(8px, env(safe-area-inset-top));
      right: max(8px, env(safe-area-inset-right));
      z-index: 5;
      width: 24px;
      height: 24px;
      display: grid;
      place-items: center;
      border: 0;
      background: transparent;
      color: rgba(36, 48, 70, 0.30);
      opacity: 0.18;
      padding: 0;
      cursor: pointer;
      font-size: 13px;
      line-height: 1;
      transition: opacity 220ms ease, transform 220ms ease, color 220ms ease;
    }

    .fullscreenBtn:hover,
    .fullscreenBtn:focus-visible {
      opacity: 0.58;
      color: rgba(36, 48, 70, 0.72);
      transform: scale(1.08);
      outline: none;
    }

    .hint {
      position: absolute;
      left: 50%;
      bottom: max(12px, env(safe-area-inset-bottom));
      transform: translateX(-50%);
      z-index: 4;
      padding: 8px 12px;
      border-radius: 999px;
      background: rgba(255,255,255,0.56);
      color: rgba(62, 74, 96, 0.58);
      box-shadow: var(--shadow-soft);
      font-size: 11px;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      opacity: 0;
      transition: opacity 600ms ease;
      pointer-events: none;
    }

    #visualizerScreen.active .hint {
      opacity: 1;
    }

    @media (max-width: 860px) {
      .grid {
        grid-template-columns: 1fr;
      }

      .panel {
        padding: 16px;
      }

      .hero h1 {
        font-size: clamp(26px, 9vw, 40px);
      }

      .submitBtn {
        min-width: 100%;
      }
    }
  </style>
</head>
<body>
  <!-- Screen 1 -->
  <section id="setupScreen" class="screen active">
    <div class="panel">
      <div class="hero">
        <div>
          <h1>Spiral Visualizer</h1>
          <p>
            Upload up to two transparent PNGs, tune their opposing motion, choose a soft animated background,
            and launch a centered fullscreen spiral scene with a bright white neumorphic interface.
          </p>
        </div>
        <div class="heroTag">White Neumorphic UI</div>
      </div>

      <div class="grid">
        <div class="card">
          <h2>Images</h2>
          <div class="uploadBox">
            <div class="fileWrap">
              <label class="fileButton">
                <div>
                  <div style="font-weight:800; margin-bottom:6px;">Upload PNG — Image A</div>
                  <div style="font-size:13px; color:var(--muted);">Clockwise layer</div>
                </div>
                <input id="file1" type="file" accept="image/png" />
              </label>
              <div class="fileMeta">
                <span id="file1Name">Leave blank if not needed</span>
                <span id="file1State"></span>
              </div>
            </div>

            <div class="fileWrap">
              <label class="fileButton">
                <div>
                  <div style="font-weight:800; margin-bottom:6px;">Upload PNG — Image B</div>
                  <div style="font-size:13px; color:var(--muted);">Counterclockwise layer</div>
                </div>
                <input id="file2" type="file" accept="image/png" />
              </label>
              <div class="fileMeta">
                <span id="file2Name">Leave blank if not needed</span>
                <span id="file2State"></span>
              </div>
            </div>
          </div>
        </div>

        <div class="card">
          <h2>Rotation</h2>
          <div class="controls">
            <div class="row">
              <div class="labelLine">
                <span>Image A speed</span>
                <span class="value" id="speed1Val">40°/s</span>
              </div>
              <input id="speed1" type="range" min="0" max="240" value="40" />
            </div>

            <div class="row">
              <div class="labelLine">
                <span>Image B speed</span>
                <span class="value" id="speed2Val">52°/s</span>
              </div>
              <input id="speed2" type="range" min="0" max="240" value="52" />
            </div>

            <div class="row">
              <div class="labelLine">
                <span>Rotation scale</span>
                <span class="value" id="rotationScaleVal">1.00×</span>
              </div>
              <input id="rotationScale" type="range" min="40" max="220" value="100" />
            </div>
          </div>
        </div>

        <div class="card">
          <h2>Background</h2>
          <div class="controls">
            <div class="row inline2">
              <div class="row">
                <div class="labelLine">
                  <span>Base color</span>
                </div>
                <input id="baseColor" type="color" value="#f7faff" />
              </div>

              <div class="row">
                <div class="labelLine">
                  <span>Accent color</span>
                </div>
                <input id="accentColor" type="color" value="#c2d4ff" />
              </div>
            </div>

            <div class="toggle">
              <div>
                <div style="font-weight:800; color:#3d4a65;">Animated gradient</div>
                <div style="font-size:13px; color:var(--muted);">Smooth color shifting background</div>
              </div>
              <label class="switch">
                <input id="gradientToggle" type="checkbox" checked />
                <span></span>
              </label>
            </div>
          </div>
        </div>

        <div class="card">
          <h2>Visual tuning</h2>
          <div class="controls">
            <div class="row">
              <div class="labelLine">
                <span>Spiral intensity</span>
                <span class="value" id="spiralIntensityVal">38</span>
              </div>
              <input id="spiralIntensity" type="range" min="0" max="100" value="38" />
            </div>

            <div class="row">
              <div class="labelLine">
                <span>Opacity</span>
                <span class="value" id="opacityVal">0.88</span>
              </div>
              <input id="opacity" type="range" min="10" max="100" value="88" />
            </div>

            <div class="row">
              <div class="labelLine">
                <span>Zoom level</span>
                <span class="value" id="zoomVal">1.00×</span>
              </div>
              <input id="zoom" type="range" min="50" max="220" value="100" />
            </div>
          </div>
        </div>
      </div>

      <div class="status" id="status"></div>

      <div class="footer">
        <button id="submitBtn" class="submitBtn">Submit</button>
      </div>
    </div>
  </section>

  <!-- Screen 2 -->
  <section id="visualizerScreen" class="screen" aria-hidden="true">
    <div class="visualBg" id="visualBg"></div>
    <div class="visualOverlay"></div>
    <canvas id="particleCanvas"></canvas>

    <div id="scene">
      <div id="sprite1" class="sprite">
        <img id="visual1" alt="Visual layer A" />
      </div>
      <div id="sprite2" class="sprite">
        <img id="visual2" alt="Visual layer B" />
      </div>
    </div>

    <button id="fullscreenBtn" class="fullscreenBtn" title="Toggle fullscreen" aria-label="Toggle fullscreen">
      ⤢
    </button>

    <div class="hint">Tap the tiny corner icon for fullscreen</div>
  </section>

  <script>
    // -----------------------------
    // Element references
    // -----------------------------
    const setupScreen = document.getElementById('setupScreen');
    const visualizerScreen = document.getElementById('visualizerScreen');
    const submitBtn = document.getElementById('submitBtn');
    const fullscreenBtn = document.getElementById('fullscreenBtn');
    const statusEl = document.getElementById('status');

    const file1 = document.getElementById('file1');
    const file2 = document.getElementById('file2');
    const file1Name = document.getElementById('file1Name');
    const file2Name = document.getElementById('file2Name');
    const file1State = document.getElementById('file1State');
    const file2State = document.getElementById('file2State');

    const speed1 = document.getElementById('speed1');
    const speed2 = document.getElementById('speed2');
    const rotationScale = document.getElementById('rotationScale');
    const baseColor = document.getElementById('baseColor');
    const accentColor = document.getElementById('accentColor');
    const gradientToggle = document.getElementById('gradientToggle');
    const spiralIntensity = document.getElementById('spiralIntensity');
    const opacitySlider = document.getElementById('opacity');
    const zoom = document.getElementById('zoom');

    const speed1Val = document.getElementById('speed1Val');
    const speed2Val = document.getElementById('speed2Val');
    const rotationScaleVal = document.getElementById('rotationScaleVal');
    const spiralIntensityVal = document.getElementById('spiralIntensityVal');
    const opacityVal = document.getElementById('opacityVal');
    const zoomVal = document.getElementById('zoomVal');

    const sprite1 = document.getElementById('sprite1');
    const sprite2 = document.getElementById('sprite2');
    const visual1 = document.getElementById('visual1');
    const visual2 = document.getElementById('visual2');
    const visualBg = document.getElementById('visualBg');

    const canvas = document.getElementById('particleCanvas');
    const ctx = canvas.getContext('2d');

    // -----------------------------
    // State
    // -----------------------------
    const state = {
      urls: [null, null],
      ready: [false, false],
      started: false,
      lastTime: 0,
      rotA: 0,
      rotB: 0,
      particles: [],
      dpr: Math.min(window.devicePixelRatio || 1, 2)
    };

    // -----------------------------
    // Helpers
    // -----------------------------
    const clamp = (n, min, max) => Math.max(min, Math.min(max, n));

    function hexToRgb(hex) {
      const clean = hex.replace('#', '');
      const full = clean.length === 3
        ? clean.split('').map(c => c + c).join('')
        : clean;

      const value = parseInt(full, 16);
      return {
        r: (value >> 16) & 255,
        g: (value >> 8) & 255,
        b: value & 255
      };
    }

    function rgbToHex({ r, g, b }) {
      const h = v => Math.round(v).toString(16).padStart(2, '0');
      return `#${h(clamp(r, 0, 255))}${h(clamp(g, 0, 255))}${h(clamp(b, 0, 255))}`;
    }

    function mixHex(a, b, t) {
      const ca = hexToRgb(a);
      const cb = hexToRgb(b);
      return rgbToHex({
        r: ca.r + (cb.r - ca.r) * t,
        g: ca.g + (cb.g - ca.g) * t,
        b: ca.b + (cb.b - ca.b) * t
      });
    }

    function setStatus(message = '', tone = '') {
      statusEl.textContent = message;
      statusEl.style.color =
        tone === 'error' ? 'var(--danger)' :
        tone === 'ok' ? 'var(--success)' :
        'var(--muted)';
    }

    function updateLabels() {
      speed1Val.textContent = `${speed1.value}°/s`;
      speed2Val.textContent = `${speed2.value}°/s`;
      rotationScaleVal.textContent = `${(rotationScale.value / 100).toFixed(2)}×`;
      spiralIntensityVal.textContent = spiralIntensity.value;
      opacityVal.textContent = (opacitySlider.value / 100).toFixed(2);
      zoomVal.textContent = `${(zoom.value / 100).toFixed(2)}×`;
    }

    function syncLayerVisibility() {
      sprite1.style.display = state.urls[0] ? 'block' : 'none';
      sprite2.style.display = state.urls[1] ? 'block' : 'none';
    }

    function updateVisualSize() {
      const maxSide = Math.max(window.innerWidth, window.innerHeight);
      const size = Math.max(maxSide * 1.35, 900);
      document.documentElement.style.setProperty('--visual-size', `${size}px`);
    }

    function clearLayer(index) {
      const target = index === 0 ? visual1 : visual2;
      const nameEl = index === 0 ? file1Name : file2Name;
      const stateEl = index === 0 ? file1State : file2State;

      if (state.urls[index]) {
        URL.revokeObjectURL(state.urls[index]);
      }

      state.urls[index] = null;
      state.ready[index] = false;
      target.removeAttribute('src');
      nameEl.textContent = 'Leave blank if not needed';
      stateEl.textContent = '';
      stateEl.className = '';
      syncLayerVisibility();
    }

    function setVisualImage(index, file) {
      const target = index === 0 ? visual1 : visual2;
      const nameEl = index === 0 ? file1Name : file2Name;
      const stateEl = index === 0 ? file1State : file2State;

      if (state.urls[index]) {
        URL.revokeObjectURL(state.urls[index]);
      }

      const url = URL.createObjectURL(file);
      state.urls[index] = url;
      state.ready[index] = false;

      target.onload = () => {
        state.ready[index] = true;
        nameEl.textContent = file.name;
        stateEl.textContent = 'Ready';
        stateEl.className = 'ok';
      };

      target.src = url;
      syncLayerVisibility();
    }

    function handleFile(file, index) {
      if (!file) {
        clearLayer(index);
        return;
      }

      if (file.type !== 'image/png') {
        setStatus('Please upload PNG files only.', 'error');
        return;
      }

      setStatus('');
      setVisualImage(index, file);
    }

    // -----------------------------
    // Particles
    // -----------------------------
    function resizeCanvas() {
      const w = window.innerWidth;
      const h = window.innerHeight;

      canvas.width = Math.floor(w * state.dpr);
      canvas.height = Math.floor(h * state.dpr);
      canvas.style.width = `${w}px`;
      canvas.style.height = `${h}px`;

      ctx.setTransform(state.dpr, 0, 0, state.dpr, 0, 0);
      initParticles();
    }

    function initParticles() {
      const count = Math.max(20, Math.floor((window.innerWidth * window.innerHeight) / 62000));
      state.particles = Array.from({ length: count }, () => ({
        x: Math.random() * window.innerWidth,
        y: Math.random() * window.innerHeight,
        r: 1 + Math.random() * 2.2,
        vx: -0.08 + Math.random() * 0.16,
        vy: -0.08 + Math.random() * 0.16,
        a: 0.04 + Math.random() * 0.09,
        phase: Math.random() * Math.PI * 2
      }));
    }

    function drawParticles(t) {
      ctx.clearRect(0, 0, window.innerWidth, window.innerHeight);

      for (const p of state.particles) {
        p.x += p.vx;
        p.y += p.vy;

        if (p.x < -40) p.x = window.innerWidth + 40;
        if (p.x > window.innerWidth + 40) p.x = -40;
        if (p.y < -40) p.y = window.innerHeight + 40;
        if (p.y > window.innerHeight + 40) p.y = -40;

        const alpha = p.a * (0.55 + 0.45 * Math.sin(t * 0.001 + p.phase));
        const grad = ctx.createRadialGradient(p.x, p.y, 0, p.x, p.y, p.r * 18);

        grad.addColorStop(0, `rgba(255,255,255,${alpha})`);
        grad.addColorStop(0.32, `rgba(124,215,255,${alpha * 0.8})`);
        grad.addColorStop(0.7, `rgba(182,162,255,${alpha * 0.35})`);
        grad.addColorStop(1, `rgba(0,0,0,0)`);

        ctx.fillStyle = grad;
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.r * 18, 0, Math.PI * 2);
        ctx.fill();
      }
    }

    // -----------------------------
    // Background animation
    // -----------------------------
    function updateBackground(t) {
      const base = baseColor.value;
      const accent = accentColor.value;
      const pulse = 0.5 + 0.5 * Math.sin(t * 0.00024);
      const pulse2 = 0.5 + 0.5 * Math.sin(t * 0.00033 + 1.4);

      const b1 = mixHex(base, accent, 0.14 + pulse * 0.18);
      const b2 = mixHex(accent, '#ffffff', 0.45 + pulse2 * 0.18);
      const b3 = mixHex(base, '#dfe9ff', 0.28);

      if (gradientToggle.checked) {
        visualBg.style.background = `
          radial-gradient(circle at ${18 + pulse * 16}% ${18 + pulse2 * 10}%, ${mixHex(b1, '#7cd7ff', 0.28)}, transparent 24%),
          radial-gradient(circle at ${80 - pulse2 * 14}% ${24 + pulse * 10}%, ${mixHex(b2, '#b6a2ff', 0.26)}, transparent 28%),
          radial-gradient(circle at ${50 + pulse * 6}% ${82 - pulse2 * 10}%, ${mixHex(b3, '#89b8ff', 0.22)}, transparent 30%),
          linear-gradient(${140 + pulse * 30}deg, ${mixHex(base, '#ffffff', 0.5)}, ${mixHex(base, '#eef2f8', 0.45)} 40%, ${mixHex(accent, '#f8fbff', 0.5)});
        `;
      } else {
        visualBg.style.background = `
          radial-gradient(circle at 50% 50%, ${mixHex(base, accent, 0.08)}, transparent 30%),
          linear-gradient(145deg, ${mixHex(base, '#ffffff', 0.45)}, ${mixHex(base, '#eef2f8', 0.25)});
        `;
      }
    }

    // -----------------------------
    // Animation
    // -----------------------------
    function animate(now) {
      const dt = state.lastTime ? (now - state.lastTime) / 1000 : 0.016;
      state.lastTime = now;

      if (state.started) {
        const speedA = Number(speed1.value);
        const speedB = Number(speed2.value);
        const rotScale = Number(rotationScale.value) / 100;
        const spiral = Number(spiralIntensity.value) / 100;
        const zoomScale = Number(zoom.value) / 100;
        const opacity = Number(opacitySlider.value) / 100;

        state.rotA += speedA * dt;
        state.rotB -= speedB * dt;

        const minSide = Math.min(window.innerWidth, window.innerHeight);
        const maxSide = Math.max(window.innerWidth, window.innerHeight);

        const orbit = now * 0.00055;
        const breathe = 0.92 + 0.08 * Math.sin(now * 0.00115);
        const ripple = 0.09 * Math.sin(now * 0.0018);

        const motionRadius = minSide * 0.12 * spiral * rotScale;
        const innerA = motionRadius * (0.9 + 0.15 * Math.sin(orbit * 1.3));
        const innerB = motionRadius * (0.9 + 0.15 * Math.cos(orbit * 1.18));

        const ax =
          Math.cos(orbit) * innerA +
          Math.sin(orbit * 2.1) * innerA * 0.18;

        const ay =
          Math.sin(orbit * 1.02) * innerA +
          Math.cos(orbit * 1.7) * innerA * 0.14;

        const bx =
          Math.cos(orbit + Math.PI) * innerB +
          Math.sin(orbit * 1.6 + Math.PI) * innerB * 0.16;

        const by =
          Math.sin(orbit * 1.02 + Math.PI) * innerB +
          Math.cos(orbit * 1.76 + Math.PI) * innerB * 0.14;

        const scaleBase = (maxSide / Math.max(window.innerWidth, window.innerHeight)) * zoomScale * breathe;
        const zA = scaleBase * (1 + ripple * 0.45);
        const zB = scaleBase * (1 - ripple * 0.35);

        if (state.urls[0]) {
          sprite1.style.transform = `translate3d(${ax}px, ${ay}px, 0) translate(-50%, -50%)`;
          visual1.style.transform = `rotate(${state.rotA.toFixed(2)}deg) scale(${zA.toFixed(3)})`;
          visual1.style.opacity = clamp(opacity * (0.92 + 0.06 * Math.sin(orbit * 2.2)), 0.04, 1).toFixed(3);
          visual1.style.filter = `
            drop-shadow(0 0 ${18 + spiral * 22}px rgba(124,215,255,0.12))
            drop-shadow(0 0 ${30 + spiral * 32}px rgba(182,162,255,0.10))
          `;
        }

        if (state.urls[1]) {
          sprite2.style.transform = `translate3d(${bx}px, ${by}px, 0) translate(-50%, -50%)`;
          visual2.style.transform = `rotate(${state.rotB.toFixed(2)}deg) scale(${zB.toFixed(3)})`;
          visual2.style.opacity = clamp(opacity * (0.90 + 0.08 * Math.cos(orbit * 2.05)), 0.04, 1).toFixed(3);
          visual2.style.filter = `
            drop-shadow(0 0 ${18 + spiral * 22}px rgba(182,162,255,0.12))
            drop-shadow(0 0 ${30 + spiral * 32}px rgba(124,215,255,0.10))
          `;
        }
      }

      updateBackground(now);
      drawParticles(now);
      requestAnimationFrame(animate);
    }

    // -----------------------------
    // Screen transition
    // -----------------------------
    function showVisualizer() {
      syncLayerVisibility();
      setupScreen.classList.remove('active');
      visualizerScreen.classList.add('active');
      visualizerScreen.setAttribute('aria-hidden', 'false');
      state.started = true;
      setStatus('');
    }

    submitBtn.addEventListener('click', showVisualizer);

    // -----------------------------
    // Fullscreen
    // -----------------------------
    async function toggleFullscreen() {
      try {
        if (!document.fullscreenElement) {
          await visualizerScreen.requestFullscreen();
        } else {
          await document.exitFullscreen();
        }
      } catch (err) {
        // Browser may block fullscreen in some situations.
      }
    }

    fullscreenBtn.addEventListener('click', toggleFullscreen);

    // -----------------------------
    // Events
    // -----------------------------
    file1.addEventListener('change', (e) => handleFile(e.target.files[0], 0));
    file2.addEventListener('change', (e) => handleFile(e.target.files[0], 1));

    [
      speed1, speed2, rotationScale,
      spiralIntensity, opacitySlider, zoom,
      baseColor, accentColor, gradientToggle
    ].forEach((el) => {
      el.addEventListener('input', updateLabels);
      el.addEventListener('change', updateLabels);
    });

    window.addEventListener('resize', () => {
      state.dpr = Math.min(window.devicePixelRatio || 1, 2);
      updateVisualSize();
      resizeCanvas();
    });

    // -----------------------------
    // Init
    // -----------------------------
    updateLabels();
    updateVisualSize();
    resizeCanvas();
    syncLayerVisibility();
    requestAnimationFrame(animate);
  </script>
</body>
</html>
