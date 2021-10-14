---
title: Opprette og fakturere en konsernintern bestilling til intern bruk
description: Dette emnet forklarer hvordan du oppretter og fakturerer en konsernintern bestilling til intern bruk
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 88a14ff962c5cf0cd1cff24b16cc7a62e9e1c8ce
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548446"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Opprette og fakturere en konsernintern bestilling til intern bruk

[!include [banner](../../includes/banner.md)]

Du kan opprette en konsernintern bestilling for en konsernintern leverandør. Dette oppretter automatisk en konsernintern salgsordre hos den konserninterne leverandøren.

![Konsernintern intern innkjøpsprosess](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Oprette en konsernintern bestilling og en tilsvarende konsernintern salgsordre

Gjør følgende i juridisk enhet AAA, som vist i illustrasjonen.

1. Velg **Leverandører** \> **Bestillinger** \> **Alle bestillinger**.
1. På listesiden **Alle bestillinger** oppretter du en bestilling for en konsernintern leverandør. Feltverdiene kopieres fra leverandørkontoen til bestillingen.

    Siden du arbeider med en konsernintern leverandør, opprettes en konsernintern salgsordre i den juridiske enheten som svarer til leverandøren. Nummeret på den konserninterne salgsordren kan være den samme som nummeret på konserninterne bestillingen, og det kan inneholde IDen for den juridiske enheten. Nummerstrukturen som brukes, avhenger av valget i feltet **Salgsordrenummerering** på **Konsernintern**-siden. Hvis du oppretter bestilling 00029\_064 i juridisk enhet AAA, er for eksempel salgsordrenummeret i juridisk enhet BBB, AAA00029\_64.

    En informasjonsmelding forteller deg at det er opprettet en konsernintern bestilling og konsernintern salgsordre. Meldingen inneholder det konserninterne salgsordrenummeret, til informasjon.

1. Legg til linjevarer i bestillingen. Tilsvarende linjeelementene legges automatisk til den konserninterne salgsordren. Hvis en vare ikke finnes i den andre juridiske enheten, vises en melding, og du kan ikke legge til varen i bestillingen. Hvis du vil løse dette problemet, bytter du til den juridiske enheten og frigir produkt til den juridiske enheten. Varen vil være tilgjengelig for å bli lagt til i salgsordrer i den juridiske enheten. Deretter bytter du tilbake til den juridiske enheten for bestillingen, og fortsetter med å legge til linjeelementer.
1. Når du er ferdig med å angi informasjon for bestillingen, bekrefter du den.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Behandle den konserninterne følgeseddelen og kundefakturaen

Gjør følgende i juridisk enhet BBB, som vist i illustrasjonen.

1. Gå til **Kunde \> Salgsordrer \> Alle salgsordrer**.
1. På listesiden **Alle salgsordrer** velger du den konserninterne salgsordren.
1. Velg kategorien **Plukk og pakk** i handlingsruten, og velg deretter **Følgeseddel**.
1. Merk av i **Postering**-avmerkingsboksen.
1. Velg **OK**. Følgeseddelen posteres i den juridiske enheten BBB.
1. På listesiden **Alle salgsordrer** velger du den konserninterne salgsordren.
1. Velg kategorien **Faktura** i handlingsruten, og velg deretter **Faktura**.
1. Merk av i **Postering**-avmerkingsboksen.
1. Velg **OK**.

    Kundefakturaen for den konserninterne salgsordren posteres i den juridiske enheten BBB.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Behandle den konserninterne produktkvitteringen og leverandørfakturaen

Gjør følgende i juridisk enhet AAA, som vist i illustrasjonen.

1. Gå til **Leverandører \> Bestillinger \> Alle bestillinger**.
1. På listesiden **Alle bestillinger** velger du den konserninterne bestillingen.
1. Velg kategorien **Motta** i handlingsruten, og velg deretter **Produktkvittering**. Produktkvitteringen opprettes. Produktkvitteringsnummeret er det samme som det konserninterne følgeseddelnummeret.
1. Merk av i **Postering**-avmerkingsboksen.
1. Velg **OK**.
1. På listesiden **Alle bestillinger** velger du den konserninterne bestillingen.
1. I handlingsvinduet velger du **Faktura**, og velger deretter **Faktura**. Leverandørfakturaen opprettes. Leverandørens fakturanummer er lik det konserninterne kundefakturanummeret.
1. Gjør deg ferdig med å registrere leverandørfakturaen, og deretter publiserer du den.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
