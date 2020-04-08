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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd5b8d9f3fd2edab50b52a8345f254ebc6b31d0a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140404"
---
# <a name="view-workflow-history"></a><span data-ttu-id="79d08-103">Vise arbeidsflytlogg</span><span class="sxs-lookup"><span data-stu-id="79d08-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79d08-104">Dette emnet beskriver fremgangsmåten for å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.</span><span class="sxs-lookup"><span data-stu-id="79d08-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="79d08-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="79d08-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="79d08-106">Gå til **Navigasjonsrute > Moduler > Felles > Forespørsler > Arbeidsflyt > Arbeidsflytlogg**.</span><span class="sxs-lookup"><span data-stu-id="79d08-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="79d08-107">Bruk dette skjemaet til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.</span><span class="sxs-lookup"><span data-stu-id="79d08-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="79d08-108">**Arbeidsflyt-ID-en** er identifikasjonskoden til arbeidsflytforekomsten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="79d08-109">**Status** er arbeidsflytstatusen for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="79d08-110">**Arbeidsflyt-ID** er identifikasjonskoden til arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="79d08-111">**Dokument** er identifikasjonskoden for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="79d08-112">**Dokumenttype** er typen dokument som ble sendt til behandling.</span><span class="sxs-lookup"><span data-stu-id="79d08-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="79d08-113">**Arbeidsflyt** er navnet på arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="79d08-114">**Versjon** er versjonsnummeret for arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="79d08-115">**Opprettingsdato og -klokkeslett** er datoen og klokkeslettet da dokumentet ble sendt.</span><span class="sxs-lookup"><span data-stu-id="79d08-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="79d08-116">**Tidsforbruk** er tiden som har gått siden dokumentet ble sendt.</span><span class="sxs-lookup"><span data-stu-id="79d08-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="79d08-117">Med **Fortsett**-knappen kan du gjenoppta arbeidsflytprosessen for det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="79d08-118">Med **Tilbakekall**-knappen kan du kalle tilbake til det valgte dokumentet slik at det ikke blir behandlet.</span><span class="sxs-lookup"><span data-stu-id="79d08-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="79d08-119">Velg koblingen i den ønskede raden i listen.</span><span class="sxs-lookup"><span data-stu-id="79d08-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="79d08-120">Kontroller at delen **Arbeidselementer** er utvidet.</span><span class="sxs-lookup"><span data-stu-id="79d08-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="79d08-121">I denne delen kan du vise arbeidselementene som er tilknyttet det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="79d08-122">Det kan for eksempel hende at en oppgave må fullføres, eller at dokumentet må godkjennes.</span><span class="sxs-lookup"><span data-stu-id="79d08-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="79d08-123">Med knappen **Tilordne på nytt** åpner du en dialogboks der du kan tilordne et arbeidselement på nytt til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="79d08-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="79d08-124">Kontroller at delen **Sporingsdetaljer** er utvidet.</span><span class="sxs-lookup"><span data-stu-id="79d08-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="79d08-125">I denne delen kan du vise arbeidsflytloggen for det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="79d08-125">In this section you can view the workflow history of the selected document.</span></span>  

