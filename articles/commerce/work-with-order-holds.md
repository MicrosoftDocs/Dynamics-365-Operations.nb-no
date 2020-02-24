---
title: Konfigurere og arbeide med telefonsenterordresperringer
description: Dette emnet beskriver hvordan du arbeider med sperringer på ordrer ved hjelp av Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 08c0eda418af1aa56c6cc71ca1f7f10460651bc9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023518"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Konfigurere og arbeide med ordresperrer i telefonsenter

[!include [banner](includes/banner.md)]

Dette emnet beskriver ordresperrefunksjonene som Dynamics 365 Commerce har for telefonsenterordrer.

## <a name="configuring-call-center-order-holds"></a>Konfigurere telefonsenterordresperrer

For å bruke sperrefunksjonene for telefonsenterordrer må du først angi sperrekoder. Hvis du vil opprette et sett med brukerdefinerte sperrekoder basert på dine forretningskrav, kan du gå til **Salg og markedsføring** \> **Oppsett** \> **Salgsordrer** \> **Ordresperrekoder**. Du kan eventuelt flagge en av sperrekodene som standard sperrekode ved å sette **Standard for salgsordre**-alternativet til **Ja**. Denne sperrekoden vil bli brukt hver gang en salgsordre er satt på vent. Hvis en salgsordre har reservert lager, og reservasjonene må fjernes automatisk hvis ordren er satt på vent av en bestemt årsak, kan du angi **Fjern beholdningsreservasjoner**-alternativet til **Ja** for årsakskodene.

Hvis du vil angi hvilken type merknad som skal registreres når brukere som plasserer en ordre på vent, angir valgfrie merknader, kan du gå til **Kunder** \> **Oppsett** \> **Kundeparametere**, og på **Salgsoppsett**-hurtigkategorien i **Generelt**-kategorien kan du angi **Merknadstype**-feltet. Bruk **På vent-salgsordrestatus**-feltet for å definere fargen som brukes til å utheve salgsordrer som er på vent når de vises på **Kundeservice**-siden.

Hvis du vil opprette et valgfritt sett med På vent-årsakskoder, kan du gå til **Retail og Commerce** \> **Kanaloppsett** \> **Infokoder**. Disse infokodene kan brukes som sekundær årsakskode for å definere hovedsperrekoden nærmere. Velg **Ny** for å opprette et årsakskodesett, og velg deretter **Delkoder** for å definere listen over tilleggsårsaker. Hvis du vil koble infokoder som du definerer til telefonsenterkanalen, kan du gå til **Retail og Commerce** \> **Kanaler** \> **Telefonsentre** \> **Alle telefonsentre**. På **Generelt**-hurtigfanen angir du **Sperrekode**-feltet.

## <a name="putting-orders-on-hold"></a>Sette ordrer på vent

Ordrer som telefonsenterbrukere oppretter i bakhandelsprogrammet, kan settes på vent manuelt eller automatisk i bestemte situasjoner.

Under ordreregistrering, men før bestillingen legges inn og bekreftes, ønsker telefonsenterbrukere kanskje å sette en ordre på vent manuelt for å hindre at den blir frigitt til lageret for videre behandling. Kunden som plasserer ordren er eksempelvis kanskje ikke klar til å forplikte seg til den, eller kritiske data som kreves for å behandle ordren, mangler kanskje.

På siden for ordreregistrering kan telefonsenterbrukeren sette en ordre på vent ved å bruke **Ordresperrer**-alternativet på **Salgsordre**-kategorien på ordreregistreringsmenyen. Brukeren kan også velge **Sperre**-menyelementet på **Salgsordresammendrag**-siden som vises når han eller hun velger **Fullført** på en salgsordre via et telefonsenter.

I begge tilfeller vises siden **Ordresperrer**. Deretter kan brukeren velge **Ny** for å opprette en sperring for ordren. I **Sperrekode**-feltet bør brukeren velge koden som best beskriver årsaken til sperringen. I **Årsakskode**-feltet kan brukeren også velge en tilleggskode for å gi et ekstra nivå for beskrivelsen av sperringen.

I **Merknader**-hurtigkategorien i **Sperremerknader**-feltet kan brukeren angi ytterligere merknader i fritt format for å gi ytterligere kontekst eller informasjon om sperringen. Disse merknadene kan hjelpe andre brukere som gjennomgår eller arbeider med sperreorden senere.

Når sperreinformasjonen er angitt og lagret, kan brukeren lukke **Ordresperrer**-siden. Brukeren returneres deretter til siden for salgsordreregistrering. Hvis det ikke kreves flere handlinger på salgsordren, kan du lukke siden salgsordreregistrering.

Hvis **Aktiver ordrefullføring**-flagget er aktivert i telefonsenterkanal, må ikke betalingen brukes på en ordre som er satt på vent. Men for en salgsordre som ikke er satt på vent, kan ikke brukere forlate siden salgsordreregistrering før betalingen er brukt. Betalingen vil selvfølgelig være nødvendig før ordrensperren frigis.

I tillegg kan telefonsenterbrukere legge en manuell svindelsperre på ordrer som er mistenkelige av en eller annen grunn. Ordrer kan også plasseres på vent automatisk når de oppfyller aktive vilkår og regler for svindel. Hvis du vil ha mer informasjon om denne typen ordresperre, se [Konfigurere svindelvarsler](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Vise og behandle ordrer på vent

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Vise venteinformasjon for én enkelt salgsordre

På **Kundestøtte**-siden kan brukere visuelt identifisere ordrer som er på vent, fordi ordrelinjene er merket med en bestemt farge. Denne fargen er definert av **På vent-salgsordrestatus**-feltet på **Kundeparametere**-siden.

> [!NOTE]
> Hvis linjen er valgt på siden, kan ikke uthevingsfargen vises.

Brukere kan også vise detaljert statusinformasjon for en salgsordre for å finne ut om ordren er på vent. Detaljert statusinformasjon kan nås fra siden **Alle salgsordrer** eller **Kundeservice**. Hvis en ordre er på vent, er **Behandler ikke**-flagget angitt for den, og **Detaljert status**-feltet viser statusen **På vent** eller **Svindelsperre**, avhengig av scenariet.

Hvis du vil vise detaljene for en enkelt ordresperre, kan brukere åpne en detaljert visning av **Ordresperre**-siden fra **Kundestøtte**-siden ved hjelp av **Alternativer**-menyen for den valgte ordren. Brukere kan også få tilgang til denne visningen fra **Alle salgsordre**-siden ved å velge **Ordresperrer**-menyelementet på **Salgsordre**-kategorien.

### <a name="viewing-all-orders-that-are-on-hold"></a>Vise alle ordrer på vent

Hvis du vil vise alle ordrer som har blitt satt på manuell eller automatisk vent, kan du gå til **Retail og Commerce** \> **Kunder** \> **Ordresperrer**.

**Ordresperrer**-arbeidsområdet viser en listevisning over alle ordrer som er på vent på grunn av manuelle eller svindelrelaterte sperrehandlinger. Ved hjelp av standard filtrerings- og sorteringsalternativer på siden kan brukere opprette visninger som gjør at de kan jobbe med eller administrere bestemte sperrekoder som de er ansvarlige for å gå gjennom. **Ordresperrer**-arbeidsområdet angir også antall dager en ordren har vært på vent. Denne informasjonen kan hjelpe brukere med å prioritere køen.

Brukere kan klikke **Ordresperre** på menyen for å få en mer detaljert visning over ordrene som er satt på vent. Denne visningen gir informasjon om kunden, alle merknader som er brukt på ordren, kunden eller sperrehandlingen. Visningen inneholder også informasjon om årsaken til en automatisk sperre, hvis bestillingen ble satt på vent fordi den samsvarer med en regel for svindel.

Både fra listevisningen og den detaljerte visningen av **Ordresperrer**-siden kan brukere vise eller redigere bestillingsrelatert tilleggsinformasjon, for eksempel betalinger, totaler og notater.

Alternativene i **Sperre - utsjekking**-kategorien kan være nyttig hvis flere brukere i firmaet arbeider i sperrekøen samtidig. Ved å velge **Sjekk ut**-alternativet kan brukere angi at de arbeider for å gå gjennom og undersøke ordresperren. På denne måten kan ikke andre brukere kaste bort tid ved å prøve å gjøre den samme jobben. Fra detaljert visning av **Ordresperrer**-siden kan brukere vise informasjon om datoen og klokkeslettet for utsjekkingen og brukeren som sjekket ut sperreposten.

Når en sperrepost er sjekket ut, kan bare brukeren som sjekket den ut, fjerne utsjekkingen. Denne begrensningen skal hindre at brukere tar poster som andre brukere allerede arbeider på. For å frigi en ordre tilbake til køen slik at andre brukere kan arbeide med den, må brukeren som sjekket ut posten, velge **Fjern utsjekking** alternativet.

> [!NOTE]
> Sperren er ikke frigitt når utsjekkingen er fjernet.

I noen tilfeller, for eksempel når en bruker er syk eller har sluttet i firmaet, kan det hende at poster som er sjekket ut til denne brukeren, må tilordnes til en annen bruker på nytt. En leder kan tilordne poster på nytt ved hjelp av **Overstyr utsjekking**-alternativet.

## <a name="releasing-orders-that-are-on-hold"></a>Frigi ordrer på vent

I både liste- og detaljert visning av **Ordresperrer**-siden inneholder **Fjern sperre**-kategorien alternativene som brukes til å frigi en ordresperre. Bruk **Fjern sperrer**-alternativet til å frigi en bestilling fra den valgte sperrekoden.

Telefonsenterordrer krever betaling. Derfor kan en sperre ikke fullstendig fjernes hvis betalingen ikke er brukt på ordren. På **Telefonsenterparametere**-siden, i **Sperrer**-kategorien, må du kontrollere at **Send når fjernet**-parameteren er aktivert. Denne innstillingen garanterer at en fjernet sperreordre gjennomgår riktig ordreoverføringlogikk for å validere og godkjenne betalinger. Hvis betalinger mangler, får brukeren en feilmelding, og sperrekoden fjernes ikke.

Hvis **Send når fjernet**-parameteren ikke er angitt, må brukere velge **Fjern og send**-alternativet på **Fjern sperre**-menyen for å garantere at ordren går gjennom alle nødvendige betalingsvalideringer. Hvis bestillingen mislykkes når **Aktiver ordrefullføring**-flagget er aktivert i telefonsenterkanalen, frigis ordren fra sperrestatusen, men **Ikke behandle**-flagget beholdes. Ordren er derfor ikke frigitt til lageret før riktige betalinger er brukt og godkjent.

Hvis brukerne vil fjerne en sperring, men gjør flere endringer i bestillingen før den frigis for videre behandling, kan de velge **Fjern og endre**-alternativet. Dette alternativet fjerner sperrekoden og åpner salgsordredetaljer, slik at brukere kan gjøre flere endringer i ordren. Brukere kan også bruke betaling og sende salgsordren til betalingensvalideringlogikken når **Aktiver ordrefullføring**-flagget er aktivert i telefonsenterkanalen.

## <a name="reporting-options"></a>Rapporteringsalternativer

Gå til **Retail og Commerce** \> **Forespørsler og rapporter** \> **Telefonsenterrapporter** \> **Rapport for ordresperre** for å kjøre en rapport om ordresperrer etter datointervall, sperrekode eller andre relaterte kriterier.
