---
title: LIST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LIST
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917287"
---
# <span data-ttu-id="0ee90-103"><a name="LIST">LIST ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="0ee90-103"><a name="LIST">LIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ee90-104">`LIST`-funksjonen returnerer en *Postliste*-verdi som består av en ny postliste som er opprettet fra de angitte argumentene.</span><span class="sxs-lookup"><span data-stu-id="0ee90-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee90-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0ee90-105">Syntax</span></span>

```
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="0ee90-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="0ee90-106">Arguments</span></span>

<span data-ttu-id="0ee90-107">`record 1`: *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="0ee90-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="0ee90-108">En referanse til en datakilde for *Post*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="0ee90-109">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0ee90-109">This argument is required.</span></span>

<span data-ttu-id="0ee90-110">`record N`: *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="0ee90-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="0ee90-111">En referanse til en datakilde for *Post*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="0ee90-112">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="0ee90-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ee90-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="0ee90-113">Return values</span></span>

<span data-ttu-id="0ee90-114">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="0ee90-114">*Record list*</span></span>

<span data-ttu-id="0ee90-115">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="0ee90-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0ee90-116">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="0ee90-116">Usage notes</span></span>

<span data-ttu-id="0ee90-117">Strukturen i listen som opprettes, inneholder bare feltene som vises i strukturen for hver post som nevnes i argumentene.</span><span class="sxs-lookup"><span data-stu-id="0ee90-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="0ee90-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0ee90-118">Example</span></span>

<span data-ttu-id="0ee90-119">Du angir datakilde **Post 1** av *Container*-typen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="0ee90-120">Denne datakilden inneholder følgende nestede felt av typen *Beregnet felt*:</span><span class="sxs-lookup"><span data-stu-id="0ee90-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="0ee90-121">**Kode:** Dette feltet inneholder et uttrykk som returnerer en verdi av *streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="0ee90-122">**Beløp:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Reell*-typen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="0ee90-123">Du angir deretter datakilde **Post 2** av *Container*-typen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="0ee90-124">Denne datakilden inneholder følgende nestede felt av typen *Beregnet felt*:</span><span class="sxs-lookup"><span data-stu-id="0ee90-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="0ee90-125">**Beløp:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Reell*-typen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="0ee90-126">**IsValid:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Boolsk*-typen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="0ee90-127">I dette tilfellet returnerer uttrykket `LIST('Record 1', 'Record 2')` en ny liste som inneholder to poster.</span><span class="sxs-lookup"><span data-stu-id="0ee90-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="0ee90-128">Strukturen i denne listen består av et enkelt **Beløp**-felt av *Reell*-typen, fordi dette feltet er det eneste feltet som vises i alle argumentene til den kalte funksjonen.</span><span class="sxs-lookup"><span data-stu-id="0ee90-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ee90-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0ee90-129">Additional resources</span></span>

[<span data-ttu-id="0ee90-130">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="0ee90-130">List functions</span></span>](er-functions-category-list.md)
