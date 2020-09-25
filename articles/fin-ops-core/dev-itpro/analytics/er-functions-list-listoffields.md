---
title: LISTOFFIELDS ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LISTOFFIELDS.
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
ms.openlocfilehash: c288050fa1f9f1be9c38696e844e782794795471
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745087"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="81092-103">LISTOFFIELDS ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="81092-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81092-104">`LISTOFFIELDS`-funksjonen returnerer en *postliste*-verdi som opprettes basert på strukturen til det angitte argumentet for typen *Opplisting* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="81092-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="81092-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="81092-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="81092-106">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="81092-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="81092-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="81092-107">Arguments</span></span>

<span data-ttu-id="81092-108">`path`: Datakildereferanse</span><span class="sxs-lookup"><span data-stu-id="81092-108">`path`: Data source reference</span></span>

<span data-ttu-id="81092-109">Den gyldige referansebanen til en datakilde for en av følgende datatyper:</span><span class="sxs-lookup"><span data-stu-id="81092-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="81092-110">Modellopplisting</span><span class="sxs-lookup"><span data-stu-id="81092-110">Model enumeration</span></span>
- <span data-ttu-id="81092-111">Formatopplisting</span><span class="sxs-lookup"><span data-stu-id="81092-111">Format enumeration</span></span>
- <span data-ttu-id="81092-112">Opplisting av programmer</span><span class="sxs-lookup"><span data-stu-id="81092-112">Application enumeration</span></span>
- <span data-ttu-id="81092-113">Container (post)</span><span class="sxs-lookup"><span data-stu-id="81092-113">Container (record)</span></span>

<span data-ttu-id="81092-114">`language`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="81092-114">`language`: *String*</span></span>

<span data-ttu-id="81092-115">Tekst som representerer en språkkode.</span><span class="sxs-lookup"><span data-stu-id="81092-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="81092-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="81092-116">Return values</span></span>

<span data-ttu-id="81092-117">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="81092-117">*Record list*</span></span>

<span data-ttu-id="81092-118">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="81092-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="81092-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="81092-119">Usage notes</span></span>

<span data-ttu-id="81092-120">Listen som opprettes, består av poster med følgende felt:</span><span class="sxs-lookup"><span data-stu-id="81092-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="81092-121">**Navn** (*Streng*-datatype)</span><span class="sxs-lookup"><span data-stu-id="81092-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="81092-122">**Etikett** (*Streng*-datatype)</span><span class="sxs-lookup"><span data-stu-id="81092-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="81092-123">**Beskrivelse** (*Streng*-datatype)</span><span class="sxs-lookup"><span data-stu-id="81092-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="81092-124">**IsTranslated** (*boolsk* datatype)</span><span class="sxs-lookup"><span data-stu-id="81092-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="81092-125">Hvis `path`-argumentet refererer til en datakilde av typen *Container (post)*, legges det til en ny post i listen som opprettes, for hvert felt i container-posten det refereres til.</span><span class="sxs-lookup"><span data-stu-id="81092-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="81092-126">For hver post som opprettes, vil **navn**-feltet returnere navnet på feltet i den refererte container-posten som gjeldende post ble opprettet for.</span><span class="sxs-lookup"><span data-stu-id="81092-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="81092-127">Hvis `path`-argumentet refererer til en datakilde for en av *Opplisting*-typene, legges det til en ny post i listen som opprettes, for hver opplistingsverdi i opplistingsposten det refereres til.</span><span class="sxs-lookup"><span data-stu-id="81092-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="81092-128">For hver post som opprettes, returnerer **Navn**-feltet verdien for den refererte opplistingen som gjeldende post ble opprettet for. **Beskrivelse**-feltet returnerer beskrivelsen av denne opplistingen, og **Etikett**-feltet returnerer etiketten for denne opplistingen.</span><span class="sxs-lookup"><span data-stu-id="81092-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="81092-129">Når syntaks 1 brukes i kjøretid, må **Etikett**- og **Beskrivelse**-feltene returnere verdier som er basert på språkinnstillingene for ER-formatet som kjører:</span><span class="sxs-lookup"><span data-stu-id="81092-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="81092-130">Hvis etikettene og beskrivelsene for det forespurte språket er tilgjengelige, returnerer **Etikett**- og **Beskrivelse**-feltene verdier som er basert på dette språket, og **IsTranslated**-feltet returnerer **Sann**.</span><span class="sxs-lookup"><span data-stu-id="81092-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="81092-131">Hvis etikettene og beskrivelsene for det forespurte språket ikke er tilgjengelige, returnerer **Etikett**- og **Beskrivelse**-feltene verdier som er basert på standard **EN-US**-språket, og **IsTranslated**-feltet returnerer **Usann**.</span><span class="sxs-lookup"><span data-stu-id="81092-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="81092-132">Når syntaks 2 brukes i kjøretid, må **Etikett**- og **Beskrivelse**-feltene returnere verdier som er basert på språket som er definert som det andre argumentet for den kalte funksjonen:</span><span class="sxs-lookup"><span data-stu-id="81092-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="81092-133">Hvis etikettene og beskrivelsene for det forespurte språket er tilgjengelige, returnerer **Etikett**- og **Beskrivelse**-feltene verdier som er basert på dette språket, og **IsTranslated**-feltet returnerer **Sann**.</span><span class="sxs-lookup"><span data-stu-id="81092-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="81092-134">Hvis etikettene og beskrivelsene for det forespurte språket ikke er tilgjengelige, returnerer **Etikett**- og **Beskrivelse**-feltene verdier som er basert på **EN-US**-språket, og **IsTranslated**-feltet returnerer **Usann**.</span><span class="sxs-lookup"><span data-stu-id="81092-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="81092-135">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="81092-135">Example 1</span></span>

<span data-ttu-id="81092-136">I følgende illustrasjon introduseres en opplisting i en ER-datamodell.</span><span class="sxs-lookup"><span data-stu-id="81092-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="81092-137">Illustrasjonen nedenfor viser disse detaljene:</span><span class="sxs-lookup"><span data-stu-id="81092-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="81092-138">Modellopplistingen settes inn i en rapport som en datakilde.</span><span class="sxs-lookup"><span data-stu-id="81092-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="81092-139">Et ER-uttrykk bruker modellopplistingen som en parameter i `LISTOFFIELDS`-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="81092-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="81092-140">En datakilde av *Postliste*-typen settes inn i en rapport ved hjelp av det opprettede ER-uttrykket.</span><span class="sxs-lookup"><span data-stu-id="81092-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="81092-141">Eksemplet nedenfor viser elementene i ER-formatet som er bundet til datakilden for *Postliste*-typen som ble opprettet ved hjelp av funksjonen `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="81092-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="81092-142">Følgende illustrasjon viser resultatet når det utformede formatet kjøres.</span><span class="sxs-lookup"><span data-stu-id="81092-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="81092-143">Basert på språkinnstillingene for de overordnede **FILE** og **FOLDER**-formatelementene, angis oversatt tekst for etiketter og beskrivelser i utdataene i ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="81092-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="81092-144">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="81092-144">Example 2</span></span>

<span data-ttu-id="81092-145">Du bruker *Beregnet felt*-datakildetypen til å konfigurere **enumType\_de** og **enumType\_deCH**-datakildene for **enumType**-datamodellopplistingen:</span><span class="sxs-lookup"><span data-stu-id="81092-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="81092-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="81092-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="81092-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="81092-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="81092-148">I dette tilfellet kan du bruke følgende uttrykk til å hente etiketten for opplistingsverdien på sveitsisk (tysk) hvis denne oversettelsen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="81092-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="81092-149">Hvis sveitsisk (tysk) oversettelse ikke er tilgjengelig, er etiketten på tysk.</span><span class="sxs-lookup"><span data-stu-id="81092-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="81092-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="81092-150">Additional resources</span></span>

[<span data-ttu-id="81092-151">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="81092-151">List functions</span></span>](er-functions-category-list.md)
