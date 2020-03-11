---
title: ALLITEMS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ALLITEMS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 3aa226be8bc27817b4369b9e5b24faee8ea52b88
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042234"
---
# <span data-ttu-id="8a19b-103"><a name="ALLITEMS">ALLITEMS ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="8a19b-103"><a name="ALLITEMS">ALLITEMS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a19b-104">`ALLITEMS`-funksjonen kjøres som et minneinternt valg og returnerer en ny utflatet *Postliste*-verdi som en liste over poster som representerer alle elementer som samsvarer med den angitte banen.</span><span class="sxs-lookup"><span data-stu-id="8a19b-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a19b-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8a19b-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="8a19b-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8a19b-106">Arguments</span></span>

<span data-ttu-id="8a19b-107">`path`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="8a19b-107">`path`: *Record list*</span></span>

<span data-ttu-id="8a19b-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="8a19b-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8a19b-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="8a19b-109">Return values</span></span>

<span data-ttu-id="8a19b-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="8a19b-110">*Record list*</span></span>

<span data-ttu-id="8a19b-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="8a19b-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8a19b-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="8a19b-112">Usage notes</span></span>

<span data-ttu-id="8a19b-113">Banen må defineres som en gyldig datakildebane til et datakildeelement av datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="8a19b-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="8a19b-114">Dataelementer som banestrengen og datoen skal føre til en feil i ER-uttrykksverktøyet under utformingen.</span><span class="sxs-lookup"><span data-stu-id="8a19b-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="8a19b-115">Vi anbefaler ikke at du bruker denne funksjonen for transaksjonsdatakilder som kan inneholde store mengder data.</span><span class="sxs-lookup"><span data-stu-id="8a19b-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="8a19b-116">I stedet bør du vurdere å bruke [ALLTEMSQUERY](er-functions-list-allitemsquery.md)-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="8a19b-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="8a19b-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="8a19b-117">Example 1</span></span>

<span data-ttu-id="8a19b-118">Hvis du angir `SPLIT("abcdef" , 2)` som datakilde **DS**, returnerer uttrykket `COUNT( ALLITEMS (DS))` **3**.</span><span class="sxs-lookup"><span data-stu-id="8a19b-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="8a19b-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="8a19b-119">Example 2</span></span>

<span data-ttu-id="8a19b-120">Hvis du angir **Vend** som datakilde for datatypen *postliste* som refererer til VendTable-programtabellen, returnerer uttrykket `ALLITEMS (Vend.'<Relations'.ContactPerson)` en sammenslått liste over poster som har tabellstrukturen **ContactPerson**, og inneholder alle kontaktpersoner som kan åpnes ved hjelp av **ContactPerson.ContactForParty == VendTable.Party**-relasjonen, og som er tilgjengelig for alle leverandører fra den refererte leverandørtabellen.</span><span class="sxs-lookup"><span data-stu-id="8a19b-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a19b-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8a19b-121">Additional resources</span></span>

[<span data-ttu-id="8a19b-122">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="8a19b-122">List functions</span></span>](er-functions-category-list.md)
