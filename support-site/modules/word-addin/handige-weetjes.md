<properties>
	<page>
		<title>handige-weetjes</title>
		<description>handige-weetjes</description>
	</page>
	<menu>
		<position>Modules / Word Add-In</position>
		<title>Handige weetjes</title>
		<sort>a</sort>
	</menu>
</properties>

# Handige weetjes #
In deze rubriek laten we aan aantal voorbeelden zien voor het aanpassen van documentsjablonen in Hybrid SaaS. Denk hierbij aan factuursjabloon, ordersjabloon, herinneringen enz. Hybrid SaaS maakt gebruik van Microsoft Word voor de opmaak van documenten. Binnen Word zijn tal van mogelijkheden. Wij zullen een aantal functies uitleggen die makkelijk zijn om zelf sjablonen aan te passen.

# Document bewerken, toevoegen en opslaan #

Zoek "Wordsjablonen"

Selecteer het betreffende sjabloon en klik op bewerken

![Wordsjablonen bewerken](images/wordsjaboon_bewerken.jpg)

Microsoft Word zal worden geopend en het geselecteerde sjabloon zal worden weergegeven. Aan de rechterkant verschijnt een overzicht van alle velden welke ingevoegd kunnen worden. Afhankelijk van het type "tabel" welke is geselecteerd bij het sjabloon worden de mogelijke velden weergegeven.

![Samenvoegvelden binnen Hybrid SaaS](images/Samenvoegvelden toevoegen.jpg)

<div class="info">
In het zoekveld kan worden gezocht op velden welke ingevoegd dienen te worden. Alle benamingen zijn in het Engels. Mocht je een veld niet kunnen vinden neem dan contact met ons op.
</div>
<div class="info">
Er zijn twee verschillende soorten velden:
- Velden welke op zichzelf staan zoals "ADRES", "FACTUURNUMMER", "FACTUURTOTAAL"
- Velden welke herhaald worden zoals "FACTUURREGELS" en "ORDERREGELS". Deze velden vallen onder een zogenaamde herhalingstabel. Dit betekent dat deze velden enkel werken als deze in een tabel staan en dat de tabel een `MERGEFIELD TABLESTART:` en `MERGEFIELD TABLEEND:` bevat.
</div>

Indien het document naar wens ia aangepast dient het document worden geüpload in Hybrid SaaS.

Klik hiervoor in het Word document op "Save & Store Template" 

![Sjabloon opslaan in Hybrid SaaS](images/save_and_store_template.jpg)



## Basis weetjes weetjes ##


ALT+F9 | Hiermee kunnen onzichtbare onderdelen zichtbaar worden gemaakt. Bijvoorbeeld `«INVOICE_NUMBER»` wordt zichtbaar als `{ MERGEFIELD INVOICE_NUMBER \* MERGEFORMAT }`



## Angelsaksische en Engelse notatie ##

Getalnotaties voor bijvoorbeeld valuta kunnen op diverse manieren worden weergegeven. Hierin wordt onderscheid gemaakt tussen het het karakter voor het scheiden van duizendtallen en het karakter om decimalen weer te geven. In Nederland maken wij gebruik van de Angelsaksische notatie waarbij duizendtallen worden gescheiden dmv een "." (punt) en decimalen dmv een "," (komma). In de Engelse notatie worden deze karakters andersom gebruikt.

Bij de uitvoer van documenten met verschillende talen is het belangrijk dat de documenten goed worden ingesteld. 

# Voorkeursnotatie  #

Ga naar de betreffende MERGEFIELD

Plaats de volgende notatie `\# "§0¤00"` vóór `\*` in het MERGEFIELD

§ = MERGEFIELDS: CURRENCY GROUP SEPARATOR
¤ = MERGEFIELDS: CURRENCY DECIMAL SEPARATOR

Voorbeeld zonder voorkeursnotatie € 12345,67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \* MERGEFORMAT}` 

Voorbeeld met voorkeursnotatie (Angelsaksisch) € 12.345,67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \# "§0¤00" \* MERGEFORMAT}`


# Engelse getalnotatiegebruik ( 00,000.00) #

*Als het een Engels document bevat (wat is aangegeven bij de localisatie in het Word document) dien je het volgende toe te voegen*

Voorbeeld zonder € 12345,67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \* MERGEFORMAT}` 

Voorbeeld met € 12.345,67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \# ,0.00 MERGEFORMAT}`

# Met Franse bedragen(€ 00000,00)  #

*Als het een Frans document bevat (wat is aangegeven bij de localisatie in het Word document) dien je het volgende toe te voegen*

Voorbeeld zonder € 12345,67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \* MERGEFORMAT}` 

Voorbeeld met € 12345,67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \# 0.00 MERGEFORMAT}`

----------

# Een maat aan de afbeelding geven #

Door middel van een size toe te voegen aan de MERGEFIELD veld kan je een afbeelding op de order ander document groter of kleiner maken

*Bij orders:*

Voorbeeld zonder: `{MERGEFIELD IMAGES:QUESTION_ATTACHMENT_IMAGES \* MERGEFORMAT}`

Voorbeeld met: `{MERGEFIELD IMAGES:QUESTION_ATTACHMENT_IMAGES / size=100 \* MERGEFORMAT}`

*Bij facturen:*

Voorbeeld zonder: `{MERGEFIELD IMAGE:ORDER_LINE_1_IMAGE \* MERGEFORMAT}`

Voorbeeld met: `{MERGEFIELD IMAGE:ORDER_LINE_1_IMAGE / size=100 \* MERGEFORMAT}`

*Bij vragenlijsten:*

Voorbeeld zonder: `{MERGEFIELD IMAGE:INVOICE_LINE_IMAGE \* MERGEFORMAT}`

Voorbeeld met: `{MERGEFIELD IMAGE:INVOICE_LINE_IMAGE / size=100 \* MERGEFORMAT}`

----------

# Een tabel opnieuw laten beginnen om een pagina #

Het komt wel eens voor dat je meerdere orderregels of diverse in een tabel heb, als de tabel dan onder aan de pagina uitvalt wil hij hem wel eens opsplitsen in 2e naar de volgende pagina.

![](images/3.jpg)

Dit kan je ook uitzetten dat het een nieuwe tabel word op een volgende pagina.
(via rechtermuisknop op het kruisje van de tabel)

Het vinkje staat over het algemeen aan. Als je deze uitzet word er een nieuwe tabel weergegeven op een volgende pagina. 

![](images/1.jpg)

Uitslag:

![](images/2.jpg)

----------