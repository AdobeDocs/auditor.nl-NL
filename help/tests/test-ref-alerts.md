---
description: Deze naslaggids bevat meer informatie over de waarschuwingen die Adobe Experience Platform Auditor weergeeft voor tests.
seo-description: Deze naslaggids bevat meer informatie over de waarschuwingen die Adobe Experience Platform Auditor weergeeft voor tests.
seo-title: Waarschuwingen
title: Waarschuwingen
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 1%

---


# Waarschuwingen{#alerts}

Deze naslaggids bevat meer informatie over de waarschuwingen die Adobe Experience Platform Auditor weergeeft voor tests.

Waarschuwingen tonen problemen waarvan je op de hoogte moet zijn, maar die geen invloed hebben op je score. Dit zijn aanbevelingen voor best practices die in sommige gevallen niet van toepassing zijn op uw implementatie.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Criteria </th> 
   <th colname="col3" class="entry"> Aanbeveling </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Correct geïmplementeerde omzettingstag</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Controleer of de juiste conversietag wordt gebruikt. </p> <p> <p>Waarschuwing:  Het gebruik van verouderde conversietags voor TubeMogul kan gegevensverlies tot gevolg hebben. </p> </p> </td> 
   <td colname="col3"> <p>Voer een upgrade uit op de conversiepixels naar de nieuwe Advertising Cloud-tags voor conversie van alleen afbeeldingen. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor Adobe Experience Platform Launch worden verwezenlijkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - JS-tag corrigeren gebruikt</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud moet de nieuwste JavaScript-tags gebruiken. </p> </td> 
   <td colname="col3"> <p>Upgrade uw Advertising Cloud JavaScript naar de nieuwste versie. Als u de verouderde JavaScript-versies gebruikt, kan de functionaliteit verloren gaan. </p> <p>Dit kan gemakkelijker door het gebruik van de uitbreiding van Advertising Cloud voor de Lancering van het Platform worden verwezenlijkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Tag met alleen afbeelding</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>De Advertising Cloud-indeling voor afbeeldingspixels moet overeenkomen met een van de volgende aanbevolen indelingen: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Upgrade uw Advertising Cloud-pixels naar de nieuwe Advertising Cloud-tags voor alleen afbeeldingen, zodat u de volledige Advertising Cloud-functionaliteit kunt benutten. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor de Lancering van het Platform worden verwezenlijkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Segmentpixels DSP synchroniseren ingeschakeld</b> </p> <p>Dikte: 0 </p> </td> 
   <td colname="col2"> <p>Controleer of de TubeMogul-segmentpixel een DSP-instelling bevat en adviseer dat de instelling aan de pixel wordt toegevoegd. </p> <p>De instelling DSP synchroniseren wordt bepaald door het gebruik van een parameter voor een queryreeks, dus </p> <p>ALS de tag wordt geactiveerd naar<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;")</span> </p> <p> OF <span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> OF <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>EN de tag bevat de URL-parameter <span class="codeph"> "sid=")</span> </p> <p>Controleer VERVOLGENS of de URL-parameter <span class="codeph"> "cs=0"</span> of<span class="codeph"> "cs=1"</span> bestaat en adviseer, als dit niet het geval is, dat <span class="codeph"> "cs=1"</span> aan die pixels wordt toegevoegd zodat de overeenkomende frequenties van de doelgroep kunnen worden verbeterd. </p> </td> 
   <td colname="col3"> <p> Voeg de URL-parameter <span class="codeph"> "cs=1"</span> toe aan uw Advertising Cloud-pixels, zodat DSP synchroniseren kan plaatsvinden, waardoor de overeenkomende frequenties voor de doelgroep toenemen. </p> <p>Dit kan het gemakkelijkst met de uitbreiding van Advertising Cloud voor de Lancering van het Platform worden verwezenlijkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    --> <p><b>DTM - pageBottom callback-plaatsing</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Extra informatie</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamisch tagbeheer vereist de functie <span class="codeph"> _satelliet.pageBottom()</span> . Voeg het inlinescript direct vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag toe voor de juiste DTM-functionaliteit. </p> <p> <p>Opmerking: Het wordt aanbevolen dat de tag de <i>laatste</i> tag in de <span class="codeph"> &lt;body&gt;</span>is. Als het binnen de <span class="codeph"> &lt;body&gt;</span> markering wordt gevonden, heeft het een kans om te functioneren, maar aangezien het niet beste praktijken is, kon het verkeerd of met onverwachte of ongewenste resultaten functioneren. </p> </p> </td> 
   <td colname="col3"> <p>Voeg het inlinescript direct vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag toe voor de juiste DTM-functionaliteit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - zelfgehoste</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Extra informatie</a> </p> </td> 
   <td colname="col2"> <p> De DTM-bibliotheek Akamai wordt gehost op <span class="filepath"> assets.adobedtm.com</span>. </p> <p> Zelf hosten is de geadviseerde benadering voor het laden van DTM omdat het grotere controle van websiteprestaties door geheim voorgeheugencontrole, vermindert derdemanuscriptgebiedsdelen, en grotere controle van het het publiceren proces verleent. De DTM-bibliotheken kunnen worden gehost en beheerd via uw eigen webhosting of CDN. </p> </td> 
   <td colname="col3"> <p>Zelfhosting is de aanbevolen methode voor het laden van DTM op een pagina. Hoewel DTM-hosting via de Akamai CDN in de meeste gevallen werkt, verbetert zelforhosting de paginaprestaties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Experience Cloud ID-service - Gebruik slechts één AdobeOrg</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/id-request.html" format="html" scope="external"> Extra informatie</a> </p> </td> 
   <td colname="col2"> <p>In een normale MCID-implementatie moet één AdobeOrg worden gebruikt. </p> </td> 
   <td colname="col3"> <p>Controleer of er meerdere AdobeOrg-id's bestaan voor deze implementatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - pageBottom callback-plaatsing</b> </p> <p>Dikte: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Extra informatie</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>Bij starten van Platform moet de <span class="codeph"> callbackfunctie </span>pageBottom als laatste in de hoofdtekst van de pagina zijn gedefinieerd, als deze synchroon wordt geïmplementeerd. </p> <p> <p>Opmerking: Het wordt aanbevolen dat de tag de <i>laatste</i> tag in de <span class="codeph"> &lt;body&gt;</span>is. Als het binnen de <span class="codeph"> &lt;body&gt;</span> markering wordt gevonden, heeft het een kans om te functioneren, maar aangezien het niet beste praktijken is, kon het verkeerd of met onverwachte of ongewenste resultaten functioneren. </p> </p> </td> 
   <td colname="col3"> <p>Bij starten van Platform is de functie <span class="codeph"> _satelliet.pageBottom()</span> vereist voor synchrone implementaties. Voeg het inline script toe vlak vóór de afsluitende <span class="codeph"> &lt;/body&gt;</span> -tag om de juiste functionaliteit voor starten van Platforms te garanderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Starten - Zelfgehost</b> </p> <p>Dikte: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Aan de slag met Adobe Experience Platform Launch</a> </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/reference/client-side-info/asynchronous-deployment.html" format="https" scope="external"> Asynchrone implementatie van Platform starten</a> </p> </td> 
   <td colname="col2"> <p>Het Platform starten wordt gehost op Adobe Akamai-instantie op <span class="filepath"> assets.adobedtm.com</span>. </p> <p>Zelf-ontvangen is de geadviseerde benadering voor het laden van de Lancering van het Platform omdat het grotere controle van websiteprestaties door geheim voorgeheugencontrole, verminderend derdemanuscriptgebiedsdelen, en grotere controle van het het publiceren proces verleent. De bibliotheken van de Lancering van het Platform kunnen door uw eigen Web worden ontvangen en worden beheerd die of CDN. </p> </td> 
   <td colname="col3"> <p>Hoewel het ontvangen van de Lancering van het Platform via Akamai CDN in de meeste gevallen werkt, adviseert men dat zelf-ontvangen als eerste stap in het verbeteren van paginaprestaties wordt uitgevoerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Starten - moet asynchroon worden geïmplementeerd</b> </p> <p>Dikte: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Extra informatie</a> </p> </td> 
   <td colname="col2"> <p>De Lancering van het Platform zou asynchroon voor optimale prestaties moeten worden opgesteld. </p> </td> 
   <td colname="col3"> <p>De asynchrone parameter opnemen in het inlinescript voor de juiste functionaliteit voor het starten van het asynchrone Platform </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Doel - Inhoud in mboxDefault</b> </p> <p>Dikte: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Extra informatie</a> </p> </td> 
   <td colname="col2"> <p> De inhoud moet in mboxDefault bestaan wanneer u at.js gebruikt. </p> </td> 
   <td colname="col3"> <p>Controleer of de inhoud beschikbaar is. </p> </td> 
  </tr> 
 </tbody> 
</table>

