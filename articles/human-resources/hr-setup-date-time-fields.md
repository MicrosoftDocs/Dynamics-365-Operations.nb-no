---
title: Forstå dato- og klokkeslettfelt
description: Forstå hva du kan forvente når du bruker dato- og klokkeslettfelt i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 924d7369129d4115d45f23864e7b851d318c52a4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467367"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="2f0a4-103">Forstå felt for dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="2f0a4-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2f0a4-104">**Dato og klokkeslett**-felt er et grunnleggende begrep i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2f0a4-105">Det er viktig å forstå hvordan du arbeider med **Dato og klokkeslett**-data i skjemaer, Dataverse og eksterne kilder.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="2f0a4-106">Forstå forskjellen mellom datatypene Dato- og Dato og klokkeslett-felt</span><span class="sxs-lookup"><span data-stu-id="2f0a4-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="2f0a4-107">**Dato og klokkeslett**-felt inneholder tidssoneinformasjon, mens **Dato**-felt ikke gjør det.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="2f0a4-108">**Dato**-felt viser den samme informasjonen på et hvilket som helst sted.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="2f0a4-109">Når du angir en dato i et **Dato**-felt, skriver Human Resources den samme datoen til databasen.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="2f0a4-110">Når du viser data i et **Dato og klokkeslett**-felt, justerer Human Resources datoen og klokkeslettet basert på brukerens tidssone som er angitt i **Brukeralternativer**-skjemaet (**Felles > Oppsett > Brukeralternativer**).</span><span class="sxs-lookup"><span data-stu-id="2f0a4-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="2f0a4-111">Dato- og klokkeslettinformasjonen du angir i feltet, er kanskje ikke lik informasjonen som er skrevet til databasen.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="2f0a4-112">[![Brukeralternativer-skjema](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="2f0a4-113">Forstå Dato og klokkeslett-felt i skjemaer</span><span class="sxs-lookup"><span data-stu-id="2f0a4-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="2f0a4-114">**Dato og klokkeslett**-data som vises på skjermen, er ikke de samme som dataene som er lagret i databasen hvis brukerens tidssone ikke er satt til UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="2f0a4-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="2f0a4-115">Data i **Dato og klokkeslett**-felt lagres alltid som UTC.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="2f0a4-116">[![Arbeiderskjema UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="2f0a4-117">Forstå Dato og klokkeslett-felt i databasen</span><span class="sxs-lookup"><span data-stu-id="2f0a4-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="2f0a4-118">Når Human Resources skriver en **Dato og klokkeslett**-verdi til databasen, lagres dataene i UTC.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="2f0a4-119">Dermed kan brukerne se alle **Dato og klokkeslett**-data i forhold til tidssonen som er definert i deres brukeralternativer.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="2f0a4-120">I eksemplet ovenfor er starttidspunktet et tidspunkt, ikke en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="2f0a4-121">Ved å endre tidssonen til den påloggede brukeren fra GMT + 12:00 til GMT UTC, vil den samme posten vise 04/30/2019 12:00:00 i stedet for 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="2f0a4-122">I eksemplet nedenfor blir ansettelsen til ansatt 000724 aktiv på samme tid uavhengig av tidssonen.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="2f0a4-123">Den ansatte vil være aktiv 04/30/2019 i GMT-tidssonen, som er det samme som 05/01/2019 i GMT+12:00-tidssonen.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="2f0a4-124">Begge refererer til samme tidspunkt og ikke en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="2f0a4-125">[![Arbeiderskjema GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="2f0a4-126">Dato og klokkeslett-data i Data Management Framework, Excel, Dataverse og Power BI</span><span class="sxs-lookup"><span data-stu-id="2f0a4-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="2f0a4-127">Data Management Framework, Excel-tillegget, Dataverse og Power BI-rapportering er alle utformet for å samhandle med data direkte på databasenivået.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="2f0a4-128">Siden det ikke finnes noen klient til å justere **Dato og klokkeslett**-data til tidssonen for brukeren, er alle **Dato og klokkeslett**-verdier i UTC, noe som kan føre til noen feilaktige antakelser når du registrerer eller viser data.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="2f0a4-129">**Dato og klokkeslett**-data som sendes via DMF, Excel eller Dataverse, antas å være i UTC av databasen.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="2f0a4-130">Dette kan føre til litt forvirring når den sendte **Dato og klokkeslett**-verdien ikke vises som forventet fordi brukeren som viser dataene, ikke har sin brukertidssone satt til UTC.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="2f0a4-131">Det samme kan skje motsatt når data eksporteres.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="2f0a4-132">**Dato og klokkeslett**-dataene i den eksporterte DMF-enheten kan være forskjellige fra det som vises i Dynamics-klienten.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="2f0a4-133">Når du bruker eksterne kilder som DMF til å vise eller redigere data, må du huske på at **Dato og klokkeslett**-verdiene anses som standard å være i UTC, uavhengig av tidssonen til brukerens datamaskin eller deres gjeldende innstillinger for brukertidssone.</span><span class="sxs-lookup"><span data-stu-id="2f0a4-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="2f0a4-134">Eksempler på samme post som vises i forskjellige produktområder</span><span class="sxs-lookup"><span data-stu-id="2f0a4-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="2f0a4-135">**Human Resources med brukertidssone satt til UTC**</span><span class="sxs-lookup"><span data-stu-id="2f0a4-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="2f0a4-136">[![Arbeiderskjema satt til UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="2f0a4-137">**Human Resources med brukertidssone satt til GMT + 12:00**</span><span class="sxs-lookup"><span data-stu-id="2f0a4-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="2f0a4-138">[![Arbeiderskjema satt til GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="2f0a4-139">**Excel via OData**</span><span class="sxs-lookup"><span data-stu-id="2f0a4-139">**Excel Via OData**</span></span>

<span data-ttu-id="2f0a4-140">[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="2f0a4-141">**DMF-oppsamling**</span><span class="sxs-lookup"><span data-stu-id="2f0a4-141">**DMF Staging**</span></span>

<span data-ttu-id="2f0a4-142">[![DMF-oppsamling](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="2f0a4-143">**DMF-eksport**</span><span class="sxs-lookup"><span data-stu-id="2f0a4-143">**DMF Export**</span></span>

<span data-ttu-id="2f0a4-144">[![DMF-eksport](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="2f0a4-145">**Excel via Dataverse**</span><span class="sxs-lookup"><span data-stu-id="2f0a4-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="2f0a4-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="2f0a4-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="2f0a4-147">Se også</span><span class="sxs-lookup"><span data-stu-id="2f0a4-147">See also</span></span>

[<span data-ttu-id="2f0a4-148">Dato og klokkeslett-data</span><span class="sxs-lookup"><span data-stu-id="2f0a4-148">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="2f0a4-149">Brukerforetrukkede tidssoner</span><span class="sxs-lookup"><span data-stu-id="2f0a4-149">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]