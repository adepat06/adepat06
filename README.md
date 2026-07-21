<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1180 610" width="100%" height="100%">
  <defs>
    <!-- Dark Mode Color Palette & Gradients -->
    <linearGradient id="bgGlow" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#1e1b4b" stop-opacity="0.6"/>
      <stop offset="50%" stop-color="#030712" stop-opacity="1"/>
      <stop offset="100%" stop-color="#064e3b" stop-opacity="0.4"/>
    </linearGradient>

    <linearGradient id="aurora" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#7c3aed" stop-opacity="0.3">
        <animate attributeName="stop-color" values="#7c3aed;#22d3ee;#10b981;#7c3aed" dur="12s" repeatCount="indefinite"/>
      </stop>
      <stop offset="50%" stop-color="#22d3ee" stop-opacity="0.2">
        <animate attributeName="stop-color" values="#22d3ee;#10b981;#7c3aed;#22d3ee" dur="12s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#10b981" stop-opacity="0.3">
        <animate attributeName="stop-color" values="#10b981;#7c3aed;#22d3ee;#10b981" dur="12s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <linearGradient id="accentGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7c3aed"/>
      <stop offset="50%" stop-color="#22d3ee"/>
      <stop offset="100%" stop-color="#10b981"/>
    </linearGradient>

    <linearGradient id="borderShimmer" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#7c3aed" stop-opacity="0.8"/>
      <stop offset="50%" stop-color="#ffffff" stop-opacity="0.1"/>
      <stop offset="100%" stop-color="#22d3ee" stop-opacity="0.8"/>
    </linearGradient>

    <linearGradient id="asciiGrad" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" stop-color="#a855f7">
        <animate attributeName="stop-color" values="#a855f7;#06b6d4;#10b981;#a855f7" dur="8s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#22d3ee">
        <animate attributeName="stop-color" values="#22d3ee;#10b981;#a855f7;#22d3ee" dur="8s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <!-- Glass Glow Filter -->
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="8" result="blur"/>
      <feComposite in="SourceGraphic" in2="blur" operator="over"/>
    </filter>
    <filter id="softGlow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feComposite in="SourceGraphic" in2="blur" operator="over"/>
    </filter>

    <style>
      .font-mono { font-family: 'Fira Code', 'Courier New', monospace; }
      .font-sans { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; }
      .text-primary { fill: #F8FAFC; }
      .text-secondary { fill: #94A3B8; }
      .text-muted { fill: #64748B; }
      .text-accent { fill: #22D3EE; }
      .glass-panel { fill: #0F172A; fill-opacity: 0.75; stroke: rgba(255, 255, 255, 0.1); stroke-width: 1.5; }
      .pill-bg { fill: rgba(30, 41, 59, 0.7); stroke: rgba(56, 189, 248, 0.25); stroke-width: 1; }
      
      /* Hover scale simulation via animation */
      .pill { transition: all 0.3s ease; }
      
      /* Typewriter Animation Keyframes */
      @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
      .cursor { animation: blink 0.8s infinite; fill: #22D3EE; }

      @keyframes floatSlow { 0%, 100% { transform: translateY(0px); } 50% { transform: translateY(-6px); } }
      .floating { animation: floatSlow 5s ease-in-out infinite; }

      @keyframes scanline { 0% { transform: translateY(-100%); } 100% { transform: translateY(610px); } }
      .scanline-line { animation: scanline 8s linear infinite; }
    </style>
  </defs>

  <!-- Canvas Base -->
  <rect width="1180" height="610" rx="20" fill="#030712"/>
  <rect width="1180" height="610" rx="20" fill="url(#bgGlow)"/>

  <!-- Animated Ambient Aurora Light Bubbles -->
  <circle cx="200" cy="150" r="250" fill="url(#aurora)" filter="url(#glow)" opacity="0.5">
    <animateTransform attributeName="transform" type="translate" values="0,0; 40,30; 0,0" dur="10s" repeatCount="indefinite"/>
  </circle>
  <circle cx="950" cy="450" r="300" fill="url(#aurora)" filter="url(#glow)" opacity="0.4">
    <animateTransform attributeName="transform" type="translate" values="0,0; -50,-40; 0,0" dur="14s" repeatCount="indefinite"/>
  </circle>

  <!-- Animated Background Particles -->
  <g opacity="0.3">
    <circle cx="120" cy="80" r="1.5" fill="#22d3ee"><animate attributeName="opacity" values="0.2;1;0.2" dur="3s" repeatCount="indefinite"/></circle>
    <circle cx="450" cy="180" r="1" fill="#7c3aed"><animate attributeName="opacity" values="1;0.2;1" dur="4s" repeatCount="indefinite"/></circle>
    <circle cx="850" cy="100" r="2" fill="#10b981"><animate attributeName="opacity" values="0.3;0.9;0.3" dur="2.5s" repeatCount="indefinite"/></circle>
    <circle cx="1050" cy="300" r="1.5" fill="#38bdf8"><animate attributeName="opacity" values="0.1;0.8;0.1" dur="3.5s" repeatCount="indefinite"/></circle>
    <circle cx="300" cy="520" r="2" fill="#a855f7"><animate attributeName="opacity" values="0.8;0.2;0.8" dur="4.5s" repeatCount="indefinite"/></circle>
  </g>

  <!-- Border Shimmer Frame -->
  <rect x="1.5" y="1.5" width="1177" height="607" rx="18.5" fill="none" stroke="url(#borderShimmer)" stroke-width="1.5" opacity="0.7"/>

  <!-- ================= LEFT PANEL: TERMINAL ASCII (38%) ================= -->
  <g transform="translate(20, 20)">
    <!-- Glass Container -->
    <rect width="428" height="570" rx="14" class="glass-panel"/>
    
    <!-- Window Header -->
    <path d="M 0 14 A 14 14 0 0 1 14 0 L 414 0 A 14 14 0 0 1 428 14 L 428 36 L 0 36 Z" fill="rgba(255, 255, 255, 0.03)"/>
    <circle cx="20" cy="18" r="5" fill="#EF4444" opacity="0.8"/>
    <circle cx="36" cy="18" r="5" fill="#F59E0B" opacity="0.8"/>
    <circle cx="52" cy="18" r="5" fill="#10B981" opacity="0.8"/>
    <text x="214" y="22" class="font-mono text-muted" font-size="11" text-anchor="middle" opacity="0.7">adelin@cyber-terminal:~</text>

    <!-- Animated ASCII Cyber Portrait -->
    <g transform="translate(30, 65)" class="floating">
      <g fill="url(#asciiGrad)" class="font-mono" font-size="9.5" letter-spacing="1.2">
        <!-- Line-by-line progressive appearance using SMIL -->
        <text x="0" y="20" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.2s" fill="freeze"/>
          .········································.
        </text>
        <text x="0" y="34" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.4s" fill="freeze"/>
          :  ______  _____   ______  _       _____ :
        </text>
        <text x="0" y="48" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.6s" fill="freeze"/>
          : /  __  \/  __  \/  ____/| |     /  ___|:
        </text>
        <text x="0" y="62" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="0.8s" fill="freeze"/>
          : |  | |  |  | |  |  |__   | |    |  |__  :
        </text>
        <text x="0" y="76" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="1.0s" fill="freeze"/>
          : |  |_|  |  |_|  |  __|   | |___ |  __|  :
        </text>
        <text x="0" y="90" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="1.2s" fill="freeze"/>
          : \______/\______/|_|      |_____/|_____| :
        </text>
        <text x="0" y="104" opacity="0">
          <animate attributeName="opacity" to="0.9" dur="0.1s" begin="1.4s" fill="freeze"/>
          '········································'
        </text>
        
        <!-- Cyber Visor / Hooded Developer Graphic Vectorized ASCII Structure -->
        <text x="0" y="130" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="1.6s" fill="freeze"/>            .---|'''''''''|---.            </text>
        <text x="0" y="144" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="1.7s" fill="freeze"/>         .-'                   '-.         </text>
        <text x="0" y="158" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="1.8s" fill="freeze"/>       .'  ___________________  '.       </text>
        <text x="0" y="172" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="1.9s" fill="freeze"/>      /   /   [CYBER-DEV]     \   \      </text>
        <text x="0" y="186" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.0s" fill="freeze"/>     |   |   > AI &amp; JAVA_     |   |     </text>
        <text x="0" y="200" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.1s" fill="freeze"/>     |   |  _________________ |   |     </text>
        <text x="0" y="214" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.2s" fill="freeze"/>     |   | [=== 101010101 ===]|   |     </text>
        <text x="0" y="228" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.3s" fill="freeze"/>      \   \___________________/   /      </text>
        <text x="0" y="242" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.4s" fill="freeze"/>       '.                       .'       </text>
        <text x="0" y="256" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.5s" fill="freeze"/>         '-._________________.-'         </text>
        <text x="0" y="270" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.6s" fill="freeze"/>           |                 |           </text>
        <text x="0" y="284" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.7s" fill="freeze"/>          /                   \          </text>
        <text x="0" y="298" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.8s" fill="freeze"/>         /_____________________\         </text>
        <text x="0" y="312" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="2.9s" fill="freeze"/>        [=======================]        </text>
        <text x="0" y="326" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="3.0s" fill="freeze"/>        |  ADELIN PATRICIA V2.6 |        </text>
        <text x="0" y="340" opacity="0"><animate attributeName="opacity" to="0.85" dur="0.1s" begin="3.1s" fill="freeze"/>        '-----------------------'        </text>
      </g>
    </g>

    <!-- Terminal Status Footer -->
    <rect x="20" y="515" width="388" height="36" rx="8" fill="rgba(255, 255, 255, 0.02)" stroke="rgba(255, 255, 255, 0.05)"/>
    <circle cx="36" cy="533" r="4" fill="#10b981"><animate attributeName="opacity" values="0.3;1;0.3" dur="2s" repeatCount="indefinite"/></circle>
    <text x="48" y="537" class="font-mono text-secondary" font-size="11">SYSTEM: ONLINE</text>
    <text x="390" y="537" class="font-mono text-muted" font-size="11" text-anchor="end">LOC: CHENNAI</text>
  </g>

  <!-- CRT Scanline effect over Left Panel -->
  <g clip-path="url(#leftPanelClip)">
    <line x1="20" y1="0" x2="448" y2="0" stroke="rgba(34, 211, 238, 0.15)" stroke-width="3" class="scanline-line"/>
  </g>

  <!-- ================= RIGHT PANEL: HERO CONTENT (62%) ================= -->
  <g transform="translate(468, 20)">
    <!-- Main Glass Window -->
    <rect width="692" height="570" rx="14" class="glass-panel"/>
    
    <!-- Window Header -->
    <path d="M 0 14 A 14 14 0 0 1 14 0 L 678 0 A 14 14 0 0 1 692 14 L 692 36 L 0 36 Z" fill="rgba(255, 255, 255, 0.03)"/>
    <circle cx="20" cy="18" r="5" fill="#EF4444" opacity="0.8"/>
    <circle cx="36" cy="18" r="5" fill="#F59E0B" opacity="0.8"/>
    <circle cx="52" cy="18" r="5" fill="#10B981" opacity="0.8"/>
    <text x="346" y="22" class="font-mono text-muted" font-size="11" text-anchor="middle" opacity="0.7">adelin-patricia — zsh — 1180x610</text>

    <!-- CONTENT SECTION -->
    <g transform="translate(35, 60)">
      
      <!-- Greeting & Name -->
      <g>
        <text x="0" y="20" class="font-sans text-secondary" font-size="18" font-weight="500">Hi 👋</text>
        <text x="0" y="55" class="font-sans text-primary" font-size="34" font-weight="800" letter-spacing="-0.5">I'm Adelin Patricia</text>
      </g>

      <!-- Animated Typing Roles (Infinite Typewriter Effect) -->
      <g transform="translate(0, 82)">
        <rect x="0" y="0" width="620" height="38" rx="8" fill="rgba(15, 23, 42, 0.6)" stroke="rgba(255, 255, 255, 0.05)"/>
        <text x="14" y="24" class="font-mono text-accent" font-size="14" font-weight="600">&gt;</text>
        
        <!-- Infinite Rotating Roles using SMIL switchable opacity text strings -->
        <g class="font-mono text-primary" font-size="13" font-weight="500">
          <!-- Role 1 -->
          <text x="32" y="24" opacity="0">
            Full Stack Java Developer
            <animate attributeName="opacity" values="0;1;1;0;0" keyTimes="0;0.05;0.18;0.22;1" dur="18s" repeatCount="indefinite"/>
          </text>
          <!-- Role 2 -->
          <text x="32" y="24" opacity="0">
            Exploring AI &amp; Machine Learning
            <animate attributeName="opacity" values="0;0;1;1;0;0" keyTimes="0;0.22;0.27;0.40;0.44;1" dur="18s" repeatCount="indefinite"/>
          </text>
          <!-- Role 3 -->
          <text x="32" y="24" opacity="0">
            GSSoC 2026 Contributor ✨
            <animate attributeName="opacity" values="0;0;1;1;0;0" keyTimes="0;0.44;0.49;0.60;0.64;1" dur="18s" repeatCount="indefinite"/>
          </text>
          <!-- Role 4 -->
          <text x="32" y="24" opacity="0">
            Open Source Contributor
            <animate attributeName="opacity" values="0;0;1;1;0;0" keyTimes="0;0.64;0.68;0.78;0.82;1" dur="18s" repeatCount="indefinite"/>
          </text>
          <!-- Role 5 -->
          <text x="32" y="24" opacity="0">
            B.Tech Information Technology Student
            <animate attributeName="opacity" values="0;0;1;1;0" keyTimes="0;0.82;0.86;0.96;1" dur="18s" repeatCount="indefinite"/>
          </text>
        </g>

        <!-- Blinking Cursor -->
        <rect x="360" y="10" width="8" height="18" fill="#22d3ee" class="cursor"/>
      </g>

      <!-- Info Grid (Sequential Reveal) -->
      <g transform="translate(0, 140)">
        <!-- Location & Edu -->
        <g transform="translate(0, 0)">
          <text x="0" y="15" font-size="14">📍</text>
          <text x="24" y="14" class="font-sans text-secondary" font-size="13" font-weight="500">Chennai, India</text>
          
          <text x="200" y="15" font-size="14">🎓</text>
          <text x="224" y="14" class="font-sans text-secondary" font-size="13" font-weight="500">B.Tech — Information Technology</text>
        </g>

        <!-- Current Focus -->
        <g transform="translate(0, 38)">
          <text x="0" y="15" font-size="14">💻</text>
          <text x="24" y="14" class="font-sans text-primary" font-size="13" font-weight="600">Current Focus:</text>
          <text x="130" y="14" class="font-sans text-secondary" font-size="13">Learning Full Stack Java &amp; AI through real-world projects.</text>
        </g>

        <!-- Portfolio & Email -->
        <g transform="translate(0, 72)">
          <text x="0" y="15" font-size="14">🌐</text>
          <text x="24" y="14" class="font-sans text-muted" font-size="13">Portfolio: <tspan fill="#94A3B8">Coming Soon</tspan></text>

          <text x="200" y="15" font-size="14">📧</text>
          <text x="224" y="14" class="font-sans text-accent" font-size="13">adelinpatricia06@gmail.com</text>
        </g>
      </g>

      <!-- Divider -->
      <line x1="0" y1="242" x2="622" y2="242" stroke="rgba(255, 255, 255, 0.08)" stroke-width="1"/>

      <!-- Skills Glass Pills -->
      <g transform="translate(0, 258)">
        <text x="0" y="14" class="font-sans text-primary" font-size="13" font-weight="700" letter-spacing="0.5">SKILLS &amp; TECHNOLOGIES</text>
        
        <g transform="translate(0, 26)" class="font-mono" font-size="11">
          <!-- Row 1 -->
          <g transform="translate(0,0)"><rect width="52" height="24" rx="12" class="pill-bg"/><text x="26" y="16" fill="#F8FAFC" text-anchor="middle">Java</text></g>
          <g transform="translate(58,0)"><rect width="36" height="24" rx="12" class="pill-bg"/><text x="18" y="16" fill="#F8FAFC" text-anchor="middle">C</text></g>
          <g transform="translate(100,0)"><rect width="48" height="24" rx="12" class="pill-bg"/><text x="24" y="16" fill="#F8FAFC" text-anchor="middle">C++</text></g>
          <g transform="translate(154,0)"><rect width="60" height="24" rx="12" class="pill-bg"/><text x="30" y="16" fill="#F8FAFC" text-anchor="middle">HTML5</text></g>
          <g transform="translate(220,0)"><rect width="52" height="24" rx="12" class="pill-bg"/><text x="26" y="16" fill="#F8FAFC" text-anchor="middle">CSS3</text></g>
          <g transform="translate(278,0)"><rect width="82" height="24" rx="12" class="pill-bg"/><text x="41" y="16" fill="#F8FAFC" text-anchor="middle">JavaScript</text></g>
          <g transform="translate(366,0)"><rect width="46" height="24" rx="12" class="pill-bg"/><text x="23" y="16" fill="#F8FAFC" text-anchor="middle">SQL</text></g>
          <g transform="translate(418,0)"><rect width="42" height="24" rx="12" class="pill-bg"/><text x="21" y="16" fill="#F8FAFC" text-anchor="middle">Git</text></g>
          <g transform="translate(466,0)"><rect width="62" height="24" rx="12" class="pill-bg"/><text x="31" y="16" fill="#F8FAFC" text-anchor="middle">GitHub</text></g>
          <g transform="translate(534,0)"><rect width="72" height="24" rx="12" class="pill-bg"/><text x="36" y="16" fill="#F8FAFC" text-anchor="middle">VS Code</text></g>

          <!-- Row 2 -->
          <g transform="translate(0,32)"><rect width="118" height="24" rx="12" class="pill-bg"/><text x="59" y="16" fill="#38BDF8" text-anchor="middle">Full Stack Java</text></g>
          <g transform="translate(124,32)"><rect width="38" height="24" rx="12" class="pill-bg"/><text x="19" y="16" fill="#38BDF8" text-anchor="middle">AI</text></g>
          <g transform="translate(168,32)"><rect width="120" height="24" rx="12" class="pill-bg"/><text x="60" y="16" fill="#F8FAFC" text-anchor="middle">Problem Solving</text></g>
          <g transform="translate(294,32)"><rect width="84" height="24" rx="12" class="pill-bg"/><text x="42" y="16" fill="#F8FAFC" text-anchor="middle">REST APIs</text></g>
          <g transform="translate(384,32)"><rect width="50" height="24" rx="12" class="pill-bg"/><text x="25" y="16" fill="#F8FAFC" text-anchor="middle">OOP</text></g>
        </g>
      </g>

      <!-- Open Source Highlight Badge & Social Icons -->
      <g transform="translate(0, 370)">
        <!-- Highlight GSSoC Badge -->
        <rect width="260" height="42" rx="10" fill="url(#accentGrad)" opacity="0.15"/>
        <rect width="260" height="42" rx="10" fill="none" stroke="url(#accentGrad)" stroke-width="1.5"/>
        <text x="16" y="26" class="font-sans text-primary" font-size="13" font-weight="700">✨ GSSoC 2026 Contributor</text>

        <!-- Social Quick Links -->
        <g transform="translate(280, 0)">
          <!-- GitHub Icon Link -->
          <a href="https://github.com/adepat06" target="_blank">
            <g transform="translate(0,0)">
              <circle cx="21" cy="21" r="20" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)"/>
              <path d="M21 11C15.47 11 11 15.47 11 21C11 25.42 13.87 29.17 17.84 30.5C18.34 30.59 18.52 30.28 18.52 30.02C18.52 29.78 18.51 29.16 18.51 28.31C15.73 28.91 15.14 26.97 15.14 26.97 C14.69 25.81 14.03 25.5 14.03 25.5C13.12 24.88 14.1 24.9 14.1 24.9C15.11 24.97 15.64 25.94 15.64 25.94C16.54 27.48 18 27.03 18.57 26.78C18.66 26.13 18.92 25.68 19.21 25.43C16.99 25.18 14.65 24.32 14.65 20.49C14.65 19.4 15.04 18.5 15.68 17.8C15.58 17.55 15.24 16.53 15.78 15.16C15.78 15.16 16.62 14.89 18.53 16.18C19.33 15.96 20.18 15.85 21.03 15.85C21.88 15.85 22.73 15.96 23.53 16.18C25.44 14.89 26.28 15.16 26.28 15.16C26.82 16.53 26.48 17.55 26.38 17.8C27.02 18.5 27.41 19.4 27.41 20.49C27.41 24.33 25.06 25.18 22.83 25.43C23.2 25.75 23.52 26.38 23.52 27.34C23.52 28.72 23.51 29.84 23.51 30.02C23.51 30.29 23.69 30.6 24.2 30.5C28.16 29.17 31 25.42 31 21C31 15.47 26.53 11 21 11Z" fill="#F8FAFC"/>
            </g>
          </a>

          <!-- LinkedIn Icon Link -->
          <a href="https://www.linkedin.com/in/adelin-patricia/" target="_blank">
            <g transform="translate(52,0)">
              <circle cx="21" cy="21" r="20" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)"/>
              <path d="M16 14C14.9 14 14 14.9 14 16V26C14 27.1 14.9 28 16 28H26C27.1 28 28 27.1 28 26V16C28 14.9 27.1 14 26 14H16ZM17.5 17.5C18.1 17.5 18.5 17.9 18.5 18.5C18.5 19.1 18.1 19.5 17.5 19.5C16.9 19.5 16.5 19.1 16.5 18.5C16.5 17.9 16.9 17.5 17.5 17.5ZM16.5 21H18.5V25.5H16.5V21ZM20 21H21.8V21.6C22.1 21.1 22.7 20.8 23.4 20.8C25 20.8 25.5 21.8 25.5 23.4V25.5H23.5V23.7C23.5 22.9 23.3 22.3 22.5 22.3C21.7 22.3 21.5 22.9 21.5 23.7V25.5H19.5V21H20Z" fill="#38BDF8"/>
            </g>
          </a>

          <!-- Email Icon Link -->
          <a href="mailto:adelinpatricia06@gmail.com">
            <g transform="translate(104,0)">
              <circle cx="21" cy="21" r="20" fill="rgba(255,255,255,0.05)" stroke="rgba(255,255,255,0.1)"/>
              <path d="M14 16C13.4 16 13 16.4 13 17V25C13 25.6 13.4 26 14 26H28C28.6 26 29 25.6 29 25V17C29 16.4 28.6 16 28 16H14ZM21 21.8L15 17.5H27L21 21.8ZM14.5 24.5V18.2L21 22.8L27.5 18.2V24.5H14.5Z" fill="#10B981"/>
            </g>
          </a>
        </g>
      </g>

      <!-- Achievement Badges (12 Mini Glass Badges Layout) -->
      <g transform="translate(0, 430)">
        <text x="0" y="10" class="font-sans text-muted" font-size="11" font-weight="600" letter-spacing="0.5">ACHIEVEMENTS &amp; RECOGNITION</text>
        <g transform="translate(0, 20)">
          <!-- Row of 12 badges -->
          <g transform="translate(0,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#A855F7" font-size="10" text-anchor="middle">🏆 '26</text></g>
          <g transform="translate(50,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#22D3EE" font-size="10" text-anchor="middle">⚡ Top</text></g>
          <g transform="translate(100,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#10B981" font-size="10" text-anchor="middle">🌱 OS</text></g>
          <g transform="translate(150,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#F59E0B" font-size="10" text-anchor="middle">🔥 100</text></g>
          <g transform="translate(200,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#EC4899" font-size="10" text-anchor="middle">🤖 AI</text></g>
          <g transform="translate(250,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#3B82F6" font-size="10" text-anchor="middle">☕ Java</text></g>
          <g transform="translate(300,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#6366F1" font-size="10" text-anchor="middle">🚀 Git</text></g>
          <g transform="translate(350,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#14B8A6" font-size="10" text-anchor="middle">💻 Dev</text></g>
          <g transform="translate(400,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#8B5CF6" font-size="10" text-anchor="middle">🎓 IT</text></g>
          <g transform="translate(450,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#F43F5E" font-size="10" text-anchor="middle">⭐ PR</text></g>
          <g transform="translate(500,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#0EA5E9" font-size="10" text-anchor="middle">🌐 Web</text></g>
          <g transform="translate(550,0)"><rect width="44" height="24" rx="6" fill="rgba(255,255,255,0.03)" stroke="rgba(255,255,255,0.08)"/><text x="22" y="16" fill="#84CC16" font-size="10" text-anchor="middle">💎 Pro</text></g>
        </g>
      </g>

    </g>
  </g>
</svg>
