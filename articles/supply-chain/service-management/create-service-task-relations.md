---
title: Opprette serviceoppgaverelasjoner
description: Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b167714dc81cf0e4ee70d7092f2ec030043abe71
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202612"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="9a05a-103">Opprette serviceoppgaverelasjoner</span><span class="sxs-lookup"><span data-stu-id="9a05a-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a05a-104">Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren.</span><span class="sxs-lookup"><span data-stu-id="9a05a-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="9a05a-105">Denne informasjonen er tilgjengelig for teknikere og kunder.</span><span class="sxs-lookup"><span data-stu-id="9a05a-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="9a05a-106">Opprette en relasjon med en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="9a05a-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="9a05a-107">Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="9a05a-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="9a05a-108">Velg en eksisterende serviceavtale, eller opprett en ny serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="9a05a-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="9a05a-109">Klikk på **Serviceoppgaver**-knappen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9a05a-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="9a05a-110">I **Serviceoppgaver**-skjemaet trykker du på CTRL+N for å opprette en ny linje, og velg deretter en serviceoppgave fra **Serviceoppgave**-listen for å knytte serviceoppgaven til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="9a05a-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="9a05a-111">Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i kategorien **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9a05a-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="9a05a-112">Lukk skjemaet for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="9a05a-112">Close the form to save the record.</span></span>

<span data-ttu-id="9a05a-113">Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="9a05a-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="9a05a-114">Du kan nå angi disse serviceoppgavene for alle tilknyttede avtalelinjer.</span><span class="sxs-lookup"><span data-stu-id="9a05a-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="9a05a-115">En serviceoppgaverelasjon som er opprettet i en serviceavtale, er tilgjengelig fra alle serviceordrer som er knyttet til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="9a05a-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="9a05a-116">Opprette en relasjon med en serviceordre</span><span class="sxs-lookup"><span data-stu-id="9a05a-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="9a05a-117">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="9a05a-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="9a05a-118">Velg en eksisterende serviceordre, eller opprett en ny serviceordre.</span><span class="sxs-lookup"><span data-stu-id="9a05a-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="9a05a-119">Klikk på **Serviceoppgaver**-knappen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9a05a-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="9a05a-120">I **Serviceoppgaver**-skjemaet trykker du på CTRL+N for å opprette en ny linje, og velg deretter en serviceoppgave fra **Serviceoppgave**-listen for å knytte serviceoppgavene til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="9a05a-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="9a05a-121">Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i kategorien **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9a05a-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="9a05a-122">Lukk skjemaet for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="9a05a-122">Close the form to save the record.</span></span>

<span data-ttu-id="9a05a-123">Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="9a05a-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="9a05a-124">Deretter kan du velge serviceoppgaven du har opprettet relasjonen til, når du oppretter nye serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="9a05a-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="9a05a-125">Serviceoppgaverelasjoner som er opprettet i en serviceordre, er tilgjengelige i den aktuelle serviceordren.</span><span class="sxs-lookup"><span data-stu-id="9a05a-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a05a-126">Se også</span><span class="sxs-lookup"><span data-stu-id="9a05a-126">See also</span></span>

[<span data-ttu-id="9a05a-127">Oversikt over serviceoppgaver</span><span class="sxs-lookup"><span data-stu-id="9a05a-127">Service tasks overview</span></span>](service-tasks.md)


  


