<!--
author:   Sebastian Zug, André Dietrich, Martin Lommatzsch, Matthias Saurbier, Thomas Schumann

email:    Sebastian.Zug@informatik.tu-freiberg.de

version:  0.0.5

language: de

narrator: Deutsch Male

mode:     Presentation

comment:  Dieser Kurs für in das Projekt LiaScript ein und diskutiert die
          Vorteile im Kontext der OER Idee.

logo:     ./images/logo.png

import:   https://raw.githubusercontent.com/LiaTemplates/LiveEdit-Embeddings/refs/tags/0.0.1/README.md
          https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md

translation: Deutsch  translations/German.md

@style
.flex-container {
    display: flex;
    flex-wrap: wrap; /* Allows the items to wrap as needed */
    align-items: stretch;
    gap: 20px; /* Adds both horizontal and vertical spacing between items */
}

.flex-child { 
    flex: 1;
    margin-right: 20px; /* Adds space between the columns */
}

@media (max-width: 600px) {
    .flex-child {
        flex: 100%; /* Makes the child divs take up the full width on slim devices */
        margin-right: 0; /* Removes the right margin */
    }
}
@end

-->

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/SODa-Tutorial/refs/heads/main/Motivation.md)

# Konzepte und Motivation hinter LiaScript


<section class="flex-container">

<!-- class="flex-child" style="min-width: 250px;" -->
> <h2>Herzlich Willkommen!</h2>
>
><h4>SODa meets LiaScript, 29. August 2025</h4>

<!-- class="flex-child" style="min-width: 250px;" -->
![partner_map](pic/LiaScript_Meets_OER.png "OER-Logo - Quelle: Jonathasmello - Eigenes Werk, CC BY 3.0, [https://commons.wikimedia.org/w/index.php?curid=18460156](https://commons.wikimedia.org/w/index.php?curid=18460156) erweitert um LiaScript Logo")

</section>

--------------------------------------------

_ Der Quellcode kann des Open Source Dokuments ist unter [Link](https://github.com/LiaPlayground/SODa-Tutorial/blob/main/Motivation.md) zu finden._


## Akteure und Ziele der Veranstaltung

Wer sind wir?
=====================

+ __Sebastian Zug__ 
+ __André Dietrich__

TU Bergakademie Freiberg, Institut für Informatik

Was wollen wir heute erreichen?
====================

| Abschnitt des Tutorials                              |     Dauer     |
| ---------------------------------------------------- | :-----------: |
| Einführung in die Konzepte von LiaScript             | 09:00 - 09:50 |
| Einstiegstutorial zu LiaScript anhand eine Beispiels | 10:00 - 10:50 |
| Erweiterte Funktionen (eigene Makros, Plugins)       | 11:00 - 11:50 |


## Ausgangspunkt

>  <!-- Style="color:green" -->__Lehrende möchten motivierende, interaktive, digitale Lehrmaterialien in ihren Unterricht einbetten.__

                  {{0-1}}
********************************************

---------------------

Beispiel Quizze:


- [[male (der)] (female [die]) [neuter (das)]]
- [    [X]           [ ]             [ ]     ]  Mann - German for man
- [    ( )           (X)             ( )     ]  Frau - German for woman

********************************************

                  {{1-2}}
********************************************

---------------------

Beispiel 3D-Modelle:

??[ear model](https://sketchfab.com/3d-models/familienschacht-freiberg-germany-7c7d30506c554385a4a4321366e2e601)


********************************************

                  {{2-3}}
********************************************

---------------------

Beispiel Simulationsumgebung:

<div>
  <wokwi-led color="red" pin="13" port="B" label="13"></wokwi-led>
  <span id="simulation-time"></span>
</div>
```cpp       arduino.cpp
// einmaliges Ausführen
void setup() {
  pinMode(13, OUTPUT);
}

// Endlosschleife
void loop() {
  digitalWrite(13, HIGH);
  delay(1000);
  digitalWrite(13, LOW);
  delay(1000);              
}
```
@AVR8js.sketch

********************************************

                  {{3-5}}
********************************************

__Aber ...__

+ Die individuelle Umsetzung ist aufwändig und zeitintensiv.
+ Für verschiedene Formate (z.B. Text, Video, Audio, 3D-Modelle) gibt es unterschiedliche Werkzeuge.
+ Bestehende Inhalte sind nicht auf die individuellen Bedürfnisse von Lehrenden und Lernenden zugeschnitten.
+ ...

> Welche weiteren Hemmnisse kennen Sie aus Ihrer Praxis?

********************************************

{{5}}
********************************************

<!--
style="width: 100%; max-width: 860px; display: block; margin-left: auto; margin-right: auto;"
-->
```ascii

      Wunsch nach                                             Wunsch nach
  einfacher Umsetzung  -----------> Konflikt <----------- spezifischen Elementen
                                                               im Material.
```

********************************************

### OER als Lösungsansatz

           {{0-3}}
**************************************

<!--
style="width: 100%; max-width: 860px; display: block; margin-left: auto; margin-right: auto;"
-->
```ascii

      Wunsch nach                                             Wunsch nach
  einfacher Umsetzung  -----------> Konflikt <----------- spezifischen Elementen
                                       |                       im Material
                                       |
                                       v
                              OER als Lösungsansatz
```

> OER beschreibt die gemeinsame Entwicklung, Nutzung und Verbreitung von Lehr- und Lernmaterialien, die unter einer offenen Lizenz stehen.

************************************

           {{1-2}}
**************************************

>  **Open Courseware / Open Educational Resources** ... teaching, learning and
> research materials in any medium, digital or otherwise,that reside in the
> **public domain** or have been released under an open license that permits
> no-cost access, use, **adaptation** and **redistribution** by others with no or 4
> limited restrictions. Open licensing is built within the existing framework of
> intellectual property rights as defined by relevant international conventions
> and respects the authorship of the work
>
> -- UNESCO 2002 Forum on the Impact of Open Courseware for Higher Education in Developing Countries [(Link)](https://unesdoc.unesco.org/ark:/48223/pf0000128515)

**************************************

           {{2-3}}
**************************************

| Anforderung an OER Materialien | Bedeutung                                  |
| ------------------------------ | ------------------------------------------ |
| `verwahren/vervielfältigen `   | Download, Speicherung und Vervielfältigung |
| `verwenden`                    | Nutzung im Lernkontext                     |
| `verarbeiten`                  | Umgestaltung und Adaption                  |
| `vermischen`                   | Kombination und Extraktion                 |
| `verbreiten`                   | (digitale) Publikation                     |


*_5 V-Freiheiten für Offenheit_ von Jöran Muuß-Merholz und Jörg Lohrer für [open-educational-ressources](https://open-educational-resources.de) - Transferstelle für OER*

**************************************


### Kritik am OER-Ansatz


| Ebene                               | Kernaussage                                                                                  |
| ----------------------------------- | -------------------------------------------------------------------------------------------- |
| Emotionale Einordnung               | "_Da kann ja jeder meine Arbeit für sich nutzen!_"                                           |
|                                     | "_Da kann mich ja jeder kontrollieren!_"                                                     |
| Rechtliche Herausforderungen        | "_Ich verwende viele Grafiken, bei deren Urheberrecht ich mir im besten Fall unsicher bin!_" |
| Auffindbarkeit                      | "_Ich finde keine Inhalte, die ich in meiner Lehre gewinnbringend integrieren kann!_"        |
| <!-- Style="color:red" --> Aufwand  | <!-- Style="color:red" --> "_Da muss man ja Informatik studiert haben!_"                     |
| <!-- Style="color:red" -->Abdeckung | <!-- Style="color:red" -->"_Da fehlen mir aber die Schnittstellen für meine Tools XY!_"      |


### Idealer Prozess 

<!--
style="width: 100%; max-width: 860px; display: block; margin-left: auto; margin-right: auto;"
-->
```ascii

Kurs.txt         Version 1.0          Kurs.txt          Version 1.1
+--------------------------+          +---------------------------+
| Kurs  Deutsche Literatur |          | Kurs  Deutsche Literatur  |
| Autor Peter Muster       | "Fehler" | Autoren Peter Muster      |
|                          |------>   |         Angelika Maier    |----->
|~~~~~~~~~~~~~~~~~~~~~~~~~~|          |~~~~~~~~~~~~~~~~~~~~~~~~~~~|
| Ab 1756 bereiste Goethe  |---.      | Ab 1786 bereiste Goethe   |--.
| Italien ...              |   |      | Italien ...               |  |
                               |                                     |    Course.txt       Version 1.1.2
                               |                                     |    +----------------------------+
                               |                                     |    | Kurs  German Literature    |
                               |                                     |    | Autoren Peter Muster       |
                               |                                     .--> |         Angelika Maier     |
                               |                                          |         Steve Gray         |
                               |                                          |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|
                               |                                          | In 1786 Goethe traveled to |
                               |                                          | Italy ...                  |
                               |      Kurs.txt         Version 1.0
                               |      +---------------------------+
                               |      | Kurs  Goethes Welt        |
                               |      | Autoren Peter Muster      |
                               .-->   |         Angelika Maier    |----->
                                      |~~~~~~~~~~~~~~~~~~~~~~~~~~~|
                                      | Während der italienischen |
                                      | Reise ...                 |
```
*Versionen der Lehrinhalte eines Kurses und deren Wiederverwendung in anderen Veranstaltungen*

{{0-1}}
********************************************************************************

| Anforderung                  | txt | Begründung                                               |
| ---------------------------- | --- | -------------------------------------------------------- |
| `verwahren/vervielfältigen ` | ++  | vorteilhaft wegen geringer Größe                         |
| `verwenden`                  | +   | analoge / digitale Verteilung an Studieren unkompliziert |
| `verarbeiten`                | ++  | verarbeitbar ohne zusätzliche Software                   |
| `vermischen`                 | +   | einfache Kombination von Textfragmenten per Copy&Paste   |
| `verbreiten`                 | +   | gut exportierbar                                         |

> **Moment, ein reines Textdokument ist als OER Inhalt perfekt? Wahrscheinlich nicht!**

********************************************************************************

### Wie lösen das andere Autorenkollektive?

Wikipedia ist ein gutes Beispiel für eine Plattform, die die 5V-Freiheiten umsetzt und dabei eine große Menge an Inhalten bereitstellt. Die Inhalte sind in einem offenen Format (MediaWiki) gespeichert und können von jedem bearbeitet und weiterverwendet werden.

Wikipedia nutzt dabei eine einfache Textsprache (Wikitext), die es ermöglicht, Inhalte zu formatieren und zu strukturieren. 

```markdown     Ausschnitt aus dem Wikipedia Artikel "TU Bergakademie Freiberg"
Die '''Technische Universität Bergakademie Freiberg''' (TU Bergakademie Freiberg, TUBAF)
ist eine staatliche [[Technische Universität]] in [[Freiberg]] in [[Sachsen]]. Sie 
versteht sich als [[Ressourcenuniversität]] und widmet sie sich in Lehre und Forschung 
der Geo-, Ingenieur-, Natur- und Wirtschaftswissenschaften. Dabei spezialisiert sie 
sich auf die Energie- und Ressourcenwirtschaft.
```

https://de.wikipedia.org/w/index.php?title=Technische_Universit%C3%A4t_Bergakademie_Freiberg&action=edit

> Der Wikipedia-Ansatz hat mit Blick auf Lehrmaterialien aber entscheidende Nachteile. Die Inhalte sind:

- nicht auf die individuellen Bedürfnisse von Lehrenden und Lernenden zugeschnitten,
- statisch und nicht interaktiv,
- nicht in einem Format, das eine einfache Integration in Lernmanagementsysteme (LMS) ermöglicht,
- ...


## LiaScript - Kernkonzepte


                        {{0-1}}
*******************************************************

> __1. Wir trennen Darstellung und Inhalt! Alle Elemente werden soweit wie möglich durch eine rein textuelle Repräsentation ausgedrückt.__

```markdown @embed.style(height: 550px; min-width: 100%; border: 1px black solid)
# Vom Text zur Darstellung

__Text__

Hallo Welt!

__Mathematik__

$f(x) = x^2$

__Tabellen__

| x | B(x) | C(x) |
|---|:----:|:----:|
| 1 |   2  |   3  |
| 4 |   5  |   6  |

```

*******************************************************

                        {{1-2}}
*******************************************************

> __2. Digitale Lehre lebt von Interaktion!__

```markdown @embed.style(height: 550px; min-width: 100%; border: 1px black solid)
# Lehre lebt von Interaktion

__Tabellen als Grafiken__

| X | B(y) | C(y) |
|---|:----:|:----:|
| 1 |   2  |   3  |
| 4 |   5  |   6  |

__Quizze__

Wann wurde die TU Bergakademie gegründet?

- [(X)] 1765
- [( )] 1896
```

*******************************************************

                        {{2-3}}
*******************************************************

> __3. Der Browser kann viel mehr als Webseiten anzuzeigen.__

````markdown @embed.style(height: 550px; min-width: 100%; border: 1px black solid)
<!--
import: https://raw.githubusercontent.com/liaTemplates/ABCjs/main/README.md
-->

# Browserfeatures / JavaScript

__Sprache__

> Click to run!
>
> {{|> Deutsch Female}}
> Hallo liebe LiaScript Interessierte!

__Datenspeicherung__

``` abc
X:353
T: GLUECK AUF DER STEIGER KOEMMT
N: E1512
O: Europa, Mitteleuropa, Deutschland
R: Staende -, Bergmanns - Lied
M: 4/4
L: 1/16
K: G
| G8F4A4 | G8z8 | B8A4c4 | B8z4G2A2 | B4B4B4A2B2 | c4A3AA4
A2B2 | c4c4c4B2c2 | d4B3BB4A4 | G8F8 | G4e4d4c2A2 | B8A8 | G8z8
```
@ABCJS.eval
````

*******************************************************

                        {{3-4}}
*******************************************************


> __4. Wir brauchen Werkzeuge für die Umsetzung in verschiedenen Umgebungen.__

<!--
style="width: 100%; max-width: 860px; display: block; margin-left: auto; margin-right: auto;"
-->
```ascii
+------------------+
| # Digital Systems|\                                      .-----------.
| (SoSe 2021)      +-+                              ╔══════|   LMS  X  |══════╗
|                    |  --------------------------> ║      '-----------'      ║
| Task 1             |                              ║ Digital Systems 2021    ║
|                    |                              ║                         ║
| + Implement ...    | --------------+              ║ import numpy as np      ║
|                    |    Trans-     |              ║ ...                     ║
|                    |    formation  |              ╚═════════════════════════╝
+--------------------+               v
                                .-,(   ),-.                .-----------.
Lizenz: ...                  .-(           )-.      ╔══════|   LMS  Y  |══════╗
Inhalt: ...                 (    OER Cloud    )     ║      '-----------'      ║
Autor: ...                   '-(           )-'  +-->║ Digital Systems 2021    ║
Versionshistorie: ...           '-.(   ).-'     |   ║                         ║
                                     |          |
                                     +----------+          .-----------.
                                                |   ╔══════|  Webapp   |══════╗
                                                |   ║      '-----------'      ║
                                                +-->║ Digital Systems 2021    ║
                                                    ║                         ║                                     .
```


*******************************************************

## Grundlegende Werkzeuge und Infrastruktur

__Wo finde ich weitere Informationen?__

+ [Projektwebseite](https://liascript.github.io/) 
+ [Dokumentation](https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md#1)
+ [Youtube-Channel](https://www.youtube.com/channel/UCyiTe2GkW_u05HSdvUblGYg)

__Welchen Editor sollte ich benutzen?__

+ LiveEditor: [https://liascript.github.io/LiveEditor/](https://liascript.github.io/LiveEditor/)
+ Visual Studio Code 
+ Codespaces

> Im Rahmen dieses Tutorials werden wir uns auf den LiveEditor konzentrieren.

__Wie "verteile" ich meine Inhalte?__

+ direkt aus dem LiveEditor (Data URLs, Nostr, Gist)
+ in einem Webspace
+ über Git Repositories
+ in einem LMS

> Seit Juli 2025 können LiaScript-Kurse direkt in OPAL importiert werden. Dies wurde durch eine Kooperation der TU Bergakademie und der TU Chemnitz sowie der BPS GmbH ermöglicht [Link](https://blog.hrz.tu-chemnitz.de/urzcommunity/2025/07/08/neu-im-opal-mit-liascript-schnell-zum-anschaulichen-interaktiven-kurs/). [Beispielkurs](https://bildungsportal.sachsen.de/opal/auth/RepositoryEntry/28960423936?4) 

## Erfahrungen bei der Nutzung

+ LiaScript ermöglicht den Einsatz interaktiver Materialien sowohl für die Vorlesungs-/übungsbegleitung als auch für die Selbstlernphasen.
+ Die Applikation von Softwareentwicklungstools ist wegen der Textbasierten Inhaltsrrepräsentation außerordentlich hilfreich.
+ Studierende werden in die Materialgestaltung aktiv einbezogen, damit steigt deren Qualität bei gleichzeitig wachsender Motivation.

> Die Materialien der AG Softwaretechnologie und Robotik finden sich unter https://github.com/TUBAF-IfI-LiaScript.

!?[](https://github.com/TUBAF-IfI-LiaScript/.github/assets/10922356/00a24602-dc63-4b9a-894b-80967b914513)

## Zusammenfassung

LiaScript löst den Inhalt vom LMS und erlaubt die Anwendung von Methoden der verteilten Softwareentwicklung.

- Beschreibungssprache
- Verteilte Entwicklung
- Serverlose Infrastruktur
- Dynamische Inhalte

> __Jetzt wird es spannend und Sie sind gefragt ...__
>
> __Rufen Sie bitte den Link [Tutorial](https://liascript.github.io/LiveEditor/?/show/file/https://raw.githubusercontent.com/LiaPlayground/SODa-Tutorial/refs/heads/main/Kochbuch.md) auf, um den LiveEditor zu starten.__
