---
title: Vis arbeidsflytlogg
description: Bruk denne fremgangsmåten til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: a40fe377322e2d64b751f6cace3eda20736cd321
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560458"
---
# <a name="view-workflow-history"></a><span data-ttu-id="6ff9a-103">Vis arbeidsflytlogg</span><span class="sxs-lookup"><span data-stu-id="6ff9a-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ff9a-104">Bruk denne fremgangsmåten til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-104">Use these steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="6ff9a-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="6ff9a-106">Gå til Felles > Forespørsler > Arbeidsflyt > Arbeidsflytlogg.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-106">Go to Common > Inquiries > Workflow > Workflow history.</span></span>
    * <span data-ttu-id="6ff9a-107">Bruk dette skjemaet til å vise status for et dokument som er sendt til arbeidsflytsystemet for behandling og godkjenning.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    * <span data-ttu-id="6ff9a-108">Arbeidsflyt-IDen er identifikasjonskoden til arbeidsflytforekomsten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-108">The Instance ID is      the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="6ff9a-109">Statusen er arbeidsflytstatusen for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-109">The Status is the workflow status of the document.</span></span>  
    * <span data-ttu-id="6ff9a-110">Arbeidsflyt-IDen er identifikasjonskoden til arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-110">The Workflow ID is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="6ff9a-111">Dokumentet er identifikasjonskoden for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-111">The Document is the identification code of the document.</span></span>  
    * <span data-ttu-id="6ff9a-112">Dokumenttypen er typen dokument som ble sendt til behandling.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-112">The Document type is the type of document that was submitted for processing.</span></span>  
    * <span data-ttu-id="6ff9a-113">Arbeidsflyten er navnet på arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-113">The Workflow is the name of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="6ff9a-114">Versjonen er versjonsnummeret for arbeidsflyten som behandler, eller som har behandlet, dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-114">The Version is the version number of the workflow that is processing, or has processed the document.</span></span>  
    * <span data-ttu-id="6ff9a-115">Opprettingsdato og -klokkeslett er datoen og klokkeslettet da dokumentet ble sendt.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-115">The Created date and time is the date and time that the document was submitted.</span></span>  
    * <span data-ttu-id="6ff9a-116">Tidsforbruk er tiden som har gått siden dokumentet ble sendt.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-116">The Elapsed time is the time that has passed since the document was submitted.</span></span>  
    * <span data-ttu-id="6ff9a-117">Med Fortsett-knappen kan du gjenoppta arbeidsflytprosessen for det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-117">The Resume button allows you to resume the workflow process for the selected document.</span></span>  
    * <span data-ttu-id="6ff9a-118">Med Tilbakekall-knappen kan du kalle tilbake til det valgte dokumentet slik at det ikke blir behandlet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-118">The Recall button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="6ff9a-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6ff9a-120">Kontroller at delen Arbeidselementer er utvidet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-120">Make sure the Work items section is expanded.</span></span>    <span data-ttu-id="6ff9a-121">I denne delen kan du vise arbeidselementene som er tilknyttet det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="6ff9a-122">Det kan for eksempel hende at en oppgave må fullføres, eller at dokumentet må godkjennes.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    * <span data-ttu-id="6ff9a-123">Med knappen Tilordne på nytt åpner du en dialogboks der du kan tilordne et arbeidselement på nytt til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-123">The Reassign button will open a dialog box where you can reassign a work item to another user.</span></span>  
    * <span data-ttu-id="6ff9a-124">Kontroller at delen Sporingsdetaljer er utvidet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-124">Make sure the Tracking details section is expanded.</span></span>    <span data-ttu-id="6ff9a-125">I denne delen kan du vise arbeidsflytloggen for det valgte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="6ff9a-125">In this section you can view the workflow history of the selected document.</span></span>  

