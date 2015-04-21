<properties>
	<page>
		<title>Automatische incasso limieten instellen</title>
	</page>
	<menu>
		<position>Handleiding / Modules / Bank / Automatische incasso</position> 
		<title>Limieten instellen</title>
	</menu>
</properties>

# Automatische incasso limieten instellen #


Het is mogelijk om een controle te laten plaatsvinden van de waarde van de automatische incasso's.

<div class="tip">
Controleer in de incasso overeenkomst met je bank welke limieten van toepassing zijn.  
</div>


## Limieten instellen ##

Op het <label>entiteit</label>-dialoog kan je de incasso bankrekening instellen: 

![](images/limiet-instellen-entiteit-incasso-bankrekening.jpg)


Als je de eigenschappen van de bankrekening aanpast, kan je de beperkingen instellen.

- Maximaal aantal transacties per batch
	- Het aantal transacties in een batch mag niet hoger zijn dan de ingegeven waarde. 
- Maximaal bedrag per transactie
	- Het bedrag van een factuur mag niet hoger zijn dan de ingegeven waarde.
- Maximaal bedrag per batch
	- Het totaal bedrag van de facturen in een enkele batch mag niet hoger zijn dan de ingegeven waarde.
- Maximaal bedrag per bestand
	- Het totaal bedrag van alle facturen in alle batches mag niet hoger zijn dan de ingegeven waarde.


<div class="info">
Indien de waarde '0' is ingegeven zal instelling worden genegeerd. 
</div>


![](images/limiet-instellen-incasso-bankrekening.jpg)


## Foutmelding tijdens aanmaken automatische incasso download ##
Indien er tijdens het aanmaken van het incassobestand één van de limieten is overschreden zal dit in het resultaatvenster worden weergegeven:

![](images/incasso-aanmaken-foutmelding.jpg)