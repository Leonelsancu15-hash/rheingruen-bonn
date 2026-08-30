# Rheingrün — Garten- und Objektpflege Bonn

Website des Betriebs Rheingrün (Johann Beratz, Dennis Frinke-Oedekoven, Leonel Sancu).
Statische Einzelseite ohne Framework und ohne Build-Schritt.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | Die komplette Website — Struktur, Styles und Skript in einer Datei |
| `404.html` | Fehlerseite |
| `robots.txt` | Freigabe für Suchmaschinen |
| `sitemap.xml` | Adresse der Startseite für Suchmaschinen |
| `.nojekyll` | Schaltet die Jekyll-Verarbeitung von GitHub Pages ab |

## Veröffentlichen mit GitHub Pages

1. Repository anlegen, zum Beispiel `rheingruen-bonn`, und diese Dateien hochladen.
2. Im Repository: **Settings → Pages**.
3. Unter *Build and deployment* als Quelle **Deploy from a branch** wählen,
   Branch `main`, Ordner `/ (root)`, speichern.
4. Nach ein bis zwei Minuten ist die Seite erreichbar unter
   `https://<benutzername>.github.io/rheingruen-bonn/`.

## Eigene Domain rheingruen-bonn.com

1. Beim Domain-Anbieter diese DNS-Einträge setzen:

   | Typ | Name | Wert |
   |---|---|---|
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |
   | CNAME | www | `<benutzername>.github.io` |

2. In **Settings → Pages → Custom domain** `rheingruen-bonn.com` eintragen und speichern.
   GitHub legt dabei automatisch eine Datei `CNAME` im Repository an.
3. Sobald DNS aktiv ist (kann einige Stunden dauern): **Enforce HTTPS** aktivieren.

## Inhalte ändern

Alles steht in `index.html`:

- Texte der vier Seiten: im Bereich `<main>`, jeweils in `<section class="page" id="page-...">`
- Farben und Schriften: ganz oben im `<style>`-Block unter `:root`
- Jahreskalender: unten im `<script>`-Block in der Liste `MONATE`
- Telefonnummer: nach `tel:+4915150466784` suchen und ersetzen

## Vor dem Livegang zwingend ergänzen

- [ ] **Impressum** nach § 5 DDG (Pflicht für geschäftliche Websites)
- [ ] **Datenschutzerklärung** nach DSGVO
- [ ] E-Mail-Adresse `info@rheingruen-bonn.com` einrichten
- [ ] Eigene Fotos statt reiner Textdarstellung
