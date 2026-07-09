---
title: "Lucas Palazzolo - Research"
layout: gridlay
excerpt: ""
sitemap: false
permalink: /research/
---


---
### Publications
---

#### Preprints

<div class="publications">
{% for publi in site.data.publist %}
  {% if publi.preprint == 1 %}
  <p id="pub-{{ publi.number }}">
    [{{ publi.number }}]
     <span class="toggle" onclick="toggleDesc('{{ publi.number }}')">▶</span> 
    {{ publi.title }} <br>
    {{ publi.authors }} 
     {% if publi.link2 %}
      — <a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a> • <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
    {% else %}
      — <a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
    {% endif %}
  </p>
  <div class="description" id="desc-{{ publi.number }}" style="display:none;">
  {{ publi.description | markdownify }}
</div>
 {% endif %}
{% endfor %}
</div>

#### Published articles

<div class="publications">
{% for publi in site.data.publist %}
  {% if publi.preprint == 0 %}
  <p id="pub-{{ publi.number }}">
    [{{ publi.number }}]
    <span class="toggle" onclick="toggleDesc('{{ publi.number }}')">▶</span>
    {{ publi.title }} <br>
    {{ publi.authors }}
     {% if publi.link2 %}
      — <a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a> • <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
    {% else %}
      — <a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
    {% endif %}
  </p>
  <div class="description" id="desc-{{ publi.number }}" style="display:none;">
  {{ publi.description | markdownify }}
</div>
 {% endif %}
{% endfor %}
</div>


---
### Communications
---

#### 2026
- **[MicroSwim 2026](https://www.lebesgue.fr/fr/microSwim26)** (July 2026), Brest, France  
  *Plenary session:* [*Optimization of Microswimmers by Bayesian Optimization*](https://www.lebesgue.fr/sites/default/files/2026-07/abstract_book%20modelling.pdf)  


#### 2025
- **[SAMO 2025](https://samo2025.sciencesconf.org/)** (April 2025), Grenoble, France  
  *Poster:* [*Parametric Shape Optimization of Flagellated Microswimmers Using Bayesian Techniques*](https://hal.science/hal-05010013)  

- **EDSFA Workshop** (May 2025), CEMEF, Sophia Antipolis, France  
  *Poster:* [*Parametric Shape Optimization of Flagellated Microswimmers Using Bayesian Techniques*](https://hal.science/hal-05010013)  

- **Groupe de travail “Étude du magnétoswimmer”** (September 2025), UFR de Mathématiques, Strasbourg, France  
  *Talk:* *Tracking Trajectories of the N-Links Model*  



#### 2024
- **Groupe de travail “Modélisation de la micronatation”** (March 2024), UFR de Mathématiques, Strasbourg, France  
  *Talk:* *Shape Optimization of Flagellated Microswimmers with Bayesian Techniques*  

- **[PGMO Days 2024](https://fondation-hadamard.fr/media/filer_public/a4/f7/a4f795b0-1a5a-4efb-a327-c44887361100/pgmo-2024-booklet1.pdf)** (November 2024), EDF Labs, Paris-Saclay, France  
  *Talk:* *Parametric Shape Optimization of Flagellated Microswimmers Using Bayesian Techniques*  



<script>
function toggleDesc(pubNumber) {
  const desc = document.getElementById('desc-' + pubNumber);
  const toggle = desc.previousElementSibling.querySelector('.toggle');

  if (desc.style.display === 'none') {
    desc.style.display = 'block';
    toggle.textContent = '▼'; // change triangle down
  } else {
    desc.style.display = 'none';
    toggle.textContent = '▶'; // change triangle right
  }
}
</script>

<style>
.toggle {
  cursor: pointer;
  font-weight: bold;
  margin-left: 5px;
  color:  rgb(11, 131, 63);   /* your green */
}
.description {
  padding-left: 20px;
  color: #555;
}

</style>