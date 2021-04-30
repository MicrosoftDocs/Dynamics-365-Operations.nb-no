---
title: Optimaliser virtuelle Dataverse-tabellspørringer
description: Optimalisere og feilsøke ytelsen til virtuelle Dataverse-tabellspørringer
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8026abd5c3e0f9b78e8c016731fd7785490bc945
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891108"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="22bba-103">Optimaliser virtuelle Dataverse-tabellspørringer</span><span class="sxs-lookup"><span data-stu-id="22bba-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="22bba-104">Problem</span><span class="sxs-lookup"><span data-stu-id="22bba-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="22bba-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="22bba-105">Overview</span></span>

<span data-ttu-id="22bba-106">Når du bruker virtuelle Dataverse-tabeller til å utvikle integreringer og andre datatilkoblinger med Dynamics 365 Human Resources, kan du oppleve ytelsesproblemer med spørringer mot de virtuelle tabellene.</span><span class="sxs-lookup"><span data-stu-id="22bba-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="22bba-107">Treg kjøring av spørring kan forekomme på tvers av forskjellige klienter eller grensesnitt.</span><span class="sxs-lookup"><span data-stu-id="22bba-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="22bba-108">Du kan for eksempel oppleve dette i følgende tilfeller:</span><span class="sxs-lookup"><span data-stu-id="22bba-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="22bba-109">Ved spørringer av en virtuell tabell via Dataverse Web-API</span><span class="sxs-lookup"><span data-stu-id="22bba-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="22bba-110">Når du oppretter en Power App-app mot en virtuell tabell</span><span class="sxs-lookup"><span data-stu-id="22bba-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="22bba-111">Når en Power BI-rapport bygges opp i en virtuell tabell</span><span class="sxs-lookup"><span data-stu-id="22bba-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="22bba-112">Ytelsesproblemet kan oppstå i alle disse grensesnittene.</span><span class="sxs-lookup"><span data-stu-id="22bba-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="22bba-113">En årsak til treg ytelse med virtuelle Dataverse-tabeller for Human Resources er sekundærnøkkelkolonnene i den virtuelle tabellen som er relatert til tabellens [navigasjonsegenskaper](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span><span class="sxs-lookup"><span data-stu-id="22bba-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="22bba-114">Når navigasjonsegenskaper opprettes for en virtuell tabell, legges en sekundærnøkkelkolonne automatisk til i tabellen for å representere verdien til nøkkelen for den relaterte virtuelle tabellens nøkkelkolonne.</span><span class="sxs-lookup"><span data-stu-id="22bba-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="22bba-115">For eksempel blir kolonnen **_mshr_fk_person_id_value** lagt til i enheten **mshr_hcmworkerbaseentity** med sekundærnøkkelegenskapen fra enheten **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="22bba-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="22bba-116">På grunn av hvordan verdiene for disse sekundærnøkkelkolonnene vedlikeholdes i en tabell, kan henting av verdiene ha negativ virkning på ytelsen til en spørring mot den virtuelle tabellen.</span><span class="sxs-lookup"><span data-stu-id="22bba-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="22bba-117">Potensielle symptomer</span><span class="sxs-lookup"><span data-stu-id="22bba-117">Potential symptoms</span></span>

<span data-ttu-id="22bba-118">Et eksempel der du kan se denne innvirkningen, er i spørringer mot Arbeider-enheten (**mshr_hcmworkerentity**) eller Basisarbeider-enheten (**mshr_hcmworkerbaseentity**).</span><span class="sxs-lookup"><span data-stu-id="22bba-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="22bba-119">Det kan hende at du ytelsesproblemet manifesterer seg selg på noen måter:</span><span class="sxs-lookup"><span data-stu-id="22bba-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="22bba-120">**Treg spørringsutførelse:** Spørringen mot den virtuelle tabellen kan returnere de forventede resultatene, men ta lengre tid enn forventet for å fullføre utføringen av spørringen.</span><span class="sxs-lookup"><span data-stu-id="22bba-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="22bba-121">**Tidsavbrudd for spørring:** Spørringen kan tidsavbrudd og returnere følgende feil: "Et token ble hentet for å kalle Finance and Operations, men Finance and Operations returnerte en feil av typen InternalServerError."</span><span class="sxs-lookup"><span data-stu-id="22bba-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="22bba-122">**Uventet feil**: Spørringen kan returnere feiltype 400 med følgende melding: "Det oppstod en uventet feil."</span><span class="sxs-lookup"><span data-stu-id="22bba-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Feiltype 400 på HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="22bba-124">**Begrensning**: Spørringen kan overbruke serverressurser og blir underlagt begrensning.</span><span class="sxs-lookup"><span data-stu-id="22bba-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="22bba-125">I dette tilfellet returnerer spørringen følgende feil: "Et token ble hentet for å kalle Finance and Operations, men Finance and Operations returnerte en feil av type 429".</span><span class="sxs-lookup"><span data-stu-id="22bba-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="22bba-126">Hvis du vil ha mer informasjon om begrensning i Human Resources, kan du se [Vanlige spørsmål om begrensning](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="22bba-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Feiltype 429 på HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="22bba-128">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="22bba-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="22bba-129">Begrens antall kolonner som er inkludert i dataspørringen</span><span class="sxs-lookup"><span data-stu-id="22bba-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="22bba-130">Ved hjelp av virtuelle tabeller er en av metodene som har flest muligheter til å forbedre spørringsytelsen, å begrense antall kolonner som er valgt i spørringen.</span><span class="sxs-lookup"><span data-stu-id="22bba-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="22bba-131">De generelle retningslinjene for optimalisering av spørringsytelse er å begrense kolonnene som returneres i spørringen, til bare de egenskapene du trenger.</span><span class="sxs-lookup"><span data-stu-id="22bba-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="22bba-132">Dette gjelder spesielt sekundærnøkkelkolonnene i virtuelle tabeller.</span><span class="sxs-lookup"><span data-stu-id="22bba-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="22bba-133">Hvis du ikke trenger verdiene i sekundærnøkkelkolonnene for integreringen eller rapporten, strukturerer du deretter spørringen for å velge bare kolonnene du trenger, unntatt sekundærnøkkelkolonnene.</span><span class="sxs-lookup"><span data-stu-id="22bba-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="22bba-134">Velge kolonner i en OData-spørring</span><span class="sxs-lookup"><span data-stu-id="22bba-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="22bba-135">Når du spør en virtuell tabell via Dataverse Web-API, kan du begrense antall kolonner som er inkludert i spørringen ved å bruke **$select** for systemspørring og definere kolonnene du trenger returnert resultater for.</span><span class="sxs-lookup"><span data-stu-id="22bba-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="22bba-136">Hvis du vil maksimere ytelsen, utelater du sekundærnøkkelkolonner (kolonner med **_mshr_FK_**-prefikset) fra spørringen.</span><span class="sxs-lookup"><span data-stu-id="22bba-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="22bba-137">Følgende spørring mot enheten **mshr_hcmworkerbaseentity** vil for eksempel bare inkludere kolonnene som er inkludert i **$select**-spørringsalternativsetningen, med sekundærnøkkelverdier utelatt.</span><span class="sxs-lookup"><span data-stu-id="22bba-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="22bba-138">Dette gir betydelige forbedringer i ytelsen for en spørring som inkluderer alle tabellkolonner.</span><span class="sxs-lookup"><span data-stu-id="22bba-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="22bba-139">Anbefalingen for å begrense antall kolonner som velges, gjelder også når du bruker spørringsalternativet **$expand** for å utvide spørringen til relaterte virtuelle tabeller ved hjelp av navigasjonsegenskaper.</span><span class="sxs-lookup"><span data-stu-id="22bba-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="22bba-140">Spørringen nedenfor inneholder for eksempel kolonner fra enheten **mshr_hcmworkerbaseentity** med utvidede kolonner fra enheten **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="22bba-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="22bba-141">Legg merke til at spørringsalternativet **$select** også er inkludert i **$expand**-spørringsalternativsetningen.</span><span class="sxs-lookup"><span data-stu-id="22bba-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="22bba-142">Når du bruker denne metoden for å hente data med **$select**-spørringsalternativet i **$expand** -spørringsalternativsetningen, opplever du vanligvis større ytelsesforbedringer når navigasjonsegenskapen mellom enhetene er en mange-til-én-relasjon.</span><span class="sxs-lookup"><span data-stu-id="22bba-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="22bba-143">Det kan hende at du ikke ser samme reduksjonen i utførelsestiden for spørringen når du utvider en én-til-mange-relasjon.</span><span class="sxs-lookup"><span data-stu-id="22bba-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="22bba-144">Hvis du vil ha mer informasjon om relasjonsdefinisjon for virtuelle Dataverse-tabeller, kan du se [Tabellrelasjoner](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="22bba-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="22bba-145">Hvis du vil ha mer informasjon om bruk av systemspørringsalternativene **$select** og **$expand** i Dataverse Web-API, kan du se [Hente relaterte enhetsoppføringer med en spørring](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="22bba-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="22bba-146">Velge kolonner i Power BI</span><span class="sxs-lookup"><span data-stu-id="22bba-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="22bba-147">Hvis du opplever noen av indikasjonene nevnt ovenfor på treg ytelse når du bygger en Power BI-rapport mot en virtuell Dataverse-tabell, kan du forbedre ytelsen ved å utelate sekundærnøkkelkolonner fra kolonnene som er valgt fra tabellen, for rapporten.</span><span class="sxs-lookup"><span data-stu-id="22bba-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="22bba-148">Hvis du for eksempel bruker Power BI Desktop til å opprette en rapport mot **mshr_hcmworkerbaseentity**-enheten, kan du bruke fremgangsmåten nedenfor for å velge kolonnene du vil ha med i rapportspørringen.</span><span class="sxs-lookup"><span data-stu-id="22bba-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="22bba-149">I Power BI Desktop, velg **Mer ...** fra rullegardinlisten **Hent data** på handlingsbåndet.</span><span class="sxs-lookup"><span data-stu-id="22bba-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="22bba-150">I **Hent data**-vinduet angir du **Common Data Service** i søkeboksen, velger **Common Data Service**-koblingen og velger deretter **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="22bba-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="22bba-151">I feltet **Server-URL** i Common Data Service-vinduet angir du organisasjons-URI-en for Dataverse-miljøet, og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="22bba-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Angi URI-en for Dataverse-miljøet](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="22bba-153">Utvid **Enheter**-noden i navigasjonsvinduet.</span><span class="sxs-lookup"><span data-stu-id="22bba-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="22bba-154">I søkeboksen angir du **mshr_hcmworkerbaseentity** og velger deretter enheten.</span><span class="sxs-lookup"><span data-stu-id="22bba-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="22bba-155">Velg **Transformer data**.</span><span class="sxs-lookup"><span data-stu-id="22bba-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="22bba-156">I vinduet i Power Query-redigering velger du **Avansert redigering**.</span><span class="sxs-lookup"><span data-stu-id="22bba-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="22bba-157">I vinduet **Avansert redigering** oppdaterer du spørringen slik at den ser ut som den nedenfor, ved å legge til eller fjerne kolonner fra matrisen etter behov.</span><span class="sxs-lookup"><span data-stu-id="22bba-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Oppdater spørringen i Avansert redigering for Power Query-redigering](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="22bba-159">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="22bba-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="22bba-160">Hvis du tidligere mottok en feil av type 429 fra spørringen før oppdatering, kan det hende at du må vente på perioden for nye forsøk før du oppdaterer spørringen for at den skal fullføres etterfølgende.</span><span class="sxs-lookup"><span data-stu-id="22bba-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="22bba-161">Klikk **Lukk og bruk** på handlingsbåndet i Power Query -redigering.</span><span class="sxs-lookup"><span data-stu-id="22bba-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="22bba-162">Deretter kan du begynne å bygge Power BI-rapportenmot kolonnene som er valgt i den virtuelle tabellen.</span><span class="sxs-lookup"><span data-stu-id="22bba-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="22bba-163">Velge kolonner i Power Apps</span><span class="sxs-lookup"><span data-stu-id="22bba-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="22bba-164">På samme måte som for Dataverse Web-API-spørringer og Power BI kan du forbedre spørringsytelsen for for Power Apps basert på virtuelle Dataverse-tabeller ved å utelate kolonner i relaterte tabeller fra appen.</span><span class="sxs-lookup"><span data-stu-id="22bba-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="22bba-165">Hvis en kolonne fra en relatert tabell er inkludert på en side, vil forespørsels-URL-adressen som er bygd for å hente dataene, inneholde sekundærnøkkelegenskapene til den relaterte tabellen.</span><span class="sxs-lookup"><span data-stu-id="22bba-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="22bba-166">Dette, som i eksemplene for [Velge kolonner i en OData-spørring](#selecting-columns-in-power-apps) ovenfor, reduserer ytelsen ved å forårsake flere dataoppslag.</span><span class="sxs-lookup"><span data-stu-id="22bba-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="22bba-167">Du omgå dette ved å validere at ingen datafelt fra relaterte tabeller er inkludert i en hvilken som helst dataform i Power App-appen.</span><span class="sxs-lookup"><span data-stu-id="22bba-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="22bba-168">Velg dataskjemaet for skjermen i trevisningsruten.</span><span class="sxs-lookup"><span data-stu-id="22bba-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="22bba-169">I **Egenskaper**-ruten velger du **Rediger** under **Felter**-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="22bba-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="22bba-170">I **Data**-ruten kontrollerer du at ingen av de valgte feltene er felter i den virtuelle tabellen til datakilden.</span><span class="sxs-lookup"><span data-stu-id="22bba-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="22bba-171">Hvis for eksempel ett av datafeltene som er inkludert på en side i appen, refererer til en annen tabell, for eksempel **ThisItem.Worker.Name**, der **Arbeider** er relatert tabell, er det fare for redusert ytelse når dataene hentes.</span><span class="sxs-lookup"><span data-stu-id="22bba-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="22bba-172">Du kan bruke [Power Apps-skjerm](/powerapps/maker/monitor-overview) til å sørge for at bare kolonnene du trenger, blir inkludert i spørringen for å hende dataene for Power App-appen.</span><span class="sxs-lookup"><span data-stu-id="22bba-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="22bba-173">Du kan vise URL-adressen som er bygd for getRows-operasjonen, for å sikre at kolonnene du har valgt for appen, blir optimale for å hente dataene.</span><span class="sxs-lookup"><span data-stu-id="22bba-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Bruk Power Apps-skjerm til å analysere getData-operasjonen.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="22bba-175">Filtrere dataspørringen</span><span class="sxs-lookup"><span data-stu-id="22bba-175">Filtering the data query</span></span>

<span data-ttu-id="22bba-176">En annen metode for å forbedre ytelsen for spørringsutførelse er å begrense antall poster som returneres i spørringsresultatene.</span><span class="sxs-lookup"><span data-stu-id="22bba-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="22bba-177">Du kan gjøre dette ved å filtrere resultatene for å sikre at du bare mottar postene du trenger.</span><span class="sxs-lookup"><span data-stu-id="22bba-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="22bba-178">Se [Filtrere resultater](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) hvis du vil ha mer informasjon om hvordan du filtrerer spørringsdata.</span><span class="sxs-lookup"><span data-stu-id="22bba-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="22bba-179">Begrense sidestørrelsen til spørringen</span><span class="sxs-lookup"><span data-stu-id="22bba-179">Limiting the page size of the query</span></span>

<span data-ttu-id="22bba-180">Hvis du arbeider med store datasett, kan du dele spørringsresultater inn i flere sider ved å legge til `odata.maxpagesize`-egenskapshodet i dataspørringer.</span><span class="sxs-lookup"><span data-stu-id="22bba-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="22bba-181">Hvis du vil ha mer informasjon om sideveksling, kan du se [Angi antall enheter som skal returneres på en side](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="22bba-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="22bba-182">Se også</span><span class="sxs-lookup"><span data-stu-id="22bba-182">See also</span></span>

- [<span data-ttu-id="22bba-183">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="22bba-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="22bba-184">Vanlige spørsmål om virtuelle tabeller for Human Resources</span><span class="sxs-lookup"><span data-stu-id="22bba-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="22bba-185">Vanlige spørsmål om begrensning</span><span class="sxs-lookup"><span data-stu-id="22bba-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]