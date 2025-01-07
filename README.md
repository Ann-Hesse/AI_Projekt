# AI_Projekt
# Projektbeschrieb
Analyse von Kundenfeedback auf der Website Yelp
Ziel: Vergleich verschiedener Modelle zur Textanalyse
Daten: Yelp Review Sentiment Dataset (Kaggel)
Datenbeschrieb: Das Feedback ist auf zwei Datensets, einem Trainings- und einem Testdatenset. Neben dem Komentar gaben die Kunden Feedback mit Sternen. Ein und zwei Sterne werden beim Labeln als Negativ = 1 angesehen und drei bis vier Sterne als Positiv = 2. Das Trainingset beinhaltet rund 560'000 Daten und das Testset rund 38'000 Daten. 
# Einschränkungen: 
- Für effektives arbeiten am Projekt wird bei allen Modellen nur 10% der vorhandenen Daten verwendet.
- Verzicht auch Modelle wie Ilama, da die Fehlermeldung "CURSO, zu wenig Speicherplatz" nicht behoben werden konnte.
# Verwendete Modelle:
  - TextBlob
  Vorteile: Wenig Setup, einfach zu bedienen und wenig Ressourcen
  Nachteil:Begrenzte Genauigkeit und keine kontextabhängige Analyse von Wörtern
  Ergebniss: Schnelle Einschätzung der Stimmung und Subjektivität.
  - TF-IDF
  Vorteile: Identifiziert wichtige Begriffe, 
  Nachteil: Speicherintensiv durch die spärliche Erzeugung von Vektoren & keine semantische oder kontextabhängige Erfassung     von Wortbedeutungen. 
  Ergebniss: Nützlich zur Identifizierung von relevanten Begriffen.
  - Word2Vec
  Vorteile: Dichte Vektoren zur Erfassung von semantischen Ähnlichkeiten zwischen Wörtern
  Nachteil: Mehr Rechenressourcen und Training ist erforderlich & keine Kontextabhängige Erfassung von Wörtern in langen        Texten.  
  Ergebniss: Leistungsfähig für Aufgaben, welche semantische Beziehungen erfordern. 
