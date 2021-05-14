---
title: Legge til datafelt i avgiftsintegrering ved hjelp av utvidelser
description: Dette emnet beskriver hvordan du bruker utvidelser i X++ til å legge til datafelt i avgiftsintegrasjonen.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8e3573f9c9971d4a5af33ece08b7e0b43f2e813a
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921171"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="02483-103">Legg til datafelt i avgiftsintegrering ved hjelp av utvidelser</span><span class="sxs-lookup"><span data-stu-id="02483-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="02483-104">Dette emnet beskriver hvordan du bruker utvidelser i X++ til å legge til datafelt i avgiftsintegrasjonen.</span><span class="sxs-lookup"><span data-stu-id="02483-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="02483-105">Disse feltene kan utvides til avgiftsdatamodellen for avgiftstjenesten og brukes til å bestemme avgiftskoder.</span><span class="sxs-lookup"><span data-stu-id="02483-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="02483-106">Hvis du vil ha mer informasjon, kan du se [Legge til datafelt i avgiftskonfigurasjoner](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="02483-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="02483-107">Datamodell</span><span class="sxs-lookup"><span data-stu-id="02483-107">Data model</span></span>

<span data-ttu-id="02483-108">Dataene i datamodellen bæres av objekter og implementeres av klasser.</span><span class="sxs-lookup"><span data-stu-id="02483-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="02483-109">Her er en liste over de viktigste objektene:</span><span class="sxs-lookup"><span data-stu-id="02483-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="02483-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="02483-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="02483-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="02483-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="02483-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="02483-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="02483-113">Illustrasjonen nedenfor viser hvordan disse objektene er relatert.</span><span class="sxs-lookup"><span data-stu-id="02483-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="02483-114">[![Datamodellobjektrelasjon](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="02483-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="02483-115">Et **Document**-objekt kan inneholde mange **Line**-objekter.</span><span class="sxs-lookup"><span data-stu-id="02483-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="02483-116">Hvert objekt inneholder metadata for avgiftstjenesten.</span><span class="sxs-lookup"><span data-stu-id="02483-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="02483-117">`TaxIntegrationDocumentObject` har `originAddress`-metadata, som inneholder informasjon om kildeadressen og `includingTax`-metadata, som angir om linjebeløpet omfatter merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="02483-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="02483-118">`TaxIntegrationLineObject` har `itemId`-, `quantity`- og `categoryId`-metadata.</span><span class="sxs-lookup"><span data-stu-id="02483-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="02483-119">`TaxIntegrationLineObject` implementerer også **Charge**-objekter.</span><span class="sxs-lookup"><span data-stu-id="02483-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="02483-120">Integrasjonsflyt</span><span class="sxs-lookup"><span data-stu-id="02483-120">Integration flow</span></span>

<span data-ttu-id="02483-121">Dataene i flyten blir manipulert av aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="02483-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="02483-122">Nøkkelaktiviteter</span><span class="sxs-lookup"><span data-stu-id="02483-122">Key activities</span></span>

* <span data-ttu-id="02483-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="02483-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="02483-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="02483-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="02483-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="02483-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="02483-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="02483-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="02483-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="02483-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="02483-128">Aktiviteter kjøres i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="02483-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="02483-129">Angi henting</span><span class="sxs-lookup"><span data-stu-id="02483-129">Setting Retrieval</span></span>
2. <span data-ttu-id="02483-130">Datahenting</span><span class="sxs-lookup"><span data-stu-id="02483-130">Data Retrieval</span></span>
3. <span data-ttu-id="02483-131">Beregningstjeneste</span><span class="sxs-lookup"><span data-stu-id="02483-131">Calculation Service</span></span>
4. <span data-ttu-id="02483-132">Valutabytte</span><span class="sxs-lookup"><span data-stu-id="02483-132">Currency Exchange</span></span>
5. <span data-ttu-id="02483-133">Dataholdbarhet</span><span class="sxs-lookup"><span data-stu-id="02483-133">Data Persistence</span></span>

<span data-ttu-id="02483-134">Du kan for eksempel utvide **Datahenting** før **Beregningstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="02483-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="02483-135">Datahenting-aktiviteter</span><span class="sxs-lookup"><span data-stu-id="02483-135">Data Retrieval activities</span></span>

<span data-ttu-id="02483-136">**Datahenting**-aktiviteter henter data fra databasen.</span><span class="sxs-lookup"><span data-stu-id="02483-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="02483-137">Kort for ulike transaksjoner kan hente data fra ulike transaksjonstabeller:</span><span class="sxs-lookup"><span data-stu-id="02483-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="02483-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="02483-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="02483-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="02483-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="02483-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="02483-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="02483-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="02483-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="02483-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="02483-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="02483-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="02483-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="02483-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="02483-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="02483-145">I disse **Datahenting**-aktivitetene kopieres data fra databasen til `TaxIntegrationDocumentObject` og `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="02483-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="02483-146">Fordi alle disse aktivitetene utvider den samme abstrakte malklassen, har de felles metoder.</span><span class="sxs-lookup"><span data-stu-id="02483-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="02483-147">Beregningstjeneste-aktiviteter</span><span class="sxs-lookup"><span data-stu-id="02483-147">Calculation Service activities</span></span>

<span data-ttu-id="02483-148">**Beregningstjeneste**-aktiviteten er koblingen mellom avgiftstjenesten og avgiftsintegreringen.</span><span class="sxs-lookup"><span data-stu-id="02483-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="02483-149">Denne aktiviteten er ansvarlig for følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="02483-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="02483-150">Konstruer forespørselen.</span><span class="sxs-lookup"><span data-stu-id="02483-150">Construct the request.</span></span>
2. <span data-ttu-id="02483-151">Poster forespørselen til avgiftstjenesten.</span><span class="sxs-lookup"><span data-stu-id="02483-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="02483-152">Få svar fra avgiftstjenesten.</span><span class="sxs-lookup"><span data-stu-id="02483-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="02483-153">Del opp svaret.</span><span class="sxs-lookup"><span data-stu-id="02483-153">Parse the response.</span></span>

<span data-ttu-id="02483-154">Et datafelt som du legger til i forespørselen, blir postert sammen med andre metadata.</span><span class="sxs-lookup"><span data-stu-id="02483-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="02483-155">Utvidelsesimplementering</span><span class="sxs-lookup"><span data-stu-id="02483-155">Extension implementation</span></span>

<span data-ttu-id="02483-156">I denne delen finner du detaljerte trinn som forklarer hvordan du implementerer utvidelsen.</span><span class="sxs-lookup"><span data-stu-id="02483-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="02483-157">Den bruker finansdimensjonene **Kostsenter** og **Prosjekt** som eksempler.</span><span class="sxs-lookup"><span data-stu-id="02483-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="02483-158">Trinn 1.</span><span class="sxs-lookup"><span data-stu-id="02483-158">Step 1.</span></span> <span data-ttu-id="02483-159">Legge til datavariabelen i objektklassen</span><span class="sxs-lookup"><span data-stu-id="02483-159">Add the data variable in the object class</span></span>

<span data-ttu-id="02483-160">Objektklassen inneholder datavariabelen og getter/setter-metodene for dataene.</span><span class="sxs-lookup"><span data-stu-id="02483-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="02483-161">Legg til datafeltet i `TaxIntegrationDocumentObject` eller `TaxIntegrationLineObject`, avhengig av nivået til feltet.</span><span class="sxs-lookup"><span data-stu-id="02483-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="02483-162">I eksemplet nedenfor brukes linjenivået, og filnavnet er `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="02483-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="02483-163">Hvis datafeltet du legger til, er på dokumentnivå, endrer du filnavnet til `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="02483-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="02483-164">**Kostsenter** og **Prosjekt** legges til som private variabler.</span><span class="sxs-lookup"><span data-stu-id="02483-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="02483-165">Opprett getter- og setter-metoder for disse datafeltene for å manipulere dataene.</span><span class="sxs-lookup"><span data-stu-id="02483-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="02483-166">Trinn 2.</span><span class="sxs-lookup"><span data-stu-id="02483-166">Step 2.</span></span> <span data-ttu-id="02483-167">Hente data fra databasen</span><span class="sxs-lookup"><span data-stu-id="02483-167">Retrieve data from the database</span></span>

<span data-ttu-id="02483-168">Angi transaksjonen, og utvid de riktige kortklassene for å hente dataene.</span><span class="sxs-lookup"><span data-stu-id="02483-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="02483-169">Hvis du for eksempel bruker en **Bestilling**-transaksjon, må du utvide `TaxIntegrationPurchTableDataRetrieval` og `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="02483-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="02483-170">`TaxIntegrationPurchParmTableDataRetrieval` arves fra `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="02483-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="02483-171">Dette bør ikke endres med mindre logikken for `purchTable`- og `purchParmTable`-tabellene er forskjellig.</span><span class="sxs-lookup"><span data-stu-id="02483-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="02483-172">Hvis datafeltet skal legges til for alle transaksjoner, utvider du alle `DataRetrieval`-klassene.</span><span class="sxs-lookup"><span data-stu-id="02483-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="02483-173">Fordi alle **Datahenting**-aktiviteter datahenting utvider den samme malklassen, er klassestrukturene, variablene og metodene like.</span><span class="sxs-lookup"><span data-stu-id="02483-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="02483-174">Følgende eksempel viser basisstrukturen når `PurchTable`-tabellen brukes.</span><span class="sxs-lookup"><span data-stu-id="02483-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="02483-175">Når metoden `CopyToDocument` kalles, finnes `this.purchTable`-bufferen allerede.</span><span class="sxs-lookup"><span data-stu-id="02483-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="02483-176">Formålet med denne metoden er å kopiere alle de nødvendige dataene fra `this.purchTable` til `document`-objektet ved å bruke setter-metoden som ble opprettet i `DocumentObject`-klassen.</span><span class="sxs-lookup"><span data-stu-id="02483-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="02483-177">På samme måte finnes det allerede en `this.purchLine`-buffer i `CopyToLine`-metoden.</span><span class="sxs-lookup"><span data-stu-id="02483-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="02483-178">Formålet med denne metoden er å kopiere alle de nødvendige dataene fra `this.purchLine` til `_line`-objektet ved å bruke setter-metoden som ble opprettet i `LineObject`-klassen.</span><span class="sxs-lookup"><span data-stu-id="02483-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="02483-179">Den mest enkle tilnærmingen er å utvide metodene `CopyToDocument` og `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="02483-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="02483-180">Vi anbefaler imidlertid at du prøver `copyToDocumentFromHeaderTable`- og `copyToLineFromLineTable`-metodene først.</span><span class="sxs-lookup"><span data-stu-id="02483-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="02483-181">Hvis de ikke fungerer slik du krever, implementerer du din egen metode og kaller den i `CopyToDocument` og `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="02483-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="02483-182">Det finnes tre vanlige situasjoner der du kan bruke denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="02483-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="02483-183">Det obligatoriske feltet er i `PurchTable` eller `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="02483-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="02483-184">I denne situasjonen kan du utvide `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="02483-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="02483-185">Her er eksempelkoden.</span><span class="sxs-lookup"><span data-stu-id="02483-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="02483-186">De nødvendige dataene er ikke i standardtabellen for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="02483-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="02483-187">Det er imidlertid noen felles relasjoner med standardtabellen, og feltet er obligatorisk på de fleste linjer.</span><span class="sxs-lookup"><span data-stu-id="02483-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="02483-188">I denne situasjonen kan du erstatte `getDocumentQueryObject` eller `getLineObject` spørre i tabellen ved en felles relasjon.</span><span class="sxs-lookup"><span data-stu-id="02483-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="02483-189">I følgende eksempel er **Lever nå**-feltet integrert med salgsordren på linjenivå.</span><span class="sxs-lookup"><span data-stu-id="02483-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="02483-190">I dette eksemplet deklareres en `mcrSalesLineDropShipment`-buffer, og spørringen defineres i `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="02483-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="02483-191">Spørringen bruker relasjonen `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="02483-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="02483-192">Mens du utvider i denne situasjonen, kan du erstatte `getLineQueryObject` med ditt eget konstruerte spørringsobjekt.</span><span class="sxs-lookup"><span data-stu-id="02483-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="02483-193">Vær imidlertid oppmerksom på følgende punkter:</span><span class="sxs-lookup"><span data-stu-id="02483-193">However, note the following points:</span></span>

    * <span data-ttu-id="02483-194">Fordi returverdien for `getLineQueryObject`-metoden er `SysDaQueryObject`, må du konstruere dette objektet ved å bruke SysDa-metoden.</span><span class="sxs-lookup"><span data-stu-id="02483-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="02483-195">Kan ikke fjerne eksisterende tabell.</span><span class="sxs-lookup"><span data-stu-id="02483-195">Can't remove existed table.</span></span>

- <span data-ttu-id="02483-196">De obligatoriske dataene er relatert til transaksjonstabellen av en komplisert koblingsrelasjon, eller relasjonens relasjon relasjon er ikke én til én (1:1), men én til mange (1:N).</span><span class="sxs-lookup"><span data-stu-id="02483-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="02483-197">I denne situasjonen blir ting litt komplisert.</span><span class="sxs-lookup"><span data-stu-id="02483-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="02483-198">Denne situasjonen gjelder for eksemplet med finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="02483-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="02483-199">I slike situasjoner kan du implementere din egen metode for å hente dataene.</span><span class="sxs-lookup"><span data-stu-id="02483-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="02483-200">Her er eksempelkoden i `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-filen.</span><span class="sxs-lookup"><span data-stu-id="02483-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="02483-201">Trinn 3.</span><span class="sxs-lookup"><span data-stu-id="02483-201">Step 3.</span></span> <span data-ttu-id="02483-202">Legge til data i forespørselen</span><span class="sxs-lookup"><span data-stu-id="02483-202">Add data to the request</span></span>

<span data-ttu-id="02483-203">Utvid `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject`- eller `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-metoden for å legge til data i forespørselen.</span><span class="sxs-lookup"><span data-stu-id="02483-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="02483-204">Her er eksempelkoden i `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-filen.</span><span class="sxs-lookup"><span data-stu-id="02483-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="02483-205">I denne koden er `_destination` wrapper-objektet som brukes til å generere posteringsforespørselen, og `_source` er `TaxIntegrationLineObject`-objektet.</span><span class="sxs-lookup"><span data-stu-id="02483-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="02483-206">Definer nøkkelen som brukes i forespørselsskjemaet, som `private const str`.</span><span class="sxs-lookup"><span data-stu-id="02483-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="02483-207">Angi feltet i `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-metoden ved å bruke `SetField`-metoden.</span><span class="sxs-lookup"><span data-stu-id="02483-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="02483-208">Datatypen til den andre parameteren skal være `string`.</span><span class="sxs-lookup"><span data-stu-id="02483-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="02483-209">Hvis datatypen ikke er `string`, må du konvertere den til `string`.</span><span class="sxs-lookup"><span data-stu-id="02483-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="02483-210">Tillegg</span><span class="sxs-lookup"><span data-stu-id="02483-210">Appendix</span></span>

<span data-ttu-id="02483-211">Dette tillegget viser den fullstendige eksempelkoden for integreringen av finansdimensjoner (**Kostsenter** og **Prosjekt**) på linjenivå.</span><span class="sxs-lookup"><span data-stu-id="02483-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="02483-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="02483-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="02483-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="02483-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="02483-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="02483-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
