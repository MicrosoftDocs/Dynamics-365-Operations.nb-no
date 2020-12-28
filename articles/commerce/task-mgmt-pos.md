---
title: Oppgavebehandling på salgsstedet
description: Dette emnet beskriver oppgavebehandling i Microsoft Dynamics 365 Commerce POS-programmet (salgssted).
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414706"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="33408-103">Oppgavebehandling på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="33408-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33408-104">Dette emnet beskriver oppgavebehandling i Microsoft Dynamics 365 Commerce POS-programmet (salgssted).</span><span class="sxs-lookup"><span data-stu-id="33408-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="33408-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="33408-105">Overview</span></span>

<span data-ttu-id="33408-106">Dynamics 365 Commerce POS-programmet har funksjoner for oppgavebehandling som gjør at butikkledere og arbeidere kan administrere oppgaver og oppdatere oppgavestatus.</span><span class="sxs-lookup"><span data-stu-id="33408-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="33408-107">Butikkarbeidere kan få tilgang til oppgaver enten ved å velge **Oppgaver**-flisen på POS-startsiden eller ved å velge oppgavevarslinger.</span><span class="sxs-lookup"><span data-stu-id="33408-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="33408-108">Som standard blir butikkarbeidere tatt til kategorien **Mine oppgaver**, der de kan vise oppgavene som er tilordnet dem.</span><span class="sxs-lookup"><span data-stu-id="33408-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="33408-109">De kan imidlertid enkelt bytte til kategoriene **Forfalte oppgaver**, **Åpne oppgaver** og **Oppgavelister**.</span><span class="sxs-lookup"><span data-stu-id="33408-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="33408-110">Oppgaveoperasjoner for butikkledere</span><span class="sxs-lookup"><span data-stu-id="33408-110">Task operations for store managers</span></span>

<span data-ttu-id="33408-111">Butikkledere kan utføre følgende oppgaveoperasjoner i POS-programmet ved hjelp av knappene på kommandolinjen:</span><span class="sxs-lookup"><span data-stu-id="33408-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="33408-112">**Tilordne** – Tilordne valgte oppgaver til en butikkarbeider.</span><span class="sxs-lookup"><span data-stu-id="33408-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="33408-113">**Oppgavestatus** – Endre statusen for valgte oppgaver.</span><span class="sxs-lookup"><span data-stu-id="33408-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="33408-114">**Filter** – Som standard vises bare aktive oppgaver.</span><span class="sxs-lookup"><span data-stu-id="33408-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="33408-115">Ved å bruke filtre kan imidlertid overordnede vise alle oppgaver, også oppgaver som er fullført eller avbrutt.</span><span class="sxs-lookup"><span data-stu-id="33408-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="33408-116">**Ny oppgave** – Opprett en oppgave under en eksisterende oppgaveliste, eller opprett en oppgave med enkelt formål.</span><span class="sxs-lookup"><span data-stu-id="33408-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="33408-117">Butikkarbeidere kan utføre følgende oppgaveoperasjoner i POS-programmet ved hjelp av knappene på kommandolinjen:</span><span class="sxs-lookup"><span data-stu-id="33408-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="33408-118">**Oppgavestatus** – Endre statusen for valgte oppgaver.</span><span class="sxs-lookup"><span data-stu-id="33408-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="33408-119">**Filter** – Som standard vises bare aktive oppgaver.</span><span class="sxs-lookup"><span data-stu-id="33408-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="33408-120">Ved å bruke filtre kan imidlertid arbeidere vise alle oppgaver, også oppgaver som er fullført eller avbrutt.</span><span class="sxs-lookup"><span data-stu-id="33408-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="33408-121">Følgende illustrasjon viser kategorien **Mine oppgaver** i Commerce POS-programmet.</span><span class="sxs-lookup"><span data-stu-id="33408-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Mine oppgaver-kategorien i Commerce POS-programmet](media/POS-task-management.png)

<span data-ttu-id="33408-123">Illustrasjonen nedenfor viser kategorien **Oppgavelister**.</span><span class="sxs-lookup"><span data-stu-id="33408-123">The following illustration shows the **Task lists** tab.</span></span>

![Oppgavelister-kategorien i Commerce POS-programmet](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="33408-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="33408-125">Additional resources</span></span>

[<span data-ttu-id="33408-126">Oversikt over oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="33408-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="33408-127">Konfigurere oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="33408-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="33408-128">Opprette oppgavelister og legge til oppgaver</span><span class="sxs-lookup"><span data-stu-id="33408-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="33408-129">Tilordne oppgavelister til butikker eller ansatte</span><span class="sxs-lookup"><span data-stu-id="33408-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
