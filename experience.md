---
layout: page
title: "Experience"
permalink: /experience/
css: "/assets/css/mainpage.css"
---

<div class="spacer"></div>

<!-- Step 1 -->
<div class="experience-step" data-observe>
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
<div class="arrow-container" data-observe>
  <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#555" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-down">
    <line x1="12" y1="5" x2="12" y2="19"></line>
    <polyline points="19 12 12 19 5 12"></polyline>
  </svg>
</div>
<div class="experience-step" data-observe>
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
<div class="arrow-container" data-observe>
  <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#555" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-down">
    <line x1="12" y1="5" x2="12" y2="19"></line>
    <polyline points="19 12 12 19 5 12"></polyline>
  </svg>
</div>
<div class="experience-step" data-observe>
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
<div class="arrow-container" data-observe>
  <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="#555" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-down">
    <line x1="12" y1="5" x2="12" y2="19"></line>
    <polyline points="19 12 12 19 5 12"></polyline>
  </svg>
</div>
<div class="experience-step" data-observe>
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

<style>
.experience-step {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}
.experience-step.visible {
  opacity: 1;
  transform: translateY(0);
}
.arrow-container {
  display: flex;
  justify-content: center;
  margin: 1rem 0;
  opacity: 0;
  transition: opacity 0.6s ease;
}
.arrow-container.visible {
  opacity: 1;
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const steps = document.querySelectorAll('[data-observe]');
  let delay = 0;

  const observer = new IntersectionObserver((entries, observer) => {
    entries
      .filter(entry => entry.isIntersecting)
      .sort((a, b) => a.target.offsetTop - b.target.offsetTop)
      .forEach((entry, index) => {
        setTimeout(() => {
          entry.target.classList.add("visible");
        }, delay);
        delay += 200;
        observer.unobserve(entry.target);
      });
  }, {
    threshold: 0.1
  });

  steps.forEach(step => observer.observe(step));
});
</script>
