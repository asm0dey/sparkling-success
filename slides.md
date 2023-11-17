---
theme: light-icons
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
title: Sparking Success
mdc: true
---

# Sparking Success

## Unveiling the Journey of Apache Spark Application Development

Pasha Finkelshteyn, <logos-jetbrains />


---

# `whoami`

* Pasha Finkelshteyn
* Mostly <logos-java/><logos-kotlin-icon/> developer
* Like <logos-python /> too
* Certificated <logos-airflow-icon/> specialist
* Average <devicon-plain-sqldeveloper/> enjoyer
* Developer Advocate for Data Engineering

---
layout: center
---

# Today I'm talking about a data engineering task lifecycle

---
clicks: 2
---

# Understanding the task

#### Tasks usually are vague:

* Create a report
* Arrange access
* Arrange data export
* Support GDPR

<br/>
<div v-if="$clicks == 1">

**And this is fine!**

</div>
<div v-if="$clicks == 2">

Our task: **find the most popular movie genre**

</div>

---
layout: image
image: lifecycle2.png
---

---

# Understand the task

Understand?

"Understand" is a casual term.

In psychology and informational science it's called "conceptualize"


---

# Conceptualization

> In information science a conceptualization is an abstract simplified view of some selected part of the world, containing the objects, concepts, and other entities that are presumed of interest for some particular purpose and the relationships between them

Wikipedia 

---

# Conceptualization

> Conceptualization is like creating a mental map or plan in your mind about something. It's the process of thinking up and understanding concepts or ideas. So, it involves taking a lot of data or information (like facts, numbers, or situations) and organizing it in your brain so that it makes sense and can be understood better. It's like building a model or a picture in your head of how things are or how they work.

GPT 4

---
layout: image-right
image: mindmap.webp
---

# Conceptualization

Writing code is usually the simplest thing.

Complex parts are:
* Find the data owners
* Find the data experts
* Understanding the desired result
* Defining the way to solve the problem

---

# Data acquisition/planning

When we found owners, we obtain the knowledge about the data from them.

<v-click>
  
In a perfect world
  
* Find data
* Understand formats/sources
* Update tools list?

# <logos-datagrip/>&nbsp;&nbsp;&nbsp;&nbsp;<logos-pycharm/>&nbsp;&nbsp;&nbsp;&nbsp;<logos-intellij-idea/>

</v-click>



---
layout: image
image: movielens.png
---

---

# Movielens

* Exports its data
* Has all the data interesting to us
* Exports in CSV
* We'll convert it to parquet (because typed and compact)

---
layout: image-right
image: pipeline.svg
clicks: 3
---

# Design the architecture

Now we know the data <v-click><span>hopefully</span></v-click>

<v-click v-if="$clicks == 2 ">

* Understand limitations
* Understand needs
* Understand SLA (SLO)
* Understand capabilities
* Draft an architecture
* Log to ADR (Architectural Decision Record)

</v-click>
<v-click v-if="$clicks == 3 ">

For the sake of demo we'll just perform `show`.

In a more real world-scenario it would be some kind of write

</v-click>

---

# Data Quality?

This step is not always required

At this point we usually need to

* Profile data
* Write tests
* Add profile to monitoring

*Tools*:

* DeeQu/PyDeeQu
* Great Expectations

---

# Development

The most boring step :)

---
layout: center
---

# DEMO

---

# Testing

After initial implementtion

At this point we already have a solution

What we should test

<table>
  <tr>
    <td><b>Data</b></td>
    <td><b>Code</b></td>
  </tr>
  <tr>
    <td>Data Quality</td>
    <td>Efficiency</td>
  </tr>
  <tr>
    <td>Data Integrity</td>
    <td>Correctness</td>
  </tr>
  <tr>
    <td></td>
    <td>Completeness</td>
  </tr>
</table>

---

# Deployment 

Boring part again :)

---
layout: center
---

# DEMO

---

# Operation

Real production

After the first successful deploy/run, we need to automate the job
* Replace hardcoded with parameters
* Decide on backfilling
* Update/Create DAG in orchestrator <logos-airflow-icon/>

---

# Monitoring
So we know what's happening there

* Grafana dashboard
* In a perfect world AirBnB-like solution

---
layout: center
---

# Iterate

---
layout: image
image: lifecycle2.png
---

# Lifycecle

---

# Summary

* All data engineering tasks share the same lifecycle
* Programming complex data engineering requires adequate tooling
* The work always starts with conceptualization!
* Coding is interesting but is not the only interesting part

---


# Thank you! Time for questions 😄

<div class="text-left">
<p><ph-twitter-logo-fill/> asm0di0</p>
<p><mdi-mastodon/> @asm0dey@fosstodon.org</p>
<p><ph-envelope-simple-open-fill/> me@asm0dey.site</p>
<p><ph-twitch-logo-fill/> https://jb.gg/twitch</p>
<p><ph-github-logo-fill/><ph-instagram-logo-fill/><ph-linkedin-logo-fill/><ph-telegram-logo-fill/> asm0dey</p>
<p><ph-globe-duotone/><a href="https://linktr.ee/asm0dey">https://linktr.ee/asm0dey</a></p>
</div>
