---
title: Integrering av Microsoft Project-klient
description: Planlegging og vedlikehold av en prosjektplan kan være komplisert, slik at prosjektledere må bruke verktøy som hjelper dem med denne oppgaven. Integrasjon med Microsoft Project-klienten gir støtte for å åpne og behandle en arbeidsnedbrytningsstruktur for prosjekt.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 610990612d5fb38025bf39cc648d0c9572da37b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174972"
---
# <a name="microsoft-project-client-integration"></a>Integrering av Microsoft Project-klient

[!include [banner](../includes/banner.md)]

Planlegging og vedlikehold av en prosjektplan kan være komplisert, slik at prosjektledere må bruke verktøy som hjelper dem med denne oppgaven. Integrasjon med Microsoft Project-klienten gir støtte for å åpne og behandle en arbeidsnedbrytningsstruktur for prosjekt. Prosjektlederen kan publisere endringer tilbake til arbeidsnedbrytningsstrukturen for prosjekt i Dynamics 365 Finance.

> [!NOTE]
> Hvis du bruker juli-oppdateringen (versjon 10.0.4), må du installere KB 4054797 og 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurere Microsoft Project-klienttillegget
For å aktivere integrasjonen med Microsoft Project-klienten, må et Microsoft Dynamics 365-tillegg installeres på brukerens Microsoft Project-programklient. Dette gjøres ved å åpne **Prosjektstyringsarbeidsområdet**.

•   Klikk på **Konfigurer prosjektklienttillegget** fra **Koblinger** > **Oppsett**-delen i arbeidsområdet.

•   Klikk på **Åpne** og deretter **Kjør** når du blir spurt.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Åpne og redigere en eksisterende utkastarbeidsnedbrytningsstruktur i Microsoft Project-klienten
Hvis et prosjekt i Dynamics 365 Finance allerede har opprettet en arbeidsnedbrytningsstruktur, kan arbeidsnedbrytningsstrukturen åpnes i Microsoft Project Client-programmet hvis arbeidsnedbrytningsstrukturen har statusen Utkast. Hvis du vil åpne fra **Prosjekt**-siden, klikker du **Åpne i Microsoft Project**-koblingen fra **Plan**-kategorien. Denne siden kan også åpnes fra Microsoft Project-klientprogrammet ved å klikke **Åpne** i **Microsoft Dynamics 365**-kategorien. Velg **Juridisk enhet** og **Prosjekt** fra listen.

> [!NOTE]
> Hvis du bruker Internet Explorer som nettleser, må du klikke **Lagre** for å åpne manuelt fra plasseringen som filen er lastet ned til. Eller klikk **Lagre og åpne** for å åpne filen i Microsoft Project-klienten. Ikke endre navn på filnavnet når du lagrer.

Før du gjør endringer i filen ved hjelp av Microsoft Project Client, må du sjekke den ut. Klikk **Sjekk ut** i **Microsoft Dynamics 365**-kategorien. Dette hindrer andre brukere i å redigere arbeidsnedbrytningsstrukturen innenfra Finance samtidig. For å publisere arbeidsnedbrytningsstrukturen når du har fullført alle endringer, klikker du på **Sjekk inn** i **Microsoft Dynamics 365**-kategorien.

Hvis en prosjektgruppe allerede er lagt til prosjektet i Finance, fylles ressurslisten ut med gruppemedlemmene. Hvis en prosjektgruppe ennå ikke er lagt til i prosjektet, kan du velge ressurser og bygge teamet i Microsoft Project-klienten ved å klikke **Ressurser**-knappen i **Microsoft Dynamics 365**-kategorien. 

Følgende data blir synkronisert tilbake til Finance som en del av innsjekkingen som pågår:

•   Oppgavenavn

•   Startdato

•   Avslutningsdato

•   Foregående aktiviteter

•   Ressursnavn

•   Kategori

•   Ressurskategori

•   Arbeidstimer

•   Merknader

•   Prioritet

> [!NOTE]
> Hvis du legger til andre kolonner i Microsoft Project-klientfilen, vil de ikke bli lagret i filen, og ikke vises når filen åpnes på nytt.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Opprette arbeidsnedbrytningsstrukturen for et eksisterende prosjekt ved hjelp av Microsoft Project-klienten
Når du skal opprette en ny arbeidsnedbrytningsstruktur ved hjelp av Microsoft Project-klienten, gjør du følgende:


1.  Åpne Microsoft Project-klienten.

2.  I kategorien **Microsoft Dynamics 365** klikker du **Åpne**.

3.  Velg **Juridisk enhet** for prosjektet.

4.  Velg **prosjektet**.

5.  Klikk på **Sjekk ut** i kategorien **Microsoft Dynamics 365**.

6.  Når du er klar til å publisere til Finance, klikker du på **Sjekk inn** i kategorien **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Erstatt den eksisterende arbeidsnedbrytningsstrukturen for et eksisterende prosjekt ved hjelp av Microsoft Project-klienten
Hvis du vil opprette en ny arbeidsnedbrytningsstruktur ved hjelp av Microsoft Project-klienten og erstatte en eksisterende arbeidsnedbrytningsstruktur for et eksisterende prosjekt, gjør du følgende:

1.  Åpne Microsoft Project-klienten.

2.  Opprett tidsplanen i Microsoft Project-klienten.

3.  I **Microsoft Dynamics 365**-kategorien klikker du **Lagre endringer** > **Erstatt eksisterende prosjekt**.

4.  Velg **Juridisk enhet** for prosjektet.

5.  Velg **prosjektet**.

6.  Klikk **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Opprette et nytt prosjekt fra Microsoft Project-klienten


1.  Åpne Microsoft Project-klienten.

2.  Opprett tidsplanen i Microsoft Project-klienten.

3.  I **Microsoft Dynamics 365**-kategorien klikker du **Lagre endringer** > **Lagre i nytt prosjekt**.

4.  Velg **Juridisk enhet** for prosjektet.

5.  Angi **prosjekt-ID**-en om nødvendig.

6.  Skriv inn **prosjektnavnet**.

7.  Velg **prosjekttype**, **prosjektgruppe** og **prosjektkontrakt-ID**. Du kan eventuelt opprette en ny prosjektkontrakt ved å klikke **Ny**.

8.  Velg **Kalender** som skal brukes for ressurser.

11. Klikk **OK**.
