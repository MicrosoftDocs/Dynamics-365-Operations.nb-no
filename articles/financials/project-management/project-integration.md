---
title: Integrering av Microsoft Project-klient
description: "Planlegging og vedlikehold av en prosjektplan kan være komplisert, slik at prosjektledere må bruke verktøy som hjelper dem med denne oppgaven. Integrasjon med Microsoft Project-klienten gir støtte for å åpne og behandle en arbeidsnedbrytningsstruktur for prosjekt."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a>Integrering av Microsoft Project-klient

[!include [banner](../includes/banner.md)]

Planlegging og vedlikehold av en prosjektplan kan være komplisert, slik at prosjektledere må bruke verktøy som hjelper dem med denne oppgaven. Integrasjon med Microsoft Project-klienten gir støtte for å åpne og behandle en arbeidsnedbrytningsstruktur for prosjekt. Prosjektlederen kan publisere endringer tilbake til arbeidsnedbrytningsstrukturen for prosjekt i Finance and Operations.

> [!NOTE]
> Hvis du bruker juli-oppdateringen for Microsoft Dynamics 365 for Finance and Operations, må du installere KB 4054797 og 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurere Microsoft Project-klienttillegget
For å aktivere integrasjonen med Microsoft Project-klienten, kreves det et Microsoft Dynamics 365-tillegg installert på brukerens Microsoft Project-programklient. Dette gjøres ved å åpne **Prosjektstyringsarbeidsområdet**.

•   Klikk på **Konfigurer prosjektklienttillegget** fra **Koblinger** > **Oppsett**-delen i arbeidsområdet.

•   Klikk på **Åpne** og deretter **Kjør** når du blir spurt.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Åpne og redigere en eksisterende utkastarbeidsnedbrytningsstruktur i Microsoft Project-klienten
Hvis et prosjekt i Finance and Operations allerede har opprettet en arbeidsnedbrytningsstruktur, kan arbeidsnedbrytningsstrukturen åpnes i Microsoft Project-klientprogrammet hvis arbeidsnedbrytningsstrukturen har statusen Utkast. Hvis du vil åpne fra **Prosjekt**-siden, klikker du **Åpne i Microsoft Project**-koblingen fra **Plan**-kategorien. Denne siden kan også åpnes fra Microsoft Project-klientprogrammet ved å klikke **Åpne** i **Microsoft Dynamics 365**-kategorien. Velg **Juridisk enhet** og **Prosjekt** fra listen.

> [!NOTE]
> Hvis du bruker Internet Explorer som nettleser, må du klikke **Lagre** for å åpne manuelt fra plasseringen som filen er lastet ned til. Eller klikk **Lagre og åpne** for å åpne filen i Microsoft Project-klienten. Ikke endre navn på filnavnet når du lagrer.

Før du gjør endringer i filen ved hjelp av Microsoft Project-klienten, må du sjekke den ut. Klikk **Sjekk ut** i **Microsoft Dynamics 365**-kategorien. Dette hindrer andre brukere i å redigere arbeidsnedbrytningsstrukturen innenfra Finance and Operations samtidig. For å publisere arbeidsnedbrytningsstrukturen når du har fullført alle endringer, klikker du på **Sjekk inn i** **Microsoft Dynamics 365**-kategorien.

Hvis en prosjektgruppe allerede er lagt til prosjektet i Finance and Operations, fylles ressurslisten ut med gruppemedlemmene. Hvis en prosjektgruppe ennå ikke er lagt til i prosjektet, kan du velge ressurser og bygge teamet i Microsoft Project-klienten ved å klikke **Ressurser**-knappen i **Microsoft Dynamics 365**-kategorien. 

Følgende data blir synkronisert tilbake til Finance and Operations som en del av sjekken som pågår:

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

2.  I **Microsoft Dynamics 365**-kategorien, klikk **Åpne**.

3.  Velg **Juridisk enhet** for prosjektet.

4.  Velg **prosjektet**.

5.  Klikk på **Sjekk ut** i **Microsoft Dynamics 365**-kategorien.

6.  Når du er klar til å publisere til Finance and Operations, klikker du **Sjekk inn** i **Microsoft Dynamics 365**-kategorien.

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

