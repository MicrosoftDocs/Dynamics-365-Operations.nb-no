---
title: Ytelse for planlegging av prosjektressurs
description: Dette emnet inneholder informasjon om hvordan du kan forbedre ytelsen til ressursplanlegging for et stort antall prosjekter.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760629"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="37275-103">Ytelse for planlegging av prosjektressurs</span><span class="sxs-lookup"><span data-stu-id="37275-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="37275-104">Det kan oppstå ytelsesproblemer knyttet til ressursplanlegging når antall prosjekter blir tusenvis.</span><span class="sxs-lookup"><span data-stu-id="37275-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="37275-105">Hvis du vil forbedre ressursplanleggingsytelsen, finnes det en funksjon som gjør det mulig for brukere å redusere tiden det tar å starte ressurstilgjengelighetsskjemaet.</span><span class="sxs-lookup"><span data-stu-id="37275-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="37275-106">Dette fjerner mer spesifikt den oppsamlede synkroniseringsprosessen for ressurskapasitet og bruker tabellen **ResProjectResource** til å øke hastigheten på ressursoppslaget.</span><span class="sxs-lookup"><span data-stu-id="37275-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="37275-107">Merk at tabellen **ResRollup** ikke lenger vil bli brukt.</span><span class="sxs-lookup"><span data-stu-id="37275-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37275-108">Hvis det finnes en avhengighet av den oppsamlede synkroniseringsprosessen for ressurskapasitet eller tabellen **ResProjectResource**, må du ikke bruke denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="37275-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="37275-109">Aktiver ytelsesforbedring for ressursplanlegging</span><span class="sxs-lookup"><span data-stu-id="37275-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="37275-110">Fullfør trinnene nedenfor for å aktivere ytelsesforbedring for ressursplanlegging.</span><span class="sxs-lookup"><span data-stu-id="37275-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="37275-111">Gå til **Funksjonsbehandling** > **Alle**, og i funksjonslisten finner du **funksjonen Aktiver ytelsesforbedring for prosjektressursplanlegging** .</span><span class="sxs-lookup"><span data-stu-id="37275-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="37275-112">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="37275-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="37275-113">Hvis du ikke finner funksjonen i listen, velger du **Se etter oppdateringer** for å oppdatere listen.</span><span class="sxs-lookup"><span data-stu-id="37275-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="37275-114">Oppdater nettleseren, og gå deretter til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektressurser** > **Synkroniser kapasitet for ressurskalendere på tvers av alle firmaer**.</span><span class="sxs-lookup"><span data-stu-id="37275-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="37275-115">Sett **Fjern eksisterende kapasitetsposter** til **Ja** for å fjerne tidligere data.</span><span class="sxs-lookup"><span data-stu-id="37275-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="37275-116">Hvis du vil generere trinnvise data, seter du verdien til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="37275-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="37275-117">I feltet **Periodekode** velger du perioden det skal genereres data i.</span><span class="sxs-lookup"><span data-stu-id="37275-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="37275-118">Hvis du velger en periodekode, trenger du ikke å definere en start- og sluttdato.</span><span class="sxs-lookup"><span data-stu-id="37275-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="37275-119">Hvis du lar feltet **Periodekode** stå tomt, må du velge bestemte start- og sluttdatoer for å generere data.</span><span class="sxs-lookup"><span data-stu-id="37275-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="37275-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="37275-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="37275-121">Dette distribuerer generelle data til tabellen **ResCalendarCapacity** på tvers av alle firmaer i miljøet, så den satsvise jobben må bare kjøres i én juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="37275-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="37275-122">Dataene i denne satsvise jobben er nødvendige for å beregne ressurskapasitet via den tilknyttede kalenderen.</span><span class="sxs-lookup"><span data-stu-id="37275-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="37275-123">Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektressurser** > **Fyll ut prosjektressurser på tvers av alle firmaer** og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="37275-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="37275-124">Dette er dataoppgraderingsskriptet for generelle data i tabellene **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="37275-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="37275-125">Verdiene for feltet **PSAPRojSchedRole.RootActivity** oppdateres også.</span><span class="sxs-lookup"><span data-stu-id="37275-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="37275-126">Hvis dette ikke kjøres, vil du få en advarsel når du prøver å utføre ressursplanleggingsoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="37275-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="37275-127">Deaktiver ytelsesforbedring for ressursplanlegging</span><span class="sxs-lookup"><span data-stu-id="37275-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="37275-128">Gå til **Funksjonsbehandling** > **Alle** og søk etter **funksjonen Aktiver ytelsesforbedring for prosjektressursplanlegging** .</span><span class="sxs-lookup"><span data-stu-id="37275-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="37275-129">Velg funksjonen, og velg deretter **Deaktiver**.</span><span class="sxs-lookup"><span data-stu-id="37275-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="37275-130">Oppdater nettleseren.</span><span class="sxs-lookup"><span data-stu-id="37275-130">Refresh your browser.</span></span>
4. <span data-ttu-id="37275-131">Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Kapasitetsynkronisering** > **Synkroniser opprullinger av ressurskapasitet**.</span><span class="sxs-lookup"><span data-stu-id="37275-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="37275-132">På siden **Synkronisering av opprulling av kapasitet** setter du **Fjern eksisterende kapasitetsposter** til **Ja** for å fjerne tidligere data.</span><span class="sxs-lookup"><span data-stu-id="37275-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="37275-133">Hvis du vil generere trinnvise data, seter du verdien til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="37275-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="37275-134">I feltet **Periodekode** velger du perioden det skal genereres data i.</span><span class="sxs-lookup"><span data-stu-id="37275-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="37275-135">Hvis du velger en periodekode, trenger du ikke å definere en start- og sluttdato.</span><span class="sxs-lookup"><span data-stu-id="37275-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="37275-136">Hvis du lar feltet **Periodekode** stå tomt, må du velge bestemte start- og sluttdatoer for å generere data.</span><span class="sxs-lookup"><span data-stu-id="37275-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="37275-137">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="37275-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="37275-138">Dette distribuerer generelle data til tabellen **ResRollup** på tvers av alle firmaer i miljøet, så den satsvise jobben må bare kjøres i én juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="37275-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="37275-139">Denne satsvise jobben er nødvendig for alle visninge av typen **Ressurstilgjengelighet**.</span><span class="sxs-lookup"><span data-stu-id="37275-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="37275-140">Hvis denne satsvise jobben ikke kjøres, vil **ResRollup-** dataene bli generert direkte, noe som kan ta tid.</span><span class="sxs-lookup"><span data-stu-id="37275-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
