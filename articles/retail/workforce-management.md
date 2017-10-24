---
title: Arbeidsstyringsoversikt
description: "Dette emnet beskriver hvordan du kan bruke arbeidsstyringstjenesten (WFM - Workforce Management) til å utnytte de kjente salgsstedsklientene (POS), Modern POS og Cloud POS, slik at forretningshåndterere enkelt kan administrere arbeidsstyrken."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Arbeidsstyringsoversikt

[!include[banner](includes/banner.md)]
    
Arbeidsstyrketjenesten (WMF) utnytter det kjente salgsstedet (POS) klienter, Modern POS og Cloud POS, for å la butikkledere enkelt administrere deres arbeidskraft. WFM-tjenesten bruker utvidelsesrammen for å laste ned de relevante pakkene i POS. Disse pakkene lastes ned når POS er stengt og gjenåpnes. Derfor, når Microsoft lanserer nye funksjoner for WFM, må POS-appen lukkes og gjenåpnes.

Ved å bruke denne tjenesten, kan ledere i butikker enkelt lage og publisere ukentlig arbeidsplan for sine butikker. Butikkarbeidere kan da raskt se sine egne tidsplaner og planene for sine kolleger. På den måten kan de finne ut hvem som skal jobbe med dem under de tildelte skiftene. Butikkarbeidere kan også lage forespørsler om fravær, bytte av skift og tilbud om skift. Alle disse forespørslene utløser en definert arbeidsflyt.

Under et skift kan butikkarbeidere dra nytte av innstempling og utstemplings-funksjonen som er innebygget i POS-klientene. Dataene sendes deretter til hovedkvarteret (HQ) for lønnsbehandling. Funksjonene innstempling og utstempling er en eksisterende funskjon i POS. For mer informasjon om oppsett og støttede scenarier, se [Innstempling og utstempling](retail-time-attendance.md)

## <a name="supported-scenarios"></a>Scenarier som støttes
Denne delen inneholder mer informasjon om de støttede scenariene.

- **Opprett og publiser tidsplaner** – WFM-tjenesten bruker POS-tillatelser som er konfigurert i HQ for å bestemme om en arbeider har butikksjefs privilegier. Kun butikksjefer kan opprette og publisere tidsplaner ved å bruke Tidsplanleggings-operasjonen. De kan raskt lage en tidsplan ved å kopiere og lime inn et eksisterende arbeidskift fra en arbeidstaker til en annen arbeidstaker. De kan også lage en tidsplan ved å importere timeplanen fra en hvilken som helst forrige uke til den nåværende uken.

    Hvis en tidsplan ikke er publisert, er den i utkasttilstand og ser annerledes ut enn en publisert tidsplan. Butikkansvarlige kan publisere en tidsplan ved å klikke **Publiser**-knappen for hvilken som helst uke. Etter at tidsplanen er publisert for en uke, blir eventuelle endringer automatisk publisert. Eksempler på endringer inkluderer tillegg eller sletting av arbeidsskift eller fravær eller endringer i arbeidsskift eller fravær. Butikkarbeidere kan kun se tidsplaner som har blitt publisert for ulike uker.
    
- **Opprett og godkjenn forespørsler** – Butikkansatte kan opprette tre typer forespørsler:

    - Be om fravær
    - Be om bytte av skift
    - Be om skifttilbud

    Disse forespørslene kan opprettes ved å bruke Planlegge forespørsel-operasjonen. Hvdder forespørsel følger en definert arbeidsflyt, og ansatte kan enkelt se nåværende status for deres forespørsel.
    
    Fraværsforespørsler sendes automatisk til butikkansvarlig for godkjenning. Hvis det er flere butikkansvarlige, kan alle ledere se en bestemt forespørsel, men bare én leder kan godkjenne eller avvise det. Fraværstyper er konfigurert i detaljhandel-HQ ved å bruke **Permisjon og fraværstyper**-siden i **Detaljhandel**-modulen. Etter at butikkansvarlig har godkjent eller avvist en forespørsel flyttes den til kategorien **Historikk** for planleggingsforespørsler-operasjonen.
    
    Et bytte av skift eller skifttilbud-forespørsel går først til den ansatte som forespørselen ble sendt til. Butikkansvarlig kan kun se forespørselen etter at denne arbeideren har godkjent den Derfor, hvis arbeideren avviser skiftbytte eller tilbudsforespørsel om skift, kan lederen ikke se den. Arbeideren som opprettet forespørselen, kan også avbryte det før lederen godkjenner eller avviser den.

- **Vis aktive butikkansatte i planleggingsvisning** – når en ansatt er lagt til en butikk ved, for eksempel, å tilknytte ham eller henne med butikkens adressebok for ansatte, blir arbeideren tilgjengelig for planlegging i WFM-tjenesten. En gjentagende batchjobb som heter **Prosessarbeidsdata for arbeidsstyringsadministrasjon** kjøres i HQ. Denne jobben forbereder butikansattes tilknytninger som sendes til Common Data Service (CDS).

    Den samme prosessen brukes når en ansatt fjernes fra en butikk. Imidlertid vises den ansatte som er fjernet fremdeles for tidligere, nåværende og fremtidige uker dersom et aktiv arbeidsskift eller fravær er tildelt den arbeideren. Derfor, med mindre disse arbeidsskiftene og fraværene blir slettet, vil den fjernede arbeideren fortsette å bli vist i disse ukene.

