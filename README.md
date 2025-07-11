<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet" />
  <style>
    body {
      font-family: 'Inter', sans-serif;
      background-color: #fdfdfd;
      color: #222;
      max-width: 960px;
      margin: auto;
      padding: 2rem;
      line-height: 1.6;
    }

    h1, h2, h3 {
      font-weight: 600;
    }

    img.avatar {
      width: 180px;
      border-radius: 50%;
      margin-bottom: 0.3rem;
    }

    .intro {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
    }

    .intro img.gif {
      height: 160px;
    }

    .badge {
      display: inline-block;
      margin: 4px 4px;
    }

    .social-icons img {
      height: 30px;
      margin-right: 10px;
      vertical-align: middle;
      opacity: 0.8;
    }

    .social-icons img:hover {
      opacity: 1;
    }

    footer {
      text-align: center;
      margin-top: 4rem;
      color: #999;
    }

    .center {
      text-align: center;
    }

    .section {
      margin: 3rem 0;
    }

    .section img.gif {
      float: right;
      height: 170px;
    }
  </style>
</head>
<body>
  <div class="center">
    <img class="avatar" src="https://www.w3schools.com/howto/img_avatar.png" alt="Unknown Person" />
    <h2>Jose Luis Lopez</h2>
    <div class="social-icons">
      <a href="https://www.tupaginaweb.com" target="_blank" title="Página web">
        <img width="32" height="32" src="https://img.icons8.com/color/48/domain.png" alt="WWW" />
      </a>
      <a href="https://www.instagram.com/" target="_blank" title="Instagram">
        <img width="32" height="32" src="https://img.icons8.com/color/48/instagram-new--v1.png" alt="Instagram" />
      </a>
      <a href="https://www.linkedin.com/" target="_blank" title="LinkedIn">
        <img width="32" height="32" src="https://img.icons8.com/color/48/linkedin.png" alt="LinkedIn" />
      </a>
      <a href="mailto:correo@gmail.com" target="_blank" title="Gmail">
        <img width="32" height="32" src="https://img.icons8.com/color/48/gmail-new.png" alt="Gmail" />
      </a>
      <a href="https://www.youtube.com/" target="_blank" title="YouTube">
        <img width="32" height="32" src="https://img.icons8.com/color/48/youtube-play.png" alt="YouTube" />
      </a>
    </div>
  </div>
  <hr style="margin: 1.5rem auto; border: none; border-top: 2px solid #e0e0e0; width: 60%;" />
  <div class="intro" style="display: block;">
    <p>Hi there! I'm Jose Luis Lopez — but you can call me Joselu 🚀</p>
    <p>I'm currently studying Computer Engineering at the University of Granada, passionate about all things tech and beyond.</p>
  </div>
  
  <div class="section" style="margin-top: 0.1em;">
    <ul style="margin-top: 0.05em;">
      <li>🧠 Fascinated by Artificial Intelligence and Cybersecurity</li>
      <li>💻 Exploring the world of web & app development while diving deeper into advanced tech fields</li>
      <li>🛫 Huge fan of military aviation — yes, jets & afterburners are life 🔥</li>
      <li>🎯 Always learning, building, hacking: from hackathons to personal projects and internships</li>
      <li>🏋🏼‍♂️ Outside the screen, you'll find me training or geeking out over fighter jets</li>
    </ul>
  </div>
  
  <hr style="margin: 1.5rem auto; border: none; border-top: 2px solid #e0e0e0; width: 60%;" />
  <div class="section" style="margin-top: 0;">
    <div class="badges" style="display: flex; flex-direction: column; gap: 0.2em; align-items: center; background: #fafbfc; border-radius: 16px; padding: 6px 0 4px 0; box-shadow: 0 2px 8px 0 rgba(60,60,60,0.04);">
        <div style="width:100%;">
          <p style="margin-bottom: 0.15em;">🔧 Languages</p>
          <div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
            <img class="badge" src="https://img.shields.io/badge/JavaScript-F7DF1C?style=flat-square&logo=javascript&logoColor=323330" alt="JavaScript" />
            <img class="badge" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=fff" alt="TypeScript" />
            <img class="badge" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=fff" alt="Python" />
            <img class="badge" src="https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=fff" alt="Java" />
            <img class="badge" src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=fff" alt="C++" />
            <img class="badge" src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=sqlite&logoColor=fff" alt="SQL" />
            <img class="badge" src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=fff" alt="Bash" />
            <img class="badge" src="https://img.shields.io/badge/HTML5-E44D27?style=flat-square&logo=html5&logoColor=fff" alt="HTML5" />
            <img class="badge" src="https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css" alt="CSS" />
            <img class="badge" src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=fff" alt="C" />
          </div>
        </div>
        <!-- 🧰 Herramientas de Desarrollo -->
        <div style="width:100%;">
          <p style="margin-bottom: 0.15em;">🧰 Development Tools</p>
          <div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
            <img class="badge" src="https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visual%20studio%20code&logoColor=white" alt="VS Code" />
            <img class="badge" src="https://img.shields.io/badge/IntelliJ-000000?style=flat-square&logo=intellijidea&logoColor=fff" alt="IntelliJ" />
            <img class="badge" src="https://img.shields.io/badge/Vim-019733?style=flat-square&logo=vim&logoColor=fff" alt="Vim" />
            <img class="badge" src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=fff" alt="Git" />
            <img class="badge" src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=fff" alt="GitHub" />
            <img class="badge" src="https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=fff" alt="GitLab" />
            <img class="badge" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=fff" alt="Docker" />
            <img class="badge" src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=fff" alt="Postman" />
            <img class="badge" src="https://img.shields.io/badge/Homebrew-FBB040?style=flat-square&logo=homebrew&logoColor=fff" alt="Homebrew" />
            <img class="badge" src="https://img.shields.io/badge/NPM-CB3837?style=flat-square&logo=npm&logoColor=fff" alt="NPM" />
            <img class="badge" src="https://img.shields.io/badge/Yarn-2C8EBB?style=flat-square&logo=yarn&logoColor=fff" alt="Yarn" />
            <img class="badge" src="https://img.shields.io/badge/Cursor-292929?style=flat-square&logo=cursor&logoColor=white" alt="Cursor" />
          </div>
        </div>
        <!-- 📦 Frameworks y Librerías -->
        <div style="width:100%;">
          <p style="margin-bottom: 0.15em;">📦 Frameworks & Libraries</p>
          <div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
            <img class="badge" src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=fff" alt="React" />
            <img class="badge" src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vue.js&logoColor=fff" alt="Vue.js" />
            <img class="badge" src="https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=fff" alt="Angular" />
            <img class="badge" src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=fff" alt="Express.js" />
            <img class="badge" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=fff" alt="FastAPI" />
            <img class="badge" src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=fff" alt="Django" />
            <img class="badge" src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=fff" alt="Flask" />
            <img class="badge" src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=fff" alt="Node.js" />
            <img class="badge" src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=fff" alt="Next.js" />
            <img class="badge" src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=fff" alt="Spring Boot" />
            <img class="badge" src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=fff" alt="Tailwind CSS" />
            <img class="badge" src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=fff" alt="Bootstrap" />
            <img class="badge" src="https://img.shields.io/badge/Material%20UI-0081CB?style=flat-square&logo=mui&logoColor=fff" alt="Material UI" />
          </div>
        </div>
        <!-- ☁️ Tecnologías y Plataformas -->
        <div style="width:100%;">
          <p style="margin-bottom: 0.15em;">☁️ Technologies & Platforms</p>
          <div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
            <img class="badge" src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white" alt="AWS" />
            <img class="badge" src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=fff" alt="Firebase" />
            <img class="badge" src="https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=fff" alt="Netlify" />
            <img class="badge" src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=fff" alt="Vercel" />
            <img class="badge" src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=fff" alt="MongoDB" />
            <img class="badge" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=fff" alt="PostgreSQL" />
            <img class="badge" src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=fff" alt="MySQL" />
            <img class="badge" src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=fff" alt="Redis" />
            <img class="badge" src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=000" alt="Linux" />
            <img class="badge" src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=fff" alt="Nginx" />
            <img class="badge" src="https://img.shields.io/badge/Apache-D22128?style=flat-square&logo=apache&logoColor=fff" alt="Apache" />
          </div>
        </div>
        <!-- 🧪 Testing y CI/CD -->
        <div style="width:100%;">
          <p style="margin-bottom: 0.15em;">🧪 Testing & CI/CD</p>
          <div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
            <img class="badge" src="https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=fff" alt="Jest" />
            <img class="badge" src="https://img.shields.io/badge/Mocha-8D6748?style=flat-square&logo=mocha&logoColor=fff" alt="Mocha" />
            <img class="badge" src="https://img.shields.io/badge/Cypress-17202C?style=flat-square&logo=cypress&logoColor=fff" alt="Cypress" />
            <img class="badge" src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=fff" alt="GitHub Actions" />
            <img class="badge" src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=fff" alt="Jenkins" />
            <img class="badge" src="https://img.shields.io/badge/Travis%20CI-3EAAAF?style=flat-square&logo=travisci&logoColor=fff" alt="Travis CI" />
            <img class="badge" src="https://img.shields.io/badge/Docker%20Compose-2496ED?style=flat-square&logo=docker&logoColor=fff" alt="Docker Compose" />
            <img class="badge" src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=fff" alt="Kubernetes" />
          </div>
        </div>
        <!-- 🛠️ Otros -->
        <div style="width:100%;">
          <p style="margin-bottom: 0.15em;">🛠️ Others</p>
          <div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">
            <img class="badge" src="https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=figma&logoColor=fff" alt="Figma" />
            <img class="badge" src="https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=fff" alt="Notion" />
            <img class="badge" src="https://img.shields.io/badge/Trello-0052CC?style=flat-square&logo=trello&logoColor=fff" alt="Trello" />
            <img class="badge" src="https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=fff" alt="Jira" />
            <img class="badge" src="https://img.shields.io/badge/Markdown-000000?style=flat-square&logo=markdown&logoColor=fff" alt="Markdown" />
            <img class="badge" src="https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=fff" alt="LaTeX" />
            <img class="badge" src="https://img.shields.io/badge/Traefik-24A1C1?style=flat-square&logo=traefikmesh&logoColor=fff" alt="Traefik" />
          </div>
        </div>
      </div>

  <hr style="margin: 1.5rem auto; border: none; border-top: 2px solid #e0e0e0; width: 60%;" />
  <div class="center" style="margin-top: 1.5rem;">
    ⭐️ ⭐️ ⭐️  From JoseLu — Last update: 11 June 2025 ⭐️ ⭐️ ⭐️
  </div>

</body>
</html>
