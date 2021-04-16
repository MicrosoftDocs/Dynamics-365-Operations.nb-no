---
title: ALLITEMS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ALLITEMS.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 5ddcf989bdfd1d1f5d0a412a2ffefe0e3037ca79
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746729"
---
# <a name="allitems-er-function"></a><span data-ttu-id="9c3b2-103">ALLITEMS ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="9c3b2-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c3b2-104">`ALLITEMS`-funksjonen kjøres som et minneinternt valg og returnerer en ny utflatet *Postliste*-verdi som en liste over poster som representerer alle elementer som samsvarer med den angitte banen.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c3b2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9c3b2-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="9c3b2-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="9c3b2-106">Arguments</span></span>

<span data-ttu-id="9c3b2-107">`path`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="9c3b2-107">`path`: *Record list*</span></span>

<span data-ttu-id="9c3b2-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c3b2-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="9c3b2-109">Return values</span></span>

<span data-ttu-id="9c3b2-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="9c3b2-110">*Record list*</span></span>

<span data-ttu-id="9c3b2-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9c3b2-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="9c3b2-112">Usage notes</span></span>

<span data-ttu-id="9c3b2-113">Banen må defineres som en gyldig datakildebane til et datakildeelement av datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="9c3b2-114">Dataelementer som banestrengen og datoen skal føre til en feil i ER-uttrykksverktøyet under utformingen.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="9c3b2-115">Vi anbefaler ikke at du bruker denne funksjonen for transaksjonsdatakilder som kan inneholde store mengder data.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="9c3b2-116">I stedet bør du vurdere å bruke [ALLTEMSQUERY](er-functions-list-allitemsquery.md)-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="9c3b2-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="9c3b2-117">Example 1</span></span>

<span data-ttu-id="9c3b2-118">Hvis du angir `SPLIT("abcdef" , 2)` som datakilde **DS**, returnerer uttrykket `COUNT( ALLITEMS (DS))` **3**.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9c3b2-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="9c3b2-119">Example 2</span></span>

<span data-ttu-id="9c3b2-120">Hvis du angir **Vend** som datakilde for datatypen *postliste* som refererer til VendTable-programtabellen, returnerer uttrykket `ALLITEMS (Vend.'<Relations'.ContactPerson)` en sammenslått liste over poster som har tabellstrukturen **ContactPerson**, og inneholder alle kontaktpersoner som kan åpnes ved hjelp av **ContactPerson.ContactForParty == VendTable.Party**-relasjonen, og som er tilgjengelig for alle leverandører fra den refererte leverandørtabellen.</span><span class="sxs-lookup"><span data-stu-id="9c3b2-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c3b2-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9c3b2-121">Additional resources</span></span>

[<span data-ttu-id="9c3b2-122">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="9c3b2-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]