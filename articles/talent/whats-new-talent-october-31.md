---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (31. oktober 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
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
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "858796"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="c8088-103">Hva er nytt eller endret i Dynamics 365 for Talent Core HR (31. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="c8088-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8088-104">**Build 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="c8088-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="c8088-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="c8088-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="c8088-106">Opprette koblinger fra Talent til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8088-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="c8088-107">Med den nye navigeringsfunksjonaliteten kan du koble fra Talent til Finance and Operations, noe som gir deg direkte navigasjon til Finance and Operations-sider.</span><span class="sxs-lookup"><span data-stu-id="c8088-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="c8088-108">Når koblinger er konfigurert, kan du angi navnet og gruppen for koblingen, hvor koblingen skal vises i Talent, og målsiden som skal åpnes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8088-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="c8088-109">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="c8088-109">Coming soon</span></span>
<span data-ttu-id="c8088-110">Feltkontekst legges til i fremtiden for å tillate direkte navigasjon til tilsvarende poster i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8088-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="c8088-111">Du kan for eksempel bruke **Kobling til felt** for å gi kontekst for å navigere direkte til en bestemt ansatt eller posisjon i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8088-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="c8088-112">Konfigurer målsystemer</span><span class="sxs-lookup"><span data-stu-id="c8088-112">Configure target systems</span></span>

<span data-ttu-id="c8088-113">I Talent kan systemansvarlige definere koblinger som skal vises gjennom arbeidsområdet for systemadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="c8088-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="c8088-114">En del av konfigurasjonen er Finance and Operations-miljøene som du vil navigere til som "mål" for koblingen.</span><span class="sxs-lookup"><span data-stu-id="c8088-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="c8088-115">Du kan gjøre dette ved å gi systemet et navn og oppgi URL-adressen for Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="c8088-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="c8088-116">Her er et eksempel på en Finance and Operations-URL-adresse som du kunne angitt: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="c8088-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="c8088-117">Når du har konfigurert målsystemene dine, kan du definere koblingene.</span><span class="sxs-lookup"><span data-stu-id="c8088-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="c8088-118">Konfigurer koblinger</span><span class="sxs-lookup"><span data-stu-id="c8088-118">Configure links</span></span>

<span data-ttu-id="c8088-119">Hver kobling som opprettes, har følgende informasjon definert.</span><span class="sxs-lookup"><span data-stu-id="c8088-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="c8088-120">Kobling – navnet på koblingen, brukes bare til identifikasjon.</span><span class="sxs-lookup"><span data-stu-id="c8088-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="c8088-121">Aktiver denne koblingen – satt til **Ja** hvis du vil vise koblingen til brukere av Talent.</span><span class="sxs-lookup"><span data-stu-id="c8088-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="c8088-122">Visningsnavn – definerer navnet som vises som en kobling til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8088-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="c8088-123">Disse dataene er for øyeblikket ikke er oversatt.</span><span class="sxs-lookup"><span data-stu-id="c8088-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="c8088-124">Overflatekobling i skjema – velg hvilken side du vil vise koblingen på.</span><span class="sxs-lookup"><span data-stu-id="c8088-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="c8088-125">Gruppe – Grupper er ikke obligatoriske, men hvis du vil organisere koblingene ved hjelp av grupper, velger du en eksisterende gruppe eller oppretter en ny med **Gruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c8088-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="c8088-126">Målsystem – Velg målsystemet som ble opprettet ved hjelp av alternativet **Konfigurer målsystem**.</span><span class="sxs-lookup"><span data-stu-id="c8088-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="c8088-127">Dette blir Finance and Operations-miljøet som skal brukes når du navigerer via koblingen.</span><span class="sxs-lookup"><span data-stu-id="c8088-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="c8088-128">Bruk brukerens gjeldende firma – Velg **Ja** hvis du vil bruke brukerens gjeldende firmakontekst når du navigerer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8088-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="c8088-129">Hvis **Nei** er valgt, kan du velge firmaet som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="c8088-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="c8088-130">Element på målmeny – Angi menyelementet fra Finance and Operation som koblingen skal bruke ved navigering.</span><span class="sxs-lookup"><span data-stu-id="c8088-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="c8088-131">Menyelementer som du kan navigere direkte til, er tilgjenglige.</span><span class="sxs-lookup"><span data-stu-id="c8088-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="c8088-132">For å åpne det påkrevde menyelementet åpner du Finance and Operations og åpner siden som er målet for navigasjonen.</span><span class="sxs-lookup"><span data-stu-id="c8088-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="c8088-133">Kopier menyelementet fra URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="c8088-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="c8088-134">Hvis du for eksempel vil at koblingen skal gå til ansattlisten i Finance and Operations, angir du verdien som vises etter "&mi" i URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="c8088-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="c8088-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="c8088-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="c8088-136">Menyelementet for å navigere til siden for ansattlisten i dette eksemplet, er: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="c8088-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="c8088-137">Koble til datakilde – Velg kilden til dataene som koblingen refererer til.</span><span class="sxs-lookup"><span data-stu-id="c8088-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="c8088-138">De vanligste kildene som **Arbeider** og **Posisjon** er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="c8088-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="c8088-139">Kobling til felt – (kommer snart) Dette feltvalget tillater direkte navigasjon fra én enkelt post i Talent til én enkelt post i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8088-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="c8088-140">Tilgang til koblinger</span><span class="sxs-lookup"><span data-stu-id="c8088-140">Access to links</span></span>

<span data-ttu-id="c8088-141">Systemansvarlige vil se de nylig opprettede koblingene på de definerte sidene, selv om alternativet **Aktiver denne koblingen** er satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="c8088-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="c8088-142">Dette kan brukes til å teste koblinger før de vises til andre ansatte.</span><span class="sxs-lookup"><span data-stu-id="c8088-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="c8088-143">Alle andre roller vil bare se de konfigurerte koblingene når alternativet **Aktiver denne koblingen** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c8088-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="c8088-144">Ansatte som har tilgang til sidene der koblingene vises, vil ha tilgang til koblingene.</span><span class="sxs-lookup"><span data-stu-id="c8088-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="c8088-145">Brukere kan også ha definert sikkerhetsrettigheter i Finance and Operations for å få tilgang til sidene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8088-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="c8088-146">Hvis ikke vises en sikkerhetsdialogboks når koblingen brukes.</span><span class="sxs-lookup"><span data-stu-id="c8088-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="c8088-147">Andre endringer/reparasjoner</span><span class="sxs-lookup"><span data-stu-id="c8088-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="c8088-148">Stillinger med en fremtidig startdato kan ikke tilordnes til en ny ansatt</span><span class="sxs-lookup"><span data-stu-id="c8088-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="c8088-149">Det er gjort endringer for å tillatte ansattilordninger til stillinger med dato i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="c8088-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="c8088-150">Stillinger som har startdatoer i fremtiden, kan velges, og ansattilordningen utføres ved lagring eller fullføring av arbeidsflyten (hvis arbeidsflyten er aktivert).</span><span class="sxs-lookup"><span data-stu-id="c8088-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="c8088-151">Ny ansatt kan ikke tilordnes eksisterende stilling</span><span class="sxs-lookup"><span data-stu-id="c8088-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="c8088-152">Det er gjort endringer, slik at ny ansattilordning nå kan tilordnes eksisterende stillinger.</span><span class="sxs-lookup"><span data-stu-id="c8088-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="c8088-153">Ansiennitetsdato/kontoradresse forsvinner når startdatoen for ansettelsen er passert, og posten blir lagret</span><span class="sxs-lookup"><span data-stu-id="c8088-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="c8088-154">Endringer er gjort for å rette synligheten for **Ansiennitetsdato** og **Kontoradresse** under lagring av endringer for tidligere ansatte.</span><span class="sxs-lookup"><span data-stu-id="c8088-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="c8088-155">Kan ikke angi data for ansettelser med dato i fremtiden på arbeidersiden</span><span class="sxs-lookup"><span data-stu-id="c8088-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="c8088-156">Ansettelsesdata for ansettelser med dato i fremtiden er deaktivert på hovedsiden for arbeider.</span><span class="sxs-lookup"><span data-stu-id="c8088-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="c8088-157">Ansettelsesdata kan angis på sidene **Datobehandling**.</span><span class="sxs-lookup"><span data-stu-id="c8088-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="c8088-158">Andre endringer vil bli gjort i fremtidige versjoner for å gjøre det mulig å registrere ansettelsesdata direkte under arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="c8088-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="c8088-159">Legg til ValidFrom og ValidTo i HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="c8088-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="c8088-160">DMF-enheten (Data Management Framework) HcmPersonalContactPersonEntity er oppdatert for å inkludere "gyldig fra"- og "gyldig til"- datoer for å aktivere bestemte fordelsintegreringsscenarier.</span><span class="sxs-lookup"><span data-stu-id="c8088-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="c8088-161">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="c8088-161">Known issue</span></span>
- <span data-ttu-id="c8088-162">**Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene.</span><span class="sxs-lookup"><span data-stu-id="c8088-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="c8088-163">**Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket.</span><span class="sxs-lookup"><span data-stu-id="c8088-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c8088-164">Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert.</span><span class="sxs-lookup"><span data-stu-id="c8088-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="c8088-165">(Dette problemet vil bli løst i neste plattformoppdatering.)</span><span class="sxs-lookup"><span data-stu-id="c8088-165">(This issue will be fixed in the next platform update.)</span></span>
