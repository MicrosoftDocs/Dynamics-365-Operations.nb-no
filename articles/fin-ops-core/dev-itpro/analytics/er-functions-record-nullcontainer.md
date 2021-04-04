---
title: NULLCONTAINER ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NULLCONTAINER.
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
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563228"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="7704e-103">NULLCONTAINER ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="7704e-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7704e-104">`NULLCONTAINER`-funksjonen returnerer en nullverdi for *Container (post)*-verdi som har samme struktur som den angitte postlisten eller posten.</span><span class="sxs-lookup"><span data-stu-id="7704e-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7704e-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7704e-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="7704e-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7704e-106">Arguments</span></span>

<span data-ttu-id="7704e-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="7704e-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="7704e-108">Den gyldige banen til en datakilde for typen *Postliste* eller *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="7704e-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7704e-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="7704e-109">Return values</span></span>

<span data-ttu-id="7704e-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="7704e-110">*Container (record)*</span></span>

<span data-ttu-id="7704e-111">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="7704e-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7704e-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="7704e-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="7704e-113">Denne funksjonen er foreldet.</span><span class="sxs-lookup"><span data-stu-id="7704e-113">This function is obsolete.</span></span> <span data-ttu-id="7704e-114">Bruk `EMPTYRECORD`-funksjonen i stedet.</span><span class="sxs-lookup"><span data-stu-id="7704e-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="7704e-115">Hvis du vil ha mer informasjon, kan du se [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="7704e-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="7704e-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="7704e-116">Example</span></span>

<span data-ttu-id="7704e-117">`NULLCONTAINER (SPLIT ("abc", 1))` returnerer en ny, tom post som har samme struktur som listen som returneres av `SPLIT`- funksjonen.</span><span class="sxs-lookup"><span data-stu-id="7704e-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="7704e-118">Hvis du vil ha mer informasjon, kan du se [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="7704e-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7704e-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="7704e-119">Additional resources</span></span>

[<span data-ttu-id="7704e-120">Registreringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="7704e-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]