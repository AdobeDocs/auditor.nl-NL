---
description: informatie over de tests van de Adobe Experience Platform Auditor
seo-description: information about the Adobe Experience Platform Auditor tests
seo-title: Test rubric 0.0.8
title: Testrubriek 0.0.8
uuid: c62b7169-a650-4650-876f-c254eb57cb25
exl-id: 0313e271-5664-4a34-9e3c-8cb1c61d8b93
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '1998'
ht-degree: 4%

---

# Testrubriek 0.0.8{#test-rubric}

## Testrubriek 0.0.8

<!-- Note to writer: Please review the tables on this page for formatting and accuracy. Compare to original file.-->

![](assets/space.png)

## Waarschuwingen {#alerts}

Deze naslaggids bevat meer informatie over de waarschuwingen die Adobe Experience Platform Auditor weergeeft voor tests.

Waarschuwingen tonen problemen waarvan je op de hoogte moet zijn, maar die geen invloed hebben op je score.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Testen </th> 
    <th colname="col2" class="entry"> Criteria </th> 
    <th colname="col3" class="entry"> Aanbeveling </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - Correct geïmplementeerde omzettingstag</b> </p> <p>Dikte: 0 </p> </td> 
    <td colname="col2"> <p>Controleer of de juiste conversietag wordt gebruikt. </p> <p> <p>Waarschuwing: Het gebruik van verouderde conversietags voor TubeMogul kan gegevensverlies tot gevolg hebben. </p> </p> </td> 
    <td colname="col3"> <p>Voer een upgrade uit op de conversiepixels naar de nieuwe Advertising Cloud-tags voor conversie van alleen afbeeldingen. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor Adobe Experience Platform Launch worden verwezenlijkt. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - Tag met alleen afbeelding</b> </p> <p>Dikte: 0 </p> </td> 
    <td colname="col2"> <p>De Advertising Cloud-indeling voor afbeeldingspixels moet overeenkomen met een van de volgende aanbevolen indelingen: </p> <p> 
      <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
       <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;hash_value&gt;</span> </p> </li> 
       <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;hash_value&gt;</span> </p> </li> 
       <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;numeric_id&gt;?</span> </p> </li> 
      </ul> </p> </td> 
    <td colname="col3"> <p>Upgrade uw Advertising Cloud-pixels naar de nieuwe Advertising Cloud-tags voor alleen afbeeldingen, zodat u de volledige Advertising Cloud-functionaliteit kunt benutten. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor Platform launch worden verwezenlijkt. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - Segmentpixels DSP synchroniseren ingeschakeld</b> </p> <p>Dikte: 0 </p> </td> 
    <td colname="col2"> <p>Controleer of de TubeMogul-segmentpixel een DSP-instelling bevat en adviseer dat de instelling aan de pixel wordt toegevoegd. </p> <p>De instelling DSP synchroniseren wordt bepaald door het gebruik van een parameter voor een queryreeks, dus </p> <p>ALS de tag wordt geactiveerd naar<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;hash_value&gt;"</span> </p> <p> OF <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;hash_value&gt;"</span> </p> <p> OF <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;numeric_id&gt;?"</span> </p> <p>EN de tag bevat de URL-parameter <span class="codeph"> "sid=")</span> </p> <p>Controleer VERVOLGENS of de URL-parameter <span class="codeph"> "cs=0"</span> of<span class="codeph"> "cs=1"</span> bestaat, en als niet adviseert dat <span class="codeph"> "cs=1"</span> worden toegevoegd aan deze pixels, zodat de overeenkomende populatiegraad kan worden verbeterd. </p> </td> 
    <td colname="col3"> <p> De URL-parameter toevoegen <span class="codeph"> "cs=1"</span> op uw Advertising Cloud-pixels zodat DSP synchroniseren kan plaatsvinden. Hierdoor nemen de overeenkomende populaties toe. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor Platform launch worden verwezenlijkt. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottom callback-plaatsing</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aanvullende informatie</a> </p> 
     <!--
       TEa9df69942f404055a64262889c8b21d3 
     --> </td> 
    <td colname="col2"> <p> Dynamische Tag Management vereist<span class="codeph"> _satelliet.pageBottom()</span> functie. </p> <p>Het wordt aanbevolen de tag als <i>last</i> in de <span class="codeph"> &lt;body&gt;</span>. Als deze is gevonden in het dialoogvenster <span class="codeph"> &lt;body&gt;</span> -tag, heeft de kans om te werken, maar omdat dit niet de beste praktijk is, kan deze onjuist functioneren of onverwachte of ongewenste resultaten opleveren. </p> </td> 
    <td colname="col3"> <p>Voeg het inlinescript onmiddellijk vóór het sluiten toe <span class="codeph"> &lt;/body&gt;</span> -tag voor een correcte DTM-functionaliteit. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Experience Cloud ID-service - Gebruik slechts één AdobeOrg</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/id-request.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p>In een normale MCID-implementatie moet één AdobeOrg worden gebruikt. </p> </td> 
    <td colname="col3"> <p>Controleer of er meerdere AdobeOrg-id's bestaan voor deze implementatie. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Doel - Inhoud in mboxDefault</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De inhoud moet in mboxDefault bestaan wanneer u at.js gebruikt. </p> </td> 
    <td colname="col3"> <p>Controleer of de inhoud beschikbaar is. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Configuratie {#configuration}

Deze verwijzing verstrekt meer informatie over de controleur van het Platform van tests voor configuratie presteert.

De Auditor van het Platform evalueert de markeringen tegen andere regels en geadviseerde beste praktijken.

<table id="table_A8A1FC360482447185C8460A18426638"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Testen </th> 
    <th colname="col2" class="entry"> Criteria </th> 
    <th colname="col3" class="entry"> Aanbeveling </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - Conversienamen gebruiken alleen alfanumerieke tekens</b> </p> <p>Dikte: 3 </p> </td> 
    <td colname="col2"> <p>De <span class="codeph"> ev_conversion_property_name</span> parameter mag alleen numerieke en decimale waarden bevatten, behalve "<span class="codeph"> ev_transid</span>" parameter (de <span class="codeph"> ev_transid</span> waarde kan tekst of numerieke waarden bevatten) </p> <p>Zoeken naar <span class="codeph"> everesttech.net</span> pixels met een URL-parameter die begint met <span class="codeph"> ev_</span>. </p> <p>Voorbeeld: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47</span> </p> </td> 
    <td colname="col3"> <p> Zorg ervoor dat de parameters van de transactieeigenschap alleen numerieke en decimale waarden bevatten. </p> <p> <p>Waarschuwing: Andere waardetypen kunnen gegevensverlies veroorzaken. </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - Conversienamen gebruiken URL-veilige tekens</b> </p> <p>Dikte: 3 </p> </td> 
    <td colname="col2"> <p> Namen van conversie-eigenschappen mogen geen en-teken of vraagteken bevatten. </p> <p> Voorbeeld: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>Zorg ervoor dat de parameters van de transactieeigenschap geen niet-gecodeerd en/of vraagteken bevatten. Hiermee wordt de URL-indeling verbroken. </p> <p> <p>Waarschuwing: Eigenschapparameters die een niet-gecodeerd en/of vraagteken bevatten, (bijvoorbeeld: <span class="codeph"> ev_formComplete?=1</span> of <span class="codeph"> ev_formComplete&amp;Submit=1</span>), kan leiden tot gegevensverlies. </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - Transactie-ID correct geïmplementeerd</b> </p> <p>Dikte: 1 </p> </td> 
    <td colname="col2"> <p> De eigenschapsnaam <span class="codeph"> ev_transid=</span> mag niet leeg zijn. </p> <p>Voorbeeld: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>De eigenschapsnaam <span class="codeph"> ev_transid=</span> mag niet zonder waarde (<span class="codeph"> ev_transid=</span>). Als dit zonder een waarde wordt verlaten, zou er verlies van transactiegegevens kunnen zijn. Een waarde toewijzen aan de <span class="codeph"> ev_transid=</span> of verwijder de parameter uit de pixel. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - Instantiated in DOM</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/testing-and-validation-process/impl-validation.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De Adobe Analytics-code is niet geïnstalleerd of kan niet worden uitgevoerd. Retourneert 0 wanneer er geen analytische code op de webpagina is gevonden. </p> </td> 
    <td colname="col3"> <p>Controleer of de tag Analytics is geïmplementeerd op de pagina en niet wordt geblokkeerd door daaropvolgende scriptactiviteiten. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analyse - eenmaal geïnstantieerd</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De Adobe Analytics-code is meerdere keren gedetecteerd op de pagina. . Retourneert 0 wanneer er geen analytische code op de webpagina is gevonden. </p> </td> 
    <td colname="col3"> <p>Zorg ervoor dat er slechts één tag Analytics op de pagina staat. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analyse - nieuwste versie</b> </p> <p>Dikte: 3 </p> <p><a href="https://docs.adobe.com/content/help/nl-NL/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De meest recente versie van de Codebibliotheek Analytics wordt niet uitgevoerd op uw pagina's. Codebibliotheken die Experience Cloud-technologieën van stroom voorzien, worden voortdurend bijgewerkt en getweend om te profiteren van prestatieverbeteringen en de nieuwste functies te bieden. Retourneert 0 wanneer er geen analytische code op de webpagina is gevonden. </p> </td>       
    <td colname="col3"> <p>Installeer de nieuwste versie van de bibliotheek Analytics. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - zelfgehoste</b> </p> <p>Dikte: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De DTM-bibliotheek Akamai wordt gehost op Adobe-instantie op <span class="filepath"> assets.adobedtm.com</span>. </p> <p> Zelf hosten is de geadviseerde benadering voor het laden van DTM omdat het grotere controle van websiteprestaties door geheim voorgeheugencontrole, vermindert derdemanuscriptgebiedsdelen, en grotere controle van het het publiceren proces verleent. De DTM-bibliotheken kunnen worden gehost en beheerd via uw eigen webhosting of CDN. </p> </td> 
    <td colname="col3"> <p>Zelfhosting is de aanbevolen methode voor het laden van DTM op een pagina. Hoewel DTM-hosting via de Akamai CDN in de meeste gevallen werkt, verbetert zelforhosting de paginaprestaties. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - tags van derden worden asynchroon geladen nadat DOM gereed is</b> </p> <p>Dikte: 3 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/resources/load-order.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p>Om een evenwicht te vinden tussen een goede gebruikerservaring en het verzamelen van nauwkeurige gegevens, zouden de markeringen van de derde partij bij DOM klaar moeten teweegbrengen. Zo zorgt u ervoor dat deze volgende scripts worden uitgevoerd zonder dat dit van invloed is op de functionaliteit van de site. </p> </td> 
    <td colname="col3"> <p>Los dit probleem op door alle regels aan te passen die pixels van derden uitvoeren om bij DOM Ready te worden geactiveerd. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID-service - Laatste versie</b> </p> <p>Dikte: 2 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> Uw pagina's worden niet uitgevoerd met de nieuwste versie van de codebibliotheek voor bezoekers-id's, <span class="codeph"> bezoekerAPI.js</span>. Codebibliotheken die Experience Cloud-technologieën van stroom voorzien, worden voortdurend bijgewerkt en getweend om te profiteren van prestatieverbeteringen en de nieuwste functies te bieden. </p> </td> 
    <td colname="col3"> <p>Installeer de nieuwste versie van de bibliotheek met bezoekersidentiteiten. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Doel - Laatste versie</b> </p> <p>Dikte: 2 </p> <p><a href="https://marketing.adobe.com/resources/help/en_US/dtm/target/" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De meest recente versie van de doelcodebibliotheek wordt niet uitgevoerd op uw pagina's. Codebibliotheken die Experience Cloud-technologieën van stroom voorzien, worden voortdurend bijgewerkt en getweend om te profiteren van prestatieverbeteringen en de nieuwste functies te bieden. </p> </td> 
    <td colname="col3"> <p>Installeer de nieuwste versie van de doelbibliotheek. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Doel - mboxDefault komt eerder dan mboxCreate </b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p>Het juiste gebruik van <span class="codeph"> mboxCreate</span> ziet er ongeveer als volgt uit: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Inhoud van de klant—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
    <td colname="col3"> <p>Zorg ervoor dat u een <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> tag voor aanroepen <span class="codeph"> mboxCreate()</span>. om.js zal geen één voor u toevoegen. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Doel: geldig DOCTYPE</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> Er is een ongeldig DOCTYPE gedetecteerd. In dit scenario worden geen vakjes geactiveerd. </p> <p>Voor at.js, moet DOCTYPE op de wijze van Normen zijn of het Doel zal niet werken. </p> </td> 
    <td colname="col3"> <p>Werk het DOCTYPE op de pagina bij. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Codeconsistentie {#tag-consistency}

Deze verwijzing verstrekt meer informatie over de tests de Auditor van het Platform voor markeringsconsistentie presteert.

De Auditor van het Platform evalueert of de markeringen over URLs verenigbaar zijn.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Testen </th> 
    <th colname="col2" class="entry"> Criteria </th> 
    <th colname="col3" class="entry"> Aanbeveling </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Analyse - Consistente codeversie </b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> Er zijn meerdere versies van de Analytics-code gevonden. </p> </td> 
    <td colname="col3"> <p>Vervang alle instanties van Analytics door de huidige versie. </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## Tagaanwezigheid {#tag-presence}

Deze verwijzing verstrekt meer informatie over de tests de Auditor van het Platform voor markeringsaanwezigheid uitvoert.

De Auditor van het Platform evalueert of de markering bestaat, en of het op de juiste plaats in uw paginacode, etc. is.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> Testen </th> 
    <th colname="col2" class="entry"> Criteria </th> 
    <th colname="col3" class="entry"> Aanbeveling </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> </td> 
    <td colname="col2"> <p> De Advertising Cloud-tag is niet beschikbaar in het DOM. </p> </td> 
    <td colname="col3"> <p>Implementeer de Advertising Cloud-tag met de Advertising Cloud-extensie voor Platform launch. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - Geïmplementeerde segmentpixel</b> </p> <p>Dikte: 5 </p> </td> 
    <td colname="col2"> <p> Upgrade de Advertising Cloud-segmentpixels naar de nieuwe Advertising Cloud-tags voor alleen afbeeldingen. Het gebruik van verouderde AMO-segmenttags kan leiden tot gegevensverlies. </p> </td> 
    <td colname="col3"> <p>Implementeer het Advertising Cloud-segmentpixel met de Advertising Cloud-extensie voor Platform launch. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analyse - geladen in DOM</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De Adobe Analytics-tag is niet gedetecteerd. </p> </td> 
    <td colname="col3"> <p>Installeer de nieuwste versie van Analytics. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM - Bibliotheek geladen</b> </p> <p>Dikte: 5 </p> <p>Aanvullende informatie: </p> <p> 
      <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
       <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTM-probleemoplossing</a> </li> 
       <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Code voor kop- en voetteksten toevoegen</a> </li> 
      </ul> </p> </td> 
    <td colname="col2"> <p> Een globaal _satelliet-object is niet gevonden in de DOM. Dynamic Tag Management is niet geïnstalleerd of kan niet worden uitgevoerd. </p> </td> 
    <td colname="col3"> <p>Controleer of de DTM-bibliotheek op de pagina is geïmplementeerd en niet wordt geblokkeerd door daaropvolgende scriptactiviteiten. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM - Eén insluitcode</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> Productieplaatsen mogen slechts één DTM-bibliotheek laden. </p> </td> 
    <td colname="col3"> <p>Controleer of alleen de productiebibliotheek op de pagina wordt geladen. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottom callback bestaat in &lt;body&gt;</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De <span class="codeph"> _satelliet.pageBottom()</span> callback is niet gevonden in het dialoogvenster <span class="codeph"> &lt;body&gt;</span> van de pagina, vereist door Dynamic Tag Management. </p> <p>Deze test mislukt als de <span class="codeph"> pageBottom </span>de vraag wordt niet gevonden bij allen op de pagina, of als het in <span class="codeph"> &lt;head&gt;</span> -tag (of een andere onverwachte locatie). Het gaat alleen door als <span class="codeph"> pageBottom</span> bevindt zich ergens in de <span class="codeph"> &lt;body&gt;</span> tag. Als het helemaal niet op de pagina staat, werkt het niet en de andere twee <span class="codeph"> pageBottom</span> de tests zullen ook mislukken . </p> </td> 
    <td colname="col3"> <p>Voeg het inlinescript onmiddellijk vóór het sluiten toe <span class="codeph"> &lt;/body&gt;</span> -tag voor een correcte DTM-functionaliteit. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - pageBottom-tag geactiveerd</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De DTM <span class="codeph"> pageBottom</span> tag is niet gedetecteerd. </p> <p>Dit zou kunnen voorkomen als de vraag binnen een <span class="codeph"> indien</span> verklaring die in iets gelijkaardig aan resulteert <span class="codeph"> if (false) {_satelliet.pageBottom()}</span>. Dus, hoewel het zou kunnen bestaan en correct geplaatst zijn, zou de markering niet kunnen branden. </p> </td> 
    <td colname="col3"> <p>De DTM installeren <span class="codeph"> pageBottom</span> roep op elke pagina. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID-service - aanwezigheid cookie</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De <span class="codeph"> AMCV_</span> cookie niet gevonden. U moet een bezoekersobject instantiëren vanuit het dialoogvenster <span class="codeph"> VisitorAPI.js</span> code. </p> </td> 
    <td colname="col3"> <p> Als dit een DTM-implementatie is, controleert u of de AdobeOrg-id correct is ingevoerd in de MCID-tool. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID-service - MID-waarde aanwezig</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/nl-NL/id-service/using/intro/cookies.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De gemiddelde waarde is niet gevonden in het dialoogvenster <span class="codeph"> AMCV_</span> cookie. </p> </td> 
    <td colname="col3"> <p>Test opnieuw om te controleren op een eventuele MCID API-latentie. Neem contact op met de klantenservice van Adobe als de aandoening aanhoudt. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Experience Cloud ID-service - moet worden geïnstalleerd</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
    <td colname="col2"> <p> De Experience Cloud ID-servicecode is niet gevonden. De ECID wordt ten zeerste aanbevolen om ervoor te zorgen dat u de meeste waarde uit uw Experience Cloud-oplossingen haalt en is van essentieel belang voor ID-beheer in alle EG-oplossingen. </p> </td> 
    <td colname="col3"> <p>Installeer de meest recente versie van MCID. </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Doel - Bibliotheek geladen in &lt;head&gt;</b> </p> <p>Dikte: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Aanvullende informatie</a> </p> 
     <!--
       TE61c380082a4b4706b28a84aa047599a7 
     --> </td> 
    <td colname="col2"> <p> De doelbibliotheek moet in het dialoogvenster <span class="codeph"> &lt;head&gt;</span> tag. </p> </td> 
    <td colname="col3"> <p> Controleer of de doelbibliotheek is geladen in het dialoogvenster <span class="codeph"> &lt;head&gt;</span> tag. </p> </td> 
   </tr> 
  </tbody> 
</table>
