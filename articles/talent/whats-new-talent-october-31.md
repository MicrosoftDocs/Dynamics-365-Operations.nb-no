---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (31. oktober 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
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
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897379"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a><span data-ttu-id="0a999-103">Hva er nytt eller endret i Dynamics 365 Talent – Core HR (31. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="0a999-103">What's new or changed in Dynamics 365 Talent - Core HR (October 31, 2018)</span></span>

<span data-ttu-id="0a999-104">**Build 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="0a999-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="0a999-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="0a999-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance"></a><span data-ttu-id="0a999-106">Opprette koblinger fra Talent til Finance</span><span class="sxs-lookup"><span data-stu-id="0a999-106">Create links from Talent to Finance</span></span>
<span data-ttu-id="0a999-107">Med den nye navigeringsfunksjonaliteten kan du koble fra Talent til Finance, noe som gir deg direkte navigasjon til Finance-sider.</span><span class="sxs-lookup"><span data-stu-id="0a999-107">This new navigation functionality allows you to link from Talent to Finance, giving you direct navigation into Finance pages.</span></span> <span data-ttu-id="0a999-108">Når koblinger er konfigurert, kan du angi navnet og gruppen for koblingen, hvor koblingen skal vises i Talent, og målsiden som skal åpnes i Finance.</span><span class="sxs-lookup"><span data-stu-id="0a999-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="0a999-109">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="0a999-109">Coming soon</span></span>
<span data-ttu-id="0a999-110">Feltkontekst legges til i fremtiden for å tillate direkte navigasjon til tilsvarende poster i Finance.</span><span class="sxs-lookup"><span data-stu-id="0a999-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance.</span></span> <span data-ttu-id="0a999-111">Du kan for eksempel bruke **Kobling til felt** for å gi kontekst for å navigere direkte til en bestemt ansatt eller posisjon i Finance.</span><span class="sxs-lookup"><span data-stu-id="0a999-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="0a999-112">Konfigurer målsystemer</span><span class="sxs-lookup"><span data-stu-id="0a999-112">Configure target systems</span></span>

<span data-ttu-id="0a999-113">I Talent kan systemansvarlige definere koblinger som skal vises gjennom arbeidsområdet for systemadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="0a999-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="0a999-114">En del av konfigurasjonen er Finance-miljøene som du vil navigere til som "mål" for koblingen.</span><span class="sxs-lookup"><span data-stu-id="0a999-114">Part of the configuration is the Finance environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="0a999-115">Du kan gjøre dette ved å gi systemet et navn og oppgi URL-adressen for Finance-miljøet.</span><span class="sxs-lookup"><span data-stu-id="0a999-115">You do this by giving the target system a name and providing the URL of the Finance environment.</span></span> <span data-ttu-id="0a999-116">Her er et eksempel på en Finance-URL-adresse som du kunne angitt: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="0a999-116">Here is an example of a Finance URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="0a999-117">Når du har konfigurert målsystemene dine, kan du definere koblingene.</span><span class="sxs-lookup"><span data-stu-id="0a999-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="0a999-118">Konfigurer koblinger</span><span class="sxs-lookup"><span data-stu-id="0a999-118">Configure links</span></span>

<span data-ttu-id="0a999-119">Hver kobling som opprettes, har følgende informasjon definert.</span><span class="sxs-lookup"><span data-stu-id="0a999-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="0a999-120">Kobling – navnet på koblingen, brukes bare til identifikasjon.</span><span class="sxs-lookup"><span data-stu-id="0a999-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="0a999-121">Aktiver denne koblingen – satt til **Ja** hvis du vil vise koblingen til brukere av Talent.</span><span class="sxs-lookup"><span data-stu-id="0a999-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="0a999-122">Visningsnavn – definerer navnet som vises som en kobling til Finance.</span><span class="sxs-lookup"><span data-stu-id="0a999-122">Display name - Define the name that will appear as a link to Finance.</span></span> <span data-ttu-id="0a999-123">Disse dataene er for øyeblikket ikke er oversatt.</span><span class="sxs-lookup"><span data-stu-id="0a999-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="0a999-124">Overflatekobling i skjema – velg hvilken side du vil vise koblingen på.</span><span class="sxs-lookup"><span data-stu-id="0a999-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="0a999-125">Gruppe – Grupper er ikke obligatoriske, men hvis du vil organisere koblingene ved hjelp av grupper, velger du en eksisterende gruppe eller oppretter en ny med **Gruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0a999-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="0a999-126">Målsystem – Velg målsystemet som ble opprettet ved hjelp av alternativet **Konfigurer målsystem**.</span><span class="sxs-lookup"><span data-stu-id="0a999-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="0a999-127">Dette blir Finance-miljøet som skal brukes når du navigerer via koblingen.</span><span class="sxs-lookup"><span data-stu-id="0a999-127">This will be the Finance environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="0a999-128">Bruk brukerens gjeldende firma – Velg **Ja** hvis du vil bruke brukerens gjeldende firmakontekst når du navigerer til Finance.</span><span class="sxs-lookup"><span data-stu-id="0a999-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance.</span></span> <span data-ttu-id="0a999-129">Hvis **Nei** er valgt, kan du velge firmaet som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="0a999-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="0a999-130">Element på målmeny – Angi menyelementet fra Finance som koblingen skal bruke ved navigering.</span><span class="sxs-lookup"><span data-stu-id="0a999-130">Target menu item - Enter the menu item from Finance that the link should use when navigating.</span></span> <span data-ttu-id="0a999-131">Menyelementer som du kan navigere direkte til, er tilgjenglige.</span><span class="sxs-lookup"><span data-stu-id="0a999-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="0a999-132">For å åpne det påkrevde menyelementet åpner du Finance og åpner siden som er målet for navigasjonen.</span><span class="sxs-lookup"><span data-stu-id="0a999-132">To find the menu item required, open Finance and open the page that is the target of the navigation.</span></span> <span data-ttu-id="0a999-133">Kopier menyelementet fra URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="0a999-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="0a999-134">Hvis du for eksempel vil at koblingen skal gå til ansattlisten i Finance and Operations, angir du verdien som vises etter "&mi" i URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="0a999-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="0a999-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="0a999-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="0a999-136">Menyelementet for å navigere til siden for ansattlisten i dette eksemplet, er: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="0a999-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="0a999-137">Koble til datakilde – Velg kilden til dataene som koblingen refererer til.</span><span class="sxs-lookup"><span data-stu-id="0a999-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="0a999-138">De vanligste kildene som **Arbeider** og **Posisjon** er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="0a999-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="0a999-139">Kobling til felt – (kommer snart) Dette feltvalget tillater direkte navigasjon fra én enkelt post i Talent til én enkelt post i Finance.</span><span class="sxs-lookup"><span data-stu-id="0a999-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="0a999-140">Tilgang til koblinger</span><span class="sxs-lookup"><span data-stu-id="0a999-140">Access to links</span></span>

<span data-ttu-id="0a999-141">Systemansvarlige vil se de nylig opprettede koblingene på de definerte sidene, selv om alternativet **Aktiver denne koblingen** er satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="0a999-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="0a999-142">Dette kan brukes til å teste koblinger før de vises til andre ansatte.</span><span class="sxs-lookup"><span data-stu-id="0a999-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="0a999-143">Alle andre roller vil bare se de konfigurerte koblingene når alternativet **Aktiver denne koblingen** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0a999-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="0a999-144">Ansatte som har tilgang til sidene der koblingene vises, vil ha tilgang til koblingene.</span><span class="sxs-lookup"><span data-stu-id="0a999-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="0a999-145">Brukere kan også ha definert sikkerhetsrettigheter i Finance for å få tilgang til sidene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0a999-145">Users can also have security rights within Finance defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="0a999-146">Hvis ikke vises en sikkerhetsdialogboks når koblingen brukes.</span><span class="sxs-lookup"><span data-stu-id="0a999-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="0a999-147">Andre endringer/reparasjoner</span><span class="sxs-lookup"><span data-stu-id="0a999-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="0a999-148">Stillinger med en fremtidig startdato kan ikke tilordnes til en ny ansatt</span><span class="sxs-lookup"><span data-stu-id="0a999-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="0a999-149">Det er gjort endringer for å tillatte ansattilordninger til stillinger med dato i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="0a999-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="0a999-150">Stillinger som har startdatoer i fremtiden, kan velges, og ansattilordningen utføres ved lagring eller fullføring av arbeidsflyten (hvis arbeidsflyten er aktivert).</span><span class="sxs-lookup"><span data-stu-id="0a999-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="0a999-151">Ny ansatt kan ikke tilordnes eksisterende stilling</span><span class="sxs-lookup"><span data-stu-id="0a999-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="0a999-152">Det er gjort endringer, slik at ny ansattilordning nå kan tilordnes eksisterende stillinger.</span><span class="sxs-lookup"><span data-stu-id="0a999-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="0a999-153">Ansiennitetsdato/kontoradresse forsvinner når startdatoen for ansettelsen er passert, og posten blir lagret</span><span class="sxs-lookup"><span data-stu-id="0a999-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="0a999-154">Endringer er gjort for å rette synligheten for **Ansiennitetsdato** og **Kontoradresse** under lagring av endringer for tidligere ansatte.</span><span class="sxs-lookup"><span data-stu-id="0a999-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="0a999-155">Kan ikke angi data for ansettelser med dato i fremtiden på arbeidersiden</span><span class="sxs-lookup"><span data-stu-id="0a999-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="0a999-156">Ansettelsesdata for ansettelser med dato i fremtiden er deaktivert på hovedsiden for arbeider.</span><span class="sxs-lookup"><span data-stu-id="0a999-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="0a999-157">Ansettelsesdata kan angis på sidene **Datobehandling**.</span><span class="sxs-lookup"><span data-stu-id="0a999-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="0a999-158">Andre endringer vil bli gjort i fremtidige versjoner for å gjøre det mulig å registrere ansettelsesdata direkte under arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="0a999-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="0a999-159">Legg til ValidFrom og ValidTo i HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="0a999-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="0a999-160">DMF-enheten (Data Management Framework) HcmPersonalContactPersonEntity er oppdatert for å inkludere "gyldig fra"- og "gyldig til"- datoer for å aktivere bestemte fordelsintegreringsscenarier.</span><span class="sxs-lookup"><span data-stu-id="0a999-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="0a999-161">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="0a999-161">Known issue</span></span>
- <span data-ttu-id="0a999-162">**Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene.</span><span class="sxs-lookup"><span data-stu-id="0a999-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="0a999-163">**Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket.</span><span class="sxs-lookup"><span data-stu-id="0a999-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="0a999-164">Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert.</span><span class="sxs-lookup"><span data-stu-id="0a999-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="0a999-165">(Dette problemet vil bli løst i neste plattformoppdatering.)</span><span class="sxs-lookup"><span data-stu-id="0a999-165">(This issue will be fixed in the next platform update.)</span></span>
