# Klassifizierung von Insekten an Hand des Flügelschlags

Insekten eines Typs und Geschlechts haben sehr ähnliche Flügelschläge in Winkel und Frequenz. Da ihre (unverletzten) Flügel auch ähnlich gebaut sind hören sie sich auch sehr ähnlich an (harmonische Oberwellen). Ausnahmen sind Männchen einiger Mosquitoarten, die in der Paarungszeit den Klang der Weibchen, das die umwerben, immitieren.
[Insect-flight](https://en.wikipedia.org/wiki/Insect_flight)

Der Flügelschlag kann mit verschiedenen Verfahren vermessen werden. Akustisch durch Schall oder Licht, Radar, Highspeedkamera mit Bildverarbeitung

[Spitzen, Jeroen & Takken, Willem. (2018). Keeping track of mosquitoes: A review of tools to track, record and analyse mosquito flight. Parasites & Vectors. 11. 10.1186/s13071-018-2735-6. ](https://parasitesandvectors.biomedcentral.com/articles/10.1186/s13071-018-2735-6)

### Akustisches Mikrofon
Die passive, schallbasierte Vermessung des Flügelschlags ist sehr störungsbehaftet außerhalb des Labors. Wind und Reflektionen von anderen Tieren erzeugen breitbandige Störungen, die schwer zu entfernen sind. Somit ist es schwer, das eigentliche Nutzsignal zu isolieren. Fledermäuse nutzen daher aktive Echolokation und Erkennung, indem sie ein definiertes Signal aussenden und dieses Muster mit dem empfangenen Signal überlagern, um das Nutzsignal vom Hintergrundgreräusch trennen zu können.Ähnlich funktionieren auch moderne Radarsysteme. Je nach Verhalten des ausgesandten Signals können unterschiedliche Charakteristika an Beute und Umgebung erkannt werden. [Animal-echolocation](https://en.wikipedia.org/wiki/Animal_echolocation)

### Optisches Mikrofon
Strahlt man Licht auf ein fliegendes Insekt, so hat der Flügelschlag Einfluss auf die Intensität des Lichts hinter dem Insekt, da durch den sich ändernden Anstellwinkel der Flügel mal mehr oder weniger Licht abgeschattet wird. Ebenso ist das auch mit dem reflektierten Licht. Diese Helligkeitsschwankungen können durch einen Photodetektor gemessen werden. Niederfrequente Änderungen, die durch Sonnenlicht oder die Bewegung des Körpers hervorgerufen werden,lassen sich gut ausfiltern. Das erzeugte Signal hat eine Bandbreite im einstelligen kHZ Bereich und kann so mit günstigen Mikrocontrollern erfasst und verarbeitet werden. 

Zu zeigen: 
* eventuell auch Erkennung auf µC möglich mit Bayes
* horizontale oder vertikale Messung robuster

[Chen, Y., Why, A., Batista, G., Mafra-Neto, A., Keogh, E. Flying Insect Detection and Classification with Inexpensive Sensors. J. Vis. Exp. (92), e52111, doi:10.3791/52111 (2014).](https://arxiv.org/abs/1403.2654v1)

[Keogh, E.,Naive Bayes Classifier](https://www.cs.ucr.edu/~eamonn/CE/Bayesian%20Classification%20withInsect_examples.pdf)

[MDPI and ACS Style
Sandrini Moraes, F.; Edson Nava, D.; Scheunemann, T.; Santos da Rosa, V. Development of an Optoelectronic Sensor for Detecting and Classifying Fruit Fly (Diptera: Tephritidae) for Use in Real-Time Intelligent Traps. Sensors 2019, 19, 1254.](https://www.mdpi.com/1424-8220/19/5/1254/htm)

[Potamitis I, Rigakis I, Fysarakis K (2015)
Insect Biometrics: Optoacoustic Signal Processing
and Its Applications to Remote Monitoring of McPhail
Type Traps. PLoS ONE 10(11): e0140474.
doi:10.1371/journal.pone.0140474](https://pdfs.semanticscholar.org/1b32/68c05733fc8ac109b37251a67e5672cd6d9b.pdf)

[Rigakis, Iraklis & Potamitis, Ilyas & Tatlas, Nicolaos-Alexandros & Livadaras, Ioannis & Ntalampiras, Stavros. (2019). A Multispectral Backscattered Light Recorder of Insects’ Wingbeats. Electronics. 8. 277. 10.3390/electronics8030277. ](https://www.mdpi.com/2079-9292/8/3/277/htm)

[Michael A B Deakin, Formulae for insect wingbeat frequency, Journal of Insect Science, Volume 10, Issue 1, 2010, 96](https://doi.org/10.1673/031.010.9601)

[I. Potamitis and I. Rigakis, "Large Aperture Optoelectronic Devices to Record and Time-Stamp Insects’ Wingbeats," in IEEE Sensors Journal, vol. 16, no. 15, pp. 6053-6061, Aug.1, 2016.
doi: 10.1109/JSEN.2016.2574762](https://ieeexplore.ieee.org/document/7482663)

### Radar

In der Radartechnik wurde die Erkennung eines Flugzeugtyps durch Vermessung der Turbinenschaufeln und deren Drehzahl oder die Erkennung von Personen anhand ihres Gangs entwickelt. Hierbei wird der Umstand ausgenutzt, dass Teile des zu vermessenden Objekts relativ zum Großteil des Objekts bewegen (Beine und Arme). Bewegt sich das zu vermessende Objekt ebenfalls, so überlagert sich die relative Bewegung mit der globalen Bewegung. Bei den häufig eigesetzten Dopplerradaren wird dies durch eine periodische Änderung der Ausgangsfrequenz deutlich. Dabei ist die Grundfrequenz proportional zur Fluggeschindigkeit, relativ zum Radar und die Periodendauer der Frequenzänderungen entspricht der relativen Bewegung. Diese Frequenzänderung wird auch als Microdoppler bezeichnet. 
Dieses Verfahren kann auch zur Erkennung des Flügelschlags verwendet werden. Da Radare empfindlich auf sie zu oder von ihnen weg bewegenden Objekten reagieren, sollte der Radar in der Flugebene des Insekts sein.
Auch hier muss das Nutzsignal herausgefiltert werden. Neben der Frequenzmodulation durch den Flügel kann auch die Phasenmodulation verwendet werden, da diese auch periodisch moduliert wird durch den Flügelschlag. Hierzu braucht man neben dem reellen in-Phasesignal noch das imaginäre Q-Signal des Radars. Günstige Geräte führen dies meist nicht nach außen. Auch die das Arbeitsfrequenzband hat einen Einfluss auf das Ergebnis.

[Wang, R., Hu, C., Fu, X., Long, T., & Zeng, T. (2017). Micro-Doppler measurement of insect wing-beat frequencies with W-band coherent radar. Scientific reports, 7(1), 1396. doi:10.1038/s41598-017-01616-4](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5431090/)

### Highspeed Bildverarbeitung

Die Aufnahme eines fliegenden Insekts mittels einer Highspeedkamera, lässt auch Rückschlüsse auf die Schlagfrequenz zu. Diese Kameras brauchen wegen der kurzen Belichtungszeit des Bilder eine ausreichend starke Beleuchtung. Auch sind diese Kameras und die Hardware zur Verarbeitung der Bilder vergleichsweise teurer als die oben genannten Methoden. Daher wird dieses Verfahren zunächst nicht weiter verfolgt.
