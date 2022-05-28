---
title: Importer innkommende forhåndsvarsler for forsendelse via V3-dataenheten
description: Dette emnet beskriver hvordan du kan administrere import av inngående avanserte forsendelsesmerknader (ASN) gjennom den innkommende ASN-dataenheten.
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 44ec0230236451a413d483b3e9f3ddc58b49a0b0
ms.sourcegitcommit: 90ffd763d18f97654b9dbc9e3f71c998e6094c6b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740140"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>Importer innkommende forhåndsvarsler for forsendelse via V3-dataenheten

[!include [banner](../../includes/banner.md)]

ASN-merknader om avanserte forsendelser varsler deg om leverandørleveringer. De kan hjelpe avsenderen med å beskrive forsendelsesinnholdet og tilleggsinformasjon om den, for eksempel varer og emballasje.

ASNer kan hjelpe lagerarbeidere med å få informasjon om hva som ankommer når. Derfor kan de forberede seg. I tillegg kan lagerarbeidere bruke ASN-leveranser til å samsvare detaljene i en forsendelse med den tilknyttede bestillingen som ble opprettet tidligere.

Dette emnet viser en samling scenarier som viser, gjennom eksempler, hvordan du arbeider ASN-filer.

> [!IMPORTANT]
> *Innkommende ASN*-import gjelder bare for varer som er aktivert for avansert lagerstyring (WMS). Før du mottar et ASN-register, må du registrere en bestilling i systemet mot leverandøren som sender ASN.

## <a name="inbound-asn-v3-entity"></a>Innkommende ASN V3-enhet

Du importerer innkommende ASN-er ved hjelp av den sammensatte dataenheten *Innkommende ASN V3*. *Innkommende ASN V3* benytter følgende enheter:

- Topptekst for innkommende last
- Topptekst for innkommende forsendelse
- Pakkestrukturer for innkommende last
- Pakkestrukturkasser for innkommende last
- Linjer for pakkestrukturkasser for innkommende last
- Pakkestrukturlinjer for innkommende last

Den sammensatte dataenheten *Innkommende ASN V3* er beregnet på asynkrone integreringsscenarier der XML-filbaserte importer brukes.

## <a name="xml-format-for-importing-asns"></a>XML-format for import av ASNer

Microsoft Dynamics 365 Supply Chain Management støtter følgende XML-format for import av ASNer. Hver node i XML-filen representerer et attributt fra en individuell enhet.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Eksempler

Følgende underdeler er eksempler på ASN XML-importfiler for leverandørforsendelser.

### <a name="example-1"></a>Eksempel 1

Følgende eksempel viser en XML-fil for import av leverandørforsendelser for én bestilling når ingen kassedetaljer er inkludert.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>Eksempel 2

Følgende eksempel viser en XML-fil for import av leverandørforsendelser for én bestilling når kassedetaljer er inkludert.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>Eksempel 3

Følgende eksempel viser en XML-fil for import av leverandørforsendelser for flere bestillinger når kassedetaljer er inkludert.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>Kontrollere resultatene av å importere en ASN-fil

Følg denne fremgangsmåten for å kontrollere resultatene av import av en ASN-fil.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Finn og åpne en belastning som ble opprettet som del av en ASN-import.
1. I hurtigfanen **Last** skal du se verdier som er basert på XML-filen.
1. I hurtigfanen **Lastlinjer** skal du se bestillingsnumre og varedetaljer som er basert på XML-filen.
1. I hurtigruten i fanen **Send og motta** i gruppen **Motta** velger du **Pakkestruktur** for å vise pakkestrukturen til en last.
1. I hurtigfanen **Paller** skal du se nummerskilt som er basert på XML-filen.
1. I hurtigfanen **Saker** skal du se saker som er basert på XML-filen.
1. I hurtigfanen **Varer** skal du se varer og antall som er basert på XML-filen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
