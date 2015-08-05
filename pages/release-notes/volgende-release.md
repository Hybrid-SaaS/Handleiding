<properties>
	<page>
		<title>Release notes volgende versie</title>
	</page>
	<menu>
		<position>Release notes</position>
		<title>Volgende versie</title>
	</menu>
</properties>





# Release notes volgende versie #
In de release notes staan de wijzigingen voor de volgende productieversie van Hybrid SaaS.


<div class="warning">
De beschreven aanpassingen zijn nog niet algemeen beschikbaar. De volgende release van Hybrid SaaS zal deze functionaliteiten bevatten.
</div>







## Balans & Winst en verliesrekening ##
<div class="tag-update"></div>

**Controle op ontbrekende boekstuknummer in de Inkoopfacturen**

In de balans & winst en verliesrekening is er nu een controlefunctie bij gekomen, er zal nu ook worden gecontroleerd of de boekstuknummers van alle "inkoopfacturen" in volgorde zullen doorlopen. 
Indien er nummers niet correct aansluiten, zal dit worden aangegeven:

![](images/boekstuknummercontrole.png)







## Systeemfunctionaliteit ##
<div class="tag-update"></div>

**Email, feedback als er geen e-mail is verzonden**

Er is een nieuw overzichtsvenster toegevoegd voor applicatie beheerders. In dit venster komen notificaties terecht van e-mails die niet werden verzonden:

![](images/notificatie-query.jpg)

Ook is het nu mogelijk om een e-mail bericht te ontvangen indien het verzenden niet is gelukt.

![](images/instellen-notificatie-adressen.jpg)

Zodra je het hebt ingesteld ontvang je een e-mail als het verzenden niet is gelukt. De e-mail ziet er als volgt uit.

![](images/voorbeeld-notificatie-email.jpg)




## Ticketsysteem ##
<div class="tag-update"></div>

**Tekst selecteren in ticket historie**

Het is nu mogelijk om in de ticket historie tekst te selecteren en te kopiëren.

![](images/ticket-tekst-selecteren.jpg)



<div class="tag-fix"></div>

**XSS bij aanlevering vanuit e-mail**

Het kon voorkomen dat een xss werd doorgelaten indien een ticket was aangemaakt dmv een email. Dit is nu ondervangen.  


<div class="tag-fix"></div>

**Control characters vanuit e-mail**

Het kon voorkomen dat bepaalde systeem karakters een foutmelding kon geven in Hybrid SaaS. Deze karakters worden uitgefilterd en geven geen problemen meer.  



## Automatische incasso ##
<div class="tag-update"></div>

Het was niet mogelijk om automatisch een betalingskorting toe te passen op automatische incassofacturen met een documentschema waar een betalingskorting van toepassing is.

Indien er een kortingspercentage is ingegeven en de facturen worden geïncasseerd zal Hybrid SaaS hier automatisch rekening mee houden:

![](images/documentschema-betalingskorting-incasso.jpg)

In het overzichtsvenster '*Facturen gereed voor automatische incasso*' is de betalingskorting en het te incasseren bedrag zichtbaar:

![](images/incasso-facturen-met-betalingskorting.jpg)

Na export is ook bij het overzichtsvenster '*Automatische incasso's bij bank*' de betalingskorting en het te incasseren bedrag zichtbaar:

![](images/incasso-facturen-met-betalingskorting-bij-bank.jpg) 


Na het inlezen van de banktransacties zullen de aangeboden automatische incasso's worden gesplitst over 2 grootboekrekeningen, het originele factuurbedrag en de betalingskorting

![](images/bank-inlezen-automatische-grootboek-koppeling.jpg)


deze grootboek kan je instellen op in het entiteit-scherm

![](images/entiteit-instelling-grootboek-betalingskorting.jpg)









## Bankrekening ##
<div class="tag-fix"></div>

**Verwijderen van bankrekening import**

Het verwijderen van een bankrekeningimport gaf een foutmelding dat de periode was geblokkeerd, deze melding was niet terecht.



