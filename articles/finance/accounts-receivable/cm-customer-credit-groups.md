---
title: Kundekredittgrupper
description: Dette emnet gir informasjon om kundekredittgrupper.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b1e93d562e66cb8d4c5819a749459ea8783b1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237548"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="71715-103">Kundekredittgrupper</span><span class="sxs-lookup"><span data-stu-id="71715-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71715-104">Du kan definere grupper med kunder som har en delt kredittgrense.</span><span class="sxs-lookup"><span data-stu-id="71715-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="71715-105">Den individuelle kredittgrensen som er definert på kundefakturakontoen, tas også hensyn til.</span><span class="sxs-lookup"><span data-stu-id="71715-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="71715-106">Medlemmer av en kundekredittgruppe kan velges fra ulike juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="71715-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="71715-107">Når du legger til en kunde i listen over kunder i kundekredittgruppen, endres utløpsdatoen for kredittgrensen for hver kunde til utløpsdatoen som er tilordnet gruppen.</span><span class="sxs-lookup"><span data-stu-id="71715-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="71715-108">Du kan definere kundekredittgrupper på siden **Kundekredittgrupper** (**Kredittbehandling \> Kundekredittgrupper \> Kundekredittgrupper**).</span><span class="sxs-lookup"><span data-stu-id="71715-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="71715-109">I feltene **Gruppenummer** og **Beskrivelse** angir du en ID for og en beskrivelse av gruppen.</span><span class="sxs-lookup"><span data-stu-id="71715-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="71715-110">I feltene **Kredittgrense** og **Valuta** angir du kredittgrensen og valutaen som skal brukes når systemet kontrollerer kredittgrensen for medlem av gruppen.</span><span class="sxs-lookup"><span data-stu-id="71715-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="71715-111">I feltet **Kredittgrense til dato** angir du datoen da kredittgrensen utløper.</span><span class="sxs-lookup"><span data-stu-id="71715-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="71715-112">Kundekredittgrupper må ha en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="71715-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="71715-113">Når du er ferdig med å definere en kundekredittgruppe, kan du legge til kunder i den ved å angi deres juridiske enhet og kundekonto-ID.</span><span class="sxs-lookup"><span data-stu-id="71715-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="71715-114">Når du legger til en ny kunde i en kundekredittgruppe, søker systemet etter den samme kundekontoen på tvers av alle juridiske enheter og ber deg om å legge den til i kundekredittgruppen.</span><span class="sxs-lookup"><span data-stu-id="71715-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="71715-115">Bruk menyen **Aldersfordelte saldoer** til å vise detaljer for aldersfordelingssaldoen for alle fakturakunder i en kundekredittgruppe.</span><span class="sxs-lookup"><span data-stu-id="71715-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="71715-116">Siden **Aldersfordelingssaldo** viser et sammendrag av de aldersfordelte saldoene for fakturakundekontoene.</span><span class="sxs-lookup"><span data-stu-id="71715-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]