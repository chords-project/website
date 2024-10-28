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

  - name: Marco Peressotti
    image: mperessotti.jpg

  - name: Dan Plyukhin
    image: dplyukhin.jpg

  - name: Xueying Qin
    image: xqin.jpg

  - name: Viktor Strate Kløvedal
    image: viktorstrate.jpg

sponsors:
  - name: European Research Council
    logo: /images/logos/erc-logo.svg
    link: https://erc.europa.eu/

  - name: Villum Foundation
    logo: /images/logos/villum-logo.png
    link: https://veluxfoundations.dk/en

  - name: Independent Research Fund Denmark
    logo: /images/logos/irfd-logo.png
    link: https://dff.dk/en/

  - name: University of Southern Denmark
    logo: /images/logos/sdu-logo.svg
    link: https://sdu.dk/en
---

Chords is made possible by the efforts of many [people](#people) and generous [sponsors](#sponsors).

## Contact

You can contact us by joining this Discord server or sending an individual e-mail to any of the [people listed in the next section](#people).

## People

{{< people.inline >}}

<ul class="hx-grid hx-gap-4" style="grid-template-columns: repeat(4, minmax(0, 1fr)); margin: 1rem 0 0;">
    {{ range .Page.Param "people" }}
    <li class="hx-block">
        {{ $image := resources.Get (path.Join "images/people" .image) }}
        {{ $image := $image.Fill "400x400 q80 webp" | images.Filter images.Grayscale }}
        <img src="{{ $image.RelPermalink }}" width="{{ math.Div $image.Width 2 }}" height="{{ math.Div $image.Height 2 }}" loading="lazy" alt="{{ .name }}">
        <p class="hx-text-center" style="margin-top: 0;">{{ .name }}</p>
    </li>
    {{ end}}
</ul>

{{< /people.inline >}}

## Sponsors

{{< sponsor.inline >}}

<ul style="margin-left: 0; display: inline-flex; gap: 0 4rem; flex-wrap: wrap; align-items: center; justify-content: center; width: 100%;">
    {{ range .Page.Param "sponsors" }}
    <li style="margin: 0; display: block;">
        <a href="{{.link}}" target="_blank">
            <img style="margin: 2rem 0" width="200" height="200" src="{{.logo}}" alt="{{.name}}" loading="lazy">
        </a>
    </li>
    {{ end }}
</ul>

{{< /sponsor.inline >}}
