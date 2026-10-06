# Testentwurf

## 1. Testentwurfsverfahren

Für die funktionalen Anforderungen werden insbesondere
Anwendungsfalltests und Zustandsübergangstests eingesetzt.

Für die Accessibility-Anforderungen werden automatisierte
Accessibility-Prüfungen mit geeigneten Werkzeugen sowie manuelle
Prüfungen eingesetzt.


# 2. Funktionale Testfälle

## TC-001 – Anmeldung eines bestehenden Benutzers

* **Vorbedingung:** Ein gültiges Testkonto ist vorhanden.
* **Eingabe:** Gültige Zugangsdaten eines bestehenden Benutzers.
* **Erwartetes Ergebnis:** Der Benutzer wird erfolgreich angemeldet.
* **Testentwurf:** Anwendungsfalltest
* **Automatisierung:** Selenium


## TC-002 – Produkt in den Warenkorb legen

* **Vorbedingung:** Eine Produktseite mit einer verfügbaren Größe ist geöffnet.
* **Eingabe:** Auswahl einer Größe und Hinzufügen des Produkts zum Warenkorb.
* **Erwartetes Ergebnis:** Das ausgewählte Produkt wird dem Warenkorb hinzugefügt.
* **Testentwurf:** Anwendungsfalltest
* **Automatisierung:** Selenium


## TC-003 – Warenkorb nach der Anmeldung

* **Vorbedingung:** Ein Produkt befindet sich im Warenkorb und der Benutzer ist nicht angemeldet.
* **Eingabe:** Anmeldung mit einem gültigen Testkonto.
* **Erwartetes Ergebnis:** Das zuvor hinzugefügte Produkt bleibt nach der Anmeldung im Warenkorb erhalten.
* **Testentwurf:** Zustandsübergangstest
* **Automatisierung:** Selenium

### Zustandsübergang

Gast → Produkt im Warenkorb → Anmeldung → angemeldeter Benutzer → Produkt weiterhin im Warenkorb


## TC-004 – Produkt aus dem Warenkorb entfernen

* **Vorbedingung:** Ein Produkt befindet sich im Warenkorb.
* **Eingabe:** Entfernen des Produkts aus dem Warenkorb.
* **Erwartetes Ergebnis:** Das Produkt wird aus dem Warenkorb entfernt.
* **Testentwurf:** Anwendungsfalltest
* **Automatisierung:** Selenium


## TC-005 – Anzeige der Versandkosten

* **Vorbedingung:** Ein Produkt befindet sich im Warenkorb und der Bestellprozess kann aufgerufen werden.
* **Eingabe:** Aufrufen des entsprechenden Bestellschritts.
* **Erwartetes Ergebnis:** Die für die Bestellung geltenden Versandkosten werden korrekt angezeigt.
* **Testentwurf:** Anwendungsfalltest
* **Automatisierung:** Selenium


# 3. Accessibility / WCAG

**Voraussetzung:**  
Die zu prüfende Webseite ist vollständig geladen.

**Testentwurfsverfahren:**  
Automatisierte Accessibility-Prüfung und manuelle Prüfung.


## TC-006 – Formularbeschriftungen

* **Eingabe:** Eine Seite mit Formularfeldern wird geöffnet und mit einem Accessibility-Prüfwerkzeug analysiert.
* **Erwartetes Ergebnis:** Formularfelder besitzen eine programmatisch erkennbare Beschriftung.
* **Testentwurf:** Automatisierte Accessibility-Prüfung
* **Testmittel:** WAVE / Lighthouse / Accessibility Checker


## TC-007 – Alternativtexte bei Produktbildern

* **Eingabe:** Eine Seite mit Produktbildern wird geöffnet und mit einem Accessibility-Prüfwerkzeug analysiert.
* **Erwartetes Ergebnis:** Informative Produktbilder besitzen einen geeigneten Alternativtext, der den Informationszweck des Bildes angemessen beschreibt.
* **Testentwurf:** Automatisierte Accessibility-Prüfung und manuelle Prüfung
* **Testmittel:** WAVE / Lighthouse / Accessibility Checker

> Ein Accessibility-Prüfwerkzeug kann beispielsweise feststellen, ob
> ein `alt`-Attribut fehlt. Die inhaltliche Qualität und Aussagekraft
> eines vorhandenen Alternativtextes muss zusätzlich manuell bewertet
> werden.


## TC-008 – Tastaturbedienbarkeit

* **Eingabe:** Die Webseite wird ausschließlich mit der Tastatur bedient.
* **Erwartetes Ergebnis:** Interaktive Elemente können über die Tastatur erreicht und bedient werden. Der aktuelle Fokus ist erkennbar.
* **Testentwurf:** Manueller Accessibility-Test
* **Testmittel:** Tastatur


# 4. Automatisierung

Die funktionalen Testfälle TC-001 bis TC-005 sollen mit Selenium
automatisiert werden.

Die Accessibility-Testfälle TC-006 und TC-007 werden mit geeigneten
Accessibility-Prüfwerkzeugen unterstützt und teilweise manuell bewertet.

TC-008 wird vollständig manuell durchgeführt, da die vollständige
Bewertung der Tastaturbedienbarkeit nicht zuverlässig durch eine
automatisierte Prüfung ersetzt werden kann.

Damit werden im Projekt sowohl automatisierte als auch manuelle
Testverfahren eingesetzt.