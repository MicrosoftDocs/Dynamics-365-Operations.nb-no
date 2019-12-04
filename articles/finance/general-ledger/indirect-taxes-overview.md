---
title: Oversikt over merverdiavgift
description: Dette emnet inneholder en oversikt over avgiftssystemet. Den beskriver elementene i mva-oppsettet, og hvordan de fungerer sammen.
author: ShylaThompson
manager: AnnBe
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16a67ef625fdde0755e96c959be1fb2989ca53b6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770672"
---
# <a name="sales-tax-overview"></a>Oversikt over merverdiavgift

[!include [banner](../includes/banner.md)]

Dette emnet inneholder en oversikt over avgiftssystemet. Den beskriver elementene i mva-oppsettet, og hvordan de fungerer sammen.

<a name="overview"></a>Oversikt
--------

Merverdiavgiftsrammeverket støtter mange typer indirekte avgifter, blant annet skatter, merverdiavgift (mva), mva for varer og tjenester (GST), enhetsbaserte gebyrer og kildeskatt. Disse avgiftene beregnes og dokumenteres under transaksjoner for innkjøp og salg. De må regelmessig rapporteres og betales til skattemyndighetene. 

Diagrammet nedenfor viser enhetene for mva-oppsett og hvordan de er relatert.

[![Diagram som viser oversikt over avgiftsoppsettsenheter](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

For hver type merverdiavgift som et firma må ta hensyn til, må en mva-kode defineres. En mva-kode inneholder mva-satser og beregningsreglene for merverdiavgiften. 

Hver mva-kode må være koblet til en mva-utligningsperiode. Mva-utligningsperioder definerer intervallene for rapportering og betaling av merverdiavgifter til skattemyndighetene. Hver mva-utligningsperiode må tilordnes en skattemyndighet. En skattemyndighet representerer enheten som merverdiavgift rapporteres og betales til. Den definerer også oppsettet for mva-rapporten. Skattemyndighetene kan være relatert til leverandørkontoer. Hvis du vil ha mer informasjon, kan du se [Definere mva-utligningsperioder](tasks/set-up-sales-tax-settlement-periods.md).

Hver mva-kode må også være koblet til en finansposteringsgruppe. En finansposteringsgruppe angir hovedkontoene som beløpene for mva-kodene skal posteres til. 

Du kan også definere valgfrie mva-rapporteringskoder. Disse kan tilordnes på mva-koder for de ulike beløpstypene som beregnes for mva-koden. **Mva-betaling etter rapporteringskode**-rapporten viser totaler per mva-rapporteringskode for en gitt mva-utligningsperiode og intervall. 

Hver transaksjon som merverdiavgift må beregnes og posteres for, må ha en mva-gruppe og en mva-gruppe for vare. Mva-grupper er knyttet til parten (for eksempel kunde eller leverandør) i transaksjonen, mens mva-grupper for varer er knyttet til ressursen (for eksempel vare- eller innkjøpskategori) for transaksjonen. Mva-grupper inneholder en liste over avgiftskoder. Avgiftskodene som finnes i både mva-gruppen og mva-gruppen for vare for en transaksjon, er mva-koden som gjelder for transaksjonen. 

Tabellen nedenfor beskriver enhetene og rekkefølgen for mva-oppsettet.

| Oppsettaktivitet                                                  | Nødvendig/valgfritt og beskrivelse                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opprett hovedkontoer.                                           | Obligatorisk. Du må opprette hovedkontoene firmaet bruker til å betale og registrere avgifter, før du kan sette opp mva-funksjonaliteten.                                                                                                                                                                             |
| Konfigurer finansposteringsgrupper for merverdiavgift.                     | Obligatorisk. Finansposteringsgrupper definererer hovedkontoene for registrering og betaling av merverdiavgift.   Hvis du vil ha mer informasjon, kan du se [Definere finansposteringsgrupper for merverdiavgift](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Konfigurer skattemyndigheter.                                   | Obligatorisk. Skattemyndighetene er enhetene som mva må rapporteres og betales til.    Hvis du vil ha mer informasjon, kan du se [Definere skattemyndigheter](tasks/set-up-sales-tax-authorities.md).                                                                                                                                          |
| Definer mva-utligningsperioder.                            | Obligatorisk. Mva-utligningsperiodene inneholder informasjon om når og hvor ofte merverdiavgift må rapporteres og betales. De er relatert til skattemyndighetene.                                                                                                                                                       |
| Definer koder for mva-rapportering.                               | Valgfritt. Mva-rapporteringskoder kan tilordnes mva-koder for å rapportere beløp for flere mva-koder i én mva-rapporteringskode. Hvis du vil ha mer informasjon, kan du se [Definere mva-rapporteringskoder](tasks/set-up-sales-tax-reporting-codes.md).                                         |
| Definer mva-koder.                                         | Obligatorisk. Mva-koder inneholder mva-satsene og beregningsreglene for hver merverdiavgift. Mva-koder er relatert til en utligningsperiode for merverdiavgift og en finansposteringsgruppe. Hvis du vil ha mer informasjon, kan du se [Definere mva-koder](tasks/set-up-sales-tax-codes.md).                                |
| Definer mva-grupper.                                        | Obligatorisk. Mva-grupper inneholder en liste over salgskoder som gjelder for parten (kunden eller leverandøren) i en transaksjon. For en gitt transaksjon fastsetter skjæringspunktet for mva-koder i mva-gruppen og mva-gruppen for vare mva-kodene som gjelder for transaksjonen.                  |
| Definere mva-grupper for vare.                                   | Obligatorisk. Mva-gruppen for vare inneholder en liste over salgskoder som gjelder for ressursen (produkt, tjeneste og så videre) for en transaksjon. For en gitt transaksjon fastsetter skjæringspunktet for mva-koder i mva-gruppen og mva-gruppen for vare mva-kodene som gjelder for transaksjonen. Hvis du vil ha mer informasjon, se [Definere mva-grupper og mva-grupper for vare](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Definer mva-parametere på programparametersidene. | Obligatorisk. Ulike områder, for eksempel Økonomimodul, Kunde og Leverandør, må sette opp parametere for korrekt beregning av indirekte avgifter. Selv om de fleste av disse parameterne har standardverdier, må de endres for å tilpasses kravene i hvert enkelt firma.                                          |

## <a name="sales-tax-on-transactions"></a>Merverdiavgift på transaksjoner
På hver transaksjon (salg/kjøp-dokumentlinjer, journaler og så videre), må du angi en mva-gruppe og en mva-gruppe for vare for å beregne merverdiavgift. Standardgrupper angis i hoveddata (for eksempel kunde, leverandør, vare og innkjøpskategori), men du kan endre gruppene i en transaksjon manuelt om nødvendig. Begge gruppene inneholder en liste over mva-koder, og skjæringspunktet mellom de to listene med mva-koder bestemmer listen over aktuelle mva-koder for transaksjonen. 

For hver transaksjon kan du slå opp den beregnede merverdiavgiften ved å åpne **Mva-transaksjon**-siden. Du kan slå opp merverdiavgiften for en dokumentlinje eller for hele dokumentet. Du kan justere den beregnede merverdiavgiften for bestemte dokumenter (for eksempel leverandørfaktura og økonomijournaler) hvis det opprinnelige dokumentet viser beløp som er avvikende.

## <a name="sales-tax-settlement-and-reporting"></a>Mva-utligning og -rapportering
Merverdiavgift må rapporteres og betales til skattemyndighetene i regulerte intervaller (månedlig, kvartalsvis og så videre). Du kan utligne avgiftskontoer for intervallet og forskyve saldoene til mva-oppgjørskontoen, som angitt i finansposteringsgruppene. Du får tilgang til denne funksjonaliteten på siden **Utlign og poster merverdiavgift**. Du må angi mva-utligningsperioden som merverdiavgiften skal utlignes for. 

Etter at merverdiavgiften er betalt skal saldoen på mva-oppgjørskontoen balanseres mot bankkontoen. Hvis skattemyndigheten som er angitt for utligningsperioden for merverdiavgift, er knyttet til en leverandørkonto, posteres mva-saldoen som en åpen leverandørfaktura og kan inkluderes i det vanlige betalingsforslaget.

## <a name="conditional-sales-tax"></a>Betinget mva.
Betinget merverdiavgift er en merverdiavgift som betales proporsjonalt til det faktiske beløpet som betales på en faktura. Standard merverdiavgift beregnes derimot på faktureringstidspunktet. Betinget merverdiavgift må betales til skattemyndighetene ved betalingsposteringen, og ikke ved fakturapostering. Når fakturaen posteres, må transaksjonen rapporteres i sales tax book-rapporten. Transaksjonen må imidlertid utelates fra mva-betalingsrapporten. 

Hvis du merker av for Betinget mva. i parameterskjemaet for økonomimodulen, kan ingen merverdiavgift trekkes fra før du har betalt fakturaen. Dette er et lovefestet krav i noen land/områder.

> [!NOTE]
> Når du merker av for Betinget mva., må du definere mva-koder og mva-grupper og opprette finansposteringsgrupper for å støtte funksjonen. |

###  <a name="example"></a>Eksempel

Du utligner merverdiavgift hver måned. Den 15. juni oppretter du en kundefaktura på EUR 10 000 pluss mva.
-   Mva er 25 prosent eller 2 500.
-   Fakturabetalingen forfaller 30. juli.

Vanligvis ville du måtte utligne og betale 2 500 til skattemyndighetene når fakturaen er postert i juni, selv om du ikke har mottatt betalingen fra kunden. 

Hvis du bruker en betinget mva, utligner du imidlertid med skattemyndighetene når du mottar betaling fra kunden den 30. juli.

### <a name="postdated-check"></a>Etterdatert sjekk

Hvis du bruker etterdatert sjekk som betalingsmåte når betalingen opprettes, blir ikke bankkontoen tømt. I noen land blir mva "realisert" gjeld når betalingen fjerner banken, som betyr at den etterdaterte sjekken er utlignet. Du kan aktivere den ved å velge alternativet for **Realiser betinget merverdiavgift når etterdaterte sjekker trekkes** i **Kontant- og bankbehandling > Oppsett > Parametere for kontant- og bankbehandling > Etterdaterte sjekker**.

Hvis du vil ha mer informasjon, kan du se [Definere kildeskattgrupper](tasks/set-up-withholding-tax.md).
