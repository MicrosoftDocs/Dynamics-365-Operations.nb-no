---
title: Motta delleveringer av returnerte varer
description: Delvise leveringer defineres som returordrelinjer, ikke som returordreforsendelser.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51213f8f46638b0cce10251e761d7f276c39d924
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836140"
---
# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="ad7bd-103">Motta delleveringer av returnerte varer</span><span class="sxs-lookup"><span data-stu-id="ad7bd-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ad7bd-104">Delvise leveringer defineres som returordrelinjer, ikke som returordreforsendelser.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="ad7bd-105">Dette betyr at hvis du mottar hele antallet som er angitt på én returordrelinje, men ingenting fra de andre linjene i returordren, er leveringen ikke en delvis levering.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="ad7bd-106">Hvis en returordrelinje krever at ti enheter av en bestemt vare returneres, men du bare mottar fire, er dette imidlertid en delvis levering.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="ad7bd-107">Hvis en returforsendelse inneholder mindre enn hele antallet i en returordrelinje, kan du sette forsendelsen til side og vente til resten av det returnerte antallet ankommer, eller du kan registrere og postere den delvise leveringen.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="ad7bd-108">Registrere og postere en delvis levering</span><span class="sxs-lookup"><span data-stu-id="ad7bd-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="ad7bd-109">Når du har valgt en returordre for ankomst i skjemaet **Oversikt over ankomst - Lager: %1, Mottakssone: %2, Journalnavn: %3**, klikker du **Start ankomst** for å opprette ankomstjournalen, og klikk deretter **Journaler** \> **Vis ankomster fra mottak** for å åpne **Lokasjonsjournal-skjemaet**.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="ad7bd-110">Merk linjen du vil arbeide med i journalen, og klikk deretter **Linjer** for å åpne skjemaet **Journallinjer, lokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="ad7bd-111">Merk linjen til varenummeret som har ankommet med bare en del av antallet, og klikk deretter **Funksjoner** \> **Del** for å åpne **Del**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="ad7bd-112">I feltet **Delingsantall** angir du det totale antallet av varer som er mottatt, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="ad7bd-113">I skjemaet **Journallinjer, lokasjoner** merker du linjen for antallet av varer som er ankommet, og klikk deretter **Poster**.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="ad7bd-114">Du kan postere linjen for resten av antallet etter at varene er ankommet.</span><span class="sxs-lookup"><span data-stu-id="ad7bd-114">You can post the line for the additional quantity after the items have arrived.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]