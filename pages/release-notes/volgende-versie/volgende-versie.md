<properties>
	<page>
		<title>Release notes volgende versie</title>
	</page>
	<menu>
		<position>Release notes </position>
		<title>Volgende versie</title>
	</menu>
</properties>

# Release notes volgende versie #

In de release notes staan de wijzigingen voor de volgende productieversie van Hybrid SaaS.

<div class="info">
De beschreven aanpassingen zijn nog niet algemeen beschikbaar. De volgende release van Hybrid SaaS zal deze functionaliteiten bevatten.
</div>
 
---------------------------------------------------------------------------------------------------------	
<div class="tag-fix"></div>
**Verbetering werking geëxporteerde inkoopfacturen**

Op inkoopfacturen werden betalings en financiële exports niet altijd weergegeven.

![](images/inkoop-factuur-export-info.jpg)

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
Indien het deblokkeren van een inkoopfactuur niet mogelijk is omdat er een financiële export aanwezig is, verschijnt er nu een verbeterde melding die direct verwijst naar het nummer van de export.

![](images/inkoop-factuur-melding-deblokkeren.jpg)

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**Verbetering werking geëxporteerde verkoopfacturen**

Indien het deblokkeren van een verkoopfactuur niet mogelijk is omdat er een financiële export aanwezig is, verschijnt er nu een verbeterde melding die direct verwijst naar het nummer van de export.

![](images/verkoop-factuur-melding-deblokkeren.jpg)

---------------------------------------------------------------------------------------------------------
<div class="tag-new"></div>
**Individuele financiële export records ongedaan maken**

Het is mogelijk om losse transacties van een financiële export ongedaan te maken. Hiervoor is een nieuwe menu knop toegevoegd genaamd **Ongedaan maken** 

![](images/financiele-export-ongedaan-maken.jpg)

Na het aanklikken van deze knop en bevestigen van de onderstaande vraag zal de export ongedaan worden gemaakt en kan daarmee opnieuw worden aangeboden. Tevens kan na het ongedaan maken van de financiële export record de gekoppelde inkoop/verkoopfactuur worden gedeblokkeerd.

![](images/financiele-export-ongedaan-maken-vraag.jpg)

Na het ongedaan maken is dit ook zichtbaar in de het overzicht met gekoppelde records van de export in de kolom *Ongedaan gemaakt*

![](images/financiele-export-ongedaan-gemaakt.jpg)

Tevens is de actie gelogd bij de gekoppelde factuur

![](images/financiele-export-ongedaan-gemaakt-log.jpg)

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**BTW**

Wijzigen van de standaard btw code vraagt of je de btw code van de adviesverkoopprijzen in producten wilt aanpassen, bij importeren van nieuwe producten uit excel zet het systeem nu ook standaard de btw code voor de adviesverkoopprijzen

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**BANK**

![](images/.jpg)
Indien er imports zijn zonder transacties (zoals rabobank ze aanlevert) zal deze als 'correct' worden weergegeven in de controle

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**CONTRACTEN**

Bij de keuze om een contractwaarde per 3 maanden (kwartaal) vast te leggen werd er in de planning een met afrondingen gewerkt. Hierdoor kwam er een verkeerde waarde op de factuur. Dit is aangepast. Het juiste bedrag wordt nu berekend en getoond op de factuur
![](images/contract-3-maanden.jpg)


---------------------------------------------------------------------------------------------------------
<div class="tag-new"></div>
**TIJDREGISTRATIE**


Overboekknop op meerdere plekken beschikbaar. Binnen de module tijdregistratie is de knop om een tijdregistratie over te boeken op meerder plaatsen toegevoegd. Zo is hij nu beschikbaar bij:

- Alle tijdregistraties
- Alle goed te keuren tijdregistraties
- Controle voor goedkeuring
- Alle afgekeurde tijdregistraties
- Goed te keuren tijdregistraties van mijn projecten


![](images/tijdregistratie-overboeken.jpg)

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**Bank**

Verwijderde incasso exports zijn niet meer zichtbaar (INKOOP)FACTUUR - Het deblokkeren houdt rekening met verwijderde en ongedane financiële exports

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**PROGNOSE**

 Directe koppeling op tijdregistratie gezet, zo kun je ook tijd overboeken tussen prognose onderdelen

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**TIJDREGISTATIES**

 Weergegeven uurtarieven worden bijgewerkt indien de factuur is aangepast of afgekeurd, via excel export zie je het originele tarief nog wel.

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**BANK**

 Mogelijkheid tot het ongedaan maken van individuele financiële export records + logging INKOOP/VERKOOPFACTUUR - Deblokkeren geeft betere melding door blokkade financieel export INKOOPFACTUUR - Weergave van gekoppelde financiële exports in tabblad interne opmerking

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**TIJDREGISTRATIE**

Koppeling met prognose / PROGNOSE nieuwe methode / TICKET doorbelasten (beta) / FACTUREN aantal gescande bijlagen zichtbaar

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**TICKET**

Gerelateerde tickets gaan niet meer automatisch mee met de status wijziging
![](images/tickets-gerelateerd-status.jpg)

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**Adressen**

Je kunt aangeven welk adres in de storelocator wordt weergegeven

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**Storelocator**

De storelocator accepteerd nu ook EN /system/storelocator/?language=EN

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**TICKETS**

Opslaan van tickets is efficiënter geworden (x aantal loopings zaten er in), tevens bij actie toewijzen controleert het dialoog eerst of het onderwerp / categorie is ingegeven

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**GEBRUIKERS**

Je kunt aangeven per gebruiker of deze alle gebruikers kan selecteren bij een gebruikers selectie keuze, zo niet dan kun je dit per afdeling instellen

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**TICKETS**

Door facturen van tickets tegen een vaste prijs (naar meerdere opdrachtgevers)

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**INKOOPFACTUUR**

Bij wijzigen datum komt meteen de juiste boekperiode in de factuur

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**TICKET**

Door belasting kosten haalt laatste werkcode op en neemt de opdrachtgever over uit het ticket

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**MANDAGENSTAAT**

Na het verwijderen van een mandagenstaat komen de registraties nu weer terug als te verwerken. voorheen moest je alle registraties opnieuw goedkeuren

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**MANDAGENSTAAT**

Je kunt bij de werkcode aangeven of de registraties NIET op een mandagenstaat komen te staan, dit is handig voor interne uren. bij verwerken wordt het vinkje geen mandagenstaat aangezet op de tijdregistratie

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**CORRESPONDENTIE**

Koppeling vanuit kenmerk om de gekoppelde stukken in te zien

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**WERKCODE - FACTUREN**

Extra journalisatie (t.b.v. onderhanden werk)

---------------------------------------------------------------------------------------------------------
<div class="tag-fix"></div>
**WEBSITE**

Gerelateerde producten werden dubbel weergegeven.
Als je producten aan een ander product relateerde dan werd dit product dubbel opgeslagen en hierdoor ook dubbel zichtbaar op de website. dit is aangepast. 
![](images/product-gerelateerd-dubbel.jpg)

---------------------------------------------------------------------------------------------------------
<div class="tag-update"></div>
**KENMERKEN**

Bulk CMS eigenschappen kunnen bewerken vanaf product kenmerken. Je kan nu via de product kenmerken de CMS gegevens in één keer aanpassen.
![](images/cms-bulk-aanpassing-1.jpg)
![](images/cms-bulk-aanpassing-2.jpg)
---------------------------------------------------------------------------------------------------------
<div class="tag-new"></div>
**INKOOPFACTUUR**

Commissie afdracht velden beschikbaar gemaakt. Deze extra velden kunnen nu gebruikt worden in de word sjablonene die gebruik maken van de tabel "inkoopfacturen". 
![](images/word-sjabloon-commissie.jpg)


---------------------------------------------------------------------------------------------------------
<div class="tag-new"></div>
**E-MAIL SJABLONEN**

De verlof aanvraag e-mail kan nu zelf worden beheerd door middel van een sjabloon. 

---------------------------------------------------------------------------------------------------------
**12**

---------------------------------------------------------------------------------------------------------
