<!-- markdownlint-disable MD033 MD041 MD036 -->

<div align="center">

<style>
/* ═══════════════════════════════════════════════════════════
   Modern Minimalist Design System
   ═══════════════════════════════════════════════════════════ */

/* Core Animation Keyframes */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideInSmooth {
  from {
    opacity: 0;
    transform: translateX(-15px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes pulse {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0.6;
  }
}

@keyframes gentleGlow {
  0%, 100% {
    box-shadow: 0 0 10px rgba(168, 85, 247, 0.1);
  }
  50% {
    box-shadow: 0 0 20px rgba(168, 85, 247, 0.2);
  }
}

/* Reduced Motion Support */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

/* Global Styles */
img {
  border-radius: 8px;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Subtle Hover Effects */
img:hover {
  transform: translateY(-3px);
  filter: brightness(1.05);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
}

a {
  transition: all 0.25s ease;
}

/* Badge Micro-interactions */
img[src*="shields.io"],
img[src*="badge"] {
  transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
  border-radius: 6px;
}

img[src*="shields.io"]:hover,
img[src*="badge"]:hover {
  transform: translateY(-2px) scale(1.02);
  box-shadow: 0 4px 12px rgba(168, 85, 247, 0.15);
}

/* Stats Card Animations */
.github-stats-card,
.github-streak-card,
.language-chart {
  animation: fadeIn 0.8s cubic-bezier(0.4, 0, 0.2, 1) both;
  border-radius: 12px;
  transition: all 0.3s ease;
}

.github-stats-card {
  animation-delay: 0.1s;
}

.github-streak-card {
  animation-delay: 0.2s;
}

.language-chart {
  animation-delay: 0.3s;
}

.github-stats-card:hover,
.github-streak-card:hover,
.language-chart:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.08);
}

/* Skill Bar Modern Design */
.skill-container {
  animation: fadeIn 0.6s ease both;
  margin: 24px 0;
}

.skill-item {
  opacity: 0;
  animation: slideInSmooth 0.6s cubic-bezier(0.4, 0, 0.2, 1) forwards;
  margin-bottom: 20px;
}

.skill-item:nth-child(1) { animation-delay: 0.1s; }
.skill-item:nth-child(2) { animation-delay: 0.15s; }
.skill-item:nth-child(3) { animation-delay: 0.2s; }
.skill-item:nth-child(4) { animation-delay: 0.25s; }
.skill-item:nth-child(5) { animation-delay: 0.3s; }
.skill-item:nth-child(6) { animation-delay: 0.35s; }

.skill-bar {
  width: 100%;
  height: 8px;
  background: linear-gradient(90deg, #f3f4f6 0%, #e5e7eb 100%);
  border-radius: 12px;
  overflow: hidden;
  box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.05);
  margin-top: 8px;
}

.skill-fill {
  height: 100%;
  background: linear-gradient(90deg, #a855f7 0%, #7c3aed 50%, #6d28d9 100%);
  border-radius: 12px;
  animation: fillSmooth 1.5s cubic-bezier(0.4, 0, 0.2, 1) forwards;
  box-shadow: 0 2px 8px rgba(168, 85, 247, 0.3);
  position: relative;
}

.skill-fill::after {
  content: attr(data-percentage);
  position: absolute;
  right: 12px;
  top: -24px;
  color: #6b7280;
  font-size: 11px;
  font-weight: 600;
  opacity: 0;
  animation: fadeIn 0.5s ease 1.2s forwards;
  letter-spacing: 0.5px;
}

@keyframes fillSmooth {
  from {
    width: 0%;
    opacity: 0.8;
  }
  to {
    width: var(--target-width);
    opacity: 1;
  }
}

/* Typography Enhancements */
h1, h2, h3 {
  letter-spacing: -0.02em;
  font-weight: 700;
  line-height: 1.2;
}

h2 {
  margin: 48px 0 24px 0;
  font-size: 28px;
}

p {
  line-height: 1.7;
  color: #4b5563;
}

/* Section Spacing */
hr {
  border: none;
  height: 1px;
  background: linear-gradient(90deg, transparent, #e5e7eb, transparent);
  margin: 56px 0;
}

/* Loading Shimmer Effect */
@keyframes shimmer {
  0% {
    background-position: -1000px 0;
  }
  100% {
    background-position: 1000px 0;
  }
}

/* Responsive Grid */
@media (max-width: 768px) {
  .github-stats-card,
  .github-streak-card {
    width: 100% !important;
    margin-bottom: 16px;
  }

  h2 {
    font-size: 24px;
  }
}

/* Professional Table Styling */
table {
  border-collapse: separate;
  border-spacing: 0;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
}

td {
  padding: 24px;
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(10px);
}

/* Smooth Link Transitions */
a:hover {
  opacity: 0.85;
}

/* Clean List Styling */
ul, ol {
  line-height: 1.8;
  margin: 16px 0;
}

li {
  margin: 8px 0;
}

/* Modern Code Block */
code {
  background: linear-gradient(135deg, #f9fafb 0%, #f3f4f6 100%);
  padding: 2px 8px;
  border-radius: 6px;
  font-size: 0.9em;
  border: 1px solid #e5e7eb;
}

/* Elegant Dividers */
.divider {
  height: 2px;
  background: linear-gradient(90deg, transparent, #a855f7, transparent);
  margin: 40px 0;
  border-radius: 2px;
}
</style>

# 👋 Hi, I'm **Robiuzzaman Parvez**

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=A855F7&center=true&vCenter=true&width=600&lines=Lead+Software+Engineer;Full+Stack+Developer;Open+Source+Enthusiast;Problem+Solver+%26+Innovator" alt="Typing Animation" />
</p>

<!-- Social Badges -->
<p align="center">
  <a href="https://www.linkedin.com/in/robi-parvez" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:parvezrobi@yahoo.com">
    <img src="https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://github.com/robiparvez" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <img src="https://komarev.com/ghpvc/?username=robiparvez&color=A855F7&style=for-the-badge&label=Profile+Views" alt="Profile Views" />
</p>

</div>

---

## 🚀 **About Me**

I'm a **Lead Software Engineer** at **RedDot Digital Limited** based in **Dhaka, Bangladesh**. With over a decade of experience in software development, I specialize in building scalable web applications and innovative solutions that solve real-world problems.

```yaml
Name: Robiuzzaman Parvez
Role: Lead Software Engineer @ RedDot Digital Limited
Location: Dhaka, Bangladesh
Focus: Full Stack Development, Cloud Architecture, DevOps
Status: Open to Collaboration & Interesting Projects
Hireable: Yes ✅
```

### 💡 **What I Do**

- 🔧 Design and develop **enterprise-grade** web applications
- ⚡ Build **high-performance** APIs and microservices
- 🎨 Create **responsive** and **accessible** user interfaces
- 📊 Implement **data-driven** solutions with modern analytics
- 🌐 Architect **scalable** cloud infrastructure
- 🤝 Mentor junior developers and contribute to **open source**

---

## 🛠️ **Tech Stack & Expertise**

<div align="center">

### **Programming Languages**

<p>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++" />
</p>

### **Frontend Development**

<p>
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white" alt="Vue.js" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
</p>

### **Backend Development**

<p>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js" />
  <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel" />
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
</p>

### **Databases & Storage**

<p>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
</p>

### **DevOps & Cloud**

<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes" />
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx" />
</p>

### **Tools & IDEs**

<p>
  <img src="https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white" alt="VS Code" />
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman" />
  <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" alt="Figma" />
  <img src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white" alt="Jira" />
</p>

</div>

---

## 📈 **Skills Proficiency**

<div align="center" class="skill-container">

<div style="max-width: 640px; margin: 0 auto; padding: 0 20px;">

<div class="skill-item">
  <strong style="color: #374151; font-size: 14px; font-weight: 600;">JavaScript/TypeScript</strong>
  <div class="skill-bar">
    <div class="skill-fill" style="--target-width: 95%;" data-percentage="95%"></div>
  </div>
</div>

<div class="skill-item">
  <strong style="color: #374151; font-size: 14px; font-weight: 600;">React/Next.js</strong>
  <div class="skill-bar">
    <div class="skill-fill" style="--target-width: 90%;" data-percentage="90%"></div>
  </div>
</div>

<div class="skill-item">
  <strong style="color: #374151; font-size: 14px; font-weight: 600;">Node.js/Express</strong>
  <div class="skill-bar">
    <div class="skill-fill" style="--target-width: 88%;" data-percentage="88%"></div>
  </div>
</div>

<div class="skill-item">
  <strong style="color: #374151; font-size: 14px; font-weight: 600;">Python/Django</strong>
  <div class="skill-bar">
    <div class="skill-fill" style="--target-width: 85%;" data-percentage="85%"></div>
  </div>
</div>

<div class="skill-item">
  <strong style="color: #374151; font-size: 14px; font-weight: 600;">PHP/Laravel</strong>
  <div class="skill-bar">
    <div class="skill-fill" style="--target-width: 82%;" data-percentage="82%"></div>
  </div>
</div>

<div class="skill-item">
  <strong style="color: #374151; font-size: 14px; font-weight: 600;">DevOps/Docker</strong>
  <div class="skill-bar">
    <div class="skill-fill" style="--target-width: 80%;" data-percentage="80%"></div>
  </div>
</div>

</div>

</div>

---

## 📊 **GitHub Analytics**

<div align="center">

<img width="49%" class="github-stats-card" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=robiparvez&theme=tokyonight" alt="GitHub Stats" />
<img width="49%" class="github-streak-card" src="https://github-readme-streak-stats.herokuapp.com/?user=robiparvez&theme=tokyonight&hide_border=true" alt="GitHub Streak" />

<img width="60%" class="language-chart" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=robiparvez&theme=tokyonight" alt="Top Languages" />

</div>

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=robiparvez&theme=tokyo-night&hide_border=true&area=true&custom_title=Contribution%20Activity%20Graph" alt="Contribution Graph" />
</div>

---

## 🏆 **Featured Projects**

<div align="center">

### 🌟 **Activity Tracker Desktop App**
>
> A powerful desktop application for tracking productivity and time management built with TypeScript

[Activity Tracker](https://github.com/robiparvez/activity-tracker-desktop-app)

**Tech Stack:** TypeScript • Electron • Node.js • Desktop App Development

---

### 🚀 **OpenProject WorkLogger**
>
> Automated work logging solution for OpenProject with intelligent time tracking capabilities

[OpenProject WorkLogger](https://github.com/robiparvez/openproject-worklogger)

**Tech Stack:** JavaScript • Node.js • API Integration • Automation

---

### 💡 **NINSBD Platform**
>
> Modern web platform with cutting-edge features and responsive design

[NINSBD](https://github.com/robiparvez/ninsbd)

**Tech Stack:** JavaScript • Web Development • Modern UI/UX

---

### 📊 **ML Gold Price Analyzer**
>
> Machine learning application for analyzing and predicting gold price trends

[ML Gold Price Analyzer](https://github.com/robiparvez/ml-gold-price-analyzer)

**Tech Stack:** Python • Machine Learning • Data Analysis

---

### 🔍 **Live Search JSON Data**
>
> Real-time JSON data search implementation using jQuery with intuitive filtering

[Live Search](https://github.com/robiparvez/Live-Search-JSON-Data-Using-jQuery)

**Tech Stack:** PHP • jQuery • JavaScript • Real-time Search

---

### 💬 **Laravel Chat Application**
>
> Real-time chat application built with Laravel and Pusher for instant messaging

[Laravel Chat](https://github.com/robiparvez/Laravel-chat-app-with-Pusher)

**Tech Stack:** Laravel • Pusher • JavaScript • Real-time Communication

</div>

---

## 🎯 **Current Focus & Interests**

<table>
  <tr>
    <td align="center" width="50%">

### 🔭 **Working On**

- Building scalable microservices architecture
- Implementing ML-powered productivity tools
- Contributing to open source projects
- Mentoring developers in modern web technologies

</td>
    <td align="center" width="50%">

### 🌱 **Learning & Exploring**

- Advanced Kubernetes orchestration
- AI/ML integration in web applications
- Serverless architecture patterns
- Web3 and blockchain technologies

</td>
  </tr>
  <tr>
    <td align="center" width="50%">

### 💬 **Ask Me About**

- Full stack web development
- JavaScript/TypeScript ecosystems
- Cloud architecture (AWS)
- DevOps best practices
- API design and microservices

</td>
    <td align="center" width="50%">

### ⚡ **Fun Facts**

- 📚 Passionate about clean code & best practices
- 🎯 Love solving complex algorithmic challenges
- 🌍 Active contributor to developer communities
- ☕ Powered by coffee and curiosity

</td>
  </tr>
</table>

---

## 📫 **Get In Touch**

<div align="center">

I'm always open to interesting conversations and collaboration opportunities!

<p>
  <a href="https://www.linkedin.com/in/robi-parvez" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Robiuzzaman_Parvez-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:parvezrobi@yahoo.com">
    <img src="https://img.shields.io/badge/Email-parvezrobi@yahoo.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://github.com/robiparvez" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-robiparvez-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
</p>

### 📍 **Location:** Dhaka, Bangladesh 🇧🇩

### 💼 **Company:** RedDot Digital Limited

### 🌐 **Portfolio:** [LinkedIn Profile](https://www.linkedin.com/in/robi-parvez)

</div>

---

## 📈 **Professional Metrics**

<div align="center">

| 📊 Metric | 📈 Value |
| ----------- | ---------- |
| **Total Repositories** | 48+ |
| **Years of Experience** | 10+ |
| **GitHub Followers** | 7+ |
| **Public Contributions** | Active |
| **Hireable Status** | ✅ Yes |

</div>

---

## 🌟 **Support & Acknowledgments**

<div align="center">

If you find my work helpful or interesting, consider:

⭐ **Starring** my repositories
🔄 **Sharing** with your network
🤝 **Contributing** to open source projects
💬 **Reaching out** for collaboration

---

<sub>**💜 Built with passion by Robiuzzaman Parvez**</sub>

<sub>Last Updated: December 25, 2025 | Made with ❤️ and ☕</sub>

![Wave](https://raw.githubusercontent.com/mayhemantt/mayhemantt/Update/svg/Bottom.svg)

</div>

<!--
  Accessibility Features:
  - Semantic HTML structure
  - Proper alt text for all images
  - High contrast color scheme
  - Readable typography with proper hierarchy
  - ARIA-friendly badges and links
  - Mobile-responsive layout
  - WCAG 2.1 AA compliant color contrast
-->

<!--
  SEO Optimization:
  - Descriptive headings and titles
  - Rich metadata through badges
  - Proper link structure
  - Keyword-rich content
  - Professional presentation
-->

<!--
  Enhanced Features (December 25, 2025):
  - Professional CSS animations with fade-in, slide-in, and hover effects
  - Animated skill proficiency bars with percentage indicators
  - Enhanced GitHub stats with PR metrics and reviews
  - Improved language statistics with custom titles
  - Responsive design with mobile-optimized animations
  - Accessibility-compliant animations (prefers-reduced-motion support)
  - Lightweight animations that don't impact performance
-->
