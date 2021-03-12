---
title: Vise arbeidsflytlogg
description: Dette emnet beskriver fremgangsmåten for å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 325478ed89b9c650899001dd08d1c98550fce520
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798986"
---
# <a name="view-workflow-history"></a><span data-ttu-id="6f5f9-103">Vise arbeidsflytlogg</span><span class="sxs-lookup"><span data-stu-id="6f5f9-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f5f9-104">Dette emnet beskriver fremgangsmåten for å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="6f5f9-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="6f5f9-106">Gå til **Navigasjonsrute > Moduler > Felles > Forespørsler > Arbeidsflyt > Arbeidsflytlogg**.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="6f5f9-107">Bruk dette skjemaet til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="6f5f9-108">**Arbeidsflyt-ID-en** er identifikasjonskoden til arbeidsflytforekomsten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="6f5f9-109">**Status** er arbeidsflytstatusen for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="6f5f9-110">**Arbeidsflyt-ID** er identifikasjonskoden til arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="6f5f9-111">**Dokument** er identifikasjonskoden for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="6f5f9-112">**Dokumenttype** er typen dokument som ble sendt til behandling.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="6f5f9-113">**Arbeidsflyt** er navnet på arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="6f5f9-114">**Versjon** er versjonsnummeret for arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="6f5f9-115">**Opprettingsdato og -klokkeslett** er datoen og klokkeslettet da dokumentet ble sendt.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="6f5f9-116">**Tidsforbruk** er tiden som har gått siden dokumentet ble sendt.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="6f5f9-117">Med **Fortsett**-knappen kan du gjenoppta arbeidsflytprosessen for det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="6f5f9-118">Med **Tilbakekall**-knappen kan du kalle tilbake til det valgte dokumentet slik at det ikke blir behandlet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="6f5f9-119">Velg koblingen i den ønskede raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="6f5f9-120">Kontroller at delen **Arbeidselementer** er utvidet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="6f5f9-121">I denne delen kan du vise arbeidselementene som er tilknyttet det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="6f5f9-122">Det kan for eksempel hende at en oppgave må fullføres, eller at dokumentet må godkjennes.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="6f5f9-123">Med knappen **Tilordne på nytt** åpner du en dialogboks der du kan tilordne et arbeidselement på nytt til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="6f5f9-124">Kontroller at delen **Sporingsdetaljer** er utvidet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="6f5f9-125">I denne delen kan du vise arbeidsflytloggen for det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6f5f9-125">In this section you can view the workflow history of the selected document.</span></span>  

