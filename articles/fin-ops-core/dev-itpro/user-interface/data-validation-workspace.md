---
title: Arbeidsområde for sjekkliste for datavalidering
description: Med arbeidsområdet Sjekkliste for datavalidering kan du spore prosesser for validering av data på tvers av firmaer, områder og personer. Sjekklisten kan brukes i løpet av en ny implementering, etter en oppgradering eller etter en overføring.
author: bking
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DataValidationWorkspace
audience: Application User
ms.reviewer: rhaertle
ms.assetid: ''
ms.search.region: Global
ms.author: bking
ms.openlocfilehash: a3ac338670fdc9fc7cb526cdcdc1e7199904da8f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687581"
---
# <a name="data-validation-checklist-workspace"></a>Arbeidsområde for sjekkliste for datavalidering

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over **arbeidsområdet for sjekkliste for datavalidering** og den tilknyttede konfigurasjonen.

Med arbeidsområdet **Sjekkliste for datavalidering** kan du spore prosesser for validering av data på tvers av firmaer, områder og personer. Sjekklisten kan brukes i løpet av en ny implementering, etter en oppgradering eller etter en overføring. Avhengig av visningen av arbeidsområdet **Sjekkliste for datavalidering** vil du se alle oppgaver og statuser for et datavalideringsprosjekt eller bare oppgavene som er tilordnet til deg.

Du må først velge et datavalideringsprosjekt øverst i arbeidsområdet. Alle data som vises i arbeidsområdet, blir deretter filtrert etter det valgte datavalideringsprosjektet.

## <a name="summary-tiles"></a>Sammendrag-fliser

**Sammendrag**-flisene gir en oversikt over prosessen, og indikatorer hjelper deg med å holde datavalideringsprosessen på sporet. Du kan se alle gjenværende oppgaver, gjennomførte oppgaver, pågående oppgaver og ikke påbegynte oppgaver for prosessen. Denne informasjonen er for alle firmaer som er inkludert i den valgte datavalideringsprosjektet.

## <a name="tasks-and-status-section"></a>Delen Oppgaver og status

I delen **Oppgaver og status** vises status for det generelle datavalideringsprosjektet på forskjellige måter: status etter juridisk enhet, etter område og etter oppgaveliste. Du kan velge filteret for å vise statusen for et bestemt firma. Hver statuskategori gir en detaljert oversikt over både prosenten som er fullført og hvor mange oppgaver som gjenstår.

Den siste kategorien er for den detaljerte oppgavelisten. Denne listen viser hele oppgavelisten.
Du kan filtrere listen over oppgaver på flere måter. Klikk **Rediger oppgave** for å endre statusen til en oppgave eller tilordne en oppgave. Klikk **vedlegg** for å vise vedlegg for en oppgave.

Oppgavenavnet er en hyperkobling til siden brukeren må gå til for å fullføre arbeidet. Du kan angi denne hyperkoblingen ved å bruke feltet **Menyelementnavn** når du redigerer eller oppretter en oppgave fra skjemaet **Konfigurer datavalideringsprosjekt**.

Du kan knytte filer, notater, bilder og nettadresser til en oppgave ved hjelp av handlingen **Vedlegg**. Du kan for eksempel legge ved en rapportfil som ble skrevet ut for en oppgave. Et ikon vises i **Vedlegg**-kolonnen for oppgaven hvis det finnes et vedlegg.

Alternativet **Fullført av** fylles automatisk ut når aktiviteten er fullført, med navnet på arbeideren som fullført oppgaven. Når en oppgave er merket som fullført, oppdateres feltet **Fullføringsdato** automatisk til gjeldende dato og klokkeslett.

## <a name="configure-data-validation-project-page"></a>Konfigurere datavalideringsprosjektsiden

Før du kan bruke arbeidsområdet **Sjekkliste for datavalidering**, må du konfigurere prosessen ved hjelp av siden **Konfigurer datavalideringsprosjekt**. (Klikk **Arbeidsområder** \> **Sjekkliste for datavalidering** \> **Konfigurer datavalideringsprosjekt**.)

## <a name="task-areas"></a>Oppgaveområder

Du kan bruke oppgaveområder til å gruppere datavalideringsoppgaver i logiske eierskapsområder i organisasjonen. Leverandører, Kunder eller Økonomimodul kan for eksempel brukes som oppgaveområder.

**Menyelementnavnet** er tilknyttet arbeidsinnsatsen for oppgaven og kan brukes til å gå direkte til den tilknyttede siden fra oppgavekoblingen i arbeidsområdet. En datavalideringsoppgave som skal kjøre **aldersfordelingsrapporten** for leverandører som kan kobles til  **aldersfordelingsrapport**-siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]