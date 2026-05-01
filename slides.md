---
theme: default
title: 'LyonCraft 2026 - Rémy Cassagne'
author: Rémy Cassagne
fonts:
  sans: Inter
  display: Bebas Neue
  mono: Fira Code
transition: slide-left
colorSchema: dark
aspectRatio: 16/9
canvasWidth: 980
---

<!--
=================================================
  SLIDE 1 — COVER
=================================================
-->

<div class="cover-frame">
  <div class="cover-door-left" />
  <div class="cover-door-right" />
</div>

<div class="cover-content" v-motion :initial="{ opacity: 0, y: 30 }" :enter="{ opacity: 1, y: 0, transition: { duration: 800 } }">
  <p class="cover-tag">Rémy Cassagne - LyonCraft 2026</p>
  <div class="cover-title-container">
  <h1 class="cover-title">Développeur <br>par obstination</h1>
    <h3 class="cover-sub">
      Ou comment les galères valent mieux que les filières
    </h3>
  </div>
</div>

<style>
  .cover-frame {
    position: absolute;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
  }
  .cover-door-left,
  .cover-door-right {
    position: absolute;
    bottom: -20px;
    width: 160px;
    height: 260px;
    border-radius: 50% 50% 0 0 / 20% 20% 0 0;
    border: 3px solid;
    opacity: 0.12;
  }
  .cover-door-left  { left: 40px;  border-color: #52b788; box-shadow: 0 0 40px rgba(82,183,136,0.7); }
  .cover-door-right { right: 40px; border-color: #4895ef; box-shadow: 0 0 40px rgba(72,149,239,0.7); }

  .cover-content {
    position: relative; 
    z-index: 2; 
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }
  .cover-tag {
    font-family: 'Inter', sans-serif;
    font-size: 0.85rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--factory-orange);
  }
  .cover-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1rem;
    color: #ffffff;
    text-shadow: 0 0 80px rgba(72,149,239,0.25);
  }
  .cover-sub {
    font-family: 'Inter', sans-serif;
    font-size: 1.5rem;
    color: #ffffff;
  }
</style>

<!--
Phrase d'intro 
-->

---
layout: center
title: "Question d'accroche"
---
<!-- ================================================
     SLIDE 2 — QUESTION D'ACCROCHE
================================================= -->

<div class="hook-slide" v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 600 } }">
  <p class="hook-question">Comment passe-t-on de<br><strong>vendeur de surgelés porte à porte</strong><br>à<br><strong>dev fullstack en production</strong><br>sur un site e-commerce avec des milliers d'users ?</p>
</div>

<style>
  .hook-slide { text-align: center; }
  .hook-question {
    font-family: 'Bebas Neue', sans-serif !important;
    font-size: 2.8rem;
    line-height: 1.3;
    color: #e8f0fe;
  }
  .hook-question strong { color: var(--factory-orange); }
</style>


---
layout: center
title: "Le parcours"
---
<!-- ================================================
     SLIDE 3 — LE PARCOURS
================================================= -->

<div class="parcours-block" v-motion :initial="{ opacity: 0, y: 20 }" :enter="{ opacity: 1, y: 0, transition: { duration: 700 } }">
  <div class="parcours-list">
    <div v-click class="parcours-item parcours-blocked">Pas de bac. Pas de diplômes.</div>
    <div v-click class="parcours-item parcours-blocked">Deux piscines de l'école 42 échouées.</div>
    <div v-click class="parcours-item parcours-blocked">Une école abandonnée. Un bootcamp.</div>
    <div v-click class="parcours-item parcours-blocked">Six mois sans mission et des centaines de refus.</div>
    <div v-click class="parcours-reveal">Et pourtant, me voilà devant vous.</div>
  </div>
</div>

<style>
  .parcours-block {
    text-align: center;
  }
  .parcours-list {
    display: flex;
    flex-direction: column;
    gap: 0.7rem;
    align-items: center;
  }
  .parcours-item {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 2rem;
    line-height: 1.2;
  }
  .parcours-reveal {
    margin-top: 1rem;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 2.6rem;
    color: #ffffff;
    text-shadow: 0 0 90px rgba(252,191,73,0.6), 0 0 10px #ffb300;
  }
</style>

<!-- Transition : Je vais vous expliquer pourquoi tout ce qui n'a pas marché
est exactement ce qui m'a construit -->

---
layout: statement
title: "La thèse"
---
<!-- ================================================
     SLIDE 4 — THÈSE
     ================================================ -->

<h3 class="thesis-text" v-motion :initial="{ opacity: 0, y: 20 }" :enter="{ opacity: 1, y: 0, transition: { duration: 700 } }">
  Ce qui m'a construit comme développeur,<br>
  c'est <span class="highlight-orange">pas la formation</span> que j'ai suivie.<br>
  C'est tout ce que j'ai <span class="highlight-orange">traversé</span> avant, pendant, et autour.
</h3>

<style>
  .thesis-text {
    text-align: center;
    font-size: 2rem;
    line-height: 1.5;
  }
</style>


---
layout: center
title: "Plan du talk"
---
<!-- ================================================
     SLIDE 5 — PLAN DU TALK
     ================================================ -->

<h1 class="plan-title">Aujourd'hui en 3 actes :</h1>

<div class="plan-grid">
  <div v-click class="plan-item plan-green">
    <div class="plan-door" style="border-color: #52b788; box-shadow: 0 0 20px rgba(82,183,136,0.3)" />
    <div class="plan-text">
      <h3 class="plan-act">Acte 1</h3>
      <h4 class="plan-label">Ce que la vente m'a appris<br>avant le code</h4>
    </div>
  </div>
  <div v-click class="plan-item plan-blue">
    <div class="plan-door" style="border-color: #4895ef; box-shadow: 0 0 20px rgba(72,149,239,0.3)" />
    <div class="plan-text">
      <h3 class="plan-act">Acte 2</h3>
      <h4 class="plan-label">Les portes fermées<br>comme moteur</h4>
    </div>
  </div>
  <div v-click class="plan-item plan-red">
    <div class="plan-door" style="border-color: #e63946; box-shadow: 0 0 20px rgba(230,57,70,0.3)" />
    <div class="plan-text">
      <h3 class="plan-act">Acte 3</h3>
      <h4 class="plan-label">Arriver en prod<br>sans filet</h4>
    </div>
  </div>
</div>

<style>
  .plan-title {
    text-align: center;
    font-size: 2.5rem;
    padding-bottom: 3.5rem;
  }
  .plan-grid {
    display: flex;
    gap: 3rem;
    justify-content: center;
  }
  .plan-item {
    display: flex;
    align-items: center;
    gap: 1rem;
  }
  .plan-door {
    width: 50px; height: 85px;
    border-radius: 40% 40% 0 0 / 20% 20% 0 0;
    border: 2px solid;
    flex-shrink: 0;
  }
  .plan-act {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 1.3rem;
    letter-spacing: 0.2em;
  }
  .plan-label {
    font-size: 1rem;
    line-height: 1.4;
  }
  .plan-green .plan-act { color: #52b788; }
  .plan-blue  .plan-act { color: #4895ef; }
  .plan-red   .plan-act { color: #e63946; }
</style>

---
layout: full
title: "Acte 1 - Ce que la vente m'a appris avant le code"
---
<!-- ================================================
     SLIDE 6 — SECTION ACTE 1 - Ce que la vente m'a appris avant le code
     ================================================ -->

<Door
  color="#52b788"
  darkColor="#2d6a4f"
  number="ACTE 01"
  act="Acte 1"
  title="Ce que la vente m'a appris avant le code"
/>

---
layout: cover
title: "La vente porte à porte"
---
<!-- ================================================
     SLIDE 7 — SETUP VENTE
     ================================================ -->

<SequenceBlock badge="" badge-color="#52b788" title="La vente porte à porte">
  <TimelineItem v-click>
    <p>Inconnus -> Rentrer chez des gens qu'on connaît pas.</p>
  </TimelineItem>
  <TimelineItem v-click>
    <p>Terrain difficile -> Circulation, accès à certains lieux ...</p>
  </TimelineItem>
  <TimelineItem v-click variant="blocked">
    <p>Refus constants -> Mauvais résultats.</p>
  </TimelineItem>
</SequenceBlock>


---
layout: cover
title: "Compétence 1 - Définir le besoin"
---
<!-- ================================================
     SLIDE 8 — COMPÉTENCE 1 - Définir le besoin avant d'agir
     ================================================ -->

<SkillCompare number="01" title="Définir le besoin avant d'agir" color-hex="#52b788" left-context="En vente" right-context="Chez Oli's Lab">
  <template #left>
    <p>Pas de pitch sans comprendre ce que le client veut vraiment. Poser des questions d'abord.</p>
  </template>
  <template #right>
    <p>"C'est quoi l'objectif métier derrière cette feature ?"<br>"Pourquoi on fait ça comme ça et pas autrement ?"</p>
  </template>
</SkillCompare>


---
layout: cover
title: "Compétence 2 - Poser les bonnes questions"
---
<!-- ================================================
     SLIDE 9 — COMPÉTENCE 2 - Poser les bonnes questions vite
     ================================================ -->

<SkillCompare number="02" title="Poser les bonnes questions vite" color-hex="#52b788" left-context="En vente" right-context="Codebase legacy">
  <template #left>
    <p>30 secondes pour qualifier un prospect. Aller à l'essentiel. Identifier les noeuds.</p>
  </template>
  <template #right>
    <p>Peu de temps pour comprendre avant d'agir. Même réflexe : pas tout lire, trouver les points d'entrée.</p>
  </template>
</SkillCompare>


---
layout: cover
title: "Compétence 3 - L'inconnu"
---
<!-- ================================================
     SLIDE 10 — COMPÉTENCE 3 - Ne pas avoir peur de l'inconnu
     ================================================ -->

<SkillCompare number="03" title="Ne pas avoir peur de l'inconnu" color-hex="#52b788" left-context="En vente" right-context="En prod">
  <template #left>
    <p>Taper des portes d'inconnus, ça forge. Même taper celle de son voisin on a du mal au début.</p>
  </template>
  <template #right>
    <p>Hériter d'une codebase sans tests, sans doc, sans filet... et ne pas paniquer.</p>
    <p v-click style="color: #19e67b; margin-top: 0.5rem; font-weight: 600;">Ce n'est pas du courage, c'est de l'habitude.</p>
  </template>
</SkillCompare>

<!--
Transition : "Mais avant d'arriver là, il y a eu beaucoup de portes — et pas celles que j'avais choisies de frapper."
-->


---
layout: full
title: "Acte 2 - Les portes fermées"
---
<!-- ================================================
     SLIDE 11 — SECTION ACTE 2 - Les portes fermées comme moteur
     ================================================ -->

<Door
  color="#4895ef"
  darkColor="#1e3a5f"
  number="ACTE 02"
  act="Acte 2"
  title="Les portes fermées comme moteur"
/>


---
layout: cover
title: "42 - Piscine #1"
---
<!-- ================================================
     SLIDE 12 — 42 PISCINE #1
     ================================================ -->

<SequenceBlock badge="Séquence 1" badge-color="#4895ef" title="42 - Piscine #1">
  <TimelineItem v-click>
    <p>Déclic intellectuel immédiat. Je fais la piscine. J'accroche tout de suite.</p>
  </TimelineItem>
  <TimelineItem v-click variant="blocked">
    <p><strong>Refusé</strong> sans feedback -> Le vide.</p>
  </TimelineItem>
  <TimelineItem v-click>
    <p>Réponse -> Retourner vendre, mais apprendre le C en parallèle. Seul. Sans cours, sans cadre.</p>
  </TimelineItem>
</SequenceBlock>


---
layout: cover
title: "42 - Piscine #2"
---
<!-- ================================================
     SLIDE 13 — 42 PISCINE #2
     ================================================ -->

<SequenceBlock badge="Séquence 1 - suite" badge-color="#4895ef" title="42 - Piscine #2">
  <TimelineItem v-click>
    <p>Un an plus tard. Je suis meilleur, je le sais, je le sens -> Plus rapide, plus structuré.</p>
  </TimelineItem>
  <TimelineItem v-click variant="blocked">
    <p><strong>Refusé à nouveau.</strong> Toujours sans feedback -> Introspection</p>
  </TimelineItem>
  <TimelineItem v-click>
    <p>Vivre avec l'absence de réponse -> Décider quand même de continuer.</p>
  </TimelineItem>
</SequenceBlock>


---
layout: statement
title: "Le blocage redirige"
---
<!-- ================================================
     SLIDE 14 — Le blocage redirige
     ================================================ -->

<div v-motion :initial="{ opacity: 0, scale: 0.9 }" :enter="{ opacity: 1, scale: 1, transition: { duration: 600 } }">
  <p class="statement-text">Le blocage <strong class="highlight-orange">ne m'arrête pas</strong>.</p>
  <p class="statement-text">Il me <strong class="highlight-orange">redirige</strong>.</p>
</div>


---
layout: default
title: "Ada + 6 mois solo"
---
<!-- ================================================
     SLIDE 15 — ADA + 6 MOIS SOLO
     ================================================ -->

<SequenceBlock badge="Séquence 2" badge-color="#4895ef" title="Ada Tech School + 6 mois seul">
  <TimelineItem v-click>
    <p>Ada Tech School : bases web, JS, front, premiers projets.<br>Découverte de <strong>mes premiers meetups</strong>.</p>
  </TimelineItem>
  <TimelineItem v-click variant="blocked">
    <p>Décalage entre ce qui est affiché et ce qui est vécu.<br><strong>Ce n'est pas un abandon, c'est une décision.</strong></p>
  </TimelineItem>
  <TimelineItem v-click variant="insight">
    <p>6 mois seul. Boulot alimentaire et en parallèle -> TypeScript, React, Next.js, Portfolio.<br>
    <strong>Je ne suis pas un cursus, je construis ma progression.</strong></p>
  </TimelineItem>
</SequenceBlock>


---
layout: two-cols
title: "La culture technique"
---
<!-- ================================================
     SLIDE 16 — LES LECTURES
     ================================================ -->

::default::

<div style="height: 100%;" v-motion :initial="{ x: -20, opacity: 0 }" :enter="{ x: 0, opacity: 1 }">
  <Tag variant="blue" label="Pendant ces 6 mois" style="margin-bottom: 1.2rem;" />
  <div style="height: 100%; display: flex; align-items: center; padding-bottom: 6rem;">
    <h2 style="font-size: 2.4rem; margin-bottom: 1.2rem;">Je construis<br>une culture technique</h2>
  </div>
</div>

::right::

<div class="books-list" v-motion :initial="{ x: 20, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { delay: 200 } }">
  <div v-click class="book-item">
    <div class="book-spine" style="background: #4895ef;" />
    <div>
      <div class="book-title">Software Craft</div>
      <div class="book-author">Cyril Martraire et al.</div>
    </div>
  </div>
  <div v-click class="book-item">
    <div class="book-spine" style="background: #4895ef;" />
    <div>
      <div class="book-title">Clean Code</div>
      <div class="book-author">Robert C. Martin</div>
    </div>
  </div>
  <div v-click class="book-item">
    <div class="book-spine" style="background: #4895ef;" />
    <div>
      <div class="book-title">Itération Product(ives)</div>
      <div class="book-author">Colin Damon</div>
    </div>
  </div>
</div>

<style>
  .books-list { display: flex; flex-direction: column; gap: 1.2rem; justify-content: center; height: 100%; padding: 1rem; }
  .book-item { display: flex; align-items: center; gap: 1rem; padding: 0.8rem 1rem; background: rgba(255,255,255,0.04); border-radius: 8px; border: 1px solid rgba(255,255,255,0.08); }
  .book-spine { width: 6px; height: 50px; border-radius: 3px; flex-shrink: 0; }
  .book-title { font-family: 'Bebas Neue', sans-serif; font-size: 1.6rem; color: #ffffff; }
  .book-author { font-size: 1rem; color: #ffffff; margin-top: 0.2rem; }
</style>

<!--
À l'époque je pensais juste survivre.
Avec le recul, je construisais quelque chose que personne ne m'aurait enseigné si j'avais suivi un parcours classique.
-->

---
layout: center
title: "Le Wagon"
---
<!-- ================================================
     SLIDE 17 — LE WAGON
     ================================================ -->

<div>
  <Tag variant="blue" label="Séquence 3" style="margin-bottom: 2rem;" />
  <h1>Le Wagon</h1>

  <div class="wagon-grid">
    <div v-click class="wagon-card">
      <div class="wagon-icon">⚡</div>
      <p>J'arrive avec une longueur d'avance.</p>
    </div>
    <div v-click class="wagon-card">
      <div class="wagon-icon">🚂</div>
      <p>Le Wagon apporte Ruby + structure + diplôme.</p>
    </div>
    <div v-click class="wagon-card wagon-card-highlight">
      <div class="wagon-icon">🔥</div>
      <p><strong>L'autodidaxie n'est pas un palliatif, c'est une méthode.</strong></p>
    </div>
  </div>
</div>

<style>
  .wagon-block h1 { 
    font-family: 'Bebas Neue', sans-serif; 
    color: #ffffff;
  }
  .wagon-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.2rem;
  }
  .wagon-card {
    padding: 1.2rem;
    background: rgba(255,255,255,0.04);
    border-radius: 10px;
    border: 1px solid rgba(255,255,255,0.08);
  }
  .wagon-card-highlight {
    background: rgba(72,149,239,0.08);
    border-color: rgba(72,149,239,0.3);
  }
  .wagon-icon {
    font-size: 1.8rem;
  }
  .wagon-card p {
    margin: 0;
    font-size: 1rem;
    line-height: 1.6;
  }
  .wagon-card strong {
    color: #4895ef;
  }
</style>

<!--
Transition : Mais apprendre seul dans son coin, c'est une chose. <br>Livrer en production, c'est une autre.
-->


---
layout: full
title: "Acte 3 - Prod sans filet"
---
<!-- ================================================
     SLIDE 18 — SECTION ACTE 3 (PORTE ROUGE)
     ================================================ -->

<Door
  color="#e63946"
  darkColor="#9b2226"
  number="ACTE 03"
  act="Acte 3"
  title="Arriver en prod sans filet"
/>


---
layout: cover
title: "KicksFolio"
---
<!-- ================================================
     SLIDE 19 — KICKSFOLIO
     ================================================ -->

<div class="prod-block">
  <Tag variant="red" label="KicksFolio" style="margin-bottom: 1rem;" />
  <h2>App mobile sneakers</h2>

  <div class="prod-grid">
    <div class="prod-desc">
      <p v-click>App mobile sneakers pour gérer sa collection et la partager.<br>Deux centres d'intérêt qui se rejoignent.</p>
      <p v-click>Je vais jusqu'au bout. <span class="highlight-orange">Publiée sur les stores.</span></p>
    </div>
    <img src="./assets/images/kicksfolio.jpg" alt="KicksFolio" class="kicksfolio-screenshot" />
  </div>
</div>

<style>
  .prod-block { padding: 1rem 2rem; }
  .prod-block h2 { font-size: 2.6rem; margin: 0.2rem 0 1.5rem; }
  .prod-grid { display: flex; gap: 2rem; }
  .prod-desc p { font-size: 1.05rem; line-height: 1.4; }
  .prod-desc strong { color: #ffffff; }
  .kicksfolio-screenshot { width: 300px; height: auto; object-fit: contain; border-radius: 10px; box-shadow: 0 0 20px rgba(255, 255, 255, 0.5); }
</style>

<!--
Transition : KicksFolio m'a appris ce qu'aucun bootcamp n'enseigne : le coût réel d'aller jusqu'au bout.
-->

---
layout: center
title: "La période creuse"
---
<!-- ================================================
     SLIDE 20 — PÉRIODE CREUSE
     ================================================ -->

<div class="creuse-block">
  <Tag variant="red" label="La période creuse" style="margin-bottom: 1rem;" />
  <h2>6 mois, et des centaines de refus.</h2>

  <div class="creuse-content">
    <div v-click class="creuse-stat">
      <div class="stat-number highlight-red">6</div>
      <div class="stat-label">mois sans mission</div>
    </div>
    <div class="creuse-divider" />
    <div v-click class="creuse-text">
      <p>Pas bloqué sur la technique. Bloqué sur <strong>comment raconter le parcours atypique</strong> sans le défendre.</p>
      <p v-click>Comment se présenter quand on n'a pas le parcours qu'on attendait de toi ?</p>
    </div>
  </div>
</div>

<style>
  .creuse-block { padding: 1rem 2rem; }
  .creuse-block h2 { font-size: 2.6rem; margin: 0.2rem 0 1.5rem; }
  .creuse-content { display: flex; align-items: center; gap: 2.5rem; }
  .creuse-stat { text-align: center; flex-shrink: 0; }
  .stat-number { font-family: 'Bebas Neue', sans-serif; font-size: 7rem; line-height: 1; }
  .stat-label { font-size: 0.9rem; letter-spacing: 0.15em; text-transform: uppercase; color: #8faac3; }
  .creuse-divider { width: 2px; height: 120px; background: rgba(230,57,70,0.3); flex-shrink: 0; }
  .creuse-text p { font-size: 1.1rem; line-height: 1.7; margin-bottom: 0.8rem; }
  .creuse-text strong { color: #ffffff; }
</style>


---
layout: statement
title: "Savoir se vendre"
---
<!-- ================================================
     SLIDE 21 — STATEMENT SAVOIR SE VENDRE
     ================================================ -->

<div v-motion :initial="{ opacity: 0, y: 20 }" :enter="{ opacity: 1, y: 0, transition: { duration: 600 } }">
  <p class="statement-text">Savoir <strong class="highlight-orange">vendre</strong>, c'est bien.</p>
  <p class="statement-text">Savoir <strong class="highlight-orange">se vendre</strong>, c'est mieux.</p>
</div>

---
layout: default
title: "Le post LinkedIn"
---
<!-- ================================================
     SLIDE 22 — LE POST LINKEDIN
     ================================================ -->

<div class="linkedin-block">
  <Tag variant="red" label="Le post LinkedIn" style="margin-bottom: 1rem;" />
  <h2>Demander de l'aide publiquement</h2>

  <div class="linkedin-grid">
    <img src="./assets/images/linkedin-post.png" alt="LinkedIn post" class="lk-content" />
    <div class="linkedin-result" v-click>
      <p class="result-item"><span class="result-icon">📅</span> Agenda rempli en quelques jours</p>
      <p class="result-item"><span class="result-icon">👥</span> Plus d'une dizaine de personnes</p>
      <p class="result-item"><span class="result-icon">🎯</span> Simulations d'entretien, retours francs</p>
      <p v-click class="result-highlight">C'est ce post qui a tout débloqué.</p>
    </div>
  </div>
</div>

<style>
  .linkedin-block { 
    padding: 1rem 2rem; 
  }
  .linkedin-block h2 { 
    font-size: 2.6rem; 
    margin: 0.2rem 0 1.5rem; 
  }
  .linkedin-grid { 
    display: grid; 
    grid-template-columns: 1fr 1fr; 
    gap: 2rem; 
    align-items: start; 
  }
  .lk-subtitle { 
    font-size: 0.75rem; 
    color: #8faac3; 
    margin-top: 0.5rem;
    padding: 0.8rem 1rem;
    background: rgba(72,149,239,0.07);
    border: 1px solid rgba(72,149,239,0.18);
    border-radius: 6px;
  }
  .lk-content { 
    font-size: 0.9rem; 
    line-height: 1.6; 
    color: #c5d5e8; 
    margin: 0; 
    margin-top: 0.5rem;
    padding: 0.8rem 1rem;
    background: rgba(72,149,239,0.07);
    border: 1px solid rgba(72,149,239,0.18);
    border-radius: 6px;
  }
  .linkedin-result { 
    display: flex; 
    flex-direction: column;  
  }
  .result-item { 
    display: flex; 
    align-items: center; 
    gap: 0.8rem; 
    font-size: 1rem; 
    color: #e8f0fe; 
    margin-top: 0.5rem;
    padding: 0.8rem 1rem;
    background: rgba(72,149,239,0.07);
    border: 1px solid rgba(72,149,239,0.18);
    border-radius: 6px;
  }
  .result-icon { 
    font-size: 1.2rem; 
  }
  .result-highlight {
    margin-top: 0.5rem;
    padding: 0.8rem 1rem;
    background: rgba(72,149,239,0.1);
    border: 1px solid rgba(72,149,239,0.3);
    border-radius: 6px;
    color: var(--factory-orange);
    font-size: 1rem;
    font-weight: 700;
  }
</style>


---
layout: center
title: "Oli's Lab - La boucle"
---
<!-- ================================================
     SLIDE 23 — OLI'S LAB : LA BOUCLE
     ================================================ -->

<div class="boucle-block">
  <Tag variant="red" label="Oli's Lab" style="margin-bottom: 1rem;" />
  <h2>La boucle se ferme</h2>

  <div class="boucle-grid">
    <div v-click class="boucle-mission">
      <p class="bm-label" style="color: #e63946;">La mission</p>
      <ul>
        <li>Codebase legacy, sans tests, sans doc</li>
        <li>Migration Next.js prévue, pas commencée</li>
        <li>CMS Payload à construire de zéro</li>
      </ul>
    </div>
    <div v-click class="boucle-arrow">
      <div class="ba-line" />
      <div class="ba-icon">↩</div>
    </div>
    <div v-click class="boucle-link">
      <p class="bm-label" style="color: #52b788;">Le lien</p>
      <p class="boucle-link-text">Ne pas avoir peur de l'inconnu, appris en sonnant des portes <strong>=</strong> naviguer dans cette codebase sans paniquer.</p>
      <p v-click class="highlight-orange">C'est de l'habitude.</p>
    </div>
  </div>
</div>

<style>
  .boucle-block { padding: 1rem 2rem; }
  .boucle-block h2 { font-size: 2.6rem; margin: 0.2rem 0 1.5rem; }
  .boucle-grid { display: grid; grid-template-columns: 1fr 60px 1fr; gap: 1rem; align-items: center; }
  .boucle-mission { padding: 1.2rem; background: rgba(230,57,70,0.05); border: 1px solid rgba(230,57,70,0.2); border-radius: 10px; }
  .boucle-mission ul { list-style: none; padding: 0; display: flex; flex-direction: column; gap: 0.2rem; }
  .bm-label { font-family: 'Bebas Neue', sans-serif; letter-spacing: 0.15em; font-size: 1.3rem }
  .boucle-mission li { font-size: 1rem; padding-left: 1rem; position: relative; }
  .boucle-mission li::before { content: '▸'; color: #e63946; position: absolute; left: 0; }
  .boucle-arrow { display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 0.3rem; }
  .ba-line { width: 2px; height: 90px; background: linear-gradient(to bottom, rgba(230,57,70,0.4), rgba(82,183,136,0.4)); }
  .ba-icon { font-size: 2rem; color: #8faac3; }
  .boucle-link { padding: 1.2rem; background: rgba(82,183,136,0.05); border: 1px solid rgba(82,183,136,0.2); border-radius: 10px; }
  .boucle-link-text { font-size: 1rem; line-height: 1.6; margin-bottom: 0.5rem; }
</style>


---
layout: full
title: "Conclusion"
---
<!-- ================================================
     SLIDE 24 — SECTION CONCLUSION (PORTE DORÉE)
     ================================================ -->

<Door
  color="#fcbf49"
  darkColor="#f77f00"
  number="FIN"
  act="Conclusion"
  title="Ce qui nous forge en tant que développeur"
/>


---
layout: center
title: "Le même pattern, trois fois"
---
<!-- ================================================
     SLIDE 25 — RECAP DES PATTERNS
     ================================================ -->

<h1 style="text-align:center; margin-bottom: 2rem;">Le même pattern, trois fois</h1>

<div class="recap-list">
  <div v-click class="recap-item">
    <div class="recap-dot" style="background: #52b788;" />
    <div>
      <div class="recap-label">42 × 2</div>
      <div class="recap-text">Blocage → Apprendre le C seul → Continuer</div>
    </div>
  </div>
  <div v-click class="recap-item">
    <div class="recap-dot" style="background: #4895ef;" />
    <div>
      <div class="recap-label">Ada + 6 mois solo</div>
      <div class="recap-text">Décision → Stack autodidacte → Culture craft</div>
    </div>
  </div>
  <div v-click class="recap-item">
    <div class="recap-dot" style="background: #e63946;" />
    <div>
      <div class="recap-label">Le Wagon → Oli's Lab</div>
      <div class="recap-text">Validation → Prod → La boucle se ferme</div>
    </div>
  </div>
  <div v-click class="recap-conclusion">
    À chaque fois une progression que <strong>personne ne m'aurait donnée autrement</strong>.
  </div>
</div>

<style>
  .recap-list { display: flex; flex-direction: column; gap: 1.2rem; max-width: 700px; }
  .recap-item { display: flex; align-items: center; gap: 1.2rem; padding: 0.9rem 1.2rem; background: rgba(255,255,255,0.04); border-radius: 8px; border: 1px solid rgba(255,255,255,0.08); }
  .recap-dot { width: 12px; height: 12px; border-radius: 50%; flex-shrink: 0; }
  .recap-label { font-family: 'Bebas Neue', sans-serif; font-size: 1.3rem; letter-spacing: 0.1em; color: #ffffff; }
  .recap-text { font-size: 1.1rem; color: #ffffff; margin-top: 0.2rem; }
  .recap-conclusion { padding: 1rem 1.2rem; background: rgba(252,191,73,0.06); border: 1px solid rgba(252,191,73,0.2); border-radius: 8px; font-size: 1.1rem;  color: #e8f0fe; }
  .recap-conclusion strong { color: #fcbf49; }
</style>


---
layout: cover
title: "La boucle Colin"
---
<!-- ================================================
     SLIDE 26 — LA BOUCLE COLIN
     ================================================ -->

<h2 class="slide-h2-centered">Ce que le craft fait en dehors des lignes de code : <br>il <strong class="highlight-orange">crée des cercles</strong> où les gens se retrouvent.</h2>

<!--
Clin d'oeil à Colin, la boucle est bouclée.
-->

---
layout: cover
title: "Phrase de sortie"
---
<!-- ================================================
     SLIDE 27 — PHRASE DE SORTIE
     ================================================ -->

<div v-motion :initial="{ opacity: 0, y: 30 }" :enter="{ opacity: 1, y: 0, transition: { duration: 800 } }">
  <h2 class="slide-h2-centered">Ce qui nous forge en tant que développeur,<br>c'est <strong class="highlight-orange">pas la formation</strong> qu'on a suivie.<br>
    C'est la <strong class="highlight-orange">culture</strong> qu'on se crée en route.
  </h2>
</div>


---
layout: end
title: "Merci"
---
<!-- ================================================
     SLIDE 28 — FIN / MERCI
     ================================================ -->

<div class="end-content" v-motion :initial="{ opacity: 0 }" :enter="{ opacity: 1, transition: { duration: 600 } }">
  <h1 class="end-name">Rémy Cassagne <br>Développeur par obstination</h1>
  <div class="end-handles">
    <span>@remyShift</span>
  </div>
  <div class="container">
    <img src="/assets/images/qr-linkedin-github.png" alt="QR Code LinkedIn" class="end-qr" />
    <div class="end-doors">
      <div class="end-door" style="border-color: #52b788; box-shadow: 0 0 15px rgba(82,183,136,0.3)" />
      <div class="end-door" style="border-color: #4895ef; box-shadow: 0 0 15px rgba(72,149,239,0.3)" />
      <div class="end-door" style="border-color: #e63946; box-shadow: 0 0 15px rgba(230,57,70,0.3)" />
      <div class="end-door" style="border-color: #fcbf49; box-shadow: 0 0 15px rgba(252,191,73,0.3)" />
    </div>
    <img src="/assets/images/qr-lyon-craft-feedback.png" alt="QR Code LyonCraft Feedback" class="end-qr feedback-qr" />
  </div>
</div>

<style>
  .end-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
    gap: 1.2rem;
    text-align: center;
  }
  .end-name {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 3.5rem;
    line-height: 1;
    color: #ffffff;
    letter-spacing: 0.05em;
  }
  .end-handles {
    font-size: 1rem;
    color: #8faac3;
    letter-spacing: 0.1em;
  }
  .container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 3rem;
  }
  .end-qr {
    width: 250px;
    height: auto;
    border-radius: 10px;
    border: 1px solid #8faac3;
  }
  .feedback-qr {
    background-color: #ffffff;
  }
  .end-doors {
    display: flex;
    gap: 1.5rem;
    align-items: flex-end;
  }
  .end-door {
    width: 60px;
    height: 100px;
    border-radius: 40% 40% 0 0 / 20% 20% 0 0;
    border: 2px solid;
  }
</style>
