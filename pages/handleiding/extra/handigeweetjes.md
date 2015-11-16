<properties>
	<page>
		<title>handige-weetjes</title>
		<description>handige-weetjes</description>
	</page>
	<menu>
		<position>Handleiding</position>
		<title>Handige Weetjes</title>
		<sort>h</sort>
	</menu>
</properties>

----------


## Word sjablonen ##

**Bedrag weergeven met komma's en punten (€ 00.000,00)**

In het Word Document het betreffende MERGEFIELD veld opzoeken

Voorbeeld zonder € 12345.67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \* MERGEFORMAT}` 

Voorbeeld met € 12,345.67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \# .0,00 MERGEFORMAT}` 

 

**Engelse bedragen werken met een andere duizendtal notatie**

*Als het een Engels document bevat (wat is aangegeven bij de localisatie in het Word document) dien je het volgende toe te voegen*

Voorbeeld zonder € 12345,67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \* MERGEFORMAT}` 

Voorbeeld met € 12.345,67: `{MERGEFIELD INVOICE_Line_Total_excl_VAT \# ,0.00 MERGEFORMAT}`

----------
