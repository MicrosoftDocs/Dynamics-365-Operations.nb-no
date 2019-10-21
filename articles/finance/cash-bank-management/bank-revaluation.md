---
title: Bankrevaluering av utenlandsk valuta
description: Dette emnet gir en oversikt over prosessen for bankrevaluering av utenlandsk valuta. Det inneholder informasjon om oppsettet, kjøring av prosessen, beregning av prosessen og tilbakeføring av revalueringstransaksjoner.
author: mikefalkner
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: d7e7006679757d7e779b86c58649cd3869e1c7d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188447"
---
# <a name="bank-foreign-currency-revaluation"></a>Bankrevaluering av utenlandsk valuta

[!include [banner](../includes/banner.md)]


Dette emnet gir en oversikt over prosessen for bankrevaluering av utenlandsk valuta. Den forklarer hvordan du kan definere og kjøre prosessen og gir informasjon om beregning av prosessen. Det forklarer også hvordan du tilbakefører revalueringstransaksjoner, hvis tilbakeføring kreves.

Som en del av en periodeslutt krever regnskapskonvensjoner at bankkontosaldi i utenlandsk valuta revalueres ved å bruke ulike valutakurstyper (gjeldende, historisk, gjennomsnitt, osv.). Funksjonen for bankrevaluering av utenlandsk valuta kan brukes til å revaluere én eller flere bankkontoer. Funksjonen er også en global funksjon. Fra én side kan du derfor revaluere banker på tvers av alle de juridiske enhetene som du har tilgang til.

> [!NOTE]
> Når du kjører revalueringsprosessen, blir saldoen i hver bankkonto som er postert i utenlandsk valuta, revaluert. Transaksjonene for urealisert fortjeneste eller tap som opprettes under revalueringsprosessen, genereres av systemet. To transaksjoner kan opprettes, én for regnskapsvalutaen og én for rapporteringsvalutaen, hvis rapporteringsvaluta er relevant. Hver regnskapspost posteres til den urealiserte fortjenesten eller tapet og hovedkontoen som revalueres.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Klargjøre for kjøring av revaluering av utenlandsk valuta

Følgende oppsett kreves før du kan kjøre revalueringprosessen.

- Angi valutakurs på **Finans**-siden. Hvis en valutakurstype ikke er definert for hovedkontoen, brukes denne valutakurstypen under revaluering av utenlandsk valuta.
- På **Finans**-siden angir du kontoene for realisert fortjeneste, realisert tap, urealisert fortjeneste og urealisert tap, for revaluering av valuta. Realisert fortjeneste- og realisert tap-kontoer brukes når kunde- og leverandørtransaksjoner utlignes. Urealisert fortjeneste- og urealisert tap-kontoer brukes til å revaluere åpne transaksjoner og hovedkontoer for økonomimodul.
- På siden **Kontoer for revaluering av valuta** velger du andre kontoer for revaluering av valuta for hver valuta og firma. Hvis ingen kontoer er definert, brukes kontoene fra **Finans**-siden.

## <a name="enable-foreign-currency-revaluation"></a>Aktivere revaluering av utenlandsk valuta

Du må aktivere funksjonen for bankrevaluering av utenlandsk valuta før du kan behandle revaluering av utenlandsk valuta.

1. Gå til **Kontant- og bankbehandling \> Oppsett \> Parametere for kontant- og bankbehandling**.
2. På **Generelt**-fanen under **Revaluering av utenlandsk valuta** setter du **Aktiver bankrevaluering**-alternativet til **Ja** for å aktivere funksjonen for gjeldende juridiske enhet. 
3. I kategorien **Nummerserier** legger du til en nummerserie for revaluering av utenlandsk valuta.
4. Oppdater leseren for å se **Revaluering av utenlandsk valuta** i **Periodiske oppgaver**-delen på områdesiden.

Du må aktivere funksjonen for hver juridiske enhet som bruker revaluering av utenlandsk valuta. Hvis du er tilordnet rollen som systemansvarlig eller funksjonsleder, kan du eliminere dette trinnet ved å aktivere funksjonen med navnet **Aktiver bankrevaluering uten en parameter** i arbeidsområdet **Funksjonsbehandling**.

> [!NOTE]
> Hvis den juridiske enheten bruker en russisk, polsk eller ungarsk lands-/områdekode, kan du allerede gjøre bankrevalueringen av utenlandsk valuta. Du kan ikke bruke revaluering av utenlandsk valuta som brukes av andre land eller regioner.

## <a name="process-foreign-currency-revaluation"></a>Behandle en revaluering av utenlandsk valuta

Når installasjonen er fullført, kan du bruke siden **Revaluering av utenlandsk valuta** i Kontant- og bankbehandling til å revaluere saldoene for én eller flere bankkontoer på tvers av alle juridiske enheter. Du kan kjøre prosessen i sanntid, eller du kan planlegge å kjøre den ved hjelp av en satsvis jobb.

Siden **Revaluering av utenlandsk valuta** viser historikken for hver revalueringsprosess. Den viser når prosessen ble kjørt, og hvilke vilkår som ble definert, og inneholder en kobling til bilaget som ble opprettet for revalueringen. Den viser også om en tidligere revaluering ble tilbakeført. Hvis du vil kjøre prosessen for revaluering, velger du **Revaluering av utenlandsk valuta** i handlingsruten for å åpne **Bankrevaluering av utenlandsk valuta**-dialogboksen.

Feltet **Revalueringsdato** angir fristen for å beregne saldo for utenlandsk valuta som skal revalueres. Summen av alle banktransaksjoner som inntraff til og med denne datoen, revalueres.

Feltet **Valutakursdato** angir datoen for valutakursen som skal brukes til å revaluere valutabalansene. Du kan for eksempel revaluere saldoene fra og med 31. januar, men bruke valutakursen som er definert for 1. februar.

Revalueringsprosessen kan kjøres for én eller flere juridiske enheter. Oppslaget viser bare de juridiske enhetene som du har tilgang til. Velg de juridiske enhetene som du vil velge bankkontoene for, som er kvalifisert for revaluering av utenlandsk valuta. Alle bankkontoer for disse juridiske enhetene vises i rutenettet.

Sett alternativet **Forhåndsvis for postering** til **Ja** hvis du vil se resultatene av revalueringen før du posterer den. Revalueringen av utenlandsk valuta er en forhåndsvisning som kan posteres. Du trenger ikke kjøre revalueringsprosessen på nytt. Du kan eksportere resultatet i forhåndsvisningen til Microsoft Excel for å føre historikken over hvordan beløpene ble beregnet. Du kan ikke bruke satsvis behandling hvis du vil forhåndsvise resultatet av revalueringen.

Velg **OK** for å behandle revaluering av utenlandsk valuta. Det opprettes en post for å spore loggen for hver kjøring. En separat oppføring opprettes for hver juridiske enhet og hvert posteringslag.

## <a name="calculate-unrealized-gainloss"></a>Beregne urealisert tap/fortjeneste

I Kontant- og bankbehandling anses bankvalutaen for å være basisvalutaen, og den revalueres ikke. Saldoen for bankkontoen i regnskapsvalutaen revalueres ved hjelp av valutakursen mellom bankvalutaen og regnskapsvalutaen på **Valutakursdato**. Saldoen for bankkontoen i rapporteringsvalutaen revalueres også ved hjelp av valutakursen mellom bankvalutaen og rapporteringsvalutaen på **Valutakursdato**.

Det opprettes en transaksjon for forskjellen mellom saldoen på bankkontoen og den nye saldoen som beregnes for regnskapsvalutaen. En annen transaksjon opprettes for forskjellen mellom saldoen på bankkontoen og den nye saldoen som beregnes for rapporteringsvalutaen. Postene for disse transaksjonene er merket som avstemt. 

Ingen oppføring gjøres for regnskapsvalutaen hvis bankvalutaen samsvarer med regnskapsvalutaen. På samme måte gjøres det ingen oppføring for rapporteringsvalutaen hvis bankvalutaen samsvarer med rapporteringsvalutaen.

Transaksjonen for revaluering av utenlandsk valuta er også delt på tvers av dimensjonene som finnes på banktransaksjonene. Delingen er basert på saldoen for hver dimensjon. For eksempel er den totale banksaldoen 10 000, men saldoen for forretningsenhet 001 er 4 000, mens saldoen for forretningsenhet 002 er 6 000. I dette tilfellet posteres 40 prosent av revalueringsbeløpet til revalueringskontoen som har forretningsenhet 001, og 60 prosent posteres til revalueringskontoen som har forretningsenhet 002. Hvis kontostrukturen ikke inkluderer en forretningsenhet, posteres hele beløpet til revalueringskontoen.

## <a name="reverse-foreign-currency-revaluation"></a>Tilbakefør revaluering av utenlandsk valuta

Hvis du må tilbakeføre revalueringstransaksjonen, velger du **Tilbakefør transaksjon** på handlingssiden på siden **Revaluering av utenlandsk valuta**. Det opprettes en ny historisk post for revaluering av utenlandsk valuta for å beholde det historiske revisjonssporet for når revalueringen skjedde eller ble tilbakeført.

Hvis du vil reversere flere revalueringer, må du tilbakeføre den nyeste revalueringen først. Deretter fortsetter du å tilbakeføre eldre revalueringer i datorekkefølgen. Du kan deretter behandle nye revalueringer for periodene som du tilbakeførte.
