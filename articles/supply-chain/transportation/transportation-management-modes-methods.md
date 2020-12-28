---
title: Moduser og metoder for transportstyring
description: Dette emnet viser hvordan du definerer moduser og metoder for transportstyring.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: ceb3930cdb7764f846e88edfff6906b902a7f5fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434873"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="1ff84-103">Moduser og metoder for transportstyring</span><span class="sxs-lookup"><span data-stu-id="1ff84-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ff84-104">Transportstyringsmodusen representerer typen transport som transportøren bruker for fraktleveringer, for eksempel LTL, TL eller pakke.</span><span class="sxs-lookup"><span data-stu-id="1ff84-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="1ff84-105">Transportmetoden representerer typen transport som transportøren bruker for fraktleveringer, for eksempel fly, land, hav eller tog.</span><span class="sxs-lookup"><span data-stu-id="1ff84-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="1ff84-106">Moduser og transportmetoder brukes i flere kontekster.</span><span class="sxs-lookup"><span data-stu-id="1ff84-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="1ff84-107">Bare moduser brukes i ruteplaner, mens både moduser og transportmetoder brukes når du konfigurerer transportører og transportørtjenester.</span><span class="sxs-lookup"><span data-stu-id="1ff84-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="1ff84-108">Det finnes ingen eksplisitte relasjoner eller hierarkier mellom moduser og transportmetoder.</span><span class="sxs-lookup"><span data-stu-id="1ff84-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="1ff84-109">Opprette en modus</span><span class="sxs-lookup"><span data-stu-id="1ff84-109">Create a mode</span></span>

<span data-ttu-id="1ff84-110">Følg trinnene nedenfor for å opprette en modus:</span><span class="sxs-lookup"><span data-stu-id="1ff84-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="1ff84-111">Gå til **Transportstyring \> Oppsett \> Transportører \> Modus**.</span><span class="sxs-lookup"><span data-stu-id="1ff84-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="1ff84-112">Velg **Ny** for å opprette en ny modus.</span><span class="sxs-lookup"><span data-stu-id="1ff84-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="1ff84-113">Angi en unik ID og et beskrivende navn for modusen.</span><span class="sxs-lookup"><span data-stu-id="1ff84-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="1ff84-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1ff84-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="1ff84-115">Opprette en transportmetode</span><span class="sxs-lookup"><span data-stu-id="1ff84-115">Create a transportation method</span></span>

<span data-ttu-id="1ff84-116">Hvis du vil opprette en transportmetode, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="1ff84-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="1ff84-117">Gå til **Transportstyring \> Oppsett \> Transportører \> Transportmetoder**.</span><span class="sxs-lookup"><span data-stu-id="1ff84-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="1ff84-118">Velg **Ny** for å opprette en ny transportmetode.</span><span class="sxs-lookup"><span data-stu-id="1ff84-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="1ff84-119">Angi en unik ID og et beskrivende navn for transportmetoden.</span><span class="sxs-lookup"><span data-stu-id="1ff84-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="1ff84-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1ff84-120">Close the page.</span></span>
