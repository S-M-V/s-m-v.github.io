---
title: "SMV | CV"
layout: gridlay
excerpt: "SMV: CV"
sitemap: false
permalink: /CV/
---

<h1>📝 CV</h1>
{% assign number_printed = 0 %}
{% for member in site.data.CV_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/CV/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">
    {% for i in (1..member.number_educ) %}
      {% capture field %}education{{ i }}{% endcapture %}
      <li>{{ member[field] | markdownify }}</li>
    {% endfor %}
  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


---

## Education

* Ph.D. in Nanoscience and Nanotechnology (2021)  
  Institute of Molecular Science, University of Valencia, Spain  
  PhD Supervisor: Prof. Eugenio Coronado  
* M.S. in Molecular Nanoscience and Nanotechnology, University of Valencia, Spain (2015)  
* B.S. in Physics, University of Valencia, Spain (2013)  

---

## Current Position

* **Ramón y Cajal Research Fellow (From 2026)**  
  Institute of Molecular Science (ICMol), University of Valencia, Spain.

---

## Previous Positions

* **Kavli Research Fellow (2025–2026)**  
  Department of Quantum Nanoscience, Kavli Institute of Nanoscience, Delft University of Technology, The Netherlands  
  Hosts: Prof. Toeno van der Sar and Prof. Sonia Conesa-Boj
  
* **Marie-Curie-Skłodowska Postdoctoral Fellow (2023–2025)**  
  Department of Quantum Nanoscience, Delft University of Technology, The Netherlands  
  Supervisor: Prof. Toeno van der Sar  
  Funded by the European Commission [(Grant ID 101103355)](https://cordis.europa.eu/project/id/101103355)  

* **APOSTD Postdoctoral Research Fellow (2022–2023)**  
  Department of Quantum Nanoscience, Delft University of Technology, The Netherlands
  Supervisor: Prof. Herre van der Zant  
  Funded by the Generalitat Valenciana (APOSTD CIAPOS2021/215)  

* **Postdoctoral Research Fellow (2021–2022)**  
  Institute of Molecular Science, University of Valencia, Spain  
  Supervisor: Prof. Eugenio Coronado  

---

## Awards

* [2026 Olivier Kahn International Award](https://www.eimm.eu/okia_awards_laureates.php)
* [2026  IEEE Magnetics Society Early Career Award](https://ieeemagnetics.org/post/congratulations-2026-ieee-magnetics-society-award-winners)
* 2024 Magnetochemistry Young Investigator Award  
* [2023 Young Scientist Award](https://magnetism.eu/news/224/38-news.htm) by the European Magnetism Association  
* Lindau Alumni (73rd Lindau Nobel Laureate Meeting, Physics, 2024)  
* “Best 2021 thesis from the GENAM”, Nanoscience and Molecular Materials Section of the Spanish Royal Society of Physics and the Spanish Royal Society of Chemistry
* Honorific thesis mention by the Spanish Royal Academy of Doctors  

---

## Selected Talks

### Plenary Talks

**2026**
- European Conference on Molecular Magnetism (*Olivier Kahn Lecture*), Copenhaguen, Denmark  

**2025**
- 2nd European School on Advanced Materials, Almagro, Spain  

**2023**
- 13th Joint European Magnetic Symposia (delivery of the 2023 Young Scientist Award by the European Magnetism Association). Madrid, Spain

### Invited Talks

**2026**
- International Symposium on Advanced Magnetic Materials and Applications (ISAMMA 2026). Busan, Korea
- 2026 Multiscale Phenomena in Condensed Matter. Krakow, Poland
- Young Research Leaders Group Workshop: Transport and transfer of angular momentum by the Spin Phenomena Interdisciplinary Center. Mainz, Germany
- QuantumMatter 2026, Barcelona, Spain

**2025**
- Invited seminar (Theme 3 seminar), Radboud Universiteit, Nijmegen, The Netherlands.
- SQLM Workshop, Kaiserslautern, Germany.
- International Conference on Layered Materials & Devices: From Atoms to Chips! Braga, Portugal
- 16th International Symposium on Crystalline Organic Metals, Superconductors and Magnets (ISCOM 2025). Okazaki, Japan
- Quantum Functionalities of Nanomagnets - SPICE workshop. Mainz, Germany
- 4th European Conference on Molecular Spintronics ECMOLS 2025. Dublin, Ireland
- Metal-Organic Frameworks as quantum materials. Baltimore, United States

**2024**
- Magnons on an Island – 2024, Texel, The Netherlands  
- 9th European Conference on Molecular Magnetism ECMM2024. Krakow, Poland
- 2D Materials Conference – attocube ‘meet the leading experts’. Munich, Germany
- FUNLAYERS Hands-on workshop on synchrotron techniques for research in Spintronics and Energy Storage. ALBA synchrotron, Barcelona, Spain

**2023**
- 18th International Conference on Molecular-based Magnets (Rising Star Session). Nanjing, China
- 2023 Pre-ICMM Symposium on "Emerging Research on Molecule-Based Magnets: From Theory to Experiment". Guangzhou, China
- Modulation of physico-chemical processes by elastic strain engineering. Besançon, France
- European Magnetism Association (EMA) Early-Career Seminars. Online, Europe

---

## Teaching

- **Molecular Spintronics** (6 ECTS/year, 2016–2021)  
  Master in Molecular Nanoscience and Nanotechnology, University of Valencia, Spain  
- **Student Supervision**: 1 Ph.D., 3 Master’s, 4 Undergraduate  

---

## Service and Leadership

- Governing board member, Condensed Matter Division & Valencian Section of the Spanish Royal Society of Physics (2018–2022)  
- Organizer of scientific meetings for young researchers:  
  - [EPS Young Minds session at CMD2020GEFES](https://members.eps.org/blogpost/751263/357485/EPS-Young-Minds-at-the-conference-CMD2020GEFES), together with Dr. Roberta Caruso  
  - [2025 SPICE Young Research Leaders Group Workshop](https://www.spice.uni-mainz.de/yrlgw-2025-home/), together with Dr. Talieh Ghiasi  

- **Peer Review Activities**  
  - Reviewer for major agencies: European Research Council, Spanish Agencia Estatal de Investigación, US Department of Energy, Swiss National Science Foundation, French National Research Agency, Polish National Science Center, ...
  - Journals (> 160 reviews, > 35 journals; see [ORCID](https://orcid.org/0000-0001-6319-9238)): *Advanced Materials*, *Nature Communications*, *Nano Letters*, *ACS Nano*, *PRL*, *PRX*, *PRB*, ...  
