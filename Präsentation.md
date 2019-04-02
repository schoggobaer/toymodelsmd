## HTML und Syntax
- (kleiner Gag) „Der erste Prototyp der Seite wurde nach den Designkriterien einer *Motherfucking Website* erstellt“ (http://motherfuckingwebsite.com/)

- Besonderes Augenmerk auf semantische Korrektheit – Großteil der Aufgabe bestand aus dem Lesen der offiziellen WHATWG-HTML-Spezifikation und dem Suchen nach passenden Elementen. Darunter zum Beispiel:
  - `<header` mit `<h1>Toy Models Shop</h1>`-Link, der von jeder Unterseite zurück auf die Hauptseite führt
  - `<menu>` auf der Hauptseite als Container für den Warenkorb, da wir weitere Menüelemente erwarten
  - `<main>` beinhaltet den vom Nutzer erwarteten Hauptinhalt jeder Seite
  - `<footer>` mit Link zu Impressum, ebenfalls von jeder Seite erreichbar; ist nämlich auch gesetzlich vorgeschrieben 😉 (§5, Absatz 1 Telemediengesetz, „leicht erkennbar, unmittelbar erreichbar, und ständig verfügbar“)

- Überschriften für besseren Überblick in diesem ersten Prototypen; später würde diese Aufgabe von ansprechendem Webdesign übernommen werden
- `<option>`-values auf Englisch, da wir vielleicht internationalisieren möchten
- Eingabefelder mit `required`-Attribut (Hier Screenshot davon einfügen, was passiert, wenn man versucht, das Formular ohne Texteingabe abzusenden)
- Suchfeld mit `autofocus`, da „die Tests mit unserer Fokusgruppe ergeben haben, dass 90% der Nutzer direkt nach dem Laden der Seite das Suchfeld fokussieren“
- GET-Methode in allen Forms für diesen ersten Prototyp, demonstriert korrekte Funktion direkt in der Adresszeile des Browsers.

### Probleme
Viel Duplizierung von gleichen Markup-Blöcken in mehreren HTML-Dateien.

Abhilfe durch Technologien wie SSI… oder der in den nächsten Prototypen zu erwartenden dynamischen Seitengenerierung mittels einer vollwertigen Programmiersprache.

## Webserver
- Port ändern :
```Listen 1338```
- Ordner bereitstellen für den Webserver
```
Alias "/toymodels" "C:\Users\Schoggoladentieger\Source\GitHub\toymodels\htdocs" 
<Directory "C:\Users\Schoggoladentieger\Source\GitHub\toymodels">

	Options Indexes
	#
    # AllowOverride controls what directives may be placed in .htaccess files.
    # It can be "All", "None", or any combination of the keywords:
    #   AllowOverride FileInfo AuthConfig Limit
    #
	AllowOverride All
	#
    # Controls who can get stuff from this server.
    #
	Require all granted
</Directory>```

