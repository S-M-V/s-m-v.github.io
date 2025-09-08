---
title: "SMV - CV"
layout: gridlay
excerpt: "SMV: CV"
sitemap: false
permalink: /CV/
---

# CV

{% if site.data.CV_members %}
  {% for member in site.data.CV_members %}
  <div class="col-sm-12 clearfix" style="margin-bottom: 30px;">
    <img src="{{ site.url }}{{ site.baseurl }}/images/CV/{{ member.photo }}" class="img-responsive" width="25%" style="float: left; margin-right: 15px;" />
    <h4>{{ member.name }}</h4>
    <i>{{ member.info }}</i>
    {{ member.social_icons | raw }}
    <ul style="overflow: hidden;">
      {% for i in (1..member.number_educ) %}
        <li>{{ member["education" | append: i] | markdownify }}</li>
      {% endfor %}
    </ul>
  </div>
  {% endfor %}
{% else %}
  <p>No team member data available.</p>
{% endif %}

---

## Education

* Ph.D. in Nanoscience and Nanotechnology (2021)  
  Institute for Molecular Science, University of Valencia, Spain  
  PhD Supervisor: Prof. Eugenio Coronado  
* M.S. in Molecular Nanoscience and Nanotechnology, University of Valencia, Spain (2015)  
* B.S. in Physics, University of Valencia, Spain (2013)  

---

## Current Position

* **Kavli Research Fellow (2025–2026)**  
  Department of Quantum Nanoscience, Kavli Institute of Nanoscience, Delft University of Technology, The Netherlands  
  Hosts: Prof. Toeno van der Sar and Prof. Sonia Conesa-Boj  

---

## Previous Positions

* **Marie-Curie-Skłodowska Postdoctoral Fellow (2023–2025)**  
  Department of Quantum Nanoscience, Delft University of Technology, The Netherlands  
  Supervisor: Prof. Toeno van der Sar  
  Funded by the European Commission [(Grant ID 101103355)](https://cordis.europa.eu/project/id/101103355)  

* **APOSTD Postdoctoral Research Fellow (2022–2023)**  
  Same department, Supervisor: Prof. Herre van der Zant  
  Funded by the Generalitat Valenciana (APOSTD CIAPOS2021/215)  

* **Postdoctoral Research Fellow (2021–2022)**  
  Institute for Molecular Science, University of Valencia, Spain  
  Supervisor: Prof. Eugenio Coronado  

---

## Awards

* 2024 Magnetochemistry Young Investigator Award  
* [2023 Young Scientist Award](https://magnetism.eu/news/224/38-news.htm) by the European Magnetism Association  
* Lindau Alumni (73rd Lindau Nobel Laureate Meeting, Physics, 2024)  
* “Best 2021 thesis from the GENAM” – awarded by the Spanish Royal Society of Physics & Chemistry  
* Honorific thesis mention by the Spanish Royal Academy of Doctors  

---

## Selected Talks

### Plenary Talks

**2025**
- 2nd European School on Advanced Materials, Almagro, Spain  

**2023**
- 13th Joint European Magnetic Symposia – EMA Young Scientist Award talk, Madrid, Spain  

### Invited Talks

**2025**
- International Conference on Layered Materials & Devices, Braga, Portugal  
- ISCOM 2025, Okazaki, Japan  
- SPICE Workshop: Quantum Functionalities of Nanomagnets, Mainz, Germany  
- ECMOLS 2025, Dublin, Ireland  
- Metal-Organic Frameworks as Quantum Materials, Baltimore, USA  

**2024**
- Magnons on an Island – 2024, Texel, The Netherlands  
- ECMM2024, Krakow, Poland  
- 2D Materials Conference – Attocube, Munich, Germany  
- FUNLAYERS Workshop, ALBA Synchrotron, Barcelona, Spain  

**2023**
- ICMM 2023 – Rising Star Session, Nanjing, China  
- Pre-ICMM Symposium, Guangzhou, China  
- Workshop on Strain Engineering, Besançon, France  
- EMA Early-Career Seminars, Online  

---

## Teaching

- **Molecular Spintronics** (6 ECTS/year, 2016–2021)  
  Master in Molecular Nanoscience and Nanotechnology, University of Valencia, Spain  
- **Student Supervision**: 1 Ph.D., 3 Master’s, 4 Undergraduate  

---

## Service and Leadership

- Governing board member, Condensed Matter Division & Valencian Section, Spanish Royal Society of Physics (2018–2022)  
- Organizer of scientific meetings for young researchers:  
  - [EPS Young Minds session at CMD2020GEFES](https://members.eps.org/blogpost/751263/357485/EPS-Young-Minds-at-the-conference-CMD2020GEFES)  
  - [2025 SPICE Young Research Leaders Group Workshop](https://www.spice.uni-mainz.de/yrlgw-2025-home/)  

- **Peer Review Activities**  
  - Reviewer for: US DOE, ERC, Polish NCN  
  - Journals: *Advanced Materials*, *Nano Letters*, *PRL*, *PRX*, *PRB*, etc.  
