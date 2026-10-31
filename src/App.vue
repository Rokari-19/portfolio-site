<script setup>
import { ref } from 'vue'
const menuOpen = ref(false)
const projects = [
 { number:'01 / PLATFORM', name:'Ryde Along', description:'A transport discovery concept helping people navigate routes, stops, transfers, and local knowledge.', tags:'PRODUCT · Django · Mapping', art:'art-blue', visual:'orbit' },
 { number:'02 / DEVELOPER TOOLING', name:'Database Migration Tool', description:'A modular migration system built around adapters, testing, and predictable database changes.', tags:'Python · Alembic · pytest', art:'art-silver', visual:'terminal' },
 { number:'03 / REAL-TIME', name:'Speechs', description:'A communication product exploring real-time audio, video, and reliable service integrations.', tags:'Flutter · WebRTC · Backend', art:'art-cream', visual:'wave' }
]
const skills=['Python','Django / DRF','FastAPI','PostgreSQL','AWS','Docker','Redis','React','Flutter']
const experience=[
 {date:'2025 — PRESENT',title:'Systems Engineer',company:'Bunker Seaworld',description:'Building and maintaining software systems, internal tooling, and infrastructure while contributing to technical direction and operational reliability.',type:'FULL-TIME'},
 {date:'2025',title:'Lead Backend Developer',company:'Zavod-IT',description:'Led backend delivery, coordinated engineering work, and designed services with an emphasis on maintainability and production readiness.',type:'REMOTE'},
 {date:'2022 — 2026',title:'B.Sc. Cyber Security',company:'Bingham University',description:'Studied secure systems, software, and the foundations of computing.',type:'EDUCATION'}
]
</script>
<template>
<header class="nav shell">
<a class="wordmark" href="#top" aria-label="Home">OI<span>.</span></a>
<button class="menu-toggle" :aria-expanded="menuOpen" aria-label="Toggle navigation" @click="menuOpen=!menuOpen">☰</button>
<nav :class="{'nav-open':menuOpen}" aria-label="Main navigation"><a href="#work" @click="menuOpen=false">Work</a><a href="#about" @click="menuOpen=false">About</a><a href="#experience" @click="menuOpen=false">Experience</a><a href="#contact" @click="menuOpen=false">Contact</a></nav>
<a class="nav-cta" href="#contact">Let’s talk <span>↗</span></a>
</header>
<main id="top">
<section class="hero shell"><div class="eyebrow"><span class="status"></span> AVAILABLE FOR SELECT PROJECTS <span class="mono">/ 2026</span></div><h1>Building useful<br><em>things that last.</em></h1><div class="hero-bottom"><p class="intro">I’m <strong>Oshomah Iyelobu</strong>, a software developer and systems engineer focused on thoughtful products, dependable backend systems, and infrastructure that stays out of the way.</p><a class="round-link" href="#work" aria-label="Explore selected work">↓</a></div><div class="hero-mark" aria-hidden="true">TWZ<span>—</span></div></section>
<section class="ticker" aria-label="Specialties"><div>BACKEND ENGINEERING <b>✳</b> SYSTEMS DESIGN <b>✳</b> CLOUD INFRASTRUCTURE <b>✳</b> PRODUCT DEVELOPMENT <b>✳</b> BACKEND ENGINEERING <b>✳</b></div></section>
<section id="work" class="section shell"><div class="section-head"><span class="kicker">01 / SELECTED WORK</span><p>Ideas made tangible.</p></div><div class="projects">
<article v-for="(project,index) in projects" :key="project.name" class="project" :class="{'project-feature':index===0}"><div class="project-art" :class="project.art"><span class="art-label">{{project.number}}</span><div v-if="project.visual==='orbit'" class="orbit"><i></i><i></i><i></i><b>RY</b></div><div v-else-if="project.visual==='terminal'" class="terminal"><span>migration.run()</span><small>→ schema checked<br>→ adapters loaded<br>→ changes applied</small></div><div v-else class="wave"><i v-for="n in 9" :key="n"></i></div></div><div class="project-info"><div><h3>{{project.name}}</h3><p>{{project.description}}</p></div><span class="tags">{{project.tags}}</span></div></article>
</div></section>
<section id="about" class="about"><div class="shell about-grid"><div><span class="kicker">02 / A LITTLE ABOUT ME</span><h2>Practical by nature.<br><em>Curious by default.</em></h2></div><div class="about-copy"><p>I work across the application and infrastructure layers: designing APIs, shaping data models, deploying services, and making the pieces behave together.</p><p>I care about clear architecture, useful abstractions, and shipping software that solves a real problem instead of merely adding another dashboard to the world.</p><div class="skills"><span v-for="skill in skills" :key="skill">{{skill}}</span></div></div></div></section>
<section id="experience" class="section shell"><div class="section-head"><span class="kicker">03 / EXPERIENCE</span><p>Where I’ve made an impact.</p></div><div class="timeline"><div v-for="role in experience" :key="role.title" class="role"><span class="date">{{role.date}}</span><div><h3>{{role.title}} <span>/ {{role.company}}</span></h3><p>{{role.description}}</p></div><span class="role-type">{{role.type}}</span></div></div></section>
<section class="quote shell"><span class="kicker">A WORKING PRINCIPLE</span><blockquote>“Good software should make the complicated feel <em>obvious.</em>”</blockquote></section>
<section id="contact" class="contact"><div class="shell contact-inner"><span class="kicker">04 / HAVE SOMETHING IN MIND?</span><h2>Let’s build<br><em>what should exist.</em></h2><div class="contact-bottom"><p>Open to thoughtful collaborations, challenging problems, and conversations about building better systems.</p><a class="contact-link" href="mailto:hello@example.com">hello@example.com <span>↗</span></a></div></div></section>
</main><footer class="footer shell"><a class="wordmark" href="#top">OI<span>.</span></a><p>Designed with intention. Built with care.</p><span class="mono">© 2026 / PORTFOLIO</span></footer>
</template>