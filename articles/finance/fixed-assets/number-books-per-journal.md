---
title: Antall tablåer per journal
description: Dette emnet beskriver relasjonen mellom journalene og aktivatablåene når du oppretter en anleggsmiddelanskaffelse eller et avskrivningsforslag via en satsvis jobb. Du kan definere maksimalt antall tablåer som skal tas med for hver anskaffelse og for avskrivning.
author: moaamer
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e948b4353d0216f1e09019a98319e343bd535861
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822039"
---
# <a name="number-of-books-per-journal"></a>Antall tablåer per journal

[!include [banner](../includes/banner.md)]

Dette emnet beskriver relasjonen mellom journalene og aktivatablåene når du oppretter en anleggsmiddelanskaffelse eller et avskrivningsforslag via en satsvis jobb. Du kan definere det maksimale antallet tablåer som er inkludert for hver anskaffelse og avskrivning ved hjelp av feltene i delen **Antall tablåer per journal** i kategorien **Generelt** på siden **Parametere for anleggsmidler** (**Anleggsmidler \> Oppsett \> Parametere for anleggsmidler**). Med disse feltene kan du fordele antall anleggsmiddeltablåer per anskaffelsesjournal og avskrivningsjournal.

For et anskaffelsesforslag er standardverdien minst 10 000 tablåer. For et avskrivningsforslag er standardverdien minst 2000 tablåer.

Hvis det for eksempel er 4 000 anleggsmidler, og to tablåer er knyttet til hvert anleggsmiddel, posteres ett tablå til det gjeldende laget, og det andre tablået posteres til skattelaget. Hvis du anskaffer 4 000 anleggsmidler ved hjelp av satsvis behandling, vil den satsvise jobben som oppretter en anskaffelsesjournal for anleggsmidler, inneholde 4 000 aktivatablåer.

> [!NOTE]
> Journalen som opprettes, vil fortsatt bli brukt til den satsvise jobben er fullført.
>
> De avledede tablåene er ikke inkludert i det maksimale antall tabler per journal.

Du kan bruke satsvis behandling til å kjøre avskrivning for samme settet med anskaffede aktivaer. En satsvis jobb oppretter for eksempel to avskrivningsjournaler, som hver består av 2 000 aktivatablåer. Den første journalen vil inneholde tablåer som er knyttet til anleggsmidlene som er nummerert fra 1 til 2 000. Den andre journalen vil deretter inneholde tablåer som er knyttet til anleggsmidlene som er nummerert fra 2001 til og med 4000.

Jobben for satsvis behandling utelukker lukkede tablåer. I en satsvis jobb for avskrivning, er for eksempel 10 i de første 2 000 tablåene lukket. I dette tilfellet vil den første journalen inneholde tablåer som er knyttet til anleggsmidlene som er nummerert fra 1 til og med 2011. Den andre journalen vil deretter inneholde tablåer som er knyttet til anleggsmidlene som er nummerert fra 2012 til og med 4000.

> [!NOTE]
> Hvis du har ID-er for anleggsmidler med forskjellige skilletegn (for eksempel – eller /), og du oppretter anleggsmiddeltransaksjoner i satsvise jobber, må du kjøre en egen satsvis jobb for hver type skilletegn. Systemet kan ikke behandle forskjellige skilletegn innenfor den samme satsvise jobben.

Grensen for antall tabler brukes hvis dupliserte aktiva-IDer ikke finnes i samme journal. Hvis aktiva-IDen er den samme som tablå-IDen, kan imidlertid antall tablåer per journal overstiges for å beholde aktiva-IDen i samme journal.

Det finnes for eksempel 5 001 anleggsmiddel-IDer, tre tablåer er knyttet til hver anleggsmiddel-ID, og hvert anleggsmiddeltablå posteres til det samme posteringslaget. Du kjører avskrivning for tre påfølgende måneder, uten sammendrag.  Avskrivningsjournalen blir opprettet ved hjelp av en satsvis jobb, og systemet vil opprette sju journaler som har 667 anleggsmiddel-IDer og tre tablåer for hver anleggsmiddel-ID. Resultatet vil være 2 001 tablåer. I løpet av tre måneder vil det derfor være 6 003 journallinjer for å vedlikeholde de samme anleggsmiddel-IDene i samme journal. Systemet vil også opprette én journal som har 332 anleggsmiddel-IDer og tre tablåer for hver anleggsmiddel-ID. I løpet av tre måneder vil det være 2 988 linjer.

> [!NOTE] 
> Hvis parameteren **Summer avskrivning** er aktivert når du oppretter et avskrivningsforslag, har ikke verdien i feltet **Antall tablåer per journal – Avskrivningsforslag** noen virkning. I dette tilfellet er antallet tablåer per journal 6000, som er den interne definerte grensen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
