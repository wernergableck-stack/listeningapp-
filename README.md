# listeningapp-<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LBS Theresienfeld - Listening Exam Trainer (Großhandelskaufmann 3. Lehrjahr)</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            mono: ['JetBrains Mono', 'monospace'],
          },
          colors: {
            brand: {
              50: '#f0f7ff',
              100: '#e0effe',
              500: '#0284c7',
              600: '#0369a1',
              700: '#075985',
              800: '#0c4a6e',
              900: '#082f49',
            }
          }
        }
      }
    }
  </script>
  <style>
    /* Custom scrollbar and smooth transitions */
    ::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    ::-webkit-scrollbar-track {
      background: #f1f5f9;
    }
    ::-webkit-scrollbar-thumb {
      background: #cbd5e1;
      border-radius: 9999px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #94a3b8;
    }
    .pulse-ring {
      animation: pulse-ring 1.8s cubic-bezier(0.215, 0.61, 0.355, 1) infinite;
    }
    @keyframes pulse-ring {
      0% { transform: scale(0.95); opacity: 0.8; }
      50% { transform: scale(1.1); opacity: 0.3; }
      100% { transform: scale(0.95); opacity: 0.8; }
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 antialiased font-sans min-h-screen flex flex-col justify-between">

  <header class="bg-white border-b border-slate-200 sticky top-0 z-40 shadow-sm">
    <div class="max-w-6xl mx-auto px-4 py-3 sm:px-6 flex flex-wrap items-center justify-between gap-3">
      <div class="flex items-center space-x-3">
        <div class="h-10 w-10 rounded-xl bg-gradient-to-tr from-sky-600 to-indigo-700 flex items-center justify-center text-white shadow-md font-bold text-lg">
          LT
        </div>
        <div>
          <div class="flex items-center gap-2">
            <h1 class="text-base sm:text-lg font-bold text-slate-900 leading-tight">LBS Theresienfeld</h1>
            <span class="inline-flex items-center px-2 py-0.5 rounded text-xs font-semibold bg-sky-100 text-sky-800 border border-sky-200">
              GERS B1/B1+
            </span>
          </div>
          <p class="text-xs text-slate-500">Großhandelskaufmann 3. Klasse &bull; Abschluss-Schularbeit Listening Trainer</p>
        </div>
      </div>

      <!-- Quick Status Badges -->
      <div class="flex items-center gap-3">
        <div class="bg-slate-100 border border-slate-200 rounded-lg px-3 py-1.5 flex items-center gap-2 text-xs font-medium text-slate-700">
          <svg class="w-4 h-4 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
          </svg>
          <span id="headerCandidate">Kandidat: Julian</span>
        </div>
        <div id="examModeBadge" class="bg-amber-50 border border-amber-200 text-amber-800 rounded-lg px-3 py-1.5 text-xs font-semibold flex items-center gap-1.5">
          <span class="w-2 h-2 rounded-full bg-amber-500 animate-ping"></span>
          Prüfungsmodus (2x Anhören)
        </div>
      </div>
    </div>
  </header>

  <main class="max-w-6xl mx-auto px-4 py-6 sm:px-6 w-full flex-1">
    
    <!-- Hero / Info Banner -->
    <div class="bg-gradient-to-r from-slate-900 via-sky-950 to-indigo-950 text-white rounded-2xl p-5 sm:p-6 mb-8 shadow-xl relative overflow-hidden">
      <div class="absolute -right-8 -bottom-8 opacity-10 pointer-events-none">
        <svg class="w-64 h-64" fill="currentColor" viewBox="0 0 24 24">
          <path d="M12 3v10.55c-.59-.34-1.27-.55-2-.55-2.21 0-4 1.79-4 4s1.79 4 4 4 4-1.79 4-4V7h4V3h-6z"/>
        </svg>
      </div>

      <div class="relative z-10 max-w-3xl">
        <div class="inline-flex items-center gap-2 bg-white/10 backdrop-blur-md px-2.5 py-1 rounded-full text-xs font-medium text-sky-200 mb-2">
          <span>🎧 B2B International Listening Practice</span>
          <span>&bull;</span>
          <span>4 Welt-Akzente</span>
        </div>
        <h2 class="text-xl sm:text-2xl font-extrabold tracking-tight mb-2">
          Offizielle Reifeprüfungs- & Schularbeits-Simulation
        </h2>
        <p class="text-sm text-slate-300 leading-relaxed mb-4">
          Jedes Audiobeispiel simuliert eine authentische B2B-Situation im Großhandel (Mumbai, Chicago, London, Melbourne). 
          Gemäß den Prüfungsrichtlinien darf jede Hörsequenz <strong>maximal zweimal (2x)</strong> abgespielt werden. 
          Die Transkripte und didaktischen Erklärungen werden erst nach Abgabe freigeschaltet.
        </p>

        <!-- Global Voice & Audio Engine Diagnostics -->
        <div class="bg-white/10 backdrop-blur-md rounded-xl p-3 text-xs flex flex-wrap items-center justify-between gap-3 border border-white/10">
          <div class="flex items-center gap-2">
            <svg class="w-4 h-4 text-sky-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 100-6 3 3 0 000 6z"/>
            </svg>
            <span class="text-slate-200 font-medium">Sprachausgabe-System:</span>
            <span id="ttsStatusText" class="text-amber-300 font-medium">Initialisiere Stimmen...</span>
          </div>

          <div class="flex items-center gap-3">
            <label for="globalVoiceOverride" class="text-slate-300">Stimmen-Fallback:</label>
            <select id="globalVoiceOverride" class="bg-slate-800 text-slate-200 text-xs rounded-lg px-2.5 py-1 border border-slate-700 focus:outline-none focus:ring-1 focus:ring-sky-400">
              <option value="auto">⚡ Automatische Akzente (Empfohlen)</option>
            </select>
          </div>
        </div>
      </div>
    </div>

    <!-- Exam Score Result Modal / Card (Hidden initially, shown after submit) -->
    <div id="resultsCard" class="hidden mb-8 bg-white border border-slate-200 rounded-2xl p-6 sm:p-8 shadow-xl transition-all">
      <!-- Dynamic JS will populate the results -->
    </div>

    <!-- Task Navigation Tabs / Progress Indicator -->
    <div class="flex items-center justify-between border-b border-slate-200 pb-3 mb-6">
      <div class="flex items-center gap-2">
        <span class="text-xs font-semibold text-slate-500 uppercase tracking-wider">Aufgaben-Übersicht:</span>
        <span class="text-xs px-2 py-0.5 rounded-full bg-slate-200 text-slate-700 font-bold">20 Punkte gesamt</span>
      </div>
      <div class="text-xs font-medium text-slate-500">
        4 Aufgabenbereiche &bull; B1 B2B-Standard
      </div>
    </div>

    <!-- ========================================================================= -->
    <!-- TASK 1: CLOZE / LÜCKENTEXT (INCOTERMS & FREIGHT) -->
    <!-- ========================================================================= -->
    <section class="bg-white rounded-2xl border border-slate-200 p-5 sm:p-7 shadow-sm mb-8 transition hover:border-slate-300">
      <div class="flex flex-wrap items-start justify-between gap-4 mb-5 border-b border-slate-100 pb-4">
        <div>
          <div class="flex items-center gap-2 mb-1">
            <span class="h-6 w-6 rounded-full bg-sky-600 text-white flex items-center justify-center text-xs font-bold">1</span>
            <h3 class="text-base sm:text-lg font-bold text-slate-900">Task 1: Lückentext &ndash; Incoterms & Dispatch Advice</h3>
            <span class="text-xs px-2 py-0.5 rounded bg-emerald-100 text-emerald-800 font-semibold border border-emerald-200">5 Punkte</span>
          </div>
          <p class="text-xs sm:text-sm text-slate-500">
            <strong>Szenario:</strong> Rajeev Patel (Export Manager, Mumbai Steel & Hardware) bespricht die Fracht- und Zollbedingungen mit Julian.
          </p>
        </div>

        <div class="inline-flex items-center gap-1.5 px-3 py-1 bg-amber-50 text-amber-900 border border-amber-200 rounded-xl text-xs font-medium">
          <span>🇮🇳 Akzent: <strong>Indian English (en-IN)</strong></span>
        </div>
      </div>

      <!-- Audio Player Controls for Task 1 -->
      <div class="bg-slate-50 border border-slate-200 rounded-xl p-4 mb-6">
        <div class="flex flex-wrap items-center justify-between gap-4">
          <div class="flex items-center gap-3">
            <button id="btnPlayT1" onclick="playTaskAudio(1)" class="px-4 py-2 bg-sky-600 hover:bg-sky-700 active:scale-95 text-white rounded-xl text-sm font-semibold shadow-sm flex items-center gap-2 transition">
              <svg id="iconPlayT1" class="w-4 h-4 fill-current" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
              <span id="btnTextT1">Audio abspielen</span>
            </button>
            <button id="btnStopT1" onclick="stopAudio()" class="px-3 py-2 bg-slate-200 hover:bg-slate-300 text-slate-700 rounded-xl text-sm font-medium transition" title="Stoppen">
              <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24"><path d="M6 6h12v12H6z"/></svg>
            </button>
            <div class="text-xs text-slate-600 font-medium">
              Verbleibende Wiederholungen: <span id="playsLeftT1" class="font-bold text-sky-700">2 von 2</span>
            </div>
          </div>

          <div class="flex items-center gap-4 text-xs">
            <div class="flex items-center gap-1.5">
              <label for="speedT1" class="text-slate-500 font-medium">Tempo:</label>
              <select id="speedT1" class="bg-white border border-slate-300 rounded-lg px-2 py-1 text-slate-700">
                <option value="0.85">0.85x (Langsamer)</option>
                <option value="1.0" selected>1.0x (Original)</option>
                <option value="1.15">1.15x (Schnell)</option>
              </select>
            </div>
            <div id="playingBadgeT1" class="hidden items-center gap-1.5 text-sky-600 font-semibold">
              <span class="w-2 h-2 rounded-full bg-sky-600 animate-ping"></span>
              Audio läuft...
            </div>
          </div>
        </div>

        <!-- Progress Bar Mock -->
        <div class="w-full bg-slate-200 rounded-full h-1.5 mt-3 overflow-hidden">
          <div id="progressBarT1" class="bg-sky-600 h-1.5 rounded-full transition-all duration-300" style="width: 0%;"></div>
        </div>
      </div>

      <!-- Exercise Form Content -->
      <div class="text-sm leading-relaxed text-slate-700 bg-white p-4 border border-slate-150 rounded-xl space-y-4">
        <p class="font-medium text-slate-900 text-xs uppercase tracking-wider text-slate-400">
          Arbeitsanweisung: Höre die Nachricht an und wähle die passenden Fachbegriffe aus den Dropdowns aus.
        </p>
        
        <div class="p-4 bg-slate-50/70 border border-slate-200 rounded-xl space-y-3 leading-loose">
          <span>"Dear Julian, concerning consignment #IN-908, we are ready to dispatch the raw fittings. As per our revised agreement, the quotation is based on</span>
          
          <!-- Blank 1 -->
          <label class="inline-block mx-1">
            <select id="t1_gap1" class="px-2.5 py-1 text-xs font-semibold bg-white border border-slate-300 rounded-lg shadow-sm focus:border-sky-500 focus:ring-1 focus:ring-sky-500">
              <option value="">-- Wähle Incoterm --</option>
              <option value="EXW">EXW (Ex Works)</option>
              <option value="FOB">FOB (Free on Board)</option>
              <option value="CIF">CIF (Cost, Insurance & Freight)</option>
              <option value="DDP">DDP (Delivered Duty Paid)</option>
            </select>
          </label>
          
          <span>Hamburg Port. This means our company covers maritime transport and marine insurance, but the critical</span>
          
          <!-- Blank 2 -->
          <label class="inline-block mx-1">
            <select id="t1_gap2" class="px-2.5 py-1 text-xs font-semibold bg-white border border-slate-300 rounded-lg shadow-sm focus:border-sky-500 focus:ring-1 focus:ring-sky-500">
              <option value="">-- Wähle Begriff --</option>
              <option value="payment obligation">payment obligation</option>
              <option value="transfer of risk">transfer of risk</option>
              <option value="ownership title">ownership title</option>
              <option value="customs duty">customs duty</option>
            </select>
          </label>
          
          <span>occurs once the goods pass over the vessel's rail in Mumbai. Furthermore, import taxes and</span>
          
          <!-- Blank 3 -->
          <label class="inline-block mx-1">
            <select id="t1_gap3" class="px-2.5 py-1 text-xs font-semibold bg-white border border-slate-300 rounded-lg shadow-sm focus:border-sky-500 focus:ring-1 focus:ring-sky-500">
              <option value="">-- Wähle Begriff --</option>
              <option value="customs clearance">customs clearance</option>
              <option value="factory packaging">factory packaging</option>
              <option value="vessel chartering">vessel chartering</option>
              <option value="airway handling">airway handling</option>
            </select>
          </label>
          
          <span>in Austria are strictly the buyer's responsibility. Please do the needful and confirm receipt of the original</span>
          
          <!-- Blank 4 -->
          <label class="inline-block mx-1">
            <select id="t1_gap4" class="px-2.5 py-1 text-xs font-semibold bg-white border border-slate-300 rounded-lg shadow-sm focus:border-sky-500 focus:ring-1 focus:ring-sky-500">
              <option value="">-- Wähle Dokument --</option>
              <option value="Bill of Lading">Bill of Lading</option>
              <option value="Air Waybill">Air Waybill</option>
              <option value="Pro Forma Invoice">Pro Forma Invoice</option>
              <option value="Certificate of Non-Delivery">Certificate of Non-Delivery</option>
            </select>
          </label>
          
          <span>before next Tuesday. If there is any discrepancy, please revert back to avoid any</span>
          
          <!-- Blank 5 -->
          <label class="inline-block mx-1">
            <select id="t1_gap5" class="px-2.5 py-1 text-xs font-semibold bg-white border border-slate-300 rounded-lg shadow-sm focus:border-sky-500 focus:ring-1 focus:ring-sky-500">
              <option value="">-- Wähle Begriff --</option>
              <option value="demurrage charges">demurrage charges (Hafengelagerausfall)</option>
              <option value="skonto discount">skonto discount (Skonto)</option>
              <option value="bonus voucher">bonus voucher</option>
              <option value="currency gain">currency gain</option>
            </select>
          </label>
          <span>at the port."</span>
        </div>
      </div>

      <!-- Transcript & Solution Box (Hidden until submitted) -->
      <div id="solutionBoxT1" class="hidden mt-4 pt-4 border-t border-slate-200 text-xs">
        <!-- Injected via JS -->
      </div>
    </section>

    <!-- ========================================================================= -->
    <!-- TASK 2: MULTIPLE CHOICE (B2B COMPLAINT, DISCOUNT & ADJUSTMENT) -->
    <!-- ========================================================================= -->
    <section class="bg-white rounded-2xl border border-slate-200 p-5 sm:p-7 shadow-sm mb-8 transition hover:border-slate-300">
      <div class="flex flex-wrap items-start justify-between gap-4 mb-5 border-b border-slate-100 pb-4">
        <div>
          <div class="flex items-center gap-2 mb-1">
            <span class="h-6 w-6 rounded-full bg-sky-600 text-white flex items-center justify-center text-xs font-bold">2</span>
            <h3 class="text-base sm:text-lg font-bold text-slate-900">Task 2: Inhaltliche Fragen &ndash; Voicemail Complaint & Payment Terms</h3>
            <span class="text-xs px-2 py-0.5 rounded bg-emerald-100 text-emerald-800 font-semibold border border-emerald-200">5 Punkte</span>
          </div>
          <p class="text-xs sm:text-sm text-slate-500">
            <strong>Szenario:</strong> Mike Miller (Purchasing Director bei Apex Wholesale, Chicago) hinterlässt eine dringende Beschwerde auf Julians Anrufbeantworter.
          </p>
        </div>

        <div class="inline-flex items-center gap-1.5 px-3 py-1 bg-blue-50 text-blue-900 border border-blue-200 rounded-xl text-xs font-medium">
          <span>🇺🇸 Akzent: <strong>US American English (en-US)</strong></span>
        </div>
      </div>

      <!-- Audio Player Controls for Task 2 -->
      <div class="bg-slate-50 border border-slate-200 rounded-xl p-4 mb-6">
        <div class="flex flex-wrap items-center justify-between gap-4">
          <div class="flex items-center gap-3">
            <button id="btnPlayT2" onclick="playTaskAudio(2)" class="px-4 py-2 bg-sky-600 hover:bg-sky-700 active:scale-95 text-white rounded-xl text-sm font-semibold shadow-sm flex items-center gap-2 transition">
              <svg id="iconPlayT2" class="w-4 h-4 fill-current" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
              <span id="btnTextT2">Audio abspielen</span>
            </button>
            <button id="btnStopT2" onclick="stopAudio()" class="px-3 py-2 bg-slate-200 hover:bg-slate-300 text-slate-700 rounded-xl text-sm font-medium transition" title="Stoppen">
              <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24"><path d="M6 6h12v12H6z"/></svg>
            </button>
            <div class="text-xs text-slate-600 font-medium">
              Verbleibende Wiederholungen: <span id="playsLeftT2" class="font-bold text-sky-700">2 von 2</span>
            </div>
          </div>

          <div class="flex items-center gap-4 text-xs">
            <div class="flex items-center gap-1.5">
              <label for="speedT2" class="text-slate-500 font-medium">Tempo:</label>
              <select id="speedT2" class="bg-white border border-slate-300 rounded-lg px-2 py-1 text-slate-700">
                <option value="0.85">0.85x (Langsamer)</option>
                <option value="1.0" selected>1.0x (Original)</option>
                <option value="1.15">1.15x (Schnell)</option>
              </select>
            </div>
            <div id="playingBadgeT2" class="hidden items-center gap-1.5 text-sky-600 font-semibold">
              <span class="w-2 h-2 rounded-full bg-sky-600 animate-ping"></span>
              Audio läuft...
            </div>
          </div>
        </div>
        <div class="w-full bg-slate-200 rounded-full h-1.5 mt-3 overflow-hidden">
          <div id="progressBarT2" class="bg-sky-600 h-1.5 rounded-full transition-all duration-300" style="width: 0%;"></div>
        </div>
      </div>

      <!-- Multiple Choice Questions -->
      <div class="space-y-6 text-sm">
        
        <!-- Question 1 -->
        <div class="border border-slate-200 rounded-xl p-4 bg-slate-50/50">
          <p class="font-semibold text-slate-900 mb-3">
            1. Why is Mike Miller calling Julian's wholesale department?
          </p>
          <div class="space-y-2">
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q1" value="A" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">A) He wants to cancel all future orders due to severe bankruptcy.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q1" value="B" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">B) Twelve crates arrived damaged with cracked hydraulic valves, and parts are missing.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q1" value="C" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">C) His warehouse rejected the whole vessel because the carrier had no license.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q1" value="D" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">D) He is praising the prompt delivery and wants to place a repeat order immediately.</span>
            </label>
          </div>
        </div>

        <!-- Question 2 -->
        <div class="border border-slate-200 rounded-xl p-4 bg-slate-50/50">
          <p class="font-semibold text-slate-900 mb-3">
            2. What does Mike demand regarding the invoice payment and cash discount (Skonto)?
          </p>
          <div class="space-y-2">
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q2" value="A" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">A) He refuses to pay any invoice forever until a 50% penalty is granted.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q2" value="B" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">B) He will deduct the standard 3% cash discount even though the 10-day payment deadline has already passed.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q2" value="C" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">C) He will pay via Letter of Credit only if Julian covers the bank charges.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q2" value="D" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">D) He offers to wire the total gross sum if Julian delivers a gift voucher.</span>
            </label>
          </div>
        </div>

        <!-- Question 3 -->
        <div class="border border-slate-200 rounded-xl p-4 bg-slate-50/50">
          <p class="font-semibold text-slate-900 mb-3">
            3. How many units were delivered in total, and how many are defective?
          </p>
          <div class="space-y-2">
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q3" value="A" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">A) 500 units ordered; 50 broken; 450 in perfect shape.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q3" value="B" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">B) 1,000 units delivered; 120 units totally shattered.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q3" value="C" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">C) 250 units delivered; only 12 crates were checked so far.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q3" value="D" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">D) 200 items missing, but no goods are broken.</span>
            </label>
          </div>
        </div>

        <!-- Question 4 -->
        <div class="border border-slate-200 rounded-xl p-4 bg-slate-50/50">
          <p class="font-semibold text-slate-900 mb-3">
            4. What specific document does Mike demand Julian's office to issue by Friday noon?
          </p>
          <div class="space-y-2">
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q4" value="A" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">A) An official Credit Note (Gutschrift) covering the defective items and return freight.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q4" value="B" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">B) A new price catalogue for the upcoming summer season.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q4" value="C" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">C) A legal summons for the freight forwarder's insurance broker.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q4" value="D" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">D) A signed customs declaration for US Homeland Security.</span>
            </label>
          </div>
        </div>

        <!-- Question 5 -->
        <div class="border border-slate-200 rounded-xl p-4 bg-slate-50/50">
          <p class="font-semibold text-slate-900 mb-3">
            5. What will happen if Julian's company does NOT respond before the deadline?
          </p>
          <div class="space-y-2">
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q5" value="A" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">A) Mike will sue them in the European Supreme Court immediately.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q5" value="B" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">B) Mike will switch the entire annual supply contract to an alternative supplier in Poland.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q5" value="C" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">C) Mike will destroy the goods and charge disposal fees to Julian's personal account.</span>
            </label>
            <label class="flex items-start gap-3 p-2 rounded-lg hover:bg-white cursor-pointer transition border border-transparent hover:border-slate-200">
              <input type="radio" name="t2_q5" value="D" class="mt-1 text-sky-600 focus:ring-sky-500">
              <span class="text-slate-700">D) Nothing, it was just an informal inquiry.</span>
            </label>
          </div>
        </div>

      </div>

      <!-- Transcript & Solution Box -->
      <div id="solutionBoxT2" class="hidden mt-4 pt-4 border-t border-slate-200 text-xs"></div>
    </section>

    <!-- ========================================================================= -->
    <!-- TASK 3: CHRONOLOGISCHE REIHENFOLGE (SEQUENCING COMPLAINT PROCESS) -->
    <!-- ========================================================================= -->
    <section class="bg-white rounded-2xl border border-slate-200 p-5 sm:p-7 shadow-sm mb-8 transition hover:border-slate-300">
      <div class="flex flex-wrap items-start justify-between gap-4 mb-5 border-b border-slate-100 pb-4">
        <div>
          <div class="flex items-center gap-2 mb-1">
            <span class="h-6 w-6 rounded-full bg-sky-600 text-white flex items-center justify-center text-xs font-bold">3</span>
            <h3 class="text-base sm:text-lg font-bold text-slate-900">Task 3: Chronologische Reihenfolge &ndash; B2B Claim Workflow</h3>
            <span class="text-xs px-2 py-0.5 rounded bg-emerald-100 text-emerald-800 font-semibold border border-emerald-200">5 Punkte</span>
          </div>
          <p class="text-xs sm:text-sm text-slate-500">
            <strong>Szenario:</strong> Victoria Sterling (Head of Quality Management, London Wholesale Logistics) schult die Lehrlinge über den exakten Ablauf bei Transportschäden.
          </p>
        </div>

        <div class="inline-flex items-center gap-1.5 px-3 py-1 bg-red-50 text-red-900 border border-red-200 rounded-xl text-xs font-medium">
          <span>🇬🇧 Akzent: <strong>British English (en-GB)</strong></span>
        </div>
      </div>

      <!-- Audio Player Controls for Task 3 -->
      <div class="bg-slate-50 border border-slate-200 rounded-xl p-4 mb-6">
        <div class="flex flex-wrap items-center justify-between gap-4">
          <div class="flex items-center gap-3">
            <button id="btnPlayT3" onclick="playTaskAudio(3)" class="px-4 py-2 bg-sky-600 hover:bg-sky-700 active:scale-95 text-white rounded-xl text-sm font-semibold shadow-sm flex items-center gap-2 transition">
              <svg id="iconPlayT3" class="w-4 h-4 fill-current" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
              <span id="btnTextT3">Audio abspielen</span>
            </button>
            <button id="btnStopT3" onclick="stopAudio()" class="px-3 py-2 bg-slate-200 hover:bg-slate-300 text-slate-700 rounded-xl text-sm font-medium transition" title="Stoppen">
              <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24"><path d="M6 6h12v12H6z"/></svg>
            </button>
            <div class="text-xs text-slate-600 font-medium">
              Verbleibende Wiederholungen: <span id="playsLeftT3" class="font-bold text-sky-700">2 von 2</span>
            </div>
          </div>

          <div class="flex items-center gap-4 text-xs">
            <div class="flex items-center gap-1.5">
              <label for="speedT3" class="text-slate-500 font-medium">Tempo:</label>
              <select id="speedT3" class="bg-white border border-slate-300 rounded-lg px-2 py-1 text-slate-700">
                <option value="0.85">0.85x (Langsamer)</option>
                <option value="1.0" selected>1.0x (Original)</option>
                <option value="1.15">1.15x (Schnell)</option>
              </select>
            </div>
            <div id="playingBadgeT3" class="hidden items-center gap-1.5 text-sky-600 font-semibold">
              <span class="w-2 h-2 rounded-full bg-sky-600 animate-ping"></span>
              Audio läuft...
            </div>
          </div>
        </div>
        <div class="w-full bg-slate-200 rounded-full h-1.5 mt-3 overflow-hidden">
          <div id="progressBarT3" class="bg-sky-600 h-1.5 rounded-full transition-all duration-300" style="width: 0%;"></div>
        </div>
      </div>

      <!-- Interactive Sequence Reordering List -->
      <div class="space-y-3 text-sm">
        <p class="font-medium text-slate-900 text-xs uppercase tracking-wider text-slate-400">
          Arbeitsanweisung: Höre der Abteilungsleiterin aufmerksam zu. Bringe die 5 Prozess-Schritte mit den ⬆ / ⬇ Buttons in die korrekte chronologische Reihenfolge (1 = zuerst, 5 = zuletzt).
        </p>

        <div id="sequenceContainer" class="space-y-2">
          <!-- Populated by JS -->
        </div>
      </div>

      <!-- Transcript & Solution Box -->
      <div id="solutionBoxT3" class="hidden mt-4 pt-4 border-t border-slate-200 text-xs"></div>
    </section>

    <!-- ========================================================================= -->
    <!-- TASK 4: MATCHING (AUSTRALIAN WHOLESALE SUPPLIERS & COMMERCIAL TERMS) -->
    <!-- ========================================================================= -->
    <section class="bg-white rounded-2xl border border-slate-200 p-5 sm:p-7 shadow-sm mb-8 transition hover:border-slate-300">
      <div class="flex flex-wrap items-start justify-between gap-4 mb-5 border-b border-slate-100 pb-4">
        <div>
          <div class="flex items-center gap-2 mb-1">
            <span class="h-6 w-6 rounded-full bg-sky-600 text-white flex items-center justify-center text-xs font-bold">4</span>
            <h3 class="text-base sm:text-lg font-bold text-slate-900">Task 4: Zuordnung (Matching) &ndash; Partner Statements & Contract Terms</h3>
            <span class="text-xs px-2 py-0.5 rounded bg-emerald-100 text-emerald-800 font-semibold border border-emerald-200">5 Punkte</span>
          </div>
          <p class="text-xs sm:text-sm text-slate-500">
            <strong>Szenario:</strong> Lachlan Cooper (Senior Trader, Pacific Bulk Goods, Melbourne) führt telefonische B2B-Verhandlungen über 5 verschiedene Geschäftspartner.
          </p>
        </div>

        <div class="inline-flex items-center gap-1.5 px-3 py-1 bg-emerald-50 text-emerald-900 border border-emerald-200 rounded-xl text-xs font-medium">
          <span>🇦🇺 Akzent: <strong>Australian English (en-AU)</strong></span>
        </div>
      </div>

      <!-- Audio Player Controls for Task 4 -->
      <div class="bg-slate-50 border border-slate-200 rounded-xl p-4 mb-6">
        <div class="flex flex-wrap items-center justify-between gap-4">
          <div class="flex items-center gap-3">
            <button id="btnPlayT4" onclick="playTaskAudio(4)" class="px-4 py-2 bg-sky-600 hover:bg-sky-700 active:scale-95 text-white rounded-xl text-sm font-semibold shadow-sm flex items-center gap-2 transition">
              <svg id="iconPlayT4" class="w-4 h-4 fill-current" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
              <span id="btnTextT4">Audio abspielen</span>
            </button>
            <button id="btnStopT4" onclick="stopAudio()" class="px-3 py-2 bg-slate-200 hover:bg-slate-300 text-slate-700 rounded-xl text-sm font-medium transition" title="Stoppen">
              <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24"><path d="M6 6h12v12H6z"/></svg>
            </button>
            <div class="text-xs text-slate-600 font-medium">
              Verbleibende Wiederholungen: <span id="playsLeftT4" class="font-bold text-sky-700">2 von 2</span>
            </div>
          </div>

          <div class="flex items-center gap-4 text-xs">
            <div class="flex items-center gap-1.5">
              <label for="speedT4" class="text-slate-500 font-medium">Tempo:</label>
              <select id="speedT4" class="bg-white border border-slate-300 rounded-lg px-2 py-1 text-slate-700">
                <option value="0.85">0.85x (Langsamer)</option>
                <option value="1.0" selected>1.0x (Original)</option>
                <option value="1.15">1.15x (Schnell)</option>
              </select>
            </div>
            <div id="playingBadgeT4" class="hidden items-center gap-1.5 text-sky-600 font-semibold">
              <span class="w-2 h-2 rounded-full bg-sky-600 animate-ping"></span>
              Audio läuft...
            </div>
          </div>
        </div>
        <div class="w-full bg-slate-200 rounded-full h-1.5 mt-3 overflow-hidden">
          <div id="progressBarT4" class="bg-sky-600 h-1.5 rounded-full transition-all duration-300" style="width: 0%;"></div>
        </div>
      </div>

      <!-- Matching Grid -->
      <div class="space-y-4 text-sm">
        <p class="font-medium text-slate-900 text-xs uppercase tracking-wider text-slate-400">
          Arbeitsanweisung: Weise jedem Lieferanten bzw. B2B-Kunden (A–E) die zutreffende vertragliche Sondervereinbarung zu.
        </p>

        <div class="grid grid-cols-1 md:grid-cols-1 gap-3">
          
          <!-- Statement 1 -->
          <div class="p-3.5 border border-slate-200 rounded-xl bg-slate-50 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
            <div class="text-slate-800">
              <span class="font-bold text-slate-900">Partner 1: Sydney Timber Wholesalers</span>
              <p class="text-xs text-slate-500 mt-0.5">Welche Kondition hat Lachlan für diesen Holz-Großhändler vereinbart?</p>
            </div>
            <select id="t4_match1" class="text-xs font-medium bg-white border border-slate-300 rounded-lg px-3 py-2 sm:w-80 shadow-sm focus:border-sky-500">
              <option value="">-- Passende Kondition zuordnen --</option>
              <option value="A">A) Gewährt 15% Mengenrabatt nur bei Vorkasse (Cash with order)</option>
              <option value="B">B) Verlangt 60 Tage Zahlungsziel bei 2% Skonto binnen 14 Tagen</option>
              <option value="C">C) Übernimmt Frachtkosten nur bis zum Freihafen Fremantle (FAS)</option>
              <option value="D">D) Besteht auf unwiderrufliches Akkreditiv (Irrevocable Letter of Credit)</option>
              <option value="E">E) Liefert auf offene Rechnung erst nach erfolgreicher Bonitätsprüfung</option>
            </select>
          </div>

          <!-- Statement 2 -->
          <div class="p-3.5 border border-slate-200 rounded-xl bg-slate-50 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
            <div class="text-slate-800">
              <span class="font-bold text-slate-900">Partner 2: Brisbane Agri-Exports</span>
              <p class="text-xs text-slate-500 mt-0.5">Welche Vereinbarung betrifft das Agrar-Exportunternehmen?</p>
            </div>
            <select id="t4_match2" class="text-xs font-medium bg-white border border-slate-300 rounded-lg px-3 py-2 sm:w-80 shadow-sm focus:border-sky-500">
              <option value="">-- Passende Kondition zuordnen --</option>
              <option value="A">A) Gewährt 15% Mengenrabatt nur bei Vorkasse (Cash with order)</option>
              <option value="B">B) Verlangt 60 Tage Zahlungsziel bei 2% Skonto binnen 14 Tagen</option>
              <option value="C">C) Übernimmt Frachtkosten nur bis zum Freihafen Fremantle (FAS)</option>
              <option value="D">D) Besteht auf unwiderrufliches Akkreditiv (Irrevocable Letter of Credit)</option>
              <option value="E">E) Liefert auf offene Rechnung erst nach erfolgreicher Bonitätsprüfung</option>
            </select>
          </div>

          <!-- Statement 3 -->
          <div class="p-3.5 border border-slate-200 rounded-xl bg-slate-50 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
            <div class="text-slate-800">
              <span class="font-bold text-slate-900">Partner 3: Perth Mining Hardware</span>
              <p class="text-xs text-slate-500 mt-0.5">Welche Transport- oder Zahlungsbedingung gilt für Westaustralien?</p>
            </div>
            <select id="t4_match3" class="text-xs font-medium bg-white border border-slate-300 rounded-lg px-3 py-2 sm:w-80 shadow-sm focus:border-sky-500">
              <option value="">-- Passende Kondition zuordnen --</option>
              <option value="A">A) Gewährt 15% Mengenrabatt nur bei Vorkasse (Cash with order)</option>
              <option value="B">B) Verlangt 60 Tage Zahlungsziel bei 2% Skonto binnen 14 Tagen</option>
              <option value="C">C) Übernimmt Frachtkosten nur bis zum Freihafen Fremantle (FAS)</option>
              <option value="D">D) Besteht auf unwiderrufliches Akkreditiv (Irrevocable Letter of Credit)</option>
              <option value="E">E) Liefert auf offene Rechnung erst nach erfolgreicher Bonitätsprüfung</option>
            </select>
          </div>

          <!-- Statement 4 -->
          <div class="p-3.5 border border-slate-200 rounded-xl bg-slate-50 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
            <div class="text-slate-800">
              <span class="font-bold text-slate-900">Partner 4: Auckland Retail Distributors</span>
              <p class="text-xs text-slate-500 mt-0.5">Wie sichert Lachlan das Risiko beim Übersee-Großhändler ab?</p>
            </div>
            <select id="t4_match4" class="text-xs font-medium bg-white border border-slate-300 rounded-lg px-3 py-2 sm:w-80 shadow-sm focus:border-sky-500">
              <option value="">-- Passende Kondition zuordnen --</option>
              <option value="A">A) Gewährt 15% Mengenrabatt nur bei Vorkasse (Cash with order)</option>
              <option value="B">B) Verlangt 60 Tage Zahlungsziel bei 2% Skonto binnen 14 Tagen</option>
              <option value="C">C) Übernimmt Frachtkosten nur bis zum Freihafen Fremantle (FAS)</option>
              <option value="D">D) Besteht auf unwiderrufliches Akkreditiv (Irrevocable Letter of Credit)</option>
              <option value="E">E) Liefert auf offene Rechnung erst nach erfolgreicher Bonitätsprüfung</option>
            </select>
          </div>

          <!-- Statement 5 -->
          <div class="p-3.5 border border-slate-200 rounded-xl bg-slate-50 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
            <div class="text-slate-800">
              <span class="font-bold text-slate-900">Partner 5: Melbourne Solar Tech</span>
              <p class="text-xs text-slate-500 mt-0.5">Unter welcher Bedingung wird die Ware auf Ziel versendet?</p>
            </div>
            <select id="t4_match5" class="text-xs font-medium bg-white border border-slate-300 rounded-lg px-3 py-2 sm:w-80 shadow-sm focus:border-sky-500">
              <option value="">-- Passende Kondition zuordnen --</option>
              <option value="A">A) Gewährt 15% Mengenrabatt nur bei Vorkasse (Cash with order)</option>
              <option value="B">B) Verlangt 60 Tage Zahlungsziel bei 2% Skonto binnen 14 Tagen</option>
              <option value="C">C) Übernimmt Frachtkosten nur bis zum Freihafen Fremantle (FAS)</option>
              <option value="D">D) Besteht auf unwiderrufliches Akkreditiv (Irrevocable Letter of Credit)</option>
              <option value="E">E) Liefert auf offene Rechnung erst nach erfolgreicher Bonitätsprüfung</option>
            </select>
          </div>

        </div>
      </div>

      <!-- Transcript & Solution Box -->
      <div id="solutionBoxT4" class="hidden mt-4 pt-4 border-t border-slate-200 text-xs"></div>
    </section>

    <!-- Submit / Finalize Test Bar -->
    <div class="sticky bottom-4 z-30 bg-white/95 backdrop-blur-md border border-slate-200 rounded-2xl p-4 shadow-2xl flex flex-wrap items-center justify-between gap-4">
      <div>
        <h4 class="font-bold text-slate-900 text-sm">Schularbeit abschließen</h4>
        <p class="text-xs text-slate-500">Alle 4 Aufgaben werden sofort nach dem österreichischen Notenschlüssel ausgewertet.</p>
      </div>

      <div class="flex items-center gap-3">
        <button onclick="resetExam()" class="px-4 py-2 border border-slate-300 hover:bg-slate-100 text-slate-700 rounded-xl text-xs font-semibold transition">
          Test zurücksetzen ↻
        </button>
        <button id="btnSubmitExam" onclick="gradeExam()" class="px-6 py-2.5 bg-emerald-600 hover:bg-emerald-700 text-white rounded-xl text-sm font-bold shadow-md hover:shadow-lg active:scale-95 transition flex items-center gap-2">
          <span>Prüfung abgeben & benoten</span>
          <svg class="w-4 h-4 fill-none stroke-current" stroke-width="2.5" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
        </button>
      </div>
    </div>

  </main>

  <footer class="bg-white border-t border-slate-200 py-6 text-center text-xs text-slate-500 mt-12">
    <p>LBS Theresienfeld &bull; Fachbereich Großhandel &bull; B1 Vocational English Listening Exam Suite</p>
    <p class="mt-1 text-slate-400">Didaktisch optimiert für Reifeprüfungs- und Berufsschulstandards (GERS B1/B1+).</p>
  </footer>

  <script>
    // =========================================================================
    // DATA MODEL: AUDIO SCRIPTS, TRANSCRIPTS & REASONING (IN GERMAN)
    // =========================================================================
    const examData = {
      task1: {
        accent: "Indian English (en-IN)",
        accentLang: "en-IN",
        playsMax: 2,
        playsUsed: 0,
        script: "Namaste Julian, this is Rajeev Patel calling from Mumbai Steel and Hardware Export division. Concerning our latest heavy consignment reference India nine zero eight, we are totally prepared to dispatch the raw pipe fittings. As per our newly revised wholesale agreement, this quotation is strictly based on CIF Hamburg Port. I repeat, CIF Hamburg Port. This means that our company in Mumbai covers the marine freight and international insurance up to Hamburg dock. But Julian, please be very attentive: the critical transfer of risk occurs much earlier, precisely when the goods pass the ship's rail at Mumbai port. Furthermore, all Austrian import tariffs, taxes and import customs clearance are strictly your company's responsibility in Theresienfeld. We will not cover any customs charges on your end. Please do the needful and confirm receipt of our original ocean Bill of Lading before next Tuesday. If there is any discrepancy in the documents, kindly revert back immediately so that we can avoid heavy demurrage charges while the container waits at the port terminal. Thank you very much.",
        answers: {
          t1_gap1: "CIF",
          t1_gap2: "transfer of risk",
          t1_gap3: "customs clearance",
          t1_gap4: "Bill of Lading",
          t1_gap5: "demurrage charges"
        },
        explanations: {
          t1_gap1: "Rajeev sagt wörtlich: 'this quotation is strictly based on CIF Hamburg Port'. FOB oder DDP wurden ausdrücklich ausgeschlossen.",
          t1_gap2: "Fachbegriff 'transfer of risk' (Gefahrenübergang): Bei CIF geht das Risiko bereits im Verladehafen (Mumbai) auf den Käufer über, obwohl der Verkäufer die Fracht bis Hamburg zahlt.",
          t1_gap3: "'customs clearance' (Zollabfertigung): Liegt bei CIF immer beim Importeur/Käufer in Österreich.",
          t1_gap4: "'Bill of Lading' (Seefrachtbrief/Konnossement) ist das traditionelle Wertpapier für den Seetransport aus Indien.",
          t1_gap5: "'demurrage charges' (Standgelder/Lagergelder), wenn Container im Hafen verzögert abgeholt werden."
        }
      },
      task2: {
        accent: "US American English (en-US)",
        accentLang: "en-US",
        playsMax: 2,
        playsUsed: 0,
        script: "Hey Julian, Mike Miller here from Apex Wholesale in Chicago. Look, I gotta tell you, we have a pretty serious issue with consignment forty-four stroke B that just pulled into our warehouse bay this morning. Our receiving team inspected the pallets, and twelve full wooden crates arrived completely crushed. We're looking at cracked hydraulic valves all over the floor, and roughly a hundred and twenty units are completely ruined and unsellable. We received one thousand units in total, but right now ten percent of the batch is scrap metal. Now, about our invoice terms: your accounts department sent a reminder insisting that our ten-day cash discount window closed yesterday. No way, man! Because of this massive inconvenience and the rework we have to do, I'm personally authorizing my accounting team to deduct our three percent Skonto cash discount on the remaining valid balance anyway. What I need from you right now, no later than Friday noon Central Time, is a formal credit note for the damaged goods plus an extra freight compensation credit. If your office cannot deliver this adjustment note by Friday twelve PM, we will immediately freeze all outstanding purchase orders and re-route our annual two-million-dollar supply contract over to our German backup supplier. Give me a call back on my cell right away. Thanks.",
        answers: {
          t2_q1: "B",
          t2_q2: "B",
          t2_q3: "B",
          t2_q4: "A",
          t2_q5: "B"
        },
        explanations: {
          t2_q1: "Richtig ist B: 12 Kisten waren zerquetscht mit gebrochenen Ventilen ('twelve full wooden crates arrived completely crushed... cracked hydraulic valves').",
          t2_q2: "Richtig ist B: Mike zieht den 3% Skonto-Abzug ('deduct our three percent Skonto cash discount') trotzdem ab, obwohl die 10 Tage verstrichen sind.",
          t2_q3: "Richtig ist B: Es wurden 1.000 Einheiten geliefert, wovon 120 Einheiten zerstört sind ('received one thousand units in total... 120 units are completely ruined').",
          t2_q4: "Richtig ist A: Er fordert eine Gutschriftanzeige ('formal credit note') bis Freitagmittag.",
          t2_q5: "Richtig ist B: Bei Nichterfüllung wird der Jahresvertrag im Wert von 2 Mio. Dollar an einen alternativen Partner vergeben."
        }
      },
      task3: {
        accent: "British English (en-GB)",
        accentLang: "en-GB",
        playsMax: 2,
        playsUsed: 0,
        script: "Good morning, everyone. In wholesale logistics, when a customer notifies us of defective goods, Julian and our junior trainees must follow our mandatory five-step quality procedure in exact order. Please take notes. Step one: the moment a complaint letter or telephone call arrives, you must immediately open our ERP system and log a formal Notice of Defect, noting down the exact batch number and consignment date. Step two: request detailed photographic evidence and the official haulier's consignment note with the driver's signature showing the damage remark. Do not promise any refund yet! Step three: forward these documents to our technical inspection team to assess whether the damage was caused by faulty packaging or during transit. Step four: once the liability is confirmed, issue an official Credit Note or dispatch a replacement delivery free of charge to soothe the client. And finally, step five: forward the total claim file to our transport insurance company to recover our company's financial loss. Make sure this sequence is followed rigorously.",
        correctOrder: [
          "Log formal Notice of Defect in the ERP system with batch number",
          "Request photographic evidence and signed haulier's consignment note",
          "Forward documents to technical inspection team to determine liability",
          "Issue an official Credit Note or dispatch a replacement delivery",
          "Submit the final claim file to the transport insurer to recover losses"
        ],
        // Initial shuffled state for the student
        userOrder: [
          "Submit the final claim file to the transport insurer to recover losses",
          "Log formal Notice of Defect in the ERP system with batch number",
          "Issue an official Credit Note or dispatch a replacement delivery",
          "Request photographic evidence and signed haulier's consignment note",
          "Forward documents to technical inspection team to determine liability"
        ]
      },
      task4: {
        accent: "Australian English (en-AU)",
        accentLang: "en-AU",
        playsMax: 2,
        playsUsed: 0,
        script: "G'day Julian, Lachlan here from Pacific Bulk Goods down under in Melbourne. Just running through our wholesale accounts for the quarter. First up, Sydney Timber Wholesalers: good mates of ours, but they drive a hard bargain. We agreed that they will get a fifteen percent quantity discount, but only on the strict condition of cash with order, no credit whatsoever. Second, Brisbane Agri-Exports: they've had tight cash flow during harvest, so we agreed on a sixty-day payment target, but they can still take a two percent cash discount if they settle the bill within fourteen days. Third, over in Western Australia, Perth Mining Hardware: shipping out there is costly, so under our trade terms, we will only cover freight costs up to Fremantle Port FAS, free alongside ship, after which it's on their coin. Fourth, our mates across the Tasman Sea, Auckland Retail Distributors: because it's trans-Tasman overseas trade with currency volatility, we strictly insist on an Irrevocable Letter of Credit confirmed by an Aussie bank before any ship leaves dock. And fifth, Melbourne Solar Tech: they are an energetic new startup, but until we receive a clean solvency report and bank references, we will not deliver on open account. Once their credit check passes, they're good to go. Cheers, mate!",
        answers: {
          t4_match1: "A",
          t4_match2: "B",
          t4_match3: "C",
          t4_match4: "D",
          t4_match5: "E"
        },
        explanations: {
          t4_match1: "Sydney Timber: 15% Rabatt nur bei Barzahlung/Vorkasse ('15% quantity discount, but only on cash with order').",
          t4_match2: "Brisbane Agri: 60 Tage Zahlungsziel mit 2% Skonto binnen 14 Tagen.",
          t4_match3: "Perth Mining: Frachtkosten nur bis Fremantle FAS (Free Alongside Ship).",
          t4_match4: "Auckland Retail: Absicherung über unwiderrufliches Akkreditiv ('Irrevocable Letter of Credit').",
          t4_match5: "Melbourne Solar: Lieferung auf offene Rechnung ('open account') erst nach Bonitätsprüfung."
        }
      }
    };

    // Global Speech Synthesis Engine State
    let synth = window.speechSynthesis;
    let voices = [];
    let currentUtterance = null;
    let currentActiveTask = null;
    let audioInterval = null;

    function initVoices() {
      if (!('speechSynthesis' in window)) {
        document.getElementById('ttsStatusText').innerText = "⚠️ Web Speech API nicht unterstützt. Bitte Chrome/Safari nutzen.";
        return;
      }

      voices = synth.getVoices();
      const voiceSelect = document.getElementById('globalVoiceOverride');

      if (voices.length > 0) {
        document.getElementById('ttsStatusText').innerText = `${voices.length} System-Stimmen aktiv`;
        document.getElementById('ttsStatusText').className = "text-emerald-400 font-semibold";
        
        // Populate fallback dropdown
        voiceSelect.innerHTML = '<option value="auto">⚡ Automatische Akzente (Empfohlen)</option>';
        voices.forEach((v, idx) => {
          if (v.lang.startsWith('en')) {
            const opt = document.createElement('option');
            opt.value = idx;
            opt.textContent = `${v.name} (${v.lang})`;
            voiceSelect.appendChild(opt);
          }
        });
      }
    }

    if ('speechSynthesis' in window) {
      speechSynthesis.onvoiceschanged = initVoices;
      initVoices();
    }

    // Helper: Find best matching native voice for a specific locale
    function getBestVoiceForLocale(locale) {
      const overrideVal = document.getElementById('globalVoiceOverride').value;
      if (overrideVal !== 'auto' && voices[overrideVal]) {
        return voices[overrideVal];
      }

      // Exact match (e.g. en-IN, en-AU, en-GB, en-US)
      let match = voices.find(v => v.lang.toLowerCase() === locale.toLowerCase());
      if (match) return match;

      // Partial match (e.g. starts with en-IN or contains India/Australia in name)
      match = voices.find(v => v.lang.toLowerCase().replace('_', '-').startsWith(locale.toLowerCase().slice(0, 5)));
      if (match) return match;

      // Search by country name keyword
      if (locale === 'en-IN') match = voices.find(v => /india/i.test(v.name));
      if (locale === 'en-AU') match = voices.find(v => /australia/i.test(v.name));
      if (locale === 'en-GB') match = voices.find(v => /uk|british|united kingdom/i.test(v.name));
      if (locale === 'en-US') match = voices.find(v => /us|united states/i.test(v.name));

      // General English fallback
      return match || voices.find(v => v.lang.startsWith('en')) || null;
    }

    function playTaskAudio(taskNumber) {
      const task = examData[`task${taskNumber}`];

      // Check max plays constraint (Schularbeitsmodus)
      if (task.playsUsed >= task.playsMax) {
        showToast(`Aufgabe ${taskNumber}: Du hast bereits die maximal erlaubten 2 Durchgänge angehört!`, "amber");
        return;
      }

      // Stop any running playback
      stopAudio();

      // Register play count
      task.playsUsed++;
      updatePlayCounters();

      currentActiveTask = taskNumber;
      const speedVal = parseFloat(document.getElementById(`speedT${taskNumber}`).value) || 1.0;

      // Build Utterance
      currentUtterance = new SpeechSynthesisUtterance(task.script);
      currentUtterance.rate = speedVal;
      currentUtterance.pitch = taskNumber === 1 ? 1.05 : (taskNumber === 3 ? 1.0 : 0.98);

      const targetVoice = getBestVoiceForLocale(task.accentLang);
      if (targetVoice) {
        currentUtterance.voice = targetVoice;
        currentUtterance.lang = targetVoice.lang;
      } else {
        currentUtterance.lang = task.accentLang;
      }

      // UI state updates
      document.getElementById(`btnTextT${taskNumber}`).innerText = "Pausieren / Neustart";
      document.getElementById(`playingBadgeT${taskNumber}`).classList.remove('hidden');
      document.getElementById(`playingBadgeT${taskNumber}`).classList.add('flex');

      // Simple visual progress bar simulation based on words count
      const totalWords = task.script.split(/\s+/).length;
      const estimatedDurationSec = (totalWords / (2.5 * speedVal));
      let elapsed = 0;
      const progBar = document.getElementById(`progressBarT${taskNumber}`);
      progBar.style.width = '0%';

      clearInterval(audioInterval);
      audioInterval = setInterval(() => {
        elapsed += 0.2;
        const pct = Math.min(100, Math.round((elapsed / estimatedDurationSec) * 100));
        progBar.style.width = pct + '%';
        if (pct >= 100) clearInterval(audioInterval);
      }, 200);

      currentUtterance.onend = () => {
        clearInterval(audioInterval);
        progBar.style.width = '100%';
        resetPlayerUI(taskNumber);
      };

      currentUtterance.onerror = (e) => {
        clearInterval(audioInterval);
        resetPlayerUI(taskNumber);
        console.error("Speech error", e);
      };

      synth.speak(currentUtterance);
    }

    function stopAudio() {
      if (synth.speaking || synth.pending) {
        synth.cancel();
      }
      clearInterval(audioInterval);
      if (currentActiveTask) {
        resetPlayerUI(currentActiveTask);
      }
      currentActiveTask = null;
    }

    function resetPlayerUI(taskNumber) {
      const btnText = document.getElementById(`btnTextT${taskNumber}`);
      if (btnText) btnText.innerText = "Audio abspielen";
      const badge = document.getElementById(`playingBadgeT${taskNumber}`);
      if (badge) {
        badge.classList.remove('flex');
        badge.classList.add('hidden');
      }
    }

    function updatePlayCounters() {
      for (let i = 1; i <= 4; i++) {
        const t = examData[`task${i}`];
        const left = t.playsMax - t.playsUsed;
        const el = document.getElementById(`playsLeftT${i}`);
        if (el) {
          el.innerText = `${left} von ${t.playsMax}`;
          if (left === 0) {
            el.className = "font-bold text-red-600";
            document.getElementById(`btnPlayT${i}`).classList.add('opacity-50', 'cursor-not-allowed');
          }
        }
      }
    }

    function renderSequenceTask() {
      const container = document.getElementById('sequenceContainer');
      container.innerHTML = '';

      examData.task3.userOrder.forEach((itemText, index) => {
        const div = document.createElement('div');
        div.className = "p-3 bg-white border border-slate-200 rounded-xl flex items-center justify-between gap-3 shadow-sm hover:border-slate-300 transition";
        div.innerHTML = `
          <div class="flex items-center gap-3">
            <span class="w-6 h-6 rounded-full bg-slate-100 border border-slate-300 flex items-center justify-center text-xs font-bold text-slate-700">
              ${index + 1}
            </span>
            <span class="text-xs sm:text-sm font-medium text-slate-800">${itemText}</span>
          </div>
          <div class="flex items-center gap-1">
            <button onclick="moveSequence(${index}, -1)" ${index === 0 ? 'disabled' : ''} class="p-1.5 rounded-lg border border-slate-200 hover:bg-slate-100 disabled:opacity-30 disabled:hover:bg-transparent text-slate-600">
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 15l7-7 7 7"/></svg>
            </button>
            <button onclick="moveSequence(${index}, 1)" ${index === examData.task3.userOrder.length - 1 ? 'disabled' : ''} class="p-1.5 rounded-lg border border-slate-200 hover:bg-slate-100 disabled:opacity-30 disabled:hover:bg-transparent text-slate-600">
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M19 9l-7 7-7-7"/></svg>
            </button>
          </div>
        `;
        container.appendChild(div);
      });
    }

    function moveSequence(index, direction) {
      const arr = examData.task3.userOrder;
      const target = index + direction;
      if (target < 0 || target >= arr.length) return;
      const temp = arr[index];
      arr[index] = arr[target];
      arr[target] = temp;
      renderSequenceTask();
    }

    function gradeExam() {
      stopAudio();

      let scoreT1 = 0;
      let scoreT2 = 0;
      let scoreT3 = 0;
      let scoreT4 = 0;

      // 1. Grade Task 1 (Cloze) - 5 points
      const ans1 = examData.task1.answers;
      for (const [key, val] of Object.entries(ans1)) {
        const userVal = document.getElementById(key).value;
        const elem = document.getElementById(key);
        if (userVal === val) {
          scoreT1++;
          elem.classList.add('border-emerald-500', 'bg-emerald-50', 'text-emerald-900');
          elem.classList.remove('border-red-500', 'bg-red-50');
        } else {
          elem.classList.add('border-red-500', 'bg-red-50', 'text-red-900');
          elem.classList.remove('border-emerald-500', 'bg-emerald-50');
        }
      }

      // 2. Grade Task 2 (Multiple Choice) - 5 points
      const ans2 = examData.task2.answers;
      for (let i = 1; i <= 5; i++) {
        const radios = document.getElementsByName(`t2_q${i}`);
        let selected = null;
        radios.forEach(r => { if (r.checked) selected = r.value; });
        if (selected === ans2[`t2_q${i}`]) {
          scoreT2++;
        }
      }

      // 3. Grade Task 3 (Sequencing) - 5 points
      const correctSeq = examData.task3.correctOrder;
      const userSeq = examData.task3.userOrder;
      userSeq.forEach((item, idx) => {
        if (item === correctSeq[idx]) {
          scoreT3++;
        }
      });

      // 4. Grade Task 4 (Matching) - 5 points
      const ans4 = examData.task4.answers;
      for (let i = 1; i <= 5; i++) {
        const selElem = document.getElementById(`t4_match${i}`);
        if (selElem.value === ans4[`t4_match${i}`]) {
          scoreT4++;
          selElem.classList.add('border-emerald-500', 'bg-emerald-50');
        } else {
          selElem.classList.add('border-red-500', 'bg-red-50');
        }
      }

      const totalScore = scoreT1 + scoreT2 + scoreT3 + scoreT4; // Max 20 points
      const percent = (totalScore / 20) * 100;

      // Austrian Grading Scale (Standard Lehrberufe / Schularbeiten)
      // >= 87.5% : 1 (Sehr gut)
      // >= 75.0% : 2 (Gut)
      // >= 62.5% : 3 (Befriedigend)
      // >= 50.0% : 4 (Genügend)
      // <  50.0% : 5 (Nicht genügend)
      let austrianGrade = { note: 5, label: "Nicht genügend", color: "red", badgeBg: "bg-red-500" };
      if (percent >= 87.5) {
        austrianGrade = { note: 1, label: "Sehr gut", color: "emerald", badgeBg: "bg-emerald-600" };
      } else if (percent >= 75.0) {
        austrianGrade = { note: 2, label: "Gut", color: "blue", badgeBg: "bg-sky-600" };
      } else if (percent >= 62.5) {
        austrianGrade = { note: 3, label: "Befriedigend", color: "amber", badgeBg: "bg-amber-600" };
      } else if (percent >= 50.0) {
        austrianGrade = { note: 4, label: "Genügend", color: "orange", badgeBg: "bg-orange-600" };
      }

      // Display Full Exam Results Banner
      displayResultsBanner(totalScore, percent, austrianGrade, scoreT1, scoreT2, scoreT3, scoreT4);

      // Unlock Detailed Transcripts & Review mode in all tasks
      revealSolutions(scoreT1, scoreT2, scoreT3, scoreT4);

      // Scroll smoothly to results
      document.getElementById('resultsCard').scrollIntoView({ behavior: 'smooth' });
    }

    function displayResultsBanner(score, percent, grade, s1, s2, s3, s4) {
      const card = document.getElementById('resultsCard');
      card.classList.remove('hidden');

      card.innerHTML = `
        <div class="border-b border-slate-100 pb-6 mb-6 flex flex-wrap items-center justify-between gap-4">
          <div>
            <span class="text-xs font-bold uppercase tracking-wider text-slate-400">Offizielles Prüfungsergebnis</span>
            <h2 class="text-2xl font-black text-slate-900 mt-1">Prüfungsurkunde: Schularbeit B1 Großhandel</h2>
            <p class="text-xs text-slate-500">Kandidat: Julian &bull; Lehrgang: 3. Klasse Großhandelskaufmann &bull; LBS Theresienfeld</p>
          </div>

          <!-- Grade Badge -->
          <div class="flex items-center gap-3 bg-slate-50 border border-slate-200 px-5 py-3 rounded-2xl">
            <div class="${grade.badgeBg} text-white w-14 h-14 rounded-xl flex flex-col items-center justify-center font-black shadow-md">
              <span class="text-2xl leading-none">${grade.note}</span>
              <span class="text-[9px] uppercase tracking-tight">Note</span>
            </div>
            <div>
              <div class="text-lg font-extrabold text-slate-900 leading-tight">${grade.label}</div>
              <div class="text-xs font-semibold text-slate-500">${score} von 20 Punkten (${percent.toFixed(1)}%)</div>
            </div>
          </div>
        </div>

        <!-- Breakdown Grid -->
        <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 text-center mb-6">
          <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl">
            <span class="text-[11px] font-semibold text-slate-500 block">Task 1 (Incoterms)</span>
            <span class="text-base font-bold ${s1 >= 4 ? 'text-emerald-600' : 'text-slate-800'}">${s1} / 5 Pkt.</span>
          </div>
          <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl">
            <span class="text-[11px] font-semibold text-slate-500 block">Task 2 (Multiple Choice)</span>
            <span class="text-base font-bold ${s2 >= 4 ? 'text-emerald-600' : 'text-slate-800'}">${s2} / 5 Pkt.</span>
          </div>
          <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl">
            <span class="text-[11px] font-semibold text-slate-500 block">Task 3 (Sequencing)</span>
            <span class="text-base font-bold ${s3 >= 4 ? 'text-emerald-600' : 'text-slate-800'}">${s3} / 5 Pkt.</span>
          </div>
          <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl">
            <span class="text-[11px] font-semibold text-slate-500 block">Task 4 (Matching)</span>
            <span class="text-base font-bold ${s4 >= 4 ? 'text-emerald-600' : 'text-slate-800'}">${s4} / 5 Pkt.</span>
          </div>
        </div>

        <!-- Grade Scale Guide -->
        <div class="bg-slate-50 border border-slate-200 rounded-xl p-3.5 text-xs text-slate-600">
          <div class="font-bold text-slate-800 mb-1.5">Österreichischer Berufsschul-Notenschlüssel (20 Punkte Max):</div>
          <div class="flex flex-wrap gap-x-4 gap-y-1">
            <span><strong>Sehr gut (1):</strong> 17.5 – 20 Pkt. (88–100%)</span>
            <span><strong>Gut (2):</strong> 15 – 17 Pkt. (75–87%)</span>
            <span><strong>Befriedigend (3):</strong> 12.5 – 14.5 Pkt. (63–74%)</span>
            <span><strong>Genügend (4):</strong> 10 – 12 Pkt. (50–62%)</span>
            <span class="text-red-600"><strong>Nicht genügend (5):</strong> &lt; 10 Pkt. (&lt;50%)</span>
          </div>
        </div>

        <div class="mt-4 flex items-center justify-between text-xs text-slate-500">
          <span>🔓 Die offiziellen Hörtranskripte & didaktischen Erklärungen wurden unten freigeschaltet.</span>
          <button onclick="window.print()" class="text-sky-600 hover:underline font-semibold flex items-center gap-1">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 17h2a2 2 0 002-2v-4a2 2 0 00-2-2H5a2 2 0 00-2 2v4a2 2 0 002 2h2m2 4h6a2 2 0 002-2v-4a2 2 0 00-2-2H9a2 2 0 00-2 2v4a2 2 0 002 2zm8-12V5a2 2 0 00-2-2H9a2 2 0 00-2 2v4h10z"/></svg>
            Ergebnis drucken / als PDF sichern
          </button>
        </div>
      `;
    }

    function revealSolutions(s1, s2, s3, s4) {
      // 1. Task 1 Solution Box
      const box1 = document.getElementById('solutionBoxT1');
      box1.classList.remove('hidden');
      box1.innerHTML = `
        <div class="p-4 bg-sky-50/70 border border-sky-200 rounded-xl space-y-3">
          <div class="font-bold text-sky-900 text-sm flex items-center gap-2">
            <span>📜 Vollständiges Audio-Transkript (Indian English) & Lösung:</span>
          </div>
          <div class="text-slate-700 italic border-l-2 border-sky-400 pl-3 leading-relaxed text-xs">
            "${examData.task1.script}"
          </div>
          <div class="mt-2 space-y-1 text-slate-700 text-xs">
            <p><strong>Lösungsschlüssel & Didaktische Erklärung:</strong></p>
            <ul class="list-disc list-inside space-y-1">
              <li><strong>1. CIF:</strong> ${examData.task1.explanations.t1_gap1}</li>
              <li><strong>2. Transfer of risk:</strong> ${examData.task1.explanations.t1_gap2}</li>
              <li><strong>3. Customs clearance:</strong> ${examData.task1.explanations.t1_gap3}</li>
              <li><strong>4. Bill of Lading:</strong> ${examData.task1.explanations.t1_gap4}</li>
              <li><strong>5. Demurrage charges:</strong> ${examData.task1.explanations.t1_gap5}</li>
            </ul>
          </div>
        </div>
      `;

      // 2. Task 2 Solution Box
      const box2 = document.getElementById('solutionBoxT2');
      box2.classList.remove('hidden');
      box2.innerHTML = `
        <div class="p-4 bg-blue-50/70 border border-blue-200 rounded-xl space-y-3">
          <div class="font-bold text-blue-900 text-sm flex items-center gap-2">
            <span>📜 Vollständiges Audio-Transkript (US American English) & Lösung:</span>
          </div>
          <div class="text-slate-700 italic border-l-2 border-blue-400 pl-3 leading-relaxed text-xs">
            "${examData.task2.script}"
          </div>
          <div class="mt-2 space-y-1 text-slate-700 text-xs">
            <p><strong>Lösungsanalyse:</strong></p>
            <ul class="list-disc list-inside space-y-1">
              <li><strong>Frage 1 (B):</strong> ${examData.task2.explanations.t2_q1}</li>
              <li><strong>Frage 2 (B):</strong> ${examData.task2.explanations.t2_q2}</li>
              <li><strong>Frage 3 (B):</strong> ${examData.task2.explanations.t2_q3}</li>
              <li><strong>Frage 4 (A):</strong> ${examData.task2.explanations.t2_q4}</li>
              <li><strong>Frage 5 (B):</strong> ${examData.task2.explanations.t2_q5}</li>
            </ul>
          </div>
        </div>
      `;

      // 3. Task 3 Solution Box
      const box3 = document.getElementById('solutionBoxT3');
      box3.classList.remove('hidden');
      box3.innerHTML = `
        <div class="p-4 bg-red-50/70 border border-red-200 rounded-xl space-y-3">
          <div class="font-bold text-red-900 text-sm flex items-center gap-2">
            <span>📜 Vollständiges Audio-Transkript (British English) & Offizielle Reihenfolge:</span>
          </div>
          <div class="text-slate-700 italic border-l-2 border-red-400 pl-3 leading-relaxed text-xs">
            "${examData.task3.script}"
          </div>
          <div class="mt-2 text-xs">
            <p class="font-bold text-slate-800 mb-1">Korrekte zeitliche Kette:</p>
            <ol class="list-decimal list-inside space-y-1 text-slate-700">
              ${examData.task3.correctOrder.map(step => `<li><span class="font-medium">${step}</span></li>`).join('')}
            </ol>
          </div>
        </div>
      `;

      // 4. Task 4 Solution Box
      const box4 = document.getElementById('solutionBoxT4');
      box4.classList.remove('hidden');
      box4.innerHTML = `
        <div class="p-4 bg-emerald-50/70 border border-emerald-200 rounded-xl space-y-3">
          <div class="font-bold text-emerald-900 text-sm flex items-center gap-2">
            <span>📜 Vollständiges Audio-Transkript (Australian English) & Partner-Zuordnung:</span>
          </div>
          <div class="text-slate-700 italic border-l-2 border-emerald-400 pl-3 leading-relaxed text-xs">
            "${examData.task4.script}"
          </div>
          <div class="mt-2 space-y-1 text-slate-700 text-xs">
            <p><strong>Exakte Begründungen:</strong></p>
            <ul class="list-disc list-inside space-y-1">
              <li><strong>Partner 1 (A):</strong> ${examData.task4.explanations.t4_match1}</li>
              <li><strong>Partner 2 (B):</strong> ${examData.task4.explanations.t4_match2}</li>
              <li><strong>Partner 3 (C):</strong> ${examData.task4.explanations.t4_match3}</li>
              <li><strong>Partner 4 (D):</strong> ${examData.task4.explanations.t4_match4}</li>
              <li><strong>Partner 5 (E):</strong> ${examData.task4.explanations.t4_match5}</li>
            </ul>
          </div>
        </div>
      `;
    }

    function resetExam() {
      stopAudio();

      // Reset play counters
      for (let i = 1; i <= 4; i++) {
        examData[`task${i}`].playsUsed = 0;
        const btn = document.getElementById(`btnPlayT${i}`);
        btn.classList.remove('opacity-50', 'cursor-not-allowed');
        const prog = document.getElementById(`progressBarT${i}`);
        if (prog) prog.style.width = '0%';
        const sBox = document.getElementById(`solutionBoxT${i}`);
        if (sBox) sBox.classList.add('hidden');
      }
      updatePlayCounters();

      // Clear Task 1 inputs
      for (let i = 1; i <= 5; i++) {
        const el = document.getElementById(`t1_gap${i}`);
        el.value = "";
        el.className = "px-2.5 py-1 text-xs font-semibold bg-white border border-slate-300 rounded-lg shadow-sm focus:border-sky-500 focus:ring-1 focus:ring-sky-500";
      }

      // Clear Task 2 radio inputs
      for (let i = 1; i <= 5; i++) {
        const radios = document.getElementsByName(`t2_q${i}`);
        radios.forEach(r => r.checked = false);
      }

      // Reset Task 3 sequence
      examData.task3.userOrder = [
        "Submit the final claim file to the transport insurer to recover losses",
        "Log formal Notice of Defect in the ERP system with batch number",
        "Issue an official Credit Note or dispatch a replacement delivery",
        "Request photographic evidence and signed haulier's consignment note",
        "Forward documents to technical inspection team to determine liability"
      ];
      renderSequenceTask();

      // Clear Task 4 matching
      for (let i = 1; i <= 5; i++) {
        const el = document.getElementById(`t4_match${i}`);
        el.value = "";
        el.className = "text-xs font-medium bg-white border border-slate-300 rounded-lg px-3 py-2 sm:w-80 shadow-sm focus:border-sky-500";
      }

      // Hide results banner
      document.getElementById('resultsCard').classList.add('hidden');
      window.scrollTo({ top: 0, behavior: 'smooth' });
      showToast("Prüfung wurde zurückgesetzt! Alle Durchgänge wieder verfügbar.", "blue");
    }

    // Helper toast message
    function showToast(message, type = "blue") {
      const toast = document.createElement('div');
      toast.className = `fixed bottom-20 right-6 z-50 px-4 py-3 rounded-xl shadow-xl text-xs font-bold text-white transition-all transform duration-300 ${type === 'amber' ? 'bg-amber-600' : (type === 'red' ? 'bg-red-600' : 'bg-slate-900')}`;
      toast.innerText = message;
      document.body.appendChild(toast);
      setTimeout(() => {
        toast.style.opacity = '0';
        setTimeout(() => toast.remove(), 300);
      }, 3500);
    }

    // Initialize sequence task on DOM ready
    window.addEventListener('DOMContentLoaded', () => {
      renderSequenceTask();
      updatePlayCounters();
    });
  </script>
</body>
</html>