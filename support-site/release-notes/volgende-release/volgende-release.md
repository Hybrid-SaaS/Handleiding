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

## Modules ##

<div class="tag-fix"></div>

**Uitzetten module**

Bij het uitzetten van een module werden soms de rechten niet correct aangepast. Na deze update zullen de juiste rechten aangepast worden.

## Ticket ##

<div class="tag-fix"></div>

**Het vergoten van de melding**

Er is een mogelijkheid gemaakt om het scherm van de melding te kunnen vergroten zodat de tekst beter leesbaar is.
![](images/vergoten-melding.png)

<div class="tag-fix"></div>

**Vreemde taal of tekens**

Een email doorzetten naar een ticket gaf o.a. Chinese tekens (unicode) niet goed weer. Dit is opgelost.
 
**Extra veldcodes**

Er zijn 2 nieuwe veldcodes toegevoegd om te gebruiken: 

* `[%TICKET_TYPE%]` hierbij kan je de type van het ticket vermelden
* `[%TICKET_CUSTOMER_CODE%]` hierbij kan je de klantnaam vermelden

## Tijdregistratie ##

<div class="tag-fix"></div>

**Reisduur werd meegerekend in de totale interne uren**

Bij het aanmaken van een Tijdregistratie werd de reisduur meegerekend bij de interne uren, deze werden ook doorberekend op de factuur. Dit is verholpen. 
Je kan de duur registeren, alleen de reiskosten die ingevuld worden, worden nu door belast, en eventuele kilometer vergoeding. De reisduur is voor intern gebruik.

## Cloud ##

<div class="tag-fix"></div>

**Geen juiste weergave op de mobiele versie**

Bestanden in de cloud weergave werden niet goed geopend op mobiele apparaten omdat de mimetype niet gezet was.
Er zijn aanpassingen gedaan in de changelog

## Word sjablonen ##

**CSV bestand is nu een Excel bestand**

Er is een mogelijkheid om een query mee te geven met het verzenden van een factuur. Dit was een een CSV tekst bestand en dat is nu omgezet naar een Excel bestand met cijfers. Deze word in de bijlage van de mail toegevoegd met als naam export.xlsx mist je geen andere naam hebt doorgegeven 

## Algemeen ##

**Hybrid SaaS op 2 schermen openen**

![](images/1.png)

Het is nu mogelijk om je omgeving op je 2e scherm ook te openen, dit door middel van je rechtermuisknop in de balk.
Hierin kan je een 2e sessie openen

LET OP! je kan geen vensters verslepen van het ene scherm naar het andere scherm. het is bedoeld om verschillende schermen open te kunnen hebben staan

---