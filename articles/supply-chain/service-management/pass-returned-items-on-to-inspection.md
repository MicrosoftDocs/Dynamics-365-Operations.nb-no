---
title: Sende returnerte varer til inspeksjon
description: Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04b27a5560b6126fde3028f653a89059bb765844
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254971"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="48cd1-103">Sende returnerte varer til inspeksjon</span><span class="sxs-lookup"><span data-stu-id="48cd1-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="48cd1-104">Når du registrerer en returnert vare, kan du beslutte at den bør sendes til inspeksjon før den returneres til lager eller avhendes på en annen måte.</span><span class="sxs-lookup"><span data-stu-id="48cd1-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="48cd1-105">Klikk på **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Vareankomst**.</span><span class="sxs-lookup"><span data-stu-id="48cd1-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="48cd1-106">\-eller-</span><span class="sxs-lookup"><span data-stu-id="48cd1-106">\-or-</span></span>
    
    <span data-ttu-id="48cd1-107">Klikk på **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Produksjonsinnlevering**.</span><span class="sxs-lookup"><span data-stu-id="48cd1-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="48cd1-108">I skjemaet **Lokasjonsjournal** registrerer du mottaket av varen på vanlig måte.</span><span class="sxs-lookup"><span data-stu-id="48cd1-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="48cd1-109">Hvis du vil ha informasjon om hvordan du registrerer mottak av returnerte varer, kan du se <A href="register-the-receipt-of-returned-items.md">Registrere mottaket av returnerte varer</A>.</span><span class="sxs-lookup"><span data-stu-id="48cd1-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="48cd1-110">På fanen **Standardverdier** i området **Behandlingsmåte** merker du av for **Karantenestyring**.</span><span class="sxs-lookup"><span data-stu-id="48cd1-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="48cd1-111">Nå vil systemet opprette en karanteneordre, og personen eller avdelingen som utfører inspeksjoner, vil svare på denne ordren ved hjelp av **Karanteneordre**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="48cd1-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="48cd1-112">Se også</span><span class="sxs-lookup"><span data-stu-id="48cd1-112">See also</span></span>

[<span data-ttu-id="48cd1-113">Ta returnerte varer gjennom inspeksjon</span><span class="sxs-lookup"><span data-stu-id="48cd1-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="48cd1-114">Angi hvordan du kvitter deg med returnerte varer</span><span class="sxs-lookup"><span data-stu-id="48cd1-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]