---
layout: page
title: "Other"
permalink: /other/
---

<div id="language-toggle" style="text-align: right; margin-bottom: 1rem;">
  <button onclick="switchLanguage('en')">English</button>
  <button onclick="switchLanguage('ja')">日本語</button>
</div>

<!-- English Section -->
<div class="lang lang-en">
  <h1 style="text-align: center;">Other Interests</h1>
  <p style="text-align: left;">
    One of my passions outside of physics is <strong>long-distance running</strong>. During my time in Princeton, I ran more than 40,000 km – the equivalent of a full lap around the Earth. I have completed hundreds of marathons, often using running as a way to explore cities, meet people, and reflect on ideas.
  </p>
  <p style="text-align: left;">
    You can read more about this journey through various media:
  </p>

  <div class="social-icons">
    <a href="https://www.instagram.com/p/DItoh7dtVnc/" target="_blank"><img src="/qanat_website/assets/img/instagram.png" alt="Instagram" class="icon"></a>
    <a href="https://www.facebook.com/share/r/1AP8WNAAHf/" target="_blank"><img src="/qanat_website/assets/img/facebook.png" alt="Facebook" class="icon"></a>
    <a href="https://www.linkedin.com/posts/princeton-university_former-princeton-postdoc-kanato-goto-runs-activity-7320099524494987265-Skdl?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAJ5FZwBxh7HWbzfxJFd9DdjiPpXoMRqJX4" target="_blank"><img src="/qanat_website/assets/img/linkedin.png" alt="LinkedIn" class="icon"></a>
    <a href="https://www.youtube.com/watch?v=lp8Yb3nnbAE" target="_blank"><img src="/qanat_website/assets/img/youtube.png" alt="YouTube" class="icon"></a>
  </div>
</div>

<!-- Japanese Section -->
<div class="lang lang-ja">
  <h1 style="text-align: center;">その他の活動</h1>
  <p style="text-align: left;">
    私は物理以外にも<strong>長距離ランニング</strong>を大切にしています。プリンストンで過ごした2年半の間に約4万キロを走破しました。これは地球一周に相当し、日々のランニングが研究や人生の大切な支えとなっていました。
  </p>
  <p style="text-align: left;">
    この活動は以下のメディアでも紹介されています：
  </p>

  <div class="social-icons">
    <a href="https://www.instagram.com/p/DItoh7dtVnc/" target="_blank"><img src="/qanat_website/assets/img/instagram.png" alt="Instagram" class="icon"></a>
    <a href="https://www.facebook.com/share/r/1AP8WNAAHf/" target="_blank"><img src="/qanat_website/assets/img/facebook.png" alt="Facebook" class="icon"></a>
    <a href="https://www.linkedin.com/posts/princeton-university_former-princeton-postdoc-kanato-goto-runs-activity-7320099524494987265-Skdl?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAJ5FZwBxh7HWbzfxJFd9DdjiPpXoMRqJX4" target="_blank"><img src="/qanat_website/assets/img/linkedin.png" alt="LinkedIn" class="icon"></a>
    <a href="https://www.youtube.com/watch?v=lp8Yb3nnbAE" target="_blank"><img src="/qanat_website/assets/img/youtube.png" alt="YouTube" class="icon"></a>
  </div>
</div>

<script>
function switchLanguage(lang) {
  document.querySelectorAll('.lang').forEach(el => {
    el.style.display = el.classList.contains('lang-' + lang) ? 'block' : 'none';
  });
}
switchLanguage('en');
</script>

<style>
.lang { display: none; }
.icon {
  width: 40px;
  height: 40px;
  margin: 10px;
  transition: transform 0.2s;
}
.icon:hover {
  transform: scale(1.1);
}
.social-icons {
  text-align: center;
}
#language-toggle button {
  background: none;
  border: 1px solid #ccc;
  padding: 5px 10px;
  margin-left: 0.5rem;
  font-size: 0.9rem;
  cursor: pointer;
}
#language-toggle button:hover {
  background-color: #eee;
}
</style>
