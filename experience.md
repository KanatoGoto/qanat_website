---
layout: page
title: "Experience"
permalink: /experience/
css: "/assets/css/mainpage.css"
---

<!-- ダミースペースで最初の表示を画面内に限定 -->
<div style="height: 100vh;"></div>

<div class="spacer"></div>

<!-- Step 1 -->
<div class="experience-step fadein-up" data-observe>
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
<div class="experience-step fadein-up" data-observe>
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
<div class="experience-step fadein-up" data-observe>
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
<div class="experience-step fadein-up" data-observe>
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

<style>
.fadein-up {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}
.fadein-up.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>

<script>
window.onload = function () {
  const faders = document.querySelectorAll('[data-observe]');
  const appearOptions = {
    threshold: 0.3,
    rootMargin: "0px 0px -10% 0px"
  };

  const appearOnScroll = new IntersectionObserver((entries, observer) => {
    entries.forEach(entry => {
      if (!entry.isIntersecting) return;
      entry.target.classList.add("visible");
      observer.unobserve(entry.target);
    });
  }, appearOptions);

  faders.forEach(fader => {
    appearOnScroll.observe(fader);
  });
};
</script>
