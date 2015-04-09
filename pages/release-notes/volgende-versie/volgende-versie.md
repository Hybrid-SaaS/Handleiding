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
 


## Verbetering werking geëxporteerde inkoopfacturen ##

<div class="tag-fix"></div>
Op inkoopfacturen werden betalings en financiële exports niet altijd weergegeven.

![](images/inkoop-factuur-export-info.jpg)



<div class="tag-update"></div>
Indien het deblokkeren van een inkoopfactuur niet mogelijk is omdat er een financiële export aanwezig is, verschijnt er nu een verbeterde melding die direct verwijst naar het nummer van de export.

![](images/inkoop-factuur-melding-deblokkeren.jpg)



## Verbetering werking geëxporteerde verkoopfacturen ##

<div class="tag-update"></div>
Indien het deblokkeren van een verkoopfactuur niet mogelijk is omdat er een financiële export aanwezig is, verschijnt er nu een verbeterde melding die direct verwijst naar het nummer van de export.

![](images/verkoop-factuur-melding-deblokkeren.jpg)


## Individuele financiële export records ongedaan maken ##

<div class="tag-new"></div>
Het is mogelijk om losse transacties van een financiële export ongedaan te maken. Hiervoor is een nieuwe menu knop toegevoegd genaamd **Ongedaan maken** 

![](images/financiele-export-ongedaan-maken.jpg)

Na het aanklikken van deze knop en bevestigen van de onderstaande vraag zal de export ongedaan worden gemaakt en kan daarmee opnieuw worden aangeboden. Tevens kan na het ongedaan maken van de financiële export record de gekoppelde inkoop/verkoopfactuur worden gedeblokkeerd.

![](images/financiele-export-ongedaan-maken-vraag.jpg)

Na het ongedaan maken is dit ook zichtbaar in de het overzicht met gekoppelde records van de export in de kolom *Ongedaan gemaakt*

![](images/financiele-export-ongedaan-gemaakt.jpg)

Tevens is de actie gelogd bij de gekoppelde factuur

![](images/financiele-export-ongedaan-gemaakt-log.jpg)
