---
title: Tilordne oppgavelister til butikker eller ansatte
description: Denne artikkelen beskriver hvordan du tilordner oppgavelister til butikker eller ansatte i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: faff772051738f624b86fd23fb6bf29173e909ea
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746201"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Tilordne oppgavelister til butikker eller ansatte

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du tilordner oppgavelister til butikker eller ansatte i Microsoft Dynamics 365 Commerce.

Ved hjelp av oppgavebehandling i Dynamics 365 Commerce kan du tilordne en oppgaveliste til flere butikker eller ansatte, eller til en kombinasjon av butikker og ansatte. Det kan for eksempel hende at en regional leder for 20 butikker vil tilordne oppgavelisten **Forberedelser for høytiden** til alle de 20 butikkene.

## <a name="start-the-task-list-assignment-process"></a>Starte tilordningsprosessen for oppgaveliste

Før du begynner å tilordne oppgaver, må du passe på at du har opprettet en oppgaveliste ved å følge trinnene i artikkelen [Opprett oppgavelister og legg til oppgaver](task-mgmt-create-lists.md). Følg denne fremgangs måten for å starte prosessen med å tilordne en oppgaveliste.

1. Gå til **Retail og Commerce \> Oppgavebehandling \> Administrasjon av oppgavebehandling**.
1. Velg oppgavelisten du vil tilordne.
1. Velg **Start prosess**.
1. I dialogboksen **Start prosess**, i kategorien **Generelt**, i feltet **Prosessnavn** angir du et navn (for eksempel **Butikker i østlige region**).
1. I **Måldato**-feltet angir du en dato.
1. Hvis du vil tilordne oppgavelisten til butikker, går du til kategorien **Butikker** og bruker filteret **Organisasjonshierarki** til å finne og velge butikkene.

    Hvis du vil tilordne oppgavelisten til ansatte, går du til kategorien **Ansatte** for å finne og velge de ansatte.

1. Velg **OK** for å starte prosessen. Oppgavelisten tilordnes til de valgte butikkene eller ansatte.

Illustrasjonen nedenfor viser et eksempel på hvordan du finner og velger butikker i dialogboksen **Start prosess**.

![Finne og velge butikker i dialogboksen Start prosess.](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Tilordne oppgavelister regelmessig

Forhandleren har noen ganger gjentakende oppgaver, for eksempel "Sjekkliste for torsdagslukking" eller "Sjekkliste for første dag i måneden". Det kan derfor hende at de vil tilordne oppgavelisten regelmessig.

1. Gå til **Retail og Commerce \> Oppgavebehandling \> Administrasjon av oppgavebehandling**.
1. Velg oppgavelisten du vil tilordne.
1. Velg **Start prosess**.
1. I dialogboksen **Start prosess**, i kategorien **Generelt**, i feltet **Prosessnavn** angir du et navn.
1. Sett alternativet **Gjentakelse** til **Ja**.
1. Angi et antall dager i feltet **Forskyvning av måldato for gjentakelse i dager**. Hvis du for eksempel angir **4**, er måldatoen gjentakelsesdatoen pluss fire dager.
1. I kategorien **Kjør i bakgrunnen** velger du **Regelmessighet**.
1. Angi frekvenskriteriene i dialogboksen **Definer regelmessighet**, og velg deretter **OK**.

Illustrasjonen nedenfor viser et eksempel på hvordan du kan angi frekvenskriterier i dialogboksen **Definer regelmessighet**.

![Angi frekvenskriterier i dialogboksen Definer regelmessighet.](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Status for sporing av oppgaveliste

Hvis du er en regional leder eller butikkleder, vil du kanskje spore statusen for oppgavelister som er tilordnet til flere butikker eller ansatte. Deretter kan du følge opp med butikker eller ansatte som ikke utførte de tildelte oppgavene i tide. Med Commerce Back Office kan du vise statusen for oppgavelister, tildele oppgaver på nytt eller endre statusen for en oppgave.

Følg denne fremgangsmåten for å spore statusen for oppgavelisten for alle oppgaver.

1. Gå til **Retail og Commerce \> Oppgavebehandling \> Oppgavebehandlingsprosesser**.
1. Velg kategorien **Alle oppgavelister** for å vise statusen for alle oppgavelistene som er tilordnet forskjellige butikker.

Følg denne fremgangsmåten for å spore statusen for alle oppgaver som er tilordnet til deg.

1. Gå til **Retail og Commerce \> Oppgavebehandling \> Oppgavebehandlingsprosesser**.
1. Velg kategorien **Mine oppgaver** eller **Alle oppgaver** for å vise eller oppdatere statusen for oppgaver som er tilordnet til deg.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over oppgavebehandling](task-mgmt-overview.md)

[Konfigurere oppgavebehandling](task-mgmt-configure.md)

[Opprette oppgavelister og legge til oppgaver](task-mgmt-create-lists.md)

[Oppgavebehandling på salgsstedet](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
