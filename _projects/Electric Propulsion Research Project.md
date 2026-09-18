---
layout: page
title: "Electrospray Electric Propulsion Research"
permalink: /projects/electric-propulsion-research/
image: /assets/images/space_image.png
---

<style>
/* ---------- PROJECT PAGE ---------- */

.research-project {
  max-width: 1050px;
  margin: 0 auto;
  padding: 40px 35px 80px 35px;
  font-family: Georgia, "Times New Roman", serif;
  color: #333;
  line-height: 1.55;
}

.research-project h1 {
  font-size: 3.1rem;
  line-height: 1.08;
  margin: 0 0 30px 0;
  font-weight: 700;
}

.research-project h2 {
  font-size: 2.35rem;
  line-height: 1.15;
  margin-top: 45px;
  margin-bottom: 22px;
  font-weight: 700;
}

.research-project h3 {
  font-size: 1.4rem;
  margin-top: 30px;
  margin-bottom: 12px;
}

.research-project p,
.research-project li {
  font-size: 1.2rem;
  line-height: 1.65;
}

.research-project ul {
  margin-top: 15px;
  margin-bottom: 25px;
}

.research-project li {
  margin-bottom: 5px;
}

.research-project a {
  color: #0066ff;
  text-decoration: underline;
}

.research-project hr {
  border: 0;
  border-top: 1px solid #bdbdbd;
  margin: 35px 0;
}


/* ---------- INTRO / TABLE OF CONTENTS ---------- */

.project-intro {
  display: grid;
  grid-template-columns: 340px 1fr;
  gap: 45px;
  align-items: start;
  margin-bottom: 35px;
}

.project-intro-image {
  width: 100%;
  border-radius: 10px;
  display: block;
}

.project-toc h2 {
  margin-top: 0;
  margin-bottom: 15px;
}

.project-toc a {
  display: block;
  font-size: 1.35rem;
  line-height: 1.5;
  margin-bottom: 3px;
}


/* ---------- IMAGES ---------- */

.project-image {
  display: block;
  width: 100%;
  max-width: 850px;
  margin: 28px auto 10px auto;
  border-radius: 10px;
}

.image-caption {
  display: block;
  max-width: 850px;
  margin: 8px auto 30px auto;
  font-size: 1rem !important;
  font-style: italic;
}


/* ---------- POSTER ---------- */

.poster-container {
  width: 100%;
  height: 850px;
  margin: 25px 0 15px 0;
  border: 1px solid #d0d0d0;
  border-radius: 8px;
  overflow: hidden;
}

.poster-container iframe {
  width: 100%;
  height: 100%;
  border: none;
}


/* ---------- MOBILE ---------- */

@media (max-width: 800px) {

  .research-project {
    padding: 25px 20px 60px 20px;
  }

  .research-project h1 {
    font-size: 2.4rem;
  }

  .research-project h2 {
    font-size: 1.9rem;
  }

  .research-project p,
  .research-project li {
    font-size: 1.05rem;
  }

  .project-intro {
    grid-template-columns: 1fr;
    gap: 25px;
  }

  .project-intro-image {
    max-width: 450px;
  }

  .poster-container {
    height: 600px;
  }
}
</style>


<div class="research-project">

<h1>Electrospray Electric Propulsion Research</h1>


<div class="project-intro">

<div>

<img
  src="{{ '/assets/images/space_image.png' | relative_url }}"
  alt="Electrospray electric propulsion research"
  class="project-intro-image">

</div>


<div class="project-toc">

<h2>Table of Contents</h2>

<a href="#project-overview">Project Overview</a>
<a href="#my-work">My Work</a>
<a href="#experimental-approach">Experimental Approach</a>
<a href="#surface-characterization">Surface Characterization</a>
<a href="#research-poster">Research Poster</a>
<a href="#skills">Skills & Tools</a>
<a href="#research-support">Research Support</a>

</div>

</div>


<hr>


<h2 id="project-overview">Project Overview</h2>

<p>
During Summer 2026, I conducted research in Cornell's ASTRA Lab focused on
<strong>electrospray electric propulsion and plume-surface interactions with spacecraft structural materials</strong>.
</p>

<p>
My work investigated how electrospray thruster plumes interact with nearby spacecraft surfaces,
with a focus on <strong>erosion, deposition, and long-term material durability</strong>.
Understanding these interactions is important for predicting how propulsion plumes affect
spacecraft hardware and the lifetime of electrospray propulsion systems.
</p>


<h2 id="my-work">My Work</h2>

<p>
I contributed to both the experimental hardware and analysis for the project. My work included:
</p>

<ul>
  <li>Designing and manufacturing electromechanical components for thruster operation and vacuum testing</li>
  <li>Conducting vacuum chamber testing with an electrospray propulsion system</li>
  <li>Testing spacecraft structural materials, including aluminum and tungsten</li>
  <li>Measuring plume-induced erosion and deposition using profilometry</li>
  <li>Characterizing exposed surfaces using scanning electron microscopy (SEM)</li>
  <li>Developing MATLAB tools for experimental data analysis</li>
  <li>Supporting heater and thruster hardware development</li>
  <li>Analyzing how plume effects vary spatially relative to the center of the thruster plume</li>
</ul>


<h2 id="experimental-approach">Experimental Approach</h2>

<p>
Material samples were exposed to an electrospray plume under vacuum conditions and subsequently
analyzed using several surface-characterization techniques.
</p>

<p>
The experimental setup was operated inside a vacuum chamber, allowing the electrospray thruster
and material samples to be tested under the low-pressure conditions required for thruster operation.
</p>


<img
  src="{{ '/assets/images/vaccuum_chamber.jpeg' | relative_url }}"
  alt="Vacuum chamber experimental setup used for electrospray testing"
  class="project-image">

<p class="image-caption">
Vacuum chamber setup used for electrospray plume-surface interaction testing.
</p>


<h2 id="surface-characterization">Surface Characterization</h2>

<p>
<strong>Profilometry:</strong> Surface profiles before and after plume exposure were used to
quantify changes in surface height and estimate net volumetric erosion or deposition.
</p>

<p>
<strong>Scanning Electron Microscopy (SEM):</strong> SEM imaging was used to examine changes
in surface morphology at higher resolution and identify localized effects of plume exposure.
</p>

<p>
These measurements were used to compare the response of different spacecraft materials and
investigate how erosion and deposition varied spatially across the electrospray plume.
</p>


<h2 id="research-poster">Research Poster</h2>

<p>
My research and experimental results were summarized in the presentation poster below.
</p>


<div class="poster-container">

<iframe
  src="{{ '/assets/electric-propulsion-poster.pdf' | relative_url }}"
  title="Electrospray Electric Propulsion Research Poster">
</iframe>

</div>


<p>
<a
  href="{{ '/assets/electric-propulsion-poster.pdf' | relative_url }}"
  target="_blank">
  Open full research poster in a new tab →
</a>
</p>


<h2 id="skills">Skills & Tools</h2>

<ul>
  <li>Electrospray electric propulsion</li>
  <li>Vacuum chamber testing</li>
  <li>Experimental hardware design and manufacturing</li>
  <li>Profilometry</li>
  <li>Scanning Electron Microscopy (SEM)</li>
  <li>MATLAB</li>
  <li>Experimental data analysis</li>
  <li>Electromechanical system design</li>
  <li>Surface characterization</li>
</ul>


<h2 id="research-support">Research Support</h2>

<p>
This research was conducted through the <strong>Cornell ASTRA Lab</strong> and supported in part
by the Cornell Engineering Undergraduate Research Grants Program.
</p>

<p>
<strong>NASA Space Technology Graduate Research Opportunity</strong><br>
Grant #80NSSC23K1212
</p>

<p>
<strong>Cornell NanoScale Facility / National Nanotechnology Coordinated Infrastructure</strong><br>
Award #2025233
</p>


</div>
