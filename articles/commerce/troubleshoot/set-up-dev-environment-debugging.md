---
title: Konfigurere et utviklingsmiljø for e-handel for feilsøking mot en virtuell maskin for Retail Server på Lag 1
description: Dette emnet forklarer hvordan du konfigurerer et utviklingsmiljø for e-handel for feilsøking mot en virtuell maskin (VM) for Retail Server på Lag 1.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801489"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="d5f63-103">Konfigurere et utviklingsmiljø for e-handel for feilsøking mot en virtuell maskin for Retail Server på Lag 1</span><span class="sxs-lookup"><span data-stu-id="d5f63-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5f63-104">Dette emnet forklarer hvordan du konfigurerer et utviklingsmiljø for e-handel for feilsøking mot en virtuell maskin (VM) for Retail Server på Lag 1.</span><span class="sxs-lookup"><span data-stu-id="d5f63-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="d5f63-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d5f63-105">Description</span></span>

<span data-ttu-id="d5f63-106">Microsoft Dynamics 365 Commerce Lag 1-miljøer distribueres vanligvis for Commerce Runtime (CRT) og utvikling av POS-utvidelse (point of sale).</span><span class="sxs-lookup"><span data-stu-id="d5f63-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="d5f63-107">De er frittstående miljøer.</span><span class="sxs-lookup"><span data-stu-id="d5f63-107">They are standalone environments.</span></span> <span data-ttu-id="d5f63-108">På grunn av SaaS (software as a service) i arkitekturen, omfatter de ikke e-handelkomponenter.</span><span class="sxs-lookup"><span data-stu-id="d5f63-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="d5f63-109">I noen scenarioer vil du kanskje teste kall til utvidelser i et Lag 1-miljø, slik at du kan feilsøke utvidelser fra e-commerce-komponenter.</span><span class="sxs-lookup"><span data-stu-id="d5f63-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="d5f63-110">For generelle instruksjoner kan du se [Feilsøke mot et Commerce-utviklingsmiljø på lag 1](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="d5f63-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="d5f63-111">Når du feilsøker mot et Lag 1-miljø, ettersom området nå kaller en annen Retail Server, kan kall på tvers av servere forårsake ulike feil som er knyttet til innholdssikkerhetspolicyen.</span><span class="sxs-lookup"><span data-stu-id="d5f63-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="d5f63-112">Illustrasjonen nedenfor viser et eksempel på en feil som kan oppstå når en variant er valgt på en produktdetaljerside.</span><span class="sxs-lookup"><span data-stu-id="d5f63-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Feil når en variant er valgt på en produktdetaljerside](media/unhandled-rejection-error.jpg)

<span data-ttu-id="d5f63-114">Illustrasjonen nedenfor viser et eksempel på en lignende feil i webleserens feilsøkingsverktøy (F12 Developer Tools).</span><span class="sxs-lookup"><span data-stu-id="d5f63-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="d5f63-115">Feilmeldingen nevner et brudd på direktivet for innholdssikkerhetspolicy.</span><span class="sxs-lookup"><span data-stu-id="d5f63-115">The error message mentions violation of the content security policy directive.</span></span>

![Feil under feilsøkingsverktøy](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="d5f63-117">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="d5f63-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="d5f63-118">Deaktivere innholdssikkerhetspolicy for området i Commerce-områdebyggeren</span><span class="sxs-lookup"><span data-stu-id="d5f63-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="d5f63-119">Velg området du arbeider på.</span><span class="sxs-lookup"><span data-stu-id="d5f63-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="d5f63-120">Velg **Innstillinger** og deretter **Utvidelser**.</span><span class="sxs-lookup"><span data-stu-id="d5f63-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="d5f63-121">Velg **Deaktiver innholdssikkerhetspolicy** i fanen **Innholdssikkerhetspolicy**.</span><span class="sxs-lookup"><span data-stu-id="d5f63-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="d5f63-122">Velg **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="d5f63-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="d5f63-123">B2C-pålogging (Business-to-consumer) vil ikke fungere i et lokalt utviklingsmiljø.</span><span class="sxs-lookup"><span data-stu-id="d5f63-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="d5f63-124">Du kan imidlertid bruke gjesteutsjekkinger eller lage sidesimuleringer for å etterligne en brukers pålogging etter behov.</span><span class="sxs-lookup"><span data-stu-id="d5f63-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5f63-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d5f63-125">Additional resources</span></span>

[<span data-ttu-id="d5f63-126">Komme i gang med omfattende elektronisk utvikling av e-handel</span><span class="sxs-lookup"><span data-stu-id="d5f63-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="d5f63-127">Behandle innholdssikkerhetspolicy (CSP) på e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="d5f63-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
