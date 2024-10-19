---
title: Mapa vztahů
description: 
published: false
date: 2024-10-19T19:50:15.552Z
tags: 
editor: markdown
dateCreated: 2024-10-19T19:24:49.462Z
---

iiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiii

<div class=game>
  <h1>Map of relationships</h1>

  <button id="resetButton">Reset Positions</button>
  <button id="randomPairs">Make random pairs</button>
  <button id="mfpair">Make boy-girl pairs</button>

  <div>
    <label for="timeSlider">Time: </label>
    <input type="range" id="timeSlider" min="2022" max="2025" step="0.1" value="2022">
    <span id="timeLabel">2022.0</span>
    <button id="playButton">Play</button>
  </div>
  

  <!-- Container for the network graph -->
  <div id="network"></div>

  <!-- Include vis.js library -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/vis/4.21.0/vis.min.js"></script>
  <!-- Link to your JavaScript -->
  <script src="script.js"></script>
</div>

