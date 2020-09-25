---
title: Synkronisere ressurskapasitet
description: Dette emnet inneholder informasjon om hvordan du synkroniserer kapasiteten til en ressurs på tvers av kalendere og prosjekter.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760622"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="c14b5-103">Synkronisere ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="c14b5-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c14b5-104">Prosessene for ressurssynkronisering sikrer at informasjon for kalenderen og grunnkalenderen slår ned i prosjektressursplanlegging.</span><span class="sxs-lookup"><span data-stu-id="c14b5-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="c14b5-105">Hvis kalenderen er endret, vil prosessene foreta de nødvendige oppdateringene i planleggingen av prosjektressurser.</span><span class="sxs-lookup"><span data-stu-id="c14b5-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="c14b5-106">Prosessene bidrar også til å forbedre ytelsen, fordi kalenderens ressursinformasjon er synkronisert på forhånd.</span><span class="sxs-lookup"><span data-stu-id="c14b5-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="c14b5-107">Derfor opptrer oppdateringer til ressursplanleggingsinformasjon raskere.</span><span class="sxs-lookup"><span data-stu-id="c14b5-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="c14b5-108">Vi anbefaler at du planlegger prosessene som en satsvis jobb i stedet for én om gangen.</span><span class="sxs-lookup"><span data-stu-id="c14b5-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="c14b5-109">Ellers er det fare for at noen glemmer datoene da informasjonen ble sist synkronisert.</span><span class="sxs-lookup"><span data-stu-id="c14b5-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="c14b5-110">Hvis inklusive datoer ikke brukes, kan det oppstå mellomrom under synkronisering av dato.</span><span class="sxs-lookup"><span data-stu-id="c14b5-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="c14b5-112">Synkroniser opprullinger av ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="c14b5-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="c14b5-113">Synkroniseringsprosessen er utformet for å synkronisere all kalenderinformasjon for ressursen.</span><span class="sxs-lookup"><span data-stu-id="c14b5-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="c14b5-114">Denne informasjonen inneholder grunnkalenderinformasjon om eventuelle endringer i prosjektets kapasitetstabell i ressurskalender.</span><span class="sxs-lookup"><span data-stu-id="c14b5-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="c14b5-115">Hvis det legges til nye ressurser i prosjektet, synkronisering bidrar til å sikre at det finnes oppdatert kalenderinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="c14b5-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="c14b5-116">Denne synkroniseringen kan utføres når som helst.</span><span class="sxs-lookup"><span data-stu-id="c14b5-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="c14b5-117">Vi anbefaler at du bruker et parti.</span><span class="sxs-lookup"><span data-stu-id="c14b5-117">We recommend that you use a batch.</span></span> <span data-ttu-id="c14b5-118">Alternativene er tilgjengelige under synkronisering av kapasitetsreservasjoner.</span><span class="sxs-lookup"><span data-stu-id="c14b5-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="c14b5-119">Velg **Prosjektstyring og regnskap** &gt; **Periodisk** &gt; **Kapasitetssynkronisering** &gt; **Synkroniser opprullinger av ressuskapasitet**.</span><span class="sxs-lookup"><span data-stu-id="c14b5-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="c14b5-120">Sett alternativene i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="c14b5-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="c14b5-121">Alternativ</span><span class="sxs-lookup"><span data-stu-id="c14b5-121">Option</span></span>      | <span data-ttu-id="c14b5-122">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c14b5-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="c14b5-123">Periodekode</span><span class="sxs-lookup"><span data-stu-id="c14b5-123">Period code</span></span> | <span data-ttu-id="c14b5-124">Velg valgfritt intervallkoden for hovedboken for å angi start- og sluttdatoer for synkroniseringsprosessen for opprullinger av ressurskapasitet.</span><span class="sxs-lookup"><span data-stu-id="c14b5-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="c14b5-125">Startdato</span><span class="sxs-lookup"><span data-stu-id="c14b5-125">Start date</span></span>  | <span data-ttu-id="c14b5-126">Skriv inn startdato for synkroniseringsprosessen for opprullinger av ressurskapasitet.</span><span class="sxs-lookup"><span data-stu-id="c14b5-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="c14b5-127">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="c14b5-127">End date</span></span>    | <span data-ttu-id="c14b5-128">Skriv inn sluttdato for synkroniseringsprosessen for opprullinger av ressurskapasitet.</span><span class="sxs-lookup"><span data-stu-id="c14b5-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="c14b5-129">[![Synkroniseringsprosess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="c14b5-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
