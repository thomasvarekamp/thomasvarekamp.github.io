---
title: "Sony artiesten. Wie lijkt (niet) op elkaar?"
date: 22-06-2020
tags: [data wrangling, data science, music]
header:
---
In de bedrijfsbeschrijving van Sony Music Entertainment staat een lijst met artiesten die Sony representeert. Mijn hypothese is dat specifiek deze artiesten hier in staan om te laten zien dat Sony een veelzijdig roster aan artiesten vertegenwoordigd.


Maar, is dat ook zo?


De volgende artiesten worden genoemd: Beyoncé, BLØF, Bruce Springsteen, Calvin Harris, Dimitri Vegas & Like Mike, Enrique Iglesias, Gavin James, George Ezra, Justin Timberlake, King Princess, Kygo, Little Mix, Mariah Carey, Martin Garrix, Nielson, Pharrell Williams, P!nk, Rosalía, Tom Walker en Travis Scott.


Ik ga eerst met behulp van de Spotify API gegevens ophalen van de artiesten en de liedjes. Vervolgens pak ik de gemiddelden van alle kenmerken van deze tracks. Hieronder vallen: acousticness, danceability, energy, instrumentalness, liveness, loudness, speechiness, valence, tempo. Hier zal ik met behulp van een principal component analyse de dimensies reduceren om te onderzoeken of deze nieuwe dimensies bruikbare informatie bevatten en om de artiesten mee te onderscheiden.


*Spotify hanteert de volgende definities:*

acousticness: confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.

danceability: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.

energy: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.

instrumentalness: Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.

liveness: Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.

loudness: The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude).

speechiness: Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.

valence: A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).

tempo: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.

Hier een deel van de data:

<img src="{{ site.url }}{{ site.baseurl }}/images/Table.png" alt="">

Vervolgens maak ik een aantal grafieken om een beter gevoel te krijgen bij de data:

<img src="{{ site.url }}{{ site.baseurl }}/images/Energy.png" alt="">

Dimitri Vegas en Like Mike maken voornamelijk energieke Bigroom House, dus het lijkt mij logisch dat zij op nummer 1 staan. Wat interessant is dat Enrique Iglesias boven Martin Garrix staat, terwijl Martin Garrix vroeger veel house uitbracht. Waarschijnlijk heeft zijn overgang naar meer pop muziek ervoor gezorgd dat het gemiddelde is gedaald. Dit zou uitgezocht kunnen worden door de data per liedje te bekijken, maar dat is buiten de scope van deze analyse.

<img src="{{ site.url }}{{ site.baseurl }}/images/Speechiness.png" alt="">

Welke grafiek ik ook interessant vind om te maken, is speechiness. De afgelopen 10 jaar heeft er een grote verschuiving in populariteit van elektronische instrumentale liedjes naar pop muziek met zang of rap plaatsgevonden. Beyoncé scoort hier veruit het hoogste. Interessant om te zien dat BLØF, een poprockband, hier het laagst scoort.

# PCA en clustering: welke artiesten lijken (niet) op elkaar?

Een PCA (principale componenten analyse) is een methode om de variatie in een dataset samen te vatten en samenhang tussen de gegevens zichtbaar te maken. In plaats van 9 variabelen te pakken uit de dataset, is het wellicht mogelijk om de data samenvatten in 2-3 variabelen zodat te visualiseren is.

<img src="{{ site.url }}{{ site.baseurl }}/images/PCA.png" alt="">

Hierboven is te zien dat zo’n 60% van de dataset samengevat kan worden met 2 componenten. Ik kan nu zien hoe zwaar elke variabele weegt in het component en zo dus zien hoe deze is samengevat:

<img src="{{ site.url }}{{ site.baseurl }}/images/PCA table.png" alt="">

Ik zie dat bij component 1 danceability, energy, loudness en tempo hoog scoren. Mijn interpretatie is dat deze artiesten die hoog scoren op dit component het goed doen in de club. Bij component 2 scoren liveness en tempo hoog, terwijl danceability, instrumentalness en valence laag scoren. Ik vermoed dat dit voornamelijk om artiesten gaan die verdrietige / boze (lage valence) liedjes maken met zang of rap.

<img src="{{ site.url }}{{ site.baseurl }}/images/Club vs emo.png" alt="">

Het is te zien dat Martin Garrix zowel hoog scoort op de emotionele-as, als de club-as. Dit klopt ook wel met mijn beeld. In the name of love en Higher Ground passen hier bij. Travis Scott scoort ook hoog op allebei de assen. Interessant is dat Dimitri Vegas en Like Mike het hoogst scoren op de club-as, wat in mijn ogen ook correct is. Justin Timberlake en Pharell Williams scoren laag op de emotionele / boze-as. Zij maken dan ook veel vrolijke muziek.

## Conclusie
De artiesten in de bedrijfsbeschrijving van Sony verschillen redelijk van elkaar. Wel zijn er duidelijke overeenkomsten te vinden tussen artiesten als er gekeken wordt naar de PCA componenten. Zo scoort de muziek van Martin Garrix, Travis Scott en DMVLM over het algemeen goed op de as die ik classificeer als club en is de muziek van Justin Timberlake en Pharell Williams voornamelijk niet emotioneel of boos.






