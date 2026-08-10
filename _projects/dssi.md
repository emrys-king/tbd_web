---
layout: project
title: 'Data Science for Social Impact Hackathon'
author-profile: true
collection: projects
sort_date: 2025.04
display_date: "2025"
preprint: "https://cameraperture.shinyapps.io/dssi_app/"
preprintdisplay: "App"
github: "https://github.com/emrys-king/DSSI_Datathon"
---

[Charlotte Imbert](https://cameraperture.github.io/) and I were delighted to win second place at the inaugural Data Science For Social Impact (DSSI) Hackathon, hosted at Harvey Mudd College in April 2025.

We were given 4 hours to explore the World Bank’s Millennium Development Goals dataset — a rich collection covering 263 countries and regions between 2006 and 2015 — and build a stunning visualization addressing the success of the Millennium Development Goals. Focusing on the 6th goal (combat HIV/AIDS, malaria, and other diseases) and drawing inspiration from a certain book by John Green, we focused on global incidence of tuberculosis (TB). We chose to present our visualization via an interactive Shiny dashboard to explore how TB death rates correlate with health, education, and economic proxy variables.

<object data="{{ site.url }}{{ site.baseurl }}/images/appsc.jpeg" type="application/jpeg" width="500px" height="300px">
    <embed src="{{ site.url }}{{ site.baseurl }}/images/appsc.jpeg">
        <p>The image cannot be loaded. Please download the image to view it: <a href="{{ site.url }}{{ site.baseurl }}/images/appsc.jpeg">Download image</a>.</p>
    </embed>
</object>

We found some expected trends, like a correlation between TB incidence and TB mortality. However, TB treatment success rates had almost no correlation with TB mortality. Rather, detection of TB was more influential. Since the disease has variable rates of progression, detection is often the most important step, as it unlocks various kinds of treatment. Early detection is also an indication of well-established, accessible healthcare systems. This observation is corroborated by the negative correlation between TB deaths and the percent of births attended by skilled medical staff.

The final product of is currently hosted on [Charlotte’s website](https://cameraperture.shinyapps.io/dssi_app/).