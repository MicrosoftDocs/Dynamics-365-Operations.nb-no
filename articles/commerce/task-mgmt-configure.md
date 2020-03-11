---
title: Konfigurere oppgavebehandling
description: Dette emnet beskriver hvordan du konfigurerer funksjoner for oppgavebehandling i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036861"
---
# <a name="configure-task-management"></a><span data-ttu-id="816f7-103">Konfigurere oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="816f7-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="816f7-104">Dette emnet beskriver hvordan du konfigurerer funksjoner for oppgavebehandling i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="816f7-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="816f7-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="816f7-105">Overview</span></span>

<span data-ttu-id="816f7-106">Før Dynamics 365 Commerce-ledere og -ansatte kan bruke funksjonene for oppgavestyring i Commerce, må oppgavebehandling være konfigurert.</span><span class="sxs-lookup"><span data-stu-id="816f7-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="816f7-107">Konfigurasjonstrinn omfatter å gi tillatelser til ledere og ansatte, distribuere tillatelser til salgsstedsklienter (POS), definere POS-varslinger og konfigurere **Oppgaver**-flisen på startsiden for et POS-program.</span><span class="sxs-lookup"><span data-stu-id="816f7-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="816f7-108">Konfigurere tillatelser for butikkledere</span><span class="sxs-lookup"><span data-stu-id="816f7-108">Configure permissions for store managers</span></span>

<span data-ttu-id="816f7-109">Alle ansatte i en gitt butikk kan vise alle oppgaver som er tilordnet til butikken.</span><span class="sxs-lookup"><span data-stu-id="816f7-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="816f7-110">De kan også oppdatere statusen for oppgavene som er tilordnet til dem.</span><span class="sxs-lookup"><span data-stu-id="816f7-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="816f7-111">Personer som butikkledere må imidlertid ha administrasjonsrettigheter for aktiviteter for å administrere oppgaver som er tilordnet til butikken, og til å opprette oppgaver med enkelt formål.</span><span class="sxs-lookup"><span data-stu-id="816f7-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="816f7-112">Følg denne fremgangsmåten for å konfigurere tillatelser for oppgavebehandling for butikkledere.</span><span class="sxs-lookup"><span data-stu-id="816f7-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="816f7-113">Gå til **Retail og Commerce \> Ansatte \> Tillatelsesgrupper**.</span><span class="sxs-lookup"><span data-stu-id="816f7-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="816f7-114">Velg en bestemt tillatelsesgruppe (for eksempel **Leder**), og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="816f7-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="816f7-115">I hurtigfanen **Tillatelser** setter du alternativet **Tillat oppgavebehandling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="816f7-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="816f7-116">I hurtigfanen **Varslinger** legger du til operasjonen **Oppgavestyring** og angir en verdi i feltet **Visningsrekkefølge**.</span><span class="sxs-lookup"><span data-stu-id="816f7-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="816f7-117">Angi for eksempel **2** hvis **Ordreoppfyllelse**-operasjonen allerede har en verdi for **Visningsrekkefølge** på **1**.</span><span class="sxs-lookup"><span data-stu-id="816f7-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="816f7-118">Hvis en person som ikke er leder, må ha tillatelser for oppgavebehandling på salgsstedet, kan du gi tilgang til den enkelte.</span><span class="sxs-lookup"><span data-stu-id="816f7-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="816f7-119">Du kan også opprette en ny tillatelses gruppe for ikke-overordnede og sette alternativet **Tillat oppgavebehandling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="816f7-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="816f7-120">Følgende illustrasjon viser hvordan du konfigurerer tillatelser for oppgavebehandling for butikkledere.</span><span class="sxs-lookup"><span data-stu-id="816f7-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Konfigurere tillatelser for oppgavebehandling for butikkledere](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="816f7-122">Konfigurere tillatelser for ansatte</span><span class="sxs-lookup"><span data-stu-id="816f7-122">Configure permissions for employees</span></span>

<span data-ttu-id="816f7-123">Ansatte må ha tillatelse til å opprette oppgavelister, behandle tildelingskriterier og konfigurere gjentakelsen av en hvilken som helst oppgaveliste.</span><span class="sxs-lookup"><span data-stu-id="816f7-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="816f7-124">Hvis du vil konfigurere disse tillatelsene, tilordner du de ansatte til rollen **Retail-oppgaveleder**.</span><span class="sxs-lookup"><span data-stu-id="816f7-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="816f7-125">Hvis du vil konfigurere tillatelser for en ansatt, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="816f7-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="816f7-126">Gå til **Retail og Commerce \> Ansatte \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="816f7-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="816f7-127">Velg en ansatt.</span><span class="sxs-lookup"><span data-stu-id="816f7-127">Select an employee.</span></span>
1. <span data-ttu-id="816f7-128">På hurtigfanen **Brukerens roller** velger du **Tilordne roller**.</span><span class="sxs-lookup"><span data-stu-id="816f7-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="816f7-129">I dialogboksen **Tilordne roller til bruker** velger du rollen **Retail-oppgaveleder** og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="816f7-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="816f7-130">Distribuere tillatelser til POS-klienter</span><span class="sxs-lookup"><span data-stu-id="816f7-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="816f7-131">Før ansatte kan bruke POS-klienter, må tillatelser distribueres og synkroniseres til disse klientene.</span><span class="sxs-lookup"><span data-stu-id="816f7-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="816f7-132">Følg denne fremgangsmåten for å distribuere tillatelser til POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="816f7-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="816f7-133">Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.</span><span class="sxs-lookup"><span data-stu-id="816f7-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="816f7-134">Velg distribusjonsplanen **1060** (**Stab**), og velg deretter **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="816f7-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="816f7-135">Velg distribusjonsplanen **1070** (**Kanalkonfigurasjon**), og velg deretter **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="816f7-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="816f7-136">Konfigurere POS-varslinger for oppgaver</span><span class="sxs-lookup"><span data-stu-id="816f7-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="816f7-137">Oppgavebehandling må konfigureres slik at varslinger blir tilgjengelige i POS-programmet.</span><span class="sxs-lookup"><span data-stu-id="816f7-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="816f7-138">Hvis du vil konfigurere POS-varslinger for oppgaver, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="816f7-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="816f7-139">Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> POS-operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="816f7-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="816f7-140">Finn operasjonen **1400** (**Oppgavebehandling**), og merk av for **Aktiver varslinger** for den.</span><span class="sxs-lookup"><span data-stu-id="816f7-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="816f7-141">Følgende illustrasjon viser operasjonen **Oppgavebehandling** på siden **POS-operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="816f7-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Operasjonen Oppgavebehandling på siden POS-operasjoner](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="816f7-143">Hvis du vil ha mer informasjon om hvordan du konfigurerer POS-varslinger, kan du se [Vise ordrevarslinger på salgsstedet (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="816f7-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="816f7-144">Konfigurere Oppgaver-flisen på startsiden for et POS-program</span><span class="sxs-lookup"><span data-stu-id="816f7-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="816f7-145">Før du konfigurerer **Oppgaver**-flisen på startsiden for et POS-program, kan du se [Skjermoppsett for salgssted (POS)](pos-screen-layouts.md) for informasjon om hvordan du konfigurerer og legger til nye knapper i et POS-skjermoppsett.</span><span class="sxs-lookup"><span data-stu-id="816f7-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="816f7-146">Gjør følgende for å konfigurere **Oppgaver**-flisen på startsiden for et POS-program.</span><span class="sxs-lookup"><span data-stu-id="816f7-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="816f7-147">Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="816f7-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="816f7-148">Velg et skjermoppsett, velg en oppsettsstørrelse, og velg deretter en knappegruppe.</span><span class="sxs-lookup"><span data-stu-id="816f7-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="816f7-149">På hurtigfanen **Knappegrupper** velger du **Designer** for å redigere den valgte knappegruppen.</span><span class="sxs-lookup"><span data-stu-id="816f7-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="816f7-150">Legg til en **Oppgaver**-flis i den aktuelle delen på startsiden.</span><span class="sxs-lookup"><span data-stu-id="816f7-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="816f7-151">Illustrasjonen nedenfor viser et eksempel på en **Oppgaver**-flis på en POS-startside.</span><span class="sxs-lookup"><span data-stu-id="816f7-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Oppgaver-flis på en POS-startside](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="816f7-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="816f7-153">Additional resources</span></span>

[<span data-ttu-id="816f7-154">Oversikt over oppgavebehandling</span><span class="sxs-lookup"><span data-stu-id="816f7-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="816f7-155">Opprette oppgavelister og legge til oppgaver</span><span class="sxs-lookup"><span data-stu-id="816f7-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="816f7-156">Tilordne oppgavelister til butikker eller ansatte</span><span class="sxs-lookup"><span data-stu-id="816f7-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="816f7-157">Oppgavebehandling på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="816f7-157">Task management in POS</span></span>](task-mgmt-POS.md)
