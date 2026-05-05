<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <meta name="theme-color" content="#0b0f14" />
  <title>Shadow Fight Inspired 2D Game</title>
  <style>
    :root {
      --bg: #0b0f14;
      --panel: rgba(18, 24, 33, 0.78);
      --panel-2: rgba(255, 255, 255, 0.06);
      --text: #e9eef5;
      --muted: #9aa7b7;
      --accent: #5ad1ff;
      --accent-2: #7cff9b;
      --danger: #ff6b6b;
      --shadow: 0 12px 40px rgba(0, 0, 0, 0.35);
      --radius: 18px;
    }

    * { box-sizing: border-box; }
    html, body {
      margin: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
      background:
        radial-gradient(circle at 50% 20%, rgba(90, 209, 255, 0.08), transparent 28%),
        linear-gradient(180deg, #0b0f14 0%, #101723 100%);
      color: var(--text);
      font-family: Arial, Helvetica, sans-serif;
      -webkit-tap-highlight-color: transparent;
      touch-action: none;
      user-select: none;
    }

    #game {
      position: relative;
      width: 100vw;
      height: 100vh;
      overflow: hidden;
    }

    #scene {
      position: absolute;
      inset: 0;
      overflow: hidden;
    }

    .sky-glow {
      position: absolute;
      inset: -10% -10% auto -10%;
      height: 40%;
      background: radial-gradient(circle at 50% 70%, rgba(90,209,255,0.12), transparent 55%);
      pointer-events: none;
    }

    .floor {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 23%;
      background:
        linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01)),
        linear-gradient(180deg, #171d26 0%, #11161d 100%);
      border-top: 1px solid rgba(255,255,255,0.06);
    }

    .floor::before {
      content: "";
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      height: 2px;
      background: linear-gradient(90deg, transparent, rgba(124,255,155,0.35), transparent);
      opacity: 0.45;
    }

    .grid {
      position: absolute;
      inset: 0;
      background-image:
        linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
      background-size: 48px 48px;
      mask-image: linear-gradient(180deg, rgba(0,0,0,0.5), transparent 65%);
      opacity: 0.18;
      pointer-events: none;
    }

    #player {
      position: absolute;
      left: 50%;
      bottom: 23%;
      width: 140px;
      height: 170px;
      transform: translateX(-50%);
      transform-origin: center bottom;
      will-change: transform, left;
      pointer-events: none;
      image-rendering: auto;
      filter: drop-shadow(0 12px 18px rgba(0,0,0,0.45));
    }

    #player img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      display: block;
      transition: opacity 80ms linear;
      user-select: none;
      -webkit-user-drag: none;
    }

    .hud {
      position: absolute;
      top: 14px;
      left: 14px;
      right: 14px;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 12px;
      pointer-events: none;
      z-index: 20;
    }

    .card {
      background: var(--panel);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
    }

    .titleCard {
      padding: 12px 14px;
      min-width: 180px;
    }

    .titleCard h1 {
      margin: 0;
      font-size: 16px;
      line-height: 1.15;
      letter-spacing: 0.3px;
    }

    .titleCard p {
      margin: 4px 0 0;
      color: var(--muted);
      font-size: 12px;
    }

    .statusCard {
      padding: 10px 12px;
      min-width: 190px;
      text-align: right;
    }

    .statusCard .small {
      display: block;
      color: var(--muted);
      font-size: 11px;
      margin-bottom: 2px;
    }

    .statusCard .big {
      font-size: 14px;
      font-weight: 700;
    }

    .controls {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      display: grid;
      grid-template-columns: 1fr auto 1fr;
      gap: 12px;
      padding: 16px;
      z-index: 30;
      pointer-events: none;
    }

    .pad {
      pointer-events: auto;
      display: flex;
      gap: 12px;
      align-items: flex-end;
    }

    .pad.leftPad { justify-content: flex-start; }
    .pad.rightPad { justify-content: flex-end; }

    button.ctrl {
      appearance: none;
      border: 1px solid rgba(255,255,255,0.1);
      background: linear-gradient(180deg, rgba(255,255,255,0.09), rgba(255,255,255,0.04));
      color: var(--text);
      border-radius: 18px;
      min-width: 78px;
      height: 74px;
      padding: 12px 14px;
      font-size: 16px;
      font-weight: 700;
      letter-spacing: 0.3px;
      box-shadow: var(--shadow);
      touch-action: none;
      user-select: none;
      -webkit-user-select: none;
      transition: transform 90ms ease, background 90ms ease, border-color 90ms ease;
    }

    button.ctrl:active, button.ctrl.active {
      transform: translateY(2px) scale(0.98);
      border-color: rgba(90,209,255,0.35);
      background: linear-gradient(180deg, rgba(90,209,255,0.18), rgba(255,255,255,0.06));
    }

    button.ctrl.punch {
      min-width: 104px;
      background: linear-gradient(180deg, rgba(255,107,107,0.22), rgba(255,255,255,0.05));
    }

    button.ctrl.punch:active, button.ctrl.punch.active {
      border-color: rgba(255,107,107,0.42);
      background: linear-gradient(180deg, rgba(255,107,107,0.34), rgba(255,255,255,0.07));
    }

    .hint {
      position: absolute;
      left: 50%;
      top: 64px;
      transform: translateX(-50%);
      color: rgba(233,238,245,0.75);
      font-size: 12px;
      background: rgba(18,24,33,0.5);
      border: 1px solid rgba(255,255,255,0.08);
      border-radius: 999px;
      padding: 7px 12px;
      pointer-events: none;
      z-index: 20;
    }

    @media (max-width: 520px) {
      #player {
        width: 120px;
        height: 150px;
      }

      .titleCard, .statusCard {
        min-width: unset;
      }

      .statusCard {
        max-width: 48vw;
      }

      button.ctrl {
        min-width: 72px;
        height: 70px;
      }

      button.ctrl.punch {
        min-width: 96px;
      }
    }
  </style>
</head>
<body>
  <div id="game">
    <div id="scene">
      <div class="sky-glow"></div>
      <div class="grid"></div>
      <div class="floor"></div>
      <div class="hint">Move with Left / Right. Tap Punch to test the attack animation.</div>

      <div id="player" aria-label="player sprite">
        <img id="playerSprite" alt="player character" draggable="false" />
      </div>
    </div>

    <div class="hud">
      <div class="card titleCard">
        <h1>Shadow Fight Inspired Demo</h1>
        <p>Single-file browser game</p>
      </div>
      <div class="card statusCard">
        <span class="small">State</span>
        <span class="big" id="stateText">Idle</span>
      </div>
    </div>

    <div class="controls">
      <div class="pad leftPad">
        <button class="ctrl" id="btnLeft">Left</button>
        <button class="ctrl" id="btnRight">Right</button>
      </div>
      <div></div>
      <div class="pad rightPad">
        <button class="ctrl punch" id="btnPunch">Punch</button>
      </div>
    </div>
  </div>

  <script>
    (() => {
      const ASSET = {
        idle: "Frames/Control/Stand.png",
        walk1: "Frames/Control/Walk1.png",
        walk2: "Frames/Control/Walk2.png",
        punch: "Frames/Control/Punch.png",
      };

      const player = document.getElementById("player");
      const sprite = document.getElementById("playerSprite");
      const stateText = document.getElementById("stateText");
      const btnLeft = document.getElementById("btnLeft");
      const btnRight = document.getElementById("btnRight");
      const btnPunch = document.getElementById("btnPunch");

      const keys = {
        left: false,
        right: false,
        punchLocked: false,
      };

      const playerState = {
        x: window.innerWidth * 0.5,
        facing: 1, // 1 = right, -1 = left
        mode: "idle",
        walkFrame: 0,
        lastWalkSwitch: 0,
        punchUntil: 0,
        speed: 220,
      };

      const images = {};
      for (const [name, src] of Object.entries(ASSET)) {
        const img = new Image();
        img.src = src;
        images[name] = img;
      }

      function setSprite(src) {
        if (sprite.src !== new URL(src, location.href).href) {
          sprite.src = src;
        }
      }

      function getMode() {
        if (performance.now() < playerState.punchUntil) return "punch";
        if (keys.left || keys.right) return "walk";
        return "idle";
      }

      function updateTransform() {
        const flip = playerState.facing === -1 ? -1 : 1;
        player.style.left = `${playerState.x}px`;
        player.style.transform = `translateX(-50%) scaleX(${flip})`;
      }

      function applySprite(now) {
        const mode = getMode();

        if (mode === "punch") {
          setSprite(ASSET.punch);
          stateText.textContent = "Punch";
          return;
        }

        if (mode === "walk") {
          if (now - playerState.lastWalkSwitch >= 400) {
            playerState.walkFrame = playerState.walkFrame === 0 ? 1 : 0;
            playerState.lastWalkSwitch = now;
          }
          setSprite(playerState.walkFrame === 0 ? ASSET.walk1 : ASSET.walk2);
          stateText.textContent = "Walking";
          return;
        }

        setSprite(ASSET.idle);
        stateText.textContent = "Idle";
      }

      function clamp(value, min, max) {
        return Math.max(min, Math.min(max, value));
      }

      function punch() {
        if (keys.punchLocked) return;
        keys.punchLocked = true;
        playerState.punchUntil = performance.now() + 300;
        stateText.textContent = "Punch";
        window.setTimeout(() => {
          keys.punchLocked = false;
        }, 300);
      }

      function bindHoldButton(button, onDown, onUp) {
        const start = (e) => {
          e.preventDefault();
          button.classList.add("active");
          onDown();
        };
        const end = (e) => {
          e.preventDefault();
          button.classList.remove("active");
          onUp?.();
        };

        button.addEventListener("pointerdown", start);
        button.addEventListener("pointerup", end);
        button.addEventListener("pointercancel", end);
        button.addEventListener("pointerleave", (e) => {
          if (e.buttons === 0) button.classList.remove("active");
        });
      }

      bindHoldButton(btnLeft, () => { keys.left = true; }, () => { keys.left = false; });
      bindHoldButton(btnRight, () => { keys.right = true; }, () => { keys.right = false; });
      bindHoldButton(btnPunch, () => { punch(); }, () => {});

      window.addEventListener("keydown", (e) => {
        if (e.repeat) return;
        if (e.key === "ArrowLeft" || e.key.toLowerCase() === "a") keys.left = true;
        if (e.key === "ArrowRight" || e.key.toLowerCase() === "d") keys.right = true;
        if (e.key === " " || e.key.toLowerCase() === "j") punch();
      });

      window.addEventListener("keyup", (e) => {
        if (e.key === "ArrowLeft" || e.key.toLowerCase() === "a") keys.left = false;
        if (e.key === "ArrowRight" || e.key.toLowerCase() === "d") keys.right = false;
      });

      window.addEventListener("blur", () => {
        keys.left = false;
        keys.right = false;
      });

      function resizeClamp() {
        const margin = 70;
        const minX = margin;
        const maxX = window.innerWidth - margin;
        playerState.x = clamp(playerState.x, minX, maxX);
      }

      window.addEventListener("resize", () => {
        resizeClamp();
        updateTransform();
      });

      function loop(now) {
        const dt = Math.min(0.032, (now - (loop.last || now)) / 1000);
        loop.last = now;

        const moveLeft = keys.left && !keys.right;
        const moveRight = keys.right && !keys.left;

        if (performance.now() >= playerState.punchUntil) {
          if (moveLeft) {
            playerState.x -= playerState.speed * dt;
            playerState.facing = -1;
          } else if (moveRight) {
            playerState.x += playerState.speed * dt;
            playerState.facing = 1;
          }
        }

        const margin = 70;
        playerState.x = clamp(playerState.x, margin, window.innerWidth - margin);

        updateTransform();
        applySprite(now);
        requestAnimationFrame(loop);
      }

      // Initial state
      sprite.src = ASSET.idle;
      updateTransform();
      resizeClamp();
      requestAnimationFrame(loop);
    })();
  </script>
</body>
</html>
