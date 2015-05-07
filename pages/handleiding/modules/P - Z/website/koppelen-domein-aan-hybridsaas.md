<properties>
	<page>
		<title>Domeinnaam DNS instellen</title>
		<description>Uitleg over hoe je je dns moet instellen voor gebruik van de Hybrid SaaS webshop.</description>
	</page>
	<menu>
		<position>Handleiding / Webshop</position>
		<title>Dns instellen</title>
	</menu>
</properties>


# Hoe stel ik de DNS-records in voor mijn domeinnaam? #

Om je eigen domeinnaam te koppelen aan de webshop van Hybrid SaaS dien je hiervoor <label keyword="dns">DNS-records</label> in te stellen. In essentie is dit om domeinnamen aan <label keyword="ip">ip-adressen</label> te koppelen. <label keyword="dns">DNS-records</label> zijn essentieel voor de bereikbaarheid van je domeinnaam. 

<div class="info">
Omdat een internetdomein jouw eigendom is past Hybrid SaaS geen DNS-records aan. Je dient de DNS wijzigingen zelf door te voeren.
</div>

## Jouw domein koppelen aan Hybrid SaaS ##
Om je domein te koppelen aan jouw Hybrid SaaS-omgeving moet je een wijziging doorvoeren in je DNS-records.

<div class="tip">
Wij raden aan om je domein te koppelen met een <label>CNAME</label>-record, dit omdat het voor kan komen dat zonder vooraankondiging het IP-adres van je Hybrid SaaS omgeving kan worden gewijzigd in geval van disaster-recovery.
</div>

## Hoe stel ik een doorverwijzing via CNAME in? ##
In de meeste gevallen kan je provider de doorverwijzing voor je instellen. Neem dus contact op met de support van je provider. Bij sommige providers heb je zelf de mogelijkheid om zelf de instellingen aan te passen. 
 
<div class="warning">
Let op:
Als je een domein via CNAME naar je Hybrid SaaS website wilt doorverwijzen, laat dat dan ook aan onze support weten. Het domein moet namelijk ook nog in ons systeem aan jouw Hybrid SaaS-omgeving worden gekoppeld.
</div>

## Wat geef ik door aan mijn provider? ##
Met de volgende informatie kan je provider de CNAME instellen:

www.*domeinnaam.xx* **CNAME** *omgeving*.hybridsaas.com

Vervang hierbij domeinnaam.xx door de naam en de extensie van jouw domein.
Vervang *omgeving* door jouw Hybrid SaaS omgevingsnaam.
 
Nadat je de aanpassingen hebt ingevoerd, kan het tot 24 uur duren voor je domein met jouw Hybrid SaaS website is verbonden.

<div class="info">
- Je domein blijft gehost bij je provider.
- De instellingen voor de domeinnaam moeten worden aangepast, zodat bezoekers op die domeinnaam de website vinden die in Hybrid SaaS is aangemaakt.
</div>
