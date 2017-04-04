---
title: Salgsavtaler
description: "Denne artikkelen inneholder informasjon om salgsavtaler. En salgsavtale er en kontrakt som forplikter kunden til å kjøpe produkter i et bestemt antall eller for et bestemt beløp over tid, i bytte mot spesielle priser og rabatter."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 9554
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4dd1eae27ae33837fbab16f764083168578d0a29
ms.lasthandoff: 03/31/2017


---

# <a name="sales-agreements"></a>Salgsavtaler

Denne artikkelen inneholder informasjon om salgsavtaler. En salgsavtale er en kontrakt som forplikter kunden til å kjøpe produkter i et bestemt antall eller for et bestemt beløp over tid, i bytte mot spesielle priser og rabatter.

En salgsavtale er en kontrakt som forplikter kunden til å kjøpe produkter i et bestemt antall for et bestemt beløp over tid, i bytte mot spesialpriser, spesialrabatter og andre spesielle vilkår, for eksempel betaling og levering. Prisene og rabattene i salgsavtalen overstyrer priser og rabatter som er angitt i en eventuell forretningsavtale.  

Gyldighetsperioden for en salgsavtale er definert av feltene **Gyldig fra** og **Utløpsdato** på avtalen. Kundens salgsordre kvalifiserer for avtalevilkårene hvis den ønskede forsendelsesdatoen for ordren er innenfor gyldighetsperioden. Alle salgsordrelinjer som er koblet til en salgsavtale, bidrar til å oppfylle denne salgsavtalen.  

Du kan opprette en salgsordre direkte fra en salgsavtale ved hjelp av **Frigivelsesordre**-handlingen. Du kan også velge en gyldig salgsavtale når du tar i mot ordrer (se "Bruke salgsavtaler i ordreprosessen" i denne artikkelen).  

**Merk:** i tidligere versjoner, salgsavtaler ble referert til som rammeordrer.

## <a name="commitment-types"></a>Forpliktelsestyper
Hver linje i en salgsavtale uttrykker en forpliktelse til å selge noe. Det er vanligvis to kategorier av forpliktelse:

-   **Verdiforpliktelse **– kunden godtar å kjøpe produkter for et bestemt beløp.
-   **Antallsforpliktelse **– kunden godtar å kjøpe et bestemt antall produkter.

En kontrakt kan dessuten forplikte kunden til å kjøpe et bestemt produkt eller produkter i en produktkategori. Ved å kombinere disse to faktorene (verdi kontra antall, og bestemte produkter kontra produktkategorier) får vi fire typer forpliktelse:

-   **Produktantallsforpliktelse** – kunden godtar å kjøpe et bestemt antall produkter. Linjer som bruker denne forpliktelsestypen, er definert av et varenummer og av antallet og enheten som ble avtalt. **Beløp**-feltet er ikke tilgjengelig.
-   **Produktverdiforpliktelse **– kunden godtar å kjøpe bestemte produkter for et bestemt beløp. Linjer som bruker denne forpliktelsestypen, er definert av et varenummer og beløpet som ble avtalt. Feltene **Antall** og **Enhet** er ikke tilgjengelige.
-   **Verdiforpliktelse for produktkategori ** – kunden godtar å kjøpe produkter for en bestemt salgskategori for et bestemt beløp. Linjer som bruker denne forpliktelsestypen, er definert av en kategori i hierarkiet av salgskategorier og et beløp. Feltene **Antall** og **Enhet** er ikke tilgjengelige.
-   **Verdiforpliktelse ** – kunden godtar å kjøpe hvilke som helst produkter i alle innkjøpskategorier for et bestemt beløp. Feltene **Antall** og **Enhet** er ikke tilgjengelige.

Linjer i den samme salgsavtalen kan ha ulike typer forpliktelser.

## <a name="pricing-terms-for-sales-agreements"></a>Prisvilkår for salgsavtaler
Prisvilkårene kan variere, avhengig av forpliktelsestypen. Prisvilkårene fra denne salgsavtalen overstyrer alle andre prisvilkår som gjelder basert på forretningsavtaler i en salgsordre som er knyttet til en salgsavtale. Tabellen nedenfor beskriver prisrelaterte felt som påvirkes av hver forpliktelsestype. "Ja" angir at feltet kan oppdateres på en ordrelinje.

| Forpliktelsestype                   | Enhetspris | Prisenhet | Rabattprosent | Kontantrabattbeløp |
|-----------------------------------|------------|------------|------------------|----------------------|
| Produktantallsforpliktelse       | Ja        | Ja        | Ja              | Ja                  |
| Produktverdiforpliktelse          |            |            | Ja              |                      |
| Verdiforpliktelse for produktkategori |            |            | Ja              |                      |
| Verdiforpliktelse                  |            |            | Ja              |                      |

## <a name="policies-for-sales-agreements"></a>Policyer for salgsavtaler
De følgende policyene påvirker hvordan koblingen mellom en salgsavtaleforpliktelse og de tilhørende salgsordrelinjene fungerer:

-   **Maks. håndheves** – Det totale antallet eller beløpet for alle ordrelinjer kan ikke overskride antallet eller beløpet som er angitt i den tilknyttede forpliktelsen.
-   **Pris og rabatt er fast** – Prisen på en ordrelinje og prisen på den tilknyttede forpliktelsen må være den samme. Hvis prisen er endret på ordrelinjen, brytes koblingen til forpliktelsen. Hvis koblingen brytes, bidrar ikke ordrelinjen til oppfyllelsen av forpliktelsen.
-   **Laveste frigivelsesbeløp** og **Høyeste frigivelsesbeløp** – Hvis et beløp er angitt, vises en melding hvis du gjør endringer i en ordrelinje som fører til at den er forskjellig fra den tilknyttede forpliktelsen.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Oppfyllelsesberegninger for salgsavtaler
Oppfyllelsesantall og -beløp vises i fanen **Oppfyllelse** i hurtigfanen **Linjedetaljer** på siden **Salgsavtaler**.  

I **Oppfyllelse**-området kan du vise totalt antall og totalbeløp for alle ordrelinjer som er koblet til den angitte salgsavtalen. Du kan også vise gjenstående beløp eller antall som kreves for å oppfylle forpliktelsen.  

I **Avtale**-området kan du vise antallene og beløpene fra den angitte salgsavtalen. Disse antallene og beløpene er de totale antallene og totalbeløpene som er forpliktet.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Bekreftelser og versjonshistorikk for salgsavtaler
Når du bekrefter en salgsavtale, lagres den gjeldende versjonen av salgsavtalen i en historikktabell. Hvis du endrer salgsavtalen, kan du bekrefte den på nytt hvis du vil lagre en annen versjon av salgsavtalen i historikken.  

Hvis du ikke bekrefter en salgsavtale, kan du fortsatt bruke den til å opprette salgsordrer. Historikkinformasjon for salgsavtalen lagres imidlertid ikke.  

Du kan forhåndsvise eller skrive ut alle endringer av bekreftelsene. Deretter kan du dele endringene med kunden for å få dem godkjent.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Bruke salgsavtaler i bestillingsprosessen
Hvis du ikke frigir salgsordrer for en salgsavtale direkte, kan du fortsatt koble en salgsavtale til en ordre under ordreregistreringsprosessen. Når du oppretter en ny salgsordre og velger en salgsavtale, brukes vilkårene i denne avtalen, f.eks. betalingsbetingelser, leveringsbetingelser og leveringsadresse, på ordrehodet, og koblingen mellom avtalen og ordren opprettes. Når du kan velge produkter og kategorier som er angitt i salgsavtalen, kopieres deretter prisene og rabattene fra avtalen på ordrelinjene. Den samme salgsordren kan inneholde både linjer som ikke knyttet til en salgsavtale, og linjer som har en forpliktelse for en salgsavtale.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Endre salgsordrer som er koblet til salgsavtaler
Hvis du har opprettet (frigitt) en salgsordre mot en salgsavtale, kan noen felt på denne salgsordrelinjer bare endres hvis du fjerner koblingen til de tilknyttede salgsavtalelinjene. Tabellen nedenfor viser noen av disse feltene.

| Felt                                                             | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ønsket forsendelsesdato                                               | Hvis du endrer den ønskede forsendelsesdatoen til en dato som er tidligere enn **Gyldighetsdato**-verdien på salgsavtalelinjen, må du fjerne koblingen til salgsavtalelinjen før du kan lagre den endrede forsendelsesdatoen. Hvis du endrer den ønskede forsendelsesdatoen til en dato som er senere enn **Utløpsdato**-verdien på salgsavtalelinjen, må du fjerne koblingen til salgsavtalelinjen før du kan lagre den endrede forsendelsesdatoen. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet amount | Hvis du endrer verdien i noen av disse feltene, og hvis det er merket av for **Pris og rabatt er fast** på en tilknyttet salgsavtalelinje, vises en meldingsboks der du blir bedt om å lagre endringen. Klikk **Ja** til å fjerne koblingen til salgsavtalelinjen og Omberegn pris. Klikk **ingen** å fjerne koblingen til salgsavtalelinjen uten å beregne prisen på nytt.                                                                   |
| Nettobeløp                                                        | Hvis du angir et beløp som overstiger beløpet som er angitt på en salgsavtalelinje der det er merket av for **Maks. håndheves** vises en meldingsboks der du blir bedt om å lagre det endrede beløpet. Klikk **Ja** til å fjerne koblingen til salgsavtalelinjen og Omberegn pris. Klikk **ingen** å fjerne koblingen til salgsavtalelinjen uten å beregne prisen på nytt.                                                                 |
| Antall                                                          | Hvis du angir et antall som overstiger antallet som er angitt på en salgsavtalelinje der det er merket av for **Maks. håndheves** vises en meldingsboks der du blir bedt om å lagre det endrede antallet. Klikk **Ja** til å fjerne koblingen til salgsavtalelinjen og Omberegn pris. Klikk **ingen** å fjerne koblingen til salgsavtalelinjen uten å beregne prisen på nytt.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Returnere en vare som er bestilt fra en salgsavtale
Når en kunde returnerer et produkt som ble bestilt fra en salgsavtale, kan Microsoft Dynamics 365 for operasjoner finne og Oppdater automatisk relaterte salgsavtalen-engasjement for å gjenspeile endringen i antall eller beløp. Ved å opprette en returordre på grunnlag av den opprinnelige salgsordren som er koblet til en salgsavtale, oppretter du en relasjon mellom salgsavtaleforpliktelsen, salgsordrelinjen og returordrefakturaen.  

Hvis du ikke ønsker å trekke returvareantallet fra salgsavtaleforpliktelsen, kan du bruke **Fjern kobling**-kontrollen på ** Returordre**-siden for å fjerne koblingen mellom returordren og salgsavtaleforpliktelsen. Hvis du må gjenopprette koblingen senere, klikker du **Opprett kobling**.  

**Obs! ** En returordre kan bare kobles til én salgsavtale. Hvis en kunde returnerer flere produkter som ble bestilt gjennom flere salgsavtaler, må du opprette en ny returordre for hvert produkt og opprette en kobling til den tilhørende salgsavtalen.

## <a name="automatic-search-for-sales-agreements"></a>Automatisk søk etter salgsavtaler
I noen situasjoner der salgsordrer er opprettet indirekte, som når du oppretter en kreditnota eller konserninterne salgsordrer, kan du kontrollere om Microsoft Dynamics 365 for operasjoner søker automatisk etter gjeldende salgsavtaler.

## <a name="financial-dimensions-on-sales-agreements"></a>finansdimensjoner i salgsavtaler
Du kan kopiere finansdimensjoner til dokumenthoder eller enkeltlinjer i en salgsavtale. Du kan endre dimensjonene i et avtalehode eller en avtalelinje når som helst. I dette tilfellet kopieres dimensjonene automatisk til frigivelseshodet eller frigivelseslinjen i frigivelsesordrer.


