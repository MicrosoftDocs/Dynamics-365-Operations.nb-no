---
title: Feil feltverdi i TaxTrans
description: Denne artikkelen gir informasjon om feilsøking av feil feltverdier i TaxTrans.
author: EricWangChen
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6e7329ffdc04207116c92cb42e02750b176713fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899821"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Feil feltverdi i TaxTrans

[!include [banner](../includes/banner.md)]

Hvis en feltverdi i **TaxTrans** er feil, bruker du informasjonen i denne artikkelen til å forsøke å løse problemet.

## <a name="overview-of-values"></a>Oversikt over verdier
Listen nedenfor viser hvordan **TaxTrans**, **TaxUncommitted** og **TmpTaxWorkTrans** er lignende datasett, men fungerer annerledes.

  - **TaxTrans** er det siste posterte mva-transaksjonsresultatet som fastholdes i databasen.
  - **TaxUncommitted** er resultatet av midlertidig beregnet avgift som fastholdes i databasen (om nødvendig), som senere vil bli brukt til postering.
  - **TmpTaxWorkTrans** er resultatet av midlertidig beregnet avgift i minnetabellen (tabelltype = InMemory).

Hvis du finner rotårsaken til en feil **TaxTrans**-kolonne, har du også funnet rotårsaken til en feil **TaxUncommitted**- eller **TmpTaxWorkTrans**-kolonne. Det er fordi de tre kolonnene kopieres fra hverandre.

Vanligvis genereres **TmpTaxWorkTrans** under avgiftsberegning, og hvis det er aktuelt, genereres **TaxUncommitted**. Under avgiftspostering genereres **TaxTrans**.


## <a name="add-breakpoints"></a>Legge til stoppunkt
Fullfør fremgangsmåten nedenfor for legge til stoppunkt: 

1. Legg til utvidelser og stoppunkt i *insert()* og *update()* i tilleggene som vist nedenfor.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Du kan også legge til stoppunkt direkte når **TaxUncommitted** ikke er inkludert.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Reprodusere og feilsøke

Når stoppunktene er angitt, vises alle endringer i data ved feilsøking. Hvis du vil finne rotårsaken til feil kolonne i **TaxTrans**, **TaxUncommitted** eller **TmpTaxWorkTrans**, kan du se gjennom og legge merke til følgende elementer:

- Det siste stoppunktet der kolonnen er riktig.
- Det første stoppunktet der kolonnen er uriktig.
- Hva som skjer mellom disse to punktene.

## <a name="determine-whether-customization-exists"></a>Fastslå om det finnes tilpasning
Hvis du har fullført trinnene i de forrige delene, men ikke kunne løse problemet, må du avgjøre om det finnes tilpasning. Hvis det ikke finnes noen tilpasning, kan du kontakte Microsoft Kundestøtte for hjelp.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

