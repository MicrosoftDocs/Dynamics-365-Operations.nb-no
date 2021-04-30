---
title: Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering
description: Dette emnet beskriver hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c4d596f27ffe15a97dc04e2ce7e85d21f8e7161f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908401"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="8d71a-103">Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="8d71a-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d71a-104">Dette emnet beskriver hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.</span><span class="sxs-lookup"><span data-stu-id="8d71a-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="8d71a-105">Hvis du vil klargjøre Teams med informasjon fra Dynamics 365 Commerce og synkronisere oppgavebehandlingsfunksjonene mellom Teams og POS-programmet (salgsstedet), må du aktivere integreringsfunksjonene i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8d71a-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="8d71a-106">Når du aktiverer Teams-integrering, godtar du å dele dataene dine med Teams.</span><span class="sxs-lookup"><span data-stu-id="8d71a-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="8d71a-107">Data som deles med Teams, kan ligge i et annet land enn Commerce-dataene, og de kan være underlagt andre samsvarsstandarder.</span><span class="sxs-lookup"><span data-stu-id="8d71a-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="8d71a-108">Hvis du vil ha mer informasjon om disse endringene, kan du se [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="8d71a-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="8d71a-109">Hvis du vil ha informasjon om Microsofts personvernerklæringer, kan du se [Microsofts personvernerklæring](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="8d71a-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="8d71a-110">Aktiver Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="8d71a-110">Enable Teams integration</span></span>

<span data-ttu-id="8d71a-111">Før du kan aktivere Microsoft Teams-integrering med Commerce, må du registrere Teams-programmet med leieren i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="8d71a-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="8d71a-112">Følg denne fremgangsmåten for å registrere Teams-programmet med leieren i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="8d71a-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="8d71a-113">følg trinnene i [Hurtigstart: Registrer en app i Microsoft-identitetsplattformen](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) for å registrere Teams-appen med leieren i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="8d71a-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="8d71a-114">Kopier verdien for **App-ID (klient)** fra **Oversikt**-siden for den registrerte appen.</span><span class="sxs-lookup"><span data-stu-id="8d71a-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="8d71a-115">Du bruker denne verdien for å aktivere Teams-integrering i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8d71a-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="8d71a-116">Kopier sertifikatverdien som ble angitt da du [la til et sertifikat](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) i trinn 1.</span><span class="sxs-lookup"><span data-stu-id="8d71a-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="8d71a-117">Sertifikatet kalles også offentlig nøkkel eller programnøkkel.</span><span class="sxs-lookup"><span data-stu-id="8d71a-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="8d71a-118">Du bruker denne verdien for å aktivere Teams-integrering i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8d71a-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="8d71a-119">Følg denne fremgangsmåten for å aktivere Teams-integrering i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8d71a-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8d71a-120">Gå til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.</span><span class="sxs-lookup"><span data-stu-id="8d71a-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="8d71a-121">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="8d71a-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8d71a-122">Sett alternativet **Aktiver Microsoft Teams-integrering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8d71a-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="8d71a-123">I feltene **App-ID** og **Appnøkkel** angir du verdiene du fikk da du registrerte Teams-appen i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="8d71a-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="8d71a-124">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8d71a-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="8d71a-125">Illustrasjonen nedenfor viser et eksempel på konfigurasjonen av Teams-integrering i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8d71a-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Konfigurasjon av Teams-integrering i Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="8d71a-127">Deaktiver Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="8d71a-127">Disable Teams integration</span></span>

<span data-ttu-id="8d71a-128">Følg denne fremgangsmåten for å deaktivere Microsoft Teams-integrering i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8d71a-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8d71a-129">Gå til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.</span><span class="sxs-lookup"><span data-stu-id="8d71a-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="8d71a-130">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="8d71a-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="8d71a-131">Sett alternativet **Aktiver Microsoft Teams-integrering** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="8d71a-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="8d71a-132">Fjern verdiene fra feltene **App-ID** og **Appnøkkel**.</span><span class="sxs-lookup"><span data-stu-id="8d71a-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="8d71a-133">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8d71a-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="8d71a-134">Når du har deaktivert Teams-integrering med Commerce, vil ikke POS-terminaler lenger vise oppgaver som er publisert fra Teams-appen.</span><span class="sxs-lookup"><span data-stu-id="8d71a-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d71a-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8d71a-135">Additional resources</span></span>

[<span data-ttu-id="8d71a-136">Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="8d71a-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="8d71a-137">Klargjøring av Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d71a-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="8d71a-138">Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="8d71a-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="8d71a-139">Behandle brukerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8d71a-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="8d71a-140">Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8d71a-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="8d71a-141">Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="8d71a-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
