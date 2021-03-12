---
title: Opprette en erstatningsordre for vare
description: Erstatningsordrer for varer opprettes vanligvis etter at et produkt er returnert og kontrollert.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0006ea9ec64cd95a709ec91509cb3a9828df160
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996657"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="88818-103">Opprette en erstatningsordre for vare</span><span class="sxs-lookup"><span data-stu-id="88818-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="88818-104">Erstatningsordrer for varer opprettes vanligvis etter at et produkt er returnert og kontrollert.</span><span class="sxs-lookup"><span data-stu-id="88818-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="88818-105">Når en vare må erstattes før den er returnert, eller når originalvaren ikke vil bli returnert, kan du opprette en erstatningsordre for en vare rett etter at du har opprettet en returordre.</span><span class="sxs-lookup"><span data-stu-id="88818-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="88818-106">Opprette en erstatningsordre når du mottar en returnert vare</span><span class="sxs-lookup"><span data-stu-id="88818-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="88818-107">Klikk på **Salg og markedsføring** \> **Vanlig** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="88818-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="88818-108">Opprett en ny returordre eller velg en returordre fra listen, for å åpne skjemaet **Returordre – autorisasjonsreturnr.: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="88818-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="88818-109">Klikk på **Returlinje**, og velg deretter **Erstatningsvare**.</span><span class="sxs-lookup"><span data-stu-id="88818-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="88818-110">Velg varen du vil erstatte den returnerte varen med.</span><span class="sxs-lookup"><span data-stu-id="88818-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="88818-111">Angi spesifikasjonene for varen, og klikk deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="88818-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="88818-112">Klikk på **Følgeseddel** for å generere følgeseddelen for returordren.</span><span class="sxs-lookup"><span data-stu-id="88818-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="88818-113">En salgsordre genereres for erstatningsvaren som du har valgt.</span><span class="sxs-lookup"><span data-stu-id="88818-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="88818-114">Når salgsordren er opprettet for erstatningsvaren, søkes det automatisk i salgsavtalene, og hvis det finnes en gjeldende salgsavtale, gjøres den gjeldende for slagsordren.</span><span class="sxs-lookup"><span data-stu-id="88818-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="88818-115">Opprette en erstatningsordre før du mottar en vare som vil bli returnert</span><span class="sxs-lookup"><span data-stu-id="88818-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="88818-116">Klikk på **Salg og markedsføring** \> **Vanlig** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="88818-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="88818-117">Opprett en ny returordre eller velg en returordre fra listen, for å åpne skjemaet **Returordre – autorisasjonsreturnr.: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="88818-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="88818-118">Klikk på **Søk etter salgsordre** hvis du vil finne salgsordren for den returnerte varen.</span><span class="sxs-lookup"><span data-stu-id="88818-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="88818-119">Fyll ut skjemaet **Søk etter salgsordre**, og klikk deretter **OK** for å lukke skjemaet og gå tilbake til skjemaet **Returordre – autorisasjonsreturnr.: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="88818-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="88818-120">Salgsordrelinjen for den returnerte varen kopieres til returordren.</span><span class="sxs-lookup"><span data-stu-id="88818-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="88818-121">Klikk på **Erstatningsordre** for å åpne skjemaet **Opprett salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="88818-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="88818-122">Merk av for **Kopier returordrelinjer** for å overføre detaljer fra returordren du valgte i skjemaet **Returordre – autorisasjonsreturnr.: %1, %2**, til denne salgsordren.</span><span class="sxs-lookup"><span data-stu-id="88818-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="88818-123">Angi eller endre detaljer etter behov.</span><span class="sxs-lookup"><span data-stu-id="88818-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="88818-124">Hvis du identifiserte salgsordren i trinn 3 og salgsordrelinjen for den returnerte varen er koblet til salgsavtalen, vil ID-en for gjeldende salgsavtale for erstatningsordren for varen automatisk vises i feltet **Salgsavtale-ID**.</span><span class="sxs-lookup"><span data-stu-id="88818-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="88818-125">Klikk på **OK** for å lukke skjemaet **Opprett salgsordre** og åpne skjemaet **Salgsordre**, der du kan fortsette å angi informasjon for den nye salgsordren.</span><span class="sxs-lookup"><span data-stu-id="88818-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="88818-126">Eventuelle gjeldende returordrelinjer kopieres til den nye salgsordren.</span><span class="sxs-lookup"><span data-stu-id="88818-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="88818-127">Hvis ID-en for salgsavtalen automatisk vises i feltet **Salgsavtale-ID**, er salgsavtalen koblet til salgsordrehodet for erstatningsordren for varen.</span><span class="sxs-lookup"><span data-stu-id="88818-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="88818-128">Hvis det finnes en gjeldende forpliktelse i salgsavtalen som ikke er oppfylt ennå, og salgsordren opprettes før salgsavtalen utløper, blir det opprettet en kobling mellom salgsavtalelinjen og salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="88818-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="88818-129">Informasjon fra salgsavtalen, for eksempel varepris, kopieres derfor til den nye salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="88818-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


