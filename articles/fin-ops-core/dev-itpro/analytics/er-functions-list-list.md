---
title: LIST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LIST
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4945ffd0e7bb7bbd238e2d3156c5599d3d423046
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563854"
---
# <a name="list-er-function"></a><span data-ttu-id="b1cb1-103">LIST ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="b1cb1-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1cb1-104">`LIST`-funksjonen returnerer en *Postliste*-verdi som består av en ny postliste som er opprettet fra de angitte argumentene.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1cb1-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b1cb1-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="b1cb1-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b1cb1-106">Arguments</span></span>

<span data-ttu-id="b1cb1-107">`record 1`: *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="b1cb1-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="b1cb1-108">En referanse til en datakilde for *Post*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="b1cb1-109">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-109">This argument is required.</span></span>

<span data-ttu-id="b1cb1-110">`record N`: *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="b1cb1-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="b1cb1-111">En referanse til en datakilde for *Post*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="b1cb1-112">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1cb1-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b1cb1-113">Return values</span></span>

<span data-ttu-id="b1cb1-114">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="b1cb1-114">*Record list*</span></span>

<span data-ttu-id="b1cb1-115">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b1cb1-116">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="b1cb1-116">Usage notes</span></span>

<span data-ttu-id="b1cb1-117">Strukturen i listen som opprettes, inneholder bare feltene som vises i strukturen for hver post som nevnes i argumentene.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="b1cb1-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b1cb1-118">Example</span></span>

<span data-ttu-id="b1cb1-119">Du angir datakilde **Post 1** av *Container*-typen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="b1cb1-120">Denne datakilden inneholder følgende nestede felt av typen *Beregnet felt*:</span><span class="sxs-lookup"><span data-stu-id="b1cb1-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="b1cb1-121">**Kode:** Dette feltet inneholder et uttrykk som returnerer en verdi av *streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="b1cb1-122">**Beløp:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Reell*-typen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="b1cb1-123">Du angir deretter datakilde **Post 2** av *Container*-typen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="b1cb1-124">Denne datakilden inneholder følgende nestede felt av typen *Beregnet felt*:</span><span class="sxs-lookup"><span data-stu-id="b1cb1-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="b1cb1-125">**Beløp:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Reell*-typen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="b1cb1-126">**IsValid:** Dette feltet inneholder et uttrykk som returnerer en verdi av *Boolsk*-typen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="b1cb1-127">I dette tilfellet returnerer uttrykket `LIST('Record 1', 'Record 2')` en ny liste som inneholder to poster.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="b1cb1-128">Strukturen i denne listen består av et enkelt **Beløp**-felt av *Reell*-typen, fordi dette feltet er det eneste feltet som vises i alle argumentene til den kalte funksjonen.</span><span class="sxs-lookup"><span data-stu-id="b1cb1-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1cb1-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b1cb1-129">Additional resources</span></span>

[<span data-ttu-id="b1cb1-130">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="b1cb1-130">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]