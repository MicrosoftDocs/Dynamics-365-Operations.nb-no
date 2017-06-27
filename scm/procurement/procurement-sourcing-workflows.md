---
title: "Arbeidsflyter for innkjøp og leverandører"
description: "Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen. Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 67bdb8436ff379b0e55cfe1660597e8f93235eeb
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="procurement-and-sourcing-workflows"></a>Arbeidsflyter for innkjøp og leverandører

[!include[banner](../includes/banner.md)]


Noen organisasjoner krever at innkjøpsrekvisisjoner og bestillinger er godkjent av en annen bruker enn den som registrerte transaksjonen. Hvis du vil konfigurere en godkjenningsprosess, kan du opprette en arbeidsflyt.

En arbeidsflyt representerer en forretningsprosess. Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument. Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:
-   **Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter. Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.
-   **Prosessynlighet** – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst. Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.
-   **Sentralisert arbeidsliste**– Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet på tvers av alle arbeidsflyter de deltar i. Dette er tilgjengelig på siden Arbeidselementer.

## <a name="the-types-of-workflows-that-you-can-create"></a> Arbeidsflyttypene som du kan opprette
Arbeidsflyttypene nedenfor er tilgjengelige for Innkjøp og leverandører.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Type**                         | **Bruk denne typen til å gjøre følgende:**                                          |
| Gjennomgang av innkjøpsrekvisisjon      | Opprett gjennomgangsarbeidsflyter for innkjøpsrekvisisjoner.            |
| Gjennomgang av innkjøpsrekvisisjonslinje | Opprett gjennomgangsarbeidsflyter for innkjøpsrekvisisjonslinjer.       |
| Bestillingsarbeidsflyt          | Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillinger.     |
| Bestillingslinjearbeidsflyt     | Opprett gjennomgangs- og godkjenningsarbeidsflyter for bestillingslinjer. |

## <a name="creating-a-workflow"></a>Opprette en arbeidsflyt
Hvis du vil opprette en arbeidsflyt, kan du gå til Innkjøp og leverandører &gt; Oppsett &gt; Arbeidsflyter for innkjøp og leverandører, og opprette en ny arbeidsflyt ved å velge typen arbeidsflyt som du vil opprette.  

Du kan dra arbeidsflytelementer til utformingen og koble elementene til en flyt på arbeidsflytlerretet. Arbeidsflytelementene må konfigureres. For arbeidsflytelementer for godkjenning og oppgave kan du konfigurere hvilken deltaker som skal utføre handlingen.
Deltakertyper
----------------------

Du kan tilordne et godkjenningstrinn til deltakergruppene nedenfor.

| Brukergruppe    | Beskrivelse                                                               |
|---------------|---------------------------------------------------------------------------|
| Deltaker   | Tilordne godkjenningstrinnet til medlemmer av en gruppe eller rolle.                   |
| Hierarki     | Tilordne godkjenningstrinnet til brukere i et bestemt organisasjonshierarki. |
| Arbeidsflytbruker | Tilordne godkjenningstrinnet til brukere av denne arbeidsflyten.                       |
| Kø         | Tilordne godkjenningstrinnet til en arbeidselementkø.                            |
| Bruker          | Tilordne godkjenningstrinnet til bestemte brukere.                               |



<a name="see-also"></a>Se også
--------

[Definere arbeidsflyter for forretningsprosesser for innkjøpsrekvisisjoner](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Arbeidsflyt for innkjøpsrekvisisjon](purchase-requisitions-workflow.md)




