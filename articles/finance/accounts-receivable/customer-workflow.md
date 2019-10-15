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
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8ff91a1df82d6195da266b97c347ef27afec662d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176043"
---
# <a name="customer-workflow"></a><span data-ttu-id="94d58-104">Arbeidsflyt for kunde</span><span class="sxs-lookup"><span data-stu-id="94d58-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94d58-105">Arbeidsflyten for kunde har blitt lagt til i versjon 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="94d58-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="94d58-106">Du kan endre bestemte felt for en kunde og deretter sende endringene til godkjenning ved hjelp av arbeidsflyten før de legges til for kunden.</span><span class="sxs-lookup"><span data-stu-id="94d58-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="94d58-107">Definere arbeidsflyten for kunde</span><span class="sxs-lookup"><span data-stu-id="94d58-107">Set up the customer workflow</span></span>

<span data-ttu-id="94d58-108">Før du kan bruke funksjonen for arbeidsflyt for kunde, må du aktivere den.</span><span class="sxs-lookup"><span data-stu-id="94d58-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="94d58-109">Gå til **Kunder \> Oppsett \> Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="94d58-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="94d58-110">I fanen **Generelt** i hurtigfanen **Kundegodkjenning** setter du verdien for alternativet **Aktiver kundegodkjenninger** til **Ja** for å aktivere funksjonen.</span><span class="sxs-lookup"><span data-stu-id="94d58-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="94d58-111">I feltet **Virkemåte for dataenhet** velger du virkemåten som dataenhetene skal bruke når data importeres:</span><span class="sxs-lookup"><span data-stu-id="94d58-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="94d58-112">**Tillat endringer uten godkjenning** – en enhet kan oppdatere kundeposten uten å behandle den med arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="94d58-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="94d58-113">**Forkast endringer** – kan ikke gjøre endringer i kundeposten.</span><span class="sxs-lookup"><span data-stu-id="94d58-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="94d58-114">Importen vil mislykkes for feltene som er aktivert for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="94d58-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="94d58-115">**Opprette forslag til endring** – alle felt blir endret, bortsett fra feltene som er aktivert for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="94d58-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="94d58-116">De nye verdiene for disse feltene legges til kunden som foreslåtte endringer, og arbeidsflyten vil starte automatisk.</span><span class="sxs-lookup"><span data-stu-id="94d58-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="94d58-117">I listen over kundefelt merker du deretter av for **Aktiver** for hvert felt som må godkjennes før endringene kan utføres.</span><span class="sxs-lookup"><span data-stu-id="94d58-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="94d58-118">Gå til **Kunder \> Oppsett \> Arbeidsflyter for Kunde**.</span><span class="sxs-lookup"><span data-stu-id="94d58-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="94d58-119">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="94d58-119">Select **New**.</span></span>
7. <span data-ttu-id="94d58-120">Velg **Arbeidsflyten til foreslåtte kundeendringer**.</span><span class="sxs-lookup"><span data-stu-id="94d58-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="94d58-121">Definere arbeidsflyten slik at den samsvarer med godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="94d58-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="94d58-122">Elementet **Arbeidsflytgodkjenning for foreslåtte kundeendringer** for godkjenning av arbeidsflyt vil gjelde for endringene for kunden.</span><span class="sxs-lookup"><span data-stu-id="94d58-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="94d58-123">Endre kundeinformasjon og sende inn endringene til arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="94d58-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="94d58-124">Når du endrer et felt som er aktivert for arbeidsflyten, vises siden **Foreslått endringer**.</span><span class="sxs-lookup"><span data-stu-id="94d58-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="94d58-125">Denne siden viser den opprinnelige verdien i feltet og den nye verdien du angav.</span><span class="sxs-lookup"><span data-stu-id="94d58-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="94d58-126">Feltet du endret, tilbakestilles til opprinnelig verdi.</span><span class="sxs-lookup"><span data-stu-id="94d58-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="94d58-127">En statusmelding på siden informerer deg om at endringene ikke har blitt sendt.</span><span class="sxs-lookup"><span data-stu-id="94d58-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="94d58-128">Hver gang du endrer et felt som er aktivert for arbeidsflyten, legges feltet til i listen over foreslåtte endringer.</span><span class="sxs-lookup"><span data-stu-id="94d58-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="94d58-129">Hvis du vil forkaste den foreslåtte verdien for et felt, bruker du **Forkast**-knappen ved siden av feltet i listen.</span><span class="sxs-lookup"><span data-stu-id="94d58-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="94d58-130">Hvis du vil forkaste alle endringer, kan du bruke knappen **Forkast alle endringer** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="94d58-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="94d58-131">Velg **OK** for å lukke siden.</span><span class="sxs-lookup"><span data-stu-id="94d58-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="94d58-132">Når du har minst én foreslått endring, vises det to ytterligere menyer i handlingsruten: **Foreslåtte endringer** og **Arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="94d58-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="94d58-133">Velg **Foreslåtte endringer** for å åpne siden **Foreslåtte endringer** og se gjennom endringene.</span><span class="sxs-lookup"><span data-stu-id="94d58-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="94d58-134">Velg **Arbeidsflyt \>Send** for å sende endringene til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="94d58-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="94d58-135">Statusen på siden endres til **Endringer som venter på godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="94d58-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="94d58-136">Arbeidsflyten følger standard arbeidsflytprosessen i programmet.</span><span class="sxs-lookup"><span data-stu-id="94d58-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="94d58-137">Godkjenneren er rettet mot siden **Kunde**, der han eller hun kan se endringene på siden **Foreslåtte endringer** og deretter velge **Arbeidsflyt \> Godkjenn** for å godkjenne arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="94d58-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="94d58-138">Når alle godkjenninger er fullført, oppdateres feltene med verdier som du har foreslått.</span><span class="sxs-lookup"><span data-stu-id="94d58-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
