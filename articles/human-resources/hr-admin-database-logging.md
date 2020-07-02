---
title: Konfigurere og administrere databaselogging
description: Du kan spore endringer i tabeller og felt i Dynamics 365 Human Resources med databaselogging.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443591"
---
# <a name="configure-and-manage-database-logging"></a>Konfigurere og administrere databaselogging

Du kan spore endringer i tabeller og felt i Dynamics 365 Human Resources med databaselogging. Dette emnet beskriver hvordan du gjør følgende:

- Administrerer sikkerhet og ytelse for databaselogging
- Definer databaselogging
- Rydder opp i databaselogger

## <a name="overview-of-database-logging"></a>Oversikt over databaselogging

Databaselogging sporer spesifikke endringer i Microsoft Dynamics 365 Human Resources-tabeller og -felt. Disse endringene omfatter innsetting, oppdatering eller sletting. Databaselogging lagrer en post over endringer i tabeller eller felt i databaseloggtabellen.

Firmaets bruk av databaselogging omfatter:

- Opprett en overvåkingsregistrering for endringer i bestemte tabeller som inneholder sensitiv informasjon.
- Spore enkelttransaksjoner. Databaselogging er ikke ment for sporing av automatiserte transaksjoner som kjøres i satsvise jobber.

## <a name="security-for-database-logging"></a>Sikkerhet for databaselogging

Databaselogger kan inneholde sensitive data. Begrens tilgangen til å bare inkludere sikkerhetsroller som trenger tilgang til loggdataene.

## <a name="database-logging-and-performance"></a>Databaselogging og ytelse

Selv om det er verdifullt fra et forretningsperspektiv, kan databaselogging være dyrt i ressursbruk og -behandling. Ytelseimplikasjonene for databaselogging omfatter følgende:

- Databaseloggtabellen kan vokse raskt og føre til en økning i størrelsen på databasen. Veksten avhenger av hvor mye loggdata du bestemmer deg for å beholde. Som standard beholder databaseloggtabellen bare 30 dager med loggdata. 

- Databaselogging kan påvirke lange automatiserte prosesser negativt, for eksempel lange dataimporter.

### <a name="best-practices"></a>Anbefalte fremgangsmåter

For å forbedre ytelsen begrenses loggoppføringer ved å velge bestemte felt du skal logge i stedet for hele tabeller. For å opprettholde generell ytelse er databaselogging begrenset til 20 tabeller.

> [!NOTE]
> Bare oppdateringer kan logges for individuelle felt.

## <a name="set-up-database-logging"></a>Definer databaselogging

Du kan bruke veiviseren **Registrerer databaseendringer** til å konfigurere databaselogging. Veiviseren gir en fleksibel måte å konfigurere logging for tabeller eller felt på.

1. Gå til **Systemadministrasjon > Koblinger > Database > Oppsett av databaselogg**. Velg **Ny** for å starte veiviseren **Registrerer databaseendringer**.
2. Fullfør veiviseren.

## <a name="clean-up-database-logs"></a>Rydder opp i databaselogger

Du kan slette hele eller deler av databaseloggene ved hjelp av følgende alternativer:

- Velg alle logger for en bestemt tabell.
- Velg bestemte typer databaselogg.
- Velg dato og klokkeslett for oppretting av logg.

Gjør følgende for å konfigurere opprydding i databaselogg: 

1. Gå til **Systemadministrasjon > Koblinger > Database > Databaselogg**. Velg **Opprydding i logg**.

2. Velg en metode for valg av logger du vil slette, ved å angi ett av følgende alternativer:

   - Tabell-ID
   - Loggtype
   - Opprettingsdato og -klokkeslett

3. Bruk kategorien **Opprydding i databaselogg** for å bestemme når du vil kjøre loggoppryddingsoppgaven. Som standard er databaselogger tilgjengelige i 30 dager.
