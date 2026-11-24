<!DOCTYPE html>
<html lang="en" class="dark" data-palette="gold">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sonai Das — Live Cyber Portfolio &amp; GitHub SVG Studio</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: JetBrains Mono & Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=JetBrains+Mono:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet" />

  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
            mono: ['JetBrains Mono', 'Fira Code', 'monospace'],
          }
        }
      }
    };
  </script>

  <style>
    /* =====================================================================
       DESIGN TOKENS: DARK / LIGHT x GOLD / CYAN PALETTES
       ===================================================================== */
    :root {
      /* Light Mode + Gold (Default Light) */
      --page-bg: #edf1f7;
      --win-bg: #f8fafc;
      --win-border: rgba(180, 138, 36, 0.5);
      --win-shadow: 0 22px 55px rgba(10, 15, 28, 0.14), 0 0 24px rgba(212, 175, 55, 0.16);
      --pane-bg: #ffffff;
      --pane-border: #b88c24;
      --pane-glow: 0 0 14px rgba(184, 140, 36, 0.14);
      --tab-bg: rgba(212, 175, 55, 0.22);
      --accent: #a67c18;
      --accent-bright: #d4af37;
      --accent-soft: rgba(212, 175, 55, 0.12);
      --accent-border: rgba(184, 140, 36, 0.38);
      --secondary: #1d4ed8;
      --rail-dash: rgba(184, 140, 36, 0.28);
      --text-main: #0f172a;
      --text-muted: #475569;
      --chip-bg: rgba(184, 140, 36, 0.09);
      --chip-border: rgba(184, 140, 36, 0.34);
      --chip-hover: rgba(184, 140, 36, 0.2);
      --stack-bg: #f1f5f9;
      --cursor-color: #a67c18;
      --studio-bg: #ffffff;
      --studio-border: rgba(184, 140, 36, 0.35);
    }

    html.dark {
      /* Dark Mode + Midnight Navy & Gold */
      --page-bg: #050811;
      --win-bg: #0a0f1c;
      --win-border: rgba(212, 175, 55, 0.55);
      --win-shadow: 0 28px 80px rgba(0, 0, 0, 0.85), 0 0 32px rgba(212, 175, 55, 0.18), inset 0 0 28px rgba(212, 175, 55, 0.04);
      --pane-bg: #0d1323;
      --pane-border: #d4af37;
      --pane-glow: 0 0 18px rgba(212, 175, 55, 0.15), inset 0 0 20px rgba(212, 175, 55, 0.03);
      --tab-bg: rgba(212, 175, 55, 0.22);
      --accent: #d4af37;
      --accent-bright: #f5d97e;
      --accent-soft: rgba(212, 175, 55, 0.11);
      --accent-border: rgba(212, 175, 55, 0.34);
      --secondary: #3b82f6;
      --rail-dash: rgba(212, 175, 55, 0.22);
      --text-main: #e2e8f0;
      --text-muted: #94a3b8;
      --chip-bg: rgba(212, 175, 55, 0.08);
      --chip-border: rgba(212, 175, 55, 0.32);
      --chip-hover: rgba(212, 175, 55, 0.2);
      --stack-bg: #080d18;
      --cursor-color: #d4af37;
      --studio-bg: #0c1221;
      --studio-border: rgba(212, 175, 55, 0.3);
    }

    /* Cyberpunk Cyan Palette Override (Light Mode) */
    html[data-palette="cyan"]:not(.dark) {
      --win-border: rgba(8, 145, 178, 0.5);
      --win-shadow: 0 22px 55px rgba(10, 15, 28, 0.12), 0 0 24px rgba(0, 240, 255, 0.16);
      --pane-border: #0891b2;
      --pane-glow: 0 0 14px rgba(8, 145, 178, 0.15);
      --tab-bg: rgba(8, 145, 178, 0.18);
      --accent: #0891b2;
      --accent-bright: #00f0ff;
      --accent-soft: rgba(8, 145, 178, 0.1);
      --accent-border: rgba(8, 145, 178, 0.35);
      --rail-dash: rgba(8, 145, 178, 0.26);
      --chip-bg: rgba(8, 145, 178, 0.08);
      --chip-border: rgba(8, 145, 178, 0.32);
      --chip-hover: rgba(8, 145, 178, 0.18);
      --cursor-color: #0891b2;
      --studio-border: rgba(8, 145, 178, 0.35);
    }

    /* Cyberpunk Cyan Palette Override (Dark Mode) */
    html.dark[data-palette="cyan"] {
      --win-border: rgba(0, 240, 255, 0.55);
      --win-shadow: 0 28px 80px rgba(0, 0, 0, 0.85), 0 0 32px rgba(0, 240, 255, 0.2), inset 0 0 28px rgba(0, 240, 255, 0.04);
      --pane-border: #00f0ff;
      --pane-glow: 0 0 18px rgba(0, 240, 255, 0.18), inset 0 0 20px rgba(0, 240, 255, 0.04);
      --tab-bg: rgba(0, 240, 255, 0.18);
      --accent: #00f0ff;
      --accent-bright: #7df9ff;
      --accent-soft: rgba(0, 240, 255, 0.1);
      --accent-border: rgba(0, 240, 255, 0.32);
      --rail-dash: rgba(0, 240, 255, 0.2);
      --chip-bg: rgba(0, 240, 255, 0.08);
      --chip-border: rgba(0, 240, 255, 0.3);
      --chip-hover: rgba(0, 240, 255, 0.2);
      --cursor-color: #00f0ff;
      --studio-border: rgba(0, 240, 255, 0.3);
    }

    * {
      box-sizing: border-box;
    }

    body {
      background-color: var(--page-bg);
      color: var(--text-main);
      transition: background-color 0.35s ease, color 0.35s ease;
      overflow-x: hidden;
    }

    .ambient-bg {
      background-image:
        radial-gradient(circle at 18% 15%, var(--accent-soft), transparent 42%),
        radial-gradient(circle at 84% 85%, rgba(59, 130, 246, 0.08), transparent 45%);
    }

    /* Outer macOS Window */
    .cyber-window {
      background-color: var(--win-bg);
      border: 1.5px solid var(--win-border);
      box-shadow: var(--win-shadow);
      transition: background-color 0.35s ease, border-color 0.35s ease, box-shadow 0.35s ease;
    }

    /* Inner Dashed Panes */
    .cyber-pane {
      position: relative;
      background-color: var(--pane-bg);
      border: 1.5px dashed var(--pane-border);
      box-shadow: var(--pane-glow);
      transition: background-color 0.35s ease, border-color 0.35s ease, box-shadow 0.35s ease;
    }

    /* Angled Top-Left Trapezoidal Accent Tab */
    .cyber-tab {
      position: absolute;
      top: 0;
      left: 14px;
      width: 106px;
      height: 13px;
      background-color: var(--tab-bg);
      clip-path: polygon(0 0, 100% 0, calc(100% - 12px) 100%, 0 100%);
      border-bottom: 1px solid var(--accent-border);
      pointer-events: none;
      z-index: 20;
    }

    /* Perimeter Dashed Rails & Glowing Light Segments */
    .rail-h {
      background-image: repeating-linear-gradient(
        to right,
        var(--rail-dash) 0px,
        var(--rail-dash) 5px,
        transparent 5px,
        transparent 16px
      );
    }
    .rail-v {
      background-image: repeating-linear-gradient(
        to bottom,
        var(--rail-dash) 0px,
        var(--rail-dash) 5px,
        transparent 5px,
        transparent 16px
      );
    }

    .neon-seg {
      position: absolute;
      border-radius: 9999px;
      will-change: opacity, transform;
    }

    .seg-primary {
      background: var(--accent-bright);
      box-shadow: 0 0 8px var(--accent-bright), 0 0 16px var(--accent);
    }

    .seg-secondary {
      background: var(--secondary);
      box-shadow: 0 0 8px var(--secondary), 0 0 16px rgba(59, 130, 246, 0.75);
    }

    @keyframes segPulse {
      0%, 100% { opacity: 0.42; transform: scaleX(0.92); }
      50% { opacity: 1; transform: scaleX(1.08); }
    }
    @keyframes glideRight {
      0% { left: -8%; opacity: 0; }
      12% { opacity: 0.95; }
      88% { opacity: 0.95; }
      100% { left: 104%; opacity: 0; }
    }
    @keyframes glideLeft {
      0% { left: 104%; opacity: 0; }
      12% { opacity: 0.95; }
      88% { opacity: 0.95; }
      100% { left: -8%; opacity: 0; }
    }

    .pulse-1 { animation: segPulse 3.2s ease-in-out infinite; }
    .pulse-2 { animation: segPulse 3.8s ease-in-out 0.9s infinite; }
    .pulse-3 { animation: segPulse 4.2s ease-in-out 1.8s infinite; }
    .glide-top { animation: glideRight 9.5s linear infinite; }
    .glide-bottom { animation: glideLeft 11s linear 2.2s infinite; }

    /* CRT Portrait Container (Always Dark Midnight Navy for Contrast) */
    .crt-box {
      background: radial-gradient(ellipse at 50% 42%, #111b33 0%, #090f1d 60%, #04070f 100%);
      box-shadow: inset 0 0 42px rgba(0, 0, 0, 0.9), 0 0 1px var(--accent-border);
    }
    .crt-scanlines {
      background: linear-gradient(
        to bottom,
        rgba(255, 255, 255, 0) 50%,
        rgba(0, 0, 0, 0.24) 50%
      );
      background-size: 100% 4px;
      pointer-events: none;
    }

    /* Drag-and-drop highlight */
    .crt-drag-over {
      box-shadow: inset 0 0 36px var(--accent), 0 0 20px var(--accent) !important;
      border-color: var(--accent-bright) !important;
    }

    /* Terminal Custom Scrollbar */
    .term-scroll::-webkit-scrollbar {
      width: 5px;
    }
    .term-scroll::-webkit-scrollbar-track {
      background: transparent;
    }
    .term-scroll::-webkit-scrollbar-thumb {
      background-color: var(--accent-border);
      border-radius: 9999px;
    }

    /* Blinking Block Cursor */
    @keyframes cursorBlink {
      0%, 49% { opacity: 1; }
      50%, 100% { opacity: 0; }
    }
    .block-cursor {
      display: inline-block;
      width: 9px;
      height: 16px;
      background-color: var(--cursor-color);
      vertical-align: middle;
      animation: cursorBlink 1.05s step-end infinite;
      box-shadow: 0 0 8px var(--accent);
    }

    /* Pulsing Online Status Dot */
    @keyframes statusPing {
      0% { transform: scale(1); opacity: 0.85; }
      75%, 100% { transform: scale(2.4); opacity: 0; }
    }
    .status-ping {
      animation: statusPing 2.2s cubic-bezier(0, 0, 0.2, 1) infinite;
    }

    /* Accent Text & Interactive Elements */
    .accent-text {
      color: var(--accent);
    }
    .accent-glow-text {
      color: var(--accent-bright);
      text-shadow: 0 0 14px var(--accent-soft);
    }
    html:not(.dark) .accent-glow-text {
      color: #0f172a;
      text-shadow: none;
    }

    .cmd-chip {
      background-color: var(--chip-bg);
      border: 1px solid var(--chip-border);
      color: var(--accent);
      transition: all 0.2s ease;
    }
    .cmd-chip:hover {
      background-color: var(--chip-hover);
      border-color: var(--accent-bright);
      transform: translateY(-1px);
    }

    .social-btn {
      color: var(--accent);
      transition: transform 0.2s ease, filter 0.2s ease;
    }
    .social-btn:hover {
      transform: scale(1.16);
      filter: drop-shadow(0 0 7px var(--accent));
    }

    .stack-card {
      background-color: var(--stack-bg);
      border: 1px solid var(--accent-border);
      transition: background-color 0.35s ease, border-color 0.35s ease;
    }

    .studio-bar {
      background-color: var(--studio-bg);
      border: 1px solid var(--studio-border);
      transition: background-color 0.35s ease, border-color 0.35s ease;
    }

    /* Custom Range Sliders */
    input[type="range"].cyber-slider {
      -webkit-appearance: none;
      appearance: none;
      height: 4px;
      border-radius: 9999px;
      background: var(--accent-border);
      outline: none;
    }
    input[type="range"].cyber-slider::-webkit-slider-thumb {
      -webkit-appearance: none;
      appearance: none;
      width: 14px;
      height: 14px;
      border-radius: 9999px;
      background: var(--accent-bright);
      border: 2px solid #0a0f1c;
      cursor: pointer;
      box-shadow: 0 0 8px var(--accent);
    }
    input[type="range"].cyber-slider::-moz-range-thumb {
      width: 14px;
      height: 14px;
      border-radius: 9999px;
      background: var(--accent-bright);
      border: 2px solid #0a0f1c;
      cursor: pointer;
    }

    @keyframes entryFade {
      from { opacity: 0; transform: translateY(4px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .term-entry {
      animation: entryFade 0.2s ease-out forwards;
    }
  </style>
</head>
<body class="ambient-bg min-h-screen w-full flex flex-col items-center justify-center p-2 sm:p-4 md:p-5 font-sans antialiased">

  <!-- Hidden file input for photo uploads -->
  <input id="photoFileInput" type="file" accept="image/png,image/jpeg,image/webp" class="hidden" />

  <!-- =====================================================================
       1. MAIN LIVE PORTFOLIO UI (CYBERPUNK MACOS WINDOW)
       ===================================================================== -->
  <div id="cyberWindow" class="cyber-window relative w-full max-w-[1180px] rounded-2xl overflow-hidden flex flex-col">

    <!-- TOP PERIMETER DASHED RAIL + GLOWING SEGMENTS -->
    <div class="pointer-events-none absolute top-2.5 left-5 right-5 h-[2px] rail-h z-10">
      <span class="neon-seg seg-primary w-9 h-[2.5px] -top-[0.5px] left-[16%] pulse-1"></span>
      <span class="neon-seg seg-secondary w-9 h-[2.5px] -top-[0.5px] left-[33%] pulse-2"></span>
      <span class="neon-seg seg-primary w-10 h-[2.5px] -top-[0.5px] left-[50%] pulse-3"></span>
      <span class="neon-seg seg-secondary w-9 h-[2.5px] -top-[0.5px] left-[67%] pulse-1"></span>
      <span class="neon-seg seg-primary w-9 h-[2.5px] -top-[0.5px] left-[84%] pulse-2"></span>
      <span class="neon-seg seg-primary w-12 h-[2px] -top-[0.5px] glide-top"></span>
    </div>

    <!-- BOTTOM PERIMETER DASHED RAIL + GLOWING SEGMENTS -->
    <div class="pointer-events-none absolute bottom-2.5 left-5 right-5 h-[2px] rail-h z-10">
      <span class="neon-seg seg-secondary w-8 h-[2.5px] -top-[0.5px] left-[6%] pulse-2"></span>
      <span class="neon-seg seg-primary w-9 h-[2.5px] -top-[0.5px] left-[22%] pulse-1"></span>
      <span class="neon-seg seg-secondary w-9 h-[2.5px] -top-[0.5px] left-[38%] pulse-3"></span>
      <span class="neon-seg seg-primary w-10 h-[2.5px] -top-[0.5px] left-[54%] pulse-2"></span>
      <span class="neon-seg seg-secondary w-9 h-[2.5px] -top-[0.5px] left-[70%] pulse-1"></span>
      <span class="neon-seg seg-primary w-9 h-[2.5px] -top-[0.5px] left-[86%] pulse-3"></span>
      <span class="neon-seg seg-secondary w-12 h-[2px] -top-[0.5px] glide-bottom"></span>
    </div>

    <!-- SIDE VERTICAL RAILS -->
    <div class="pointer-events-none absolute left-2 top-8 bottom-8 w-[2px] rail-v z-10 hidden sm:block">
      <span class="neon-seg seg-primary w-[3px] h-4 -left-[0.5px] top-[34%] pulse-2"></span>
    </div>
    <div class="pointer-events-none absolute right-2 top-8 bottom-8 w-[2px] rail-v z-10 hidden sm:block">
      <span class="neon-seg seg-secondary w-[3px] h-4 -left-[0.5px] top-[62%] pulse-1"></span>
    </div>

    <!-- TOP WINDOW BAR -->
    <header class="relative z-20 flex items-center justify-between px-5 sm:px-7 pt-5 pb-3 select-none">
      <!-- Left: macOS Traffic Light Dots -->
      <div class="flex items-center gap-2.5">
        <button id="btnTrafficReset" title="Reset Terminal" aria-label="Reset Terminal"
          class="group w-3.5 h-3.5 rounded-full bg-[#ff5f56] hover:brightness-110 transition-transform hover:scale-110 flex items-center justify-center shadow-[0_0_8px_rgba(255,95,86,0.45)]">
          <span class="opacity-0 group-hover:opacity-100 text-[9px] font-bold text-black/75 leading-none">×</span>
        </button>
        <button id="btnTrafficMin" title="Toggle Portrait Pane" aria-label="Toggle Portrait Pane"
          class="group w-3.5 h-3.5 rounded-full bg-[#ffbd2e] hover:brightness-110 transition-transform hover:scale-110 flex items-center justify-center shadow-[0_0_8px_rgba(255,189,46,0.45)]">
          <span class="opacity-0 group-hover:opacity-100 text-[9px] font-bold text-black/75 leading-none">−</span>
        </button>
        <button id="btnTrafficMax" title="Toggle Wide View" aria-label="Toggle Wide View"
          class="group w-3.5 h-3.5 rounded-full bg-[#27c93f] hover:brightness-110 transition-transform hover:scale-110 flex items-center justify-center shadow-[0_0_8px_rgba(39,201,63,0.45)]">
          <span class="opacity-0 group-hover:opacity-100 text-[8px] font-bold text-black/75 leading-none">+</span>
        </button>
        <span class="hidden md:inline-block ml-3 font-mono text-[11px] tracking-[0.18em] uppercase opacity-70 accent-text">
          SONAI_OS // LIVE_STUDIO
        </span>
      </div>

      <!-- Right: Minimalist Cybernetic Icons (Reset, Split/Focus, Dark/Light Mode) -->
      <div class="flex items-center gap-3.5 sm:gap-5 pr-1">
        <!-- Reset Terminal -->
        <button id="btnResetTerminal" title="Reset Terminal Session" aria-label="Reset Terminal Session"
          class="p-1.5 rounded-lg accent-text opacity-85 hover:opacity-100 hover:bg-amber-500/10 transition-all">
          <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
            <rect x="3" y="3" width="18" height="18" rx="4"></rect>
            <line x1="12" y1="8" x2="12" y2="16"></line>
            <line x1="8" y1="12" x2="16" y2="12"></line>
          </svg>
        </button>

        <!-- Split / Focus Toggle -->
        <button id="btnSplitToggle" title="Toggle Split / Focus View" aria-label="Toggle Split or Focus View"
          class="p-1.5 rounded-lg accent-text opacity-85 hover:opacity-100 hover:bg-amber-500/10 transition-all">
          <svg class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
            <rect x="3" y="4" width="18" height="16" rx="3"></rect>
            <line x1="3" y1="9" x2="21" y2="9"></line>
            <line x1="11" y1="9" x2="11" y2="20"></line>
          </svg>
        </button>

        <!-- Dark / Light Mode Toggle -->
        <button id="btnThemeToggle" title="Toggle Dark / Light Mode" aria-label="Toggle Dark or Light Mode"
          class="flex items-center gap-1.5 px-2.5 py-1 rounded-lg border transition-all font-mono text-[10px] uppercase tracking-wider accent-text"
          style="border-color: var(--accent-border); background-color: var(--accent-soft);">
          <svg class="w-4 h-4 hidden dark:block" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
            <circle cx="8" cy="12" r="4"></circle>
            <circle cx="16" cy="12" r="4" fill="currentColor" fill-opacity="0.3"></circle>
          </svg>
          <svg class="w-4 h-4 block dark:hidden" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8">
            <circle cx="8" cy="12" r="4" fill="currentColor" fill-opacity="0.3"></circle>
            <circle cx="16" cy="12" r="4"></circle>
          </svg>
          <span id="themeToggleText" class="hidden sm:inline">Dark</span>
        </button>
      </div>
    </header>

    <!-- DUAL-PANE MAIN CONTENT -->
    <main class="relative z-20 flex flex-col lg:flex-row gap-4 sm:gap-5 px-4 sm:px-6 pb-6 pt-1 flex-1">

      <!-- =================================================================
           LEFT PANE: INTERACTIVE DOT-MATRIX CRT PORTRAIT
           ================================================================= -->
      <section id="leftPane" class="cyber-pane w-full lg:w-[44%] rounded-2xl p-3 flex flex-col justify-between transition-all duration-300">
        <div class="cyber-tab"></div>

        <!-- Always-Dark CRT Screen Container -->
        <div id="crtDropZone" class="crt-box relative w-full h-[380px] sm:h-[460px] lg:h-[515px] rounded-xl overflow-hidden border transition-all"
             style="border-color: var(--accent-border);">
          <!-- Top Accent Gradient Line -->
          <div class="pointer-events-none absolute top-0 left-0 right-0 h-[2px] z-20"
               style="background: linear-gradient(90deg, var(--accent-bright), #3b82f6, var(--accent-bright));"></div>

          <!-- Interactive Dot-Matrix Canvas -->
          <canvas id="portraitCanvas" class="absolute inset-0 w-full h-full block cursor-crosshair"></canvas>

          <!-- CRT Scanlines Overlay -->
          <div class="crt-scanlines absolute inset-0 z-10"></div>

          <!-- Unobtrusive Top-Right Upload Photo Overlay Button -->
          <div class="absolute top-3 right-3 z-20 flex items-center gap-1.5">
 
