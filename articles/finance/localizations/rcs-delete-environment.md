---
title: Regulatory Configuration Service (RCS) – Slette et RCS-miljø
description: Dette emnet beskriver hvordan en systemadministrator for Regulatory Configuration Service (RCS) kan slette et RCS-miljø og tilknyttede data.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295824"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="74e27-103">Regulatory Configuration Service (RCS) – Slette et RCS-miljø</span><span class="sxs-lookup"><span data-stu-id="74e27-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74e27-104">Dette emnet beskriver hvordan en systemadministrator for Regulatory Configuration Service (RCS) kan slette et RCS-miljø og tilknyttede data.</span><span class="sxs-lookup"><span data-stu-id="74e27-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="74e27-105">Før du kan fullføre trinnene i dette emnet må følgende forutsetninger være på plass:</span><span class="sxs-lookup"><span data-stu-id="74e27-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="74e27-106">Du må ha **Systemadministrator**-rollen tilordnet deg for RCS-miljøet.</span><span class="sxs-lookup"><span data-stu-id="74e27-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="74e27-107">**Systemadministrator**-rollen må ha rollen **RCSDeleteEnvironmentDuty** tilordnet.</span><span class="sxs-lookup"><span data-stu-id="74e27-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="74e27-108">Slette et RCS-miljø</span><span class="sxs-lookup"><span data-stu-id="74e27-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="74e27-109">Åpne RCS, og velg arbeidsområdeflisen **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="74e27-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="74e27-110">Velg **Slett RCS-miljø** i delen **Relaterte koblinger**.</span><span class="sxs-lookup"><span data-stu-id="74e27-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![Slette RCS-miljø-kobling i delen Relaterte koblinger](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="74e27-112">I dialogboksen som vises, kan du se gjennom meldingene om omfanget av sletting av miljøet.</span><span class="sxs-lookup"><span data-stu-id="74e27-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Meldinger i dialogboksen Slett RCS-miljø](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="74e27-114">Sletting av et RCS-miljø kan ikke tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="74e27-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="74e27-115">Operasjonen sletter det valgte RCS-miljøet og alle relaterte data, inkludert funksjoner og konfigurasjoner som er lagret i det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="74e27-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="74e27-116">Funksjoner og konfigurasjoner som deles med andre organisasjoner, blir ikke delt og slettet hvis de ikke har noen avhengigheter.</span><span class="sxs-lookup"><span data-stu-id="74e27-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="74e27-117">Funksjoner og konfigurasjoner som har avhengigheter, merkes som avsluttet.</span><span class="sxs-lookup"><span data-stu-id="74e27-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="74e27-118">I feltet som oppgis, angir du globalt unik identifikator (GUID) for RCS-miljøet for å bekrefte at du vil slette det.</span><span class="sxs-lookup"><span data-stu-id="74e27-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="74e27-119">Miljøets GUID tas med i slettingsmeldingen.</span><span class="sxs-lookup"><span data-stu-id="74e27-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="74e27-120">Velg **Slett miljø**.</span><span class="sxs-lookup"><span data-stu-id="74e27-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="74e27-121">RCS-miljøet og eventuelle tilknyttede data blir nå slettet.</span><span class="sxs-lookup"><span data-stu-id="74e27-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74e27-122">Etter at du har slettet et RCS-miljø, finnes det ingen måte å gjenopprette dataene på.</span><span class="sxs-lookup"><span data-stu-id="74e27-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="74e27-123">Et nytt RCS-miljø kan opprettes i et hvilket som helst tilgjengelig RCS-område.</span><span class="sxs-lookup"><span data-stu-id="74e27-123">A new RCS environment can be created in any available RCS region.</span></span>
