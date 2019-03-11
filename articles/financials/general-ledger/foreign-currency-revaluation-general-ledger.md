---
title: Revaluering av utenlandsk valuta for finans
description: 'Dette emnet gir en oversikt over følgende handlinger for prosessen for revaluering av utenlandsk valuta i økonomimodulen: oppsett, kjøring av prosessen, beregning for prosessen, og tilbakeføring av revalueringstransaksjoner, om nødvendig.'
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb04c5a9e7db1a6c6a8d8c7126bfa80208d1fd53
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "315550"
---
# <a name="foreign-currency-revaluation-for-general-ledger"></a>Revaluering av utenlandsk valuta for finans

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over følgende handlinger for prosessen for revaluering av utenlandsk valuta i økonomimodulen: oppsett, kjøring av prosessen, beregning for prosessen, og tilbakeføring av revalueringstransaksjoner, om nødvendig. 

Som en del av en periodeslutt krever regnskapskonvensjoner at finanskontosaldi i utenlandsk valuta revalueres ved å bruke ulike valutakurstyper (gjeldende, historisk, gjennomsnitt, osv.). En regnskapskonvensjon krever for eksempel at aktiva og passiva revalueres med den gjeldende valutakursen, anleggsmidler med den historiske kursen og resultatkontoer med det månedlige gjennomsnittet. Revaluering av utenlandsk valuta i økonomimodulen kan brukes til å revaluere balansen og resultatet. 

> [!NOTE]
> Revaluering av utenlandsk valuta er også tilgjengelig i Kunder og Leverandører. Hvis du bruker disse modulene, skal utestående transaksjoner revalueres ved hjelp av revaluering av utenlandsk valuta i disse modulene. Revaluering av utenlandsk valuta i kunder og leverandører oppretter en regnskapspost i økonomimodulen for å gjenspeile urealisert fortjeneste eller tap, noe som sikrer at underfinans og økonomimodul kan avstemmes. Fordi revalueringen av utenlandsk valuta i kunder og leverandører oppretter regnskapsposter i økonomimodulen, skal hovedkontoene for kunder og leverandører utelates fra revaluering av utenlandsk valuta i økonomimodulen. 

Når du kjører revalueringsprosessen, blir saldoen i hver hovedkonto postert i utenlandsk valuta revaluert. Transaksjonene for urealisert fortjeneste eller tap som opprettes under revalueringsprosessen, genereres av systemet. To transaksjoner kan opprettes, én for regnskapsvalutaen og én for rapporteringsvalutaen, hvis det er relevant. Hver regnskapspost posteres til urealisert fortjeneste eller tap og hovedkontoen revalueres.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Klargjøre for kjøring av revaluering av utenlandsk valuta
Følgende oppsett kreves før du kan kjøre revalueringprosessen.

-   På **Hovedkonto**-siden:
-   Hvis hovedkontoen skal revalueres i økonomimodul, velger du **Revaluering av utenlandsk valuta**. Hvis hovedkontoen ikke skal revalueres (for eksempel for AR og AP ved revaluering i underfinansene), fjerner du avmerkingen.
-   Hvis hovedkontoen er markert for revaluering, angir du **valutakurstypen**. Denne valutakurstypen skal brukes for revaluering av hovedkontoen. Et separat felt, **Valutakurstype for finansrapportering**, er tilgjengelig for finansrapportering. De to feltene holdes synkronisert, slik at ulike valutakurstyper kan brukes for revaluering og finansrapportering.

-   På **Finans**-siden:
-   Angi **valutakurstypen**. Hvis valutakurstypen ikke er definert for hovedkontoen, brukes denne valutakurstypen under revaluering av utenlandsk valuta.
-   Angi kontoene for realisert fortjeneste, realisert tap, urealisert fortjeneste og urealisert tap, for revaluering av valuta. Kontoene for realisert fortjeneste og realisert tap brukes for utligning av AR- og AP-transaksjoner, og kontoene for urealisert fortjeneste og urealisert tap brukes for revaluering av åpne transaksjoner og hovedkontoene i økonomimodulen.

-   På siden **Valutarevalueringskontoer**:
-   Velg ulike revalueringskontoer for valuta for hver valuta og firma. Hvis ingen kontoer er definert, brukes kontoene fra **Finans**-siden.

## <a name="process-foreign-currency-revaluation"></a>Behandle en revaluering av utenlandsk valuta
Når oppsettet er fullført, kan du bruke siden **Revaluering av utenlandsk valuta** til å revaluere saldoene fra hovedkontoene. Du kan kjøre prosessen i sanntid eller planlegge å kjøre den ved hjelp av en satsvis jobb. 

Siden **Revaluering av utenlandsk valuta** viser loggen for hver revalueringsprosess, inkludert da prosessen ble kjørt, hvilke kriterier som ble definert, en kobling til bilaget som ble opprettes for revalueringen, og en post hvis en tidligere revaluering ble tilbakeført. For å kjøre revalueringsprosessen klikk knappen **Revaluering av utenlandsk valuta**. 

Verdiene **Fra-dato** og **Til dato** definerer datointervallet for å beregne saldo for utenlandsk valuta som skal revalueres. Når du revaluerer resultatkontoer, revalueres summen av alle transaksjoner som forekommer i datointervallet. Når du revaluerer balansekontoer, ignoreres Fra-datoen. I stedet bestemmes saldoen som skal revalueres ved å gå fra begynnelsen av regnskapsåret til Til-datoen. 

**Kursdato** kan brukes til å definere datoen som skal brukes for valutakursen. Du kan for eksempel revaluere saldoene mellom den datointervallet fra 1. januar til 31. januar, men bruke valutakursen som er definert for 1. februar. 

Velg hvilke hovedkontoer som skal revalueres: Alle, Balanse eller Resultat. Bare hovedkontoer som er merket for revaluering (på siden for hovedkonto) blir revaluert. Hvis du vil begrense området for hovedkontoer, kan du bruke kategorien **Poster som skal inkluderes** til å definere et område for hovedkontoer eller individuelle hovedkontoer. 

Revalueringsprosessen kan kjøres for én eller flere juridiske enheter. Oppslaget viser bare de juridiske enhetene som du har tilgang til. Velg de juridiske enhetene som du vil kjøre revalueringsprosessen for. 

Revalueringen kan kjøres for én eller flere utenlandske valutaer. Oppslaget inkluderer alle valutaer som ble bokført i datoområdet som er relevant for typen hovedkontoen (balanse eller resultat) for de juridiske enhetene som er valgt for revaluering. Regnskapsvalutaen vil bli inkludert i listen, men ingenting revalueres hvis regnskapsvalutaen er valgt. 

Angi **Forhåndsvis for postering** til **Ja** hvis du vil se resultatet av revaluering av økonomimodulen. Forhåndsvisningen i økonomimodulen er forskjellig fra simuleringen i AR- og AP-revalueringen av utenlandsk valuta. Simuleringen i AR og AP er en rapport, men økonomimodulen er en forhåndsvisning som kan posteres, uten å måtte kjøre revalueringen på nytt. Resultatet av forhåndsvisningen kan eksporteres til Microsoft Excel for å bevare historikken over hvordan beløpene ble beregnet. Du kan ikke bruke satsvis behandling hvis du vil forhåndsvise resultatet av revalueringen. Fra forhåndsvisningen har brukeren muligheten til å postere resultatet av alle juridiske enheter ved hjelp av **Poster**-knappen. Hvis det er et problem med resultatene for en juridisk enhet, har brukeren også mulighet til å postere et delsett av de juridiske enhetene ved hjelp av knappen **Velg juridiske enheter for postering**. 

Når prosessen for revaluering av utenlandsk valuta er fullført, opprettes en post for å spore loggen for hver kjøring.  En separat oppføring opprettes for hver juridiske enhet og posteringslag.

## <a name="calculate-unrealized-gainloss"></a>Beregne urealisert tap/fortjeneste
Transaksjonene for urealisert tap/fortjeneste blir opprettet på en annen måte mellom revaluering av økonomimodulen og AR- og AP-revaluering. I AR og AP tilbakeføres den tidligere revalueringen fullstendig (forutsatt at transaksjonen ikke er utlignet ennå), og en ny revalueringstransaksjon opprettes for urealisert fortjeneste/tap basert på den nye valutakursen. Dette er fordi vi revaluerer hver enkelt transaksjon i AR og AP. I økonomimodulen tilbakeføres ikke den forrige revalueringen. I stedet opprettes det en transaksjon for delta mellom saldoen for hovedkontoen, inkludert eventuelle tidligere revalueringsbeløp, og den nye verdien, basert på valutakursen for kursdatoen. 

**Eksempel** Følgende saldoer finnes for hovedkontoen 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Dato**   | **Finanskonto** | **Transaksjonsbeløp** | **Regnskapsbeløp** |
| 20. januar | 110110 (kontant)      | 500 EUR (debet)        | 1000 USD (debet)      |

Hovedkontoen revalueres den 31. januar.  Urealisert fortjeneste/tap beregnes på følgende måte.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Gjeldende saldo i transaksjonsvaluta** | **Gjeldende saldo i regnskapsvaluta** | **Valutakursen ved revaluering** | **Nytt regnskapsvalutabeløp** | **Urealisert fortjeneste/tap**    |
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833,33 EUR (500 x 1,666667)        | 166,67 tap (833,33 – 1000) |

Følgende regnskappost opprettes.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Dato**   | **Finanskonto**       | **Debet** | **Kreditt** |
| 31. januar | 110110 (kontant)            |           | 166.67     |
| 31. januar | 801400 (urealisert tap) | 166.67    |            |

Ingen nye transaksjoner posteres for februar måned.  Hovedkontoen revalueres den 28. februar.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Gjeldende saldo i transaksjonsvaluta** | **Gjeldende saldo i regnskapsvaluta** | **Valutakursen ved revaluering** | **Nytt regnskapsvalutabeløp** | **Urealisert fortjeneste/tap**    |
| 500 EUR                                     | 833,33 USD (1000 - 166,67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | 416,67 fortjeneste (1250 – 833,33) |

Følgende regnskappost opprettes.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Dato**    | **Finanskonto**       | **Debet** | **Kreditt** |
| 28. februar | 110110 (kontant)            | 416.67    |            |
| 28. februar | 801600 (urealisert fortjeneste) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Tilbakefør revaluering av utenlandsk valuta
Hvis du vil tilbakeføre revalueringstransaksjonen, velger du knappen **Tilbakefør transaksjon** på siden **Revaluering av utenlandsk valuta**. Det opprettes en ny historisk post for revaluering av utenlandsk valuta for å beholde det historiske revisjonssporet for når revalueringen skjedde eller ble tilbakeført. 

Du kan tilbakestille resultatene av revalueringen utenfor datorekkefølgen, men du må kanskje også tilbakeføre en mer oppdatert revaluering for å sikre riktig saldo for hver revaluerte hovedkonto. Tilbakeføringene kan oppstå utenfor datorekkefølgen fordi det finnes ingen måte å kontrollere hvilke hovedkontoer som revalueres og frekvensen for når de revalueres. En organisasjon kan for eksempel velge å revaluere de viktigste kontantkontoene kvartalvis, men alle andre hovedkontoer månedlig.



