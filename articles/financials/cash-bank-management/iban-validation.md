---
title: Administrere validering av internasjonale bankkontnumre (IBAN)
description: Dette emnet forklarer hvordan du administrerer validering av internasjonale bankkontnumre (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: nb-no
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="23848-103">Administrere validering av internasjonale bankkontnumre (IBAN)</span><span class="sxs-lookup"><span data-stu-id="23848-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23848-104">Validering av et internasjonalt bankkontonummer (IBAN) øker valideringsmengden som utføres når du legger til et IBAN-nummer for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="23848-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="23848-105">Strukturen til IBAN-nummeret lagres i Microsoft Dynamics 365 for Finance and Operations og lastes automatisk når du først bruke IBAN-nummeret på bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="23848-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="23848-106">Bankkontonummeret er en del av den definerte strukturen for et IBAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="23848-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="23848-107">Basert på denne strukturen, om plasseringen og lengden på kontonummeret i IBAN-nummeret ikke samsvarer med stillingen som er definert i strukturen for hvert land eller område, får du advarsler.</span><span class="sxs-lookup"><span data-stu-id="23848-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="23848-108">Definere IBAN-strukturer</span><span class="sxs-lookup"><span data-stu-id="23848-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="23848-109">Gå til **Kontant- og bankbehandling \> Oppsett \> IBAN-strukturer**.</span><span class="sxs-lookup"><span data-stu-id="23848-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="23848-110">Legg merke til at IBAN-strukturene for hvert land eller område er opprettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="23848-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="23848-111">Hvis du må tilpasse strukturer for et bestemt land eller område, kan du redigere dem.</span><span class="sxs-lookup"><span data-stu-id="23848-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="23848-112">Strukturdefinsjonene blir en del av hver nye versjon.</span><span class="sxs-lookup"><span data-stu-id="23848-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="23848-113">Du kan bruke menyen **Tilbakestill strukturer** til å laste inn de nyeste definisjonene etter hver oppdatering.</span><span class="sxs-lookup"><span data-stu-id="23848-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="23848-114">Validere IBAN-strukturen i en bankkonto</span><span class="sxs-lookup"><span data-stu-id="23848-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="23848-115">Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="23848-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="23848-116">Opprett en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="23848-116">Create a bank account.</span></span>
3. <span data-ttu-id="23848-117">Angi et IBAN-nummer på hurtigfanen **Tilleggsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="23848-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="23848-118">Hvis plasseringen og lengden på kontonummeret i IBAN-nummeret ikke samsvarer med stillingen som er definert i strukturen for hvert land eller område, får du en melding.</span><span class="sxs-lookup"><span data-stu-id="23848-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="23848-119">Du kan ikke fortsette hvis lengden på IBAN-nummeret ikke samsvarer med lengden i IBAN-strukturen.</span><span class="sxs-lookup"><span data-stu-id="23848-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="23848-120">Valideringen kontrollerer også at bankkontonummeret samsvarer med delen av IBAN-nummeret som representerer bankkontonummeret.</span><span class="sxs-lookup"><span data-stu-id="23848-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="23848-121">Hvis bankkontonummeret ikke samsvarer, får du en advarsel.</span><span class="sxs-lookup"><span data-stu-id="23848-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="23848-122">Denne meldingen er bare en advarsel.</span><span class="sxs-lookup"><span data-stu-id="23848-122">This message is only a warning.</span></span> <span data-ttu-id="23848-123">Du kan fortsette selv om bankkontonummeret ikke samsvarer.</span><span class="sxs-lookup"><span data-stu-id="23848-123">You can continue even if the bank account number doesn't match.</span></span>

