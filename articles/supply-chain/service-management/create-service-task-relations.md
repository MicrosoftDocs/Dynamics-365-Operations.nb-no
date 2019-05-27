---
title: Opprette serviceoppgaverelasjoner
description: Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552121"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="d77d5-103">Opprette serviceoppgaverelasjoner</span><span class="sxs-lookup"><span data-stu-id="d77d5-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d77d5-104">Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren.</span><span class="sxs-lookup"><span data-stu-id="d77d5-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="d77d5-105">Denne informasjonen er tilgjengelig for teknikere og kunder.</span><span class="sxs-lookup"><span data-stu-id="d77d5-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="d77d5-106">Opprette en relasjon med en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="d77d5-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="d77d5-107">Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="d77d5-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="d77d5-108">Velg en eksisterende serviceavtale, eller opprett en ny serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="d77d5-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="d77d5-109">Klikk på **Serviceoppgaver**-knappen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d77d5-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="d77d5-110">I **Serviceoppgaver**-skjemaet trykker du på CTRL+N for å opprette en ny linje, og velg deretter en serviceoppgave fra **Serviceoppgave**-listen for å knytte serviceoppgaven til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="d77d5-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="d77d5-111">Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i kategorien **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d77d5-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="d77d5-112">Lukk skjemaet for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="d77d5-112">Close the form to save the record.</span></span>

<span data-ttu-id="d77d5-113">Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="d77d5-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="d77d5-114">Du kan nå angi disse serviceoppgavene for alle tilknyttede avtalelinjer.</span><span class="sxs-lookup"><span data-stu-id="d77d5-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="d77d5-115">En serviceoppgaverelasjon som er opprettet i en serviceavtale, er tilgjengelig fra alle serviceordrer som er knyttet til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="d77d5-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="d77d5-116">Opprette en relasjon med en serviceordre</span><span class="sxs-lookup"><span data-stu-id="d77d5-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="d77d5-117">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="d77d5-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="d77d5-118">Velg en eksisterende serviceordre, eller opprett en ny serviceordre.</span><span class="sxs-lookup"><span data-stu-id="d77d5-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="d77d5-119">Klikk på **Serviceoppgaver**-knappen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d77d5-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="d77d5-120">I **Serviceoppgaver**-skjemaet trykker du på CTRL+N for å opprette en ny linje, og velg deretter en serviceoppgave fra **Serviceoppgave**-listen for å knytte serviceoppgavene til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="d77d5-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="d77d5-121">Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i kategorien **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d77d5-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="d77d5-122">Lukk skjemaet for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="d77d5-122">Close the form to save the record.</span></span>

<span data-ttu-id="d77d5-123">Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="d77d5-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="d77d5-124">Deretter kan du velge serviceoppgaven du har opprettet relasjonen til, når du oppretter nye serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="d77d5-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="d77d5-125">Serviceoppgaverelasjoner som er opprettet i en serviceordre, er tilgjengelige i den aktuelle serviceordren.</span><span class="sxs-lookup"><span data-stu-id="d77d5-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="d77d5-126">Se også</span><span class="sxs-lookup"><span data-stu-id="d77d5-126">See also</span></span>

[<span data-ttu-id="d77d5-127">Serviceoppgaver </span><span class="sxs-lookup"><span data-stu-id="d77d5-127">Service tasks</span></span>](service-tasks.md)


  


