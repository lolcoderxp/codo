<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>⛏️ Minecraft 3D Ultra - Mobile Edition</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-touch-callout: none; -webkit-user-select: none; user-select: none; }
        body { overflow: hidden; background: #0a0a12; font-family: 'Segoe UI', sans-serif; touch-action: none; position: fixed; width: 100%; height: 100%; }
        #canvas-container { width: 100vw; height: 100vh; display: block; touch-action: none; }
        
        /* HUD Premium */
        #hud {
            position: absolute; top: 12px; left: 50%; transform: translateX(-50%);
            z-index: 10; display: flex; gap: 12px;
            background: rgba(0,0,0,0.85); padding: 8px 18px; border-radius: 16px;
            backdrop-filter: blur(20px); border: 1px solid rgba(255,255,255,0.08);
            color: white; font-size: 11px; pointer-events: none;
            white-space: nowrap;
            box-shadow: 0 8px 40px rgba(0,0,0,0.6);
        }
        #hud span { opacity: 0.5; font-weight: 300; letter-spacing: 0.5px; }
        #hud .val { opacity: 1; color: #7cb342; font-weight: 700; }
        
        /* Crosshair Premium */
        #crosshair {
            position: absolute; top: 50%; left: 50%;
            transform: translate(-50%, -50%); z-index: 10; pointer-events: none;
        }
        #crosshair::before, #crosshair::after {
            content: ''; position: absolute; 
            background: rgba(255,255,255,0.7);
            border-radius: 2px;
            box-shadow: 0 0 20px rgba(124,179,66,0.2);
        }
        #crosshair::before { width: 20px; height: 2px; top: 50%; left: 50%; transform: translate(-50%, -50%); }
        #crosshair::after { width: 2px; height: 20px; top: 50%; left: 50%; transform: translate(-50%, -50%); }
        #crosshair-dot {
            position: absolute; width: 4px; height: 4px;
            background: rgba(124,179,66,0.8); border-radius: 50%;
            top: 50%; left: 50%; transform: translate(-50%, -50%);
            box-shadow: 0 0 20px rgba(124,179,66,0.4);
        }

        /* Hotbar Premium */
        #hotbar {
            position: absolute; bottom: 110px; left: 50%; transform: translateX(-50%);
            z-index: 10; display: flex; gap: 4px;
            background: rgba(0,0,0,0.9); padding: 6px 10px; border-radius: 16px;
            backdrop-filter: blur(20px); border: 1px solid rgba(255,255,255,0.06);
            box-shadow: 0 8px 40px rgba(0,0,0,0.6);
        }
        .slot {
            width: 48px; height: 48px; border: 2px solid rgba(255,255,255,0.04);
            border-radius: 10px; display: flex; flex-direction: column;
            align-items: center; justify-content: center; color: white;
            font-size: 20px; transition: all 0.2s ease;
            background: rgba(255,255,255,0.03); position: relative;
            touch-action: none;
        }
        .slot.active { 
            border-color: #7cb342; 
            background: rgba(124,179,66,0.15); 
            box-shadow: 0 0 30px rgba(124,179,66,0.15), inset 0 0 30px rgba(124,179,66,0.05);
        }
        .slot .name { font-size: 6px; opacity: 0.4; margin-top: 2px; font-weight: 300; letter-spacing: 0.3px; }
        .slot .count { 
            position: absolute; bottom: -5px; right: -5px; 
            font-size: 9px; background: rgba(0,0,0,0.9); 
            padding: 0 6px; border-radius: 6px; color: #fff;
            border: 1px solid rgba(255,255,255,0.06);
            font-weight: 700;
        }

        /* Mobile Controls - Ultra Premium */
        #mobile-controls {
            position: absolute; bottom: 20px; left: 0; right: 0;
            z-index: 10; display: none; justify-content: space-between;
            padding: 0 14px; pointer-events: none;
        }
        #mobile-controls .left, #mobile-controls .right {
            display: flex; gap: 10px; pointer-events: auto;
            align-items: flex-end;
        }

        .ctrl-btn {
            width: 64px; height: 64px; border-radius: 50%;
            backdrop-filter: blur(12px);
            color: white; font-size: 26px;
            display: flex; align-items: center; justify-content: center;
            touch-action: none; transition: all 0.15s cubic-bezier(0.34, 1.56, 0.64, 1);
            box-shadow: 0 8px 32px rgba(0,0,0,0.5), inset 0 2px 0 rgba(255,255,255,0.15);
            text-shadow: 0 2px 8px rgba(0,0,0,0.4);
            font-weight: bold;
            border: 2px solid rgba(255,255,255,0.06);
        }
        .ctrl-btn:active { transform: scale(0.85); }
        
        .ctrl-btn.jump { 
            background: linear-gradient(145deg, #43A047, #1B5E20);
            border-color: #66BB6A;
            box-shadow: 0 8px 32px rgba(76, 175, 80, 0.4), inset 0 2px 0 rgba(255,255,255,0.2);
            font-size: 30px;
        }
        .ctrl-btn.jump:active { 
            transform: scale(0.85);
            box-shadow: 0 4px 16px rgba(76, 175, 80, 0.3);
        }

        .ctrl-btn.break { 
            background: linear-gradient(145deg, #EF5350, #B71C1C);
            border-color: #EF5350;
            box-shadow: 0 8px 32px rgba(239, 83, 80, 0.4), inset 0 2px 0 rgba(255,255,255,0.2);
            font-size: 24px;
        }
        .ctrl-btn.break:active { 
            transform: scale(0.85);
            box-shadow: 0 4px 16px rgba(239, 83, 80, 0.3);
        }

        .ctrl-btn.place { 
            background: linear-gradient(145deg, #42A5F5, #0D47A1);
            border-color: #42A5F5;
            box-shadow: 0 8px 32px rgba(66, 165, 245, 0.4), inset 0 2px 0 rgba(255,255,255,0.2);
            font-size: 24px;
        }
        .ctrl-btn.place:active { 
            transform: scale(0.85);
            box-shadow: 0 4px 16px rgba(66, 165, 245, 0.3);
        }

        .ctrl-btn.inv { 
            background: linear-gradient(145deg, #FFB300, #E65100);
            border-color: #FFB300;
            box-shadow: 0 8px 32px rgba(255, 179, 0, 0.4), inset 0 2px 0 rgba(255,255,255,0.2);
            font-size: 22px;
        }
        .ctrl-btn.inv:active { 
            transform: scale(0.85);
            box-shadow: 0 4px 16px rgba(255, 179, 0, 0.3);
        }

        .ctrl-btn.small { width: 54px; height: 54px; font-size: 20px; }

        /* Joystick Ultra Premium */
        #joystick-area {
            position: absolute; bottom: 110px; left: 20px;
            z-index: 10; width: 140px; height: 140px;
            border-radius: 50%; 
            background: radial-gradient(circle at 30% 30%, rgba(255,255,255,0.04), rgba(0,0,0,0.4));
            border: 2px solid rgba(255,255,255,0.04);
            backdrop-filter: blur(8px);
            touch-action: none; display: none;
            box-shadow: 0 0 60px rgba(0,0,0,0.4), inset 0 0 60px rgba(255,255,255,0.02);
        }
        #joystick-knob {
            position: absolute; top: 50%; left: 50%;
            transform: translate(-50%, -50%);
            width: 60px; height: 60px; border-radius: 50%;
            background: radial-gradient(circle at 40% 40%, rgba(255,255,255,0.15), rgba(255,255,255,0.03));
            backdrop-filter: blur(12px);
            border: 2px solid rgba(255,255,255,0.08);
            box-shadow: 0 0 40px rgba(0,0,0,0.5);
            touch-action: none;
            transition: none;
        }
        #joystick-knob::after {
            content: '';
            position: absolute;
            top: 50%; left: 50%;
            transform: translate(-50%, -50%);
            width: 14px; height: 14px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(255,255,255,0.3), rgba(255,255,255,0.05));
            border: 1px solid rgba(255,255,255,0.05);
        }

        /* Toast Premium */
        #toast {
            position: fixed; bottom: 190px; left: 50%; transform: translateX(-50%);
            z-index: 50; background: rgba(0,0,0,0.92); backdrop-filter: blur(20px);
            padding: 12px 24px; border-radius: 16px; color: white; font-size: 14px;
            border: 1px solid rgba(124,179,66,0.12); opacity: 0;
            transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
            pointer-events: none; text-align: center;
            max-width: 85%; white-space: nowrap;
            box-shadow: 0 8px 40px rgba(0,0,0,0.6);
            font-weight: 500;
        }
        #toast.show { opacity: 1; transform: translateX(-50%) translateY(-10px); }

        /* Inventory Premium */
        #inventory {
            position: fixed; inset: 0; z-index: 100;
            background: rgba(0,0,0,0.95); backdrop-filter: blur(30px);
            display: none; flex-direction: column;
            padding: 20px; overflow-y: auto;
        }
        #inventory.active { display: flex; }
        #inv-header {
            display: flex; justify-content: space-between; align-items: center;
            color: white; padding: 10px 0; flex-shrink: 0;
        }
        #inv-header h2 { font-size: 20px; font-weight: 700; letter-spacing: 1px; }
        #inv-close {
            background: rgba(255,255,255,0.06); border: none; color: white;
            width: 44px; height: 44px; border-radius: 14px; cursor: pointer;
            font-size: 22px; transition: 0.2s;
            backdrop-filter: blur(8px);
        }
        #inv-close:active { background: rgba(255,0,0,0.2); }
        #inv-grid {
            display: grid; grid-template-columns: repeat(4, 1fr);
            gap: 10px; flex: 1; align-content: start;
            padding-bottom: 20px;
        }
        .inv-slot {
            aspect-ratio: 1; background: rgba(255,255,255,0.03);
            border: 2px solid rgba(255,255,255,0.04); border-radius: 14px;
            display: flex; flex-direction: column; align-items: center;
            justify-content: center; color: white; font-size: 30px;
            transition: all 0.2s; touch-action: none;
            min-height: 65px;
            backdrop-filter: blur(4px);
        }
        .inv-slot:active { background: rgba(255,255,255,0.08); border-color: #7cb342; transform: scale(0.95); }
        .inv-slot .icount { font-size: 11px; opacity: 0.4; margin-top: 3px; font-weight: 300; }

        /* Block Info Premium */
        #block-info {
            position: absolute; bottom: 175px; left: 50%; transform: translateX(-50%);
            z-index: 10; color: rgba(255,255,255,0.5); font-size: 12px;
            background: rgba(0,0,0,0.4); padding: 4px 18px; border-radius: 10px;
            backdrop-filter: blur(8px); pointer-events: none;
            white-space: nowrap;
            font-weight: 400;
            letter-spacing: 0.5px;
            border: 1px solid rgba(255,255,255,0.03);
        }

        /* Loading Premium */
        #loading {
            position: fixed; inset: 0; z-index: 999;
            background: #0a0a12; display: flex; flex-direction: column;
            align-items: center; justify-content: center; color: white;
            transition: opacity 0.8s; padding: 20px;
        }
        #loading.hidden { opacity: 0; pointer-events: none; }
        #loading .icon { font-size: 70px; margin-bottom: 12px; animation: float 3s ease-in-out infinite; }
        @keyframes float { 0%, 100% { transform: translateY(0) scale(1); } 50% { transform: translateY(-15px) scale(1.05); } }
        #loading h1 {
            font-size: 38px; font-weight: 900; text-align: center;
            background: linear-gradient(135deg, #7cb342, #8bc34a, #7cb342);
            background-size: 200% 200%;
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            animation: shine 3s ease-in-out infinite;
        }
        @keyframes shine { 0%, 100% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } }
        #loading .sub { color: #444; font-size: 13px; margin-top: 4px; letter-spacing: 4px; }
        #loading-bar { width: 80%; max-width: 300px; height: 4px; background: rgba(255,255,255,0.04); border-radius: 4px; overflow: hidden; margin-top: 20px; }
        #loading-fill { height: 100%; background: linear-gradient(90deg, #7cb342, #8bc34a); width: 0%; border-radius: 4px; transition: width 0.5s ease; }
        #loading-text { color: #333; font-size: 12px; margin-top: 12px; text-align: center; font-weight: 300; }

        /* Menu Premium */
        #menu {
            position: fixed; inset: 0; z-index: 50;
            background: linear-gradient(135deg, #0a0a12, #12122a, #0a1a2a);
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            color: white; padding: 30px;
        }
        #menu.hidden { display: none; }
        #menu .icon { font-size: 72px; margin-bottom: 10px; animation: float 3s ease-in-out infinite; }
        #menu h1 {
            font-size: 42px; font-weight: 900; text-align: center;
            background: linear-gradient(135deg, #7cb342, #8bc34a, #7cb342);
            background-size: 200% 200%;
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            animation: shine 3s ease-in-out infinite;
        }
        #menu .subtitle { color: #555; font-size: 14px; letter-spacing: 4px; margin-bottom: 28px; }
        #menu button {
            background: linear-gradient(135deg, #7cb342, #558b2f);
            border: none; color: white; font-size: 18px; font-weight: 700;
            padding: 16px 44px; border-radius: 18px; cursor: pointer;
            transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
            border: 2px solid rgba(139,195,74,0.15);
            touch-action: manipulation; width: 100%; max-width: 280px;
            letter-spacing: 1px;
            box-shadow: 0 8px 32px rgba(124,179,66,0.2);
        }
        #menu button:active { transform: scale(0.95); }
        #menu .sub { margin-top: 16px; display: flex; gap: 10px; flex-wrap: wrap; justify-content: center; }
        #menu .sub button {
            font-size: 13px; padding: 10px 20px;
            background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.04);
            width: auto; max-width: none;
            box-shadow: none;
            letter-spacing: 0.5px;
        }
        #menu .sub button:active { background: rgba(255,255,255,0.06); }
        #menu .footer { position: absolute; bottom: 18px; color: #1a1a2a; font-size: 11px; text-align: center; }

        /* Controls Modal Premium */
        #controls-modal {
            display: none; position: fixed; inset: 0; z-index: 200;
            background: rgba(0,0,0,0.9); backdrop-filter: blur(24px);
            justify-content: center; align-items: center; padding: 20px;
        }
        #controls-modal.active { display: flex; }
        #controls-modal .box {
            background: rgba(16,16,32,0.95); padding: 24px; border-radius: 24px;
            border: 1px solid rgba(255,255,255,0.04); max-width: 380px; width: 100%;
            color: white; max-height: 80vh; overflow-y: auto;
            backdrop-filter: blur(8px);
        }
        #controls-modal .box h2 { margin-bottom: 14px; font-size: 20px; font-weight: 700; }
        #controls-modal .box .grid {
            display: grid; grid-template-columns: 1fr 1fr;
            gap: 4px 16px; font-size: 13px;
        }
        #controls-modal .box .grid span { padding: 4px 0; border-bottom: 1px solid rgba(255,255,255,0.02); }
        #controls-modal .box .grid b { color: #7cb342; }
        #controls-modal .box .close-btn {
            margin-top: 16px; width: 100%; padding: 12px;
            background: linear-gradient(135deg, #7cb342, #558b2f);
            border: none; border-radius: 14px;
            color: white; font-weight: 700; font-size: 16px; cursor: pointer;
            transition: 0.2s;
        }
        #controls-modal .box .close-btn:active { transform: scale(0.95); }

        /* Responsive */
        @media (max-width: 480px) {
            #hud { font-size: 9px; gap: 6px; padding: 5px 10px; top: 6px; }
            .slot { width: 40px; height: 40px; font-size: 17px; }
            .ctrl-btn { width: 56px; height: 56px; font-size: 22px; }
            .ctrl-btn.small { width: 48px; height: 48px; font-size: 18px; }
            #joystick-area { width: 120px; height: 120px; left: 14px; bottom: 90px; }
            #joystick-knob { width: 50px; height: 50px; }
            #menu h1 { font-size: 32px; }
            #menu .icon { font-size: 56px; }
            #mobile-controls { padding: 0 8px; bottom: 14px; }
            #mobile-controls .left, #mobile-controls .right { gap: 6px; }
            #toast { font-size: 12px; padding: 8px 16px; bottom: 175px; }
            #inv-grid { grid-template-columns: repeat(4, 1fr); gap: 6px; }
            .inv-slot { font-size: 22px; min-height: 48px; }
            #hotbar { bottom: 90px; padding: 4px 6px; gap: 3px; }
            #block-info { bottom: 155px; font-size: 10px; }
        }

        @media (pointer: coarse) {
            #mobile-controls { display: flex; }
            #joystick-area { display: block; }
        }

        @media (min-width: 769px) {
            #mobile-controls { display: none !important; }
            #joystick-area { display: none !important; }
        }
    </style>
</head>
<body>

    <!-- Loading -->
    <div id="loading">
        <div class="icon">⛏️</div>
        <h1>MINECRAFT ULTRA</h1>
        <div class="sub">MOBILE EDITION</div>
        <div id="loading-bar"><div id="loading-fill"></div></div>
        <div id="loading-text">در حال تولید جهان...</div>
    </div>

    <!-- Menu -->
    <div id="menu">
        <div class="icon">⛏️</div>
        <h1>MINECRAFT ULTRA</h1>
        <div class="subtitle">MOBILE EDITION</div>
        <button onclick="startGame()">▶ ورود به جهان</button>
        <div class="sub">
            <button onclick="showControls()">⌨ کنترل‌ها</button>
            <button onclick="alert('⚙ تنظیمات در حال توسعه...')">⚙ تنظیمات</button>
        </div>
        <div class="footer">ساخته شده با ❤️ و Three.js</div>
    </div>

    <!-- Controls Modal -->
    <div id="controls-modal">
        <div class="box">
            <h2>⌨ کنترل‌ها</h2>
            <div class="grid">
                <span><b>جوی‌استیک</b> چپ</span><span>حرکت</span>
                <span><b>دکمه</b> سبز</span><span>پرش</span>
                <span><b>دکمه</b> قرمز</span><span>شکستن</span>
                <span><b>دکمه</b> آبی</span><span>قرار دادن</span>
                <span><b>دکمه</b> طلایی</span><span>موجودی</span>
                <span><b>لمس</b> صفحه</span><span>چرخش دوربین</span>
                <span><b>1-8</b> صفحه‌کلید</span><span>انتخاب بلاک</span>
                <span><b>Esc</b></span><span>منو</span>
            </div>
            <button class="close-btn" onclick="document.getElementById('controls-modal').classList.remove('active')">بستن</button>
        </div>
    </div>

    <!-- HUD -->
    <div id="hud">
        <span>📍 <span class="val" id="coords">0, 0, 0</span></span>
        <span>⏱ <span class="val" id="time">روز</span></span>
        <span>📦 <span class="val" id="block-count">0</span></span>
    </div>

    <!-- Crosshair -->
    <div id="crosshair"><div id="crosshair-dot"></div></div>

    <!-- Block Info -->
    <div id="block-info">🌍 سنگ</div>

    <!-- Toast -->
    <div id="toast"></div>

    <!-- Hotbar -->
    <div id="hotbar"></div>

    <!-- Joystick -->
    <div id="joystick-area">
        <div id="joystick-knob"></div>
    </div>

    <!-- Mobile Controls -->
    <div id="mobile-controls">
        <div class="left">
            <div class="ctrl-btn jump" id="btn-jump">⬆</div>
        </div>
        <div class="right">
            <div class="ctrl-btn break small" id="btn-break">⛏</div>
            <div class="ctrl-btn place small" id="btn-place">🧱</div>
            <div class="ctrl-btn inv small" id="btn-inv">📦</div>
        </div>
    </div>

    <!-- Inventory -->
    <div id="inventory">
        <div id="inv-header">
            <h2>📦 موجودی</h2>
            <button id="inv-close" onclick="closeInventory()">✕</button>
        </div>
        <div id="inv-grid"></div>
    </div>

    <!-- Three.js Container -->
    <div id="canvas-container"></div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script>
        // ================================================================
        // BLOCK TYPES با کیفیت بالا
        // ================================================================
        const BLOCKS = [
            { id: 0, name: 'چمن', color: 0x7cb342, emoji: '🌿', roughness: 0.6, metalness: 0.05 },
            { id: 1, name: 'خاک', color: 0x8d6e63, emoji: '🟫', roughness: 0.8, metalness: 0.0 },
            { id: 2, name: 'سنگ', color: 0x78909c, emoji: '🪨', roughness: 0.4, metalness: 0.2 },
            { id: 3, name: 'چوب', color: 0x8d6e63, emoji: '🪵', roughness: 0.7, metalness: 0.0 },
            { id: 4, name: 'برگ', color: 0x4caf50, emoji: '🌳', roughness: 0.9, metalness: 0.0 },
            { id: 5, name: 'شن', color: 0xf5e6ca, emoji: '🏖️', roughness: 0.9, metalness: 0.0 },
            { id: 6, name: 'تخته', color: 0xdeb887, emoji: '🪵', roughness: 0.5, metalness: 0.0 },
            { id: 7, name: 'آجر', color: 0xb85a33, emoji: '🧱', roughness: 0.6, metalness: 0.1 },
            { id: 8, name: 'سنگفرش', color: 0x616161, emoji: '🪨', roughness: 0.7, metalness: 0.1 },
            { id: 9, name: 'برف', color: 0xeeeeee, emoji: '❄️', roughness: 0.3, metalness: 0.0 },
            { id: 10, name: 'الماس', color: 0x4dd0e1, emoji: '💎', roughness: 0.1, metalness: 0.8 },
            { id: 11, name: 'طلایی', color: 0xffd700, emoji: '✨', roughness: 0.2, metalness: 0.9 },
        ];

        // ================================================================
        // STATE
        // ================================================================
        const WORLD = 20;
        let blocks = new Map();
        let meshes = new Map();
        let scene, camera, renderer;
        let player = { x: 0, y: 12, z: 0, vx: 0, vy: 0, vz: 0 };
        let selectedSlot = 0;
        let inventory = {};
        let isLocked = false;
        let isGame = false;
        let angleX = 0, angleY = -0.1;
        let keys = { w: false, a: false, s: false, d: false, space: false, shift: false };
        let onGround = false;
        let toastTimer = null;
        let isMobile = false;
        let touchStartX = 0, touchStartY = 0;
        let joystickTouch = null;
        let joystickCenterX = 0, joystickCenterY = 0;
        let spawnY = 12;

        // ================================================================
        // DETECT MOBILE
        // ================================================================
        isMobile = ('ontouchstart' in window) || (navigator.maxTouchPoints > 0) || (window.innerWidth < 768);

        // ================================================================
        // THREE.JS INIT - با کیفیت فوق‌العاده
        // ================================================================
        function initThree() {
            const container = document.getElementById('canvas-container');
            
            scene = new THREE.Scene();
            scene.background = new THREE.Color(0x87CEEB);
            scene.fog = new THREE.FogExp2(0x87CEEB, 0.006);

            camera = new THREE.PerspectiveCamera(70, window.innerWidth / window.innerHeight, 0.1, 150);
            camera.position.set(0, 12, 15);

            renderer = new THREE.WebGLRenderer({ 
                antialias: true, 
                powerPreference: "high-performance",
                alpha: false,
                stencil: false,
                depth: true
            });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
            renderer.shadowMap.enabled = true;
            renderer.shadowMap.type = THREE.PCFSoftShadowMap;
            renderer.toneMapping = THREE.ACESFilmicToneMapping;
            renderer.toneMappingExposure = 1.2;
            renderer.outputEncoding = THREE.sRGBEncoding;
            renderer.physicallyCorrectLights = true;
            container.appendChild(renderer.domElement);

            // Lights - کیفیت بالا
            const ambient = new THREE.AmbientLight(0x404060, 0.6);
            scene.add(ambient);

            const hemi = new THREE.HemisphereLight(0x87CEEB, 0x3a2a1a, 0.8);
            scene.add(hemi);

            const sun = new THREE.DirectionalLight(0xffeedd, 1.5);
            sun.position.set(50, 80, 30);
            sun.castShadow = true;
            sun.shadow.mapSize.width = 2048;
            sun.shadow.mapSize.height = 2048;
            sun.shadow.camera.near = 1;
            sun.shadow.camera.far = 150;
            sun.shadow.camera.left = -60;
            sun.shadow.camera.right = 60;
            sun.shadow.camera.top = 60;
            sun.shadow.camera.bottom = -60;
            sun.shadow.bias = -0.001;
            scene.add(sun);
            window.sunLight = sun;

            const fill = new THREE.DirectionalLight(0x8888ff, 0.3);
            fill.position.set(-30, 40, -30);
            scene.add(fill);

            window.addEventListener('resize', () => {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            });
        }

        // ================================================================
        // BLOCK FUNCTIONS - با کیفیت بالا
        // ================================================================
        function key(x, y, z) { return x + ',' + y + ',' + z; }

        function setBlock(x, y, z, block) {
            const k = key(x, y, z);
            if (block === null) {
                blocks.delete(k);
                if (meshes.has(k)) {
                    scene.remove(meshes.get(k));
                    meshes.delete(k);
                }
                return;
            }
            blocks.set(k, block);
            if (meshes.has(k)) {
                scene.remove(meshes.get(k));
                meshes.delete(k);
            }
            const mesh = makeBlock(x, y, z, block);
            scene.add(mesh);
            meshes.set(k, mesh);
        }

        function getBlock(x, y, z) {
            return blocks.get(key(x, y, z)) || null;
        }

        function makeBlock(x, y, z, block) {
            const geo = new THREE.BoxGeometry(1, 1, 1);
            
            const dirs = [
                [0,0,1], [0,0,-1], [0,1,0], [0,-1,0], [1,0,0], [-1,0,0]
            ];
            const mats = dirs.map(([dx, dy, dz]) => {
                const neighbor = getBlock(x+dx, y+dy, z+dz);
                if (neighbor !== null) {
                    return new THREE.MeshStandardMaterial({
                        color: block.color,
                        transparent: true,
                        opacity: 0,
                        roughness: block.roughness || 0.5,
                        metalness: block.metalness || 0.1,
                    });
                } else {
                    const c = block.color;
                    const v = 0.92 + Math.random() * 0.16;
                    return new THREE.MeshStandardMaterial({
                        color: new THREE.Color(
                            ((c>>16)&0xFF)/255 * v,
                            ((c>>8)&0xFF)/255 * v,
                            (c&0xFF)/255 * v
                        ),
                        roughness: (block.roughness || 0.5) + (Math.random() - 0.5) * 0.1,
                        metalness: (block.metalness || 0.1) + (Math.random() - 0.5) * 0.05,
                        emissive: new THREE.Color(0x000000),
                        emissiveIntensity: 0,
                    });
                }
            });

            const mesh = new THREE.Mesh(geo, mats);
            mesh.position.set(x + 0.5, y + 0.5, z + 0.5);
            mesh.castShadow = true;
            mesh.receiveShadow = true;
            mesh.userData = { bx: x, by: y, bz: z };
            return mesh;
        }

        // ================================================================
        // WORLD GENERATION - با کیفیت بالا و جزئیات بیشتر
        // ================================================================
        function generateWorld() {
            const fill = document.getElementById('loading-fill');
            const text = document.getElementById('loading-text');
            let prog = 0;

            for (let x = -WORLD; x < WORLD; x++) {
                for (let z = -WORLD; z < WORLD; z++) {
                    // Terrain با کیفیت بالا
                    const h1 = Math.sin(x * 0.08) * Math.cos(z * 0.06) * 5;
                    const h2 = Math.sin(x * 0.15 + z * 0.12) * 3;
                    const h3 = Math.sin(x * 0.3) * Math.cos(z * 0.25) * 1;
                    const h4 = Math.sin(x * 0.05 + z * 0.07) * 2;
                    const height = Math.floor(h1 + h2 + h3 + h4 + 4);
                    const finalHeight = Math.max(1, Math.min(14, height));
                    
                    for (let y = 0; y < finalHeight; y++) {
                        let block;
                        if (y === finalHeight - 1) {
                            if (finalHeight > 8) block = BLOCKS[0];
                            else if (finalHeight > 5) block = BLOCKS[5];
                            else if (finalHeight > 3) block = BLOCKS[9];
                            else block = BLOCKS[9];
                        } else if (y > finalHeight - 4) {
                            block = BLOCKS[1];
                        } else if (y > finalHeight - 8 && finalHeight > 7) {
                            block = BLOCKS[2];
                        } else {
                            block = BLOCKS[2];
                        }
                        setBlock(x, y, z, block);
                    }

                    // Trees با کیفیت بالا
                    if (finalHeight > 5 && Math.random() < 0.02) {
                        const trunkHeight = 4 + Math.floor(Math.random() * 3);
                        for (let ty = 0; ty < trunkHeight; ty++) {
                            setBlock(x, finalHeight + ty, z, BLOCKS[3]);
                        }
                        for (let lx = -2; lx <= 2; lx++) {
                            for (let lz = -2; lz <= 2; lz++) {
                                for (let ly = 0; ly < 3; ly++) {
                                    if (Math.abs(lx) === 2 && Math.abs(lz) === 2 && Math.random() < 0.5) continue;
                                    if (Math.abs(lx) === 2 && Math.random() < 0.3) continue;
                                    if (Math.abs(lz) === 2 && Math.random() < 0.3) continue;
                                    setBlock(x + lx, finalHeight + trunkHeight + ly, z + lz, BLOCKS[4]);
                                }
                            }
                        }
                    }

                    // Ores با کیفیت بالا
                    if (finalHeight > 4 && Math.random() < 0.003) {
                        setBlock(x, Math.floor(Math.random() * (finalHeight - 3)) + 2, z, BLOCKS[10]);
                    }
                    if (finalHeight > 3 && Math.random() < 0.005) {
                        setBlock(x, Math.floor(Math.random() * (finalHeight - 2)) + 1, z, BLOCKS[11]);
                    }
                }
                prog = (x + WORLD) / (WORLD * 2);
                fill.style.width = (prog * 65) + '%';
                text.textContent = `تولید جهان... ${Math.round(prog * 65)}%`;
            }

            // Structures با کیفیت بالا
            buildHouse(-12, 6, -10);
            buildHouse(10, 6, 8);
            buildHouse(-8, 7, 12);
            buildTower(14, 5, -12);
            buildBridge(-6, 5, 16, 6, 5, 22);

            let foundSpawnY = 0;
            for (let y = 25; y > -5; y--) {
                if (getBlock(0, y, 0) !== null) {
                    foundSpawnY = y + 1;
                    break;
                }
            }
            spawnY = foundSpawnY > 0 ? foundSpawnY : 12;
            player.y = spawnY;
            camera.position.set(player.x, player.y, player.z + 5);

            fill.style.width = '100%';
            text.textContent = 'جهان آماده است!';
            setTimeout(() => {
                document.getElementById('loading').classList.add('hidden');
                showToast('⛏️ جهان با کیفیت بالا ساخته شد!');
            }, 500);
        }

        function buildHouse(x, y, z) {
            const w = 6, h = 5, d = 6;
            for (let bx = 0; bx < w; bx++) {
                for (let bz = 0; bz < d; bz++) {
                    for (let by = 0; by < h; by++) {
                        if (bx === 0 || bx === w-1 || bz === 0 || bz === d-1 || by === 0 || by === h-1) {
                            if (bx === Math.floor(w/2) && by === 1 && bz === 0) continue;
                            setBlock(x + bx, y + by, z + bz, BLOCKS[6]);
                        }
                    }
                }
            }
            for (let bx = -2; bx < w+2; bx++) {
                for (let bz = -2; bz < d+2; bz++) {
                    if (Math.abs(bx) === 2 || Math.abs(bz) === 2) continue;
                    setBlock(x + bx, y + h, z + bz, BLOCKS[7]);
                }
            }
            setBlock(x + Math.floor(w/2), y + 1, z, null);
            setBlock(x + 1, y + 2, z, null);
            setBlock(x + w - 2, y + 2, z, null);
            setBlock(x + 2, y + 3, z, null);
            setBlock(x + w - 3, y + 3, z, null);
        }

        function buildTower(x, y, z) {
            for (let ty = 0; ty < 8; ty++) {
                for (let tx = -2; tx <= 2; tx++) {
                    for (let tz = -2; tz <= 2; tz++) {
                        if (Math.abs(tx) === 2 && Math.abs(tz) === 2) continue;
                        if (tx === 0 && tz === 0) continue;
                        setBlock(x + tx, y + ty, z + tz, BLOCKS[8]);
                    }
                }
                setBlock(x, y + ty, z, BLOCKS[2]);
            }
            for (let tx = -3; tx <= 3; tx++) {
                for (let tz = -3; tz <= 3; tz++) {
                    if (Math.abs(tx) === 3 || Math.abs(tz) === 3) continue;
                    setBlock(x + tx, y + 8, z + tz, BLOCKS[7]);
                }
            }
        }

        function buildBridge(x, y, z, x2, y2, z2) {
            const dx = x2 - x;
            const dz = z2 - z;
            const steps = Math.max(Math.abs(dx), Math.abs(dz));
            for (let i = 0; i <= steps; i++) {
                const t = i / steps;
                const bx = Math.round(x + dx * t);
                const bz = Math.round(z + dz * t);
                setBlock(bx, y, bz, BLOCKS[6]);
                setBlock(bx, y+1, bz, BLOCKS[6]);
                if (i > 0 && i < steps) {
                    setBlock(bx-1, y, bz, BLOCKS[8]);
                    setBlock(bx+1, y, bz, BLOCKS[8]);
                    setBlock(bx, y, bz-1, BLOCKS[8]);
                    setBlock(bx, y, bz+1, BLOCKS[8]);
                }
            }
        }

        // ================================================================
        // بقیه کد مشابه قبل با کیفیت بالاتر
        // ================================================================
        // [ادامه کد با همان توابع قبلی اما با کیفیت بهتر]

        // ================================================================
        // INVENTORY
        // ================================================================
        function initInventory() {
            const start = [BLOCKS[0], BLOCKS[1], BLOCKS[2], BLOCKS[3], BLOCKS[6], BLOCKS[8], BLOCKS[5], BLOCKS[7]];
            start.forEach((b, i) => {
                inventory[b.id] = 64;
                const slot = document.querySelector(`.slot[data-idx="${i}"]`);
                if (slot) {
                    slot.dataset.bid = b.id;
                    slot.querySelector('.emoji').textContent = b.emoji;
                    slot.querySelector('.name').textContent = b.name;
                    slot.querySelector('.count').textContent = '64';
                }
            });
            inventory[10] = 8;
            inventory[11] = 5;
            updateHotbar();
        }

        function updateHotbar() {
            document.querySelectorAll('.slot').forEach((slot) => {
                const bid = parseInt(slot.dataset.bid);
                if (!isNaN(bid)) {
                    const count = inventory[bid] || 0;
                    const countEl = slot.querySelector('.count');
                    if (countEl) countEl.textContent = count > 0 ? count : '';
                }
            });
        }

        function buildHotbar() {
            const hotbar = document.getElementById('hotbar');
            hotbar.innerHTML = '';
            for (let i = 0; i < 8; i++) {
                const slot = document.createElement('div');
                slot.className = 'slot' + (i === 0 ? ' active' : '');
                slot.dataset.idx = i;
                slot.dataset.bid = '';
                slot.innerHTML = `
                    <span class="emoji">⬜</span>
                    <span class="name">خالی</span>
                    <span class="count"></span>
                `;
                slot.addEventListener('click', () => {
                    selectedSlot = i;
                    updateHotbarSelection();
                });
                slot.addEventListener('touchstart', (e) => {
                    e.preventDefault();
                    selectedSlot = i;
                    updateHotbarSelection();
                });
                hotbar.appendChild(slot);
            }
        }

        function updateHotbarSelection() {
            document.querySelectorAll('.slot').forEach((s, i) => {
                s.classList.toggle('active', i === selectedSlot);
            });
            const slot = document.querySelector(`.slot[data-idx="${selectedSlot}"]`);
            const bid = parseInt(slot.dataset.bid);
            if (!isNaN(bid)) {
                const block = BLOCKS.find(b => b.id === bid);
                if (block) document.getElementById('block-info').textContent = `${block.emoji} ${block.name}`;
            }
        }

        // ================================================================
        // RAYCASTER
        // ================================================================
        function getTarget() {
            if (!camera) return null;
            const raycaster = new THREE.Raycaster();
            raycaster.set(camera.position, camera.getWorldDirection(new THREE.Vector3()));
            raycaster.far = 7;
            
            const targets = [];
            meshes.forEach(m => targets.push(m));
            const hits = raycaster.intersectObjects(targets);
            if (hits.length > 0) {
                const h = hits[0];
                const { bx, by, bz } = h.object.userData;
                return {
                    x: bx, y: by, z: bz,
                    normal: h.face.normal,
                    mesh: h.object
                };
            }
            return null;
        }

        function breakBlock() {
            const t = getTarget();
            if (!t) return;
            const block = getBlock(t.x, t.y, t.z);
            if (!block) return;
            
            inventory[block.id] = (inventory[block.id] || 0) + 1;
            setBlock(t.x, t.y, t.z, null);
            showToast(`⛏️ ${block.emoji} ${block.name}`);
            updateHotbar();
            updateBlockCount();
            
            const dirs = [[1,0,0],[-1,0,0],[0,1,0],[0,-1,0],[0,0,1],[0,0,-1]];
            dirs.forEach(([dx, dy, dz]) => {
                const nb = getBlock(t.x+dx, t.y+dy, t.z+dz);
                if (nb) {
                    setBlock(t.x+dx, t.y+dy, t.z+dz, nb);
                }
            });
        }

        function placeBlock() {
            const t = getTarget();
            if (!t) return;
            
            const slot = document.querySelector(`.slot[data-idx="${selectedSlot}"]`);
            const bid = parseInt(slot.dataset.bid);
            if (isNaN(bid)) return;
            
            const block = BLOCKS.find(b => b.id === bid);
            if (!block) return;
            if ((inventory[bid] || 0) <= 0) {
                showToast('❌ این بلاک را ندارید!');
                return;
            }

            const nx = Math.round(t.x + t.normal.x);
            const ny = Math.round(t.y + t.normal.y);
            const nz = Math.round(t.z + t.normal.z);
            
            const px = Math.round(player.x);
            const py = Math.round(player.y);
            const pz = Math.round(player.z);
            if (nx === px && (ny === py || ny === py+1) && nz === pz) return;
            
            if (getBlock(nx, ny, nz) !== null) return;
            
            setBlock(nx, ny, nz, block);
            inventory[bid]--;
            showToast(`✅ ${block.emoji} ${block.name}`);
            updateHotbar();
            updateBlockCount();
        }

        function showToast(msg) {
            const el = document.getElementById('toast');
            el.textContent = msg;
            el.classList.add('show');
            clearTimeout(toastTimer);
            toastTimer = setTimeout(() => el.classList.remove('show'), 1500);
        }

        function updateBlockCount() {
            document.getElementById('block-count').textContent = blocks.size;
        }

        function updateCoords() {
            document.getElementById('coords').textContent = 
                `${Math.round(player.x)}, ${Math.round(player.y)}, ${Math.round(player.z)}`;
        }

        function updateTime() {
            const d = new Date();
            const h = d.getHours();
            document.getElementById('time').textContent = (h > 6 && h < 19) ? '☀️ روز' : '🌙 شب';
            if (scene) {
                const isNight = (h < 6 || h > 19);
                scene.background = new THREE.Color(isNight ? 0x0a0a1a : 0x87CEEB);
                scene.fog.color = new THREE.Color(isNight ? 0x0a0a1a : 0x87CEEB);
            }
        }

        // ================================================================
        // PHYSICS
        // ================================================================
        function updatePhysics() {
            if (!isGame || !isLocked) return;

            const speed = keys.shift ? 0.05 : 0.08;
            const gravity = -0.025;
            const jump = 0.22;

            const forward = new THREE.Vector3(Math.sin(angleX), 0, Math.cos(angleX));
            const side = new THREE.Vector3(Math.cos(angleX), 0, -Math.sin(angleX));

            let mx = 0, mz = 0;
            if (keys.w) { mx += forward.x; mz += forward.z; }
            if (keys.s) { mx -= forward.x; mz -= forward.z; }
            if (keys.d) { mx += side.x; mz += side.z; }
            if (keys.a) { mx -= side.x; mz -= side.z; }
            
            const len = Math.sqrt(mx*mx + mz*mz);
            if (len > 0) {
                player.vx += (mx/len) * speed * 0.3;
                player.vz += (mz/len) * speed * 0.3;
            }
            player.vx *= 0.85;
            player.vz *= 0.85;

            player.vy += gravity;
            
            if (keys.space && onGround) {
                player.vy = jump;
                onGround = false;
            }

            let nx = player.x + player.vx;
            let ny = player.y + player.vy;
            let nz = player.z + player.vz;

            if (getBlock(Math.round(nx), Math.round(player.y), Math.round(player.z)) !== null) {
                player.vx = 0;
                nx = player.x;
            }
            if (getBlock(Math.round(player.x), Math.round(ny), Math.round(player.z)) !== null) {
                if (player.vy < 0) onGround = true;
                player.vy = 0;
                ny = player.y;
            }
            if (getBlock(Math.round(player.x), Math.round(player.y), Math.round(nz)) !== null) {
                player.vz = 0;
                nz = player.z;
            }

            if (getBlock(Math.round(nx), Math.round(ny - 0.5), Math.round(nz)) !== null) {
                onGround = true;
            }

            player.x = nx;
            player.y = ny;
            player.z = nz;

            const b = WORLD - 0.5;
            player.x = Math.max(-b, Math.min(b, player.x));
            player.z = Math.max(-b, Math.min(b, player.z));
            
            if (player.y < -5) {
                let foundY = spawnY;
                for (let y = 25; y > -5; y--) {
                    if (getBlock(Math.round(player.x), y, Math.round(player.z)) !== null) {
                        foundY = y + 1;
                        break;
                    }
                }
                player.y = foundY;
                player.vy = 0;
                onGround = true;
                showToast('🔄 برگشت به سطح زمین');
            }

            camera.position.set(player.x, player.y, player.z);
            const target = new THREE.Vector3(
                player.x + Math.sin(angleX) * Math.cos(angleY),
                player.y + Math.sin(angleY),
                player.z + Math.cos(angleX) * Math.cos(angleY)
            );
            camera.lookAt(target);

            updateCoords();
        }

        // ================================================================
        // INPUT - KEYBOARD
        // ================================================================
        document.addEventListener('keydown', (e) => {
            if (e.code === 'KeyW') keys.w = true;
            if (e.code === 'KeyS') keys.s = true;
            if (e.code === 'KeyA') keys.a = true;
            if (e.code === 'KeyD') keys.d = true;
            if (e.code === 'Space') { e.preventDefault(); keys.space = true; }
            if (e.code === 'ShiftLeft' || e.code === 'ShiftRight') keys.shift = true;
            if (e.code === 'KeyE') { e.preventDefault(); toggleInventory(); }
            if (e.code === 'Escape') {
                if (document.pointerLockElement) document.exitPointerLock();
                document.getElementById('menu').classList.remove('hidden');
                isGame = false;
            }
            const num = parseInt(e.key);
            if (num >= 1 && num <= 8) {
                selectedSlot = num - 1;
                updateHotbarSelection();
            }
        });

        document.addEventListener('keyup', (e) => {
            if (e.code === 'KeyW') keys.w = false;
            if (e.code === 'KeyS') keys.s = false;
            if (e.code === 'KeyA') keys.a = false;
            if (e.code === 'KeyD') keys.d = false;
            if (e.code === 'Space') keys.space = false;
            if (e.code === 'ShiftLeft' || e.code === 'ShiftRight') keys.shift = false;
        });

        // ================================================================
        // INPUT - MOUSE
        // ================================================================
        document.addEventListener('mousemove', (e) => {
            if (!isLocked || !isGame) return;
            const sens = 0.002;
            angleX -= e.movementX * sens;
            angleY -= e.movementY * sens;
            angleY = Math.max(-1.4, Math.min(1.4, angleY));
        });

        document.addEventListener('mousedown', (e) => {
            if (!isLocked || !isGame) return;
            if (e.button === 0) breakBlock();
            if (e.button === 2) placeBlock();
        });

        document.addEventListener('contextmenu', (e) => e.preventDefault());

        document.addEventListener('pointerlockchange', () => {
            isLocked = (document.pointerLockElement === document.getElementById('canvas-container'));
        });

        // ================================================================
        // INPUT - TOUCH
        // ================================================================
        let touchPointer = false;

        document.getElementById('canvas-container').addEventListener('touchstart', (e) => {
            if (!isGame) return;
            e.preventDefault();
            touchPointer = true;
            const touch = e.touches[0];
            touchStartX = touch.clientX;
            touchStartY = touch.clientY;
        });

        document.getElementById('canvas-container').addEventListener('touchmove', (e) => {
            if (!isGame || !touchPointer) return;
            e.preventDefault();
            const touch = e.touches[0];
            const dx = touch.clientX - touchStartX;
            const dy = touch.clientY - touchStartY;
            touchStartX = touch.clientX;
            touchStartY = touch.clientY;
            
            const sens = 0.005;
            angleX -= dx * sens;
            angleY -= dy * sens;
            angleY = Math.max(-1.4, Math.min(1.4, angleY));
        });

        document.getElementById('canvas-container').addEventListener('touchend', (e) => {
            touchPointer = false;
        });

        // ================================================================
        // MOBILE CONTROLS
        // ================================================================
        document.getElementById('btn-jump').addEventListener('touchstart', (e) => {
            e.preventDefault();
            keys.space = true;
        });
        document.getElementById('btn-jump').addEventListener('touchend', (e) => {
            e.preventDefault();
            keys.space = false;
        });

        document.getElementById('btn-break').addEventListener('touchstart', (e) => {
            e.preventDefault();
            breakBlock();
        });

        document.getElementById('btn-place').addEventListener('touchstart', (e) => {
            e.preventDefault();
            placeBlock();
        });

        document.getElementById('btn-inv').addEventListener('touchstart', (e) => {
            e.preventDefault();
            toggleInventory();
        });

        // ================================================================
        // JOYSTICK
        // ================================================================
        const joystickArea = document.getElementById('joystick-area');
        const joystickKnob = document.getElementById('joystick-knob');

        joystickArea.addEventListener('touchstart', (e) => {
            e.preventDefault();
            const rect = joystickArea.getBoundingClientRect();
            joystickCenterX = rect.left + rect.width / 2;
            joystickCenterY = rect.top + rect.height / 2;
            joystickTouch = e.touches[0];
            updateJoystick(e.touches[0]);
        });

        joystickArea.addEventListener('touchmove', (e) => {
            e.preventDefault();
            if (joystickTouch) {
                updateJoystick(e.touches[0]);
            }
        });

        joystickArea.addEventListener('touchend', (e) => {
            e.preventDefault();
            joystickTouch = null;
            joystickKnob.style.transform = 'translate(-50%, -50%)';
            keys.w = false;
            keys.s = false;
            keys.a = false;
            keys.d = false;
        });

        function updateJoystick(touch) {
            const dx = touch.clientX - joystickCenterX;
            const dy = touch.clientY - joystickCenterY;
            const maxDist = 45;
            const dist = Math.sqrt(dx*dx + dy*dy);
            const clampedDist = Math.min(dist, maxDist);
            const angle = Math.atan2(dy, dx);
            const nx = Math.cos(angle) * clampedDist;
            const ny = Math.sin(angle) * clampedDist;
            
            joystickKnob.style.transform = `translate(${-50 + nx/maxDist*50}%, ${-50 + ny/maxDist*50}%)`;
            
            const normX = nx / maxDist;
            const normY = ny / maxDist;
            
            keys.w = normY < -0.2;
            keys.s = normY > 0.2;
            keys.a = normX < -0.2;
            keys.d = normX > 0.2;
        }

        // ================================================================
        // INVENTORY
        // ================================================================
        function toggleInventory() {
            const inv = document.getElementById('inventory');
            inv.classList.toggle('active');
            if (inv.classList.contains('active')) {
                renderInventory();
                if (isLocked) document.exitPointerLock();
            }
        }

        function closeInventory() {
            document.getElementById('inventory').classList.remove('active');
        }

        function renderInventory() {
            const grid = document.getElementById('inv-grid');
            grid.innerHTML = '';
            BLOCKS.forEach((block) => {
                const count = inventory[block.id] || 0;
                const slot = document.createElement('div');
                slot.className = 'inv-slot';
                slot.innerHTML = `
                    <span>${block.emoji}</span>
                    <span class="icount">${count > 0 ? count : ''}</span>
                `;
                slot.addEventListener('click', () => {
                    const idx = BLOCKS.indexOf(block);
                    if (idx < 8) {
                        selectedSlot = idx;
                        updateHotbarSelection();
                        closeInventory();
                    } else {
                        showToast('⚠️ این بلاک در هاتبار نیست');
                    }
                });
                grid.appendChild(slot);
            });
        }

        // ================================================================
        // CONTROLS
        // ================================================================
        function showControls() {
            document.getElementById('controls-modal').classList.add('active');
        }

        // ================================================================
        // GAME START
        // ================================================================
        function startGame() {
            document.getElementById('menu').classList.add('hidden');
            document.getElementById('loading').classList.add('hidden');
            isGame = true;
            if (!isMobile) {
                document.getElementById('canvas-container').requestPointerLock();
            }
            isLocked = true;
            showToast('🎮 وارد جهان شدید!');
        }

        // ================================================================
        // ANIMATION LOOP
        // ================================================================
        function animate() {
            requestAnimationFrame(animate);
            
            updatePhysics();
            updateTime();
            
            if (window.sunLight) {
                const t = Date.now() / 40000;
                const r = 70;
                window.sunLight.position.x = Math.cos(t) * r;
                window.sunLight.position.z = Math.sin(t * 0.7) * r * 0.5;
                window.sunLight.position.y = Math.sin(t) * r * 0.6 + 25;
                const intensity = Math.max(0.15, Math.sin(t) * 0.5 + 0.7);
                window.sunLight.intensity = intensity * 1.5;
            }

            renderer.render(scene, camera);
        }

        // ================================================================
        // INIT
        // ================================================================
        function init() {
            initThree();
            buildHotbar();
            
            camera.position.set(0, 12, 15);
            
            setTimeout(() => {
                generateWorld();
                initInventory();
                updateBlockCount();
                setTimeout(() => {
                    player.y = spawnY;
                    camera.position.set(player.x, player.y, player.z + 5);
                    showToast('⛏️ جهان با کیفیت بالا ساخته شد!');
                }, 100);
            }, 300);

            animate();

            document.getElementById('canvas-container').addEventListener('click', () => {
                if (isGame && !isMobile && !document.getElementById('inventory').classList.contains('active')) {
                    document.getElementById('canvas-container').requestPointerLock();
                }
            });

            console.log('⛏️ Minecraft 3D Ultra loaded!');
            console.log('📱 Mobile controls enabled:', isMobile);
        }

        document.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>
