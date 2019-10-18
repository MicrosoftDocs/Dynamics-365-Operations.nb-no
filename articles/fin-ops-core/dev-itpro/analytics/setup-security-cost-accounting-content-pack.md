---
title: Definere sikkerhet for Power BI-innhold for analyse av kostnadsregnskap
description: Dette emnet forklarer hvordan du kan overføre tilgangsnivåsikkerhet i Kostnadsregnskap til radnivåsikkerhet i Microsoft Power BI. Denne funksjonaliteten lar brukere bare se Power BI-data som de har tilgang til.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b0f7dffd85dc1c7a58a3e1f55eaa26ecbf6e8360
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185181"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="493e8-104">Definere sikkerhet for Power BI-innhold for analyse av kostnadsregnskap</span><span class="sxs-lookup"><span data-stu-id="493e8-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="493e8-105">Dette emnet forklarer hvordan du kan overføre tilgangsnivåsikkerhet i Kostnadsregnskap til radnivåsikkerhet i Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="493e8-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="493e8-106">Denne funksjonaliteten lar brukere bare se Power BI-data som de har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="493e8-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="493e8-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="493e8-107">Overview</span></span>

<span data-ttu-id="493e8-108">**Kostregnskapsanalyse**-innholdet for Microsoft Power BI bruker Power BI-radnivåsikkerhet til å begrense brukertilgangen.</span><span class="sxs-lookup"><span data-stu-id="493e8-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="493e8-109">Sikkerheten er basert på organisasjonshierarkiet for tilgangsnivå som er definert i parametere for kostnadsregnskapet.</span><span class="sxs-lookup"><span data-stu-id="493e8-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="493e8-110">Hvis du vil ha mer informasjon om **Kostregnskapsanalyse**-innhold for Power BI, kan du se [Kostnadsregnskapsanalyse-innhold for Power BI.](cost-accounting-analysis-content-pack.md)</span><span class="sxs-lookup"><span data-stu-id="493e8-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="493e8-111">Installasjon</span><span class="sxs-lookup"><span data-stu-id="493e8-111">Setup</span></span>
<span data-ttu-id="493e8-112">For å overføre tilgangsnivåsikkerhet til Power BI må eieren av Power BI-innholdet følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="493e8-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="493e8-113">Brukeren som publiserer **Kostregnskapsanalyse**-innholdet for Power BI blir automatisk eieren.</span><span class="sxs-lookup"><span data-stu-id="493e8-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="493e8-114">Bare en eier kan konfigurere sikkerhet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="493e8-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="493e8-115">Før en eier legger til andre brukere på PowerBI.com kan ingen unntatt eieren se alle dataene i Power BI-innholdet **Kostnadsregnskapsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="493e8-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="493e8-116">Publisere definisjonsfilen til Power BI.</span><span class="sxs-lookup"><span data-stu-id="493e8-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="493e8-117">Logg på PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="493e8-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="493e8-118">Finn datasettet for **Kostnadsregnskapsanalyse**-innhold for Power BI.</span><span class="sxs-lookup"><span data-stu-id="493e8-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="493e8-119">Åpne sikkerhetssiden.</span><span class="sxs-lookup"><span data-stu-id="493e8-119">Open the security page.</span></span>

    ![Åpne sikkerhetssiden](./media/CA-picture-1.png)

5. <span data-ttu-id="493e8-121">Rollen **Kontroller for kostnadsobjekt** er allerede opprettet.</span><span class="sxs-lookup"><span data-stu-id="493e8-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="493e8-122">Legg til andre medlemmer som er en del av organisasjonshierarkiet for tilgangsnivået for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="493e8-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Legge til medlemmer](./media/CA-picture-2.png)

<span data-ttu-id="493e8-124">Brukere som legges til i rollen **Kontroller for kostnadsobjekt**, kan bare se dataene som de har tillatelse til å se i henhold til definisjonen i organisasjonshierarkiet for tilgangsnivået for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="493e8-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="493e8-125">Sikkerheten på radnivå gjelder fliser og rapporter som er innebygd fra Power BI.</span><span class="sxs-lookup"><span data-stu-id="493e8-125">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="493e8-126">Oppdatere sikkerhet</span><span class="sxs-lookup"><span data-stu-id="493e8-126">Updating security</span></span>
<span data-ttu-id="493e8-127">Hvis oppdateringer gjøres i tilgangsnivåsikkerhet i kostnadsregnskapet og du vil at Power BI skal gjenspeile disse oppdateringene, må du oppdatere enhetsbutikken for **Kostnadsregnskapsanalyse**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="493e8-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="493e8-128">Når du har fullført oppdateringen av enhetsbutikken, må du oppdatere artefaktene på PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="493e8-128">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="493e8-129">Hvis du vil ha mer informasjon om hvordan du utfører en oppdatering for enhetsbutikk, kan du se [Oppdatere enhetsbutikken](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="493e8-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="493e8-130">Eieren av **Kostnadsregnskapsanalyse**-innholdet for Power BI må også utføre en oppdatering av enhetsbutikken hvis nye brukere gis tilgang til organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="493e8-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="493e8-131">I tillegg må eieren legge til nye brukere i rollen **Kontroller for kostnadsobjekt** på PowerBI.com, slik at radnivåsikkerhet gjelder for dem.</span><span class="sxs-lookup"><span data-stu-id="493e8-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="493e8-132">Deaktivere sikkerhet</span><span class="sxs-lookup"><span data-stu-id="493e8-132">Disabling security</span></span>
<span data-ttu-id="493e8-133">Vi antar at organisasjonen vil begrense tilgang til data.</span><span class="sxs-lookup"><span data-stu-id="493e8-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="493e8-134">Hvis sikkerhetsparameterene er deaktivert av en eller annen grunn ved kjøring av kostnadsregnskap, må eieren legge brukere til i rollen **Regnskapsfører lager** i Power BI i stedet.</span><span class="sxs-lookup"><span data-stu-id="493e8-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="493e8-135">Hvis du endrer sikkerhet fra en aktivert tilstand til en deaktivert tilstand, er det en god idé å fjerne brukere fra rollen **Kontroller for kostnadsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="493e8-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="493e8-136">Utfør dette omvendt hvis du aktiverer sikkerhet på nytt.</span><span class="sxs-lookup"><span data-stu-id="493e8-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="493e8-137">Brukere kan tilhøre begge rollene.</span><span class="sxs-lookup"><span data-stu-id="493e8-137">Users can belong to both roles.</span></span> <span data-ttu-id="493e8-138">Felles tilgang er foreningen av begge rollene.</span><span class="sxs-lookup"><span data-stu-id="493e8-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="493e8-139">For **Kostnadsregnskapsanalyse**-innhold for Power BI har brukere med felles tilgang ubegrenset tilgang til data.</span><span class="sxs-lookup"><span data-stu-id="493e8-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="493e8-140">Hvis målet ditt er å bruke begrenset tilgang, må brukere bare tilordnes til rollen **Kontroller for kostnadsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="493e8-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="493e8-141">Disse oppdateringene for radnivåsikkerhet trer i kraft umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="493e8-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="493e8-142">Berørte brukere må oppdatere nettleseren.</span><span class="sxs-lookup"><span data-stu-id="493e8-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="493e8-143">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="493e8-143">Additional resources</span></span>
<span data-ttu-id="493e8-144">Hvis du vil ha mer informasjon om radnivåsikkerhet i Power BI, kan du se [Administrere sikkerhet for modellen i Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="493e8-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
