---
title: GETENUMVALUEBYNAME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GETENUMVALUEBYNAME.
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
ms.openlocfilehash: 87613978c149b5d41aefc58f9896424229819626
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041192"
---
# <span data-ttu-id="d5529-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="d5529-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5529-104">`GETENUMVALUEBYNAME`-funksjonen søker etter en bestemt *opplistings*-verdi i den angitte opplistingsdatakilden ved hjelp av opplistingsnavnet som er angitt som en *Streng*-verdi.</span><span class="sxs-lookup"><span data-stu-id="d5529-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="d5529-105">Hvis *opplistings*-verdien blir funnet, returnerer funksjonen den.</span><span class="sxs-lookup"><span data-stu-id="d5529-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="d5529-106">Hvis ikke returnerer funksjonen opplistingsverdien **null**.</span><span class="sxs-lookup"><span data-stu-id="d5529-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5529-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d5529-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="d5529-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d5529-108">Arguments</span></span>

<span data-ttu-id="d5529-109">`enumeration data source path`: *Opplisting*</span><span class="sxs-lookup"><span data-stu-id="d5529-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="d5529-110">Den gyldige referansebanen til en datakilde for en av følgende opplistingstyper:</span><span class="sxs-lookup"><span data-stu-id="d5529-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="d5529-111">ER-modellopplisting</span><span class="sxs-lookup"><span data-stu-id="d5529-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="d5529-112">ER-formatopplisting</span><span class="sxs-lookup"><span data-stu-id="d5529-112">ER format enumeration</span></span>
- <span data-ttu-id="d5529-113">Microsoft Dynamics 365 Finance-opplisting</span><span class="sxs-lookup"><span data-stu-id="d5529-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="d5529-114">`enumeration value text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="d5529-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="d5529-115">En strengverdi som representerer navnet på en enkelt opplistingsverdi.</span><span class="sxs-lookup"><span data-stu-id="d5529-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="d5529-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="d5529-116">Return values</span></span>

<span data-ttu-id="d5529-117">*Opplisting* som kan nullstilles</span><span class="sxs-lookup"><span data-stu-id="d5529-117">Nullable *Enum*</span></span>

<span data-ttu-id="d5529-118">Den resulterende opplistingsverdien.</span><span class="sxs-lookup"><span data-stu-id="d5529-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d5529-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="d5529-119">Usage notes</span></span>

<span data-ttu-id="d5529-120">Det blir ikke registrert noe unntak hvis en *opplisting*-verdi ikke blir funnet ved å bruke navnet på opplistingsverdien som er angitt som en *streng*-verdi.</span><span class="sxs-lookup"><span data-stu-id="d5529-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="d5529-121">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d5529-121">Example</span></span>

<span data-ttu-id="d5529-122">I følgende illustrasjon introduseres opplistingen **ReportDirection** i en datamodell.</span><span class="sxs-lookup"><span data-stu-id="d5529-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="d5529-123">Legg merke til at etiketter er definert for opplistingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="d5529-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="d5529-124">Illustrasjonen nedenfor viser disse detaljene:</span><span class="sxs-lookup"><span data-stu-id="d5529-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="d5529-125">Datakilden **$Direction** er konfigurert i en ER-rapport.</span><span class="sxs-lookup"><span data-stu-id="d5529-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="d5529-126">Denne datakilden er konfigurert basert på **ReportDirection**-modellopplistingen.</span><span class="sxs-lookup"><span data-stu-id="d5529-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="d5529-127">Uttrykket `$IsArrivals` er utformet for å bruke den modellopplistingsbaserte **$Direction**-datakilden som en parameter for denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="d5529-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="d5529-128">Verdien av denne sammenligningen er **SANN**.</span><span class="sxs-lookup"><span data-stu-id="d5529-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="d5529-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d5529-129">Additional resources</span></span>

[<span data-ttu-id="d5529-130">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="d5529-130">Text functions</span></span>](er-functions-category-text.md)
