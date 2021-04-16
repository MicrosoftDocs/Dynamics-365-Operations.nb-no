---
title: Dimensjonshierarki
description: Dette emnet gir informasjon om dimensjonshierarkier. Du bruker et dimensjonshierarki for å definere rapporteringsstruktur, kostnadspolicyer og sikkerhetsoppsett i Kostnadsregnskap.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fdf280031e2ad2356a1a2ef3bba75d1f74c8e4de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810180"
---
# <a name="dimension-hierarchy"></a>Dimensjonshierarki

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om dimensjonshierarkier. Du bruker et dimensjonshierarki for å definere rapporteringsstruktur, kostnadspolicyer og sikkerhetsoppsett i Kostnadsregnskap.  

## <a name="overview"></a>Oversikt

Dimensjonshierarkier brukes på forskjellige steder i Kostnadregnskap. Et dimensjonshierarki lar deg definere følgende informasjon:

-  Rapporteringsstrukturen som passer inn i organisasjonens krav
-  Kostnadspolicyer
-  Sikkerhetsoppsettet

Her er et eksempel på et dimensjonshierarki.

![Eksempel på et dimensjonshierarki](./media/dimension-hierarchy.png)

Du kan opprette et dimensjonshierarki for følgende typer dimensjoner:

-  Kostnadselementdimensjoner
-  Kostnadsobjektdimensjoner
-  Statistiske dimensjoner

> [!NOTE]
> - Du kan opprette flere dimensjonshierarkier for samme dimensjon hvis det kreves forskjellige perspektiver.
> - Et dimensjonshierarki kan knyttes til bare én dimensjon.
> - Et dimensjonshierarki kan ha ubegrenset antall nivåer i strukturen. Alle nivåene blir tilgjengelig i arbeidsområdet **Kostnadskontroll**. Når du bruker Microsoft Excel eller Microsoft Power BI for rapporteringsformål, eksporteres bare de 15 første nivåene i dimensjonshierarkiet. Denne begrensningen finnes fordi både Excel og Power BI krever et fast skjema.
> - Et dimensjonshierarki ikke datoeffektivt. Derfor lagres endringer i et dimensjonshierarki umiddelbart i posten, og du kan ikke sammenligne før- og etter-datoen.

## <a name="dimension-hierarchy-type"></a>Dimensjonshierarkistruktur

Når du oppretter et nytt dimensjonshierarki, må du velge en hierarkitype. Gå til **kostnadsregnskap** > **dimensjoner** > **dimensjonshierarkier**. Klikk **Ny**, og velg en dimensjonshierakitype. Du kan velge enten **Hierarki for dimensjonskategorisering** eller **Hierarki for dimensjonsklassifisering**.

### <a name="dimension-categorization-hierarchy"></a>Hierarki for dimensjonskategorisering

**Hierarki for dimensjonskategorisering** brukes til rapporteringsformål. Det støtter bare kostnadselementdimensjonene. Når du velger denne typen, gjelder følgende regler:

-  Et dimensjonsmedlem kan tilknyttes mer enn én gang i hierarkistrukturen.
-  Du kan plassere et dimensjonsmedlem for kostnadselement i forskjellige noder ved å tilordne et kostnadselement til bladnoden.

### <a name="dimension-classification-hierarchy"></a>Hierarki for dimensjonsklassifisering

**Hierarki for dimensjonklassifisering** brukes til å definere regler og til rapporteringsformål. Det støtter alle dimensjoner, for eksempel kostnadsobjekter, kostnadselementer og statistiske dimensjoner. Når du velger denne typen, kan et dimensjonsmedlem bare tilknyttes én gang i hierarkistrukturen.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Opprette og vedlikeholde et dimensjonshierarki

Et dimensjonshierarki opprettes som en trestruktur med node- og bladnoderelasjoner.

-  En node kan ha 1:_n_ undernoder.
-  En node kan ikke ha både undernoder og bladnoder tilordnet.
-  Du kan bare tilordne en bladnode på det laveste nivået i hierarkiet.

### <a name="example"></a>Eksempel

Et lite firma har følgende organisasjonsstruktur, der finans og personale er avdelinger under administrasjon, mens montering og pakking er avdelinger under produksjon.

![Eksempel på en organisasjonsstruktur](./media/dimension-hierarchy-org.png)

En kostnadsobjektdimensjon representerer alle kostsentrene i organisasjonen.

- Kostnadsobjektdimensjon
    - Kostsentre

Kostnadsobjektdimensjonen som representerer alle kostsentrene, kan defineres som vist her.

| Kostsentre | Beskrivelse |
|--------------|-------------|
| CC001        | Personale          |
| CC002        | Finans     |
| CC003        | Mva         |
| CC007        | AR/AP       |
| CC005        | Samling    |
| CC006        | Innpakning   |

En kostnadselementdimensjon representerer alle kostnadselementene i organisasjonen.

- Kostnadselementdimensjon
    - Kostnadselementer

Kostnadselementdimensjonen som representerer alle kostnadselementene, kan defineres som vist her.

| Kostnadselementer | Beskrivelse |
|---------------|-------------|
| 10001         | Elektrisitet |
| 10010         | Rengjøring    |
| 10011         | Oppvarming     |
| 40001         | Vareforbruk        |

Et dimensjonshierarki som oppfyller organisasjonens rapporteringskrav, kan defineres som vist her.

**Detaljer for dimensjonshierarki**

| Dimensjonshierarkinavn | Dimensjon    | Navn på dimensjonshierarkitype      | Hierarki for tilgangsliste |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisasjon             | Kostsentre | Hierarki for dimensjonsklassifisering | Ingen                    |

Dimensjonshierarkiet for rapportering kan defineres som vist her.

**Dimensjonsmedlemsområder**

|   Noder           |   Fra dimensjonsmedlem   |   Til dimensjonsmedlem   |
|-------------------|---------------------------|-------------------------|
| Organisasjon      |                           |                         |
| &nbsp;&nbsp;Administrator         |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personale        | CC001                     | CC001                   |
| &nbsp;&nbsp;Produksjon    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Innpakning | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Samling  | CC006                     | CC006                   |

Et dimensjonshierarki som oppfyller organisasjonens rapporteringskrav, kan defineres som vist her.

**Detaljer for dimensjonshierarki**

| Dimensjonshierarkinavn | Dimensjon     | Navn på dimensjonshierarkitype      |
|--------------------------|---------------|------------------------------------|
| Kostnadsatferd            | Kostnadselementer | Hierarki for dimensjonsklassifisering |

Dimensjonshierarkiet for policyen kan defineres som vist her.

**Dimensjonsmedlemsområder**

|   Noder           |   Fra dimensjonsmedlem   |   Til dimensjonsmedlem   |
|-------------------|---------------------------|-------------------------|
| Kostnadsatferd     |                           |                         |
| &nbsp;&nbsp;Fast kostnad    | 10001                     | 10011                   |
| &nbsp;&nbsp;Variabel kostnad | 40001                     | 40010                   |

> [!NOTE]
> Under **Dimensjonsmedlemsområder** kan en node inneholde 1:_n_ dimensionsmedlemsområder. Du kan sette inn dimensjonsmedlems-ID-er som ennå ikke finnes som dimensjonsmedlemmer. Denne fremgangsmåten gjør hierarkiet fleksibelt for fremtiden.  

### <a name="copy-a-hierarchy"></a>Kopiere et hierarki

Du kan kopiere et gjeldende dimensjonshierarki som utgangspunkt for et nytt dimensjonshierarki. Denne fremgangsmåten kan være nyttig hvis du vil sammenligne de tidligere dimensjonshierarkiene med det nye dimensjonshierarkiet.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Endre rekkefølgen på nodene i et hierarki

Du kan flytte en node opp og ned i det gjeldende nivået i strukturen. På denne måten kan du endre rekkefølgen på nodene for rapportering i **kostnadskontroll**-arbeidsområdet.

Du kan flytte en node til en ny plassering i hierarkiet ved å velge målnoden. Du kan flytte en node på to måter:

- **Flytt under** – Flytt den valgte noden fra gjeldende plassering i hierarkiet, og sett den **under** den valgte målnoden.
- **Flytt etter** – Flytt den valgte noden fra gjeldende plassering i hierarkiet, og sett den **etter** den valgte målnoden på dens nivå i hierarkiet.

> [!NOTE] 
> Rekkefølgen på nodene beholdes ikke når du eksporterer data til Excel eller Power BI, fordi disse verktøyene bruker alfanumerisk sorteringsrekkefølge som standard. Du må manuelt endre rekkefølgen.

## <a name="define-dimension-hierarchies-for-reporting"></a>Definere dimensjonshierarkier for rapportering

Dimensjonshierarkier er viktig for rapportering. De lar deg definere den bestemte strukturen som passer inn i den enkelte organisasjonen. Med aggregeringene som gjøres på nodenivå i dimensjonshierarkiet, kan interessenter på alle nivåer i organisasjonen se data på et hvilket som helst nivå.

Dimensjonshierarkier er tilgjengelige i de følgende rapporteringsverktøy. Denne fremgangsmåten hjelper med å sikre konsekvens i rapporteringsstrukturen.

- Arbeidsområdet **Kostnadskontroll** (klient):

    - Styres av konfigurasjon.

- Arbeidsområde for **kostnadskontroll** (mobilapp):

    - Styres av konfigurasjon.

- Excel

    - Gir mulighet til å velge bestemte dimensjonshierarkier per eksportdefinisjon:

        - Ett dimensjonshierarki for kostnadselement (obligatorisk)
        - Ett dimensjonshierarki for kostnadsobjekt (valgfritt)
        - Ett statistisk dimensjonshierarki (valgfritt)

- Power BI:

    - Alle dimensjonshierarkier er tilgjengelige.
    
Hvis du oppretter rapporter ved hjelp av Excel eller Power BI, eksporteres bare de 15 første nivåene i dimensjonshierarkiene. Denne begrensningen finnes det kreves et fast skjema i Excel og Power BI. Hvis et hierarki har mer enn 15 nivåer, blir ikke ytterligere nivåer eksportert. Normalisert tabellen inneholder en post for hvert dimensjonsmedlem i hierarkiet. Derfor forekommer automatisk aggregering. Denne atferden gjør at saldoene i alle de 15 tilgjengelige nivåene i hierarkiet, fremdeles er korrekt.

Følgende eksempel viser hvordan et dimensjonshierarki kan se ut i rapporteringsstrukturen.

| Dimensjonshierarki for kostnadsobjekt – nivå 1 | Dimensjonshierarki for kostnadsobjekt – nivå 2 | Dimensjonshierarki for kostnadsobjekt – nivå 3 | Dimensjonshierarki for kostnadsobjekt – nivå 4 | Dimensjonshierarki for kostnadsobjekt – nivå 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organisasjon                              | Administrator                                     | Finans                                   | CC002                                     |                                            |
| Organisasjon                              | Administrator                                     | Finans                                   | CC003                                     |                                            |
| Organisasjon                              | Administrator                                     | Finans                                   | CC007                                     |                                            |
| Organisasjon                              | Administrator                                     | Personale                                        | CC001                                     |                                            |
| Organisasjon                              | Produksjon                                | Innpakning                                 | CC005                                     |                                            |
| Organisasjon                              | Produksjon                                | Samling                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Oppdatere dimensjonshierarkiene som brukes for rapportering 

Over tid må dimensjonshierarkiene som brukes i de nevnte rapporteringsverktøyene, oppdateres. Du kan oppdatere dimensjonshierarkier ved å oppdatere klienten.

- Arbeidsområdet **Kostnadskontroll** (klient):
- Arbeidsområde for **kostnadskontroll** (mobilapp):

Oppdateringer til dimensjonshierarkier blir plukket opp hver 24. time av en hurtigbufret jobb. Når de eksporterte dataene er oppdatert, er de oppdaterte dimensjonshierarkiene tilgjengelige i følgende verktøy:

- Excel
- Power BI

> [!NOTE] 
> Hvis du vil utløse en oppdatering av hurtigbufferen for dimensjonshierarkiet manuelt, kan du opprette en ny eksport til Excel for dimensjonshierarkiet eller -hierarkiene som må oppdateres.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Definere dimensjonshierarkier for kostnadspolicyer

Kostnadsregnskap består av flere policyer der detaljerte regler er definert. Du må definere ett eller flere dimensjonshierarkier for følgende policyer:

- Kostnadsatferd
- Kostnadsdistribusjon
- Kostnadsavregninger
- Opprullet kost

Dimensjonshierarkier gjør det enkelt å opprette regler. For å unngå å opprette regler for hvert dimensjonsmedlem, kan du dra nytte av aggregeringene av dimensjonsmedlemmer som leveres av dimensjonshierarkinivåer. Hvis du har overlappende regler, må du definere bestemte regler som systemet skal ta i betraktning når det beregner administrasjonskostnader.

### <a name="example-define-a-cost-behavior-policy"></a>Eksempel: Definere en policy for kostnadsatferd

En ny policy for kostnadsatferd opprettes, og egnede dimensjonshierarkier tilordnes policyen, som vist her.

**Policy for kostnadsatferd**

| Policynavn   | Dimensjonshierarki for kostnadselement | Dimensjonsobjekt for kostnadselement | Regnskapsvaluta |
|---------------|----------------------------------|---------------------------------|---------------------|
| Kostnadsatferd | Kostnadsatferd                    | Organisasjon                    | USD                 |

**Regler**

| Dimensjonshierarkihode for kostnadselement | Dimensjonshierarkihode for kostnadsobjekt | Fast prosent | Fast beløp | Gyldig fra | Gyldig til |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Fast kostnad                            | Organisasjon                         | 100,00           | 0,00         | 1/1/2017   | Aldri    |
| 10001                                 | Organisasjon                         | 0,00             | 150.00       | 1/1/2017   | Aldri    |
| 10001 (\*)                             | Finans                              |                  | 50,00        | 1/1/2017   | Aldri    |
| Kostnadsatferd eller variabel kostnad (\*\*)   | Organisasjon                         | 0,00             | 0,00         | 1/1/2017   | Aldri    |

\* Noden for variable kostnader er ikke nødvendig. Hvis en kostnad ikke er klassifisert som en fast kostnad, må den være en variabel kostnad.

\*\* En detaljert regel blir opprettet for kombinasjonen av kostnadselementmedlem 10001 og alle kostnadobjektmedlemmer som er samlet under hierarkinivået Finans (CC002, CC003, CC007).

Reglene ovenfor viser fleksibiliteten med dimensjonshierarkier. Ved å definere reglene på høyt nivå, kan du redusere vedlikehold. Du kan definere detaljerte regler slik at de passer til et bestemt forretningsmål.

Hvis dimensjonshierarkier som brukes i reglene, oppdateres bringer oppdateringene automatisk videre i systemet.

Hvis et detaljnivå i reglene ikke lenger er obligatorisk, kan regelen utløpe.

Det er for eksempel ikke lenger nødvendig med en bestemt kostnadsatferdsregel for dimensjonshierarkinoden for kostnadsobjektet Finans. I dette tilfellet klikker du **Avslutt regel** for å la regelen utløpe.

| Dimensjonshierarkihode for kostnadselement | Dimensjonshierarkihode for kostnadsobjekt | Fast prosent | Fast beløp | Gyldig fra | Gyldig til  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Fast kostnad                            | Organisasjon                         | 100,00           | 0,00         | 1/1/2017   | Aldri     |
| 10001                                 | Organisasjon                         | 0,00             | 150,00       | 1/1/2017   | Aldri     |
| 10001                                 | Finans                              |                  | 50,00        | 1/1/2017   | 1/20/2017 |
| Kostnadsatferd eller variabel kostnad        | Organisasjon                         | 0,00             | 0,00         | 1/1/2017   | Aldri     |

En beregning av administrasjonskostnader som kjøres etter 20. januar 2017, vurderer ikke lenger denne regelen.

> [!NOTE] 
> Feltene **Gyldig fra** og **Gyldig til** er datoeffektive og tidseffektive. Du kan la regelen utløpe og kjøre en ny beregning av administrasjonskostnader på samme dag.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Definere dimensjonshierarkier for sikkerhetsoppsett

Kostnadsregnskapsdata skal gjøres tilgjengelig for alle ledere som har ansvar for en rapporteringsenhet. I kostnadsregnskapsterminologien er en rapporteringsenhet representert som et kostnadsobjekt eller et sett med kostnadsobjekter.

Alle ledere vil potensielt kunne få tilgang til svært sensitive forretningsdata, som inntekter og marginer. Det er derfor viktig at du definerer sikkerhet, slik at ledere bare ser dataene som er relevante for dem. For å bidra til å kontrollere datasikkerheten, kan du definere dimensjonshierarkier.

- Bruk av dimensjonshierarkier gjelder bare når dimensjonsverdien som er valgt i dimensjonshierarkireferansen, er en kostnadsobjektdimensjon.
- Bare ett dimensjonshierarki kan aktiveres per kostnadsobjektdimensjon i tilgangslistehierarkiet.

**Detaljer for dimensjonshierarki**

| Dimensjonshierarkinavn | Dimensjon    | Navn på dimensjonshierarkitype      | Hierarki for tilgangsliste |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisasjon             | Kostsentre | Hierarki for dimensjonsklassifisering | **Ja**               |

En ny **Brukere**-hurtigfane er tilgjengelig i hierarkidesigneren. Her kan du sette inn én eller flere bruker-ID-er på hver node i hierarkiet.

**Brukere og dimensjonsmedlemsområder**

|   Noder         |   Bruker-ID        |   Fra-dimensjonsmedlem   |   Til dimensjonsmedlem   |
|-----------------|------------------|---------------------------|-------------------------|
| Organisasjon    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Administrator         | April            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans   | Charlotte           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personale        | Magnus            | CC001                     | CC001                   |
| &nbsp;&nbsp;Produksjon    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Innpakning | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Samling  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Regnskapsførere må tilordnes det øverste nivået i hierarkiet, slik at de kan se alle oppføringene i kostnadsregnskap.

Hvis du vil aktivere tilgangslistehierarkiet og sikkerhetsinnstillingene, kan du gå til **Kostnadsregnskap** > **Oppsett** > **Parametere** > **Generelt**. Velg parameteren **Aktiver visningstilgang for dimensjonsmedlemmer for kostnadsobjekt**.

Innstillingene for hierarkiet for tilgangsliste brukes til å styre dataene som vises på følgende områder:

- Arbeidsområdet **Kostnadskontroll** (klient):

    - Data i skjemaer som brukes til å gå gjennom scenarier

- Arbeidsområde for **kostnadskontroll** (mobilapp):

    - Saldoer i kort

- Power BI:

    - Data som vises i Power BI-visualiseringer
    - Power BI-datavisualiseringer som er innebygd i Dynamics 365 Finance-klienten

> [!NOTE] 
> - Før hierarkiet for tilgangsliste kan påvirke data i Power BI, må hierarkiet for tilgangsliste og radnivåsikkerhet i Power BI sammenkobles. Hvis du vil ha mer informasjon, kan du se [Definere sikkerhet for innholdspakken Kostnadsregnskap](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Tilgangslistehierarkiet bidrar ikke til å sikre eksporten av data til Excel. Derfor skal det rapporteringsverktøyet bare brukes av regnskapsførere og ledere som må ha full tilgang til å vise dataene.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]