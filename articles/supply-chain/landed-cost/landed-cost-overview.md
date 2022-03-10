---
title: Modulen Netto innkjøpspris
description: Modulen Netto innkjøpspris hjelper virksomheter med å strømlinjeforme innkommende forsendelsesoperasjoner ved å gi brukere fullstendig økonomisk kontroll og logistikkontroll over importert frakt, fra produsent til lager.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e4861c0e8b3680f3cd3229facf059b671a4fc765
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983423"
---
# <a name="landed-cost-module"></a>Modulen Netto innkjøpspris

[!include [banner](../../includes/banner.md)]

Modulen **Netto innkjøpspris** hjelper virksomheter med å strømlinjeforme innkommende forsendelsesoperasjoner ved å gi brukere fullstendig økonomisk kontroll og logistikkontroll over importert frakt, fra produsent til lager. For importerte varer kan netto innkjøpspris utgjøre 40 prosent eller mer av den totale kostnaden for hver importerte vare. Derfor er utfordringen å gi nøyaktige estimater for netto innkjøpspris.

Virksomheter kan bruke netto innkjøpspris til å utføre følgende oppgaver:

- Estimere netto innkjøpspris når sjøreisen opprettes.
- Fordelt netto innkjøpspris på flere varer og bestillinger, eller overføringsordrer i én sjøreise.
- Støtte for overføring av varer mellom fysiske lokasjoner ved å anerkjenne netto innkjøpspris.
- Anerkjenne avsetninger for varer i transitt.

Netto innkjøpspris gir nøyaktige og betimelige kostnadsestimater for indirekte kostnader for netto innkjøpspris. Samtidig gir det økt økonomisk og logistisk oversikt over den utvidede forsyningskjeden. Det bidrar også til å redusere administrasjon av etterkalkulerings- og kostnadsfeil.

## <a name="highlights"></a>Høydepunkter

### <a name="voyages"></a>Sjøreiser

I Netto innkjøpspris er en sjøreise en konkret flytting fra en utgående lokasjon gjennom et bestemt sett med destinasjoner i en bestemt periode til en angitt innkommende lagerlokasjon. Bestillinger og ordrelinjer kan legges til i én container eller flere containere for en sjøreise, og kostnadene blir riktig tilordnet tilbake til varelinjen. Ordrer og ordrelinjer kan også legges til på tvers av juridiske enheter for én sjøreise.

### <a name="item-ownership"></a>Vareeierskap

I Microsoft Dynamics 365 Supply Chain Management mottas varer som regel på lagerdestinasjonen, og deretter faktureres de. Men i henhold til de fleste internasjonale forretningsavtaler tar en virkskomhet eierskap av varer fra det tidspunktet de forlater utskpningshavnen, altså før de har blitt fysisk mottatt. Ved hjelp av netto innkjøpspris kan virksomheter fakturere varer før de er fysisk mottatt. Dette konseptet kalles ordre for varer i transitt. Det oppretter en ny type ordre for å administrere mottaket av varene etter at den opprinnelige bestillingen er fakturert.

### <a name="costs"></a>Kostnader

Når du oppretter en sjøreise i Netto innkjøpspris, kan kostnader legges til automatisk. Disse kostnadene defineres i Netto innkjøpspris, og forskjellige kostalternativer og kostbaser er tilgjengelige for dem. Hver kostnad kan defineres for ulike nivåer av en sjøreise og fordeles på varenivå ved hjelp av fordelingsregler som støtter antall, volum, vekt, beløp og definerte volumetriske divisorer. Disse estimerte kostnadene gir et nøyaktig estimat over alle kostnadene for en sjøreise.

Netto innkjøpspris kjører deretter en foreløpig postering/avsetning av den estimerte netto innkjøpsprisen for å sikre at en nøyaktig beregning av estimerte kostnader formidles når sjøreisen opprettes. Ettersom disse automatiske kostnadene blir fakturert, tilbakeføres de estimerte kostnadene og erstattes av de faktiske kostnadene, basert på kostnadsfakturaer.

Faktiske kostnader er tilbakeførte estimerte kostnader som posteres samtidig som kostnaden faktureres, ved hjelp av avstemmingskontoer som er satt opp for hver kostnadstype (for eksempel toll, frakt og forsikring). Disse posteringene følger posteringsvirkemåten som er knyttet til den bestemte varen. Lagerpostering oppdateres automatisk, uansett om posteringstypen er først-inn-først-ut (FIFO), sist inn, først ut (LIFO), glidende avveid gjennomsnitt eller glidende gjennomsnitt. Alle posteringstyper for lagermodellgrupper støttes. Når det gjelder postering av glidende gjennomsnitt og standard kostpris, er avvikskontoer for innkjøpspris tilgjengelige for å postere forskjellene mellom estimerte kostnader og faktiske kostnader.

### <a name="item-and-order-tracking"></a>Vare- og ordresporing

Etter hvert som en sjøreise beveger seg fra den opprinnelige utgående lokasjonen til det endelige destinasjonslageret, kan brukerne oppdatere hvert trinn, eller *etappe*, etter behov. For hver etappe identifiseres det en leveringstid og en forsendelsesstatus. Bekreftede leveringsdatoer for flytting til neste etappe blir også identifisert. Til sammen gir disse leveringsdatoene en forventet leveringsdato for varene til det innkommende lageret. Brukere kan endre disse leveringsdatoene. I dette tilfellet oppdateres da den estimerte leveringsdatoen for varene automatisk, basert på leveringstidene og reisens etapper. Oversikten over varer i transitt basert på sjøreise og transportmiddel er tilgjengelig per container før mottak av varene. Ettersom datoene oppdateres på hver bestillingslinje, har virksomheter mer kontroll over logistikk og lagerplanlegging.

## <a name="landed-cost-concepts"></a>Begreper for netto innkjøpspris

Tabellen nedenfor oppsummerer noen kjernebegrep for netto innkjøpspris.

| Konsept | beskrivelse |
|---|---|
| Sjøreise | En sjøreise er vanligvis ett fartøy. Avhengig av praksis og fremgangsmåter kan det imidlertid være én leverandør eller én bestilling. Det er ingen begrensninger for bruken av dette konseptet. |
| Folio | En folio blir ofte fastsatt av tollbestemmelser. Det kan bestå av én leverandørs varer for én enhet/et firma per forsendelse. Varene i en folio kan være i én container, eller være spredt på flere containere. |
| Fraktcontainer | Forsendelsescontainere lagrer bestillingslinljer. De er på et nivå under forsendelsesnivået. De brukes vanligvis hvis kostnader fordeles for varer etter container, eller hvis mottak skjer per container. |
| Fraktcontainertype | Forsendelsescontainertyper kan bestemme prisen for en kosttype (for eksempel frakt). De gir også nyttig forsendelsesinformasjon. |
| Kostnadstype | Kosttyper identifiserer kostnader som er knyttet til importer, for eksempel toll, frakt og forsikring. |
| Automatisk kostnad | Automatiske kostnader fungerer som forretningsavtaler. En automatisk kostnad er koblet til et sjøreisenivå. |
| Havn | Havner er områder der varer mottas og overføres fra. |
| Fartøy | Et fartøy er mediet som brukes til å transportere varer, for eksempel et skip eller et fly. |
| Varer i transitt | Varer plasseres i et transittlager etter at en faktura oppdateres, avhengig av innstillingene. |
| Aktivitet | Aktiviteter kan brukes til å lagre hvert viktige trinn av reisen mellom to havner. De kan brukes til å oppdatere datoer. |
| Reisemal | Reisemaler er ruter som varer tar mellom to havner. |

Hvis du vil ha en sammenligning av terminologien for og funksjonene til modulene **Netto innkjøpspris** og **Transportstyring** (TMS), kan du se [Netto innkjøpspris vs. Transportstyring](landed-cost-vs-tms.md).
