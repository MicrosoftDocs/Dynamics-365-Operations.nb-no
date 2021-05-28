---
title: Avslutte konfigurasjoner i det globale RCS-repositoriet
description: Dette emnet beskriver hvordan du avslutter konfigurasjoner i det globale RCS-repositoriet.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018739"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="258ec-103">Avslutte konfigurasjoner i det globale RCS-repositoriet</span><span class="sxs-lookup"><span data-stu-id="258ec-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="258ec-104">Dette emnet beskriver hvordan du avslutter en konfigurasjon i det globale RCS-repositoriet.</span><span class="sxs-lookup"><span data-stu-id="258ec-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="258ec-105">Tidligere var det bare mulig å slette konfigurasjoner som ikke lenger var nødvendige.</span><span class="sxs-lookup"><span data-stu-id="258ec-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="258ec-106">Men nå kan du merke en frigitt konfigurasjon som **Avsluttet** i det globale RCS-repositoriet.</span><span class="sxs-lookup"><span data-stu-id="258ec-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="258ec-107">Med denne funksjonaliteten kan du også gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="258ec-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="258ec-108">Varsle på forhånd når en konfigurasjon skal avsluttes.</span><span class="sxs-lookup"><span data-stu-id="258ec-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="258ec-109">Inkluder aktuelle detaljer om erstatningskonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="258ec-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="258ec-110">Angi en dato for **Støttes til** for den spesifikke konfigurasjonen for å informere brukeren når den skal avsluttes.</span><span class="sxs-lookup"><span data-stu-id="258ec-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="258ec-111">Når du avslutter en konfigurasjonsversjon, kan du angi følgende valgfri informasjon:</span><span class="sxs-lookup"><span data-stu-id="258ec-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="258ec-112">**Erstatningskonfigurasjon**</span><span class="sxs-lookup"><span data-stu-id="258ec-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="258ec-113">**Versjon av erstatningskonfigurasjon**</span><span class="sxs-lookup"><span data-stu-id="258ec-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="258ec-114">**Fritekstnotat**: Bruk dette feltet til å angi dokumentasjonskoblinger eller -referanser</span><span class="sxs-lookup"><span data-stu-id="258ec-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="258ec-115">**Støttes til**: Dette feltet inneholder den foreslåtte datoen som gjeldende konfigurasjon/versjon vil bli støttet frem til.</span><span class="sxs-lookup"><span data-stu-id="258ec-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="258ec-116">Denne datoen må oppdateres manuelt.</span><span class="sxs-lookup"><span data-stu-id="258ec-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="258ec-117">Fullfør trinnene nedenfor for å avslutte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="258ec-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="258ec-118">Velg om du vil avslutte én versjon eller alle versjoner med samme innstillinger i én operasjon, ved å sette **Alle versjoner** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="258ec-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="258ec-119">Sett parameteren **Avslutt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="258ec-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="258ec-120">Velg **OK** for å avslutte konfigurasjonene.</span><span class="sxs-lookup"><span data-stu-id="258ec-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="258ec-121">Feltet **Utgått dato** fylles ut når du lagrer endringene.</span><span class="sxs-lookup"><span data-stu-id="258ec-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Avslutte konfigurasjonsinformasjon](media/Discontinue-details-2.png)
  
<span data-ttu-id="258ec-123">Du kan tilbakestille konfigurasjonen til **Delt** eller justere avsluttingsinformasjon når som helst.</span><span class="sxs-lookup"><span data-stu-id="258ec-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="258ec-124">Hvis du deler en konfigurasjon, angir du datoen for **Støttet til** og all annen informasjon relatert til avsluttingen, for å angi planene for fremtidig avslutting.</span><span class="sxs-lookup"><span data-stu-id="258ec-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="258ec-125">Hvis du vil dele informasjon om en planlagt avslutting før konfigurasjonen faktisk avsluttes, kan brukeren forhåndsfylle alle felt som er knyttet til erstatning, men la parameteren **Avslutte** være satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="258ec-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="258ec-126">Avslutting begrenser ikke operasjoner med konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="258ec-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="258ec-127">Du kan fortsette å importere, kjøre eller avlede konfigurasjonene, og disse feltene er veiledende.</span><span class="sxs-lookup"><span data-stu-id="258ec-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="258ec-128">Finans støtter visning av denne informasjonen fra versjon 10.0.14</span><span class="sxs-lookup"><span data-stu-id="258ec-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="258ec-129">Fra og med versjon 10.0.14 støtter Dynamics 365 Finance visning av avsluttingsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="258ec-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="258ec-130">På siden **Globalt repositorium** kan du vise oppdatert informasjon om avslutting.</span><span class="sxs-lookup"><span data-stu-id="258ec-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="258ec-131">Som standard blir konfigurasjoner som avsluttes, filtrert bort.</span><span class="sxs-lookup"><span data-stu-id="258ec-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="258ec-132">Siden **Importerte konfigurasjoner** (ERSolutionTable) viser konfigurasjoner som allerede ble avsluttet da de ble importert.</span><span class="sxs-lookup"><span data-stu-id="258ec-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="258ec-133">For de konfigurasjonene som ble avsluttet etter import, kan avsluttingsinformasjonen synkroniseres ved å kjøre jobben **Importere konfigurasjonsoppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="258ec-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


