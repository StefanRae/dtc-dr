# Zuyd DI-lab - Digital Twin Configurator

Project in naam van - https://dataintelligence.zuyd.nl/

## Digital Twin configurator

### Functies:

* 'Send' en 'Receive' componenten
* 'Send' componentmenu voor API's toewijzen
* Associaties leggen tussen componenten
* Drag and Drop raster interface
* Data analyse via Flask

### Dependencies:

* Godot versie 4.1.3 [https://godotengine.org/]
* Flask [https://github.com/pallets/flask]

### Bekende problemen:
* Momenteel enkel ondersteuning voor API's die een list bieden.

### Installatie & eerste gebruik:

1. Installeer Flask en maak een environment. Verplaats het `app.py` bestand in deze environment
2. Installeer Godot 4.1.3 en importeer vervolgend `project.godot` vanuit de map `digital-twin-configurator-files` in de project manager.
3. Voer de Flask server uit door in de *virtual environment* directory app.py uit te voeren (`python3 app.py`)
4. Vervang 0.0.0.0 met een van de 'running on' adressen, zichtbaar in de Flask server console, in bij de `_flaskRequest` onder `ReceiveComponent.gd`


### Gebruik:

*! Voorlopig worden slechts API's ondersteund die een lijst met nummers leveren.*

- In het raster kan een ***SendComponent*** worden toegevoegd. Deze node **verwerkt** de ruwe informatie een API 
- In het raster kan een ***ReceiveComponent*** worden toegevoegd. Deze node voert **bewerkingen** uit op de Flask server.
- Deze twee ***Componenten*** kunnen gekoppeld worden aan elkaar met ***associaties***. Met associaties wordt ruwe informatie uit een SendComponent gekoppeld aan een ReceiveComponent zodat deze gereed wordt voor verwerkingen. Associaties worden gemaakt door een lijn te trekken tussen twee 'slots' van Componenten.
- In het ***ComponentMenu***, wanneer op de **'Configure'** knop wordt gedrukt op een SendComponent, kunnen APIs toegewezen worden.
- Componenten op het raster kunnen visueel *verplaatst*, *vergroot* of *verwijderd* worden via een drag and drop interface.
- Het raster kan *ingezoomd* en *genavigeerd* worden op verticale en horizontale as. 
