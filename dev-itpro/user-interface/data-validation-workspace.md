---
title: "Arbeidsområde for datavalidering"
description: "Med arbeidsområdet Sjekkliste for datavalidering kan du spore prosesser for validering av data på tvers av firmaer, områder og personer. Sjekklisten kan brukes i løpet av en ny implementering, etter en oppgradering eller etter en overføring."
author: bking
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e105c4b171979a03c20718c1fa9d558c921cd704
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017

---

# <a name="data-validation-workspace"></a>Arbeidsområde for datavalidering

[!include[banner](../includes/banner.md)]


Dette emnet gir en oversikt over **arbeidsområdet for sjekkliste for datavalidering** og den tilknyttede konfigurasjonen.

## <a name="data-validation-checklist-workspace"></a>Arbeidsområde for sjekkliste for datavalidering

Med arbeidsområdet **Sjekkliste for datavalidering** kan du spore prosesser for validering av data på tvers av firmaer, områder og personer. Sjekklisten kan brukes i løpet av en ny implementering, etter en oppgradering eller etter en overføring. Avhengig av visningen av arbeidsområdet **Sjekkliste for datavalidering** vil du se alle oppgaver og statuser for et datavalideringsprosjekt eller bare oppgavene som er tilordnet til deg.

Du må først velge et datavalideringsprosjekt øverst i arbeidsområdet. Alle data som vises i arbeidsområdet, blir deretter filtrert etter det valgte datavalideringsprosjektet.

### <a name="summary-tiles"></a>Sammendrag-fliser

Flisene **Sammendrag** gir en oversikt over prosessen og indikatorer hjelper deg med å holde datavalideringsprosessen i rute. Du kan se alle prosessens gjenværende oppgaver, fullførte oppgaver, oppgaver som pågår, og oppgaver som ikke har startet. Denne informasjonen er for alle firmaer som er inkludert i den valgte datavalideringsprosjektet.

### <a name="tasks-and-status-section"></a>Delen Oppgaver og status

I delen **Oppgaver og status** vises status for det generelle datavalideringsprosjektet på forskjellige måter: status etter juridisk enhet, etter område og etter oppgaveliste. Du kan velge filteret for å vise statusen for et bestemt firma. Hver statuskategori gir en detaljert oversikt over både prosenten som er fullført og hvor mange oppgaver som gjenstår.

Den siste kategorien er for den detaljerte oppgavelisten. Denne listen viser hele oppgavelisten.
Du kan filtrere listen over oppgaver på flere måter. Klikk **Rediger oppgave** for å endre statusen til en oppgave eller tilordne en oppgave. Klikk **vedlegg** for å vise vedlegg for en oppgave.

Oppgavenavnet er en hyperkobling til Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations-siden eller en annen nettside brukeren må gå til for å fullføre arbeidet. Du kan angi denne hyperkoblingen ved å bruke feltet **Menyelementnavn** når du redigerer eller oppretter en oppgave fra skjemaet **Konfigurer datavalideringsprosjekt**.

Du kan knytte filer, notater, bilder og nettadresser til en oppgave ved hjelp av handlingen **Vedlegg**. Du kan for eksempel legge ved en rapportfil som ble skrevet ut for en oppgave. Et ikon vises i **Vedlegg**-kolonnen for oppgaven hvis det finnes et vedlegg.

Alternativet **Fullført av** fylles automatisk ut når aktiviteten er fullført, med navnet på arbeideren som fullført oppgaven. Når en oppgave er merket som fullført, oppdateres feltet **Fullføringsdato** automatisk til gjeldende dato og klokkeslett.

### <a name="configure-data-validation-project-page"></a>Konfigurere datavalideringsprosjektsiden

Før du kan bruke arbeidsområdet **Sjekkliste for datavalidering**, må du konfigurere prosessen ved hjelp av siden **Konfigurer datavalideringsprosjekt**. (Klikk **Arbeidsområder** \> **Sjekkliste for datavalidering** \> **Konfigurer datavalideringsprosjekt**.)

### <a name="task-areas"></a>Oppgaveområder

Du kan bruke oppgaveområder til å gruppere datavalideringsoppgaver i logiske eierskapsområder i organisasjonen. Leverandører, Kunder eller Økonomimodul kan for eksempel brukes som oppgaveområder.

**Menyelementnavnet** er tilknyttet arbeidsinnsatsen for oppgaven og kan brukes til å gå direkte til den tilknyttede siden fra oppgavekoblingen i arbeidsområdet. En datavalideringsoppgave som skal kjøre **aldersfordelingsrapporten** for leverandører som kan kobles til  **aldersfordelingsrapport**-siden.
