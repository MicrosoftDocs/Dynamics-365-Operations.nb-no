---
title: Arbeidsflytelementer
description: "Denne artikkelen beskriver de ulike elementene som utgjør en arbeidsflyt."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee20b567b402bf638a54f6394159f7f8a9f02da6
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-elements"></a>Arbeidsflytelementer

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver de ulike elementene som utgjør en arbeidsflyt.

En arbeidsflyt består av elementer. Delene nedenfor beskriver hver elementtype.

## <a name="tasks"></a>Oppgaver
En *oppgave* er en arbeidsenhet som må utføres. To typer oppgaver kan legges til en arbeidsflyt: manuelle og automatiserte oppgaver.

### <a name="manual-task"></a>Manuell oppgave

En *manuell oppgave* er en arbeidsenhet som må utføres av en bruker. En arbeidsflyt for reiseregningsrapport kan for eksempel ha manuelle oppgaver som krever at den tilordnede brukeren utfører følgende handlinger:

-   Se gjennom kvitteringene som sendes sammen med en reiseregning.
-   Ring en ansatts leder.

### <a name="automated-task"></a>Automatisert oppgave

En *automatisert oppgave* er en arbeidsenhet som må utføres av systemet. Ingen brukerhandling er nødvendig. En arbeidsflyt for reiseregningsrapport kan for eksempel ha automatiserte oppgaver som krever at systemet utfører følgende handlinger:

-   Utfør en kredittsjekk.
-   Opprett en kundepost for kunden hvis en post ikke allerede finnes.

## <a name="approval-processes"></a>Godkjenningsprosesser
En *godkjenningsprosess* er en prosess som består av separate trinn. I hvert godkjenningstrinn, kan brukeren utføre følgende handlinger:

-   Godkjenne dokumentet
-   Avvise dokumentet
-   Be om en endring i dokumentet
-   Tilordne dokumentet til en annen bruker for godkjenning

## <a name="lineitem-workflow-elements"></a>Elementer for arbeidsflyt for linjeelementer
Du kan opprette en arbeidsflyt for å behandle dokumenter eller linjeelementene på et dokument. Du har for eksempel opprettet en godkjenningsarbeidsflyt for timeregistreringer. (Vi refererer til denne arbeidsflyten som *dokumentarbeidsflyten*.) Du kan legge til et *arbeidsflyt for linjeelementer*-elementet som arbeidsflyten for dokumentet. Når linjeelementet kjøres, sendes hvert linjeelement for dokumentet til behandling. Du vil kanskje at alle linjeelementene skal behandles av den samme arbeidsflyten for linjeelement, eller du vil kanskje at hvert linjeelement skal behandles av en annen arbeidsflyt for linjeelement. La oss si at en ansatt har sendt en timeregistrering som ligner den følgende illustrasjonen. ![Arbeidsflyt med linjeelementer](./media/workflow_lineitemworkflow.gif) I dette scenariet kan det hende at du vil opprette følgende arbeidsflyter for linjeelement:

-   **Arbeidsflyt for linjeelement 1** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 1111.
-   **Arbeidsflyt for linjeelement 2** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 2222.
-   **Arbeidsflyt for linjeelement 3** – Denne arbeidsflyten brukes til å behandle linjeelementer der prosjekt-IDen er 3333.

## <a name="flowcontrol-elements"></a>Flytkontrollelementer
Følgende elementer lar deg utforme arbeidsflyter som har alternative grener eller grener som kjøres samtidig.

### <a name="manual-decision"></a>Manuell beslutning

En *manuell beslutning* er et punkt der en arbeidsflyt deles opp i to grener. En bruker må ta en beslutning, og denne beslutningen bestemmer hvilken gren som skal brukes til å behandle dokumentet som ble sendt.

### <a name="conditional-decision"></a>Betinget beslutning

En *betinget beslutning* er også et punkt der en arbeidsflyt deles opp i to grener. Imidlertid bestemmer systemet hvilken gren som skal brukes til å behandle dokumentet som ble sendt. For å ta denne beslutningen evaluerer systemet dokumentet for å fastslå om det oppfyller angitte vilkår.

### <a name="parallel-activity"></a>Parallell aktivitet

En *parallellaktivitet* er et arbeidsflytelement som omfatter to eller flere arbeidsflytgrener som kjøres samtidig.

### <a name="subworkflow"></a>Underarbeidsflyt

En *underarbeidsflyt* er en arbeidsflyt som kjøres i en annen arbeidsflyt.



