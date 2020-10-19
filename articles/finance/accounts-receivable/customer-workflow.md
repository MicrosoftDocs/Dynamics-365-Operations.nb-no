---
title: Arbeidsflyt for kunde
description: Dette emnet gir informasjon om kundearbeidsflyten. Du endrer bestemte felt for en kunde og deretter sende endringene til godkjenning ved hjelp av arbeidsflyten før de legges til for kunden.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: cb8519db2f5d52d4e317b485d6ecc910956788cb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975322"
---
# <a name="customer-workflow"></a><span data-ttu-id="12cac-104">Arbeidsflyt for kunde</span><span class="sxs-lookup"><span data-stu-id="12cac-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12cac-105">Arbeidsflyten for kunde har blitt lagt til i versjon 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="12cac-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="12cac-106">Du kan endre bestemte felt for en kunde og deretter sende endringene til godkjenning ved hjelp av arbeidsflyten før de legges til for kunden.</span><span class="sxs-lookup"><span data-stu-id="12cac-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="12cac-107">Definere arbeidsflyten for kunde</span><span class="sxs-lookup"><span data-stu-id="12cac-107">Set up the customer workflow</span></span>

<span data-ttu-id="12cac-108">Før du kan bruke funksjonen for arbeidsflyt for kunde, må du aktivere den.</span><span class="sxs-lookup"><span data-stu-id="12cac-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="12cac-109">Gå til **Kunder \> Oppsett \> Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="12cac-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="12cac-110">I fanen **Generelt** i hurtigfanen **Kundegodkjenning** setter du verdien for alternativet **Aktiver kundegodkjenninger** til **Ja** for å aktivere funksjonen.</span><span class="sxs-lookup"><span data-stu-id="12cac-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="12cac-111">I feltet **Virkemåte for dataenhet** velger du virkemåten som dataenhetene skal bruke når data importeres:</span><span class="sxs-lookup"><span data-stu-id="12cac-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="12cac-112">**Tillat endringer uten godkjenning** – en enhet kan oppdatere kundeposten uten å behandle den med arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="12cac-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="12cac-113">**Forkast endringer** – kan ikke gjøre endringer i kundeposten.</span><span class="sxs-lookup"><span data-stu-id="12cac-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="12cac-114">Importen vil mislykkes for feltene som er aktivert for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="12cac-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="12cac-115">**Opprette forslag til endring** – alle felt blir endret, bortsett fra feltene som er aktivert for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="12cac-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="12cac-116">De nye verdiene for disse feltene legges til kunden som foreslåtte endringer, og arbeidsflyten vil starte automatisk.</span><span class="sxs-lookup"><span data-stu-id="12cac-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="12cac-117">I listen over kundefelt merker du deretter av for **Aktiver** for hvert felt som må godkjennes før endringene kan utføres.</span><span class="sxs-lookup"><span data-stu-id="12cac-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="12cac-118">Gå til **Kunder \> Oppsett \> Arbeidsflyter for Kunde**.</span><span class="sxs-lookup"><span data-stu-id="12cac-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="12cac-119">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="12cac-119">Select **New**.</span></span>
7. <span data-ttu-id="12cac-120">Velg **Arbeidsflyten til foreslåtte kundeendringer**.</span><span class="sxs-lookup"><span data-stu-id="12cac-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="12cac-121">Definere arbeidsflyten slik at den samsvarer med godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="12cac-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="12cac-122">Elementet **Arbeidsflytgodkjenning for foreslåtte kundeendringer** for godkjenning av arbeidsflyt vil gjelde for endringene for kunden.</span><span class="sxs-lookup"><span data-stu-id="12cac-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="12cac-123">Endre kundeinformasjon og sende inn endringene til arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="12cac-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="12cac-124">Når du endrer et felt som er aktivert for arbeidsflyten, vises siden **Foreslått endringer**.</span><span class="sxs-lookup"><span data-stu-id="12cac-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="12cac-125">Denne siden viser den opprinnelige verdien i feltet og den nye verdien du angav.</span><span class="sxs-lookup"><span data-stu-id="12cac-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="12cac-126">Feltet du endret, tilbakestilles til opprinnelig verdi.</span><span class="sxs-lookup"><span data-stu-id="12cac-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="12cac-127">En statusmelding på siden informerer deg om at endringene ikke har blitt sendt.</span><span class="sxs-lookup"><span data-stu-id="12cac-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="12cac-128">Hver gang du endrer et felt som er aktivert for arbeidsflyten, legges feltet til i listen over foreslåtte endringer.</span><span class="sxs-lookup"><span data-stu-id="12cac-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="12cac-129">Hvis du vil forkaste den foreslåtte verdien for et felt, bruker du **Forkast**-knappen ved siden av feltet i listen.</span><span class="sxs-lookup"><span data-stu-id="12cac-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="12cac-130">Hvis du vil forkaste alle endringer, kan du bruke knappen **Forkast alle endringer** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="12cac-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="12cac-131">Velg **OK** for å lukke siden.</span><span class="sxs-lookup"><span data-stu-id="12cac-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="12cac-132">Når du har minst én foreslått endring, vises det to ytterligere menyer i handlingsruten: **Foreslåtte endringer** og **Arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="12cac-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="12cac-133">Velg **Foreslåtte endringer** for å åpne siden **Foreslåtte endringer** og se gjennom endringene.</span><span class="sxs-lookup"><span data-stu-id="12cac-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="12cac-134">Velg **Arbeidsflyt \>Send** for å sende endringene til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="12cac-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="12cac-135">Statusen på siden endres til **Endringer som venter på godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="12cac-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="12cac-136">Arbeidsflyten følger standard arbeidsflytprosessen i programmet.</span><span class="sxs-lookup"><span data-stu-id="12cac-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="12cac-137">Godkjenneren er rettet mot siden **Kunde**, der han eller hun kan se endringene på siden **Foreslåtte endringer** og deretter velge **Arbeidsflyt \> Godkjenn** for å godkjenne arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="12cac-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="12cac-138">Når alle godkjenninger er fullført, oppdateres feltene med verdier som du har foreslått.</span><span class="sxs-lookup"><span data-stu-id="12cac-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
