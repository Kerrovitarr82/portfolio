<template>
  <div :class="['app', theme]">
    <nav class="navbar">
      <div class="nav-links">
        <a href="#about">О себе</a>
        <a href="#skills">Навыки</a>
        <a href="#experience">Опыт</a>
        <a href="#projects">Проекты</a>
        <a href="#contact">Контакты</a>
      </div>
    </nav>

    <header class="hero fade-in">
      <img src="https://avatars.githubusercontent.com/u/583231?v=4" alt="avatar" class="avatar" />
      <h1>Шатов Денис</h1>
      <p>Студент магистратуры РТУ МИРЭА</p>
      <blockquote>"Улыбаемся и машем"</blockquote>
    </header>

    <section id="about" class="section slide-up">
      <h2>О себе</h2>
      <p>
        Тут пока что пусто...
      </p>
    </section>

    <section id="skills" class="section colored fade-in">
      <h2>Навыки</h2>
      <div class="skills">
        <span>Golang</span><span>PostgreSQL</span><span>Docker</span><span>Git</span><span>REST API</span>
      </div>
    </section>

    <section id="experience" class="section slide-up">
      <h2>Опыт</h2>
      <div class="card">
        <h3>ООО "Крутая Контора" (2022–н.в.)</h3>
        <p>Разработчик крутого бэкенда</p>
      </div>
      <div class="card">
        <h3>Контора поменьше (2020–2022)</h3>
        <p>Разработчик бэкенда поменьше</p>
      </div>
    </section>

    <section id="projects" class="section colored fade-in">
      <h2>Проекты</h2>
      <ul class="projects">
        <li><strong>Крутой Бэкенд</strong> — участие в разработке бэкенда для банка</li>
        <li><strong>Средний Бэкенд</strong> — участие в разработке бэкенда для магазина</li>
        <li><strong>Вообще маленький Бэкенд</strong> — пет-проект для тренировки</li>
      </ul>
    </section>

    <footer id="contact" class="footer">
      <h2>Контакты</h2>
      <p><a href="mailto:pochta@example.com">pochta@example.com</a></p>
      <p><a href="https://github.com/Kerrovitarr82" target="_blank">github.com/Kerrovitarr82</a></p>
    </footer>
  </div>
</template>

<style>
/* Базовая тема */
:root {
  --bg: #fdfdfd;
  --text: #1f1f1f;
  --accent: #0077ff;
  --muted: #666;
  --card-bg: #ffffff;
}
.dark {
  --bg: #121212;
  --text: #f1f1f1;
  --accent: #66ffe0;
  --muted: #aaa;
  --card-bg: #1e1e1e;
}

body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  background-color: var(--bg);
  color: var(--text);
  transition: background-color 0.5s, color 0.5s;
}
.app {
  transition: all 0.3s ease;
}
.navbar {
  background: var(--accent);
  color: white;
  padding: 1rem 0;
  text-align: center;
}
.nav-links {
  display: inline-flex;
  gap: 1.5rem;
  flex-wrap: wrap;
}
.nav-links a {
  color: white;
  font-weight: bold;
  text-decoration: none;
  transition: opacity 0.3s;
}
.nav-links a:hover {
  opacity: 0.7;
}
.hero {
  text-align: center;
  padding: 60px 20px;
}
.avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin-bottom: 15px;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.2);
}
.hero blockquote {
  font-style: italic;
  color: var(--muted);
}
.section {
  padding: 60px 20px;
  max-width: 900px;
  margin: auto;
}
.colored {
  background: rgba(0, 0, 0, 0.03);
}
.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}
.skills span {
  background: var(--accent);
  color: white;
  padding: 6px 12px;
  border-radius: 999px;
  font-size: 14px;
  animation: fadeInUp 0.4s ease-in-out;
}
.card {
  background-color: var(--card-bg);
  transition: background-color 0.5s;
  box-shadow: 0 4px 10px rgba(0,0,0,0.05);
  border-radius: 10px;
  padding: 20px;
  margin-bottom: 20px;
}
.projects {
  list-style: none;
  padding: 0;
}
.projects li {
  margin-bottom: 10px;
}
.footer {
  text-align: center;
  padding: 40px 20px;
  background: var(--accent);
  color: white;
}
.footer a {
  color: white;
  text-decoration: none;
}
.signature {
  margin-top: 10px;
  font-size: 12px;
  opacity: 0.7;
}



/* Анимации */
.fade-in {
  animation: fadeIn 1s ease-out;
}
.slide-up {
  animation: slideUp 1s ease-out;
}
@keyframes fadeIn {
  from { opacity: 0 }
  to { opacity: 1 }
}
@keyframes slideUp {
  from { transform: translateY(20px); opacity: 0 }
  to { transform: translateY(0); opacity: 1 }
}
@keyframes fadeInUp {
  from { transform: translateY(10px); opacity: 0 }
  to { transform: translateY(0); opacity: 1 }
}
</style>
