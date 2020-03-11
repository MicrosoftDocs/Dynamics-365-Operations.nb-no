---
title: NUMSEQVALUE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMSEQVALUE.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: fbe5e5ac17af743f8293e4255d9713b528182f66
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041314"
---
# <span data-ttu-id="19e32-103"><a name="NUMSEQVALUE">NUMSEQVALUE ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="19e32-103"><a name="NUMSEQVALUE">NUMSEQVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19e32-104">`NUMSEQVALUE`-funksjonen returnerer en *streng*-verdi som representerer den nye genererte verdien av en nummerserie, basert på den angitte nummerserien, omfanget og område-IDen.</span><span class="sxs-lookup"><span data-stu-id="19e32-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="19e32-105">Område-IDen er lik firmakoden som angis av konteksten som ER-formatet kjøres under.</span><span class="sxs-lookup"><span data-stu-id="19e32-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="19e32-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="19e32-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="19e32-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="19e32-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="19e32-108">Syntaks 3</span><span class="sxs-lookup"><span data-stu-id="19e32-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="19e32-109">Argumenter</span><span class="sxs-lookup"><span data-stu-id="19e32-109">Arguments</span></span>

<span data-ttu-id="19e32-110">`number sequence code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="19e32-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="19e32-111">En tekstverdi som representerer koden for nummerserien som en ny verdi kreves i.</span><span class="sxs-lookup"><span data-stu-id="19e32-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="19e32-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="19e32-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="19e32-113">En *Int64*-verdi som representerer post-IDen for en post i NumberSequenceTable-tabellen som inneholder definisjonen av nummerserien som en ny verdi kreves i.</span><span class="sxs-lookup"><span data-stu-id="19e32-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="19e32-114">`scope type`: *Opplistingsverdi*</span><span class="sxs-lookup"><span data-stu-id="19e32-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="19e32-115">En opplistingsverdi for **ERExpressionNumberSequenceScopeType**-opplistingen som definerer omfanget av nummerserien som en ny verdi kreves i.</span><span class="sxs-lookup"><span data-stu-id="19e32-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="19e32-116">De tilgjengelige omfangstypene er **delt**, **juridisk enhet** og **firma**.</span><span class="sxs-lookup"><span data-stu-id="19e32-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="19e32-117">`scope ID`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="19e32-117">`scope ID`: *String*</span></span>

<span data-ttu-id="19e32-118">En *streng*-verdi som identifiserer omfanget, basert på den angitte omfangstypen.</span><span class="sxs-lookup"><span data-stu-id="19e32-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="19e32-119">Returverdier</span><span class="sxs-lookup"><span data-stu-id="19e32-119">Return values</span></span>

<span data-ttu-id="19e32-120">*Streng*</span><span class="sxs-lookup"><span data-stu-id="19e32-120">*String*</span></span>

<span data-ttu-id="19e32-121">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="19e32-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="19e32-122">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="19e32-122">Usage notes</span></span>

<span data-ttu-id="19e32-123">For **Delt**-omfangstypen angir du en tom streng som område-ID.</span><span class="sxs-lookup"><span data-stu-id="19e32-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="19e32-124">For omfangstypene **Firma** og **Juridisk enhet** angir du firmakoden som område-ID.</span><span class="sxs-lookup"><span data-stu-id="19e32-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="19e32-125">Hvis du angir en tom streng som område-ID for disse omfangstypene, brukes den gjeldende firmakoden.</span><span class="sxs-lookup"><span data-stu-id="19e32-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="19e32-126">Når syntaks 1 brukes, er nummerserien forespurt for **Firma**-omfangstypen, og firmakoden angis av konteksten som ER-formatet kjøres under.</span><span class="sxs-lookup"><span data-stu-id="19e32-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="19e32-127">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="19e32-127">Example 1</span></span>

<span data-ttu-id="19e32-128">I ER-format definerer du **AskNumSeq**-datakilden for *Inndataparameter*-typen.</span><span class="sxs-lookup"><span data-stu-id="19e32-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="19e32-129">Denne datakilden refererer til den utvidede datatypen **Beskrivelse** (EDT).</span><span class="sxs-lookup"><span data-stu-id="19e32-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="19e32-130">Deretter definerer du **NumSeq**-datakilden for *Beregnet felt*-typen.</span><span class="sxs-lookup"><span data-stu-id="19e32-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="19e32-131">Denne datakilden inneholder uttrykket `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="19e32-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="19e32-132">Når **NumSeq**-datakilden kalles, returneres den nye genererte verdien av nummerserien som ble angitt under kjøring ved å skrive inn koden i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="19e32-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="19e32-133">Nummerserien blir forespurt for **Firma**-omfangstypen.</span><span class="sxs-lookup"><span data-stu-id="19e32-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="19e32-134">Firmakoden angis av konteksten som ER-formatet kjøres under.</span><span class="sxs-lookup"><span data-stu-id="19e32-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="19e32-135">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="19e32-135">Example 2</span></span>

<span data-ttu-id="19e32-136">Følgende datakilder defineres i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="19e32-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="19e32-137">**LedgerParms**-datakilden for *Tabell*-typen.</span><span class="sxs-lookup"><span data-stu-id="19e32-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="19e32-138">Denne datakilden refererer til LedgerParameters-tabellen.</span><span class="sxs-lookup"><span data-stu-id="19e32-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="19e32-139">**NumSeq**-datakilden for *Beregnet felt*-typen.</span><span class="sxs-lookup"><span data-stu-id="19e32-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="19e32-140">Denne datakilden inneholder uttrykket `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="19e32-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="19e32-141">Når **NumSeq**-datatypen kalles opp, returneres den nye genererte verdien for nummerserien som er konfigurert i økonomimodul-parameterne for firmaet som leverer konteksten som ER-formatet kjøres under.</span><span class="sxs-lookup"><span data-stu-id="19e32-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="19e32-142">Denne nummerserien identifiserer journaler unikt og fungerer som et partinummer som kobler sammen transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="19e32-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="19e32-143">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="19e32-143">Example 3</span></span>

<span data-ttu-id="19e32-144">Følgende datakilder defineres i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="19e32-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="19e32-145">Datakilden **enumScope** for Microsoft Dynamics 365 Finance *-opplistingstypen*.</span><span class="sxs-lookup"><span data-stu-id="19e32-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="19e32-146">Denne datakilden refererer til opplistingen **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="19e32-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="19e32-147">**NumSeq**-datakilden for *Beregnet felt*-typen.</span><span class="sxs-lookup"><span data-stu-id="19e32-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="19e32-148">Denne datakilden inneholder uttrykket `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="19e32-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="19e32-149">Når **NumSeq**-datatypen kalles opp, returneres den nye genererte verdien for **Gene\_1**-nummerserien som er konfigurert for firmaet som levererte konteksten som ER-formatet kjøres under.</span><span class="sxs-lookup"><span data-stu-id="19e32-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19e32-150">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="19e32-150">Additional resources</span></span>

[<span data-ttu-id="19e32-151">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="19e32-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
