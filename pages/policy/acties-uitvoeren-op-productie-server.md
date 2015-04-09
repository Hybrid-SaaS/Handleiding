<properties>
	<page>
		<title>Acties uitvoeren op een productieserver</title>
	</page>
	<menu>
		<position> Policies / Productieomgevingen </position> 
		<title>Acties uitvoeren</title>
	</menu>
</properties>

# Acties uitvoeren op een (productie)server van Hybrid SaaS #
We krijgen wel eens vragen om bepaalde acties uit te voeren via één van onze (productie)servers. Op deze pagina willen we uitleggen hoe wij hier mee omgaan.


## Productie server heeft toegang tot bepaalde resource ##

Doordat Hybrid SaaS kan koppelen met diverse externe systemen, komt het voor dat één van onze productie-servers / ip-adressen toegang heeft gekregen tot bepaalde andere externe bronnen.

<div class="info">
Een productieserver kan bijvoorbeeld zijn gewhite-list op een firewall van een toeleverancier en kan daardoor inloggen op de ftp-server van deze toeleverancier.
</div>

Eventuele verzoeken die onze helpdesk ontvangt om via één van onze servers acties uit voeren op deze externe bronnen **zullen wij niet uitvoeren**.

<div class="info">
Voorbeelden van acties die wij niet uitvoeren:

- Bestanden uploaden op een ftp-server
- Inloggen op een website
- Inloggen op een RDP sessie
</div>
