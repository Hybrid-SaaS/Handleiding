<properties>
	<page>
		<title>Werkcodes importeren</title>
		<description>Werkcodes importeren</description>
	</page>
	<menu>
		<position>Modules A - M / Balans</position> 
		<title>Werkcodes importeren</title>
		<sort>e</sort>
	</menu>
</properties>

## Werkcodes Importeren  ##

<description>Om op een eenvoudige manier werkcodes in de database te krijgen is er een import module aanwezig. Hiermee kan je eenvoudig nieuwe werkcodes toevoegen of bestaande werkcodes aanpassen. Dit doe je niet als je voor één werkcodes iets wilt aanpassen maar vaak als je een massa mutatie gaat uitvoeren, waarbij je bijvoorbeeld bij iedere werkcodes iets wilt toevoegen en/of wijzigen.
</description>

**Om bestaande werkcodes te veranderen heb je de juiste werkcode nodig. deze zal dan overschreden worden met de nieuwe informatie**

Zoek in start naar Importeren

Om te importeren klik je eerst op 
*Werkcodes importeren - Voorbeeldsheet*

Je krijgt een hele lijst met kolommen, Zie voor uitleg kolommen hieronder

(rechtermuisknop op de kolom en dan verwijderen)

Vul vervolgens alle kolommen in die nodig zijn. als je er niks aan hoef te veranderen kan je de waarde laten staan of geheel leeg maken (geen 0 van maken dan zal het overschreden worden)

Nu kan je het exportbestand opslaan op je bureaublad en afsluiten.

**Importeren**

Gebruik nu de knop "Klik hier om Werkcodes te importeren" om de Werkcodes te importeren. 
Zoek het juiste bestand op en selecteer deze.
Na de import verschijnt er een internet pagina met daarin het resultaat van de import.

<div class="info"> Je moet het Excel bestandje sluiten voordat je hem gaat importeren anders zal die een fout melding aangeven </div>

Je kan nu in Hybrid SaaS bij de Werkcodes de geïmporteerde gegevens terugvinden.

----------

## De kolommen ##

De veldnaam is **dik** gedrukt

![](images/1.png)

- Entity
	- **Entiteit**
- Type
	- **Verdichting** (Hoofdgroep)
		- Als de verdichting nog niet bestaat dan zal die aangemaakt worden
- Group Code
	- **Verdichting** (Hoofdgroep code)
		- Als de verdichting nog niet bestaat dan zal die aangemaakt worden
- Group description
	- **Verdichting** (Beschrijving)
		- Als de verdichting nog niet bestaat dan zal die aangemaakt worden
- General Ledger
	- **Grootboekrekening**
- Description
	- **Beschrijving** 
- Sale
	- **Verkoop/tijdregistratie**
		- Aan te geven met de volgende waarde:
			- 0 Vinkje aan
			- 1 Vinkje uit
				- Deze kan alleen maar aanstaan als de andere vinkjes uit staan

![](images/2.png)

- Purchase
	- **Inkoop**
		- Aan te geven met de volgende waarde:
			- 0 Vinkje aan
			- 1 Vinkje uit
				- Deze kan samen aanstaan met "Bank"
- Bank
	- **Bank transacties**
		- Aan te geven met de volgende waarde:
			- 0 Vinkje aan
			- 1 Vinkje uit
				- Deze kan samen aanstaan met "Inkoop"
- Memorial
	- **Memoriaal**
		- Aan te geven met de volgende waarde:
			- 0 Vinkje aan
			- 1 Vinkje uit
				- Deze kan alleen maar aanstaan als de andere vinkjes uit staan
- Debet
	- **Grootboek type**
		- Aan te geven met de volgende waarde:
			- 0 Credit
			- 1 Debet
- Vat
	- **BTW percentage**
		- deze moet gelijk zijn aan de waarde welke al bekend is in het systeem

----------