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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea5952376fe30f489d385c8f8295fbf86f2af085
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470743"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="706e4-103">Opprette serviceoppgaverelasjoner</span><span class="sxs-lookup"><span data-stu-id="706e4-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="706e4-104">Du kan knytte serviceoppgaver til serviceavtaler eller serviceordrer for å beskrive serviceoppgaven som skal fullføres for avtalen eller ordren.</span><span class="sxs-lookup"><span data-stu-id="706e4-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="706e4-105">Denne informasjonen er tilgjengelig for teknikere og kunder.</span><span class="sxs-lookup"><span data-stu-id="706e4-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="706e4-106">Opprette en relasjon med en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="706e4-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="706e4-107">Gå til **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="706e4-107">Go to **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="706e4-108">Velg en eksisterende serviceavtale, eller opprett en ny serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="706e4-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="706e4-109">Velg knappen **Serviceoppgaver** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="706e4-109">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="706e4-110">I skjemaet **Serviceoppgaver** velger du **Ny** for å opprette en ny linje, og velg deretter en serviceoppgave fra listen **Serviceoppgave** for å knytte serviceoppgaven til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="706e4-110">On the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="706e4-111">Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i fanen **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="706e4-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="706e4-112">Lukk skjemaet for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="706e4-112">Close the form to save the record.</span></span>

<span data-ttu-id="706e4-113">Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="706e4-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="706e4-114">Du kan nå angi disse serviceoppgavene for alle tilknyttede avtalelinjer.</span><span class="sxs-lookup"><span data-stu-id="706e4-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="706e4-115">En serviceoppgaverelasjon som er opprettet i en serviceavtale, er tilgjengelig fra alle serviceordrer som er knyttet til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="706e4-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="706e4-116">Opprette en relasjon med en serviceordre</span><span class="sxs-lookup"><span data-stu-id="706e4-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="706e4-117">Gå til **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="706e4-117">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="706e4-118">Velg en eksisterende serviceordre, eller opprett en ny serviceordre.</span><span class="sxs-lookup"><span data-stu-id="706e4-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="706e4-119">Velg knappen **Serviceoppgaver** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="706e4-119">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="706e4-120">I skjemaet **Serviceoppgaver** velger du **Ny** for å opprette en ny linje, og velg deretter en serviceoppgave fra listen **Serviceoppgave** for å knytte serviceoppgavene til servicordren.</span><span class="sxs-lookup"><span data-stu-id="706e4-120">From the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="706e4-121">Angi eventuelle interne eller eksterne beskrivelsesmerknader i fritekstfeltene i fanen **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="706e4-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="706e4-122">Lukk skjemaet for å lagre posten.</span><span class="sxs-lookup"><span data-stu-id="706e4-122">Close the form to save the record.</span></span>

<span data-ttu-id="706e4-123">Gjenta denne prosessen til du har opprettet alle de nødvendige serviceoppgaverelasjonene for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="706e4-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="706e4-124">Deretter kan du velge serviceoppgaven du har opprettet relasjonen til, når du oppretter nye serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="706e4-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="706e4-125">Serviceoppgaverelasjoner som er opprettet i en serviceordre, er tilgjengelige i den aktuelle serviceordren.</span><span class="sxs-lookup"><span data-stu-id="706e4-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="706e4-126">Se også</span><span class="sxs-lookup"><span data-stu-id="706e4-126">See also</span></span>

[<span data-ttu-id="706e4-127">Oversikt over serviceoppgaver</span><span class="sxs-lookup"><span data-stu-id="706e4-127">Service tasks overview</span></span>](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]