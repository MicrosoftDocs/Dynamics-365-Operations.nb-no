---
title: Arbeidsflyt for leverandør
description: Endre informasjon om leverandør og bruke arbeidsflyt til å godkjenne den.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e5aef18a7f541c6a0d4abf9d4461d1dd9cd27880
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810276"
---
# <a name="vendor-workflow"></a><span data-ttu-id="54d47-103">Arbeidsflyt for leverandør</span><span class="sxs-lookup"><span data-stu-id="54d47-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54d47-104">Når det brukes arbeidsflyt for leverandør, sendes endringene som gjøres i bestemte felt i arbeidsflyten for godkjenning før de kan legges til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="54d47-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="54d47-105">Definere arbeidsflyten for leverandør</span><span class="sxs-lookup"><span data-stu-id="54d47-105">Set up the vendor workflow</span></span>

<span data-ttu-id="54d47-106">Før du kan bruke funksjonen for arbeidsflyt, må du aktivere den.</span><span class="sxs-lookup"><span data-stu-id="54d47-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="54d47-107">Gå til **Leverandører \> Oppsett \> Leverandørparametere**.</span><span class="sxs-lookup"><span data-stu-id="54d47-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="54d47-108">I kategorien **Generelt** i hurtigfanen **Leverandørgodkjenning** angir du alternativet **Aktiver leverandørgodkjenninger** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="54d47-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="54d47-109">I feltet **Virkemåte for dataenhet** velger du virkemåten som skal brukes når data importeres:</span><span class="sxs-lookup"><span data-stu-id="54d47-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="54d47-110">**Tillat endringer uten godkjenning** – dataenheten kan oppdatere leverandørposten uten å behandle den med arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="54d47-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="54d47-111">**Forkast endringer** – kan ikke gjøre endringer i leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="54d47-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="54d47-112">Importen vil mislykkes for feltene som er aktivert for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="54d47-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="54d47-113">**Opprette forslag til endring** – alle felt blir endret, bortsett fra feltene som er aktivert for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="54d47-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="54d47-114">De nye verdiene for disse feltene legges til leverandøren som foreslåtte endringer, og arbeidsflyten vil starte automatisk.</span><span class="sxs-lookup"><span data-stu-id="54d47-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="54d47-115">I listen over leverandørfelt merker du av for **Aktiver** for hvert felt som må godkjennes før endringene kan utføres.</span><span class="sxs-lookup"><span data-stu-id="54d47-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="54d47-116">Gå til **Leverandører \> Oppsett \> Arbeidsflyter for leverandørreskontro**.</span><span class="sxs-lookup"><span data-stu-id="54d47-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="54d47-117">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="54d47-117">Select **New**.</span></span>
7. <span data-ttu-id="54d47-118">Velg **Arbeidsflyten til foreslåtte leverandørendringer**.</span><span class="sxs-lookup"><span data-stu-id="54d47-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="54d47-119">Definere arbeidsflyten slik at den samsvarer med godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="54d47-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="54d47-120">Elementet **Arbeidsflytgodkjenning for foreslåtte leverandørendringer** for godkjenning av arbeidsflyt vil gjelde for endringene for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="54d47-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="54d47-121">Endre leverandørinformasjon og sende inn endringene til arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="54d47-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="54d47-122">Når du endrer et felt som er aktivert for arbeidsflyten, vises siden **Foreslått endringer**.</span><span class="sxs-lookup"><span data-stu-id="54d47-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="54d47-123">Denne siden viser den opprinnelige verdien i feltet og den nye verdien du angav.</span><span class="sxs-lookup"><span data-stu-id="54d47-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="54d47-124">Feltet du endret, tilbakestilles til opprinnelig verdi.</span><span class="sxs-lookup"><span data-stu-id="54d47-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="54d47-125">En statusmelding informerer deg også om at endringene ikke har blitt sendt.</span><span class="sxs-lookup"><span data-stu-id="54d47-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="54d47-126">Hver gang du endrer et felt som er aktivert for arbeidsflyten, legges feltet til i listen på siden **Foreslåtte endringer**.</span><span class="sxs-lookup"><span data-stu-id="54d47-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="54d47-127">Hvis du vil forkaste den foreslåtte verdien for et felt, bruker du **Forkast**-knappen ved siden av feltet i listen.</span><span class="sxs-lookup"><span data-stu-id="54d47-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="54d47-128">Hvis du vil forkaste alle endringer, kan du bruke knappen **Forkast alle endringer** nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="54d47-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="54d47-129">Velg **OK** for å lukke siden.</span><span class="sxs-lookup"><span data-stu-id="54d47-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="54d47-130">Når du har minst én foreslått endring, vises det to ytterligere kategorier i handlingsruten: **Foreslåtte endringer** og **Arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="54d47-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="54d47-131">Velg **Foreslåtte endringer** for å åpne siden **Foreslåtte endringer** og se gjennom endringene.</span><span class="sxs-lookup"><span data-stu-id="54d47-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="54d47-132">Velg **Arbeidsflyt \> Send for å sende endringene til arbeidsflyten**.</span><span class="sxs-lookup"><span data-stu-id="54d47-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="54d47-133">Statusen på siden endres til **Endringer som venter på godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="54d47-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="54d47-134">Arbeidsflyten følger standard arbeidsflytprosess.</span><span class="sxs-lookup"><span data-stu-id="54d47-134">The workflow follows the standard workflow process.</span></span> <span data-ttu-id="54d47-135">Godkjenneren er rettet mot siden **Leverandør**, der endringene kan gjennomgås på siden **Foreslåtte endringer** og deretter velge **Arbeidsflyt \> Godkjenn** for å godkjenne arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="54d47-135">The approver is directed to the **Vendor** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="54d47-136">Når alle godkjenninger er fullført, oppdateres feltene med verdier som du har foreslått.</span><span class="sxs-lookup"><span data-stu-id="54d47-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]