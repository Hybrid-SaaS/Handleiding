<properties>
	<page>
		<title>uitleg</title>
		<description>Uitleg</description>
	</page>
	<menu>
		<position>Modules N - Z/ Projectbeheer</position>
		<title>Project marge informatie</title>
	</menu>
</properties>

# Project marge informatie #

Deze rubriek zal meer duidelijkheid geven over hoe de waarde word opgebouwd in de projectkaart onder de tabbel Marge informatie.

## Begin bedrag van €20.000,00 ##

Er is een offerte aangemaakt van € 20.000,00 en deze is omgezet naar een prject.
Het projectwaarde heeft hierdoor een waarde van € 20.000,00

![begin stand vanaf 0 marge informatie](images/begin-saldo.png)

## Tijdregistratie's nog niet goedgekeurd ##

Er zijn 5 lossen tijdregistraties op dit project gemaakt met als uurtarief van €10,00 en een intern uurtarief van €5,00

![losse tijdregistraties op project](images/tijdregistratie-los.png)

<div class="tip">
De uren zijn nog niet goedgekeurd
</div>

**Nog niet verwerkt**

- Uren: 50 (5 registratie's a 10 uur)
- Arbeid: €250,00 (50 uur a €5 intern uurtarief)
- Te fact. arbeid: €500,00 (50 uur a €10 uurtarief)

![waarde na toevoegen tijdregistratie](images/waarde-toevoegen-tijdregistratie.png)

## Werkbon aanmaken nog niet goedgekeurd ##

Er is een werkbon gemaakt met daarin een tijdregistratie van 15 uur met als uurtarief €10,00 en een intern uurtarief van €5,00

![werkbon aanmaken tijdregistratie](images/werkbon-tijd.png)

Ook zijn er kosten gemaakt op de werkbon 1 product van €15,00 excl btw

![werkbon aanmaken kosten](images/werkbon-kosten.png)

<div class="tip">
De werkbon is nog niet goedgekeurd
</div>

**Nog niet verwerkt**

- Uren: 65 (5 registratie's a 10 uur en 1 registratie van 15 uur)
- Arbeid: €325,00 (65 uur a €5 intern uurtarief)
- Te fact. arbeid: €650,00 (65 uur a €10 uurtarief)

![werkbon aanmaken niet goedgekeurd marge](images/werkbon-aanmaken.png)

## Werkbon goedkeuren maar nog niet factureren ##

De werkbon is goedgekeurd tot de laatste stap maar nog niet gefactureerd. Hierdoor is 1 tijdregistatie goedgekeurd en mag het product gefactureerd gaan worden.

![werkbon goedgekeurd maar nog geen factuur](images/werkbon-goedgekeurd.png)

<div class="tip">
De werkbon is goedgekeurd maar er is nog geen factuur van gemaakt
</div>

**Marge informatie**

- Uren: 15 (1 registratie van 15 uur)
- Arbeid: €75,00 (15 uur a €5 intern uurtarief)

**Nog niet verwerkt**

- Uren: 50 (5 registratie's a 10 uur)
- Arbeid: €250,00 (50 uur a €5 intern uurtarief)
- Te fact. arbeid: €650,00 (65 uur a €10 uurtarief)

## De factuur van de werkbon nog niet verstuurd ##

Er is nu een factuur aangemaakt van de werkbon. Deze is nog niet goedgekeurd en nog niet als verzonden genoteerd.

![factuur van de werkbon](images/werkbon-factuur.png)

<div class="tip">
De tijdregistratie en de kosten van de werkbon worden nu gefactureerd
</div>

![factuur van de werkbon marge](images/werkbon-factuur-marge.png)

**Marge informatie**

- Uren: 15 (1 registratie van 15 uur)
- Arbeid: €75,00 (15 uur a €5 intern uurtarief)

**Nog niet verwerkt**

- Facturen: €165,00 (het totaalbedrag van de **nieuwe** factuur excl. btw)
- Uren: 50 (5 registratie's a 10 uur)
- Arbeid: €250,00 (50 uur a €5 intern uurtarief)
- Te fact. arbeid: €500,00 (50 uur a €10 uurtarief)

## De factuur van de werkbon status verstuurd ##

![factuur verzonden marge](images/werbon-verstuurd-marge.png)

<div class="tip">
De status van de factuur is nu verstuurd, nu heeft het de waarde van gefactureerd (het is verstuurd naar de klant)
</div>

**Marge informatie**

- Gefactureerd: €165,00 (totaal van verzonden facturen)
- Resterend: €1.9835,00 (Projectwaarde minus gefactureerd)

**Marge informatie**

- Uren: 15 (1 registratie van 15 uur)
- Producten: €15,00 (Het product van de werkbon)
- Arbeid: €75,00 (15 uur a €5 intern uurtarief)

**Nog niet verwerkt**

- Uren: 50 (5 registratie's a 10 uur)
- Arbeid: €250,00 (50 uur a €5 intern uurtarief)
- Te fact. arbeid: €500,00 (50 uur a €10 uurtarief)

## De losse uren goedkeuren ##

![tijdregistratie goedkeuren ](images/tijdregistratie-los-goedgekeurd.png)

<div class="tip">
De tijdregistratie zijn goedgekeurd maar nog niet doorgezet als factuur
</div>

![tijdregistratie goedkeuren ](images/losse-uren-goedkeuren.png)

**Marge informatie**

- Gefactureerd: €165,00 (totaal van verzonden facturen)
- Resterend: €1.9835,00 (Projectwaarde minus gefactureerd)

**Marge informatie**

- Uren: 65 (5 registratie's a 10 uur en 1 registratie van 15 uur)
- Producten: €15,00 (Het product van de werkbon)
- Arbeid: €325,00 (65 uur a €5 intern uurtarief)

**Nog niet verwerkt**

- Uren: 0,00 (er zijn geen nog goed te keuren tijdregistaties)
- Arbeid: 0,00 (er zijn geen nog goed te keuren tijdregistaties)
- Te fact. arbeid: €500,00 (50 uur a €10 uurtarief)

## De losse uren doorzetten tot factuur ##

![tijdregistratie goedkeuren ](images/factuur-losse-registraties.png)

<div class="tip">
De tijdregistraties zijn verwerkt en hiervan is een factuur gemaakt maar heeft nog niet de status verzonden
</div>

![tijdregistratie goedkeuren ](images/marge-goedgekeurde-tijd.png)

**Marge informatie**

- Gefactureerd: €165,00 (totaal van verzonden facturen)
- Resterend: €1.9835,00 (Projectwaarde minus gefactureerd)

**Marge informatie**

- Uren: 65 (5 registratie's a 10 uur en 1 registratie van 15 uur)
- Producten: €15,00 (Het product van de werkbon)
- Arbeid: €325,00 (65 uur a €5 intern uurtarief)

**Nog niet verwerkt**

- Facturen: €500,00 (het totaalbedrag van de **nieuwe** factuur excl. btw)
- Uren: 0,00 (er zijn geen nog goed te keuren tijdregistaties)
- Arbeid: 0,00 (er zijn geen nog goed te keuren tijdregistaties)
- Te fact. arbeid: 0,00 (er zijn geen nog goed te keuren tijdregistaties)

## Factuur status verstuurd  ##

<div class="tip">
Alle facturen hebben de status verstuurd en alle tijdregistraties zijn verwerkt
</div>

![tijdregistratie goedkeuren ](images/eind-saldo.png)

**Marge informatie**

- Gefactureerd: €665,00 (totaal van verzonden facturen)
- Resterend: €1.9335,00 (Projectwaarde minus gefactureerd)

**Marge informatie**

- Uren: 65 (5 registratie's a 10 uur en 1 registratie van 15 uur)
- Producten: €15,00 (Het product van de werkbon)
- Arbeid: €325,00 (65 uur a €5 intern uurtarief)

<div class="tip">
De informatie bij marge infomratie is verwerkt in het stukje van gefactureerd en resterend
</div>

**Nog niet verwerkt**

- Facturen: 0,00 (er zijn geen nog goed te keuren facturen)
- Uren: 0,00 (er zijn geen nog goed te keuren tijdregistaties)
- Arbeid: 0,00 (er zijn geen nog goed te keuren tijdregistaties)
- Te fact. arbeid: 0,00 (er zijn geen nog goed te keuren tijdregistaties)

-------






