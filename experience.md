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
    <img src="/qanat_website/assets/img/custom-arrow.png" class="rotate-image fadein-up fadein-delay-2">
  </div>
</div>

<!-- Step 2 -->
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
    <img src="/qanat_website/assets/img/custom-arrow2.png" class="rotate-image fadein-up fadein-delay-4">
  </div>
</div>

<!-- Step 3 -->
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
    <img src="/qanat_website/assets/img/custom-arrow.png" class="rotate-image fadein-up fadein-delay-6">
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
.rotate-image {
  display: block;
  margin: 10px auto 30px auto;
  width: 50px;
  height: auto;
}
.circle {
  width: 120px;
  height: 120px;
  border-radius: 60px;
  background-color: #A0522D;
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 0 auto 10px auto;
  padding: 10px;
  text-align: center;
}
.custom-bullets {
  list-style: none;
  padding: 0;
  margin: 0 auto 40px auto;
  max-width: 600px;
  text-align: left;
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
