<properties>
	<page>
		<title>Partner aanmaken</title>
		<description>Partner aanmaken</description>
	</page>
	<menu>
		<position>Modules A - M /Commissiebeheer</position>
		<title>Partner aanmaken</title>
		<sort>A</sort>
	</menu>
</properties>

# Partner aanmaken #

Deze rubriek zal meer duidelijkheid te geven over het aanmaken van nieuwe partners en de instellen welke gedaan dienen te worden om de commissies op de juist manier toe te bedelen.

Er zijn een aantal verschillende instellingen welke doorlopen dienen te worden. Grofweg bestaan deze uit:
- Partner aanmaken als relatie
- Partner aanmaken als gebruiker

## Partner aanmaken als relatie ##

Zoek via het startmenu naar **Leverancier**

Klik op **Toevoegen**

![Partner aanmaken als relatie](images/partner_toevoegen_als_relatie.jpg)

### NAW gegevens partner invullen ###


Vul de benodigde NAW (naam, adres, woonplaats) gegevens in:
- Naam partner
- Vul adresgegevens in
- Controleer of het vinkje bij "leverancier" staat aangevinkt

![Partner aanmaken als relatie](images/partner_toevoegen_als_relatie.jpg)

<div class="info">
Vul bij code het partnernummer in waaronder deze partner bekend staat. Eventuele andere systemen (SSO) zullen deze code gebruiken.
</div>

<div class="warning">
Zorg ervoor dat het vinkje bij leverancier stat aangevinkt. Indien dit niet het geval is, kan het mogelijk zijn dat de partner niet correct wordt weergegeven.
</div>

### Stamgegevens partner invullen ###

Ga naar het tabblad Stamgevens

Sekecteer de juiste BTW code waar de commissieafdracht op dient plaats te vinden

## Partner aanmaken als gebruiker ##
In een commissie set wordt een verzameling met afspraken vastgelegd voor de berekening van commissies op facturen en orders. In de set wordt het percentage en de onderdelen waarop deze van toepassing zijn vastgelegd. Tevens kunnen hier targets (aantal verkochte units) worden vastgelegd waar de set betrekking op heeft. 

Zoek vanuit het startmenu naar **Commissie set** 
Kies vervolgens **Toevoegen**

![Commissie set toevoegen](images/commissie_set_toevoegen.jpg)

### Basisgegevens commissies invullen ###

Selecteer de juiste **Grootboekrekening** (GL-code)

Geef **Omschrijving** in

Kies het **Gedrag** waarop het percentage toegepast dient te worden:
-	Revshare (Factuur)
-	Lumpsum (Order)

Vul het commissiepercentage in 

![Commissie set gegevens invullen](images/commissie_set_gegevens_invullen.jpg)

<div class="tip">
Korting verdelen: Indien er korting wordt gegeven aan de klant is het mogelijk deze korting te delen met de partner. Bij het invullen van een percentage zal een voorbeeldberekening worden weergegeven.
</div>


<div class="info">
Target. Bij Target kan het target percentage worden vastgelegd. 
Voorbeeld:

- Target 1000 stuks

- Min 35% max 80%

- Resultaat: vanaf 350 stuks t/m 800 stuks
</div>

### Commissieregels toevoegen in commissieset ###

Klik op **Toevoegen** om commissieregels toe te voegen aan de set.

![Commissieregels toevoegen aan set](images/commissieregels_toevoegen_aan_set.jpg)


Selecteer de onderdelen waarop het commissiepercentage toegepast dient te worden. 

![Commissieregels beheren](images/commissieregels_beheren.jpg)

<div class="info">
Het is veelal niet mogelijk om meerdere onderdelen te selecteren in één afspraak. Indien een tweede onderdeel wordt gekozen zal de eerste selectie komen te vervallen.
</div>

<div class="info">
Veelal zal de commissie van toepassing zijn op een product, productsubgroep of productgroep.
</div>

<div class="tip">
Selecteer een klant bij "bedrijf selecteren" indien een speciale afspraak van toepassing is bij een specifieke klant.
</div>

### Afwijkende voorwaarden instellen op regelniveau ###

Het is mogelijk om afwijkende voorwaarden te laten prevaleren boven de voorwaarden welke in de set zijn vastgelegd. De afwijkende voorwaarden zullen worden gebruikt bij de berekening van de commissie.

![Afwijkende voorwaarden vastleggen](images/afwijkende_voorwaarden_vastleggen.jpg) 

## Set koppelen aan de partner ##

Nadat set is aangemaakt dient deze aan de juiste partner(s) gekoppeld te worden. Bij iedere order en factuur welke wordt aangemaakt bij een relatie waarvan de partner accountmanagers is, zal de commissie op basis van de gekozen set worden uitgerekend.

### Set toevoegen ###

Zoek vanuit het startmenu naar **Leveranciers**

Open de relatiekaart van de betreffende partner

Ga naar het tabblad **Commissies**

Klik op **Toevoegen** om een commissie set te selecteren

![Commissie sets koppelen aan partner(s)](images/commissie_sets_koppelen.jpg) 

### Set definiëren ###

Selecteer de betreffende accountmanager (naam van de partner) 

<div class="tip">
Indien deze nog niet is aangemaakt raadpleeg de volgende handleiding http://hybridsaas.support/pages/support-site/het-systeem/gebruikers-toevoegen-SSO-API/toevoegen  
</div>

Selecteer de **Commissie set**

Selecteer de **Startdatum** en **Einddatum** welke is terug te vinden in de partnerovereenkomst

![Contractafspraken vastleggen](images/contractafspraken_vastleggen.jpg) 

<div class="tip">
Wachten op betaling: Indien deze optie is geselecteerd zal de commissie worden uitgekeerd wanneer de factuur door de klant is voldaan.
</div>

<div class="info">
Gearchiveerd: Indien deze optie is geselecteerd zal de commissieafspraak op inactief worden gezet. De gekoppelde data zal worden bewaard.
</div>

### Partner koppelen aan organisatie ###

De partner dient enkel commissie te ontvangen van organisaties welke onder zijn/haar account vallen. Door de partner als accountmanager aan een organisatie te koppelen zal de commissie over de facturen, gericht aan deze organisatie, worden toebedeeld aan de partner.

Ga naar de relatiekaart van de betreffende organisatie

Ga naar het tabblad **Stamgegevens**

Klik op **Toevoegen** en selecteer de partner

Klik vervolgens op de optie **Commissie** zodat er een vinkje bij commissie komt te staan

![Accountmanager - Partner vastleggen bij organisatie ](images/partner_koppelen_aan_organisatie.jpg) 

<div class="warning">
Het vinkje bij commissie dient aan te staan om de commissie aan de juiste partner toe te bedelen.
</div>

<div class="info">
Indien er meerdere accountmanagers zijn is het mogelijk om 1 accountmanager als primair aan te wijzen. Klik hiervoor op de optie "Primair"
</div>

## Lumpsum instellingen op orders ##

Door middel van lumpsum kunnen commissies worden uitgerekend op basis van: Aantal * Prijs * Looptijd * Percentage.

Bij het aanmaken van een nieuwe order kunnen looptijden worden ingevuld. Door middel van de begin- en einddatum kan worden bepaald wat de looptijd is voor de berekening van de commissies.

Maak een nieuwe order aan

Vul de begin en einddatum in

![Contractafspraken vastleggen op order](images/contractinstellingen_op_order.jpg) 


<div class="tip">
Indien een bestaand contract wordt gekoppeld zullen de looptijden uit het contract worden overgenomen.
</div>

<div class="tip">
Nog geen contract? Bij het selecteren van een contract is het ook mogelijk om direct een nieuwe aan te maken. Vul alvast de looptijden in zodat deze worden overgenomen op de order.
</div>

<div class="info">
Indien gewenst is het mogelijk om de de factor aan te passen. De factor is het aantal keer dat het item wordt uit gefactureerd gedurende de looptijd van het contract. Dit aantal wordt overigens niet gebruikt in het contract zelf.
</div>

<div class="warning">
Let op dat bij het importeren de begindatum correct staat ingevuld. Deze begin datum zal worden gebruikt bij het aanmaken van de factuurregels.
</div>

<div class="tip">
De order kan worden geïmporteerd in een nieuw of bestaand contract. Zie voor meer informatie deze handleiding. http://hybridsaas.support/pages/support-site/modulesAM/contractenbeheer/handige-weetjes/handige-weetjes 
</div>

-------