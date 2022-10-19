Diese Vorlage ist für IntelliJ optimiert. 

# Projekt starten

  ## benötigte Programme
  - IntelliJ (https://www.jetbrains.com/idea)
  - MiKTeX (https://miktex.org)
  - TeXiFy IDEA Plugin
  - PDF Viewer Plugin (optional: zum Ansehen der PDF-Datei in IntelliJ)
  
  ## Run Configurations
  Neue Konfiguration hinzufügen (kompiliert TeX-Dokument):
    - LaTeX
    - Compiler: pdfLaTeX
    - PDF Viewer: No PDF Viewer oder Built-in PDF Viewer (PDF Viewer Plugin benötigt)
    - Main file to compile: {...}/Ausarbeitungen/{Vorlage}/{Dokument.tex}
    - Always compile at least twice
    - Output format: PDF
    - LaTeX Distribution: MiKTeX
    
  Neue Konfiguration hinzufügen (kompiliert Bibliografie):
    - BibTeX
    - Compiler: BibTeX
    - Main file that includews bibliography: {...}/Ausarbeitungen/{Vorlage}/{Dokument.tex}
    - Working directory for bibtex: {...}/Ausarbeitungen/auxil
    
  Neue Konfiguration hinzufügen (kompiliert TeX-Dokument mit Bibliografie):
    - LaTeX
    - Compiler: pdfLaTeX
    - PDF Viewer: No PDF Viewer oder Built-in PDF Viewer (PDF Viewer Plugin benötigt)
    - Main file to compile: {...}/Ausarbeitungen/{Vorlage}/{Dokument.tex}
    - Always compile at least twice
    - Output format: PDF
    - LaTeX Distribution: MiKTeX
    - External LaTeX programs: {BibTeX Konfiguration}
  

# Neue Ausarbeitung 
Neue Ausarbeitungen können im Ordner "Ausarbeitungen" erstellt werden. Dazu empfehlt es sich, den Ordner "Vorlage" zu kopieren.

# Ausarbeitung kompilieren
- Wenn sich seit des letzten Kompilats Änderungen an der Bibliograpfie ergeben haben, wird die zuletzt erläuterte Konfiguration ausgeführt.
- Wenn sich seit des letzten Kompilats keine Änderungen an der Bibliograpfie ergeben haben, wird die zuerst erläuterte Konfiguration ausgeführt.
