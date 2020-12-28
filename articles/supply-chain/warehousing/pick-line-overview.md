---
title: Definere et menyelement for en mobilenhet for å angi en plukklinjeoversikt
description: Dette emnet beskriver hvordan du definerer når en liste over alle arbeidslinjer skal vises til lagermedarbeidere som behandler lagerarbeid på en mobilenhet. Denne funksjonen kan være nyttig for lagerarbeidere som ofte må ha en oversikt over plukklinjene i en arbeidsordre, slik at de kan optimalisere plukkingsrekkefølgen.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434289"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="6ddad-104">Definere et menyelement for en mobilenhet for å angi en plukklinjeoversikt</span><span class="sxs-lookup"><span data-stu-id="6ddad-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6ddad-105">Dette emnet forklarer hvordan du konfigurerer alternativer som er knyttet til plukklinjeoversikten for menyvarer for mobilenheter som brukes til å behandle plukking av arbeid.</span><span class="sxs-lookup"><span data-stu-id="6ddad-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="6ddad-106">Plukklinjeoversikten lar lagerarbeidere vise og velge fra en liste over alle arbeidslinjene som er knyttet til den gjeldende oppgaven.</span><span class="sxs-lookup"><span data-stu-id="6ddad-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="6ddad-107">Denne funksjonen kan hjelpe arbeiderne med å optimalisere plukksekvensen.</span><span class="sxs-lookup"><span data-stu-id="6ddad-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="6ddad-108">Funksjonen inneholder alternativer som erstatter standard **Hopp over**-knapp, som la arbeidere bla gjennom linjene én om gangen, i en fast rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="6ddad-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="6ddad-109">(Alternativet for å bruke denne knappen er imidlertid fremdeles tilgjengelig.)</span><span class="sxs-lookup"><span data-stu-id="6ddad-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="6ddad-110">Administratorer kan konfigurere hvert menyelement for seg for å styre hvordan, når og hvor lagerappen presenterer plukklinjeoversikten.</span><span class="sxs-lookup"><span data-stu-id="6ddad-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="6ddad-111">Aktivere funksjonen Oversikt over arbeidsplukklinje</span><span class="sxs-lookup"><span data-stu-id="6ddad-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="6ddad-112">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="6ddad-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="6ddad-113">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="6ddad-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6ddad-114">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="6ddad-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6ddad-115">**Modul:** _Lagerstyring_</span><span class="sxs-lookup"><span data-stu-id="6ddad-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="6ddad-116">**Funksjonsnavn:** _Oversikt over arbeidsplukklinje_</span><span class="sxs-lookup"><span data-stu-id="6ddad-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="6ddad-117">Konfigurere menyelementer for å vise en liste over alle arbeidslinjer</span><span class="sxs-lookup"><span data-stu-id="6ddad-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="6ddad-118">Følg disse trinnene for å definere et menyelement for en mobilenhet for å angi en plukklinjeoversikt.</span><span class="sxs-lookup"><span data-stu-id="6ddad-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="6ddad-119">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="6ddad-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="6ddad-120">Velg eller opprett et menyelement som er knyttet til plukking av arbeid, og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6ddad-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="6ddad-121">**Modus:** *Arbeid*</span><span class="sxs-lookup"><span data-stu-id="6ddad-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="6ddad-122">**Bruke eksisterende arbeid:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="6ddad-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="6ddad-123">**Styrt av:** *Brukerstyrt* eller *Systemstyrt*</span><span class="sxs-lookup"><span data-stu-id="6ddad-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="6ddad-124">Hvis du vil ha mer informasjon om hvordan du oppretter menyelementer og bruker de ulike innstillingene som er tilgjengelige på siden **Menyelementer på mobilenheten**, kan du se [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="6ddad-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="6ddad-125">På hurtigfanen **Generelt** konfigurerer du funksjonen ved å sette feltet **Vis arbeidslinjeliste** til én av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6ddad-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="6ddad-126">**Vis bare ved forespørsel** – Arbeidere kan velge å vise plukklinjelisten ved å velge **Hopp til**-knappen i lagerappen.</span><span class="sxs-lookup"><span data-stu-id="6ddad-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="6ddad-127">**Vis ved starten av hver plukking** – Arbeidere ser listen hver gang de starter eller fullfører en plukklinje.</span><span class="sxs-lookup"><span data-stu-id="6ddad-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="6ddad-128">De kan også vise listen på nytt ved å velge **Hopp til**-knappen i lagerappen.</span><span class="sxs-lookup"><span data-stu-id="6ddad-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="6ddad-129">**Vis bare ved starten av første plukking** – Arbeidere ser listen hver gang de starter nytt plukkarbeid, men ikke etter hver linje.</span><span class="sxs-lookup"><span data-stu-id="6ddad-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="6ddad-130">De kan også vise listen på nytt ved å velge **Hopp til**-knappen i lagerappen.</span><span class="sxs-lookup"><span data-stu-id="6ddad-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="6ddad-131">**Vis aldri** – Standardknappen **Hopp over** vises i lagerappen, og visning av arbeidslinjelisten er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="6ddad-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="6ddad-132">Med **Hopp over**-knappen kan en arbeider bla gjennom linjene én om gangen, i en fast rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="6ddad-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="6ddad-133">De kan også gå gjennom listen så mange ganger som de treger, til alle linjene er behandlet.</span><span class="sxs-lookup"><span data-stu-id="6ddad-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="6ddad-134">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6ddad-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="6ddad-135">Hvis du setter feltet **Vis arbeidslinjeliste** til en hvilken som helst verdi unntatt *Vis aldri*, blir knappen **Feltliste** aldri tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="6ddad-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="6ddad-136">Velg **Feltliste** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6ddad-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="6ddad-137">På siden **Feltliste** konfigurerer du informasjonen som lagerappen viser for hver linje i listen.</span><span class="sxs-lookup"><span data-stu-id="6ddad-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="6ddad-138">Feltet for **primærkontroll** er alltid satt til *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="6ddad-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="6ddad-139">Derfor begynner hver rad i listen med et linjenummer.</span><span class="sxs-lookup"><span data-stu-id="6ddad-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="6ddad-140">Bruk de gjenstående feltene **Visningsfelt** for å legge til opptil sju ekstra visningsfelt, i henhold til hva du trenger.</span><span class="sxs-lookup"><span data-stu-id="6ddad-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="6ddad-141">I hvert **Visningsfelt**-felt velger du navnet på et arbeidslinjefelt.</span><span class="sxs-lookup"><span data-stu-id="6ddad-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="6ddad-142">Deretter vil hver linje vise en verdi for dette feltet.</span><span class="sxs-lookup"><span data-stu-id="6ddad-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="6ddad-143">Verdiene vil bli vist i den rekkefølgen du velger her.</span><span class="sxs-lookup"><span data-stu-id="6ddad-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="6ddad-144">Du kan la noen av **Visningsfelt**-feltene stå tomme hvis du ikke har behov for alle de sju verdiene.</span><span class="sxs-lookup"><span data-stu-id="6ddad-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="6ddad-145">I handlingsruten velger du **Lagre**, og deretter lukker du siden **Feltliste**.</span><span class="sxs-lookup"><span data-stu-id="6ddad-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>
