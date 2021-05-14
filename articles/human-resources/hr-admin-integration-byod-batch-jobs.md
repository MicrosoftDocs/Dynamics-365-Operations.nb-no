---
title: Optimalisere planlagte, satsvise BYOD-jobber
description: Dette emnet forklarer hvordan du optimaliserer ytelsen når du bruker funksjonen for å Vise din egen database (BYOD) sammen med Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 0c29d68b29475c2c7040d06e60f7624c49a42002
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951938"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>Optimalisere planlagte, satsvise BYOD-jobber

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet forklarer hvordan du optimaliserer ytelsen når du bruker funksjonen for å Vise din egen database (BYOD). Hvis du vil ha mer informasjon om BYOD, kan du se [Vise din egen database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Ytelseshensyn for dataeksport

Etter at enheter er publisert i måldatabasen, kan du bruke eksportfunksjonen i **Databehandling**-området til å flytte data. Med Eksport-funksjonen kan du definere en dataflyttingsjobb som inneholder én eller flere enheter. Hvis du vil ha mer informasjon om dataeksport, se [Oversikt over dataimport- og -eksportjobber](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Du kan bruke **Eksport**-siden til å eksportere data til forskjellige måldataformater, for eksempel en CSV-fil (kommadelte verdier). Denne siden støtter også SQL-databaser som et annet mål.

Du kan opprette et dataprosjekt som har flere enheter og bruke en satsvis jobb til å planlegge at dataprosjektet skal kjøres. Hvis du velger alternativet for å **eksportere i bunke**, kan du planlegge at dataeksporten skal kjøre med jevne mellomrom.

Du må være forsiktig når du legger til flere enheter i et eksportprosjekt, for å ta vare på den generelle påliteligheten til BYOD-eksporten. Når du skal bestemme antallet enheter som skal legges til det samme prosjektet, kan du vurdere følgende parametere:

- Enhetens kompleksitet
- Det forventede datavolumet per enhet
- Den totale tiden som kreves for å fullføre eksporten på jobbnivå

Du får best ytelse ved å unngå å legge til hundrevis av enheter til ett enkelt prosjekt. Det anbefales at du oppretter flere jobber, og hver av disse inneholder færre enheter.

## <a name="scheduling-byod-batch-jobs"></a>Planlegge satsvise BYOD-jobber

For å redusere innvirkningen på brukere av Microsoft Dynamics 365 Human Resources må du kjøre satsvise BYOD-jobber om natten eller etter arbeidstid. Pass på at du kontrollerer tidssonen for gjentakende satsvise jobber. Noen satsvise jobber kan bruke Stillehavskysten (normaltid).

Du kan unngå ytelsesproblemer ved å ta hensyn til følgende faktorer når du konfigurerer planleggingsfrekvensen for satsvise BYOD-jobber:

- Tiden som kreves for å fullføre hver satsvise jobb
- Forretningsbehovet for dataene i BYOD

Angi frekvensen for hver satsvise jobb til en verdi som sikrer at jobben kan fullføres før den neste planlagte kjøringen. Unngå å kjøre flere jobber parallelt, fordi denne fremgangsmåten kan ha negativ innvirkning på ytelsen til Human Resources.

For best mulig ytelse bør du alltid bruke alternativet for å **eksportere i bunke** på siden **Eksporter** til å planlegge satsvise BYOD-jobber. Unngå planlegging av gjentakende eksporter ved å gå til **Behandle \> Behandle gjentakende datajobber**.

## <a name="incremental-export"></a>Trinnvis eksport

Når du legger til en enhet for dataeksport, kan du enten utføre en trinnvis push (eksport) eller en fullstendig push. Et fullstendig push sletter alle eksisterende poster fra en enhet i BYOD-databasen. Deretter settes det gjeldende settet med poster inn fra Human Resources-enheten.

Hvis du vil utføre en trinnvis push, må du aktivere endringssporing for hver enhet på **Enheter**-siden. Hvis du vil ha mer informasjon, kan du se [Aktivere endringssporing for enheter](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

Hvis du velger en trinnvis push, er den første pushen alltid en fullstendig push. SQL sporer endringer fra denne første fullstendige pushen. Når en ny post settes inn, eller når en post oppdateres eller slettes, gjenspeiles endringen i målenheten.

## <a name="time-outs"></a>Tidsavbrudd

Her er standard tidsavbrudd for BYOD-eksporter:

- Ti minutter for avkortingsoperasjoner
- Én time for masseinnsettingsoperasjoner

Når volumer er høye, kan det hende at disse tidsavbruddsinnstillingene ikke er tilstrekkelige. Hvis du vil oppdatere dem, går du til **Dataadministrasjon \> Rammeverkparametere \> Vise din egen database**. Dette tidsavbruddet er firmaspesifikt og må defineres separat for hvert firma.

## <a name="known-limitations"></a>Kjente begrensninger

BYOD-funksjonen har følgende begrensninger:

- Det skal ikke være noen aktive låser i databasen under synkronisering. Aktive låser kan føre til langsomme skrivinger eller til og med mislykket dataeksport til Azure SQL-databasen.
- Du kan ikke eksportere sammensatte enheter til din egen database. For øyeblikket støttes ikke sammensatte enheter. Du må eksportere enkeltenheter som utgjør den sammensatte enheten. Du kan imidlertid eksportere begge enhetene i samme dataprosjekt.
- Enheter som ikke har unike nøkler, kan ikke eksporteres ved hjelp av trinnvis push. Du vil kanskje oppleve denne begrensningen særlig når du prøver å gradvis eksportere poster fra noen få ferdiglagde enheter. Fordi disse enhetene ble utformet for å aktivere import av data, har de ikke en unik nøkkel.

## <a name="troubleshooting"></a>Feilsøking

### <a name="incremental-push-doesnt-work-correctly"></a>Trinnvis push fungerer ikke riktig

**Problem:** Når en full push forekommer for en enhet, ser du et stort sett med poster i BYOD når du bruker en **select**-setning. Når du utfører et trinnvis push, kan du imidlertid bare se noen få poster i BYOD. Det ser ut som om den trinnvise pushen slettet alle poster og bare la til de endrede postene i BYOD.

**Løsning:** Tabellene for SQL-endringssporing er kanskje ikke i forventet tilstand. I noen tilfeller av denne typen anbefaler vi at du deaktiverer sporing av endringer for enheten og deretter slår den på igjen. Hvis du vil ha mer informasjon, kan du se [Aktivere endringssporing for enheter](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Oppsamlingstabeller tømmes ikke

**Problem:** Når du bruker oppsamling for prosjektet, tømmes ikke oppsamlingstabellene på riktig måte. Dataene i tabellene fortsetter derfor å vokse, noe som fører til ytelsesproblemer.

**Løsning:** Sju dager med historikk vedlikeholdes i oppsamlingstabellene. Historiske data som er eldre enn sju dager, tømmes automatisk fra oppsamlingstabellene ved hjelp av den satsvise jobben **Importer/eksporter opprydding i oppsamling**, Hvis denne jobben stopper, blir ikke tabellene tømt riktig. Hvis du starter denne satsvise jobben på nytt, fortsetter prosessen, slik at oppsamlingstabellene automatisk blir tømt.

## <a name="see-also"></a>Se også

[Oversikt over databehandling](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Vise din egen database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Oversikt over dataimport- og -eksportjobber](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Aktivere endringssporing for enheter](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
