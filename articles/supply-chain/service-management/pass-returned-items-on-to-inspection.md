---
title: Sende returnerte varer til inspeksjon
description: Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70aafb752b2c847d5d48236fd5d201a73e088c24
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "334088"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="4ebe9-103">Sende returnerte varer til inspeksjon</span><span class="sxs-lookup"><span data-stu-id="4ebe9-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4ebe9-104">Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.</span><span class="sxs-lookup"><span data-stu-id="4ebe9-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="4ebe9-105">Klikk **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Vareankomst**.</span><span class="sxs-lookup"><span data-stu-id="4ebe9-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="4ebe9-106">\-eller-</span><span class="sxs-lookup"><span data-stu-id="4ebe9-106">\-or-</span></span>
    
    <span data-ttu-id="4ebe9-107">Klikk **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Produksjonsinnlevering**.</span><span class="sxs-lookup"><span data-stu-id="4ebe9-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="4ebe9-108">I skjemaet **Lokasjonsjournal** registrerer du mottaket av varen på vanlig måte.</span><span class="sxs-lookup"><span data-stu-id="4ebe9-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="4ebe9-109">Hvis du vil ha informasjon om hvordan du registrerer mottak av returnerte varer, kan du se <A href="register-the-receipt-of-returned-items.md">Registrere mottaket av returnerte varer</A>.</span><span class="sxs-lookup"><span data-stu-id="4ebe9-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="4ebe9-110">På fanen **Standardverdier** i området **Behandlingsmåte** merker du av for **Karantenestyring**.</span><span class="sxs-lookup"><span data-stu-id="4ebe9-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="4ebe9-111">Nå vil systemet opprette en karanteneordre, og personen eller avdelingen som utfører inspeksjoner, vil svare på denne ordren ved hjelp av **Karanteneordre**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="4ebe9-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ebe9-112">Se også</span><span class="sxs-lookup"><span data-stu-id="4ebe9-112">See also</span></span>

[<span data-ttu-id="4ebe9-113">Ta returnerte varer gjennom inspeksjon</span><span class="sxs-lookup"><span data-stu-id="4ebe9-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="4ebe9-114">Angi hvordan du kvitter deg med returnerte varer</span><span class="sxs-lookup"><span data-stu-id="4ebe9-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

