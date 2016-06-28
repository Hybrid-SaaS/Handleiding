<properties>
	<page>
		<title>AccountView</title>
	</page>
	<menu>
		<position>Modules A - M / Facturatie </position> 
		<title>AccountView</title>
		<sort>a</sort>
	</menu>
</properties>

# Mutaties importeren in AccountView vanuit HybridSaas #

Om de mutaties automatisch in te lezen vanuit Hybrird SaaS in AccountView moet op de server aangegeven worden voor welke administratie dit gebeurt. Standaard staat de server ingesteld op het huidige boekjaar van de eerste administratie (als er met meerdere administraties gewerkt word). In AccountView is er de mogelijkheid om te wisselen tussen de verschillende administraties. Hybrid SaaS geeft geen onderscheid in de verschillende administraties op het moment van exporteren.

## Export vanuit Hybrid SaaS ##

In Hybrid SaaS zijn er verschillende soorten export beschikbaar, om de juiste gegevens te kunnen exporteren zijn er ook rechten aan verbonden

![rechten](images/rechten.png)

<div class="warning">
Let op! Er kan per gebruiker rechten worden aangezet maar ook per beveiligingsgroep, dit is te herkennen door:
* Als de knopjes voor het recht **groen of rood** zijn, dan word er per gebruiker iets aangepast
* Als de knopjes voor het recht **wit** zijn, dan word er per beveiligingsgroep iets aangepast, elke medewerker die hieraan gekoppeld is krijgt deze wijziging.
</div>

Er zijn 3 verschillende menukeuzes: **verkoopfacturen**, **inkoopfacturen** en **memoriaalboekingen**.

![bakjes](images/bakjes.png)

<div class="tip">
Het is handig om de verschillende bakjes op het bureaublad te plaatsen, vanuit start met de rechtermuisknop op het bakje dan verschijnt de keuze "Toon op bureaublad", daarnaast is het ook mogelijk om de naam van het bakje te veranderen, door met de rechtermuis knop op het bakje te klikken verschijnt de keuze "Naam wijzigen"</div>

Selecteer de regels die geëxporteerd moeten worden en kies voor Accountview.

- **Verkoopfacturen:**
![verkoop](images/verkoopexport.png)

- **Inkoopfacturen:**
![inkoop](images/inkoopexport.png)

- **Memoriaalboekingen:**
![memoriaal](images/memoriaalexport.png)

Vanuit alle 3 de verschillende bakjes verschijnt het onderstaand venster popt up:

![Hybrid SaaS exports](images/nieuw.png)

Hierin verschijnen de al geexporteerde bestanden en de nieuwe nog te exporteren bestanden, dit is te herkennen door het gele sterretje dit is het bestand wat net geexporteerd is. Selecteer de regel met het sterretje en kies voor *Download bestand*.
 
Bij de volgende melding word er gevraagd of het bestand opgeslagen of geopend moet worden, Kies voor opslaan en sla het bestand op in een map. Er word automatisch een naam aan het bestand gegeven welke oplopend is van nummer, bij wens kan er tijdens het opslaan de bestandsnaam veranderd worden.

![opslaan](images/opslaan.png)

<div class="tip">
Indien het gewenst is kan er een map worden aangemaakt op de computer waar deze bestanden in bewaard kunnen worden. Naast dat ze ook in Hybrid SaaS staan is er nog een extra backup aanwezig.
</div>

## Importeren in AccountView ##

Ga nu naar AccountView en kies bij *Bestand* voor *Administraties*.

![AccountViewbestand](images/avbestand.png)

Zorg dat de juiste administratie geselecteerd is en kies bij *Document* voor *Importeren* en dan voor *XML*

![AccountView import](images/avimport.png)

Om het juiste bestand te kunnen zoeken op de computer kan je het mapje selecteren. Ga naar de map waarin de exports zijn opgelsagen en selecteer het bestand en kies voor *importeren*.

![import selecteren](images/avimportbestand.png)

Na het importeren kun je het venster administratie sluiten en keer je weer terug naar de administratie die open stond.
 
![AccountView sluiten](images/avsluiten.png)
 
 -----
