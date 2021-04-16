---
title: Kjøpsavtaler
description: Denne artikkelen inneholder informasjon om kjøpsavtaler. En kjøpsavtale er en kontrakt som forplikter en organisasjon til å kjøpe et bestemt antall eller beløp ved hjelp av flere bestillinger over tid. I bytte mot denne forpliktelsen mottar kjøperen spesialpriser og -rabatter.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal, PurchLine, AgreementLines
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 972762522b4f7627648f1e1eec9dad73fe503710
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825452"
---
# <a name="purchase-agreements"></a>Kjøpsavtaler

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om kjøpsavtaler. En kjøpsavtale er en kontrakt som forplikter en organisasjon til å kjøpe et bestemt antall eller beløp ved hjelp av flere bestillinger over tid. I bytte mot denne forpliktelsen mottar kjøperen spesialpriser og -rabatter. 

Kjøpsavtaler kan gjelde et bestemt antall av et produkt, et bestemt valutabeløp for et produkt eller et bestemt valutabeløp for varene i en innkjøpskategori. Prisene og rabattene i kjøpsavtalen overstyrer prisene og rabattene som er angitt i en eventuell forretningsavtale.  

På siden **Kjøpsavtaler** kan du opprette, bruke og følge opp kjøpsavtaler som gjelder mellom organisasjonen og leverandørene. Når du har opprettet en kjøpsavtale, kan du for eksempel bestille direkte fra den. Hver kjøpsavtale har en gyldighetsperiode som er definert av personen som oppretter kjøpsavtalen. Leveringsdatoen for et kjøp må være innenfor de gyldige datoene i gyldighetsperioden.  

Når du har opprettet en kjøpsavtale, må du aktivere den før den trer i kraft. Hvis du vil aktivere en kjøpsavtale, kan du sette alternativet **Merk avtale som gyldig** til **Ja**. 

Hvis du vil hindre at kjøpsavtalen blir brukt og bekreftet, merker du avtalestatusen som **Lukket**. Du kan fortsatt oppdatere statusen til **Gyldig** når som helst etter at du har foretatt denne endringen.

## <a name="responsible-workers-on-purchase-agreements"></a>Ansvarlige arbeidstakere i kjøpsavtaler

Du kan identifisere en primær ansvarlig arbeider og sekundær ansvarlig arbeider i kjøpsavtaleklassifiseringen. Disse verdiene vil bli arvet av den resulterende kjøpsavtalen. Du er ikke pålagt å legge til ansvarlige arbeidere i kjøpsavtalen, og de kan endres direkte på en per sak-basis i selve kjøpsavtalen. Du kan ikke angi en sekundær ansvarlig arbeider uten en primær ansvarlig arbeider, selv om du ikke trenger å ha en sekundær ansvarlig arbeider. Du kan ikke angi den samme arbeideren som både den primære og den sekundære ansvarlige arbeideren.

> [!IMPORTANT]
> Før du kan bruke funksjonen for den ansvarlige parten, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:
> 
> - **Modul:** *Innkjøp og leverandører*
> - **Funksjonsnavn:** *Ansvarlig part for kjøpsavtale*

## <a name="commitment-types"></a>Forpliktelsestyper
Hver linje i en kjøpsavtale er en forpliktelse til å kjøpe noe. Du kan bruke linjer fra flere bestillinger (PO-er) til å oppfylle forpliktelsen. Det finnes fire typer forpliktelser:

-   **Produktantallsforpliktelse** – Du kjøper et bestemt antall av et produkt.
-   **Produktverdiforpliktelse** – Du kjøper et bestemt valutabeløp av et produkt.
-   **Verdiforpliktelse for produktkategori** – Du kjøper et bestemt valutabeløp i en innkjøpskategori. Beløpet kan være for en katalogvare eller en ikke-katalogvare.
-   **Verdiforpliktelse** – Du kjøper et bestemt valutabeløp av et produkt eller produkter i en innkjøpskategori.

## <a name="pricing-terms-for-purchase-agreements"></a>Prisvilkår for kjøpsavtaler
Prisvilkårene kan variere, avhengig av forpliktelsestypen. Prisvilkårene fra kjøpsavtaler overstyrer alle andre prisvilkår som er definert for forretningsavtaler. Tabellen nedenfor beskriver prisrelaterte felt som påvirkes av hver forpliktelsestype. Felt som inneholder **Ja**, kan oppdateres på en ordrelinje.

| Forpliktelsestype                   | Enhetspris | Prisenhet | Rabattprosent | Kontantrabattbeløp |
|-----------------------------------|------------|------------|------------------|----------------------|
| Produktantallsforpliktelse       | Ja        | Ja        | Ja              | Ja                  |
| Produktverdiforpliktelse          |            |            | Ja              |                      |
| Verdiforpliktelse for produktkategori |            |            | Ja              |                      |
| Verdiforpliktelse                  |            |            | Ja              |                      |

## <a name="policies-for-purchase-agreements"></a>Policyer for kjøpsavtaler
De følgende policyene påvirker hvordan koblingen mellom en kjøpsavtaleforpliktelse og de tilhørende PO-linjene fungerer:

-   **Maks. håndheves** – Det totale antallet eller beløpet for alle ordrelinjer kan ikke overskride antallet eller beløpet som er angitt i den tilknyttede forpliktelsen.
-   **Pris og rabatt er fast** – Prisen på en ordrelinje og prisen på den tilknyttede forpliktelsen må være den samme. Hvis prisen er endret på ordrelinjen, brytes koblingen til forpliktelsen. Hvis koblingen brytes, bidrar ikke ordrelinjen til oppfyllelsen av forpliktelsen.
-   **Laveste frigivelsesbeløp og Høyeste frigivelsesbeløp** – Hvis et beløp er angitt, vises en melding hvis du gjør endringer i en ordrelinje som fører til at den er forskjellig fra den tilknyttede forpliktelsen.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Oppfyllelsesberegninger for kjøpsavtaler
Oppfyllelsesantall og -beløp vises i fanen **Oppfyllelse** i hurtigfanen **Linjedetaljer** på siden **Kjøpsavtaler**.  

**Oppfyllelse**-området viser gjenstående beløp eller antall som kreves for å oppfylle forpliktelsen.  

**Avtale**-område viser det totale antallet eller det totale beløpet som salgsavtalelinjen er gyldig for.  

Du kan få tilgang til PO-linjene og fakturalinjene som bidrar til oppfyllelsesberegningen, ved å velge **Relatert informasjon**-handlingen på linjene eller i overskriften til en kjøpsavtale.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Bekreftelser og versjonshistorikk for kjøpsavtaler
Når du bekrefter en kjøpsavtale, lagres den gjeldende versjonen av kjøpsavtalen i en historikktabell. Hvis du endrer kjøpsavtalen, kan du bekrefte den på nytt hvis du vil lagre en annen versjon av kjøpsavtalen i historikken. Hvis du ikke bekrefter en kjøpsavtale, kan du fortsatt bruke den til å opprette bestillinger. Historikkinformasjon for kjøpsavtalen lagres imidlertid ikke. Du kan forhåndsvise eller skrive ut alle versjoner av avtalen. Deretter kan du dele endringene med leverandøren for å få dem godkjent.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Bruke kjøpsavtaler i bestillingsprosessen
Når du oppretter en bestilling, kan du bruke en kjøpsavtale på den. Informasjon fra vilkårene for avtalen, som betalingsbetingelser, leveringsbetingelser og leveringsadresse, kopieres deretter til overskriften til bestillingen. Hvis PO-en inneholder én eller flere linjer for produkter eller kategorier som er dekket av avtalen, brukes prisene og rabattene fra kjøpsavtalen for disse linjene. Beløpet eller antallet på ordrelinjen bidrar til oppfyllelsen av forpliktelsen i kjøpsavtalen. Den samme bestillingen kan inneholde både linjer som ikke knyttet til en kjøpsavtale, og linjer som har en forpliktelse for en kjøpsavtale.  

Du kan velge en kjøpsavtale bare når du oppretter en bestilling. Du kan ikke velge en kjøpsavtale etter at bestillingen er opprettet.  
I enkelte tilfeller der bestillinger opprettes indirekte, kan du kontrollere om Supply Chain Management automatisk søker etter gjeldende kjøpsavtaler. Du kan for eksempel gjøre dette når du autoriserer planlagte bestillinger automatisk eller oppretter bestillinger som er basert på salgsordrer.

## <a name="matching-policy-on-purchase-agreements"></a>Kontrollpolicy for kjøpsavtaler
Du kan definere en linjekontrollpolicy i hodet i kjøpsavtalen. Denne linjekontrollpolicyen vil respektere kontrollpolicyen for leverandørparametere når feltet **Tillat overstyring av kontrollpolicy** på siden **Leverandørparametere** (i hurtigfanen **Pris- og antallssamsvar**) er satt til **Høyere enn firmapolicy**. Dokumenter som refererer til kjøpsavtalen, bruker linjekontrollpolicyen som er definert i kjøpsavtalehodet, hvis ikke annet er definert i den tilsvarende innkjøpspolicyen for vare, vare og leverandør eller kategori.

## <a name="purchase-agreements-and-intercompany-trade"></a>Kjøpsavtaler og konsernintern handel
Du kan opprette konserninterne handelsforbindelser mellom leverandørkontoer og kundekontoer som er i forskjellige juridiske enheter. Når en salgsordre eller bestilling opprettes for den ene av partene, opprettes en konsernintern ordrekjede. I ordrekjeden opprettes salgsordren og bestillingen i de aktuelle juridiske enhetene.  

Du kan opprette en kjøpsavtale eller salgsavtale for en av de konserninterne handelspartene. Deretter kan du generere den tilsvarende salgsavtalen eller kjøpsavtalen for den andre konserninterne handelsparten i den andre juridiske enheten.  

Hvis du oppretter en konsernintern bestilling som bruker den konserninterne kjøpsavtalen i én juridisk enhet, bruker den motsvarende konserninterne salgsordren den motsvarende konserninterne salgsavtalen i den andre juridiske enheten. Oppfyllelsen av salgsavtaleforpliktelsene og oppfyllelsen av kjøpsavtalene synkroniseres på tilsvarende måte som den konserninterne salgsordren og den konserninterne bestillingen synkroniseres.

## <a name="financial-dimensions-on-purchase-agreements"></a>finansdimensjoner i kjøpsavtaler
Du kan kopiere finansdimensjoner til dokumenthoder eller enkeltlinjer i en kjøpsavtale. Hvis du endrer dimensjonene i overskriften for avtalen eller avtalelinjen, vil endringen ikke påvirke frigitte ordrer, men den vil vises på alle nye ordrer.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Opprette en kjøpsavtale](tasks/create-purchase-agreement.md)

[Opprette en frigivelsesordre for innkjøp fra en innkjøpsavtale](tasks/create-purchase-release-order-purchase-agreement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]