---
title: Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering
description: Dette emnet inneholder svar på vanlige spørsmål knyttet til Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019476"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="27e86-103">Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="27e86-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="27e86-104">Dette emnet inneholder svar på vanlige spørsmål knyttet til Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.</span><span class="sxs-lookup"><span data-stu-id="27e86-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="27e86-105">Hvem i butikken blir eier av et team under klargjøring av Teams fra Commerce?</span><span class="sxs-lookup"><span data-stu-id="27e86-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="27e86-106">Alle butikksjefer legges automatisk til som eiere i den tilsvarende gruppen, slik at de kan utføre operasjoner, for eksempel legge til en privat kanal og legge til eller slette medlemmer.</span><span class="sxs-lookup"><span data-stu-id="27e86-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="27e86-107">Hvordan tilordner jeg rollen "kommunikasjonsansvarlig" til en ansatt i Commerce Headquarters?</span><span class="sxs-lookup"><span data-stu-id="27e86-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="27e86-108">Kommunikasjonsledere i Microsoft Teams har muligheten til å opprette og publisere oppgavelister.</span><span class="sxs-lookup"><span data-stu-id="27e86-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="27e86-109">Organisasjonsansatte som må bli kommunikasjonsansvarlige, må ha tilordnet rollen "Retail-oppgaveleder" i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="27e86-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="27e86-110">Følg denne fremgangsmåten for å tilordne rollen Retail-oppgaveleder til en ansatt i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="27e86-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="27e86-111">Gå til **Retail og Commerce \> Ansatte \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="27e86-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="27e86-112">Velg en ansatt.</span><span class="sxs-lookup"><span data-stu-id="27e86-112">Select an employee.</span></span>
1. <span data-ttu-id="27e86-113">På hurtigfanen **Brukerens roller** velger du **Tilordne roller**.</span><span class="sxs-lookup"><span data-stu-id="27e86-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="27e86-114">I dialogboksen **Tilordne roller til bruker** velger du rollen **Retail-oppgaveleder** og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="27e86-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="27e86-115">Hvordan gjør jeg et bestemt organisasjonshierarki tilgjengelig for opplasting til Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="27e86-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="27e86-116">I Commerce Headquarters er hver organisasjons hierarki knyttet til ett eller flere formål.</span><span class="sxs-lookup"><span data-stu-id="27e86-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="27e86-117">Kontroller at hierarkiet du vil klargjøre i Microsoft Teams, har formålet **Detaljhandelsrapportering** knyttet til seg, som vist i følgende eksempelbilde.</span><span class="sxs-lookup"><span data-stu-id="27e86-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Eksempel på et organisasjonshierarkiformål i Commerce Headquarters](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="27e86-119">Hvordan aktiverer jeg detaljhandelsarbeidere for å logge seg på Commerce POS (salgssted) ved hjelp av Azure Active Directory (Azure AD)?</span><span class="sxs-lookup"><span data-stu-id="27e86-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="27e86-120">Hvis du vil ha mer informasjon om hvordan du konfigurerer påloggingsopplevelsen for Commerce POS for å bruke Azure AD-godkjenning, kan du se [Aktiver Azure Active Directory-godkjenning for POS-pålogging](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="27e86-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="27e86-121">Hvordan tilordner jeg butikker og tilsvarende grupper i Commerce Headquarters hvis organisasjonen allerede har opprettet grupper i Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="27e86-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="27e86-122">Hvis du vil ha informasjon om hvordan du tilordner butikker og grupper hvis det finnes allerede eksisterende grupper, kan du se [Tilordne butikker og tilsvarende grupper hvis organisasjonen allerede har eksisterende grupper i Microsoft Teams](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="27e86-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="27e86-123">Hvordan fjerner jeg merket for Microsoft Graph API-tokenet som er lagret i øktlageret?</span><span class="sxs-lookup"><span data-stu-id="27e86-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="27e86-124">En bruker som har logget seg på salgsstedet med en Azure Active Directory-konto (Azure AD), må logge seg ut fra POS-systemet eller lukke programmet for å tømme øktlageret.</span><span class="sxs-lookup"><span data-stu-id="27e86-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="27e86-125">En anbefalt fremgangsmåte er at butikkarbeidere alltid låser salgsstedsterminalen eller logger seg ut fra en økt når terminalen ikke brukes.</span><span class="sxs-lookup"><span data-stu-id="27e86-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="27e86-126">Hva skjer hvis en butikk ikke har butikksjefer?</span><span class="sxs-lookup"><span data-stu-id="27e86-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="27e86-127">Hvis en butikk ikke har ledere, opprettes det ikke en gruppe for butikken eller i Teams.</span><span class="sxs-lookup"><span data-stu-id="27e86-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="27e86-128">Hva skjer hvis en butikksjef forlater firmaet?</span><span class="sxs-lookup"><span data-stu-id="27e86-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="27e86-129">Alle som har eierrollen, kan legge til en ny butikksjef i Commerce Headquarters og klargjøre Teams på nytt, slik at den nye lederen får de nødvendige rettighetene i Teams for gruppen.</span><span class="sxs-lookup"><span data-stu-id="27e86-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="27e86-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="27e86-130">Additional resources</span></span>

[<span data-ttu-id="27e86-131">Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="27e86-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="27e86-132">Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="27e86-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="27e86-133">Klargjøring av Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="27e86-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="27e86-134">Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="27e86-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="27e86-135">Behandle brukerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="27e86-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="27e86-136">Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="27e86-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
