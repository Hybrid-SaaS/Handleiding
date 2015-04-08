<properties>
	<page>
		<title>SPF record toevoegen aan DNS</title>
	</page>
	<menu>
		<position>Handleiding / Onderdeel / E-mail </position> 
		<title>SPF record toevoegen</title>
	</menu>
</properties>

# SPF record toevoegen #

Om er voor te zorgen dat dat e-mails, welke vanuit Hybrid SaaS worden verstuurd, niet als spam worden aangemerkt dienen de <label keyword="spf">SPF-records</label> bij de <label keyword="dns">DNS</label> van het domein toegevoegd te worden.

<div class="info">
In dit record wordt vermeld welke mailservers namens dit domein mail mogen verzenden. Staat de mailserver van Hybrid SaaS niet in deze opsomming en verzendt deze toch mail met het betreffende domein als afzender, dan wordt de mail als onrechtmatig beschouwd. In de praktijk kan het voorkomen dat de e-mails niet bij de betreffende ontvanger worden afgeleverd. 
</div>

<div class="tip">
Deze gegevens dienen bij de serviceprovider van het domein, waar de e-mail van wordt verzonden, aangepast te worden. Uw systeembeheer weet hoe deze gegevens aangepast dienen te worden
</div>

## E-mailadres instellen ##

Voor het instellen van het e-mailadres ga je naar "e-mail sjablonen" 

Vul bij "van" het mailadres in vanwaar 

![e-mailadres instellen bij e-mailsjabloon](https://cloud.githubusercontent.com/assets/8395139/7047987/55c69a38-de10-11e4-8fad-21508c49806a.png)

<div class="info">
Wanneer het e-mailadres is ingegeven wordt automatisch gecheckt of de SPF records correct zijn ingesteld. Indien deze niet correct zijn wordt hiervan een melding gegeven.
</div>
