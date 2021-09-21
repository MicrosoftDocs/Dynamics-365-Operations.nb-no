---
title: Innstillingen Postere i belastningskonto i finans er ikke aktivert
description: Dette problemet oppstår når en bestilling faktureres hvis alternativet "Postere i belastningskonto i finans" er aktivert i fanen "Faktura" på siden "Leverandørparametere"
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477220"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Innstillingen Postere i belastningskonto i finans er ikke aktivert

## <a name="symptoms"></a>Symptomer

Dette problemet oppstår når en bestilling faktureres hvis alternativet **Postere i belastningskonto i finans** er satt til *Ja* i fanen **Faktura** på siden **Leverandørparametere**.

## <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. Gå til **Leverandører \> Oppsett \> Leverandørparametere**.
1. I fanen **Faktura** setter du alternativet **Postere i belastningskonto i finans** til *Ja*.
1. Gå til **Lagerstyring \> Oppsett \> Postering \> Postering**.
1. I fanen **Bestilling** må du kontrollere at du har slettet alle linjene i innkjøpsutgiften for produktet.
1. Gå til **Leverandører \> Bestillinger \> Alle bestillinger**.
1. Opprett en bestilling. I feltet **Leverandørkonto** velger du *1001 Acme-kontorutstyr*.
1. Legg til en bestillingslinje som har følgende innstillinger:

    - **Varenummer:** *D0011 laserprojektor*
    - **Område:** *1*
    - **Lager:** *11*
    - **Antall:** *4*

1. I handlingsruten i fanen **Bestilling** i gruppen **Handling** velger du **Bekreft**.
1. I handlingsruten i fanen **Motta** i gruppen **Generer** velger du **Produktkvittering**.
1. I dialogboksen **Poster mottaksseddel**, i feltet **Produktkvittering**, angir du et vilkårlig nummer og velger **OK**.
1. I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.
1. I **Nummer**-feltet angir du et tilfeldig nummer som fakturanummeret.
1. Oppdater samsvarsstatusen, og poster.
1. Legg merke til at du nå får følgende feilmelding når du genererer en faktura fra en bestilling: "Kontonummeret for transaksjonstypen Innkjøpsutgift for produkt finnes ikke".

## <a name="resolution"></a>Løsning

Dette avhenger av parameterinnstillingene for fakturaer og fakturagrupper. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Regnskap for innkjøpstillegg og lageravvik](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
