---
title: "Gevraagde vaardigheden van een werknemer in een data gerelateerde functie"
date: 2020-04-05
tags: [data, data science, vaardigheden, indeed, text mining]
fontsize: 10pt
header:
excerpt: "Data Science, Data, text mining"
mathjax: "true"
---
Data en data analyse worden door steeds meer organisaties gebruikt om hun bedrijfsprocessen te optimaliseren en/of een competitief voordeel te behalen. Om inzichtelijk te krijgen waar een persoon die met data met werk tegenwoordig aan moet voldoen, heb ik 1144 vacatures gescraped van Indeed in Nederland (datum: 06-01-2020), waarvan een selectie is gemaakt van 844 vacatures die expliciet functie-eisen benoemden. Belangrijk om te vermelden is dat een deel van deze vacatures in het Engels zijn. Dit zijn bedrijven die in Nederland opereren, maar opzoek zijn naar een persoon die kundig is in de Engelse taal (waarschijnlijk een internationale werkvloer, of andere vestigingen in het buitenland). Na het opschonen van de data begint het maken van een overzicht met de meest voorkomende woorden:

<img src="{{ site.url }}{{ site.baseurl }}/images/Meeste_woorden.png" alt="linearly separable data">
<sub>*Grafiek 1: Meest voorkomende woorden*</sub>

Logischerwijs scoren woorden zoals “Data”, “Experience” en “Ervaring” hoog. Interessant om te zien is dat dingen als “sql” en “python” naar voren komen. Dit zijn programmeertalen die vaak gevraagd worden. Wat ook interessant is, is het woord “management”. Kijkende naar de vacatures vermoed ik dat dit vacatures zijn waar wordt vermeld dat men moet rapporteren aan het management. 

# Iets over bigrams en netwerkgrafieken

Een netwerkgrafiek kan helpen in het onderzoeken van verbanden tussen woorden. Dit is een grafiek van woorden die elkaar opvolgen, om zo te zien welke woorden het vaakst achter elkaar worden genoemd. Er is een splitsing gemaakt tussen vacatures die in het Engels zijn en vacatures die in het Nederlands zijn. 

<img src="{{ site.url }}{{ site.baseurl }}/images/netwerk NL.png" alt="linearly separable data">
*Netwerkgrafiek Nederlands*

<img src="{{ site.url }}{{ site.baseurl }}/images/Netwerk_ENG.png" alt="linearly separable data">
*Netwerkgrafiek Engels*

<img src="{{ site.url }}{{ site.baseurl }}/images/netwerk.png" alt="linearly separable data">
*Netwerkgrafiek Nederlands en Engels*

### Conclusie
Uit deze visualisaties komen 4 duidelijke lijnen naar voren:

1. **Vaardigheden**: Communicatief vaardig, sterk analytisch vermogen, Engelse en Nederlandse taal
Een persoon die werkt met data moet communicatief vaardig zijn en een sterk analytisch vermogen hebben. Ook is een goede beheersing van de Nederlandse en Engelse taal belangrijk. 
2. **Tools**: R, Python, Power Bi, Microsoft Office, Google Analytics, Adobe Analytics
R, Python, Power Bi, Microsoft Office, Google Analytics, Adobe Analytics zijn belangrijke tools.
3. **Opleiding**: Bachelor, Master
Er wordt voornamelijk gevraagd om een Bachelor of Master opleidingsniveau.
4. **Methoden**: Agile, Scrum
Agile en scrum worden toegepast in deze organisaties. 

Interessant zal zijn om dit over een aantal maanden te herhalen om te kijken wat voor impact het Corona virus heeft gehad op de gevraagde vaardigheden. Wellicht zien we een grotere stijging in het gebruik van open source tools doordat bedrijven hun kosten verlagen. 












## H2 Heading

### H3 Heading

Here's some basic text.

And here's some *italics*

Here's some **bold** text.

What about a [link](https://github.com/dataoptimal)?


Here's a bulleted list:
* First item
+ Second item
- Third item

Here's a numbered list:
1. First
2. Second
3. Third

Python code block:
```python
    import numpy as np

    def test_function(x, y):
      z = np.sum(x,y)
      return z
```

R code block:
```r
library(tidyverse)
df <- read_csv("some_file.csv")
head(df)
```

Here's some inline code `x+y`.

Here's an image:

Here's another image using Kramdown:
![alt]({{ site.url }}{{ site.baseurl }}/images/perceptron/linsep.jpg)

Here's some math:

$$z=x+y$$

You can also put it inline $$z=x+y$$
