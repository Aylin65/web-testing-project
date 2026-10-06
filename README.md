# Web Testing Project – Chantelle

## Projektübersicht

Dieses Projekt zeigt die Planung, Dokumentation und Automatisierung
von Webtests für einen E-Commerce-Shop.

Ziel des Projekts ist es, anhand eines konkreten Beispiels einen
strukturierten Testprozess von der Anforderungsanalyse bis zur
automatisierten Testausführung zu zeigen.

## Getestete Webseite

Getestet wird der deutsche Online-Shop von Chantelle:

https://chantelle.com/de

Der Fokus liegt auf ausgewählten funktionalen Anforderungen sowie
Accessibility-Anforderungen.

## Testmethodik

Die Tests wurden auf Basis des Software Testing Life Cycle (STLC)
strukturiert.

Der Prozess umfasst:

1. Analyse der Anforderungen
2. Erstellung der Testfälle
3. Planung der Testausführung
4. Automatisierung ausgewählter Testfälle
5. Dokumentation der Ergebnisse

## Testumfang

Unter anderem werden folgende Funktionen betrachtet:

- Benutzer-Login
- Hinzufügen eines Produkts zum Warenkorb
- Erhalt des Warenkorbs nach dem Login
- Entfernen eines Produkts aus dem Warenkorb
- Anzeige der Versandkosten

Zusätzlich werden Accessibility-Anforderungen betrachtet, z. B.:

- Programmatisch erkennbare Formularbeschriftungen
- Alternativtexte für informative Bilder
- Tastaturbedienbarkeit und sichtbarer Fokus

## Verwendete Tools

- Python
- Selenium WebDriver
- Google Chrome
- PyCharm
- Git / GitHub
- WAVE / Lighthouse / Accessibility Checker

## Projektstruktur

```text
web-testing-project/
│
├── STLC/
│   ├── requirements.md
│   ├── test_cases.md
│   └── test_execution.md
│
├── TestAutomation/
│   └── test_execution.py
│
├── README.md
└── .gitignore