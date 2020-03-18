---
description: Deze verwijzing verstrekt meer informatie over de tests Auditor voor configuratie presteert.
seo-description: Deze verwijzing verstrekt meer informatie over de tests Auditor voor configuratie presteert.
seo-title: Configuratie
title: Configuratie
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Configuratie

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
    </draft-comment> <p><b>Starten - Laatste versie</b> </p> <p>Dikte: 2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Aanvullende informatie</a> </p> </td> 
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
