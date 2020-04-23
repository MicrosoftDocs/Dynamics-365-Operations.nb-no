---
title: LISTJOIN ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249041"
---
# <a name=""></a><span data-ttu-id="da099-103"><a name="LISTJOIN">LISTJOIN ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="da099-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da099-104">`LISTJOIN`-funksjonen returnerer en *Postliste*-verdi som representerer en ny sammenkoblet liste over poster som er opprettet fra de angitte argumentene.</span><span class="sxs-lookup"><span data-stu-id="da099-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="da099-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="da099-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="da099-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="da099-106">Arguments</span></span>

<span data-ttu-id="da099-107">`list 1`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="da099-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="da099-108">En referanse til en datakilde for *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="da099-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="da099-109">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="da099-109">This argument is mandatory.</span></span>

<span data-ttu-id="da099-110">`list N`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="da099-110">`list N`: *Record list*</span></span>

<span data-ttu-id="da099-111">En referanse til en datakilde for *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="da099-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="da099-112">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="da099-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="da099-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="da099-113">Return values</span></span>

<span data-ttu-id="da099-114">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="da099-114">*Record list*</span></span>

<span data-ttu-id="da099-115">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="da099-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="da099-116">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="da099-116">Usage notes</span></span>

<span data-ttu-id="da099-117">Strukturen i listen som opprettes, inneholder bare feltene som vises i strukturen for hver postliste som det er referert til i argumentene.</span><span class="sxs-lookup"><span data-stu-id="da099-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="da099-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="da099-118">Example</span></span>

<span data-ttu-id="da099-119">Du angir datakilden **Post 1** av `Container`-typen.</span><span class="sxs-lookup"><span data-stu-id="da099-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="da099-120">Denne datakilden inneholder følgende nestede felt av typen `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="da099-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="da099-121">**Kode** Dette feltet inneholder et uttrykk som returnerer en verdi av `String`-typen.</span><span class="sxs-lookup"><span data-stu-id="da099-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="da099-122">**Beløp** Dette feltet inneholder et uttrykk som returnerer en verdi av `Real`-typen.</span><span class="sxs-lookup"><span data-stu-id="da099-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="da099-123">Du angir deretter datakilden **Post 2** av `Container`-typen.</span><span class="sxs-lookup"><span data-stu-id="da099-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="da099-124">Denne datakilden inneholder følgende nestede felt av typen `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="da099-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="da099-125">**Beløp** Dette feltet inneholder et uttrykk som returnerer en verdi av `Real`-typen.</span><span class="sxs-lookup"><span data-stu-id="da099-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="da099-126">**IsValid** Dette feltet inneholder et uttrykk som returnerer en verdi av `Boolean`-typen.</span><span class="sxs-lookup"><span data-stu-id="da099-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="da099-127">I dette tilfellet returnerer uttrykket `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` en ny liste som inneholder to poster.</span><span class="sxs-lookup"><span data-stu-id="da099-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="da099-128">Strukturen i denne listen består av et enkelt **Beløp**-felt av `Real`-typen, fordi dette feltet er det eneste feltet som vises i alle argumentene til den kalte funksjonen.</span><span class="sxs-lookup"><span data-stu-id="da099-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da099-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="da099-129">Additional resources</span></span>

[<span data-ttu-id="da099-130">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="da099-130">List functions</span></span>](er-functions-category-list.md)
