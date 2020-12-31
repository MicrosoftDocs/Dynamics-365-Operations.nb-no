---
title: Justere leieavtaler
description: Emnet beskriver hvordan du justerer en leieavtale. Det kan hende at justering kreves hvis leievilkårene endres, leieavtalen utvides eller andre omstendigheter endres.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446608"
---
# <a name="adjust-leases"></a>Justere leieavtaler

[!include [banner](../includes/banner.md)]

Emnet beskriver hvordan du justerer en leieavtale. Det kan hende at justering kreves hvis leievilkårene endres, leieavtalen utvides eller andre omstendigheter endres. Aktivaleie følger retningslinjene som Accounting Standards Codification-emne 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16) gir om leieavtaleendringer. ASC 842-20-15-1 definerer en leieavtaleendring som enhver endring i vilkårene og betingelsene for en kontrakt som forårsaker endring i omfanget av, eller betalingen for, en leieavtale. Avsnitt 39 i IFRS 16 angir at en leier må revaluere leieforpliktelsen, slik at den gjenspeiler endringer i leiebetalingene.

Når det gjelder organisasjoner som følger ASC 842 eller IFRS 16, måles en leieavtale på nytt for å gjenspeile en endring i den gjeldende verdien til de fremtidige minimumsleiebetalingene (PVFMLP). Hvis PVFMLP øker, blir journaloppføringen som opprettes en debitering for bruksrettseiendelen og en kreditering for leieforpliktelsen for differansen mellom den nye PVFMLP og den forrige PVFMLP. Hvis PVFMLP reduseres, blir journaloppføringen være en debitering for leieforpliktelsen og en kreditering for bruksrettseiendelen for differansen.

Hvis justeringen reduserer bruksrettseiendelen forbi 0 (null), blir resten kreditert fortjenesten på posteringskontoen for leieavtaleendringer som er angitt på siden **Posteringskontoer for leieavtale**. Systemet gjør rede for disse transaksjonene og andre justeringsoppføringer, for eksempel klassifiseringsendringer, opprinnelige direkte kostnader, leieinsentiver, forskuddsbetalinger og avviklingskostnader som oppstår fra leieavtaleendringer.

Hvis du vil ha spesifikk veiledning om leiejusteringstransaksjoner, anbefaler vi at du ser på IFRS 16 og ASC 842.

Du justerer en leieavtale ved å følge denne fremgangsmåten. De endrede dataene oppdaterer leieplaner etter at prosessen Opprett plan har kjørt.

1. Gå til **Aktivaleie \> Leieavtaler \> Leiesammendrag**.
2. På siden **Leiesammendrag** velger du leieavtalen du vil justere, og deretter velger du **Juster leieavtale**.
3. På siden **Juster leieavtale** angir du den nye informasjonen for den justerte leieavtalen.

    Legg merke til at siden **Juster leieavtale** ligner på siden **Legg til leieavtale**. Slik som startdatoen du angir når du legger til en leieavtale, fastsetter når den nye leieavtalen starter, fastsetter feltet **Endringsdato** på siden **Juster leieavtale** når den endrede leieavtalen starter. Denne datoen kan ikke komme etter startdatoen på betalingsplanlinjene.

    > [!NOTE]
    > Feltene **Bruksrettsvurderinger** brukes på leiejusteringen. Hvis ingen opprinnelige direkte kostnader, leieinsentiver, forskuddsbetalinger eller avviklingskostnader er knyttet til den endrede leieavtalen, lar du disse feltene stå tomme. De opprinnelige beløpene gjelder ikke for den oppdaterte leieavtalen. Eventuelle tilleggskostnader som påløper når leieavtalen endres, må angis på siden **Juster leieavtale**.
    > 
    > En utleier gir for eksempel et insentiv på USD 1 000 for å godta en forlengelse av leieavtalen. I dette tilfellet angir du **1 000** i feltet **Leieinsentiver** når du justerer leieavtalen for å gjøre rede for forlengelsen. Hvis ingen insentiver er knyttet til leiejusteringen, bør du fjerne alle verdier som tidligere var angitt i dette feltet. Den samme logikken brukes på andre bruksrettsvurderinger.

    Betalingsplanlinjene for den justerte leieavtalen bør opprettes på en fremtidsgjeldende basis. Betalingsplanlinjer som opprettes på en fremtidsgjeldende basis, kan ikke starte før leieavtaleendringene trer i kraft.

    Fremgangsmåten nedenfor er nesten identisk med fremgangsmåten for opprinnelig føring av en leieavtale.

4. Velg **Opprett tidsplaner** for å generere den justerte betalingsplanen. Du får en melding om at betalingsplanen er opprettet for leieavtalen.

    > [!IMPORTANT]
    > Før du velger **Opprett tidsplaner**, må du kontrollere at endringsdatoen og betalingsplanlinjene er nøyaktige. Kontroller også at alle opprinnelige direkte kostnader, leieinsentiver, forskuddsbetalinger eller avviklingskostnader bare svarer til de kostnadene som oppstår fra justeringen.

5. Hvis du vil vise den nylig opprettede betalingsplanen, velger du **Tablåer** og åpner siden **Betalingsplan**.
6. På siden **Betalingsplan** kan du redigere de justerte betalingsbeløpene før du bekrefter betalingsplanen. Du bekrefter tidsplanen ved å velge **Bekreft tidsplan**.

    Når betalingsplanen er bekreftet, opprettes de nye tidsplanene for avskrivning av aktiva og leieforpliktelse.

7. Hvis du vil vise den nye nedbetalingsplanen for leieforpliktelse som genereres fra de nye inndataene, lukker du **Betalingsplan**-siden og åpner siden **Nedbetalingsplan for gjeld**.
8. Hvis du vil vise den nylig genererte avskrivningsplanen for aktiva, åpner du siden **Avskrivningsplan for aktiva** fra siden **Tablådetaljer**.
9. Hvis du vil generere en journaloppføring for justering, velger du **Funksjon \> Leiejustering**. Du får en melding om at journaloppføringen for justering er opprettet. 
10. Du viser journaloppføringen ved å velge **Journaler \> Journal for aktivaleie**.
11. Hvis du vil postere en journaloppføring, velger du linjen og deretter **Poster**.

## <a name="view-lease-versions"></a>Vise leieavtaleversjoner

Hvis en leieavtale er endret, kan du vise de ulike versjonene av den. Du kan også vise de historiske tidsplanene og tidligere leieavtaledetaljer.

1. På siden **Leiesammendrag** velger du leieavtalen, og deretter velger du **Historikk for leieavtaleversjon** i handlingsruten.

    Hvis den valgte leieavtalen er justert, viser siden **Historikk for leieavtaleversjon** de ulike versjonene av den. Den opprinnelige leieavtalen er merket med **1**, og påfølgende versjoner er i stigende numerisk rekkefølge.

    For en valgt leieavtaleversjon kan du vise finansdimensjoner, kontraktdetaljer, sted og betalingsplanlinjer.

2. Hvis du vil vise historiske tidsplaner, åpner du den endrede leieavtalen fra siden **Leiesammendrag**, velger det ønskede tablået og deretter **Historikk for tablåversjon** i handlingsruten.
3. På **Tablåversjon**-siden velger du ønsket versjon og ønsket tidsplan du vil vise.
