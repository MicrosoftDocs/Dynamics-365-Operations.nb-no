---
title: Du kan ikke importere en vare ved hjelp av Frigitte produkter V2-enheten
description: Du kan ikke importere en vare ved hjelp av Frigitte produkter V2-enheten.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026771"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="18fd3-103">Du kan ikke importere en vare ved hjelp av Frigitte produkter V2-enheten</span><span class="sxs-lookup"><span data-stu-id="18fd3-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="18fd3-104">KB-nummer: 4611825</span><span class="sxs-lookup"><span data-stu-id="18fd3-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="18fd3-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="18fd3-105">Symptoms</span></span>

<span data-ttu-id="18fd3-106">Når du prøver å importere en vare ved hjelp av *Frigitte produkter V2*-enheten, får du en feilmelding som ligner på følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="18fd3-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="18fd3-107">Kan ikke opprette en post i Varer - sporingsdimensjonsgrupper (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="18fd3-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="18fd3-108">Varenummer: 2040663, parti.</span><span class="sxs-lookup"><span data-stu-id="18fd3-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="18fd3-109">Posten finnes allerede.</span><span class="sxs-lookup"><span data-stu-id="18fd3-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="18fd3-110">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="18fd3-110">Resolution</span></span>

<span data-ttu-id="18fd3-111">Hvis du vil importere nye frigitte produkter, må du bruke *Frigitt produktoppretting V2*-enheten i stedet for *Frigitte produkter V2*-enheten.</span><span class="sxs-lookup"><span data-stu-id="18fd3-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
