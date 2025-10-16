# Projekt: Analyse von DAX-Crashs mit der Extremwerttheorie

##Worum geht's in diesem Projekt?

Die meisten Finanzmodelle gehen von normalverteilten Renditen aus. Das funktioniert im Alltag ganz gut, aber komplett falsch, wenn es um Krisen geht. Crashs passieren viel öfter und sind viel heftiger, als es eine Normalverteilung erlaubt (sogenannte "Fat Tails").

In diesem Projekt habe ich mich genau auf diese seltenen, aber extrem wichtigen Ereignisse konzentriert. Mithilfe der **Generalized Extreme Value (GEV) Distribution** aus der Extremwerttheorie habe ich die schlimmsten Tagesverluste des DAX seit 1990 analysiert, um eine statistisch fundierte Aussage über zukünftige Crash-Risiken zu treffen.

---

##Die Mathe dahinter

* **Extremwerttheorie (EVT):** Anstatt alle täglichen Renditen zu betrachten, fokussiert sich die EVT nur auf die Extremwerte. Die "Block Maxima"-Methode, die ich hier verwendet habe, nimmt sich z.B. nur den allerschlimmsten Verlust aus jedem Jahr.
* **Generalized Extreme Value (GEV) Distribution:** Laut Theorie konvergiert die Verteilung dieser Extremwerte gegen die GEV-Verteilung. Indem ich diese Verteilung an die historischen DAX-Daten anpasse, erstelle ich ein Modell, das speziell auf die Dynamik von Crashs zugeschnitten ist.
* **Return Level:** Das ist die praktische Anwendung des Modells. Es beantwortet die Frage: "Welchen Tagesverlust (in %) müssen wir statistisch gesehen alle 10, 20 oder 50 Jahre mindestens einmal erwarten?"

---

##Ergebnis

Das Ergebnis ist ein Modell, das die Wahrscheinlichkeit von extremen Marktereignissen viel realistischer einschätzt als Standardansätze. Die Analyse zeigt zum Beispiel, dass ein Tagesverlust von über 7% statistisch gesehen etwa alle 10 Jahre zu erwarten ist.

Das ist eine wichtige Erkenntnis für jedes Risikomanagement, da es hilft, Kapitalpuffer und Absicherungsstrategien richtig zu dimensionieren.

![Plot der GEV-Anpassung an DAX-Verluste](httpstps://i.imgur.com/your_image_placeholder.png)
*(Hier könntest du einen Screenshot deines Plots hochladen und verlinken)*

---

##Wie man's ausführt

Das Projekt ist in einem Jupyter Notebook (`.ipynb`) geschrieben. Einfach das Repository klonen und die benötigten Pakete installieren:

`pip install -r requirements.txt`
