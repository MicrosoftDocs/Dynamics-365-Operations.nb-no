---
title: Du blir bedt om å lagre varedekningsinnstillinger selv om du ikke har gjort noen endringer
description: Du blir bedt om å lagre varedekningsinnstillinger selv om du ikke har gjort noen endringer.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049482"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="7a156-103">Du blir bedt om å lagre varedekningsinnstillinger selv om du ikke har gjort noen endringer</span><span class="sxs-lookup"><span data-stu-id="7a156-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="7a156-104">KB-nummer: 4615588</span><span class="sxs-lookup"><span data-stu-id="7a156-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="7a156-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7a156-105">Symptoms</span></span>

<span data-ttu-id="7a156-106">I noen scenarier kan det hende at du får følgende melding når du åpner siden **Varedekning** etter at du har importert varer via enheten *Varedekning V2*:</span><span class="sxs-lookup"><span data-stu-id="7a156-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="7a156-107">Vil du lagre endringer før du lukker?</span><span class="sxs-lookup"><span data-stu-id="7a156-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="7a156-108">Du får denne meldingen selv om du ikke har gjort noen endringer.</span><span class="sxs-lookup"><span data-stu-id="7a156-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="7a156-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="7a156-109">Resolution</span></span>

<span data-ttu-id="7a156-110">**Varedekning**-siden inneholder kompleks standardlogikk som kan føre til at meldingen vises etter at det nylig er gjort direkte endringer i databasen, for eksempel gjennom enhetsimport.</span><span class="sxs-lookup"><span data-stu-id="7a156-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="7a156-111">Enhetsfeltet `AREGENERALSETTINGSOVERRIDDEN` er for eksempel satt til *Nei*, men du importerer en fil som inneholder nye eller endrede verdier for felt som for eksempel `PRODUCTCOVERAGEGROUPID` og/eller `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="7a156-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="7a156-112">I dette tilfellet, fordi feltet `AREGENERALSETTINGSOVERRIDDEN` er satt til *Nei*, tømmes verdiene automatisk fra feltene når du åpner **Varedekning**-siden for første gang etter importen.</span><span class="sxs-lookup"><span data-stu-id="7a156-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="7a156-113">Hvis du lagrer endringene som meldingsboksledetekst, lagres de i databasen.</span><span class="sxs-lookup"><span data-stu-id="7a156-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="7a156-114">Ellers får du samme melding neste gang du åpner siden.</span><span class="sxs-lookup"><span data-stu-id="7a156-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="7a156-115">Hvis du vil hindre denne virkemåten, men også ta med verdier for felt som `PRODUCTCOVERAGEGROUPID` gjennom enhetsimport, kan du sette `AREGENERALSETTINGSOVERRIDDEN` til *Ja* når du importerer.</span><span class="sxs-lookup"><span data-stu-id="7a156-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
