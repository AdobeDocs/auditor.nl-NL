---
description: 'null'
seo-description: 'null'
seo-title: Testrubriek 1.0.1
title: Testrubriek 1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
translation-type: tm+mt
source-git-commit: 712d0768e5e5394372293bf8231c91489519bcd1

---


# Testrubriek 1.0.1{#test-rubric}

## Testrubriek 1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## Waarschuwingen {#alerts}

Deze verwijzing verstrekt meer informatie over de vertoningen van de Auditor van alarm voor tests.

Waarschuwingen tonen problemen waarvan je op de hoogte moet zijn, maar die geen invloed hebben op je score. Dit zijn aanbevelingen voor best practices die in sommige gevallen niet van toepassing zijn op uw implementatie.

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Cloud voor advertenties - Geïmporteerde conversietag corrigeren</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Controleer of de juiste conversietag wordt gebruikt. </p> <p> <p>Waarschuwing:  Het gebruik van verouderde conversietags voor TubeMogul kan gegevensverlies tot gevolg hebben. </p> </p> </td> 
   <td colname="col3"> <p>Voer een upgrade uit op de conversiepixels naar de nieuwe conversietags voor afbeeldingen in de cloud voor advertenties. </p> <p>Dit kunt u het gemakkelijkst doen met de Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - JS-tag corrigeren gebruikt</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud moet de nieuwste JavaScript-tags gebruiken. </p> </td> 
   <td colname="col3"> <p>Voer een upgrade uit van uw JavaScript voor Adobe Advertising Cloud naar de meest recente versie. Als u de verouderde JavaScript-versies gebruikt, kan de functionaliteit verloren gaan. </p> <p>Dit kan gemakkelijker worden bereikt met de Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Cloud voor advertenties - tag Alleen afbeelding</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>De pixelindeling voor Advertising Cloud moet overeenkomen met een van de volgende aanbevolen indelingen: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Upgrade uw Cloud-advertentiepixels naar de nieuwe Cloud-afbeeldingstags voor Advertising, zodat u de volledige functionaliteit voor Advertising Cloud kunt gebruiken. </p> <p>Dit kunt u het gemakkelijkst doen met de Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Segmentpixels DSP-synchronisatie ingeschakeld</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Controleer of de TubeMogul-segmentpixel een instelling voor DSP synchroniseren bevat en adviseer dat de instelling aan de pixel wordt toegevoegd. </p> <p>De instelling DSP-sync wordt bepaald door het gebruik van een parameter voor een queryreeks, dus </p> <p>ALS de tag wordt geactiveerd naar<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;")</span> </p> <p> OF <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OF <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>EN de tag bevat de URL-parameter <span class="codeph"> "sid=")</span> </p> <p>Controleer VERVOLGENS of de URL-parameter <span class="codeph"> "cs=0"</span> of<span class="codeph"> "cs=1"</span> bestaat en adviseer, als dit niet het geval is, dat <span class="codeph"> "cs=1"</span> aan die pixels wordt toegevoegd zodat de overeenkomende frequenties van de doelgroep kunnen worden verbeterd. </p> </td> 
   <td colname="col3"> <p> Voeg de URL-parameter <span class="codeph"> "cs=1"</span> toe aan uw Cloud-advertentiepixels, zodat DSP-synchronisatie kan optreden, waardoor de overeenkomende populaties toenemen. </p> <p>Dit kan het gemakkelijkst worden verwezenlijkt met de Advertising Cloud Launch Extension. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - pageBottom callback-plaatsing</b> </p> <p>Dikte: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Aanvullende informatie</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>Dynamisch tagbeheer vereist de functie <span class="codeph"> _satelliet.pageBottom()</span> . Voeg het inlinescript onmiddellijk voorafgaand aan de sluitende lichaamsletter toe om juiste functionaliteit te verzekeren DTM. </p> <p> <p>Opmerking: Het wordt aanbevolen dat de tag de <i>laatste</i> tag in de <span class="codeph"> &lt;body&gt;</span>is. Als het binnen de <span class="codeph"> &lt;body&gt;</span> markering wordt gevonden, heeft het een kans om te functioneren, maar aangezien het niet beste praktijken is, kon het verkeerd of met onverwachte of ongewenste resultaten functioneren. </p> </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript direct vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag toe voor de juiste DTM-functionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - zelfgehoste</b> </p> <p>Dikte: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De DTM-bibliotheek wordt gehost op de Akamai-instantie van Adobe op <span class="filepath"> assets.adobedtm.com</span>. </p> <p> Zelf hosten is de geadviseerde benadering voor het laden van DTM omdat het grotere controle van websiteprestaties door geheim voorgeheugencontrole, vermindert derdemanuscriptgebiedsdelen, en grotere controle van het het publiceren proces verleent. De DTM-bibliotheken kunnen worden gehost en beheerd via uw eigen webhosting of CDN. </p> </td> 
   <td colname="col3"> <p>Zelfhosting is de aanbevolen methode voor het laden van DTM op een pagina. Hoewel DTM-hosting via de Akamai CDN in de meeste gevallen werkt, verbetert zelforhosting de paginaprestaties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Experience Cloud ID Service - Gebruik slechts één AdobeOrg</b> </p> <p>Dikte: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>In een normale MCID-implementatie moet één AdobeOrg worden gebruikt. </p> </td> 
   <td colname="col3"> <p>Controleer of er meerdere AdobeOrg-id's bestaan voor deze implementatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - pageBottom callback-plaatsing</b> </p> <p>Dikte: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Aanvullende informatie</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>Bij starten moet als synchroon geïmplementeerd een <span class="codeph"> callback-functie </span>pageBottom als laatste in de hoofdtekst van de pagina zijn gedefinieerd </p> <p> <p>Opmerking: Het wordt aanbevolen dat de tag de <i>laatste</i> tag in de <span class="codeph"> &lt;body&gt;</span>is. Als het binnen de <span class="codeph"> &lt;body&gt;</span> markering wordt gevonden, heeft het een kans om te functioneren, maar aangezien het niet beste praktijken is, kon het verkeerd of met onverwachte of ongewenste resultaten functioneren. </p> </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript direct vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag toe voor de juiste DTM-functionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Starten - Zelfgehost</b> </p> <p>Dikte: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>De Launch-bibliotheek wordt gehost op de Akamai-instantie van Adobe op <span class="filepath"> assets.adobedtm.com</span>. </p> <p>Zelf-ontvangen is de geadviseerde benadering voor het laden van Lancering omdat het grotere controle van websiteprestaties door geheim voorgeheugencontrole, verminderend derdemanuscriptgebiedsdelen, en grotere controle van het het publiceren proces verleent. De opstartbibliotheken kunnen worden gehost en beheerd via uw eigen webhosting of CDN. </p> </td> 
   <td colname="col3"> <p>Hoewel het ontvangen van de Lancering via Akamai CDN in de meeste gevallen werkt, adviseert men dat zelf-ontvangen als eerste stap in het verbeteren van paginaprestaties wordt uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Starten - moet asynchroon worden geïmplementeerd</b> </p> <p>Dikte: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Start moet asynchroon worden geïmplementeerd voor optimale prestaties. </p> </td> 
   <td colname="col3"> <p>De asynchrone parameter opnemen in het inlinescript voor de juiste functionaliteit voor asynchrone Starten </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Doel - Inhoud in mboxDefault</b> </p> <p>Dikte: 0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De inhoud moet in mboxDefault bestaan wanneer u at.js gebruikt. </p> </td> 
   <td colname="col3"> <p>Controleer of de inhoud beschikbaar is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Configuratie {#configuration}

Deze verwijzing verstrekt meer informatie over de tests Auditor voor configuratie presteert.

De tests van de configuratie kunnen voor specifieke montages, waarden, of potentiële conflicten in uw implementatie aftasten. De controleur evalueert de markeringen tegen andere regels en geadviseerde beste praktijken.

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Conversienamen gebruiken alleen alfanumerieke tekens</b> </p> <p>Dikte: 3 </p> </td> 
   <td colname="col2"> <p>De <span class="codeph"> parameter ev_conversion_property_name</span> mag alleen numerieke en decimale waarden bevatten, BEHALVE voor de parameter "<span class="codeph"> ev_transid</span>" (de <span class="codeph"> waarde ev_transid</span> kan tekst of numerieke waarden bevatten) </p> <p>Zoek naar <span class="codeph"> pixels van het type everesttech.net</span> die een URL-parameter bevatten die begint met <span class="codeph"> ev_</span>. </p> <p>Voorbeeld: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Zorg ervoor dat de parameters van de transactieeigenschap alleen numerieke en decimale waarden bevatten. </p> <p> <p>Waarschuwing:  Andere waardetypen kunnen gegevensverlies veroorzaken. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Conversienamen gebruiken URL-veilige tekens</b> </p> <p>Dikte: 3 </p> </td> 
   <td colname="col2"> <p> Namen van conversie-eigenschappen mogen geen en-teken of vraagteken bevatten. </p> <p> Voorbeeld: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Zorg ervoor dat de parameters van de transactieeigenschap geen niet-gecodeerd en/of vraagteken bevatten. Hiermee wordt de URL-indeling verbroken. </p> <p> <p>Waarschuwing: Eigenschapparameters die een niet-gecodeerd en/of vraagteken bevatten, (bijvoorbeeld: <span class="codeph"> ev_formComplete?=1</span> of <span class="codeph"> ev_formComplete&amp;Submit=1</span>), kan leiden tot gegevensverlies. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - Transactie-id correct geïmplementeerd</b> </p> <p>Dikte: 1 </p> </td> 
   <td colname="col2"> <p> De eigenschapnaam <span class="codeph"> ev_transid=</span> mag niet leeg zijn. </p> <p>Voorbeeld: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>De eigenschapnaam <span class="codeph"> ev_transid=</span> mag niet zonder een waarde worden gelaten (<span class="codeph"> ev_transid=</span>). Als dit zonder een waarde wordt verlaten, zou er verlies van transactiegegevens kunnen zijn. Wijs een waarde toe aan <span class="codeph"> ev_transid=</span> of verwijder de parameter uit het pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - Instantiated in DOM</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De Adobe Analytics-code is niet geïnstalleerd of kan niet worden uitgevoerd. Retourneert 0 wanneer er geen analytische code op de webpagina is gevonden. </p> </td> 
   <td colname="col3"> <p>Controleer of de tag Analytics is geïmplementeerd op de pagina en niet wordt geblokkeerd door daaropvolgende scriptactiviteiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analyse - eenmaal geïnstantieerd</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De Adobe Analytics-code is meerdere keren gedetecteerd op de pagina. . Retourneert 0 wanneer er geen analytische code op de webpagina is gevonden. </p> </td> 
   <td colname="col3"> <p>Zorg ervoor dat er slechts één tag Analytics op de pagina staat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analyse - nieuwste versie</b> </p> <p>Dikte: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De meest recente versie van de Codebibliotheek Analytics wordt niet uitgevoerd op uw pagina's. Codebibliotheken die werken met de functie Experience Cloud-technologieën worden voortdurend bijgewerkt en getweend om te profiteren van prestatieverbeteringen en de nieuwste functies te bieden. Retourneert 0 wanneer er geen analytische code op de webpagina is gevonden. </p> </td> 
   <td colname="col3"> <p>Installeer de nieuwste versie van de bibliotheek Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - tags van derden worden asynchroon geladen nadat DOM gereed is</b> </p> <p>Dikte: 3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Om een evenwicht te vinden tussen een goede gebruikerservaring en het verzamelen van nauwkeurige gegevens, zouden de markeringen van de derde partij bij DOM klaar moeten teweegbrengen. Zo zorgt u ervoor dat deze volgende scripts worden uitgevoerd zonder dat dit van invloed is op de functionaliteit van de site. </p> </td> 
   <td colname="col3"> <p>Los dit probleem op door alle regels aan te passen die pixels van derden uitvoeren om bij DOM Ready te worden geactiveerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - Laatste versie</b> </p> <p>Dikte: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Uw pagina's voeren niet de nieuwste versie van de codeblok van de Bezoeker-id-service uit, <span class="codeph"> bezoekerAPI.js</span>. Codebibliotheken die werken met de functie Experience Cloud-technologieën worden voortdurend bijgewerkt en getweend om te profiteren van prestatieverbeteringen en de nieuwste functies te bieden. </p> </td> 
   <td colname="col3"> <p>Installeer de nieuwste versie van de bibliotheek met bezoekersidentiteiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Starten - Laatste versie</b> </p> <p>Dikte: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Op deze pagina's wordt niet de laatste versie van de Codebibliotheek van de Lancering (Turbine) uitgevoerd. Codebibliotheken die werken met de functie Experience Cloud-technologieën worden voortdurend bijgewerkt en getweend om te profiteren van prestatieverbeteringen en de nieuwste functies te bieden. </p> </td> 
   <td colname="col3"> <p> Werk de bibliotheek van de Lancering bij door de bibliotheek van de Lancering opnieuw op te bouwen en te publiceren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Doel - Laatste versie</b> </p> <p>Dikte: 2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De meest recente versie van de doelcodebibliotheek wordt niet uitgevoerd op uw pagina's. Codebibliotheken die werken met de functie Experience Cloud-technologieën worden voortdurend bijgewerkt en getweend om te profiteren van prestatieverbeteringen en de nieuwste functies te bieden. </p> </td> 
   <td colname="col3"> <p>Installeer de nieuwste versie van de doelbibliotheek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Doel - mboxDefault komt eerder dan mboxCreate </b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Het juiste gebruik van <span class="codeph"> mboxCreate</span> ziet er als volgt uit: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Zorg ervoor dat u een <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> -tag opneemt voordat u <span class="codeph"> mboxCreate()</span>aanroept. om.js zal geen één voor u toevoegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Doel: geldig DOCTYPE</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Er is een ongeldig DOCTYPE gedetecteerd. In dit scenario worden geen vakjes geactiveerd. </p> <p>Voor at.js, moet DOCTYPE op de wijze van Normen zijn of het Doel zal niet werken. </p> </td> 
   <td colname="col3"> <p>Werk het DOCTYPE op de pagina bij. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Codeconsistentie {#tag-consistency}

Deze verwijzing verstrekt meer informatie over de tests Auditor voor markeringsconsistentie presteert.

De consistentietests van de controleur zoeken naar inconsistenties op alle gescande pagina&#39;s. Dit zijn waarden of configuraties die voor alle pagina&#39;s op de site hetzelfde moeten zijn om nauwkeurige gegevensverzameling te garanderen.

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analyse - Consistente codeversie </b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/choose-implementation-method.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Er zijn meerdere versies van de Analytics-code gevonden. </p> </td> 
   <td colname="col3"> <p>Vervang alle instanties van Analytics door de huidige versie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tagaanwezigheid {#tag-presence}

Deze verwijzing verstrekt meer informatie over de tests Auditor voor markeringsaanwezigheid uitvoert.

De controleur evalueert of de markering bestaat, en of het op de juiste plaats in uw paginacode is.

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Cloud voor advertenties - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> </td> 
   <td colname="col2"> <p> De tag Advertising Cloud is niet beschikbaar in het DOM. </p> </td> 
   <td colname="col3"> <p>Implementeer de Cloud-tag Advertising met de Launch Extension voor Advertising. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Cloud voor adverteren - segmentpixel geïmplementeerd</b> </p> <p>Dikte: 5 </p> </td> 
   <td colname="col2"> <p> Werk de pixels van het segment Advertising Cloud bij tot de nieuwe afbeeldingstags voor Advertising Cloud. Het gebruik van verouderde AMO-segmenttags kan leiden tot gegevensverlies. </p> </td> 
   <td colname="col3"> <p>Implementeer de pixel van het Advertising Cloud-segment met de Launch Extension voor Advertising Cloud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analyse - geladen in DOM</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De tag Adobe Analytics is niet gedetecteerd. </p> </td> 
   <td colname="col3"> <p>Installeer de nieuwste versie van Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Bibliotheek geladen</b> </p> <p>Dikte: 5 </p> <p>Aanvullende informatie: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/c_Troubleshooting.html" format="html" scope="external"> DTM-probleemoplossing</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Code voor kop- en voetteksten toevoegen</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Een globaal _satelliet-object is niet gevonden in de DOM. Dynamic Tag Management is niet geïnstalleerd of kan niet worden uitgevoerd. </p> </td> 
   <td colname="col3"> <p>Controleer of de DTM-bibliotheek op de pagina is geïmplementeerd en niet wordt geblokkeerd door daaropvolgende scriptactiviteiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM - Eén insluitcode</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Productieplaatsen mogen slechts één DTM-bibliotheek laden. </p> </td> 
   <td colname="col3"> <p>Controleer of alleen de productiebibliotheek op de pagina wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - pageBottom callback bestaat in &lt;body&gt;</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De callback <span class="codeph"> _satelliet.pageBottom()</span> is niet gevonden in de <span class="codeph"> &lt;body&gt;</span> van de pagina, die vereist is voor Dynamic Tag Management. </p> <p>Deze test mislukt als de <span class="codeph"> pageBottom- </span>aanroep helemaal niet op de pagina staat of als deze in de <span class="codeph"> &lt;head&gt;</span> -tag (of een andere onverwachte locatie) staat. De waarde wordt alleen doorgegeven als pageBottom <span class="codeph"> zich ergens in de tag</span> &lt;body&gt; <span class="codeph"></span> bevindt. Als het helemaal niet op de pagina is, zal het niet functioneren en de andere twee <span class="codeph"> pageBottom</span> tests zullen ook ontbreken. </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript direct vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag toe voor de juiste DTM-functionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - pageBottom-tag geactiveerd</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De tag DTM <span class="codeph"> pageBottom</span> is niet gedetecteerd. </p> <p>Dit kan zich voordoen als de aanroep zich binnen een <span class="codeph"> if</span> -instructie bevindt die iets oplevert dat lijkt op <span class="codeph"> if (false) {_satelliet.pageBottom()}</span>. Dus, hoewel het zou kunnen bestaan en correct geplaatst zijn, zou de markering niet kunnen branden. </p> </td> 
   <td colname="col3"> <p>Installeer de DTM <span class="codeph"> pageBottom</span> vraag op elke pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-overview.htmlimplementation-guides.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Kan de code voor Experience Cloud ID Service niet vinden. De Experience Cloud ID (MCID) wordt ten zeerste aanbevolen om ervoor te zorgen dat u de meeste waarde haalt uit uw Experience Cloud-oplossingen en is essentieel voor id-beheer in verschillende Experience Cloud-oplossingen. </p> </td> 
   <td colname="col3"> <p> Installeer de meest recente versie van MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - aanwezigheid van cookie</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-implementation-guides.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Het <span class="codeph"> AMCV_</span> cookie is niet gevonden. U moet een bezoekersobject instantiëren met de code <span class="codeph"> VisitorAPI.js</span> . </p> </td> 
   <td colname="col3"> <p> Als dit een DTM-implementatie is, controleert u of de AdobeOrg-id correct is ingevoerd in de MCID-tool. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID Service - MID-waarde aanwezig</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_cookies.html#concept_37156268512445F287CD4BBB2839FFAA__section_C55AF54828DC4CCE89F6118655D694C8" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De MID-waarde is niet gevonden in het <span class="codeph"> AMCV_</span> cookie. </p> </td> 
   <td colname="col3"> <p>Test opnieuw om te controleren op een eventuele MCID API-latentie. Neem contact op met de klantenservice van Adobe als de aandoening aanhoudt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Starten - Bibliotheek geladen</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> Een globaal _satelliet-object is niet gevonden in de DOM. Starten is niet geïnstalleerd of kan niet worden uitgevoerd. </p> </td> 
   <td colname="col3"> <p>Controleer of de bibliotheek Launch op de pagina is geïmplementeerd en niet wordt geblokkeerd door volgende scriptactiviteiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Starten - Er zijn niet meerdere ingesloten scripts</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Er mogen niet meerdere insluitscripts op de pagina worden geladen. Productieplaatsen mogen slechts één opstartbibliotheek laden. </p> </td> 
   <td colname="col3"> <p>Controleer of alleen de productiebibliotheek op de pagina wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Starten - pageBottom callback bestaat in &lt;body&gt;</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p> De callback <span class="codeph"> _satelliet.pageBottom()</span> is niet gevonden binnen de <span class="codeph"> &lt;body&gt;</span> van de pagina, die is vereist voor Starten. </p> <p>Deze test mislukt als de <span class="codeph"> pageBottom- </span>aanroep helemaal niet op de pagina staat of als deze in de <span class="codeph"> &lt;head&gt;</span> -tag (of een andere onverwachte locatie) staat. De waarde wordt alleen doorgegeven als pageBottom <span class="codeph"> zich ergens in de tag</span> &lt;body&gt; <span class="codeph"></span> bevindt. Als het helemaal niet op de pagina is, zal het niet functioneren en de andere twee <span class="codeph"> pageBottom</span> tests zullen ook ontbreken. </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript direct vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag toe voor de juiste opstartfunctionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Starten - pageBottom callback zou niet moeten bestaan wanneer asynchroon opgesteld</b> </p> <p>Dikte: 5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>De callback <span class="codeph"> _satelliet.pageBottom()</span> is gevonden op de pagina. Dit zou niet het geval moeten zijn wanneer Launch asynchroon wordt geïmplementeerd. </p> </td> 
   <td colname="col3"> <p>Verwijder het<span class="codeph"> script _satelliet.pageBottom()</span> om de juiste opstartfunctionaliteit in te schakelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Doel - Code-aanwezigheid</b> </p> <p>Dikte: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Aanvullende informatie</a> </p> </td> 
   <td colname="col2"> <p>Doel moet worden gedefinieerd in het DOM. </p> </td> 
   <td colname="col3"> <p>Installeer de meest recente versie van Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Doel - Bibliotheek geladen in &lt;head&gt;</b> </p> <p>Dikte: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Aanvullende informatie</a> </p> 
    <draft-comment>
      TE61c380082a4b4706b28a84aa047599a7 
    </draft-comment> </td> 
   <td colname="col2"> <p> De doelbibliotheek moet in de tag <span class="codeph"> &lt;head&gt;</span> worden geladen. </p> </td> 
   <td colname="col3"> <p> Controleer of de doelbibliotheek in de tag <span class="codeph"> &lt;head&gt;</span> is geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>
