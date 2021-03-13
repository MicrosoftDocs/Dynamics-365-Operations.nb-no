---
title: Definere sikkerhet for Power BI-innhold for analyse av kostnadsregnskap
description: Dette emnet forklarer hvordan du kan overføre tilgangsnivåsikkerhet i Kostnadsregnskap til radnivåsikkerhet i Microsoft Power BI.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d54ced21de112288c2f98c0bc895ca0d49c217e3
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093361"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="fa6f5-103">Definere sikkerhet for Power BI-innhold for analyse av kostnadsregnskap</span><span class="sxs-lookup"><span data-stu-id="fa6f5-103">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa6f5-104">Dette emnet forklarer hvordan du kan overføre tilgangsnivåsikkerhet i Kostnadsregnskap til radnivåsikkerhet i Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-104">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="fa6f5-105">Denne funksjonaliteten lar brukere bare se Power BI-data som de har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-105">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="fa6f5-106">Oversikt</span><span class="sxs-lookup"><span data-stu-id="fa6f5-106">Overview</span></span>

<span data-ttu-id="fa6f5-107">**Kostregnskapsanalyse**-innholdet for Microsoft Power BI bruker Power BI-radnivåsikkerhet til å begrense brukertilgangen.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-107">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="fa6f5-108">Sikkerheten er basert på organisasjonshierarkiet for tilgangsnivå som er definert i parametere for kostnadsregnskapet.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-108">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="fa6f5-109">Hvis du vil ha mer informasjon om **Kostregnskapsanalyse**-innhold for Power BI, kan du se [Kostnadsregnskapsanalyse-innhold for Power BI.](cost-accounting-analysis-content-pack.md)</span><span class="sxs-lookup"><span data-stu-id="fa6f5-109">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="fa6f5-110">Installasjon</span><span class="sxs-lookup"><span data-stu-id="fa6f5-110">Setup</span></span>
<span data-ttu-id="fa6f5-111">For å overføre tilgangsnivåsikkerhet til Power BI må eieren av Power BI-innholdet følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-111">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="fa6f5-112">Brukeren som publiserer **Kostregnskapsanalyse**-innholdet for Power BI blir automatisk eieren.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-112">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="fa6f5-113">Bare en eier kan konfigurere sikkerhet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-113">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="fa6f5-114">Før en eier legger til andre brukere på PowerBI.com kan ingen unntatt eieren se alle dataene i Power BI-innholdet **Kostnadsregnskapsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-114">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="fa6f5-115">Publisere definisjonsfilen til Power BI.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-115">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="fa6f5-116">Logg på PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-116">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="fa6f5-117">Finn datasettet for **Kostnadsregnskapsanalyse**-innhold for Power BI.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-117">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="fa6f5-118">Åpne sikkerhetssiden.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-118">Open the security page.</span></span>

    ![Åpne sikkerhetssiden](./media/CA-picture-1.png)

5. <span data-ttu-id="fa6f5-120">Rollen **Kontroller for kostnadsobjekt** er allerede opprettet.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-120">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="fa6f5-121">Legg til andre medlemmer som er en del av organisasjonshierarkiet for tilgangsnivået for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-121">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![Legge til medlemmer](./media/CA-picture-2.png)

<span data-ttu-id="fa6f5-123">Brukere som legges til i rollen **Kontroller for kostnadsobjekt**, kan bare se dataene som de har tillatelse til å se i henhold til definisjonen i organisasjonshierarkiet for tilgangsnivået for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-123">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="fa6f5-124">Sikkerheten på radnivå gjelder fliser og rapporter som er innebygd fra Power BI.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-124">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="fa6f5-125">Oppdatere sikkerhet</span><span class="sxs-lookup"><span data-stu-id="fa6f5-125">Updating security</span></span>
<span data-ttu-id="fa6f5-126">Hvis oppdateringer gjøres i tilgangsnivåsikkerhet i kostnadsregnskapet og du vil at Power BI skal gjenspeile disse oppdateringene, må du oppdatere enhetsbutikken for **Kostnadsregnskapsanalyse**-innholdet for Power BI.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-126">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="fa6f5-127">Når du har fullført oppdateringen av enhetsbutikken, må du oppdatere artefaktene på PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-127">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="fa6f5-128">Hvis du vil ha mer informasjon om hvordan du utfører en oppdatering for enhetsbutikk, kan du se [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="fa6f5-128">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="fa6f5-129">Eieren av **Kostnadsregnskapsanalyse**-innholdet for Power BI må også utføre en oppdatering av enhetsbutikken hvis nye brukere gis tilgang til organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="fa6f5-130">I tillegg må eieren legge til nye brukere i rollen **Kontroller for kostnadsobjekt** på PowerBI.com, slik at radnivåsikkerhet gjelder for dem.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="fa6f5-131">Deaktivere sikkerhet</span><span class="sxs-lookup"><span data-stu-id="fa6f5-131">Disabling security</span></span>
<span data-ttu-id="fa6f5-132">Vi antar at organisasjonen vil begrense tilgang til data.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="fa6f5-133">Hvis sikkerhetsparameterene er deaktivert av en eller annen grunn ved kjøring av kostnadsregnskap, må eieren legge brukere til i rollen **Regnskapsfører lager** i Power BI i stedet.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="fa6f5-134">Hvis du endrer sikkerhet fra en aktivert tilstand til en deaktivert tilstand, er det en god idé å fjerne brukere fra rollen **Kontroller for kostnadsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-134">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="fa6f5-135">Utfør dette omvendt hvis du aktiverer sikkerhet på nytt.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="fa6f5-136">Brukere kan tilhøre begge rollene.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-136">Users can belong to both roles.</span></span> <span data-ttu-id="fa6f5-137">Felles tilgang er foreningen av begge rollene.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="fa6f5-138">For **Kostnadsregnskapsanalyse**-innhold for Power BI har brukere med felles tilgang ubegrenset tilgang til data.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="fa6f5-139">Hvis målet ditt er å bruke begrenset tilgang, må brukere bare tilordnes til rollen **Kontroller for kostnadsobjekt**.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="fa6f5-140">Disse oppdateringene for radnivåsikkerhet trer i kraft umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="fa6f5-141">Berørte brukere må oppdatere nettleseren.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa6f5-142">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fa6f5-142">Additional resources</span></span>
<span data-ttu-id="fa6f5-143">Hvis du vil ha mer informasjon om radnivåsikkerhet i Power BI, kan du se [Administrere sikkerhet for modellen i Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="fa6f5-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
