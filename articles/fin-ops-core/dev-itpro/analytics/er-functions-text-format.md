---
title: FORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FORMAT.
author: NickSelin
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
ms.openlocfilehash: 6ee53ef3c1a8820f75580e2f9fbd48575d6a828f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746466"
---
# <a name="format-er-function"></a><span data-ttu-id="64986-103">FORMAT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="64986-103">FORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64986-104">`FORMAT`-funksjonen returnerer den angitte strengen som en *streng*-verdi etter at den er formatert ved å erstatte forekomster av **%N** med *N*-te argumentet.</span><span class="sxs-lookup"><span data-stu-id="64986-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N* th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="64986-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="64986-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="64986-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="64986-106">Arguments</span></span>

<span data-ttu-id="64986-107">`string`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="64986-107">`string`: *String*</span></span>

<span data-ttu-id="64986-108">En referanse til en datakilde for *Streng*-datatypen som må formateres.</span><span class="sxs-lookup"><span data-stu-id="64986-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="64986-109">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="64986-109">This argument is required.</span></span>

<span data-ttu-id="64986-110">`argument 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="64986-110">`argument 1`: *String*</span></span>

<span data-ttu-id="64986-111">Det første argumentet, som brukes til å erstatte forekomster av **%1**.</span><span class="sxs-lookup"><span data-stu-id="64986-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="64986-112">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="64986-112">This argument is required.</span></span>

<span data-ttu-id="64986-113">`argument N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="64986-113">`argument N`: *String*</span></span>

<span data-ttu-id="64986-114">Det *N*-te argumentet, som brukes til å erstatte forekomster av **%2**, **%3**, osv.</span><span class="sxs-lookup"><span data-stu-id="64986-114">The *N* th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="64986-115">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="64986-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="64986-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="64986-116">Return values</span></span>

<span data-ttu-id="64986-117">*Streng*</span><span class="sxs-lookup"><span data-stu-id="64986-117">*String*</span></span>

<span data-ttu-id="64986-118">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="64986-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="64986-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="64986-119">Usage notes</span></span>

<span data-ttu-id="64986-120">Hvis et argument ikke er angitt for en parameter, returneres parameteren som **"%N"** i strengen.</span><span class="sxs-lookup"><span data-stu-id="64986-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="64986-121">For verdier for *reell*-typen begrenses standard strengkonverteringen til to desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="64986-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="64986-122">Eksempel</span><span class="sxs-lookup"><span data-stu-id="64986-122">Example</span></span>

<span data-ttu-id="64986-123">I illustrasjonen nedenfor returnerer **PaymentModel**-datakilden en liste over kundeposter ved hjelp av **Kunde**-komponenten.</span><span class="sxs-lookup"><span data-stu-id="64986-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="64986-124">Den returnerer behandlingsdatoverdien ved hjelp av **ProcessingDate**-feltet.</span><span class="sxs-lookup"><span data-stu-id="64986-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="64986-125">I ER-formatet som er utformet for å generere en elektronisk fil for utvalgte kunder, velges **PaymentModel** som en datakilde og styrer prosessflyten.</span><span class="sxs-lookup"><span data-stu-id="64986-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="64986-126">Et unntak for å informere brukeren iverksettes hvis en valgt kunde stoppes for datoen da rapporten behandles.</span><span class="sxs-lookup"><span data-stu-id="64986-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="64986-127">Formelen som er utviklet for denne typen behandlingskontroll kan bruke følgende ressurser:</span><span class="sxs-lookup"><span data-stu-id="64986-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="64986-128">Etiketten SYS70894, som har følgende tekst:</span><span class="sxs-lookup"><span data-stu-id="64986-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="64986-129">**For EN-US språk:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="64986-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="64986-130">**For DE-språk:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="64986-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="64986-131">Etiketten SYS18389, som har følgende tekst:</span><span class="sxs-lookup"><span data-stu-id="64986-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="64986-132">**For EN-US-språk:** "Customer %1 is stopped for %2."</span><span class="sxs-lookup"><span data-stu-id="64986-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="64986-133">**For DE-språk:** "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="64986-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="64986-134">Her er uttrykket som kan utformes.</span><span class="sxs-lookup"><span data-stu-id="64986-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="64986-135">Hvis en rapport behandles for **Litware Retail**-kunden 17. desember 2015 i **EN-US**-kulturen og **EN-US**-språket, returnerer denne formelen teksten nedenfor, som kan vises for brukeren som en unntaksmelding:</span><span class="sxs-lookup"><span data-stu-id="64986-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="64986-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span><span class="sxs-lookup"><span data-stu-id="64986-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="64986-137">Hvis den samme rapporten behandles for **Litware Retail**-kunden 17. desember 2015, i **DE**-kulturen og **DE**-språket, returnerer formelen følgende tekst som bruker et annet datoformat:</span><span class="sxs-lookup"><span data-stu-id="64986-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="64986-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="64986-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="64986-139">Følgende syntaks brukes i ER-formler for etiketter:</span><span class="sxs-lookup"><span data-stu-id="64986-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="64986-140">**For etiketter fra ressurser i Microsoft Dynamics 365 Finance-appen:** **\@X**, der **X** er etikett-ID-en i applikasjonsobjekttreet (AOT)</span><span class="sxs-lookup"><span data-stu-id="64986-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="64986-141">**For etiketter som ligger i ER-konfigurasjoner:** **@"GER_LABEL:X"**, der **X** er etikett-ID-en i ER-konfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="64986-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64986-142">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="64986-142">Additional resources</span></span>

[<span data-ttu-id="64986-143">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="64986-143">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]