---
title: "Bimbo Ball - Bouncing Ball Animation"
date: 2026-03-12T16:00:00+09:00
draft: false
---

<style>
    .ball-container {
        width: 100%;
        height: 500px;
        background: linear-gradient(to bottom, #87CEEB, #E0F6FF);
        position: relative;
        overflow: hidden;
        border-radius: 10px;
        margin: 20px 0;
    }

    .ball {
        width: 50px;
        height: 50px;
        background: radial-gradient(circle at 30% 30%, #ff6b6b, #c92a2a);
        border-radius: 50%;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        animation: bounce 2s ease-in-out infinite;
        box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    }

    @keyframes bounce {
        0%, 100% {
            bottom: 0;
            animation-timing-function: cubic-bezier(0.280, 0.840, 0.420, 1);
        }
        50% {
            bottom: 400px;
            animation-timing-function: cubic-bezier(0.560, 0.055, 0.675, 0.190);
        }
    }

    .ground {
        position: absolute;
        bottom: 0;
        width: 100%;
        height: 20px;
        background: linear-gradient(to bottom, #8B7355, #654321);
        box-shadow: 0 -2px 5px rgba(0,0,0,0.2);
    }

    .controls {
        text-align: center;
        margin: 20px 0;
    }

    .ball-button {
        padding: 10px 20px;
        margin: 0 10px;
        background: #4CAF50;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 16px;
    }

    .ball-button:hover {
        background: #45a049;
    }

    #speedControl {
        margin: 0 10px;
    }
</style>

<div class="ball-container" id="ballContainer">
    <div class="ball" id="ball"></div>
    <div class="ground"></div>
</div>

<div class="controls">
    <button class="ball-button" onclick="toggleAnimation()">Pause/Play</button>
    <label for="speedControl">Speed:</label>
    <input type="range" id="speedControl" min="0.5" max="5" step="0.5" value="2" onchange="changeSpeed(this.value)">
    <span id="speedValue">2s</span>
    <button class="ball-button" onclick="changeColor()">Change Color</button>
</div>

<script>
    let isPlaying = true;
    const ball = document.getElementById('ball');
    const colors = [
        'radial-gradient(circle at 30% 30%, #ff6b6b, #c92a2a)',
        'radial-gradient(circle at 30% 30%, #4ecdc4, #2a8a84)',
        'radial-gradient(circle at 30% 30%, #ffe66d, #ffc500)',
        'radial-gradient(circle at 30% 30%, #a8e6cf, #7fcdbb)',
        'radial-gradient(circle at 30% 30%, #ff8cc8, #ff6bb3)'
    ];
    let currentColorIndex = 0;

    function toggleAnimation() {
        if (isPlaying) {
            ball.style.animationPlayState = 'paused';
        } else {
            ball.style.animationPlayState = 'running';
        }
        isPlaying = !isPlaying;
    }

    function changeSpeed(value) {
        ball.style.animationDuration = value + 's';
        document.getElementById('speedValue').textContent = value + 's';
    }

    function changeColor() {
        currentColorIndex = (currentColorIndex + 1) % colors.length;
        ball.style.background = colors[currentColorIndex];
    }

    // Add click to jump functionality
    document.getElementById('ballContainer').addEventListener('click', function(e) {
        if (e.target.id !== 'ball') {
            const rect = this.getBoundingClientRect();
            const x = e.clientX - rect.left;
            ball.style.left = x + 'px';
            ball.style.transform = 'translateX(0)';
        }
    });
</script>

## Interactive Bouncing Ball

Click anywhere in the container to move the ball horizontally!

Use the controls to pause/play, adjust speed, or change colors.