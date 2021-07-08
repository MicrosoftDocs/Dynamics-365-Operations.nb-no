---
title: Importere innkommende ASN-er via V2-dataenheten
description: Dette emnet beskriver hvordan du kan administrere import av inngående avanserte forsendelsesmerknader (ASN) gjennom den innkommende ASN V2-dataenheten.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249147"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="b6826-103">Importere innkommende ASN-er via V2-dataenheten</span><span class="sxs-lookup"><span data-stu-id="b6826-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6826-104">ASN-merknader om avanserte forsendelser varsler deg om leverandørleveringer.</span><span class="sxs-lookup"><span data-stu-id="b6826-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="b6826-105">De kan hjelpe avsenderen med å beskrive forsendelsesinnholdet og tilleggsinformasjon om den, for eksempel varer og emballasje.</span><span class="sxs-lookup"><span data-stu-id="b6826-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="b6826-106">ASNer kan hjelpe lagerarbeidere med å få informasjon om hva som ankommer når.</span><span class="sxs-lookup"><span data-stu-id="b6826-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="b6826-107">Derfor kan de forberede seg.</span><span class="sxs-lookup"><span data-stu-id="b6826-107">Therefore, they can prepare.</span></span> <span data-ttu-id="b6826-108">I tillegg kan lagerarbeidere bruke ASN-leveranser til å samsvare detaljene i en forsendelse med den tilknyttede bestillingen som ble opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="b6826-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="b6826-109">Dette emnet viser en samling scenarier som viser, gjennom eksempler, hvordan du arbeider ASN-filer.</span><span class="sxs-lookup"><span data-stu-id="b6826-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6826-110">*Innkommende ASN*-import gjelder bare for varer som er aktivert for avansert lagerstyring (WMS).</span><span class="sxs-lookup"><span data-stu-id="b6826-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="b6826-111">Før du mottar et ASN-register, må du registrere en bestilling i systemet mot leverandøren som sender ASN.</span><span class="sxs-lookup"><span data-stu-id="b6826-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="b6826-112">Innkommende ASN V2-enhet</span><span class="sxs-lookup"><span data-stu-id="b6826-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="b6826-113">Du importerer innkommende ASN-er ved hjelp av den sammensatte dataenheten *Innkommende ASN V2*.</span><span class="sxs-lookup"><span data-stu-id="b6826-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="b6826-114">*Innkommende ASN V2* benytter følgende enheter:</span><span class="sxs-lookup"><span data-stu-id="b6826-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="b6826-115">Topptekst for innkommende last</span><span class="sxs-lookup"><span data-stu-id="b6826-115">Inbound load header</span></span>
- <span data-ttu-id="b6826-116">Topptekst for innkommende forsendelse</span><span class="sxs-lookup"><span data-stu-id="b6826-116">Inbound shipment header</span></span>
- <span data-ttu-id="b6826-117">Pakkestrukturer for innkommende last</span><span class="sxs-lookup"><span data-stu-id="b6826-117">Inbound load packing structures</span></span>
- <span data-ttu-id="b6826-118">Pakkestrukturkasser for innkommende last</span><span class="sxs-lookup"><span data-stu-id="b6826-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="b6826-119">Linjer for pakkestrukturkasser for innkommende last</span><span class="sxs-lookup"><span data-stu-id="b6826-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="b6826-120">Pakkestrukturlinjer for innkommende last</span><span class="sxs-lookup"><span data-stu-id="b6826-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="b6826-121">Den sammensatte dataenheten *Innkommende ASN V2* er beregnet på asynkrone integreringsscenarier der XML-filbaserte importer brukes.</span><span class="sxs-lookup"><span data-stu-id="b6826-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="b6826-122">XML-format for import av ASNer</span><span class="sxs-lookup"><span data-stu-id="b6826-122">XML format for importing ASNs</span></span>

<span data-ttu-id="b6826-123">Microsoft Dynamics 365 Supply Chain Management støtter følgende XML-format for import av ASNer.</span><span class="sxs-lookup"><span data-stu-id="b6826-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="b6826-124">Hver node i XML-filen representerer et attributt fra en individuell enhet.</span><span class="sxs-lookup"><span data-stu-id="b6826-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="b6826-125">Eksempler</span><span class="sxs-lookup"><span data-stu-id="b6826-125">Examples</span></span>

<span data-ttu-id="b6826-126">Følgende underdeler er eksempler på ASN XML-importfiler for leverandørforsendelser.</span><span class="sxs-lookup"><span data-stu-id="b6826-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="b6826-127">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b6826-127">Example 1</span></span>

<span data-ttu-id="b6826-128">Følgende eksempel viser en XML-fil for import av leverandørforsendelser for én bestilling når ingen kassedetaljer er inkludert.</span><span class="sxs-lookup"><span data-stu-id="b6826-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="b6826-129">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b6826-129">Example 2</span></span>

<span data-ttu-id="b6826-130">Følgende eksempel viser en XML-fil for import av leverandørforsendelser for én bestilling når kassedetaljer er inkludert.</span><span class="sxs-lookup"><span data-stu-id="b6826-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="b6826-131">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="b6826-131">Example 3</span></span>

<span data-ttu-id="b6826-132">Følgende eksempel viser en XML-fil for import av leverandørforsendelser for flere bestillinger når kassedetaljer er inkludert.</span><span class="sxs-lookup"><span data-stu-id="b6826-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="b6826-133">Kontrollere resultatene av å importere en ASN-fil</span><span class="sxs-lookup"><span data-stu-id="b6826-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="b6826-134">Følg denne fremgangsmåten for å kontrollere resultatene av import av en ASN-fil.</span><span class="sxs-lookup"><span data-stu-id="b6826-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="b6826-135">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="b6826-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b6826-136">Finn og åpne en belastning som ble opprettet som del av en ASN-import.</span><span class="sxs-lookup"><span data-stu-id="b6826-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="b6826-137">I hurtigfanen **Last** skal du se verdier som er basert på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b6826-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="b6826-138">I hurtigfanen **Lastlinjer** skal du se bestillingsnumre og varedetaljer som er basert på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b6826-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="b6826-139">I hurtigruten i fanen **Send og motta** i gruppen **Motta** velger du **Pakkestruktur** for å vise pakkestrukturen til en last.</span><span class="sxs-lookup"><span data-stu-id="b6826-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="b6826-140">I hurtigfanen **Paller** skal du se nummerskilt som er basert på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b6826-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="b6826-141">I hurtigfanen **Saker** skal du se saker som er basert på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b6826-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="b6826-142">I hurtigfanen **Varer** skal du se varer og antall som er basert på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b6826-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
