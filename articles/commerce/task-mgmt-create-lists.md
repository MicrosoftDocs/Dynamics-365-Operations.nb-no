---
title: Opprette oppgavelister og legge til oppgaver
description: Dette emnet beskriver hvordan du oppretter oppgavelister og legger til oppgaver i dem i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 28bea16c3266115cf09aa80a364344789d60af7a
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477838"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="42505-103">Opprette oppgavelister og legge til oppgaver</span><span class="sxs-lookup"><span data-stu-id="42505-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42505-104">Dette emnet beskriver hvordan du oppretter oppgavelister og legger til oppgaver i dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="42505-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="42505-105">En *oppgave* definerer en bestemt del av arbeidet eller en handling som noen må fullføre på eller før en angitt forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="42505-105">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="42505-106">I Dynamics 365 Commerce kan en oppgave inneholde detaljerte instruksjoner og informasjon om en kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="42505-106">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="42505-107">Den kan også inneholde koblinger til Back-Office-operasjoner, salgsstedsoperasjoner (POS) eller områdesider, for å forbedre produktiviteten og gi den konteksten som oppgaveeieren trenger for å fullføre oppgaven effektivt.</span><span class="sxs-lookup"><span data-stu-id="42505-107">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="42505-108">En *oppgaveliste* er en samling oppgaver som må fullføres som en del av en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="42505-108">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="42505-109">Det kan for eksempel finnes en oppgaveliste som en ny arbeider må fullføre under opplastingen, en oppgaveliste for kasserere som arbeider kveldsskift, eller en oppgaveliste som må fullføres for å forberede butikken for en forestående høytid.</span><span class="sxs-lookup"><span data-stu-id="42505-109">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="42505-110">I Commerce kan alle oppgavelister som har en måldato, tilordnes til et hvilket som helst antall butikker eller ansatte, og den kan konfigureres til å gjentas.</span><span class="sxs-lookup"><span data-stu-id="42505-110">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="42505-111">Både ledere og arbeidere kan opprette oppgavelister i Commerce Back Office, og deretter tilordne dem til et sett med butikker.</span><span class="sxs-lookup"><span data-stu-id="42505-111">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="42505-112">Opprett en oppgaveliste</span><span class="sxs-lookup"><span data-stu-id="42505-112">Create a task list</span></span>

<span data-ttu-id="42505-113">Hvis du vil opprette en oppgaveliste, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="42505-113">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="42505-114">Gå til **Retail og Commerce \> Oppgavebehandling \> Administrasjon av oppgavebehandling**.</span><span class="sxs-lookup"><span data-stu-id="42505-114">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="42505-115">Velg **Ny**, og angi deretter verdier i feltene **Navn**, **Beskrivelse** og **Eier**.</span><span class="sxs-lookup"><span data-stu-id="42505-115">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="42505-116">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="42505-116">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="42505-117">Legge til oppgaver i en oppgaveliste</span><span class="sxs-lookup"><span data-stu-id="42505-117">Add tasks to a task list</span></span>

<span data-ttu-id="42505-118">Hvis du vil legge til oppgaver i en oppgaveliste, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="42505-118">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="42505-119">På hurtigfanen **Oppgaver** i en eksisterende oppgaveliste velger du **Ny** for å legge til en oppgave.</span><span class="sxs-lookup"><span data-stu-id="42505-119">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="42505-120">I dialogboksen **Opprett en ny oppgave** skriver du inn et navn på oppgaven i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="42505-120">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="42505-121">I feltet **Forfallsdato samsvarer ikke med måldato** angir du en positiv eller negativ heltallsverdi.</span><span class="sxs-lookup"><span data-stu-id="42505-121">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="42505-122">Angi for eksempel **-2** hvis oppgaven skal fullføres to dager før oppgavelistens forfalls dato.</span><span class="sxs-lookup"><span data-stu-id="42505-122">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="42505-123">I feltet **Merknader** angir du detaljerte instruksjoner.</span><span class="sxs-lookup"><span data-stu-id="42505-123">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="42505-124">I feltet **Kontaktperson** angir du navnet på en emneekspert som oppgaveeieren kan kontakte hvis han eller hun trenger hjelp.</span><span class="sxs-lookup"><span data-stu-id="42505-124">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="42505-125">I feltet **Oppgavekobling** angir du en kobling basert på typen oppgave.</span><span class="sxs-lookup"><span data-stu-id="42505-125">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="42505-126">Selv om du kan bruke feltet **Tilordnet til** til å tilordne oppgaver til noen når du oppretter en oppgaveliste, anbefaler vi at du unngår å tilordne oppgaver når oppgavelisten opprettes.</span><span class="sxs-lookup"><span data-stu-id="42505-126">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="42505-127">Du må i stedet tilordne oppgavene etter at listen er opprettet for enkeltbutikker.</span><span class="sxs-lookup"><span data-stu-id="42505-127">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="42505-128">Bruke oppgavekoblinger til å forbedre arbeiderproduktiviteten</span><span class="sxs-lookup"><span data-stu-id="42505-128">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="42505-129">Med Commerce kan du koble oppgaver til bestemte POS-operasjoner, for eksempel å kjøre en salgsrapport, vise en elektronisk opplæringsvideo for orientering til ansatte eller utføre en Back-Office-operasjon.</span><span class="sxs-lookup"><span data-stu-id="42505-129">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="42505-130">Denne funksjonen hjelper oppgaveeiere med å få den informasjonen de trenger for å fullføre en oppgave effektivt.</span><span class="sxs-lookup"><span data-stu-id="42505-130">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="42505-131">Hvis du vil legge til oppgavekoblinger mens du oppretter en oppgave, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="42505-131">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="42505-132">På hurtigfanen **Oppgaver** i en eksisterende oppgaveliste velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="42505-132">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="42505-133">I dialogboksen **Rediger oppgave**, i feltet **Oppgavekobling** velger du ett eller flere av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="42505-133">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="42505-134">Velg **Menyelement** for å konfigurere en Back-Office-operasjon, for eksempel "Produktsett".</span><span class="sxs-lookup"><span data-stu-id="42505-134">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="42505-135">Velg **POS-operasjon** for å konfigurere en POS-operasjon, for eksempel "Salgsrapporter".</span><span class="sxs-lookup"><span data-stu-id="42505-135">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="42505-136">Velg **URL-adresse** for å konfigurere en absolutt URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="42505-136">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="42505-137">Følgende illustrasjon viser valget av oppgavekoblinger i dialog boksen **Rediger oppgave**.</span><span class="sxs-lookup"><span data-stu-id="42505-137">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Velge oppgavekoblinger i dialogboksen Rediger oppgave](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="42505-139">Konfigurere en POS-operasjon slik at den kan kobles til en oppgave</span><span class="sxs-lookup"><span data-stu-id="42505-139">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="42505-140">Gjør følgende for å konfigurere en POS-operasjon slik at den kan kobles til en oppgave.</span><span class="sxs-lookup"><span data-stu-id="42505-140">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="42505-141">Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> POS-operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="42505-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="42505-142">Velg **Rediger**, finn POS-operasjonen, og merk deretter av for **Aktiver oppgavebehandling** for den.</span><span class="sxs-lookup"><span data-stu-id="42505-142">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42505-143">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="42505-143">Additional resources</span></span>

[<span data-ttu-id="42505-144">Oversikt over oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="42505-144">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="42505-145">Konfigurere oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="42505-145">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="42505-146">Tilordne oppgavelister til butikker eller ansatte</span><span class="sxs-lookup"><span data-stu-id="42505-146">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="42505-147">Oppgavebehandling på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="42505-147">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
