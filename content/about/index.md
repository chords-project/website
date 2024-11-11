---
title: About
type: about
toc: false
weight: 5

people:
  - name: Fabrizio Montesi
    image: fmontesi.jpg
    role: Project Director, Principal Investigator
    affiliation: University of Southern Denmark
    website: https://www.fabriziomontesi.com
    email: fmontesi@imada.sdu.dk

  - name: Marco Peressotti
    image: mperessotti.jpg
    role: Associate Professor
    website: https://marcoperessotti.com/
    email: peressotti@imada.sdu.dk

  - name: Dan Plyukhin
    image: dplyukhin.jpg
    role: Postdoctoral Researcher
    website: https://dplyukhin.github.io/
    email: dplyukhin@imada.sdu.dk

  - name: Xueying Qin
    image: xqin.jpg
    role: Postdoctoral Researcher
    website: https://xyunknown.github.io/
    email: xyqin@imada.sdu.dk

  - name: Giulia Manara
    image: giulia.jpg
    role: Postdoctoral Researcher
    email: manara@imada.sdu.dk

  - name: Viktor Strate Kløvedal
    image: viktorstrate.jpg
    role: PhD Student
    website: https://qpqp.dk/
    email: viktorstrate@imada.sdu.dk

  - name: Marco Santamaria
    image: msantamaria.jpg
    role: PhD Student
    email: santamaria@imada.sdu.dk

sponsors:
  - name: European Research Council
    logo: /images/logos/erc-logo.svg
    link: https://erc.europa.eu/
    body: >
      ERC Consolidator Grant [CHORDS](https://www.fabriziomontesi.com/projects/chords/) (2024--2029).

  - name: Villum Foundation
    logo: /images/logos/villum-logo.png
    link: https://veluxfoundations.dk/en
    body: >
      VILLUM Young Investigator Project [CHOCO](https://www.fabriziomontesi.com/projects/choco/) (2020--2025) and VILLUM Synergy Initiation Project [X-IDF](https://www.sdu.dk/en/forskning/forskningsenheder/samf/digitaldemocracycentre/researchprojects/x-idf) (2023--2025).

  - name: Independent Research Fund Denmark
    logo: /images/logos/irfd-logo.png
    link: https://dff.dk/en/
    body: >
      Individual Postdoctoral Grant [CRC](https://www.fabriziomontesi.com/projects/) (2014--2017).

  - name: University of Southern Denmark
    logo: /images/logos/sdu-logo.svg
    link: https://sdu.dk/en
    body: >
      Project hosting and seed funding through the project [Open Data Framework](https://www.fabriziomontesi.com/projects/) (2017--2019).
---

Chords is made possible by the efforts of many [people](#people) and generous [sponsors](#sponsors).

## Contact

You can contact us by joining this Discord server or sending an individual e-mail to any of the [people listed in the next section](#people).

<!--more-->

## People

{{< people.inline >}}

<ul class="hx-grid hx-gap-4" style="grid-template-columns: repeat(4, minmax(0, 1fr)); margin: 1rem 0 0;">
    {{ range .Page.Param "people" }}
    <li class="hx-block">
        {{ $image := resources.Get (path.Join "images/people" .image) }}
        {{ $image := $image.Fill "400x400 q80 webp" | images.Filter images.Grayscale }}
        <img src="{{ $image.RelPermalink }}" width="{{ math.Div $image.Width 2 }}" height="{{ math.Div $image.Height 2 }}" loading="lazy" alt="{{ .name }}">
        <div style="text-align: center;">
          <div><b>{{ .name }}</b>,</div>
          <div>{{ .role }}</div>
          <div style="display: flex; gap: 0.5rem; justify-content: center; margin-top: 0.4rem;">
            <a href="mailto:{{.email}}" title="Email">
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-mail"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>
            </a>
            <a href="{{ .website }}" title="Website">
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-globe"><circle cx="12" cy="12" r="10"></circle><line x1="2" y1="12" x2="22" y2="12"></line><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"></path></svg>
            </a>
          </div>
        </div>
    </li>
    {{ end}}
</ul>

{{< /people.inline >}}

## Sponsors

The Chords project is made possible by the generous funding and support of the European Research Council (project CHORDS) and previous projects for early explorations of choreographic programming.

{{< sponsor.inline >}}

{{ range .Page.Param "sponsors" }}

<div style="display: inline-flex; flex-wrap: wrap; gap: 0 4rem; align-items: center; margin-top: 2rem;">
  <img src="{{.logo}}" alt="{{.name}}" width="200" height="200" loading="lazy" />
  <div style="flex: 1 1 300px;">
    <h3 style="margin-top: 0;">{{.name}}</h3>
    <p style="margin-top: 0.5rem;">{{.body | markdownify }}</p>
  </div>
</div>

{{ end }}

{{< /sponsor.inline >}}

<hr style="margin-top: 5rem;" />

<small>
Co-funded by the European Union (ERC, CHORDS, 101124225).
Views and opinions expressed are however those of the authors only
and do not necessarily reflect those of the European Union or the European Research Council.
Neither the European Union nor the granting authority can be held responsible for them.
</small>
