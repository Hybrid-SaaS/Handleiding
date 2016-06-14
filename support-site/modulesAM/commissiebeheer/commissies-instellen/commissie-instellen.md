<properties>
	<page>
		<title>Commissie instellen</title>
		<description>Commissie toepassen</description>
	</page>
	<menu>
		<position>Modules A - M /Commissiebeheer</position>
		<title>Commissie toepassen</title>
		<sort>B</sort>
	</menu>
</properties>

# Commsissies instellen #

Deze rubriek zal meer duidelijkheid te geven over het beheren van commissies met commissiebeheer van Hybrid SaaS. Synoniemen voor commissies zijn onder ander provisies, courtage en procura. In deze beschrijving zal veelal “commissies” worden gebruikt.

Om geen misverstanden te krijgen worden eerst enkele definities benoemd:

**Revenu share** (variabele prijs) : Commissie op basis van een percentage van gerealiseerde omzet (facturen) Voorbeeld:
Product A	€100,-- (per maand)
Percentage	15%
100 * 15% = €15,--

**Lumpsum** (vastgestelde prijs): Commissies op basis van een percentage van orders. De som van alles orders maakt de contractwaarde. Lumpsum is het resultaat van de orderregeltotaal * looptijd * commissies percentage. Voorbeeld: 
Product A	€100,-- (per maand)
Looptijd 	24 maanden
Percentage	15%
100 * 24 * 15% = €360,--

## Commissiesets aanmaken ##
In een commissieset wordt een verzameling met afspraken vastgelegd voor de berekening van commissies op facturen en orders. In de set wordt het percentage en de onderdelen waarop deze van toepassing zijn vastgelegd. Tevens kunnen hier targets worden vastgelegd waar de set betrekking op heeft. 

Zoek vanuit het startmenu naar **Commissie set** > **Toevoegen**

![Commissie set toevoegen](images/commissie_set_toevoegen.jpg)

### Basisgegevens commissies invullen ###

Selecteer de juiste grootboekrekening (GL-code)

Geef een duidelijke omschrijving 

Kies het gedrag waarop het percentage dient plaats te vinden 
-	Revshare (Factuur)
-	Lumpsum (Order)

Vul het commissiepercentage in 

![Commissie set gegevens invullen](images/commissie_set_gegevens_invullen.jpg)

<div class="info">
Info: Korting verdelen. Indien er korting wordt gegeven aan de klant is het mogelijk deze korting te verdelen met de partner. Bij het invullen van een percentage zal een voorbeeld worden weergegeven.
</div>


<div class="info">
Target. Bij Target kan het target percentage worden vastgelegd. Voorbeeld:
Target 1000 stuks
Min 35% max 80%
Vanaf 350 stuks – t/m 800 stuks
</div>

### Commissieregels toevoegen aan commissieafspraken ###

Klik op **Toevoegen** om commissieregels toe te voegen aan de set

![Commissieregels toevoegen aan set](images/commissieregels_toevoegen_aan_set.jpg)

## Commissieregels beheren ##

Wanneer de commissieregel wordt toegevoegd verschijnt het volgende scherm

![Commissieregels beheren](images/commissieregels_beheren.jpg)

Selecteer de onderdelen waarop het commissiepercentage toegepast dient te worden. 

<div class="info">
Het is veelal niet mogelijk om meerdere onderdelen te selecteren in één afspraak. Indien een tweede onderdeel wordt gekozen zal de eerste selectie komen te vervallen.
</div>

<div class="info">
Veelal zal de commissie van toepassing zijn op een product, productsubgroep of productgroep.
</div>

<div class="info">
Selecteer een bedrijf indien een speciale afspraak van toepassing bij een specifieke klant.
</div>

### Afwijkende voorwaarden instellen op regelniveau ###

Het is mogelijk om afwijkende voorwaarden te laten prevaleren boven de voorwaarden welke in de set zijn vastgelegd.

![Afwijkende voorwaarden vastleggen](images/afwijkende_voorwaarden_vastleggen.jpg) 

## Set koppelen aan de partner ##

Nadat set is aangemaakt dient deze aan de juiste partner(s) gekoppeld te worden.

Zoek vanuit het startmenu naar **Leveranciers**

Open de relatiekaart van de betreffende partner door dubbel op de naam te klikken

Ga naar het tabblad **Commissies**

Klik op **Toevoegen** om een set te selecteren

![Commissie sets koppelen aan partner(s)](images/Commissie_sets_koppelen.jpg) 

Selecteer de betreffende accountmanager 

<div class="info">
Indien deze nog niet is aangemaakt raadpleeg de volgende handleiding http://hybridsaas.support/pages/support-site/het-systeem/gebruikers-toevoegen-SSO-API/toevoegen 
</div>

Selecteer de commissie set

Selecteer de startdatum en einddatum van de commissieovereenkomst

![Contractafspraken vastleggen](images/contractafspraken_vastleggen.jpg) 

<div class="info">
Wachten op betaling: Indien deze optie is gekozen zal de commissie pas worden uitgekeerd indien de factuur van de klant is voldaan.
</div>

<div class="info">
Gearchiveerd: Indien deze optie is gekozen zal de commissieafspraak op inactief worden gezet, waarbij de gekoppelde data zal worden bewaard.
</div>
