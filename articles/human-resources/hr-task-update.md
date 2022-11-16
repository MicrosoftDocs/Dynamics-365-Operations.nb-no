---
title: Definer oppgaver i Oppgavebehandling
description: Denne artikkelen forklarer hvordan du definerer oppgaver i Oppgavebehandling i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745391"
---
# <a name="set-up-tasks-in-task-management"></a>Definer oppgaver i Oppgavebehandling

[!INCLUDE [PEAP](../includes/peap-1.md)]

I versjoner av Microsoft Dynamics 365 Human Resources før versjon 10.0.30 måtte brukere som ville redigere en oppgave, redigere oppgaven individuelt på hver sjekkliste som inneholdt den. Fra og med Human Resources versjon 10.0.30 kan imidlertid brukere velge hvordan redigerte oppgaver skal håndteres. Hvis en oppgave som redigeres, er i en sjekkliste, må alternativet **Aktiver oppgradering av oppgavebehandling** velges i fanen **Oppgavebehandling** på siden **Delte parametere for personaladministrasjon** for at sjekklisten skal kunne bruke den redigerte oppgaven.

[![Aktiver oppgraderingsalternativet for oppgavebehandling på siden Delte parametere for personaladministrasjon.](./media/task-update.png)](./media/task-update.png)

Hvis endringer i oppgaver skal brukes på alle tilknyttede sjekklisteoppgaver, må det allerede finnes en relasjon mellom oppgaven i oppgavebiblioteket og oppgaven i sjekklisten. Det er lagt til et alternativ for å opprette relasjonen mellom bibliotekoppgaven og sjekklisteoppgaven.

Du kan opprette oppgaver enkeltvis og deretter bruke dem på nytt i flere sjekklister. Hvis du vil opprette en oppgave, går du til siden **Oppsett av pålasting**, kategorien **Oppgaver** og velger **Ny**.

## <a name="set-up-tasks"></a>Definer oppgaver

Du kan tilordne en opprettet oppgave til flere sjekklister ved å velge oppgaven og deretter velge **Bruk på sjekklister** på menyen.

Du kan også legge til oppgaver direkte i en sjekkliste. Hvis du vil legge til en oppgave i en sjekkliste, kan du gå til siden **Oppsett for jobbintroduksjon** i **Sjekkliste**-fanen og enten opprette en ny sjekkliste å legge til oppgaven i, eller legge til oppgaven i en eksisterende sjekkliste.

Hvis du vil redigere en bibliotekoppgave, velger du **Rediger** på menyen for oppgavebibliotek. Hvis oppgaven er knyttet til eventuelle sjekklister, vises disse sjekklistene på siden **Rediger oppgave**. Hvis du vil at oppgavene i en av sjekklistene skal oppdateres med endringene, velger du disse sjekklistene i delen **Bruk på sjekklister**.

Hvis du vil slette oppgaver fra oppgavebiblioteket, velger du **Slett**. Hvis oppgaven er knyttet til en sjekkliste, sletter ikke denne handlingen oppgaven fra sjekklisten. En separat handling er nødvendig for å fjerne en oppgave fra en sjekkliste.

### <a name="set-up-checklists"></a>Definer sjekklister

En sjekkliste er en gruppe oppgaver. Du kan opprette så mange sjekklister du krever, og du kan tilordne de samme oppgavene til flere sjekklister. Når du oppretter en sjekkliste, angir du en eier og en kalender.

Hvis du vil opprette en ny oppgave i en sjekkliste, velger du **Ny** på menylinjen for oppgaver. Når du oppretter en ny oppgave, kan du eventuelt legge til oppgaven i oppgavebiblioteket, slik at den kan deles på tvers av flere sjekklister. Du kan legge til oppgaven i oppgavebiblioteket ved å sette alternativet **Bruk oppgave i bibliotek** til **Ja**. Hvis du velger å legge til oppgaven i oppgavebiblioteket, kan du også legge til oppgaven i andre sjekklister samtidig ved å velge disse sjekklistene i delen **Bruk på sjekklister**. Hvis du lar være å legge til oppgaven i oppgavebiblioteket, finnes oppgaven bare i sjekklisten der du oppretter den.

Du kan redigere en oppgave i en sjekkliste ved å velge **Rediger** på oppgavemenyen. Hvis oppgaven er knyttet til eventuelle sjekklister, vises disse sjekklistene på siden **Rediger oppgave**. Hvis du vil at oppgavene i de andre sjekklistene skal oppdateres med endringene, velger du disse sjekklistene i delen **Bruk på sjekklister**.

Hvis du vil fjerne oppgaver fra en sjekkliste, velger du **Fjern**. Denne handlingen fjerner oppgavene fra sjekklisten. De slettes imidlertid ikke fra oppgavebiblioteket. Hvis du vil slette oppgaver fra oppgavebiblioteket, åpner du siden **Oppgavebibliotek** og velger **Slett**.
