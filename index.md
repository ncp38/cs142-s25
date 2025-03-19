---
layout: home
title: Home
nav_exclude: false
nav_order: 0
seo:
  type: Course
  name: Computer Science 142 Spring 2025
---

# {{ site.tagline }}
{: .mb-2 }
{{ site.description }}
{: .fs-6 .fw-300 }

<!--<button class="js-toggle-dark-mode dm-btn btn">Toggle Dark Mode</button>-->

{% if site.announcements %}
{{ site.announcements.last }}
[Announcements](announcements.md){: .btn .btn-outline .fs-3 }
{% endif %}

## Administrivia
- Instructor: Nate Phillips
- Office hours: Mon 2-4 PM, Wed 2-3 PM.  Also available by appointment and over Slack or Zoom.
- [Section 1 Canvas page](https://rhodes.instructure.com/courses/8526) and [Section 2 Canvas page](https://rhodes.instructure.com/courses/8518): Use for grades, online assignment submissions, and assignment solutions.
- [Syllabus](syllabus/syllabus-142-s25.pdf) and [additional policies](syllabus/additional-policies-142-s25.pdf).
- Tutoring hours: Sunday through Thursday evenings, 5-11pm, Briggs 001 


## Resources
- Textbooks and tutorials: *Introduction to Java* by Liang (textbook), 
	*Introduction to Programming in Java* by Sedgewick and Wayne (textbook),
        [official Java tutorials](https://docs.oracle.com/javase/tutorial/), 
        [Introduction to Programming Using Java](http://math.hws.edu/javanotes/index.html) (free online textbook)
- Java in the browser: [Repl.it](http://repl.it/new/java), <a href="http://codehs.com">CodeHS</a>
- Coding exercises for practice, review, and improvement: [Exercism](https://exercism.org/tracks/java/exercises)
- <a href="https://docs.oracle.com/en/java/javase/17/docs/api/">Official Java documentation</a>
     

## Calendar
{% for module in site.modules %}
{{ module }}
{% endfor %}

<!--DARKMODE UNDER CONSTRUCTION-->
<br />


<!--
<p class="dm-text">The Data 8 Website Dark Mode&trade; is in beta. You can provide feedback about the website <a href="https://forms.gle/64xx2B1Y7K32bNhR9" 
class="yellow-link">here</a></p>
-->

<script src="assets/darkmode.js"></script>
<script>
  const toggleDarkMode = document.querySelector('.js-toggle-dark-mode');

  jtd.addEvent(toggleDarkMode, 'click', function(){
    if (jtd.getTheme() === 'custom_dark') {
      jtd.setTheme('light');
      localStorage.setItem("darkMode", 0);
      toggleDarkMode.innerHTML = "Toggle Dark Mode";
      toggleDarkMode.classList.add('dm-btn');
        toggleDarkMode.classList.remove('dm-dark-btn');
    } else {
      jtd.setTheme('custom_dark');
      localStorage.setItem("darkMode", 1);
      toggleDarkMode.innerHTML = "Return to the Light";
      toggleDarkMode.classList.add('dm-dark-btn');
      toggleDarkMode.classList.remove('dm-btn');
    }
  });

    window.addEventListener("DOMContentLoaded", (event) => {
      onLoad();
  });
</script>