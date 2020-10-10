---
title: GETENUMVALUEBYNAME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: 722ea8ea233d617b0584e21e98073428f16c0801
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885233"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="f1d22-103">GETENUMVALUEBYNAME ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="f1d22-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1d22-104">`GETENUMVALUEBYNAME`-funksjonen søker etter en bestemt *opplistings*-verdi i den angitte opplistingsdatakilden ved hjelp av opplistingsnavnet som er angitt som en *Streng*-verdi.</span><span class="sxs-lookup"><span data-stu-id="f1d22-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="f1d22-105">Hvis *opplistings*-verdien blir funnet, returnerer funksjonen den.</span><span class="sxs-lookup"><span data-stu-id="f1d22-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="f1d22-106">Hvis ikke returnerer funksjonen opplistingsverdien **null**.</span><span class="sxs-lookup"><span data-stu-id="f1d22-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1d22-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f1d22-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="f1d22-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f1d22-108">Arguments</span></span>

<span data-ttu-id="f1d22-109">`enumeration data source path`: *Opplisting*</span><span class="sxs-lookup"><span data-stu-id="f1d22-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="f1d22-110">Den gyldige referansebanen til en datakilde for en av følgende opplistingstyper:</span><span class="sxs-lookup"><span data-stu-id="f1d22-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="f1d22-111">ER-modellopplisting</span><span class="sxs-lookup"><span data-stu-id="f1d22-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="f1d22-112">ER-formatopplisting</span><span class="sxs-lookup"><span data-stu-id="f1d22-112">ER format enumeration</span></span>
- <span data-ttu-id="f1d22-113">Microsoft Dynamics 365 Finance-opplisting</span><span class="sxs-lookup"><span data-stu-id="f1d22-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="f1d22-114">`enumeration value text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f1d22-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="f1d22-115">En strengverdi som representerer navnet på en enkelt opplistingsverdi.</span><span class="sxs-lookup"><span data-stu-id="f1d22-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1d22-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="f1d22-116">Return values</span></span>

<span data-ttu-id="f1d22-117">*Opplisting* som kan nullstilles</span><span class="sxs-lookup"><span data-stu-id="f1d22-117">Nullable *Enum*</span></span>

<span data-ttu-id="f1d22-118">Den resulterende opplistingsverdien.</span><span class="sxs-lookup"><span data-stu-id="f1d22-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f1d22-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="f1d22-119">Usage notes</span></span>

<span data-ttu-id="f1d22-120">Det blir ikke registrert noe unntak hvis en *opplisting*-verdi ikke blir funnet ved å bruke navnet på opplistingsverdien som er angitt som en *streng*-verdi.</span><span class="sxs-lookup"><span data-stu-id="f1d22-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f1d22-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="f1d22-121">Example 1</span></span>

<span data-ttu-id="f1d22-122">I følgende illustrasjon introduseres opplistingen **ReportDirection** i en datamodell.</span><span class="sxs-lookup"><span data-stu-id="f1d22-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="f1d22-123">Legg merke til at etiketter er definert for opplistingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="f1d22-123">Notice that labels are defined for the enumeration values.</span></span>

![Tilgjengelige verdier for en datamodellopplisting](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="f1d22-125">Illustrasjonen nedenfor viser disse detaljene:</span><span class="sxs-lookup"><span data-stu-id="f1d22-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="f1d22-126">Datakilden **$Direction** er konfigurert i en ER-rapport.</span><span class="sxs-lookup"><span data-stu-id="f1d22-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="f1d22-127">Denne datakilden er konfigurert basert på **ReportDirection**-modellopplistingen.</span><span class="sxs-lookup"><span data-stu-id="f1d22-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="f1d22-128">Uttrykket `$IsArrivals` er utformet for å bruke den modellopplistingsbaserte **$Direction**-datakilden som en parameter for denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1d22-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="f1d22-129">Verdien av denne sammenligningen er **SANN**.</span><span class="sxs-lookup"><span data-stu-id="f1d22-129">The value of this comparison expression is **TRUE**.</span></span>

![Eksempel på en datamodellopplisting](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="f1d22-131">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="f1d22-131">Example 2</span></span>

<span data-ttu-id="f1d22-132">Funksjonene `GETENUMVALUEBYNAME` og [`LISTOFFIELDS`](er-functions-list-listoffields.md) lar deg hente verdier og etiketter for støttede opplistinger som tekstverdier.</span><span class="sxs-lookup"><span data-stu-id="f1d22-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="f1d22-133">(De støttede opplistingene er programopplistinger, datamodellopplistinger og formatopplistinger.)</span><span class="sxs-lookup"><span data-stu-id="f1d22-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="f1d22-134">I følgende illustrasjon introduseres datakilden **TransType** i en modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="f1d22-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="f1d22-135">Denne datakilden refererer til programopplistingen **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="f1d22-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Datakilde for en modelltilordning som refererer til en programopplisting](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="f1d22-137">Følgende illustrasjon viser datakilden **TransTypeList** som konfigureres i en modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="f1d22-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="f1d22-138">Denne datakilden er konfigurert basert på **TransType**-programopplistingen.</span><span class="sxs-lookup"><span data-stu-id="f1d22-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="f1d22-139">Funksjonen `LISTOFFIELDS` brukes til å returnere alle opplistingsverdier som en liste med poster som inneholder felt.</span><span class="sxs-lookup"><span data-stu-id="f1d22-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="f1d22-140">På denne måten vises detaljene for hver opplistingsverdi.</span><span class="sxs-lookup"><span data-stu-id="f1d22-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="f1d22-141">Feltet **EnumValue** er konfigurert for datakilden **TransTypeList** ved hjelp av uttrykket `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`.</span><span class="sxs-lookup"><span data-stu-id="f1d22-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="f1d22-142">Dette feltet returnerer en nummereringsverdi for hver post i denne listen.</span><span class="sxs-lookup"><span data-stu-id="f1d22-142">This field returns an enumeration value for every record in this list.</span></span>

![Datakilde for en modelltilordning som returnerer alle opplistingsverdier for en valgt opplisting som en liste med oppføringer](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="f1d22-144">Følgende illustrasjon viser datakilden **VendTrans** som konfigureres i en modelltilordning.</span><span class="sxs-lookup"><span data-stu-id="f1d22-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="f1d22-145">Denne datakilden returnerer leverandørtransaksjonsposter fra **VendTrans**-programtabellen.</span><span class="sxs-lookup"><span data-stu-id="f1d22-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="f1d22-146">Finanstypen for hver transaksjon defineres av verdien til **TransType**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1d22-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="f1d22-147">Feltet **TransTypeTitle** er konfigurert for datakilden **VendTrans** ved hjelp av uttrykket `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`.</span><span class="sxs-lookup"><span data-stu-id="f1d22-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="f1d22-148">Dette feltet returnerer etiketten for en opplistingsverdi for den gjeldende transaksjonen som tekst, hvis denne opplistingsverdien er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f1d22-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="f1d22-149">Ellers returneres en tom strengverdi.</span><span class="sxs-lookup"><span data-stu-id="f1d22-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="f1d22-150">Feltet **TransTypeTitle** er bundet til **LedgerType**-feltet i en datamodell som gjør at denne informasjonen kan brukes i alle ER-format som bruker datamodellen som en datakilde.</span><span class="sxs-lookup"><span data-stu-id="f1d22-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Datakilde for en modelltilordning som returnerer leverandørtransaksjoner](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="f1d22-152">Illustrasjonen nedenfor viser hvordan du kan bruke [feilsøkingsprogrammet for datakilde](er-debug-data-sources.md) til å teste den konfigurerte modelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="f1d22-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Bruke feilsøkingsprogrammet for datakilde til å teste den konfigurerte modelltilordningen](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="f1d22-154">Feltet **LedgerType** i en datamodell viser etiketter med transaksjonstyper som forventet.</span><span class="sxs-lookup"><span data-stu-id="f1d22-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="f1d22-155">Hvis du planlegger å bruke denne fremgangsmåten for en stor mengde transaksjonsdata, må du vurdere utførelsesytelsen.</span><span class="sxs-lookup"><span data-stu-id="f1d22-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="f1d22-156">Hvis du vil ha mer informasjon, kan du se [Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="f1d22-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1d22-157">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f1d22-157">Additional resources</span></span>

[<span data-ttu-id="f1d22-158">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f1d22-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="f1d22-159">Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer</span><span class="sxs-lookup"><span data-stu-id="f1d22-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="f1d22-160">LISTOFFIELDS ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="f1d22-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="f1d22-161">FIRSTORNULL ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="f1d22-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="f1d22-162">WHERE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="f1d22-162">WHERE ER function</span></span>](er-functions-list-where.md)
