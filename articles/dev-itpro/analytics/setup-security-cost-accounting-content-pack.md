---
title: Konfigurere sikkerhet for Kostnadsregnskapsanalyse-innhold for Power BI
description: "Dette emnet forklarer hvordan du kan overføre tilgangsnivåsikkerhet i Kostnadsregnskap til radnivåsikkerhet i Microsoft Power BI. Denne funksjonaliteten lar brukere bare se Power BI-data som de har tilgang til."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 86de46818abc6ea653076c2a6f38c40bbaab18d8
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="b3681-104">Konfigurere sikkerhet for Kostnadsregnskapsanalyse-innhold for Power BI</span><span class="sxs-lookup"><span data-stu-id="b3681-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3681-105">Dette emnet forklarer hvordan du kan overføre tilgangsnivåsikkerhet i Kostnadsregnskap til radnivåsikkerhet i Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="b3681-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="b3681-106">Denne funksjonaliteten lar brukere bare se Power BI-data som de har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="b3681-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

<a name="overview"></a><span data-ttu-id="b3681-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b3681-107">Overview</span></span>
--------

<span data-ttu-id="b3681-108">**Kostregnskapsanalyse**-innholdet for Microsoft Power BI bruker Power BI-radnivåsikkerhet til å begrense brukertilgangen.</span><span class="sxs-lookup"><span data-stu-id="b3681-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="b3681-109">Sikkerheten er basert på organisasjonshierarkiet for tilgangsnivå som er definert i parametere for kostnadsregnskapet.</span><span class="sxs-lookup"><span data-stu-id="b3681-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="b3681-110">Hvis du vil ha mer informasjon om **Kostregnskapsanalyse**-innhold for Power BI, kan du se [Kostnadsregnskapsanalyse-innhold for Power BI](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="b3681-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="b3681-111">Konfigurer</span><span class="sxs-lookup"><span data-stu-id="b3681-111">Setup</span></span>
<span data-ttu-id="b3681-112">For å overføre tilgangsnivåsikkerhet til Power BI må eieren av Power BI-innholdet følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b3681-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span> <span data-ttu-id="b3681-113">**Obs!** Brukeren som publiserer **Kostregnskapsanalyse**-innholdet for Power BI blir automatisk eieren.</span><span class="sxs-lookup"><span data-stu-id="b3681-113">**Note:** The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="b3681-114">Bare en eier kan konfigurere sikkerhet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="b3681-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="b3681-115">Før en eier legger til andre brukere på PowerBI.com, kan ingen unntatt eieren se alle dataene i Power BI-innholdet **Kostnadsregnskapsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="b3681-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1.  <span data-ttu-id="b3681-116">Publisere definisjonsfilen til Power BI.</span><span class="sxs-lookup"><span data-stu-id="b3681-116">Publish the definition file to Power BI.</span></span>
2.  <span data-ttu-id="b3681-117">Logg på PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="b3681-117">Sign in to PowerBI.com.</span></span>
3.  <span data-ttu-id="b3681-118">Finn datasettet for **Kostnadsregnskapsanalyse**-innhold for Power BI.</span><span class="sxs-lookup"><span data-stu-id="b3681-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4.  <span data-ttu-id="b3681-119">Åpne sikkerhetssiden.</span><span class="sxs-lookup"><span data-stu-id="b3681-119">Open the security page.</span></span> 

    ![Åpne sikkerhetssiden](./media/CA-picture-1.png)

5.  <span data-ttu-id="b3681-121">Rollen **Kontroller for kostnadsobjekt** er allerede opprettet.</span><span class="sxs-lookup"><span data-stu-id="b3681-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="b3681-122">Legg til andre medlemmer som er en del av organisasjonshierarkiet for tilgangsnivået for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="b3681-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span> 

    ![Legge til medlemmer](./media/CA-picture-2.png)

<span data-ttu-id="b3681-124">Brukere som legges til i rollen **Kontroller for kostnadsobjekt**, kan bare se dataene som de har tillatelse til å se i henhold til definisjonen i organisasjonshierarkiet for tilgangsnivået for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="b3681-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span> <span data-ttu-id="b3681-125">**Obs!** Radnivåsikkerhet gjelder for fliser og rapporter i Microsoft Dynamics 365 for Finance and Operations som bygges inn fra Power BI.</span><span class="sxs-lookup"><span data-stu-id="b3681-125">**Note:** Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="b3681-126">Oppdatere sikkerhet</span><span class="sxs-lookup"><span data-stu-id="b3681-126">Updating security</span></span>
<span data-ttu-id="b3681-127">Hvis oppdateringer gjøres i tilgangsnivåsikkerhet i kostnadsregnskapet og du vil at Power BI skal gjenspeile disse oppdateringene, må du oppdatere enhetsbutikken for **Kostnadsregnskapsanalyse**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="b3681-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="b3681-128">Når du har fullført oppdateringen fra enhetsbutikken fra Finance and Operations, må du oppdatere artefakter på PowerBI.com. Hvis du vil ha mer informasjon om hvordan du gjør en oppdatering for enhetsbutikk, kan du se [Oppdater enhetsbutikk](power-bi-integration-entity-store.md#update-entity-store)</span><span class="sxs-lookup"><span data-stu-id="b3681-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com. For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="b3681-129">Eieren av **Kostnadsregnskapsanalyse**-innholdet for Power BI må også utføre en oppdatering av enhetsbutikken hvis nye brukere gis tilgang til organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="b3681-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="b3681-130">I tillegg må eieren legge til nye brukere i rollen **Kontroller for kostnadsobjekt** på PowerBI.com, slik at radnivåsikkerhet gjelder for dem.</span><span class="sxs-lookup"><span data-stu-id="b3681-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="b3681-131">Deaktivere sikkerhet</span><span class="sxs-lookup"><span data-stu-id="b3681-131">Disabling security</span></span>
<span data-ttu-id="b3681-132">Vi antar at organisasjonen vil begrense tilgang til data.</span><span class="sxs-lookup"><span data-stu-id="b3681-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="b3681-133">Hvis sikkerhetsparameterene er deaktivert av en eller annen grunn ved kjøring av kostnadsregnskap, må eieren legge brukere til i rollen **Regnskapsfører** i Power BI i stedet.</span><span class="sxs-lookup"><span data-stu-id="b3681-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="b3681-134">Hvis du endrer sikkerhet fra en aktivert tilstand til en deaktivert tilstand, er det en god idé å fjerne brukere fra rollen **Kontroller for kostnadsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="b3681-134">If you change security from an enabled state to a disabled state, it’s a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="b3681-135">Utfør dette omvendt hvis du aktiverer sikkerhet på nytt.</span><span class="sxs-lookup"><span data-stu-id="b3681-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="b3681-136">Brukere kan tilhøre begge rollene.</span><span class="sxs-lookup"><span data-stu-id="b3681-136">Users can belong to both roles.</span></span> <span data-ttu-id="b3681-137">Felles tilgang er foreningen av begge rollene.</span><span class="sxs-lookup"><span data-stu-id="b3681-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="b3681-138">For **Kostnadsregnskapsanalyse**-innhold for Power BI har brukere med felles tilgang ubegrenset tilgang til data.</span><span class="sxs-lookup"><span data-stu-id="b3681-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="b3681-139">Hvis målet ditt er å bruke begrenset tilgang, må brukere bare tilordnes til rollen **Kontroller for kostnadsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="b3681-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="b3681-140">Disse oppdateringene for radnivåsikkerhet trer i kraft umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="b3681-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="b3681-141">Berørte brukere må oppdatere nettleseren.</span><span class="sxs-lookup"><span data-stu-id="b3681-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3681-142">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b3681-142">Additional resources</span></span>
<span data-ttu-id="b3681-143">Hvis du vil ha mer informasjon om radnivåsikkerhet i Power BI, kan du se [Administrere sikkerhet for modellen i Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="b3681-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>




