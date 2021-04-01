---
title: Administrere validering av internasjonale bankkontnumre (IBAN)
description: Dette emnet forklarer hvordan du administrerer validering av internasjonale bankkontnumre (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: f3e7376827a42034e68cb0ee492b82f7274930ea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253993"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="adb14-103">Administrere validering av internasjonale bankkontnumre (IBAN)</span><span class="sxs-lookup"><span data-stu-id="adb14-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adb14-104">Validering av et internasjonalt bankkontonummer (IBAN) øker valideringsmengden som utføres når du legger til et IBAN-nummer for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="adb14-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="adb14-105">Informasjon om strukturen til IBAN er lagret i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="adb14-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="adb14-106">Denne informasjonen lastes automatisk første gang du bruker IBAN-nummeret på bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="adb14-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="adb14-107">Det inneholder lengden på IBAN-nummeret, startposisjonene for bankkontonummeret og registreringsnummeret samt lengden på bankkontonummeret og registreringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="adb14-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="adb14-108">Definere IBAN-strukturer</span><span class="sxs-lookup"><span data-stu-id="adb14-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="adb14-109">Gå til **Kontant- og bankbehandling \> Oppsett \> IBAN-strukturer**.</span><span class="sxs-lookup"><span data-stu-id="adb14-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="adb14-110">Legg merke til at IBAN-strukturene for hvert land eller område er opprettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="adb14-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="adb14-111">Hvis du vil tilpasse strukturene for et bestemt land eller område, kan du redigere dem.</span><span class="sxs-lookup"><span data-stu-id="adb14-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="adb14-112">Strukturdefinsjonene blir en del av hver nye versjon.</span><span class="sxs-lookup"><span data-stu-id="adb14-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="adb14-113">Du kan bruke menyen **Tilbakestill strukturer** til å laste inn de nyeste definisjonene etter hver oppdatering.</span><span class="sxs-lookup"><span data-stu-id="adb14-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="adb14-114">Validere IBAN-strukturen i en bankkonto</span><span class="sxs-lookup"><span data-stu-id="adb14-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="adb14-115">Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="adb14-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="adb14-116">Opprett en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="adb14-116">Create a bank account.</span></span>
3. <span data-ttu-id="adb14-117">Angi et IBAN-nummer på hurtigfanen **Tilleggsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="adb14-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="adb14-118">Hvis lengden på IBAN-nummeret ikke samsvarer med lengden som er definert for hvert land eller område, får du en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb14-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="adb14-119">Du kan ikke fortsette hvis lengden på IBAN-nummeret ikke samsvarer med lengden som er definert i IBAN-strukturen.</span><span class="sxs-lookup"><span data-stu-id="adb14-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="adb14-120">Valideringen kontrollerer også at bankkontonummeret samsvarer med delen av IBAN-nummeret som representerer bankkontonummeret.</span><span class="sxs-lookup"><span data-stu-id="adb14-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="adb14-121">Hvis bankkontonummeret ikke samsvarer, får du en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb14-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="adb14-122">Denne meldingen er bare en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb14-122">This message is only a warning.</span></span> <span data-ttu-id="adb14-123">Du kan fortsette selv om bankkontonummeret ikke samsvarer.</span><span class="sxs-lookup"><span data-stu-id="adb14-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="adb14-124">Valideringen kontrollerer også at bankregistreringsnummeret samsvarer med delen av IBAN-nummeret som representerer bankregistreringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="adb14-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="adb14-125">Registreringsnummeret inneholder et banknummer og ofte en ekstra bankavdeling.</span><span class="sxs-lookup"><span data-stu-id="adb14-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="adb14-126">Hvis bankregistreringsnummeret ikke samsvarer, får du en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb14-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="adb14-127">Denne meldingen er bare en advarsel.</span><span class="sxs-lookup"><span data-stu-id="adb14-127">This message is only a warning.</span></span> <span data-ttu-id="adb14-128">Du kan fortsette selv om bankregistreringsnummeret ikke samsvarer.</span><span class="sxs-lookup"><span data-stu-id="adb14-128">You can continue even if the bank routing number doesn't match.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]