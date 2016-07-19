<properties>
	<page>
		<title>Importeren</title>
		<description>Importeren</description>
	</page>
	<menu>
		<position>Modules A - M / Inkoopbeheer / Importeren</position>
		<title>via Externe Applicatie </title>
		<sort>D</sort>
	</menu>
</properties>

# Inkoop facturen Importeren  #

Doormiddel van een externe applicatie kunnen er inkoopfacturen worden ingelezen in Hybrid SaaS van een bepaalde leverancier

### Installatie Applicatie  ###

Na het opstarten van de applicatie moet je deze nog koppelen aan jouw Hybrid SaaS account:

•	Kies voor de menuoptie **instellingen**

![instellingen van applicatie](images/instellingen.jpg)

•	Kies voor de optie toevoegen

![toevoegen](images/toevoegen.jpg)

•	Vul het volgende scherm in:

![inloggegevens van de gebruiker](images/inloggegevens.png)

- Het wachtwoord is gelijk aan het Hybrid SaaS wachtwoord

- De ‘Application name’  komt uit het tabblad Externe applicaties

![gebruiker met de instellingen](images/externe-applicaties.png)

- Indien er iets niet klopt geeft de applicatie een melding

![medling indien fout](images/melding.jpg)

In het hoofdscherm is er zichtbaar welke omgeving actief is.

![instellingen van applicatie](images/instellingen.png)
 
 ### De gebruiker  ###

Deze omgeving is gekoppeld aan een gebruiker (met wachtwoord) en een externe applicatie. 

![gebruiker met de instellingen](images/externe-applicaties.png)

### Gekoppeld aan de omgeving  ###

De omgeving is gekoppeld met de gegevens van de gebruiker

![gegevens van de omgeving](images/omgevingen.png)

### Gegevens ophalen ###

De bestanden kunnen worden opgehaald van de computer 

![bestanden ophalen van computer](images/ophalen-inkoop.png)

Na het kiezen voor verwerken zullen de facturen worden geïmporteerd

Tijdens het laden kan je de voortang zien recht onderin

![](images/verwerken-inkoop.png)

### De inkoopfactuur  ###

Na verwerken zijn de facturen aangemaakt 

<div class="info"> 
Hier word een voorbeeld van een artikel getoond</div>

![import bestand inkoopfactuur](images/import-inkoop.jpg)

De inkoopfactuur is nu toegevoegd in Hybrid SaaS met de volgende eigenschappen:

![inkoopfactuur](images/inkoopfactuur.png)

Indien er een verschil in berekening van de btw op zit, zal deze automatisch worden gecorrigeerd.

![inkoopfactuur regel](images/inkoopfactuurregel.png)

De inkoopfacturen worden gekoppeld aan de standaard entiteit en standaard inkoop werkcode, daarnaast zoekt het systeem op de letterlijke naam van de leverancier die in de import staat, indien er ook producten zijn gevonden worden deze automatisch gelinked

De volgorde van opzoeken van de inkoop grootboek is als volgt:

-	Product -> Subgroep, (indien niet gevonden ->)
-	Product -> Hoofdgroep , (indien niet gevonden ->)
-	Entiteit standaard

### De periode  ###

•	De periode is nu goed gekoppeld bij aanmaken

![periode](images/periode.jpg)

•	Indien de periode geblokkeerd is, is dit in de melding terug te zien

![periode fout](images/fout-periode.jpg)

•	Periodes worden ook automatisch aangemaakt indien deze niet bestaan:

![periode aanmaken](images/periode-aanmaken.jpg)

### De foutmelding  ###

•	Indien er geen prognoseposten zijn gekoppeld krijg je een waarschuwing:

![prognose niet gevonden](images/prognose-fout.jpg)

Door te dubbelklikken op de regel komt de meldingen in beeld:

![prognose niet gevonden melding](images/prognose-melding.jpg)

•	Indien er fouten optreden tijdens het verwerken is dat terug te zien

![foutmelding in import](images/foutmelding.png)

Door te dubbelklikken op de regel komt de meldingen in beeld:

![foutmelding in import](images/foutmelding-detail.png)

----------



