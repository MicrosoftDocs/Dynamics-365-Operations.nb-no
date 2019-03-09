---
title: Personlige utgifter i en reiseregning
description: Dette emnet beskriver to metoder for håndtering av en arbeiders personlige utgifter i Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "344898"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="2651a-103">Personlige utgifter i en reiseregningsrapport</span><span class="sxs-lookup"><span data-stu-id="2651a-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2651a-104">På forretningsreise kan det hende at den ansatte belaster personlige utgifter med firmakredittkortet.</span><span class="sxs-lookup"><span data-stu-id="2651a-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="2651a-105">Hvis du ikke definerer en prosess for håndtering av personlige utgifter, kan godkjenningsprosessen for reiseregning blir avbrutt når den ansatte sender den spesifiserte reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="2651a-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="2651a-106">I Microsoft Dynamics 365 for Finance and Operations finnes to metoder for håndtering av personlige utgifter:</span><span class="sxs-lookup"><span data-stu-id="2651a-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="2651a-107">**Betalt av ansatt** – organisasjonen betaler ikke personlige utgifter som vises på regningen for firmakredittkortet.</span><span class="sxs-lookup"><span data-stu-id="2651a-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="2651a-108">I stedet opprettes det en rapport som viser personlige utgifter sammen med firmaets utgifter som er belastet firmakredittkortet.</span><span class="sxs-lookup"><span data-stu-id="2651a-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="2651a-109">**Betalt av firma** - firmaet betaler hele regningen som er betalt med firmakredittkortet, og debiterer den ansattes konto for de personlige utgiftene.</span><span class="sxs-lookup"><span data-stu-id="2651a-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="2651a-110">Du kan velge metoden som organisasjonen din bruker på siden **Parametere for reiseregning**.</span><span class="sxs-lookup"><span data-stu-id="2651a-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
