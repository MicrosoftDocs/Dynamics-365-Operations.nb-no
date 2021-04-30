---
title: Arbeidsflyter for innkjøp og leverandører
description: Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen. Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 126e9969f312ff7f6a6c64b733708754e7659214
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909237"
---
# <a name="procurement-and-sourcing-workflows"></a>Arbeidsflyter for innkjøp og leverandører

[!include [banner](../includes/banner.md)]

Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen. Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt.

En arbeidsflyt representerer en forretningsprosess. Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument. Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:

- **Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter. Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.
- **Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst. Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.
- **Sentralisert arbeidsliste**– Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet på tvers av alle arbeidsflyter de deltar i. Dette er tilgjengelig på siden Arbeidselementer.

## <a name="the-types-of-workflows-that-you-can-create"></a> Arbeidsflyttypene som du kan opprette

Arbeidsflyttypene nedenfor er tilgjengelige for Innkjøp og leverandører.

| Type | Bruk denne typen til å gjøre følgende: |
|---|---|
| Gjennomgang av innkjøpsrekvisisjon | Opprett arbeidsflyter for gjennomgang og godkjenning av innkjøpsrekvisisjoner. |
| Gjennomgang av innkjøpsrekvisisjonslinje | Opprett arbeidsflyter for gjennomgang og godkjenning av innkjøpsrekvisisjonslinjer. |
| Bestillingsarbeidsflyt | Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillinger. |
| Bestillingslinjearbeidsflyt | Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillingslinjer. |
| Arbeidsflyt for søknad om tillegging av leverandører | Opprett arbeidsflyter for gjennomgang og godkjenning for å legge til nye leverandører via leverandørforespørsler. |

> [!IMPORTANT]
> Når du legger til en ny arbeidsflyt, kan det hende at du også ser følgende foreldede arbeidsflyter som vises i dialogboksen **Opprett arbeidsflyt**. Disse er knyttet til funksjonaliteten *bekreftelse på mottak* som var tilgjengelig i [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), men som nå er avskrevet. Disse arbeidsflytene støttes ikke.
> 
> - Varslingsarbeidsflyt for forfallsdato for levering
> - Varslingsarbeidsflyt for fakturamottak
> - Varslingsarbeidsflyt for mislykket mottaksseddel
> - Varslingsarbeidsflyt for ubekreftet mottaksseddelavvisning

## <a name="creating-a-workflow"></a>Opprette en arbeidsflyt

Hvis du vil opprette en arbeidsflyt, kan du gå til Innkjøp og leverandører &gt; Oppsett &gt; Arbeidsflyter for innkjøp og leverandører, og opprette en ny arbeidsflyt ved å velge typen arbeidsflyt som du vil opprette. 

Du kan dra arbeidsflytelementer til utformingen og koble elementene til en flyt på arbeidsflytlerretet. Arbeidsflytelementene må konfigureres. For arbeidsflytelementer for godkjenning og oppgave kan du konfigurere hvilken deltaker som skal utføre handlingen.

## <a name="types-of-participants"></a>Deltakertyper

Du kan tilordne et godkjenningstrinn til deltakergruppene nedenfor.

| Brukergruppe | Beskrivelse |
|---|---|
| Deltaker | Tilordne godkjenningstrinnet til medlemmer av en gruppe eller rolle. |
| Hierarki | Tilordne godkjenningstrinnet til brukere i et bestemt organisasjonshierarki. |
| Arbeidsflytbruker | Tilordne godkjenningstrinnet til brukere av denne arbeidsflyten. |
| Kø | Tilordne godkjenningstrinnet til en arbeidselementkø. |
| Bruker | Tilordne godkjenningstrinnet til bestemte brukere. |

## <a name="additional-resources"></a>Tilleggsressurser

- [Definere arbeidsflyter for forretningsprosesser for innkjøpsrekvisisjoner](https://www.microsoft.com/download/details.aspx?id=101821)
- [Arbeidsflyt for innkjøpsrekvisisjon](purchase-requisitions-workflow.md)
- [Ønske leverandører velkommen](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]