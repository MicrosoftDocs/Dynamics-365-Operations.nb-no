---
title: Opprett en Internett-funksjonalitetsprofil
description: Dette emnet beskriver hvordan du oppretter en Internett-funksjonalitetsprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414766"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="7c732-103">Opprett en Internett-funksjonalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="7c732-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7c732-104">Dette emnet viser en oversikt over hvordan du konfigurerer en Internett-funksjonalitetsprofil for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7c732-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7c732-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="7c732-105">Overview</span></span>

<span data-ttu-id="7c732-106">Internett-funksjonalitetsprofilen inneholder ulike innstillinger som brukes for Internett-kanaler.</span><span class="sxs-lookup"><span data-stu-id="7c732-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="7c732-107">Hver Internett-kanal må angi en Internett-funksjonalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="7c732-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="7c732-108">Opprett en Internett-funksjonalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="7c732-108">Create an online functionality profile</span></span>

<span data-ttu-id="7c732-109">Prosedyren nedenfor forklarer hvordan du oppretter en Internett-funksjonalitetsprofil fra Commerce Headquarters-appen.</span><span class="sxs-lookup"><span data-stu-id="7c732-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="7c732-110">I navigasjonsruten går du til **Moduler \> Kanaloppsett \> Oppsett av nettbutikk \> Funksjonalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="7c732-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="7c732-111">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7c732-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c732-112">I **Profil**-feltet angir du en ID for profilen.</span><span class="sxs-lookup"><span data-stu-id="7c732-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="7c732-113">I **Beskrivelse**-feltet skriver du inn en verdi ("Adventure Works-profil" i eksempelbildet nedenfor).</span><span class="sxs-lookup"><span data-stu-id="7c732-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="7c732-114">I **Funksjoner**-delen endrer du innstillingene for **HANDLEKURV**, **DETALJHANDELSKUNDER** eller **UTSJEKKING** etter behov.</span><span class="sxs-lookup"><span data-stu-id="7c732-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="7c732-115">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7c732-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7c732-116">Bildet nedenfor viser et eksempel på en Internett-funksjonalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="7c732-116">The following image shows an example online functionality profile.</span></span>
  
![Eksempel på Internett-funksjonalitetsprofil](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="7c732-118">Funksjoner</span><span class="sxs-lookup"><span data-stu-id="7c732-118">Functions</span></span>

- <span data-ttu-id="7c732-119">**Slå sammen produkter**: Når denne funksjonen er aktivert, kan antallet i handlekurven oppdateres når den samme varen legges til flere ganger.</span><span class="sxs-lookup"><span data-stu-id="7c732-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="7c732-120">**Tillat utsjekking uten betalinger**: Når dette er aktivert, håndterer funksjonen scenarioet når varer som legges til i handlekurven, har en pris på 0,00.</span><span class="sxs-lookup"><span data-stu-id="7c732-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="7c732-121">**Opprett kunde i asynkron modus**: Dette er en eldre innstilling som gjelder for tredjeparts e-handelskanaler, og som ikke gjelder for e-handelsområdet i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7c732-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c732-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7c732-122">Additional resources</span></span>

[<span data-ttu-id="7c732-123">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="7c732-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7c732-124">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="7c732-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7c732-125">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="7c732-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7c732-126">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="7c732-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="7c732-127">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="7c732-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
