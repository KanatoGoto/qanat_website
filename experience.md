---
layout: page
title: "Experience"
permalink: /experience/
css: "/assets/css/mainpage.css"
---

<div class="spacer"></div>

<!-- Step 1 -->
<div class="experience-step" id="step-1">
  <div class="container">
    <div class="circle">
      <p><span class="bold-text">JSPS Research Fellow (DC1)</span><br>
      at the University of Tokyo</p>
    </div>
    <ul class="custom-bullets">
      <li><span class="bold-text">Apr 2016 - Mar 2019</span></li>
      <li>Aug 2017, Aug 2018, Visitor at Perimeter Institute</li>
      <li>Sep 2018 - Oct 2018, Visitor at Cornell University</li>
    </ul>
  </div>
</div>

<!-- Arrow + Step 2 -->
<div class="experience-step" id="step-2" style="display:none;">
  <img src="assets/img/arrow_dashedcurved.png" class="rotate-image">
  <div class="container">
    <div class="circle">
      <p><span class="bold-text">Special Postdoctoral Researcher</span><br>
      at RIKEN iTHEMS (Apr 2019 - Mar 2022)</p>
      <p><span class="bold-text">Postdoctoral Researcher</span><br>
      at Cornell University (Sep 2019 - Aug 2020)</p>
    </div>
    <div class="lists-container">
      <ul class="custom-bullets">
        <li><span class="bold-text">Apr 2019 - Mar 2022</span></li>
      </ul>
    </div>
  </div>
</div>

<!-- Arrow + Step 3 -->
<div class="experience-step" id="step-3" style="display:none;">
  <img src="assets/img/arrow_dashedcurved.png" class="rotate-image">
  <div class="container">
    <div class="circle">
      <p><span class="bold-text">Research Assistant Professor</span><br>
      at Yukawa Institute for Theoretical Physics (Apr 2022 - Mar 2025)</p>
      <p><span class="bold-text">Postdoctoral Researcher</span><br>
      at Princeton University (USA) (Sep 2022 - Mar 2025)</p>
    </div>
    <ul class="custom-bullets">
      <li><span class="bold-text">Apr 2022 - Mar 2025</span></li>
      <li>JSPS Research Fellow (PD) (Apr 2022 - Sep 2022)</li>
      <li>JSPS Research Fellow (CPD) (Oct 2022 - Mar 2025)</li>
    </ul>
  </div>
</div>

<!-- Arrow + Step 4 -->
<div class="experience-step" id="step-4" style="display:none;">
  <img src="assets/img/arrow_dashedcurved.png" class="rotate-image">
  <div class="container">
    <div class="circle">
      <p><span class="bold-text">Assistant Professor (tenured)</span><br>
      at the University of Osaka (Apr 2025 - present)</p>
    </div>
    <ul class="custom-bullets">
      <li>—</li>
    </ul>
  </div>
</div>

<!-- Navigation Button -->
<div style="text-align:center; margin-top: 2rem;">
  <button id="nextBtn">Next</button>
</div>

<script>
let currentStep = 1;
document.getElementById("nextBtn").addEventListener("click", function() {
  const current = document.getElementById(`step-${currentStep}`);
  const next = document.getElementById(`step-${currentStep + 1}`);
  if (next) {
    current.style.display = "none";
    next.style.display = "block";
    currentStep++;
  } else {
    this.disabled = true;
    this.textContent = "End of Experience";
  }
});
</script>

