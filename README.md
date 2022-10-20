## Diese Vorlage ist für **IntelliJ** optimiert. 

### Projekt starten

  #### benötigte Programme
  * [IntelliJ](https://www.jetbrains.com/idea)
  * [MiKTeX](https://miktex.org)
  * TeXiFy IDEA Plugin
  * PDF Viewer Plugin (optional: zum Ansehen der PDF-Datei in IntelliJ)
  
  #### Run Configurations (werden automatisch erstellt; *beim Working directory der BibTeX-Konfiguration kann es allerdings zu Fehlern kommen*)
  ###### Neue Konfiguration hinzufügen (kompiliert TeX-Dokument):
  * LaTeX
  * Compiler: pdfLaTeX
  * PDF Viewer: No PDF Viewer oder Built-in PDF Viewer (PDF Viewer Plugin benötigt)
  * Main file to compile: {...}/Ausarbeitungen/{Vorlage}/{Dokument.tex}
  * Directory for auxiliary files: {...}/auxil
  * Directory for output files: {...}/../Dokumente
  * Always compile at least twice: false
  * Output format: PDF
  * LaTeX Distribution: MiKTeX
    
  ###### Neue Konfiguration hinzufügen (kompiliert Bibliografie):
  * BibTeX
  * Compiler: BibTeX
  * Main file that includes bibliography: {...}/Ausarbeitungen/{Vorlage}/{Dokument.tex}
  * *Working directory for bibtex: {...}/auxil*
    
  ###### Neue Konfiguration hinzufügen (kompiliert TeX-Dokument mit Bibliografie):
  * LaTeX
  * Compiler: pdfLaTeX
  * PDF Viewer: No PDF Viewer oder Built-in PDF Viewer (PDF Viewer Plugin benötigt)
  * Main file to compile: {...}/Ausarbeitungen/{Vorlage}/{Dokument.tex}
  * Directory for auxiliary files: {...}/auxil
  * Directory for output files: {...}/../Dokumente
  * Always compile at least twice: true
  * Output format: PDF
  * LaTeX Distribution: MiKTeX
  * External LaTeX programs: {BibTeX Konfiguration}

  #### Dateien anpassen
  * "Unterschrift.jpg" in /Bilder/ mit der eigenen Unterschrift ersetzen.   
  * Ggf. "PHWT Logo" in /Bilder/ mit dem Logo der jeweiligen Institution ersetzen.
    * Wenn der Name der Datei geändert wird, muss dies auch in der Datei "Befehle.tex" dementsprechend geändert werden.
  

### Neue Ausarbeitung 
* Neue Ausarbeitungen können im Ordner "Ausarbeitungen" erstellt werden. Dazu empfehlt es sich, den Ordner "Vorlage" zu kopieren.
* Der Inhalt der Datei "Parameter.tex" muss auf die jeweilige Ausarbeitung angepasst werden. Es ergibt Sinn, die Datei auch in der Vorlage anzupassen, z.B. den Wert für Matrikelnummer.
* Der Name der Datei "Dokument.tex" sollte auf die jeweilige Ausarbeitung angepasst werden. Dieser Name muss in die Run Configuration eingetragen werden und ist der Name der erstellten PDF-Datei.

### Ausarbeitung kompilieren
* Wenn sich seit des letzten Kompilats Änderungen an der Bibliograpfie ergeben haben, wird die zuletzt erläuterte Konfiguration ausgeführt.
* Wenn sich seit des letzten Kompilats keine Änderungen an der Bibliograpfie ergeben haben, wird die zuerst erläuterte Konfiguration ausgeführt.

* Wenn kein Kompilierfehler auftritt, wird die PDF-Datei in ../Dokumente/ gespeichert.
* Sollte eine neue Section hinzugekommen sein, muss das Dokument zweimal kompiliert werden, damit das Inhaltsverzeichnis die neue Section anzeigt.
