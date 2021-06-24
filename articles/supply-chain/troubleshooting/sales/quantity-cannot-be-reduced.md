---
title: Antallet kan ikke reduseres når en salgsordre annulleres
description: Antallet kan ikke reduseres når en salgsordre annulleres.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230842"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Antallet kan ikke reduseres når en salgsordre annulleres

Feilkode: SYS138831

## <a name="symptoms"></a>Symptomer

Systemet viser følgende feilmelding:

> Antallet kan ikke reduseres. Antall lagertransaksjoner i ordre er for lavt fordi en utleveringsordre eller produksjonsordre refererer til antallet eller delen av den, eller fordi antallet eller delen av den er merket mot andre transaksjoner.

## <a name="cause"></a>Årsak

Hvis arbeid er knyttet til en salgsordre, kan du ikke annullere salgsordren før arbeidet er annullert og tilbakeført. Dette kravet gjelder selv om arbeidet som er knyttet til salgsordren, er lukket.

## <a name="resolution"></a>Løsning

Du kan løse dette problemet ved å fullføre følgende oppgaver:

1. Avbryt åpent arbeid.
1. Slett belastningen.
1. Reduser det plukkede antallet.

### <a name="cancel-open-work"></a>Avbryte åpent arbeid

Følg denne fremgangsmåten for å avbryte åpent arbeid.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.
1. I **Arbeids-ID**-feltet angir du IDen for arbeidet du vil avbryte, og som for øyeblikket har **Arbeidstatus**-verdien *Åpen*, *Pågår*, *Avbrutt*, *Kombinert* eller *Lukket*.
1. Velg **OK**.
1. Velg **Ja** for å bekrefte at du vil avbryte arbeidet.

### <a name="delete-the-load"></a>Slette belastningen

Følg denne fremgangsmåten for å slette en belastning.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Åpne den relevante salgsordren.
1. Velg **Lager \> Arbeidsdetaljer** i hurtigfanen **Salgsordrelinjer**.
1. Velg **Avbryt arbeid** i **Arbeid**-gruppen i **Arbeid**-fanen i handlingsruten på **Arbeid**-siden.
1. Bekreft at **Arbeidsstatus**-feltet er satt til *Avbrutt*.
1. Lukk **Arbeid**-siden.
1. Velg **Lager \> Lastdetaljer** i hurtigfanen **Salgsordrelinjer** på siden for salgsordredetaljer.
1. Velg deretter **Slett** i handlingsruten.
1. Velg **Ja** for å bekrefte at du vil slette belastningen.
1. Lukk **Belastning**-siden.

### <a name="reduce-the-picked-quantity"></a>Redusere det plukkede antallet

Etter at alt arbeid er avbrutt, følger du fremgangsmåten nedenfor for å redusere det plukkede antallet.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Åpne den relevante salgsordren.
1. Velg **Oppdater linje \> Plukk** på verktøylinjen i hurtigfanen **Salgsordrelinjer**.
1. Velg linjen der **Avgangsstatus**-feltet er satt til *Plukket* i **Transaksjoner**-delen på **Plukk**-siden.
1. Velg **Legg til plukklinje** på verktøylinjen i **Transaksjoner**-delen.
1. Velg **Bekreft plukking av alle** på verktøylinjen i **Plukklinjer**-delen.
1. Lukk **Plukk**-siden.
1. Velg **Avbryt** i **Vedlikehold**-gruppen i **Salgsordre**-fanen i handlingsruten på siden for salgsordredetaljer.
1. Velg **Ja** for å bekrefte at du vil avbryte salgsordren.
