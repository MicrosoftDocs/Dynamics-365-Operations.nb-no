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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1b0afeabfecb60672156692f3cd809445624020c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969982"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="ecf33-103">Opprett en Internett-funksjonalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="ecf33-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ecf33-104">Dette emnet viser en oversikt over hvordan du konfigurerer en Internett-funksjonalitetsprofil for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ecf33-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ecf33-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ecf33-105">Overview</span></span>

<span data-ttu-id="ecf33-106">Internett-funksjonalitetsprofilen inneholder ulike innstillinger som brukes for Internett-kanaler.</span><span class="sxs-lookup"><span data-stu-id="ecf33-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="ecf33-107">Hver Internett-kanal må angi en Internett-funksjonalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="ecf33-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="ecf33-108">Opprett en Internett-funksjonalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="ecf33-108">Create an online functionality profile</span></span>

<span data-ttu-id="ecf33-109">Prosedyren nedenfor forklarer hvordan du oppretter en Internett-funksjonalitetsprofil fra Commerce Headquarters-appen.</span><span class="sxs-lookup"><span data-stu-id="ecf33-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="ecf33-110">I navigasjonsruten går du til **Moduler \> Kanaloppsett \> Oppsett av nettbutikk \> Funksjonalitetsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="ecf33-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="ecf33-111">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ecf33-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ecf33-112">I **Profil**-feltet angir du en ID for profilen.</span><span class="sxs-lookup"><span data-stu-id="ecf33-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="ecf33-113">I **Beskrivelse**-feltet skriver du inn en verdi ("Adventure Works-profil" i eksempelbildet nedenfor).</span><span class="sxs-lookup"><span data-stu-id="ecf33-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="ecf33-114">I **Funksjoner**-delen endrer du innstillingene for **HANDLEKURV**, **DETALJHANDELSKUNDER** eller **UTSJEKKING** etter behov.</span><span class="sxs-lookup"><span data-stu-id="ecf33-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="ecf33-115">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ecf33-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ecf33-116">Bildet nedenfor viser et eksempel på en Internett-funksjonalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="ecf33-116">The following image shows an example online functionality profile.</span></span>
  
![Eksempel på Internett-funksjonalitetsprofil](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="ecf33-118">Funksjoner</span><span class="sxs-lookup"><span data-stu-id="ecf33-118">Functions</span></span>

- <span data-ttu-id="ecf33-119">**Slå sammen produkter**: Når denne funksjonen er aktivert, kan antallet i handlekurven oppdateres når den samme varen legges til flere ganger.</span><span class="sxs-lookup"><span data-stu-id="ecf33-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="ecf33-120">**Tillat utsjekking uten betalinger**: Når dette er aktivert, håndterer funksjonen scenarioet når varer som legges til i handlekurven, har en pris på 0,00.</span><span class="sxs-lookup"><span data-stu-id="ecf33-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="ecf33-121">**Opprett kunde i asynkron modus**: Dette er en eldre innstilling som gjelder for tredjeparts e-handelskanaler, og som ikke gjelder for e-handelsområdet i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ecf33-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ecf33-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ecf33-122">Additional resources</span></span>

[<span data-ttu-id="ecf33-123">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="ecf33-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ecf33-124">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="ecf33-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ecf33-125">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="ecf33-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="ecf33-126">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="ecf33-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="ecf33-127">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="ecf33-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
