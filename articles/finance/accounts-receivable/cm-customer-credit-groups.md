---
title: Kundekredittgrupper
description: Dette emnet gir informasjon om kundekredittgrupper.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015341"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="1a853-103">Kundekredittgrupper</span><span class="sxs-lookup"><span data-stu-id="1a853-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1a853-104">Du kan definere grupper med kunder som har samme kredittgrense.</span><span class="sxs-lookup"><span data-stu-id="1a853-104">You can define groups of customers who have the same credit limit.</span></span> <span data-ttu-id="1a853-105">Den individuelle kredittgrensen som er definert på kundefakturakontoen, tas også hensyn til.</span><span class="sxs-lookup"><span data-stu-id="1a853-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="1a853-106">Medlemmer av en kundekredittgruppe kan velges fra ulike juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="1a853-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="1a853-107">Når du legger til en kunde i listen over kunder i kundekredittgruppen, endres utløpsdatoen for kredittgrensen for hver kunde til utløpsdatoen som er tilordnet gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a853-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="1a853-108">Du kan definere kundekredittgrupper på siden **Kundekredittgrupper** (**Kredittbehandling \> Kundekredittgrupper \> Kundekredittgrupper**).</span><span class="sxs-lookup"><span data-stu-id="1a853-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="1a853-109">I feltene **Gruppenummer** og **Beskrivelse** angir du en ID for og en beskrivelse av gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a853-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="1a853-110">I feltene **Kredittgrense** og **Valuta** angir du kredittgrensen og valutaen som skal brukes når systemet kontrollerer kredittgrensen for medlem av gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a853-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="1a853-111">I feltet **Kredittgrense til dato** angir du datoen da kredittgrensen utløper.</span><span class="sxs-lookup"><span data-stu-id="1a853-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="1a853-112">Kundekredittgrupper må ha en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="1a853-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="1a853-113">Når du er ferdig med å definere en kundekredittgruppe, kan du legge til kunder i den ved å angi deres juridiske enhet og kundekonto-ID.</span><span class="sxs-lookup"><span data-stu-id="1a853-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="1a853-114">Når du legger til en ny kunde i en kundekredittgruppe, søker systemet etter den samme kundekontoen på tvers av alle juridiske enheter og ber deg om å legge den til i kundekredittgruppen.</span><span class="sxs-lookup"><span data-stu-id="1a853-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="1a853-115">Bruk menyen **Aldersfordelte saldoer** til å vise detaljer for aldersfordelingssaldoen for alle fakturakunder i en kundekredittgruppe.</span><span class="sxs-lookup"><span data-stu-id="1a853-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="1a853-116">Siden **Aldersfordelingssaldo** viser et sammendrag av de aldersfordelte saldoene for fakturakundekontoene.</span><span class="sxs-lookup"><span data-stu-id="1a853-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
