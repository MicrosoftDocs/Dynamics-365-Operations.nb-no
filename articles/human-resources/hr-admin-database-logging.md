---
title: Konfigurere og administrere databaselogging
description: Du kan spore endringer i tabeller og felt i Dynamics 365 Human Resources med databaselogging.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8faf0be5f094f18b75f2263fa622c9b7f3983274
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899770"
---
# <a name="configure-and-manage-database-logging"></a>Konfigurere og administrere databaselogging


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan spore endringer i tabeller og felt i Dynamics 365 Human Resources med databaselogging. Denne artikkelen beskriver hvordan du gjør følgende:

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
2. Velg **Neste**. 
3. På siden **Tabeller og felt** i veiviseren velger du tabellene og feltene du vil aktivere databaselogging på, og velger **Neste**.

   > [!Note]
   > Databaselogging er ikke tilgjengelig på alle tabeller i Human Resources-databasen. Hvis du velger **Vis alle tabeller** under listen, utvides listen over tabeller og felt som viser alle databasetabeller som det er tilgjengelig databaselogging for, men dette er et delsett av den fullstendige listen over databasetabeller.

4. På siden **Endringstyper** i veiviseren velger du dataoperasjonene du vil spore endringer for hver av tabellene og feltene for, og velger **Neste**. Se tabellen nedenfor hvis du vil ha en beskrivelse av dataoperasjonene som er tilgjengelige for logging.
5. På **Fullfør**-siden kan du se gjennom endringene som blir gjort, og velge **Fullfør**.

| Operasjon | beskrivelse |
| -- | -- |
| Spor nye transaksjoner | Opprett en logg for nye poster som er opprettet i tabellen. |
| Oppdatering | Opprett en logg for oppdateringer av tabellposter, eller oppdateringer til enkeltvis valgte felt i tabellen. Hvis du velger å logge oppdateringer for tabellen, opprettes det en loggpost hver gang det gjøres en oppdatering i et hvilket som helst felt i en hvilken som helst post i tabellen. Hvis du velger å logge oppdateringer for bestemte felt, opprettes det bare en loggpost når det gjøres oppdateringer i disse feltene for tabellposter. |
| Delete | Opprett en logg for poster som er slettet fra tabellen. |
| Gi nøkkel nytt navn | Opprett en loggpost når en tabellnøkkel får nytt navn. |


## <a name="clean-up-database-logs"></a>Rydder opp i databaselogger

Du kan slette hele eller deler av databaseloggene ved hjelp av følgende alternativer:

- Velg alle logger for en bestemt tabell.
- Velg bestemte typer databaselogg.
- Velg dato og klokkeslett for oppretting av logg.

Gjør følgende for å konfigurere opprydding i databaselogg: 

1. Gå til **Systemadministrasjon > Koblinger > Database > Databaselogg**. Velg **Opprydding i logg**.
2. Velg **Filtrer** under overskriften **Poster som skal inkluderes**.
3. Velg metoden som skal brukes til å velge loggene som skal slettes. Angi et av følgende alternativer:

   - Tabell-ID
   - Loggtype
   - Opprettingsdato og -klokkeslett

4. Bruk kategorien **Opprydding i databaselogg** for å bestemme når du vil kjøre loggoppryddingsoppgaven. Som standard er databaselogger tilgjengelige i 30 dager.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
