---
layout: page
title: Cake Actuator
panel: false
date: 2022-01-01 00:00:00 +0800
---

<model-viewer src="cake-actuator.glb" ar ar-modes="webxr scene-viewer quick-look" camera-controls poster="poster.webp"
    shadow-intensity="1" auto-rotate environment-image="legacy" shadow-softness="0.67" exposure="2">
    <div class="progress-bar hide" slot="progress-bar">
        <div class="update-bar"></div>
    </div>
    <button slot="ar-button" id="ar-button">
        View in your space
    </button>
    <div id="ar-prompt">
        <img src="https://modelviewer.dev/shared-assets/icons/hand.png">
    </div>
</model-viewer>