---
title: Du kan legge til bare hovedkontoen som kreditkontoen av avstemmingsårsaker
description: Når du definerer en avstemmingsårsak i Transportstyring, kan du bare legge til hovedkontoen som kreditkontoen.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026765"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="be4cd-103">Du kan legge til bare hovedkontoen som kreditkontoen av avstemmingsårsaker</span><span class="sxs-lookup"><span data-stu-id="be4cd-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="be4cd-104">KB-nummer: 4603538</span><span class="sxs-lookup"><span data-stu-id="be4cd-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="be4cd-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="be4cd-105">Symptoms</span></span>

<span data-ttu-id="be4cd-106">Når du definerer en avstemmingsårsak i Transportstyring, kan du bare legge til hovedkontoen som kreditkontoen.</span><span class="sxs-lookup"><span data-stu-id="be4cd-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="be4cd-107">Du kan ikke legge til et kostsenter eller en annen dimensjon som kreditkonto.</span><span class="sxs-lookup"><span data-stu-id="be4cd-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="be4cd-108">Du kan imidlertid bruke debetkontoen til å velge andre dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="be4cd-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="be4cd-109">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="be4cd-109">Resolution</span></span>

<span data-ttu-id="be4cd-110">Hvis avstemmingen ikke utføres for å betale leverandøren, men for å kreditere en bestemt hovedkonto, lar ikke systemet deg velge en finansdimensjon for kreditkontoen når du definerer avstemmingsårsaken.</span><span class="sxs-lookup"><span data-stu-id="be4cd-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="be4cd-111">Hvis kontostrukturen krever en bestemt finansdimensjonsverdi for hovedkontoen for kredit, kan ikke den resulterende leverandørjournalen posteres automatisk, fordi finansdimensjonsverdien mangler.</span><span class="sxs-lookup"><span data-stu-id="be4cd-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="be4cd-112">Derfor må du først angi kreditkontoen manuelt ved hjelp av **Fakturajournal**-siden.</span><span class="sxs-lookup"><span data-stu-id="be4cd-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="be4cd-113">Fordi det kreves en dimensjonsverdi for kreditkontoen, kan ikke leverandørfakturajournalen posteres automatisk.</span><span class="sxs-lookup"><span data-stu-id="be4cd-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="be4cd-114">Du må postere den manuelt etter at du manuelt har lagt til dimensjonsverdien i hovedkontoen for kreditlinjen.</span><span class="sxs-lookup"><span data-stu-id="be4cd-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
