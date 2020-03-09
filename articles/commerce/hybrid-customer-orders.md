---
title: Hybridkundeordrer
description: En hybridkundeordre er en enkelt ordre som inneholder produkter som kan utføres fra butikken av kunden, i tillegg til produkter som skal hentes eller sendes senere.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c2105aa99e0489d7643d076e84123eec628679e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023617"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="f5b47-103">Hybridkundeordrer</span><span class="sxs-lookup"><span data-stu-id="f5b47-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5b47-104">En hybridkundeordre er en enkelt ordre som inneholder produkter som kan utføres fra butikken av kunden, i tillegg til produkter som skal hentes eller sendes senere.</span><span class="sxs-lookup"><span data-stu-id="f5b47-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="f5b47-105">I Commerce kan du velge å utføre alle produkter eller utføre valgte produkter for en kundeordre.</span><span class="sxs-lookup"><span data-stu-id="f5b47-105">In Commerce, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="f5b47-106">Produktlinjer som er merket som utfør, faktureres automatisk etter at ordren er opprettet. Dette gjelder også for en ordre som skal hentes etter at ordren er opprettet.</span><span class="sxs-lookup"><span data-stu-id="f5b47-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="f5b47-107">Beløpet å betale på hybridordrer bestemmes ved å legge innbetalingsprosenten på produktlinjene for plukking og sending til hele beløpet for utføringslinjene.</span><span class="sxs-lookup"><span data-stu-id="f5b47-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="f5b47-108">For hybridordrer veksler systemet mellom kundeordremodus og hentesalgmodus som følger:</span><span class="sxs-lookup"><span data-stu-id="f5b47-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="f5b47-109">Hvis alle produkter i handlekurven er satt til **Utfør levering**, vil ordren bli behandlet som en hentesalgstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="f5b47-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="f5b47-110">Hvis noen av eller alle linjene i handlekurven er satt til enten **Plukk** eller **send levering**, vil ordren bli behandlet som en kundeordretransaksjon.</span><span class="sxs-lookup"><span data-stu-id="f5b47-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="f5b47-111">Hvis en handlevognlinje er valgt og **Velg valgt**, **Valgt for forsendelse** eller **Utfør valgte** er valgt, angis bare den bestemte handlekurvlinjen med denne leveringsmetoden.</span><span class="sxs-lookup"><span data-stu-id="f5b47-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="f5b47-112">I så fall fortsetter nedstrømsflyten av operasjonen som vanlig.</span><span class="sxs-lookup"><span data-stu-id="f5b47-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="f5b47-113">Hvis **Velg valgt**, **Valgt for forsendelse**, eller **Utfør valgte** velges uten at en handlevognlinje blir valgt, åpnes imidlertid en ny side som viser alle handlekurvlinjene.</span><span class="sxs-lookup"><span data-stu-id="f5b47-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="f5b47-114">På dette skjermbildet kan du velge flere linjer samtidig for å angi leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="f5b47-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="f5b47-115">Når du bruker denne metoden for å velge linjer, vil tidligere leveringsmåter som er knyttet til linjen, bli overstyrt.</span><span class="sxs-lookup"><span data-stu-id="f5b47-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5b47-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f5b47-116">Additional resources</span></span>

[<span data-ttu-id="f5b47-117">Kundeordrer i Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="f5b47-117">Customer orders in Modern POS (MPOS)</span></span>](customer-orders-overview.md)