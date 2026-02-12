# ADX-Window-Resize-Listener
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
</script>

// 1. Scene & Setup
const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 2000);
const renderer = new THREE.WebGLRenderer({ alpha: true, antialias: true });
renderer.setSize(window.innerWidth, window.innerHeight);
document.getElementById('canvas-container').appendChild(renderer.domElement);

// 2. Particle Geometry
const geometry = new THREE.BufferGeometry();
const vertices = [];
for (let i = 0; i < 5000; i++) {
    vertices.push(THREE.MathUtils.randFloatSpread(2000), THREE.MathUtils.randFloatSpread(2000), THREE.MathUtils.randFloatSpread(2000));
}
geometry.setAttribute('position', new THREE.Float32BufferAttribute(vertices, 3));
const material = new THREE.PointsMaterial({ 
    color: 0x00f3ff, 
    size: 3, 
    transparent: true, 
    opacity: 0.8 
});
const points = new THREE.Points(geometry, material);
scene.add(points);

camera.position.z = 1000;

// 3. Mouse Tracking Logic
let mouseX = 0;
let mouseY = 0;

window.addEventListener('mousemove', (event) => {
    // Normalize mouse coordinates from -1 to 1
    mouseX = (event.clientX - window.innerWidth / 2) / 100;
    mouseY = (event.clientY - window.innerHeight / 2) / 100;
});

// 4. Enhanced Animation Loop
function animate() {
    requestAnimationFrame(animate);

    // Subtle rotation
    points.rotation.y += 0.001;

    // Follow the mouse with "easing" (smooth lag)
    // We move the points slightly based on mouse position
    points.position.x += (mouseX - points.position.x) * 0.05;
    points.position.y += (-mouseY - points.position.y) * 0.05;

    renderer.render(scene, camera);
}
animate();

// Handle Resizing
window.addEventListener('resize', () => {
    camera.aspect = window.innerWidth / window.innerHeight;
    camera.updateProjectionMatrix();
    renderer.setSize(window.innerWidth, window.innerHeight);
});


.hud-overlay::before {
    content: " ";
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), 
                linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
    background-size: 100% 4px, 3px 100%;
    pointer-events: none; /* Allows you to still click buttons underneath */
    z-index: 10;
}

