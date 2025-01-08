# AI_Projekt
# Projektbeschrieb
Analyse von Kundenfeedback auf der Website Yelp
Daten: Yelp Review Sentiment Dataset (Kaggel)
Datenbeschrieb: Das Feedback ist auf zwei Datensets, einem Trainings- und einem Testdatenset. Neben dem Komentar gaben die Kunden Feedback mit Sternen. Ein und zwei Sterne werden beim Labeln als Negativ = 1 angesehen und drei bis vier Sterne als Positiv = 2. Das Trainingset beinhaltet rund 560'000 Daten und das Testset rund 38'000 Daten. 
Link zum Datenset: https://www.kaggle.com/datasets/ilhamfp31/yelp-review-dataset
# Zielsetzung
Ziel des Projekts ist es, verschiedene Sentiment-Analyse-Modelle auf den Yelp-Kundenbewertungen zu trainieren und deren Genauigkeit sowie Performance zu vergleichen. Dabei wird der Fokus auf der Anwendung verschiedener Methoden der Textanalyse (z. B. TextBlob, GloVe, RoBERTa) gelegt, um zu ermitteln, welche Modelle am besten geeignet sind, um das Sentiment der Bewertungen zu klassifizieren. Die Analyse der Modelle umfasst dabei folgende Punkte:
- Vergleich der Genauigkeit der Modelle
- Untersuchung der Vor- und Nachteile der jeweiligen Modelle, einschließlich der Anforderungen an Rechenressourcen und ihrer Fähigkeit, Kontextinformationen zu verarbeiten.
- Analyse der Modelle bezüglich ihrer Fähigkeit zur Identifikation relevanter Begriffe und deren semantische Erfassung.
- Evaluation der Ergebnisse hinsichtlich der Problemstellung und deren Relevanz für praktische Anwendungen im Bereich der Kundenfeedback-Analyse.
# Einschränkungen:
- Für das effektive Arbeiten am Projekt wird bei allen Modellen nur 10% der vorhandenen Daten verwendet.
- Der Einsatz von Modellen wie Ilama wurde ausgeschlossen, da immer wieder eine Fehlermeldung wegen zu wenig Speicherplatz  nicht behoben werden konnte.
- Damit das Notebook schneller durchläuft sind Verbesserungsvorschläge für den Basiccode als Komentar in der Zeile eingefügt.

# Verwendete Modelle:
  - TextBlob
  Vorteile: Wenig Setup, einfach zu bedienen und wenig Ressourcen
  Nachteil:Begrenzte Genauigkeit und keine kontextabhängige Analyse von Wörtern
  Ergebniss: Schnelle Einschätzung der Stimmung und Subjektivität.
  - GloVe (Global Vectors for Word Representation):
  Vorteile: Dichte und vektorielle Repräsentationen von Wörtern und das Erfassung von semantischen Beziehungen und     
  Kontextinformationen der Vektoren. 
  Nachteil: Speicherintensiv und keine kontextabhängige Erfassung von Wortbedeutungen. 
  Ergebniss: Nützlich für die semantische Erfassung von Wortbedeutungen.
  - RoBERTa (Robustly optimized BERT approach)
  Vorteile: Kontextabhängige Vektorrepräsentationen von Wörtern, dass heisst die Bedeutung eines Wortes wird im Kontext des 
  gesamten Satzes oder Dokuments verstanden. Bereits auf riesigen Mengen unbeschrifteter Daten vortrainiert. 
  Geeignet auf sehr grossen Datensätzen trainiert zu werden.
  Nachteil: Rechenintensiv und benötigt signifikante Hardware-Ressourcen, insbesondere GPUs, um in akzeptabler Zeit 
 trainiert oder inferiert zu werden. 
 Das Modell benötigt großen Speicher, da es viele Parameter enthält und mit großen Datensätzen trainiert wurde. Bla
 Black Box-Modell, es kann schwierig sein nachzuvollziehen warum bestimmte Vorhersagen getroffen werden.
 # Evaluation der Ergebnisse
- TextBlob:
TextBlob liefert sehr niedrige Genauigkeitswerte. Das sowohl auf die Trainingsdaten wie auch auf die Testdaten. Dies erkläre ich mir dadurch, dass TextBlob keine semantischen Analysen macht. Das Model ist zwar schnell und ressourcenschonend, jedoch nicht ausreichend leistungsfähig, um das Rückmeldungen in der Yelp-Bewertung in einer hohen Genauigkeit zu Labeln. 
- GloVe (Global Vectors for Word Representation):
Die Logistische Regression, kombiniert mit vortrainierten Wortvektoren (wie GloVe), zeigt eine signifikante Verbesserung im Vergleich zu TextBlob. Die Genauigkeit sowohl im Training als auch im Test ist viel höher, was zeigt, dass  das Modell besser zwischen positiven und negativen  Bewertungen unterscheiden kann. Mit einer Genauigkeit von rund 0.8 ist jedoch 
 noch Luft nach oben.
- RoBERTaliefert die besten Ergebnisse sowohl im Training als auch im Test. Die Trainingsgenauigkeit ist sehr hoch, und auch die Testgenauigkeit ist mit 96,53 % sehr gut. Dieses Modell hat den Vorteil, dass es auf einem Transformer-Modell basiert, das kontextabhängige Vektorrepräsentationen von Wörtern erzeugt. Dadurch wird die Bedeutung eines Wortes nicht nur isoliert betrachtet, sondern im Kontext des gesamten Satzes oder Dokuments. Dies sehe ich als ein Faktor für das eindeutig beste Resultat. Die hohe Genauigkeit auf die Testdaten zeigt, dass das Modell robust ist und zu zuverlässigen Lösungen führt.
-Fazit
Der Vergleich der Modelle zeigt, dass für das Labeln von Kundenrückmeldungen, wie beispielsweise bei Yelp-Bewertungen, sowohl die sentimentale Analyse als auch der Kontext der Wörter eine entscheidende Rolle spielen. 
