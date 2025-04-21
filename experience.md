---
layout: page
title: "Experience"
permalink: /experience/
css: "/assets/css/experience.css"
---

<div class="spacer"></div>
<!-- Experience Section -->
<div class="experience-step-row" style="position: relative;">
  <div class="container" style="display: flex; justify-content: center; gap: 0px; flex-wrap: nowrap; align-items: flex-start; max-width: 50%; margin: 0 auto;">

    <!-- Step 1 -->
    <div class="experience-step fadein-left fadein-delay-1" style="margin-top: 0; position: relative;">
      <div class="bold-text year-label">2016 - 2019<br>(Ph.D. student)</div>
      <div class="circle">
        <span class="bold-text">University of Tokyo</span><br>JSPS Research Fellow (DC1)<br>(Apr 2016 - Mar 2019)
      </div>

      <!-- 矢印：右横 -->
      <img src="/qanat_website/assets/img/custom-arrow2.png"
           alt="arrow"
           style="position: absolute; left: 280px; top: 120px; width: 60px; z-index: 1000;">
    </div>

    <!-- Step 2 -->
    <div class="experience-step fadein-left fadein-delay-2" style="margin-top: 360px; margin-left: -120px; position: relative;">
      <div class="bold-text year-label">2019 - 2022</div>
      <div style="display: flex; justify-content: center; align-items: center; gap: 0px; position: relative;">
        <div class="circle">
          <span class="bold-text">RIKEN iTHEMS</span><br>Special Postdoctoral Researcher<br>(Apr 2019 - Mar 2022)
        </div>
        <div class="circle">
          <span class="bold-text">Cornell University (USA)</span><br>Postdoctoral Researcher<br>(Sep 2019 - Aug 2020)
        </div>

        <!-- 矢印：左下 -->
        <img src="/qanat_website/assets/img/custom-arrow2.png"
             alt="arrow"
             style="position: absolute; left: 320px; top: 140px; width: 60px; z-index: 1000;">
      </div>
    </div>

    <!-- Step 3 -->
    <div class="experience-step fadein-left fadein-delay-3" style="margin-top: 0; margin-left: -120px; position: relative;">
      <div class="bold-text year-label">2022 - 2025</div>
      <div style="display: flex; justify-content: center; align-items: center; gap: 0px; position: relative;">
        <div class="circle">
          <span class="bold-text">YITP, Kyoto University</span><br>Research Assistant Professor<br>(Apr 2022 - Mar 2025)
        </div>
        <div class="circle" style="position: relative;">
          <span class="bold-text">Princeton University (USA)</span><br>Postdoctoral Researcher<br>(Sep 2022 - Mar 2025)

          <!-- 矢印：右横 -->
          <img src="/qanat_website/assets/img/custom-arrow2.png"
               alt="arrow"
               style="position: absolute; left: 260px; top: 100px; width: 60px; z-index: 1000;">
        </div>
      </div>
    </div>

    <!-- Step 4 -->
    <div class="experience-step fadein-left fadein-delay-4" style="margin-top: 360px; margin-left: -120px;">
      <div class="bold-text year-label" style="font-size: 1.56rem; margin-bottom: 20px;">2025 - Present</div>
      <div class="circle dark-green" style="transform: scale(1.2);">
        <span class="bold-text" style="font-size: 1.2em;">University of Osaka</span><br>Assistant Professor (tenured)<br>(Apr 2025 - present)
      </div>
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
.arrow-corner {
  margin-top: 10px;
  text-align: center;
}
.arrow-img {
  width: 60px;
  height: auto;
  display: block;
  margin: 10px auto 0 auto;
  z-index: 10;
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
