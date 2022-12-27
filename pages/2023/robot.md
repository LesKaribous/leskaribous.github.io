---
layout: doc
title: Robot 2023 - Mary et Dary
panel: true
date: 2022-01-01 00:00:00 +0800
toc: true
---

## Présentation

Test 

### Présentation

Test

### Présentation

Test


<model-viewer src="robot-mary.glb" ar ar-modes="webxr scene-viewer quick-look" camera-controls poster="poster.webp"
    shadow-intensity="1" exposure="2" auto-rotate camera-orbit="-95deg 74.09deg 1.058m" field-of-view="30deg">
    <button onclick="location.href='../beacon'" class="Hotspot" slot="hotspot-3"
        data-position="-0.04121248231548713m 0.36198707310934775m -0.0006178469385729191m"
        data-normal="-0.8660253380257722m -1.4106717804405923e-8m -0.500000113897334m"
        data-visibility-attribute="visible">
        <div class="HotspotAnnotation">Beacon</div>
    </button>
    <button conclick="location.href='../battery-box'" class="Hotspot" slot="hotspot-5"
        data-position="0.10645253121926604m 0.1950738811216276m 0.06161888774940195m" data-normal="1m 0m 0m"
        data-visibility-attribute="visible">
        <div class="HotspotAnnotation">Battery-Box</div>
    </button>
    <button onclick="location.href='../vacuum-ball'" class="Hotspot" slot="hotspot-6"
        data-position="-0.13638474386984212m 0.10155602860080451m 0.07716498533864533m"
        data-normal="0.08443937118529297m 0.0036049513467420404m -0.9964220977676177m"
        data-visibility-attribute="visible">
        <div class="HotspotAnnotation">Ball-Actuator</div>
    </button>
    <button onclick="location.href='../cake-actuator'" class="Hotspot" slot="hotspot-10"
        data-position="-0.1559047013593713m 0.011675476663059285m -0.01458321241847093m"
        data-normal="0.11914522106712913m 0m 0.9928768384330783m" data-visibility-attribute="visible">
        <div class="HotspotAnnotation">Cake-Actuator</div>
    </button>
    <button onclick="location.href='../robot-base'" class="Hotspot" slot="hotspot-11"
        data-position="-0.07282751691815352m 0.3230000019334171m 0.03776731903665885m" data-normal="0m 1m 0m"
        data-visibility-attribute="visible">
        <div class="HotspotAnnotation">Base-Robot</div>
    </button>
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
