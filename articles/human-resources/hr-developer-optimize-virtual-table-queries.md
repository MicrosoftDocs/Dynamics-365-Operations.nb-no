---
title: Optimaliser virtuelle Dataverse-tabellspørringer
description: Optimalisere og feilsøke ytelsen til virtuelle Dataverse-tabellspørringer
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f75176781620cd6f845c002876eba6e34d5793e7
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692233"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Optimaliser virtuelle Dataverse-tabellspørringer


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Problem

### <a name="overview"></a>Oversikt

Når du bruker virtuelle Dataverse-tabeller til å utvikle integreringer og andre datatilkoblinger med Dynamics 365 Human Resources, kan du oppleve ytelsesproblemer med spørringer mot de virtuelle tabellene. Treg kjøring av spørring kan forekomme på tvers av forskjellige klienter eller grensesnitt. Du kan for eksempel oppleve dette i følgende tilfeller:

- Ved spørringer av en virtuell tabell via Dataverse Web-API
- Når du oppretter en Power App-app mot en virtuell tabell
- Når en Power BI-rapport bygges opp i en virtuell tabell

Ytelsesproblemet kan oppstå i alle disse grensesnittene.

En årsak til treg ytelse med virtuelle Dataverse-tabeller for Human Resources er sekundærnøkkelkolonnene i den virtuelle tabellen som er relatert til tabellens [navigasjonsegenskaper](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties). Når navigasjonsegenskaper opprettes for en virtuell tabell, legges en sekundærnøkkelkolonne automatisk til i tabellen for å representere verdien til nøkkelen for den relaterte virtuelle tabellens nøkkelkolonne. For eksempel blir kolonnen **_mshr_fk_person_id_value** lagt til i enheten **mshr_hcmworkerbaseentity** med sekundærnøkkelegenskapen fra enheten **mshr_dirpersonentity**. På grunn av hvordan verdiene for disse sekundærnøkkelkolonnene vedlikeholdes i en tabell, kan henting av verdiene ha negativ virkning på ytelsen til en spørring mot den virtuelle tabellen.

### <a name="potential-symptoms"></a>Potensielle symptomer

Et eksempel der du kan se denne innvirkningen, er i spørringer mot Arbeider-enheten (**mshr_hcmworkerentity**) eller Basisarbeider-enheten (**mshr_hcmworkerbaseentity**). Det kan hende at du ytelsesproblemet manifesterer seg selg på noen måter:

- **Treg spørringsutførelse:** Spørringen mot den virtuelle tabellen kan returnere de forventede resultatene, men ta lengre tid enn forventet for å fullføre utføringen av spørringen.
- **Tidsavbrudd for spørring**: Spørringen kan bli tidsavbrutt og returnere følgende feil: "Et token ble hentet for å kalle økonomi og drift, men økonomi og drift returnerte en feil av typen InternalServerError."
- **Uventet feil**: Spørringen kan returnere feiltype 400 med følgende melding: "Det oppstod en uventet feil."

  ![Feiltype 400 på HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **Begrensning**: Spørringen kan overbruke serverressurser og blir underlagt begrensning. I dette tilfellet returnerer spørringen følgende feil: "Et token ble hentet for å kalle økonomi og drift, men økonomi og drift returnerte en feil av type 429." Hvis du vil ha mer informasjon om begrensning i Human Resources, kan du se [Vanlige spørsmål om begrensning](./hr-admin-integration-throttling-faq.md).

  ![Feiltype 429 på HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Løsning

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Begrens antall kolonner som er inkludert i dataspørringen

Ved hjelp av virtuelle tabeller er en av metodene som har flest muligheter til å forbedre spørringsytelsen, å begrense antall kolonner som er valgt i spørringen. De generelle retningslinjene for optimalisering av spørringsytelse er å begrense kolonnene som returneres i spørringen, til bare de egenskapene du trenger. Dette gjelder spesielt sekundærnøkkelkolonnene i virtuelle tabeller. Hvis du ikke trenger verdiene i sekundærnøkkelkolonnene for integreringen eller rapporten, strukturerer du deretter spørringen for å velge bare kolonnene du trenger, unntatt sekundærnøkkelkolonnene.

#### <a name="selecting-columns-in-an-odata-query"></a>Velge kolonner i en OData-spørring

Når du spør en virtuell tabell via Dataverse Web-API, kan du begrense antall kolonner som er inkludert i spørringen ved å bruke **$select** for systemspørring og definere kolonnene du trenger returnert resultater for. Hvis du vil maksimere ytelsen, utelater du sekundærnøkkelkolonner (kolonner med **_mshr_FK_**-prefikset) fra spørringen.

Følgende spørring mot enheten **mshr_hcmworkerbaseentity** vil for eksempel bare inkludere kolonnene som er inkludert i **$select**-spørringsalternativsetningen, med sekundærnøkkelverdier utelatt. Dette gir betydelige forbedringer i ytelsen for en spørring som inkluderer alle tabellkolonner.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Anbefalingen for å begrense antall kolonner som velges, gjelder også når du bruker spørringsalternativet **$expand** for å utvide spørringen til relaterte virtuelle tabeller ved hjelp av navigasjonsegenskaper. Spørringen nedenfor inneholder for eksempel kolonner fra enheten **mshr_hcmworkerbaseentity** med utvidede kolonner fra enheten **mshr_dirpersonentity**. Legg merke til at spørringsalternativet **$select** også er inkludert i **$expand**-spørringsalternativsetningen.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Når du bruker denne metoden for å hente data med **$select**-spørringsalternativet i **$expand** -spørringsalternativsetningen, opplever du vanligvis større ytelsesforbedringer når navigasjonsegenskapen mellom enhetene er en mange-til-én-relasjon. Det kan hende at du ikke ser samme reduksjonen i utførelsestiden for spørringen når du utvider en én-til-mange-relasjon. Hvis du vil ha mer informasjon om relasjonsdefinisjon for virtuelle Dataverse-tabeller, kan du se [Tabellrelasjoner](/powerapps/maker/data-platform/create-edit-entity-relationships).

Hvis du vil ha mer informasjon om bruk av systemspørringsalternativene **$select** og **$expand** i Dataverse Web-API, kan du se [Hente relaterte enhetsoppføringer med en spørring](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Velge kolonner i Power BI

Hvis du opplever noen av indikasjonene nevnt ovenfor på treg ytelse når du bygger en Power BI-rapport mot en virtuell Dataverse-tabell, kan du forbedre ytelsen ved å utelate sekundærnøkkelkolonner fra kolonnene som er valgt fra tabellen, for rapporten. Hvis du for eksempel bruker Power BI Desktop til å opprette en rapport mot **mshr_hcmworkerbaseentity**-enheten, kan du bruke fremgangsmåten nedenfor for å velge kolonnene du vil ha med i rapportspørringen.

1. I Power BI Desktop, velg **Mer ...** fra rullegardinlisten **Hent data** på handlingsbåndet.
2. I **Hent data**-vinduet angir du **Common Data Service** i søkeboksen, velger **Common Data Service**-koblingen og velger deretter **Koble til**.
3. I feltet **Server-URL** i Common Data Service-vinduet angir du organisasjons-URI-en for Dataverse-miljøet, og velger **OK**.
  
   ![Angi URI-en for Dataverse-miljøet.](./media/PowerBIDataverseURLSetup.png)
  
4. Utvid **Enheter**-noden i navigasjonsvinduet.
5. I søkeboksen angir du **mshr_hcmworkerbaseentity** og velger deretter enheten.
6. Velg **Transformer data**.
7. I vinduet i Power Query-redigering velger du **Avansert redigering**.
8. I vinduet **Avansert redigering** oppdaterer du spørringen slik at den ser ut som den nedenfor, ved å legge til eller fjerne kolonner fra matrisen etter behov.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Oppdater spørringen i Avansert redigering for Power Query-redigering.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Velg **Ferdig**.

   > [!NOTE]
   > Hvis du tidligere mottok en feil av type 429 fra spørringen før oppdatering, kan det hende at du må vente på perioden for nye forsøk før du oppdaterer spørringen for at den skal fullføres etterfølgende.

10. Klikk på **Lukk og bruk** på handlingsbåndet i Power Query-redigering.

Deretter kan du begynne å bygge Power BI-rapportenmot kolonnene som er valgt i den virtuelle tabellen.

#### <a name="selecting-columns-in-power-apps"></a>Velge kolonner i Power Apps

På samme måte som for Dataverse Web-API-spørringer og Power BI kan du forbedre spørringsytelsen for for Power Apps basert på virtuelle Dataverse-tabeller ved å utelate kolonner i relaterte tabeller fra appen. Hvis en kolonne fra en relatert tabell er inkludert på en side, vil forespørsels-URL-adressen som er bygd for å hente dataene, inneholde sekundærnøkkelegenskapene til den relaterte tabellen. Dette, som i eksemplene for [Velge kolonner i en OData-spørring](#selecting-columns-in-power-apps) ovenfor, reduserer ytelsen ved å forårsake flere dataoppslag.

Du omgå dette ved å validere at ingen datafelt fra relaterte tabeller er inkludert i en hvilken som helst dataform i Power App-appen.

1. Velg dataskjemaet for skjermen i trevisningsruten.
2. I **Egenskaper**-ruten velger du **Rediger** under **Felter**-egenskapen.
3. I **Data**-ruten kontrollerer du at ingen av de valgte feltene er felter i den virtuelle tabellen til datakilden.

Hvis for eksempel ett av datafeltene som er inkludert på en side i appen, refererer til en annen tabell, for eksempel **ThisItem.Worker.Name**, der **Arbeider** er relatert tabell, er det fare for redusert ytelse når dataene hentes.

Du kan bruke [Power Apps-skjerm](/powerapps/maker/monitor-overview) til å sørge for at bare kolonnene du trenger, blir inkludert i spørringen for å hende dataene for Power App-appen. Du kan vise URL-adressen som er bygd for getRows-operasjonen, for å sikre at kolonnene du har valgt for appen, blir optimale for å hente dataene.

![Bruk Power Apps-skjerm til å analysere getData-operasjonen.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Filtrere dataspørringen

En annen metode for å forbedre ytelsen for spørringsutførelse er å begrense antall poster som returneres i spørringsresultatene. Du kan gjøre dette ved å filtrere resultatene for å sikre at du bare mottar postene du trenger.

Se [Filtrere resultater](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) hvis du vil ha mer informasjon om hvordan du filtrerer spørringsdata.

### <a name="limiting-the-page-size-of-the-query"></a>Begrense sidestørrelsen til spørringen

Hvis du arbeider med store datasett, kan du dele spørringsresultater inn i flere sider ved å legge til `odata.maxpagesize`-egenskapshodet i dataspørringer.

Hvis du vil ha mer informasjon om sideveksling, kan du se [Angi antall enheter som skal returneres på en side](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Se også

- [Konfigurere virtuelle Dataverse-tabeller](hr-admin-integration-common-data-service-virtual-entities.md)
- [Vanlige spørsmål om virtuelle tabeller for Human Resources](hr-admin-virtual-entity-faq.md)
- [Vanlige spørsmål om begrensning](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
