---
layout: page
title: "Experience"
permalink: /experience/
css: "/assets/css/experience.css"
---

<div class="spacer"></div>

<!-- Horizontal layout of all steps -->
<div class="experience-step-row">
  <div class="container" style="display: flex; justify-content: center; gap: 0px; flex-wrap: nowrap; align-items: flex-start; max-width: 50%; margin: 0 auto;">

    <!-- Step 1 -->
    <div class="experience-step fadein-left fadein-delay-1" style="margin-top: 0;">
      <div class="bold-text year-label">2016 - 2019 (Ph.D. student)</div>
      <div class="circle">
        <span class="bold-text">University of Tokyo</span><br>JSPS Research Fellow (DC1)<br>(Apr 2016 - Mar 2019)
      </div>
       <ul class="custom-bullets">
        <li>Aug 2017,Aug 2018, Visitor at Perimeter Institute (Canada)</li>
        <li>Sep- Oct 2018, Visitor at Cornell University (USA)</li>
      </ul>
    </div>

    <!-- Step 2 -->
    <div class="experience-step fadein-left fadein-delay-2" style="margin-top: 360px; margin-left: -120px;">
      <div class="bold-text year-label">2019 - 2022</div>
      <div style="display: flex; justify-content: center; align-items: center; gap: 0px;">
        <div class="circle">
          <span class="bold-text">RIKEN iTHEMS</span><br>Special Postdoctoral Researcher<br>(Apr 2019 - Mar 2022)
        </div>
        <div class="circle">
          <span class="bold-text">Cornell University (USA)</span><br>Postdoctoral Researcher<br>(Sep 2019 - Aug 2020)
        </div>
      </div>
    </div>

    <!-- Step 3 -->
    <div class="experience-step fadein-left fadein-delay-3" style="margin-top: 0; margin-left: -120px;">
      <div class="bold-text year-label">2022 - 2025</div>
      <div style="display: flex; justify-content: center; align-items: center; gap: 0px;">
        <div class="circle">
          <span class="bold-text">YITP, Kyoto University</span><br>Research Assistant Professor<br>(Apr 2022 - Mar 2025)
        </div>
        <div class="circle">
          <span class="bold-text">Princeton University (USA)</span><br>Postdoctoral Researcher<br>(Sep 2022 - Mar 2025)
        </div>
      </div>
      <ul class="custom-bullets">
        <li><span class="bold-text">Apr 2022 - Mar 2025</span></li>
        <li>JSPS Research Fellow (PD) (Apr 2022 - Sep 2022)</li>
        <li>JSPS Research Fellow (CPD) (Oct 2022 - Mar 2025)</li>
      </ul>
    </div>

    <!-- Step 4 -->
    <div class="experience-step fadein-left fadein-delay-4" style="margin-top: 360px; margin-left: -120px;">
      <div class="bold-text year-label" style="font-size: 1.56rem;">2025 - Present</div>
      <div class="circle dark-green" style="transform: scale(1.2);">
        <span class="bold-text" style="font-size: 1.2em;">University of Osaka</span><br>Assistant Professor (tenured)<br>(Apr 2025 - present)
      </div>
      <ul class="custom-bullets">
        <li>—</li>
      </ul>
    </div>

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
.circle {
  width: 240px;
  height: 240px;
  border-radius: 50%;
  background-color: #a8d5ba;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  text-align: center;
  position: relative;
  overflow: hidden;
  flex-direction: column;
  font-size: 0.9rem;
  line-height: 1.3;
  word-break: break-word;
}
.circle.dark-green {
  background-color: #2c5e3e;
}
.year-label {
  font-size: 1.3rem;
  font-weight: bold;
  text-align: center;
  margin-bottom: 10px;
}
.custom-bullets {
  list-style: none;
  padding: 0;
  margin: 20px auto 10px auto;
  max-width: 400px;
  text-align: left;
  font-size: 0.85rem;
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const steps = document.querySelectorAll('.experience-step');
  let delay = 0;

  const observer = new IntersectionObserver((entries, observer) => {
    entries
      .filter(entry => entry.isIntersecting)
      .sort((a, b) => a.target.offsetLeft - b.target.offsetLeft)
      .forEach((entry, index) => {
        setTimeout(() => {
          entry.target.classList.add("visible");
        }, delay);
        delay += 300;
        observer.unobserve(entry.target);
      });
  }, {
    threshold: 0.1
  });

  steps.forEach(step => observer.observe(step));
});
</script>

