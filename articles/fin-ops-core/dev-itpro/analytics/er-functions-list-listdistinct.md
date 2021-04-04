---
title: LISTDISTINCT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LISTDISTINCT.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: f20565d73cea8d0cc1361bd03cda86a79a97955e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563830"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="a891f-103">LISTDISTINCT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="a891f-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a891f-104">`LISTDISTINCT`-funksjonen beregner det angitte uttrykket som en velger for hver post i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="a891f-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="a891f-105">Den returnerer en ny *Postliste*-verdi som inneholder én enkelt post for hver unike velgerverdi.</span><span class="sxs-lookup"><span data-stu-id="a891f-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a891f-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a891f-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="a891f-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a891f-107">Arguments</span></span>

<span data-ttu-id="a891f-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="a891f-108">`list`: *Record list*</span></span>

<span data-ttu-id="a891f-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="a891f-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a891f-110">`selector`: *Primitiv datatype*</span><span class="sxs-lookup"><span data-stu-id="a891f-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="a891f-111">Et gyldig uttrykk som brukes til å beregne en utvalgsverdi for hver post i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="a891f-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="a891f-112">Følgende datatyper støttes for denne parameteren:</span><span class="sxs-lookup"><span data-stu-id="a891f-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="a891f-113">Boolsk</span><span class="sxs-lookup"><span data-stu-id="a891f-113">Boolean</span></span>
- <span data-ttu-id="a891f-114">Dato</span><span class="sxs-lookup"><span data-stu-id="a891f-114">Date</span></span>
- <span data-ttu-id="a891f-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="a891f-115">DateTime</span></span>
- <span data-ttu-id="a891f-116">Guid</span><span class="sxs-lookup"><span data-stu-id="a891f-116">GUID</span></span>
- <span data-ttu-id="a891f-117">Heltall</span><span class="sxs-lookup"><span data-stu-id="a891f-117">Integer</span></span>
- <span data-ttu-id="a891f-118">Int64</span><span class="sxs-lookup"><span data-stu-id="a891f-118">Int64</span></span>
- <span data-ttu-id="a891f-119">Kommatall</span><span class="sxs-lookup"><span data-stu-id="a891f-119">Real</span></span>
- <span data-ttu-id="a891f-120">Streng</span><span class="sxs-lookup"><span data-stu-id="a891f-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="a891f-121">Returverdier</span><span class="sxs-lookup"><span data-stu-id="a891f-121">Return values</span></span>

<span data-ttu-id="a891f-122">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="a891f-122">*Record list*</span></span>

<span data-ttu-id="a891f-123">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="a891f-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a891f-124">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="a891f-124">Usage notes</span></span>

<span data-ttu-id="a891f-125">Strukturen i listen som opprettes, samsvarer med strukturen i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="a891f-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="a891f-126">Den samme velgerverdien kan beregnes for flere poster i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="a891f-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="a891f-127">I dette tilfellet er feltverdiene for den tilsvarende posten i den opprettede listen lik verdiene til den første posten fra den angitte listen som velgerverdien beregnes for.</span><span class="sxs-lookup"><span data-stu-id="a891f-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="a891f-128">Kjøringen av denne funksjonen utføres på alle datakilder for [elektronisk rapportering (ER)](general-electronic-reporting.md) for *Postliste*-typen som finnes i minnet.</span><span class="sxs-lookup"><span data-stu-id="a891f-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="a891f-129">Datakilden **GROUPBY** kan også brukes til å generere listen over poster som velgeren som har distinkte verdier, beregnes for.</span><span class="sxs-lookup"><span data-stu-id="a891f-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="a891f-130">Fra et ytelses- og minneforbruksperspektiv er det imidlertid bedre å bruke `LISTDISTINCT`-funksjonen enn datakilden **GROUPBY**, fordi kjøringen av funksjonen utføres i minnet.</span><span class="sxs-lookup"><span data-stu-id="a891f-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="a891f-131">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a891f-131">Example</span></span>

<span data-ttu-id="a891f-132">Følgende eksempel viser hvordan du kan hente listen over unike kundekontonumre som minst én salgsfaktura eller prosjektfaktura har blitt utstedt til, i løpet av en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="a891f-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="a891f-133">Angi **SalesInvoice**-datakilden for `Record list`-typen som refererer til apptabellen **CustInvoiceJour**, og filtrerer salgsfakturaer for bestemte perioder.</span><span class="sxs-lookup"><span data-stu-id="a891f-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="a891f-134">`InvoiceAccount`-feltet i denne datakilden returnerer kontonummeret til en fakturert kunde.</span><span class="sxs-lookup"><span data-stu-id="a891f-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="a891f-135">Angi **ProjectInvoice**-datakilden for `Record list`-typen som refererer til apptabellen **ProjInvoiceJour**, og filtrerer prosjektfakturaer for bestemte perioder.</span><span class="sxs-lookup"><span data-stu-id="a891f-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="a891f-136">`InvoiceAccount`-feltet i denne datakilden returnerer kontonummeret til en fakturert kunde.</span><span class="sxs-lookup"><span data-stu-id="a891f-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="a891f-137">Konfigurer datakilden **AllInvoices** for `Calculated field`-typen som inneholder uttrykket `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="a891f-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="a891f-138">Denne datakilden returnerer den sammenføyde listen over salgsfakturaer og prosjektfakturaer.</span><span class="sxs-lookup"><span data-stu-id="a891f-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="a891f-139">Konfigurer datakilden **InvoicedCustomer** for `Record list`-typen som inneholder uttrykket `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="a891f-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="a891f-140">Denne datakilden returnerer en ny liste som inneholder én enkelt post for hver unike kunde som er fakturert i løpet av den definerte perioden.</span><span class="sxs-lookup"><span data-stu-id="a891f-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="a891f-141">`InvoiceAccount`-feltet i denne listen inneholder et kundekontonummer.</span><span class="sxs-lookup"><span data-stu-id="a891f-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a891f-142">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a891f-142">Additional resources</span></span>

[<span data-ttu-id="a891f-143">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="a891f-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]