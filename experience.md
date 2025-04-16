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
    <div class="circle-with-arrow">
      <div class="circle">
        <p><span class="bold-text">JSPS Research Fellow (DC1)</span><br>
        at the University of Tokyo</p>
      </div>
      <img class="arrow-below" src="/qanat_website/assets/img/custom-arrow.png" alt="arrow">
    </div>
    <ul class="custom-bullets">
      <li><span class="bold-text">Apr 2016 - Mar 2019</span></li>
      <li>Aug 2017, Aug 2018, Visitor at Perimeter Institute</li>
      <li>Sep 2018 - Oct 2018, Visitor at Cornell University</li>
    </ul>
  </div>
</div>

<!-- Step 2 -->
<div class="experience-step" data-observe>
  <div class="container">
    <div class="circle-with-arrow">
      <div class="circle">
        <p><span class="bold-text">Special Postdoctoral Researcher</span><br>
        at RIKEN iTHEMS (Apr 2019 - Mar 2022)</p>
        <p><span class="bold-text">Postdoctoral Researcher</span><br>
        at Cornell University (Sep 2019 - Aug 2020)</p>
      </div>
      <img class="arrow-below" src="/qanat_website/assets/img/custom-arrow2.png" alt="arrow">
    </div>
    <div class="lists-container">
      <ul class="custom-bullets">
        <li><span class="bold-text">Apr 2019 - Mar 2022</span></li>
      </ul>
    </div>
  </div>
</div>

<!-- Step 3 -->
<div class="experience-step" data-observe>
  <div class="container">
    <div class="circle-with-arrow">
      <div class="circle">
        <p><span class="bold-text">Research Assistant Professor</span><br>
        at Yukawa Institute for Theoretical Physics (Apr 2022 - Mar 2025)</p>
        <p><span class="bold-text">Postdoctoral Researcher</span><br>
        at Princeton University (USA) (Sep 2022 - Mar 2025)</p>
      </div>
      <img class="arrow-below" src="/qanat_website/assets/img/custom-arrow.png" alt="arrow">
    </div>
    <ul class="custom-bullets">
      <li><span class="bold-text">Apr 2022 - Mar 2025</span></li>
      <li>JSPS Research Fellow (PD) (Apr 2022 - Sep 2022)</li>
      <li>JSPS Research Fellow (CPD) (Oct 2022 - Mar 2025)</li>
    </ul>
  </div>
</div>

<!-- Step 4 -->
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
.circle-with-arrow {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.arrow-below {
  width: 50px;
  height: auto;
  margin-top: -5px;
  margin-bottom: 10px;
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
