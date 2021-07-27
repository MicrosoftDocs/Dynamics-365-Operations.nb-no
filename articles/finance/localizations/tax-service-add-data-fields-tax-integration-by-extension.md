---
title: Legge til datafelt i avgiftsintegrering ved hjelp av utvidelser
description: Dette emnet beskriver hvordan du bruker utvidelser i X++ til å legge til datafelt i avgiftsintegrasjonen.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: cdac52ed7f11f796b9559e5454456fb139c6ba00
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346404"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Legg til datafelt i avgiftsintegrering ved hjelp av utvidelser

[!include [banner](../includes/banner.md)]


Dette emnet beskriver hvordan du bruker utvidelser i X++ til å legge til datafelt i avgiftsintegrasjonen. Disse feltene kan utvides til avgiftsdatamodellen for avgiftstjenesten og brukes til å bestemme avgiftskoder. Hvis du vil ha mer informasjon, kan du se [Legge til datafelt i avgiftskonfigurasjoner](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Datamodell

Dataene i datamodellen bæres av objekter og implementeres av klasser.

Her er en liste over de viktigste objektene:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Illustrasjonen nedenfor viser hvordan disse objektene er relatert.

[![Datamodellobjektrelasjon.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Et **Document**-objekt kan inneholde mange **Line**-objekter. Hvert objekt inneholder metadata for avgiftstjenesten.

- `TaxIntegrationDocumentObject` har `originAddress`-metadata, som inneholder informasjon om kildeadressen og `includingTax`-metadata, som angir om linjebeløpet omfatter merverdiavgift.
- `TaxIntegrationLineObject` har `itemId`-, `quantity`- og `categoryId`-metadata.

> [!NOTE]
> `TaxIntegrationLineObject` implementerer også **Charge**-objekter.

## <a name="integration-flow"></a>Integrasjonsflyt

Dataene i flyten blir manipulert av aktiviteter.

### <a name="key-activities"></a>Nøkkelaktiviteter

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Aktiviteter kjøres i følgende rekkefølge:

1. Angi henting
2. Datahenting
3. Beregningstjeneste
4. Valutabytte
5. Dataholdbarhet

Du kan for eksempel utvide **Datahenting** før **Beregningstjeneste**.

#### <a name="data-retrieval-activities"></a>Datahenting-aktiviteter

**Datahenting**-aktiviteter henter data fra databasen. Kort for ulike transaksjoner kan hente data fra ulike transaksjonstabeller:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

I disse **Datahenting**-aktivitetene kopieres data fra databasen til `TaxIntegrationDocumentObject` og `TaxIntegrationLineObject`. Fordi alle disse aktivitetene utvider den samme abstrakte malklassen, har de felles metoder.

#### <a name="calculation-service-activities"></a>Beregningstjeneste-aktiviteter

**Beregningstjeneste**-aktiviteten er koblingen mellom avgiftstjenesten og avgiftsintegreringen. Denne aktiviteten er ansvarlig for følgende funksjoner:

1. Konstruer forespørselen.
2. Poster forespørselen til avgiftstjenesten.
3. Få svar fra avgiftstjenesten.
4. Del opp svaret.

Et datafelt som du legger til i forespørselen, blir postert sammen med andre metadata. 

## <a name="extension-implementation"></a>Utvidelsesimplementering

I denne delen finner du detaljerte trinn som forklarer hvordan du implementerer utvidelsen. Den bruker finansdimensjonene **Kostsenter** og **Prosjekt** som eksempler.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>Trinn 1. Legge til datavariabelen i objektklassen

Objektklassen inneholder datavariabelen og getter/setter-metodene for dataene. Legg til datafeltet i `TaxIntegrationDocumentObject` eller `TaxIntegrationLineObject`, avhengig av nivået til feltet. I eksemplet nedenfor brukes linjenivået, og filnavnet er `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Hvis datafeltet du legger til, er på dokumentnivå, endrer du filnavnet til `TaxIntegrationDocumentObject_Extension.xpp`.

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

**Kostsenter** og **Prosjekt** legges til som private variabler. Opprett getter- og setter-metoder for disse datafeltene for å manipulere dataene.

### <a name="step-2-retrieve-data-from-the-database"></a>Trinn 2. Hente data fra databasen

Angi transaksjonen, og utvid de riktige kortklassene for å hente dataene. Hvis du for eksempel bruker en **Bestilling**-transaksjon, må du utvide `TaxIntegrationPurchTableDataRetrieval` og `TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` arves fra `TaxIntegrationPurchTableDataRetrieval`. Dette bør ikke endres med mindre logikken for `purchTable`- og `purchParmTable`-tabellene er forskjellig.

Hvis datafeltet skal legges til for alle transaksjoner, utvider du alle `DataRetrieval`-klassene.

Fordi alle **Datahenting**-aktiviteter datahenting utvider den samme malklassen, er klassestrukturene, variablene og metodene like.

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

Følgende eksempel viser basisstrukturen når `PurchTable`-tabellen brukes.

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

Når metoden `CopyToDocument` kalles, finnes `this.purchTable`-bufferen allerede. Formålet med denne metoden er å kopiere alle de nødvendige dataene fra `this.purchTable` til `document`-objektet ved å bruke setter-metoden som ble opprettet i `DocumentObject`-klassen.

På samme måte finnes det allerede en `this.purchLine`-buffer i `CopyToLine`-metoden. Formålet med denne metoden er å kopiere alle de nødvendige dataene fra `this.purchLine` til `_line`-objektet ved å bruke setter-metoden som ble opprettet i `LineObject`-klassen.

Den mest enkle tilnærmingen er å utvide metodene `CopyToDocument` og `CopyToLine`. Vi anbefaler imidlertid at du prøver `copyToDocumentFromHeaderTable`- og `copyToLineFromLineTable`-metodene først. Hvis de ikke fungerer slik du krever, implementerer du din egen metode og kaller den i `CopyToDocument` og `CopyToLine`. Det finnes tre vanlige situasjoner der du kan bruke denne fremgangsmåten:

- Det obligatoriske feltet er i `PurchTable` eller `PurchLine`. I denne situasjonen kan du utvide `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable`. Her er eksempelkoden.

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

- De nødvendige dataene er ikke i standardtabellen for transaksjonen. Det er imidlertid noen felles relasjoner med standardtabellen, og feltet er obligatorisk på de fleste linjer. I denne situasjonen kan du erstatte `getDocumentQueryObject` eller `getLineObject` spørre i tabellen ved en felles relasjon. I følgende eksempel er **Lever nå**-feltet integrert med salgsordren på linjenivå.

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

    I dette eksemplet deklareres en `mcrSalesLineDropShipment`-buffer, og spørringen defineres i `getLineQueryObject`. Spørringen bruker relasjonen `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Mens du utvider i denne situasjonen, kan du erstatte `getLineQueryObject` med ditt eget konstruerte spørringsobjekt. Vær imidlertid oppmerksom på følgende punkter:

    * Fordi returverdien for `getLineQueryObject`-metoden er `SysDaQueryObject`, må du konstruere dette objektet ved å bruke SysDa-metoden.
    * Kan ikke fjerne eksisterende tabell.

- De obligatoriske dataene er relatert til transaksjonstabellen av en komplisert koblingsrelasjon, eller relasjonens relasjon relasjon er ikke én til én (1:1), men én til mange (1:N). I denne situasjonen blir ting litt komplisert. Denne situasjonen gjelder for eksemplet med finansdimensjoner. 

    I slike situasjoner kan du implementere din egen metode for å hente dataene. Her er eksempelkoden i `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-filen.

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

### <a name="step-3-add-data-to-the-request"></a>Trinn 3. Legge til data i forespørselen

Utvid `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject`- eller `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-metoden for å legge til data i forespørselen. Her er eksempelkoden i `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-filen.

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

I denne koden er `_destination` wrapper-objektet som brukes til å generere posteringsforespørselen, og `_source` er `TaxIntegrationLineObject`-objektet. 

> [!NOTE]
> * Definer nøkkelen som brukes i forespørselsskjemaet, som `private const str`.
> * Angi feltet i `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine`-metoden ved å bruke `SetField`-metoden. Datatypen til den andre parameteren skal være `string`. Hvis datatypen ikke er `string`, må du konvertere den til `string`.

## <a name="appendix"></a>Tillegg

Dette tillegget viser den fullstendige eksempelkoden for integreringen av finansdimensjoner (**Kostsenter** og **Prosjekt**) på linjenivå.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

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
