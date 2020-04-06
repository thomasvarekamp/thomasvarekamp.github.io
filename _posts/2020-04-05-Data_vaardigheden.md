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

#### Stap 1: opschonen van de data
Ik begin met het opschonen van de tekstdata. Dit bestaat in dit geval uit het corrigeren van spellingsfouten, het groeperen (Lemmatisation) van woorden met een overkoepelende term (bijvoorbeeld “slechte” wordt “slecht”, “geïsoleerd” wordt “isolatie”), het verwijderen van woorden die niks toevoegen aan de inhoud van de tekst (bijvoorbeeld lidwoorden) en het verwijderen van leestekens. Een volledig foutloze tekst komt in de werkelijkheid bijna nooit voor, maar door deze technieken toe te passen probeer ik de foutmarge zo minimaal mogelijk te houden.

#### Stap 2: meest voorkomende woorden
Na de data preprocessing probeer ik een gevoel te krijgen wat mensen aangeven met betrekking tot ontevredenheid. Het visualiseren van de meest voorkomende woorden geeft mij een eerste impressie:
<img src="{{ site.url }}{{ site.baseurl }}/images/Meeste_woorden.png" alt="linearly separable data">
<sub>*Grafiek 1: Meest voorkomende woorden*</sub>

Logischerwijs scoren woorden zoals “Data”, “Experience” en “Ervaring” hoog. Interessant om te zien is dat dingen als “sql” en “python” naar voren komen. Dit zijn programmeertalen die vaak gevraagd worden. Wat ook interessant is, is het woord “management”. Kijkende naar de vacatures vermoed ik dat dit vacatures zijn waar wordt vermeld dat men moet rapporteren aan het management. 

#### Stap 3: Bigrams
De volgende stap in de analyse is het maken van zogenaamde bigrams. Dit zijn combinaties van woorden om te zien welke woorden het vaakst bij elkaar genoemd worden.  

Dit kan gevisualiseerd worden in een netwerkgrafiek om inzicht te krijgen in welke frequentie de woorden bij elkaar worden genoemd. De richting van de pijl geeft de leesrichting aan en de dikte van de pijl de frequentie. Er is een splitsing gemaakt tussen vacatures die in het Engels zijn en vacatures die in het Nederlands zijn. 

<img src="{{ site.url }}{{ site.baseurl }}/images/netwerk NL.png" alt="linearly separable data">
<sub>*Grafiek 2: Netwerkgrafiek Nederlands* </sub>

Wat mij opvalt dat communicatieve en analytische vaardigheden hier sterk naar voren komen (linksboven). Onderaan zie je "engelse taal" en "nederlandse taal". 

<img src="{{ site.url }}{{ site.baseurl }}/images/Netwerk_ENG.png" alt="linearly separable data">
<sub> *Grafiek 3: Netwerkgrafiek Engels* </sub>

Ook hier worden communicatieve en analytische vaardigheden frequent genoemd. Een verschil dat ik zie ten opzichte van de Nederlandse vacatures, is dat hier "team members" en "team players" genoemd worden, terwijl bij de Nederlandse vacatures "Zelfstandig werken" wordt genoemd. Blijkbaar leggen werkgevers die Engelstalige werknemers zoeken een grotere nadruk op samenwerken dan Nederlandstalige werknemers. 

<img src="{{ site.url }}{{ site.baseurl }}/images/netwerk.png" alt="linearly separable data">
<sub>*Grafiek 4: Netwerkgrafiek Nederlands en Engels* </sub>

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
