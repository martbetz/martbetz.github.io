<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>1970s Super 8 Presgrip Title</title>

<style>

html,
body{
    margin:0;
    padding:0;
    overflow-x:hidden;
}

body{
    /* Center everything both horizontally and vertically against a dark theater background */
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #0d0d0d; 
}

.presgrip-frame{
    position:relative;

    width:min(400px, calc(100vw - 32px));
    aspect-ratio:4/3;

    /* Turns this element into a container so inner elements can measure its actual width */
    container-type: inline-size;

    margin:0;

    /* Original dark red Super 8 background */
    background:#4b0d0d;

    /* Original rounded off edges with a soft, glowing red projection halo */
    border-radius: 16px;
    border: none;
    box-shadow: 
        0 0 25px rgba(220, 80, 50, 0.3),
        0 0 60px rgba(180, 40, 20, 0.15),
        inset 0 0 35px rgba(0, 0, 0, 0.65);

    box-sizing:border-box;

    overflow:hidden;
    will-change: transform;

    /* Scaled back 40% (12px reduced to 7px) for a tighter edge fade */
    -webkit-mask-image: linear-gradient(to right, transparent, black 7px, black calc(100% - 7px), transparent),
                        linear-gradient(to bottom, transparent, black 7px, black calc(100% - 7px), transparent);
    -webkit-mask-composite: intersect;
    mask-image: linear-gradient(to right, transparent, black 7px, black calc(100% - 7px), transparent),
                linear-gradient(to bottom, transparent, black 7px, black calc(100% - 7px), transparent);
    mask-composite: intersect;
}

.presgrip-screen{
    position:absolute;
    inset:0;

    background:#4b0d0d;

    overflow: hidden; /* Contains dust pops strictly within the screen boundary */
    animation: presgrip-flicker .35s infinite;
}

/* Inner viewport to handle the wobble without moving the outer frame */
.presgrip-viewport {
    position: absolute;
    inset: -10px; /* Buffer to hide edge jitter */
    overflow: hidden;
    will-change: transform;
}

.presgrip-screen::before{
    content:"";
    position:absolute;
    inset:0;

    background:
    linear-gradient(
        rgba(255,220,150,.04),
        rgba(255,220,150,.02)
    );

    mix-blend-mode:screen;
}

.presgrip-screen::after{
    content:"";
    position:absolute;
    inset:0;

    /* Original vignette from the beginning */
    background:
    radial-gradient(
        ellipse at center,
        transparent 55%,
        rgba(0,0,0,.15) 75%,
        rgba(0,0,0,.45) 100%
    );

    pointer-events:none;
    z-index: 2; /* Keeps the vignette locked to the stable edges */
}

.presgrip-title{
    position:absolute;
    inset:0;

    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;

    text-align:center;

    color:#efe6c8;

    font-family:
        "Arial Narrow",
        "Helvetica Neue",
        Arial,
        sans-serif;

    text-transform:uppercase;

    /* Subtle focus pulse mimicking film gate flutter */
    animation: presgrip-focus-pulse 2.8s infinite ease-in-out;
}

.presgrip-main{
    /* Scales based on the frame's width using container query units (cqi) */
    font-size: clamp(20px, 8cqi, 32px);
    
    font-weight:500;
    letter-spacing:.22em;
    line-height:1.15;

    /* Chromatic Aberration (red/cyan lens dispersion) */
    text-shadow:
        -0.6px 0 0.5px rgba(255, 40, 0, 0.45),
         0.6px 0 0.5px rgba(0, 200, 255, 0.35),
         0 0 2px rgba(255, 255, 220, 0.4);

    transform:rotate(-0.15deg);
}

.presgrip-grain{
    position:absolute;
    inset:-20px;

    opacity:.14;

    background-image:
    repeating-radial-gradient(
        circle,
        rgba(255,255,255,.15) 0,
        rgba(255,255,255,.15) .5px,
        transparent 1.5px,
        transparent 4px
    );

    animation:presgrip-grain .25s infinite;
}

/* Layer for dynamic, non-repeating dust & contamination pops (constrained to screen) */
.presgrip-pop-overlay {
    position: absolute;
    inset: 0;
    pointer-events: none;
    z-index: 3;
}

.dust-pop {
    position: absolute;
    background: rgba(255, 255, 240, 0.55);
    border-radius: 50%;
    pointer-events: none;
}

.dust-hair {
    position: absolute;
    background: rgba(10, 10, 10, 0.4);
    border-radius: 2px;
    pointer-events: none;
}

@keyframes presgrip-focus-pulse {
    0%   { filter: blur(0.65px); }
    35%  { filter: blur(0.50px); }
    60%  { filter: blur(0.75px); }
    85%  { filter: blur(0.55px); }
    100% { filter: blur(0.65px); }
}

@keyframes presgrip-flicker{

    0%   { filter:brightness(1.00); }
    10%  { filter:brightness(1.05); }
    15%  { filter:brightness(.97); }
    22%  { filter:brightness(1.03); }
    31%  { filter:brightness(.95); }
    46%  { filter:brightness(1.06); }
    58%  { filter:brightness(.98); }
    65%  { filter:brightness(1.04); }
    79%  { filter:brightness(.96); }
    89%  { filter:brightness(1.07); }
    100% { filter:brightness(1.00); }
}

@keyframes presgrip-grain{

    0%{
        transform:translate(0,0);
    }

    25%{
        transform:translate(3px,-2px);
    }

    50%{
        transform:translate(-2px,2px);
    }

    75%{
        transform:translate(2px,-1px);
    }

    100%{
        transform:translate(0,0);
    }
}

</style>
</head>
<body>

<div class="presgrip-frame" id="projectorFrame">

    <div class="presgrip-screen">
        <!-- Dust overlay placed here so it stays strictly within the screen boundary and away from border blur -->
        <div class="presgrip-pop-overlay" id="dustOverlay"></div>

        <div class="presgrip-viewport" id="projectorViewport">
            <div class="presgrip-title">
                <div class="presgrip-main">THE</div>
                <div class="presgrip-main">PRESGRIP</div>
                <div class="presgrip-main">PROJECT</div>
            </div>

            <div class="presgrip-grain"></div>
        </div>
    </div>

</div>

<script>
(function() {
    const frame = document.getElementById('projectorFrame');
    const viewport = document.getElementById('projectorViewport');
    const overlay = document.getElementById('dustOverlay');

    // Non-repeating randomized wobble using smooth noise-like steps
    let frameX = 0, frameY = 0, frameRot = 0;
    let targetFrameX = 0, targetFrameY = 0, targetFrameRot = 0;

    let viewX = 0, viewY = 0, viewRot = 0;
    let targetViewX = 0, targetViewY = 0, targetViewRot = 0;

    function updateWobbleTargets() {
        // Outer frame erratic jitter
        targetFrameX = (Math.random() - 0.5) * 1.2;
        targetFrameY = (Math.random() - 0.5) * 1.4;
        targetFrameRot = (Math.random() - 0.5) * 0.08;

        // Inner viewport weave (slightly offset)
        targetViewX = (Math.random() - 0.5) * 1.0;
        targetViewY = (Math.random() - 0.5) * 1.2;
        targetViewRot = (Math.random() - 0.5) * 0.06;

        // Random interval between mechanical jerks (simulating projector gear teeth slips)
        const nextInterval = Math.random() * 120 + 80;
        setTimeout(updateWobbleTargets, nextInterval);
    }

    function animateWobble() {
        // Smoothly interpolate (lerp) towards targets for organic motion
        frameX += (targetFrameX - frameX) * 0.2;
        frameY += (targetFrameY - frameY) * 0.2;
        frameRot += (targetFrameRot - frameRot) * 0.2;

        viewX += (targetViewX - viewX) * 0.15;
        viewY += (targetViewY - viewY) * 0.15;
        viewRot += (targetViewRot - viewRot) * 0.15;

        frame.style.transform = `translate(${frameX}px, ${frameY}px) rotate(${frameRot}deg)`;
        viewport.style.transform = `translate(${viewX}px, ${viewY}px) rotate(${viewRot}deg)`;

        requestAnimationFrame(animateWobble);
    }

    // Initialize wobble
    updateWobbleTargets();
    requestAnimationFrame(animateWobble);

    // Non-repeating dust & contamination pops (constrained with a safe coordinate margin)
    function spawnContaminationPop() {
        const isHair = Math.random() > 0.8;
        const pop = document.createElement('div');

        if (isHair) {
            pop.className = 'dust-hair';
            const width = Math.random() * 8 + 4;
            const height = Math.random() * 1.5 + 0.8;
            pop.style.width = width + 'px';
            pop.style.height = height + 'px';
            pop.style.transform = `rotate(${Math.random() * 360}deg)`;
        } else {
            pop.className = 'dust-pop';
            const size = Math.random() * 2 + 1;
            pop.style.width = size + 'px';
            pop.style.height = size + 'px';
            if (Math.random() > 0.5) {
                pop.style.background = 'rgba(15, 15, 15, 0.45)';
            }
        }

        // Constrained between 5% and 95% so dust never spills into outer edge blur/borders
        pop.style.left = (Math.random() * 90 + 5) + '%';
        pop.style.top = (Math.random() * 90 + 5) + '%';

        overlay.appendChild(pop);

        const duration = Math.random() * 50 + 40;
        setTimeout(() => {
            pop.remove();
        }, duration);

        const nextDelay = Math.random() * 750 + 150;
        setTimeout(spawnContaminationPop, nextDelay);
    }

    spawnContaminationPop();
})();
</script>

</body>
</html>
