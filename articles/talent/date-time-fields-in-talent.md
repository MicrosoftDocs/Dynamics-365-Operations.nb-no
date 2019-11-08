---
title: Arbeide med dato og klokkeslett i Microsoft Dynamics 365 Talent
description: Forstå hva du kan forvente når du bruker dato- og klokkeslettfelt i Microsoft Dynamics 365 Talent. Få klarhet i hva du kan forvente når du samhandler med dato- og klokkeslettdata i et skjema i Talent, en ekstern kilde eller Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: abd215243cbda68ba3f57b5fa41054a10745d11f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551032"
---
# <a name="work-with-date-and-time-in-microsoft-dynamics-365-talent"></a><span data-ttu-id="a87ac-104">Arbeide med dato og klokkeslett i Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="a87ac-104">Work with date and time in Microsoft Dynamics 365 Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a87ac-105">**Dato og klokkeslett**-felt er et grunnleggende begrep i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="a87ac-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Talent.</span></span> <span data-ttu-id="a87ac-106">Det er viktig å forstå hvordan du arbeider med **Dato og klokkeslett**-data i et Dynamics 365-skjema, Common Data Service og eksterne kilder.</span><span class="sxs-lookup"><span data-stu-id="a87ac-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="a87ac-107">Forstå forskjellen mellom datatypene Dato- og Dato og klokkeslett-felt</span><span class="sxs-lookup"><span data-stu-id="a87ac-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="a87ac-108">**Dato og klokkeslett**-felt inneholder tidssoneinformasjon, mens **Dato**-felt ikke gjør det.</span><span class="sxs-lookup"><span data-stu-id="a87ac-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="a87ac-109">**Dato**-felt viser den samme informasjonen på et hvilket som helst sted.</span><span class="sxs-lookup"><span data-stu-id="a87ac-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="a87ac-110">Når du angir en dato i et **Dato**-felt, skriver Talent den samme datoen til databasen.</span><span class="sxs-lookup"><span data-stu-id="a87ac-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="a87ac-111">Når du viser data i et **Dato og klokkeslett**-felt, justerer Talent datoen og klokkeslettet basert på brukerens tidssone som er angitt i **Brukeralternativer**-skjemaet (**Felles > Oppsett > Brukeralternativer**).</span><span class="sxs-lookup"><span data-stu-id="a87ac-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="a87ac-112">Dato- og klokkeslettinformasjonen du angir i feltet, er kanskje ikke lik informasjonen som er skrevet til databasen.</span><span class="sxs-lookup"><span data-stu-id="a87ac-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="a87ac-113">[![Brukeralternativer-skjema](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="a87ac-114">Forstå Dato og klokkeslett-felt i skjemaer</span><span class="sxs-lookup"><span data-stu-id="a87ac-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="a87ac-115">Når du angir data i et **Dato og klokkeslett**-felt, er ikke dataene som vises på skjermen, de samme som dataene som er lagret i databasen hvis brukerens tidssone ikke er satt til UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="a87ac-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="a87ac-116">Data i **Dato og klokkeslett**-felt lagres alltid som UTC.</span><span class="sxs-lookup"><span data-stu-id="a87ac-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="a87ac-117">[![Arbeider-skjema](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="a87ac-118">Forstå Dato og klokkeslett-felt i databasen</span><span class="sxs-lookup"><span data-stu-id="a87ac-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="a87ac-119">Når Talent skriver en **Dato og klokkeslett**-verdi til databasen, lagres dataene i UTC.</span><span class="sxs-lookup"><span data-stu-id="a87ac-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="a87ac-120">Dermed kan brukerne se alle **Dato og klokkeslett**-data i forhold til tidssonen som er definert i deres brukeralternativer.</span><span class="sxs-lookup"><span data-stu-id="a87ac-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="a87ac-121">I eksemplet ovenfor er starttidspunktet et tidspunkt, ikke en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="a87ac-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="a87ac-122">Ved å endre tidssonen til den påloggede brukeren fra GMT + 12:00 til GMT UTC, vil den samme posten som nettopp ble opprettet, vise 04/30/2019 12:00:00 i stedet for 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="a87ac-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="a87ac-123">I eksemplet nedenfor blir ansettelsen til ansatt 000724 aktiv på samme tid uavhengig av tidssonen.</span><span class="sxs-lookup"><span data-stu-id="a87ac-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="a87ac-124">Den ansatte vil være aktiv 04/30/2019 i GMT-tidssonen, som er det samme som 05/01/2019 i GMT+12:00-tidssonen.</span><span class="sxs-lookup"><span data-stu-id="a87ac-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="a87ac-125">Begge refererer til samme tidspunkt og ikke en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="a87ac-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="a87ac-126">[![Arbeider-skjema](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="a87ac-127">Dato og klokkeslett-data i Data Management Framework, Excel, Common Data Service og Power BI</span><span class="sxs-lookup"><span data-stu-id="a87ac-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="a87ac-128">Data Management Framework, Excel-tillegget, Common Data Service og Power BI-rapportering er alle utformet for å samhandle med data direkte på databasenivået.</span><span class="sxs-lookup"><span data-stu-id="a87ac-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="a87ac-129">Siden det ikke finnes noen klient til å justere **Dato og klokkeslett**-data til tidssonen for brukeren, er alle **Dato og klokkeslett**-verdier i UTC, noe som kan føre til noen feilaktige antakelser når du registrerer eller viser data.</span><span class="sxs-lookup"><span data-stu-id="a87ac-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="a87ac-130">**Dato og klokkeslett**-data som sendes via DMF, Excel eller Common Data Service, antas å være i UTC av databasen.</span><span class="sxs-lookup"><span data-stu-id="a87ac-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="a87ac-131">Dette kan føre til litt forvirring når den sendte **Dato og klokkeslett**-verdien ikke vises som forventet fordi brukeren som viser dataene, ikke har sin brukertidssone satt til UTC.</span><span class="sxs-lookup"><span data-stu-id="a87ac-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="a87ac-132">Det samme kan skje motsatt når data eksporteres.</span><span class="sxs-lookup"><span data-stu-id="a87ac-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="a87ac-133">**Dato og klokkeslett**-dataene i den eksporterte DMF-enheten kan være forskjellige fra det som vises i Dynamics-klienten.</span><span class="sxs-lookup"><span data-stu-id="a87ac-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="a87ac-134">Når du bruker eksterne kilder som DMF til å vise eller redigere data, er det viktig å huske på at **Dato og klokkeslett**-verdiene anses som standard å være i UTC, uavhengig av tidssonen til brukerens datamaskin eller deres gjeldende innstillinger for brukertidssone.</span><span class="sxs-lookup"><span data-stu-id="a87ac-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="a87ac-135">Eksempler på samme post som vises i forskjellige produktområder</span><span class="sxs-lookup"><span data-stu-id="a87ac-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="a87ac-136">**Talent med brukertidssone satt til UTC**</span><span class="sxs-lookup"><span data-stu-id="a87ac-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="a87ac-137">[![Arbeider-skjema](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="a87ac-138">**Talent med brukertidssone satt til GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="a87ac-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="a87ac-139">[![Arbeider-skjema](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="a87ac-140">**Excel via OData**</span><span class="sxs-lookup"><span data-stu-id="a87ac-140">**Excel Via OData**</span></span>

<span data-ttu-id="a87ac-141">[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="a87ac-142">**DMF-oppsamling**</span><span class="sxs-lookup"><span data-stu-id="a87ac-142">**DMF Staging**</span></span>

<span data-ttu-id="a87ac-143">[![DMF-oppsamling](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="a87ac-144">**DMF-eksport**</span><span class="sxs-lookup"><span data-stu-id="a87ac-144">**DMF Export**</span></span>

<span data-ttu-id="a87ac-145">[![DMF-oppsamling](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="a87ac-146">**Excel via Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="a87ac-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="a87ac-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="a87ac-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="a87ac-148">Se også</span><span class="sxs-lookup"><span data-stu-id="a87ac-148">See also</span></span>

[<span data-ttu-id="a87ac-149">Dato og klokkeslett-data</span><span class="sxs-lookup"><span data-stu-id="a87ac-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="a87ac-150">Brukerforetrukkede tidssoner</span><span class="sxs-lookup"><span data-stu-id="a87ac-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
