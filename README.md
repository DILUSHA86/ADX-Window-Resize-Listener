8.8.8.8# ADX-Window-Resize-Listener
AdxResize Listener
<script>
    // 1. Scene Setup
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 2000);
    
    // Added antialias: true for smoother visuals
    const renderer = new THREE.WebGLRenderer({ alpha: true, antialias: true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    renderer.setPixelRatio(window.devicePixelRatio); // High-DPI screen support
    document.getElementById('canvas-container').appendChild(renderer.domElement);

    // 2. Geometry Creation
    const geometry = new THREE.BufferGeometry();
    const vertices = [];
    for (let i = 0; i < 5000; i++) {
        vertices.push(
            THREE.MathUtils.randFloatSpread(2000), 
            THREE.MathUtils.randFloatSpread(2000), 
            THREE.MathUtils.randFloatSpread(2000)
        );
    }
    geometry.setAttribute('position', new THREE.Float32BufferAttribute(vertices, 3));
    const material = new THREE.PointsMaterial({ color: 0x00f3ff, size: 2 });
    const points = new THREE.Points(geometry, material);
    scene.add(points);

    camera.position.z = 1000;

    // 3. New: Handle Window Resizing
    // This prevents the "stretching" effect when the browser window is moved
    window.addEventListener('resize', () => {
        camera.aspect = window.innerWidth / window.innerHeight;
        camera.updateProjectionMatrix();
        renderer.setSize(window.innerWidth, window.innerHeight);
    });

    // 4. Animation Loop
    function animate() {
        requestAnimationFrame(animate);
        points.rotation.y += 0.0008; // Slightly slower for a "premium" feel
        points.rotation.x += 0.0003; 
        renderer.render(scene, camera);
    }
    animate();
<h1 class="typewriter">DILUSHA86</h1>
<h3 class="typewriter">[ CURRENT_PROJECT: GOLDEN_EAGLE_PRIMAL ]</h3>
<div class="audio-control" onclick="toggleAudio()">
    [ AUDIO_SENSORS: <span id="audio-status">OFF</span> ]
</div>

<audio id="bg-track" loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-10.mp3" type="audio/mpeg">
</audio>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>ADX | DILUSHA86</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<style>
:root{--blueprint-cyan:#00f3ff;--bg-dark:#020b1a;--hazard-yellow:#f4d03f}body{margin:0;background:var(--bg-dark);color:#fff;font-family:'Courier New',monospace;overflow-x:hidden}#canvas-container{position:fixed;top:0;left:0;z-index:-1}.hud-overlay{padding:40px;max-width:800px;background:rgba(2,11,26,.8);border-right:2px solid var(--blueprint-cyan);min-height:100vh;backdrop-filter:blur(10px)}.adx-badge{display:inline-block;padding:5px 15px;border:1px solid var(--blueprint-cyan);color:var(--blueprint-cyan);margin-bottom:20px}.rate-card{width:100%;border-collapse:collapse;margin-top:20px;border:1px solid rgba(0,243,255,.3)}.rate-card td,.rate-card th{padding:10px;border:1px solid rgba(0,243,255,.2);text-align:left}.btn{display:inline-block;padding:10px 20px;background:var(--blueprint-cyan);color:var(--bg-dark);text-decoration:none;font-weight:700;margin-top:20px;position:relative;transition:background .3s}.btn:hover{background:#fff;box-shadow:0 0 20px var(--blueprint-cyan)}.audio-control{margin-top:20px;cursor:pointer;color:var(--hazard-yellow);font-size:.8rem;display:inline-block;border:1px dashed var(--hazard-yellow);padding:5px 10px}@keyframes glitch{0%{transform:translate(0)}20%{transform:translate(-3px,3px)}40%{transform:translate(-3px,-3px)}60%{transform:translate(3px,3px)}80%{transform:translate(3px,-3px)}100%{transform:translate(0)}}.btn:hover::after,.btn:hover::before{content:"VIEW GITHUB ACCESS";position:absolute;top:0;left:0;width:100%;height:100%;background:var(--blueprint-cyan);display:flex;align-items:center;justify-content:center;opacity:.8}.btn:hover::before{color:#ff00c1;z-index:-1;animation:glitch .3s cubic-bezier(.25,.46,.45,.94) both infinite}.btn:hover::after{color:#00fff9;z-index:-2;animation:glitch .3s cubic-bezier(.25,.46,.45,.94) reverse both infinite}
</style>
</head>
<body>.contact-form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    margin-top: 20px;
}

.contact-form input, .contact-form textarea {
    background: rgba(0, 243, 255, 0.05);
    border: 1px solid rgba(0, 243, 255, 0.3);
    padding: 12px;
    color: var(--blueprint-cyan);
    font-family: 'Courier New', monospace;
    outline: none;
}

.contact-form input:focus, .contact-form textarea:focus {
    border-color: var(--blueprint-cyan);
    box-shadow: 0 0 10px rgba(0, 243, 255, 0.2);
}

.contact-form input::placeholder, .contact-form textarea::placeholder {
    color: rgba(0, 243, 255, 0.4);
}

<div id="canvas-container"></div>
<div class="hud-overlay">
<div class="adx-badge">ADX_GENESIS_VERIFIED</div>
<h1 class="typewriter">DILUSHA86</h1>
<p>Lead Architect of the <strong>ADX Protocol</strong>.</p>
<h3 class="typewriter">[ CURRENT_PROJECT: GOLDEN_EAGLE_PRIMAL ]</h3>
<a href="https://github.com/DILUSHA86" class="btn">VIEW GITHUB ACCESS</a>
<table class="rate-card"><tr><th>Unit</th><th>Rate</th></tr><tr><td>Neural UI</td><td>$1,500+</td></tr><tr><td>SeaWorkflow</td><td>$200/hr</td></tr></table>
<div class="audio-control" onclick="toggleAudio()">[ AUDIO_SENSORS: <span id="audio-status">OFF</span> ]</div>
<audio id="bg-track" loop><source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-10.mp3" type="audio/mpeg"></audio>
</div>
<script>
const scene=new THREE.Scene(),camera=new THREE.PerspectiveCamera(75,window.innerWidth/window.innerHeight,.1,2e3),renderer=new THREE.WebGLRenderer({alpha:!0,antialias:!0});renderer.setSize(window.innerWidth,window.innerHeight),document.getElementById("canvas-container").appendChild(renderer.domElement);const geometry=new THREE.BufferGeometry(),vertices=[];for(let i=0;i<5e3;i++)vertices.push(THREE.MathUtils.randFloatSpread(2e3),THREE.MathUtils.randFloatSpread(2e3),THREE.MathUtils.randFloatSpread(2e3));geometry.setAttribute("position",new THREE.Float32BufferAttribute(vertices,3));const points=new THREE.Points(geometry,new THREE.PointsMaterial({color:62463,size:3,transparent:!0,opacity:.8}));scene.add(points),camera.position.z=1e3;let mx=0,my=0;window.addEventListener("mousemove",e=>{mx=(e.clientX-window.innerWidth/2)/100,my=(e.clientY-window.innerHeight/2)/100});function animate(){requestAnimationFrame(animate),points.rotation.y+=.001,points.position.x+=(mx-points.position.x)*.05,points.position.y+=(-my-points.position.y)*.05,renderer.render(scene,camera)}animate(),window.addEventListener("resize",()=>{camera.aspect=window.innerWidth/window.innerHeight,camera.updateProjectionMatrix(),renderer.setSize(window.innerWidth,window.innerHeight)});const track=document.getElementById("bg-track"),statusText=document.getElementById("audio-status");function toggleAudio(){track.paused?(track.play(),statusText.innerText="ACTIVE",statusText.style.color="var(--blueprint-cyan)"):(track.pause(),statusText.innerText="OFF",statusText.style.color="var(--hazard-yellow)")}function typeWriter(e){const t=e.innerHTML;e.innerHTML="",e.style.visibility="visible";let n=0;!function o(){n<t.length?("<"===t.charAt(n)?(let r=t.indexOf(">",n);e.innerHTML+=t.substring(n,r+1),n=r+1):(e.innerHTML+=t.charAt(n),n++),setTimeout(o,70)):null}()}window.onload=()=>{document.querySelectorAll(".typewriter").forEach(e=>typeWriter(e))};
</script>
</body>
</html><link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🧠</text></svg>"><link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><rect width=%22100%22 height=%22100%22 fill=%22%2300f3ff%22 /></svg>">
<hr style="border: 0; border-top: 1px solid var(--blueprint-cyan); margin: 30px 0;">

<h3>[ ESTABLISH_UPLINK ]</h3>
<form action="https://formspree.io/f/your-id-here" method="POST" class="contact-form">
    <input type="text" name="name" placeholder="IDENTIFIER (NAME)" required>
    <input type="email" name="_replyto" placeholder="COMMS_CHANNEL (EMAIL)" required>
    <textarea name="message" placeholder="ENCRYPTED_MESSAGE" rows="4" required></textarea>
    <button type="submit" class="btn" style="width: 100%; border: none; cursor: pointer;">
        TRANSMIT_DATA
    </button>
</form>
<form id="contact-form" action="https://formspree.io/f/your-id-here" method="POST" class="contact-form">
    <input type="text" name="name" placeholder="IDENTIFIER (NAME)" required>
    <input type="email" name="_replyto" placeholder="COMMS_CHANNEL (EMAIL)" required>
    <textarea name="message" placeholder="ENCRYPTED_MESSAGE" rows="4" required></textarea>
    <button type="submit" id="submit-btn" class="btn" style="width: 100%; border: none; cursor: pointer;">
        TRANSMIT_DATA
    </button>
</form>
<div id="form-status" style="display:none; margin-top: 20px; color: var(--blueprint-cyan); border: 1px solid var(--blueprint-cyan); padding: 15px; text-align: center;">
    [ STATUS: TRANSMISSION_SUCCESSFUL_SYNC_COMPLETE ]
</div>

<div id="terminal-log">
    <div class="log-entry">> SYSTEM_INITIALIZED...</div>
</div>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>ADX | SENTINEL_DASHBOARD</title>
    <script src="https://unpkg.com/three"></script>
    <script src="https://unpkg.com/three-globe"></script>
    <style>
        body { margin: 0; background: #000; overflow: hidden; font-family: 'Courier New', monospace; }
        #globe-container { position: absolute; top: 0; z-index: 1; }
        .ui-overlay {
            position: absolute; top: 20px; left: 20px; z-index: 10;
            color: #00f3ff; pointer-events: none;
        }
        .status-box {
            border: 1px solid #00f3ff; padding: 15px;
            background: rgba(0, 243, 255, 0.1); backdrop-filter: blur(5px);
        }
    </style>
</head>
<body>

<div class="ui-overlay">
    <div class="status-box">
        <div>[ NODE_STATUS: ACTIVE ]</div>
        <div>[ THREAT_LEVEL: STABLE ]</div>
        <div id="coords">LAT: -- | LONG: --</div>
    </div>
</div>

<div id="globe-container"></div>

<script>
    // 1. Initialize the Globe
    const Globe = new ThreeGlobe()
        .globeImageUrl('//unpkg.com/three-globe/example/img/earth-night.jpg')
        .bumpImageUrl('//unpkg.com/three-globe/example/img/earth-topology.png')
        .showAtmosphere(true)
        .atmosphereColor('#00f3ff')
        .atmosphereDaylightAlpha(0.1);

    // 2. Setup Three.js Scene
    const scene = new THREE.Scene();
    scene.add(Globe);
    scene.add(new THREE.AmbientLight(0xbbbbbb, 0.3));
    scene.add(new THREE.DirectionalLight(0xffffff, 0.8));

    const renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.getElementById('globe-container').appendChild(renderer.domElement);

    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    camera.position.z = 300;

    // 3. Animation Loop
    (function animate() {
        Globe.rotation.y += 0.002; // Slow rotation
        renderer.render(scene, camera);
        requestAnimationFrame(animate);
    })();

    // 4. Function to Simulate a Security "Ping"
    function triggerPing(lat, lng, color) {
        const data = [{ lat, lng, color, size: 20 }];
        Globe.ringsData(data);
        Globe.ringColor(() => d => d.color);
        Globe.ringMaxRadius(5);
        Globe.ringPropagationSpeed(3);
        
        document.getElementById('coords').innerText = `LAT: ${lat.toFixed(2)} | LONG: ${lng.toFixed(2)}`;
    }

    // Trigger a random threat every 3 seconds
    setInterval(() => {
        const randomLat = (Math.random() - 0.5) * 180;
        const randomLng = (Math.random() - 0.5) * 360;
        triggerPing(randomLat, randomLng, '#f4d03f');
    }, 3000);

</script>
</body>
</html>
<div class="status-box">
    <div>[ NODE_STATUS: ACTIVE ]</div>
    <div>[ THREAT_LEVEL: <span id="threat-percent">0</span>% ]</div>
    <div style="width: 100%; height: 4px; background: #222; margin-top: 5px;">
        <div id="threat-bar" style="width: 0%; height: 100%; background: var(--blueprint-cyan); transition: width 0.3s, background 0.5s;"></div>
    </div>
    <div id="coords" style="margin-top: 10px;">LAT: -- | LONG: --</div>
</div>
<!-- modify this form HTML and place wherever you want your form -->
<form
  action="https://formspree.io/f/xzdadlyy"
  method="POST"
>
  <label>
    Your email:
    <input type="email" name="email">
  </label>
  <label>
    Your message:
    <textarea name="message"></textarea>
  </label>
  <!-- your other form fields go here -->
  <button type="submit">Send</button>
</form>
<form id="contact-form" action="https://formspree.io/f/your-id-here" method="POST" class="contact-form">
    <input type="text" name="name" placeholder="IDENTIFIER (NAME)" required>
    <input type="email" name="_replyto" placeholder="COMMS_CHANNEL (EMAIL)" required>
    <textarea name="message" placeholder="ENCRYPTED_MESSAGE" rows="4" required></textarea>
    <button type="submit" id="submit-btn" class="btn" style="width: 100%; border: none; cursor: pointer;">
        TRANSMIT_DATA
    </button>
</form>
<div id="form-status" style="display:none; margin-top: 20px; color: var(--blueprint-cyan); border: 1px solid var(--blueprint-cyan); padding: 15px; text-align: center;">
    [ STATUS: TRANSMISSION_SUCCESSFUL_SYNC_COMPLETE ]
</div>
<!-- modify this form HTML and place wherever you want your form --> 
<form Anuradhapura Sri Lanka
  action="https://formspree.io/f/xzdadlyy"
  method="POST"
>
  <label>
    Your email:Dilusha2010@gmail.com 
    <input type="email" name="email">
  </label>
  <label>
    Your message: ADX PROTOCOL 
    <textarea name="message"></textarea>
  </label>
  <!-- your other form fields go here -->
  <button type="submit">Send</button>
</form>
<div id="terminal-log">
    <div class="log-entry">> SYSTEM_INITIALIZED...</div>
</div>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>ADX | SENTINEL_DASHBOARD</title>
    <script src="https://unpkg.com/three"></script>
    <script src="https://unpkg.com/three-globe"></script>
    <style>
        body { margin: 0; background: #000; overflow: hidden; font-family: 'Courier New', monospace; }
        #globe-container { position: absolute; top: 0; z-index: 1; }
        .ui-overlay {
            position: absolute; top: 20px; left: 20px; z-index: 10;
            color: #00f3ff; pointer-events: none;
        }
        .status-box {
            border: 1px solid #00f3ff; padding: 15px;
            background: rgba(0, 243, 255, 0.1); backdrop-filter: blur(5px);
        }
    </style>
</head>
<body>

<div class="ui-overlay">
    <div class="status-box">
        <div>[ NODE_STATUS: ACTIVE ]</div>
        <div>[ THREAT_LEVEL: STABLE ]</div>
        <div id="coords">LAT: -- | LONG: --</div>
    </div>
</div>

<div id="globe-container"></div>

<script>
    // 1. Initialize the Globe
    const Globe = new ThreeGlobe()
        .globeImageUrl('//unpkg.com/three-globe/example/img/earth-night.jpg')
        .bumpImageUrl('//unpkg.com/three-globe/example/img/earth-topology.png')
        .showAtmosphere(true)
        .atmosphereColor('#00f3ff')
        .atmosphereDaylightAlpha(0.1);

    // 2. Setup Three.js Scene
    const scene = new THREE.Scene();
    scene.add(Globe);
    scene.add(new THREE.AmbientLight(0xbbbbbb, 0.3));
    scene.add(new THREE.DirectionalLight(0xffffff, 0.8));

    const renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    document.getElementById('globe-container').appendChild(renderer.domElement);

    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    camera.position.z = 300;

    // 3. Animation Loop
    (function animate() {
        Globe.rotation.y += 0.002; // Slow rotation
        renderer.render(scene, camera);
        requestAnimationFrame(animate);
    })();

    // 4. Function to Simulate a Security "Ping"
    function triggerPing(lat, lng, color) {
        const data = [{ lat, lng, color, size: 20 }];
        Globe.ringsData(data);
        Globe.ringColor(() => d => d.color);
        Globe.ringMaxRadius(5);
        Globe.ringPropagationSpeed(3);
        
        document.getElementById('coords').innerText = `LAT: ${lat.toFixed(2)} | LONG: ${lng.toFixed(2)}`;
    }

    // Trigger a random threat every 3 seconds
    setInterval(() => {
        const randomLat = (Math.random() - 0.5) * 180;
        const randomLng = (Math.random() - 0.5) * 360;
        triggerPing(randomLat, randomLng, '#f4d03f');
    }, 3000);

</script>
</body>
</html>
<div class="status-box">
    <div>[ NODE_STATUS: ACTIVE ]</div>
    <div>[ THREAT_LEVEL: <span id="threat-percent">0</span>% ]</div>
    <div style="width: 100%; height: 4px; background: #222; margin-top: 5px;">
        <div id="threat-bar" style="width: 0%; height: 100%; background: var(--blueprint-cyan); transition: width 0.3s, background 0.5s;"></div>
    </div>
    <div id="coords" style="margin-top: 10px;">LAT: -- | LONG: --</div>
</div>
<a href="sentinel.html" class="btn">INITIALIZE_SENTINEL_UPLINK</a>
