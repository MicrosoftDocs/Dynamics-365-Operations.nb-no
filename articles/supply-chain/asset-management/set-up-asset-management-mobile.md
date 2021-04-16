---
title: Konfigurere det mobile arbeidsområdet Aktivastyring
description: Dette emnet beskriver hvordan du konfigurerer Microsoft Dynamics 365 Supply Chain Management og mobilappen Finance and Operations (Dynamics 365) slik at de kan kjøre et mobilt arbeidsområde for aktivastyring som arbeidere kan bruke til å utføre aktivastyringsoppgaver.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837783"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="63e87-103">Konfigurere det mobile arbeidsområdet Aktivastyring</span><span class="sxs-lookup"><span data-stu-id="63e87-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63e87-104">Dette emnet beskriver hvordan du konfigurerer Microsoft Dynamics 365 Supply Chain Management og mobilappen Finance and Operations (Dynamics 365) slik at de kan kjøre et mobilt arbeidsområde for **Aktivastyring** som arbeidere kan bruke til å utføre aktivastyringsoppgaver.</span><span class="sxs-lookup"><span data-stu-id="63e87-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="63e87-105">Konfigurere vedlikeholdspersoner som brukere i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="63e87-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="63e87-106">Følg denne fremgangsmåten for hver bruker som skal ha tilgang til det mobile arbeidsområdet for **Aktivastyring**.</span><span class="sxs-lookup"><span data-stu-id="63e87-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="63e87-107">I Supply Chain Management går du til **Personale \> Arbeidere** og kontrollerer at det finnes en arbeiderpost for brukeren du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="63e87-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="63e87-108">Opprett en ny arbeiderpost etter behov.</span><span class="sxs-lookup"><span data-stu-id="63e87-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="63e87-109">Gå til **Aktivastyring \> Oppsett \> Arbeidere \> Arbeidere**, og kontroller at arbeiderposten du identifiserte (eller opprettet) i det forrige trinnet, er tilordnet til en vedlikeholdspersonpost.</span><span class="sxs-lookup"><span data-stu-id="63e87-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="63e87-110">Opprett en ny vedlikeholdspersonpost etter behov, og angi arbeiderposten fra forrige trinn i **Arbeider**-feltet.</span><span class="sxs-lookup"><span data-stu-id="63e87-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="63e87-111">Gå til **Aktivastyring \> Oppsett \> Arbeidere \> Vedlikeholdspersongrupper**, og kontroller at vedlikeholdspersonposten du identifiserte (eller opprettet) i det forrige trinnet, er hører til i en vedlikeholdspersongruppe.</span><span class="sxs-lookup"><span data-stu-id="63e87-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="63e87-112">Gå til **Systemadministrasjon \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="63e87-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="63e87-113">Velg den relevante brukeren i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="63e87-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="63e87-114">Angi arbeiderkontoen du vil knytte til den gjeldende brukerkontoen, i **Person**-feltet i hurtigfanen **Brukerdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="63e87-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="63e87-115">Denne arbeiderkontoen skal være arbeiderposten du identifiserte (eller opprettet) i trinn 1 og tilordnet til en vedlikeholdspersonpost i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="63e87-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="63e87-116">Brukertillatelser og sikkerhetsroller gjelder for funksjonene i det mobile arbeidsområdet for **Aktivastyring** på samme som for funksjonene i brukergrensesnittet i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="63e87-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="63e87-117">Derfor må hver bruker du konfigurerer med tilgang til det mobile arbeidsområdet for **Aktivastyring**, ha sikkerhetsrollene som kreves for å utføre lignende operasjoner direkte i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="63e87-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="63e87-118">Publisere det mobile arbeidsområdet Aktivastyring</span><span class="sxs-lookup"><span data-stu-id="63e87-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="63e87-119">Hvis du vil gjøre funksjoner for aktivastyring tilgjengelige i mobilappen Finance and Operations (Dynamics 365), må du publisere det mobile arbeidsområdet for **Aktivastyring**.</span><span class="sxs-lookup"><span data-stu-id="63e87-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="63e87-120">I Supply Chain Management velger du **Innstillinger**-knappen (tannhjulsymbolet i øvre høyre hjørne), og deretter velger du **Mobilapp** på menyen.</span><span class="sxs-lookup"><span data-stu-id="63e87-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="63e87-121">Finn flisen **Aktivastyring** i dialogboksen **Administrer mobilapp**.</span><span class="sxs-lookup"><span data-stu-id="63e87-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="63e87-122">Hvis den inneholder teksten «I metadata – ikke publisert», er arbeidsområdet ennå ikke publisert.</span><span class="sxs-lookup"><span data-stu-id="63e87-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="63e87-123">Hvis den inneholder teksten «I metadata – publisert», er arbeidsområdet allerede publisert, og du kan hoppe over resten av denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="63e87-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="63e87-124">![Dialogboksen Administrer mobilapp](media/mobile-workspaces.png "Dialogboksen Administrer mobilapp")</span><span class="sxs-lookup"><span data-stu-id="63e87-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="63e87-125">Velg flisen **Aktivastyring**, og velg deretter **Publiser** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="63e87-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="63e87-126">Etter noen sekunder skal du få en varsling om at arbeidsområdet er publisert.</span><span class="sxs-lookup"><span data-stu-id="63e87-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="63e87-127">I tillegg skal teksten på flisen endres til «I metadata – publisert».</span><span class="sxs-lookup"><span data-stu-id="63e87-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="63e87-128">Installere og konfigurere mobilappen Finance and Operations (Dynamics 365)</span><span class="sxs-lookup"><span data-stu-id="63e87-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="63e87-129">Gå til en av følgende appbutikker for å installere **Microsoft Finance and Operations (Dynamics 365)** på mobilenheten:</span><span class="sxs-lookup"><span data-stu-id="63e87-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="63e87-130">For Google Android-enheter</span><span class="sxs-lookup"><span data-stu-id="63e87-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="63e87-131">For Apple IOS-enheter</span><span class="sxs-lookup"><span data-stu-id="63e87-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="63e87-132">Åpne appen Finance and Operations (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="63e87-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="63e87-133">Påloggingssiden skal vises.</span><span class="sxs-lookup"><span data-stu-id="63e87-133">The sign-in page should appear.</span></span> <span data-ttu-id="63e87-134">Angi URL-adressen din for Supply Chain Management i **Logg på**-feltet, eller velg en nylig URL-adresse i listen **Siste miljøer**, og trykk deretter på **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="63e87-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="63e87-135">![Påloggingsside](media/mobile-app-sign-in.png "Påloggingsside")</span><span class="sxs-lookup"><span data-stu-id="63e87-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="63e87-136">Hvis du blir bedt om å bekrefte tilkoblingen, merker du av for **Jeg forstår** og trykker deretter på **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="63e87-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="63e87-137">På siden **Velg en konto** bruker du Microsoft-kontoen til å logge deg på mobilprogrammet.</span><span class="sxs-lookup"><span data-stu-id="63e87-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="63e87-138">Siden **Arbeidsområder** vises.</span><span class="sxs-lookup"><span data-stu-id="63e87-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="63e87-139">Den viser alle de mobile arbeidsområdene som er publisert av Supply Chain Management-forekomsten din.</span><span class="sxs-lookup"><span data-stu-id="63e87-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="63e87-140">![Liste over arbeidsområder](media/mobile-app-workspaces.png "Liste over arbeidsområder")</span><span class="sxs-lookup"><span data-stu-id="63e87-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="63e87-141">Hvis du må endre den juridiske enheten (firmaet), trykker du på Meny-knappen (noen ganger kalt hamburgeren eller hamburgerknappen) i øvre venstre hjørne, og deretter trykker du på **Endre firma**.</span><span class="sxs-lookup"><span data-stu-id="63e87-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="63e87-142">![Endre den juridiske enheten](media/mobile-app-change-comp.png "Endre den juridiske enheten")</span><span class="sxs-lookup"><span data-stu-id="63e87-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="63e87-143">Velg arbeidsområdet du vil arbeide med, på **Arbeidsområder**-siden for å åpne det.</span><span class="sxs-lookup"><span data-stu-id="63e87-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="63e87-144">![Mobilt arbeidsområde for aktivabehandling](media/mobile-app-asset-workspace.png "Mobilt arbeidsområde for aktivabehandling")</span><span class="sxs-lookup"><span data-stu-id="63e87-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="63e87-145">Arbeide med det mobile arbeidsområdet Aktivastyring</span><span class="sxs-lookup"><span data-stu-id="63e87-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="63e87-146">Hvis du vil ha mer informasjon om hvordan du arbeider med det mobile arbeidsområdet for **Aktivastyring**, kan du se [Bruke det mobile arbeidsområdet Aktivastyring](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="63e87-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="63e87-147">Hvis du vil ha mer informasjon om mobilappen Finance and Operations (Dynamics 365), kan du gå til [Startside for mobilapp](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="63e87-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]