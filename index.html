<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Rig - Studio Menu Edition</title>
    <style>
        :root { --gold: #ffcc00; --bg: #050505; --panel: #111; }
        body { background: var(--bg); color: #e0e0e0; font-family: 'Segoe UI', sans-serif; margin: 0; display: flex; height: 100vh; overflow: hidden; }
        
        /* Menu Lateral */
        #sidebar { 
            position: fixed; left: -280px; top: 0; width: 260px; height: 100%; 
            background: var(--panel); border-right: 1px solid #333; padding: 20px; 
            display: flex; flex-direction: column; transition: 0.4s cubic-bezier(0.4, 0, 0.2, 1); z-index: 1000; 
            box-shadow: 10px 0 30px rgba(0,0,0,0.5);
        }
        #sidebar.open { left: 0; }
        
        #menu-toggle {
            position: fixed; top: 20px; left: 20px; background: var(--gold); color: #000;
            border: none; padding: 10px 15px; border-radius: 8px; font-weight: bold;
            cursor: pointer; z-index: 900; text-transform: uppercase; font-size: 11px;
        }

        h3 { color: var(--gold); font-size: 10px; text-transform: uppercase; letter-spacing: 2px; margin: 20px 0 10px; border-bottom: 1px solid #333; padding-bottom: 5px; }
        .menu-item { padding: 10px; cursor: pointer; border-radius: 5px; font-size: 12px; color: #aaa; transition: 0.2s; margin-bottom: 5px; }
        .menu-item:hover { background: #222; color: #fff; }
        .menu-item.active { background: var(--gold); color: #000; font-weight: bold; }

        /* Afinador no Menu (Compacto) */
        .mini-tuner { background: #000; border: 1px solid #333; border-radius: 8px; padding: 10px; margin-top: 20px; text-align: center; }
        .mini-note { font-size: 1.8rem; font-weight: 900; color: #222; margin: 0; line-height: 1.2; }
        .mini-note.active { color: var(--gold); }
        .mini-note.in-tune { color: #00ff66 !important; text-shadow: 0 0 10px rgba(0,255,102,0.4); }
        .mini-hz { font-family: monospace; font-size: 9px; color: #444; text-transform: uppercase; margin-top: 4px; }

        /* Área Central */
        #main-content { flex: 1; display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 20px; width: 100%; }
        .pedalboard { background: #111; border-radius: 20px; padding: 25px; border: 1px solid #333; width: 90%; max-width: 450px; box-shadow: 0 15px 50px rgba(0,0,0,1); }
        
        .control-group { margin-bottom: 12px; background: #1a1a1a; padding: 12px; border-radius: 10px; border-left: 3px solid #333; }
        .control-group.fx { border-left-color: var(--gold); }
        label { display: flex; justify-content: space-between; margin-bottom: 5px; font-weight: bold; font-size: 11px; color: #777; text-transform: uppercase; }
        label span { color: var(--gold); font-family: monospace; }
        input[type="range"] { width: 100%; cursor: pointer; accent-color: var(--gold); }
        
        button#mainToggle { background: var(--gold); border: none; padding: 18px; border-radius: 12px; font-weight: 800; cursor: pointer; width: 100%; font-size: 16px; color: #000; margin-top: 10px; text-transform: uppercase; }
        button#mainToggle.active { background: #ff4444; color: #fff; }
        .status { text-align: center; font-size: 9px; color: #444; margin-top: 15px; text-transform: uppercase; }
    </style>
</head>
<body>

<button id="menu-toggle" onclick="toggleMenu(true)">☰ RIG MENU</button>

<div id="sidebar">
    <div style="display:flex; justify-content: space-between; align-items:center;">
        <h2 style="color:white; font-size: 14px; margin:0;">STUDIO CONTROL</h2>
        <span onclick="toggleMenu(false)" style="cursor:pointer; color:var(--gold); font-weight:bold; padding: 5px;">✕</span>
    </div>
    
    <h3>Guns N' Roses</h3>
    <div class="menu-item" id="btn-slash_afd" onclick="applyPreset('slash_afd')">Slash AFD Mode</div>
    <div class="menu-item" id="btn-november" onclick="applyPreset('november')">November Lead Mode</div>

    <h3>Metallica</h3>
    <div class="menu-item" id="btn-met_clean" onclick="applyPreset('met_clean')">One Intro Mode</div>
    <div class="menu-item active" id="btn-met_solo" onclick="applyPreset('met_solo')">One Kirk Solo Mode</div>

    <h3>Afinador</h3>
    <div class="mini-tuner">
        <div id="note" class="mini-note">-</div>
        <div id="cents" class="mini-hz">DESLIGADO</div>
    </div>
</div>

<div id="main-content">
    <div class="pedalboard">
        <div class="control-group">
            <label>Studio Sustain <span id="val-drive">20</span></label>
            <input type="range" id="drive" min="0" max="100" step="1" value="20" oninput="updateAudioNodes()">
        </div>

        <div class="control-group">
            <label>Tone Brightness <span id="val-presence">22</span></label>
            <input type="range" id="presence" min="-25" max="35" step="1" value="22" oninput="updateAudioNodes()">
        </div>

        <div class="control-group fx">
            <label>Chorus Level <span id="val-chorus">12%</span></label>
            <input type="range" id="chorus" min="0" max="1" step="0.01" value="0.12" oninput="updateAudioNodes()">
        </div>

        <div class="control-group fx">
            <label>Delay Level (Eco) <span id="val-delay">22%</span></label>
            <input type="range" id="delay" min="0" max="0.9" step="0.01" value="0.22" oninput="updateAudioNodes()">
        </div>

        <div class="control-group fx">
            <label>Reverb Level (Sala) <span id="val-reverb">30%</span></label>
            <input type="range" id="reverb" min="0" max="0.9" step="0.01" value="0.30" oninput="updateAudioNodes()">
        </div>

        <button id="mainToggle" onclick="togglePower()">LIGAR RIG</button>
        <div id="preset-tag" class="status">KIRK SOLO MODE</div>
    </div>
</div>

<script>
let ctx, stream, input, driveNode, inputGain, cab, masterGain;
let presenceFilter, midFilter, compressor, analyzer;
let delayNode, delayMix, reverbNode, reverbMix;
let chorusDelay, chorusOsc, chorusGain, lowCut, highCut;
let irSlash, irMetallica;
let isOn = false;

const presets = {
    slash_afd: { drive: 42, presence: 10, chorus: 0.0, delay: 0.15, reverb: 0.20, ir: 'slash', mid: 1450, tag: "SLASH AFD MODE", id: "btn-slash_afd" },
    november: { drive: 55, presence: -10, chorus: 0.05, delay: 0.18, reverb: 0.25, ir: 'slash', mid: 800, tag: "NOVEMBER RAIN MODE", id: "btn-november" },
    met_clean: { drive: 0, presence: 18, chorus: 0.55, delay: 0.25, reverb: 0.45, ir: 'met', mid: 1450, tag: "ONE INTRO MODE", id: "btn-met_clean" },
    met_solo: { drive: 20, presence: 22, chorus: 0.12, delay: 0.22, reverb: 0.30, ir: 'met', mid: 1450, tag: "KIRK SOLO MODE", id: "btn-met_solo" }
};

async function setupAudio() {
    ctx = new (window.AudioContext || window.webkitAudioContext)({ latencyHint: 0, sampleRate: 44100 });
    stream = await navigator.mediaDevices.getUserMedia({ 
        audio: { echoCancellation: false, noiseSuppression: false, autoGainControl: false, latency: 0 } 
    });
    
    input = ctx.createMediaStreamSource(stream);
    analyzer = ctx.createAnalyser();
    analyzer.fftSize = 4096;
    
    compressor = ctx.createDynamicsCompressor();
    compressor.threshold.value = -35;
    compressor.ratio.value = 12;

    inputGain = ctx.createGain();
    driveNode = ctx.createWaveShaper();
    midFilter = ctx.createBiquadFilter();
    midFilter.type = "peaking";
    midFilter.frequency.value = 1450; 

    presenceFilter = ctx.createBiquadFilter();
    presenceFilter.type = "highshelf";
    presenceFilter.frequency.value = 5500;

    lowCut = ctx.createBiquadFilter();
    lowCut.type = "highpass";
    lowCut.frequency.value = 115;

    highCut = ctx.createBiquadFilter();
    highCut.type = "lowpass";
    highCut.frequency.value = 9000;

    irSlash = await fetchIR("Marshall1960A-G12Ms-SM57-Cap-2in.wav");
    irMetallica = await fetchIR("onemetallica.wav");

    cab = ctx.createConvolver();
    cab.buffer = irMetallica;

    // Chorus
    chorusDelay = ctx.createDelay();
    chorusOsc = ctx.createOscillator();
    chorusGain = ctx.createGain();
    let lfoDepth = ctx.createGain();
    lfoDepth.gain.value = 0.002;
    chorusOsc.frequency.value = 1.1;
    chorusOsc.connect(lfoDepth);
    lfoDepth.connect(chorusDelay.delayTime);
    chorusOsc.start();

    // Delay e Reverb (ORIGINAIS)
    delayNode = ctx.createDelay();
    delayNode.delayTime.value = 0.485; 
    delayMix = ctx.createGain();

    reverbNode = ctx.createConvolver();
    reverbNode.buffer = createReverbBuffer(); 
    reverbMix = ctx.createGain();

    masterGain = ctx.createGain();
    masterGain.gain.value = 1.7;

    // CONEXÕES
    input.connect(analyzer);
    input.connect(compressor);
    compressor.connect(inputGain);
    inputGain.connect(driveNode);
    driveNode.connect(midFilter);
    midFilter.connect(presenceFilter);
    presenceFilter.connect(lowCut);
    lowCut.connect(highCut);
    highCut.connect(cab);
    
    cab.connect(masterGain); 
    cab.connect(chorusDelay); chorusDelay.connect(chorusGain); chorusGain.connect(masterGain);
    cab.connect(delayNode); delayNode.connect(delayMix); delayMix.connect(masterGain);
    cab.connect(reverbNode); reverbNode.connect(reverbMix); reverbMix.connect(masterGain);

    masterGain.connect(ctx.destination);
    
    applyPreset('met_solo');
    requestAnimationFrame(updateTuner);
}

function applyPreset(mode) {
    const p = presets[mode];
    document.getElementById("drive").value = p.drive;
    document.getElementById("presence").value = p.presence;
    document.getElementById("chorus").value = p.chorus;
    document.getElementById("delay").value = p.delay;
    document.getElementById("reverb").value = p.reverb;
    document.getElementById("preset-tag").innerText = p.tag;

    document.querySelectorAll('.menu-item').forEach(m => m.classList.remove('active'));
    document.getElementById(p.id).classList.add('active');

    if (isOn) {
        cab.buffer = (p.ir === 'slash') ? irSlash : irMetallica;
        midFilter.frequency.value = p.mid;
        updateAudioNodes();
    }
}

function updateAudioNodes() {
    if(!isOn) return;
    let d = parseFloat(document.getElementById("drive").value);
    if (d < 25) { driveNode.curve = null; inputGain.gain.value = 1.0 + (d/40); } 
    else { inputGain.gain.value = 1 + (d/12); driveNode.curve = makeCurve(d); }

    presenceFilter.gain.value = document.getElementById("presence").value;
    chorusGain.gain.value = document.getElementById("chorus").value;
    delayMix.gain.value = document.getElementById("delay").value;
    reverbMix.gain.value = document.getElementById("reverb").value;
    
    document.getElementById("val-drive").innerText = d;
    document.getElementById("val-presence").innerText = document.getElementById("presence").value;
    document.getElementById("val-chorus").innerText = Math.round(document.getElementById("chorus").value * 100) + "%";
    document.getElementById("val-delay").innerText = Math.round(document.getElementById("delay").value * 100) + "%";
    document.getElementById("val-reverb").innerText = Math.round(document.getElementById("reverb").value * 100) + "%";
}

function togglePower() {
    if (!isOn) { 
        isOn = true;
        setupAudio(); 
        document.getElementById("mainToggle").innerText = "DESLIGAR RIG"; 
        document.getElementById("mainToggle").classList.add("active"); 
    } else { location.reload(); }
}

function createReverbBuffer() {
    let len = ctx.sampleRate * 2.5;
    let buf = ctx.createBuffer(2, len, ctx.sampleRate);
    for (let c = 0; c < 2; c++) {
        let ch = buf.getChannelData(c);
        for (let i = 0; i < len; i++) ch[i] = (Math.random() * 2 - 1) * Math.pow(1 - i / len, 3);
    }
    return buf;
}

async function fetchIR(url) {
    try {
        const res = await fetch(url);
        const buf = await res.arrayBuffer();
        return await ctx.decodeAudioData(buf);
    } catch(e) { return ctx.createBuffer(2, ctx.sampleRate * 0.05, ctx.sampleRate); }
}

function makeCurve(k) {
    let n = 44100, curve = new Float32Array(n);
    for (let i = 0; i < n; i++) {
        let x = i * 2 / n - 1;
        curve[i] = (Math.PI + k) * x / (Math.PI + k * Math.abs(x));
    }
    return curve;
}

function toggleMenu(s) { document.getElementById('sidebar').classList.toggle('open', s); }

// AFINADOR (IGUAL AO SEU)
const notes = ['C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B'];
function updateTuner() {
    if (!isOn) return;
    const buffer = new Float32Array(analyzer.fftSize);
    analyzer.getFloatTimeDomainData(buffer);
    const freq = autoCorrelate(buffer, ctx.sampleRate);
    const noteEl = document.getElementById('note');
    const centsEl = document.getElementById('cents');
    if (freq === -1) {
        noteEl.className = "mini-note";
        centsEl.innerText = "SILÊNCIO";
    } else {
        const number = 12 * (Math.log2(freq / 440)) + 69;
        const noteIndex = Math.round(number) % 12;
        const diff = number - Math.round(number);
        noteEl.innerText = notes[noteIndex];
        noteEl.className = Math.abs(diff) < 0.1 ? "mini-note active in-tune" : "mini-note active";
        centsEl.innerText = Math.round(freq) + " Hz";
    }
    requestAnimationFrame(updateTuner);
}

function autoCorrelate(buf, sampleRate) {
    let size = buf.length;
    let rms = 0;
    for (let i=0; i<size; i++) rms += buf[i]*buf[i];
    rms = Math.sqrt(rms/size);
    if (rms < 0.002) return -1; 
    let r1=0, r2=size-1, thres=0.1;
    for (let i=0; i<size/2; i++) if (Math.abs(buf[i]) < thres) { r1=i; break; }
    for (let i=1; i<size/2; i++) if (Math.abs(buf[size-i]) < thres) { r2=size-i; break; }
    let b = buf.slice(r1,r2);
    size = b.length;
    let c = new Float32Array(size);
    for (let i=0; i<size; i++) for (let j=0; j<size-i; j++) c[i] += b[j]*b[j+i];
    let d=0; while (c[d]>c[d+1]) d++;
    let maxval=-1, maxpos=-1;
    for (let i=d; i<size; i++) if (c[i] > maxval) { maxval = c[i]; maxpos = i; }
    return sampleRate/maxpos;
}
</script>
</body>
</html>
