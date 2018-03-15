--- 
title: " Opprette, beregne og postere et utdrag for en detaljhandel"
description: "Denne prosedyren hjelper deg gjennom de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 33ebb28196baa9ae944dbd124274b05cb587fea4
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="05ec5-103"> Opprette, beregne og postere et utdrag for en detaljhandel</span><span class="sxs-lookup"><span data-stu-id="05ec5-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="05ec5-104">Denne prosedyren hjelper deg gjennom de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk.</span><span class="sxs-lookup"><span data-stu-id="05ec5-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="05ec5-105">Det finnes også satsvise jobber som kan konfigureres for de samme oppgavene.</span><span class="sxs-lookup"><span data-stu-id="05ec5-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="05ec5-106">Du finner fremgangsmåten for å konfigurere og kjøre de satsvise jobbene i andre emner.</span><span class="sxs-lookup"><span data-stu-id="05ec5-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="05ec5-107">Hvis du vil fullføre denne prosedyren, må du ha transaksjoner som ble fullført i POS, og deretter overført til Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="05ec5-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="05ec5-108">Denne registreringen bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="05ec5-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="05ec5-109">Denne fremgangsmåten kan referere til Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="05ec5-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="05ec5-110">Legg merke til at Dynamics AX nå kalles Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="05ec5-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="05ec5-111">Gå til Alle arbeidsområder > ..</span><span class="sxs-lookup"><span data-stu-id="05ec5-111">Go to All workspaces > ..</span></span> <span data-ttu-id="05ec5-112">> Finans for detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="05ec5-112">> Retail store financials.</span></span>
2. <span data-ttu-id="05ec5-113">Klikk Nytt utdrag.</span><span class="sxs-lookup"><span data-stu-id="05ec5-113">Click New statement.</span></span>
3. <span data-ttu-id="05ec5-114">Klikk rullegardinknappen i feltet Butikknummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="05ec5-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="05ec5-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="05ec5-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="05ec5-116">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="05ec5-116">Click OK.</span></span>
    * <span data-ttu-id="05ec5-117">Oppsett-gruppen inneholder innstillingene som styrer hvilke transaksjoner som inkluderes i utdraget, og hvordan de grupperes i utdragslinjene.</span><span class="sxs-lookup"><span data-stu-id="05ec5-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="05ec5-118">Du kan åpne Oppsett-gruppen og endre disse innstillingene, eller du kan bruke standardinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="05ec5-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="05ec5-119">Feltet Utdragsmetode angir hvordan utdragslinjene skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="05ec5-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="05ec5-120">Velg et stabsmedlem eller en kasse hvis du vil beregne et utdrag bare for bestemte stabsmedlemmer eller kasser.</span><span class="sxs-lookup"><span data-stu-id="05ec5-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="05ec5-121">Velg et alternativ i Avslutningsmetode-feltet.</span><span class="sxs-lookup"><span data-stu-id="05ec5-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="05ec5-122">Klikk Beregn utdrag.</span><span class="sxs-lookup"><span data-stu-id="05ec5-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="05ec5-123">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="05ec5-123">Click Yes.</span></span>
    * <span data-ttu-id="05ec5-124">Når du har beregnet utdraget, skal det være opprettet linjer med totalbeløp for hver betalingsmåte og utdragsmetode som ble brukt.</span><span class="sxs-lookup"><span data-stu-id="05ec5-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="05ec5-125">Angi et opptelt beløp i hver linje hvis den må angis eller oppdateres.</span><span class="sxs-lookup"><span data-stu-id="05ec5-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="05ec5-126">Telt opp-feltet fylles ut med beløp fra kasseoppgjør i POS.</span><span class="sxs-lookup"><span data-stu-id="05ec5-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="05ec5-127">Klikk Poster utdrag.</span><span class="sxs-lookup"><span data-stu-id="05ec5-127">Click Post statement.</span></span>
10. <span data-ttu-id="05ec5-128">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="05ec5-128">Click Close.</span></span>
11. <span data-ttu-id="05ec5-129">Gå til Detaljhandel og handel > Kanaler > Finans for detaljhandelsbutikk.</span><span class="sxs-lookup"><span data-stu-id="05ec5-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="05ec5-130">Klikk kategorien Posterte utdrag.</span><span class="sxs-lookup"><span data-stu-id="05ec5-130">Click the Posted statements tab.</span></span>


