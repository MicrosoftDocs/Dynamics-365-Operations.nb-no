---
title: Vekten må være positiv
description: Vekten må være positiv
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924309"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="51a4d-103">Vekten må være positiv</span><span class="sxs-lookup"><span data-stu-id="51a4d-103">Weight must be positive</span></span>

<span data-ttu-id="51a4d-104">Feilkode: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="51a4d-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="51a4d-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="51a4d-105">Symptoms</span></span>

<span data-ttu-id="51a4d-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="51a4d-106">The system shows the following error message:</span></span>

> <span data-ttu-id="51a4d-107">Vekten må være positiv.</span><span class="sxs-lookup"><span data-stu-id="51a4d-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="51a4d-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="51a4d-108">Cause</span></span>

<span data-ttu-id="51a4d-109">**Bruttovekt**-feltet er satt til *0* (null) eller en negativ verdi.</span><span class="sxs-lookup"><span data-stu-id="51a4d-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="51a4d-110">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="51a4d-110">Resolution</span></span>

<span data-ttu-id="51a4d-111">Hvis du vil angi en vekt, gjør du ett av følgende.</span><span class="sxs-lookup"><span data-stu-id="51a4d-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="51a4d-112">Angi en verdi i **Bruttovekt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="51a4d-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="51a4d-113">Velg deretter en enhet fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="51a4d-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="51a4d-114">Velg **Hent systemvekt** for å beregne **bruttovektverdien**.</span><span class="sxs-lookup"><span data-stu-id="51a4d-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
