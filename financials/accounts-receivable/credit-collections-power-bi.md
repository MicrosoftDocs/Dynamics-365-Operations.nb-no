---
title: Power BI-innholdet Behandling av kreditt og innkrevinger
description: "Dette emnet beskriver hva som er inkludert i Power BI-innholdet Behandling av kreditt og innkrevinger. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, UnifiedOperations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: c066e1a190a5536ad67368b4e059ab6bc66718e6
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017

---

# Power BI-innholdet Behandling av kreditt og innkrevinger
<a id="credit-and-collections-management-power-bi-content" class="xliff"></a>

Dette emnet beskriver hva som er inkludert i Microsoft Power BI-innholdet **Behandling av kreditt og innkrevinger**. Det forklarer hvordan du kan få tilgang til Power BI-rapporter, og gir informasjon om datamodellen og enhetene som brukes til å bygge innholdet.

## Oversikt
<a id="overview" class="xliff"></a>

Power BI-innholdet **Behandling av kreditt og innkrevinger** ble laget for ledere for kreditt og innkreving, samt innkrevingsassistenter. Det gir nøkkelmål for kredit og innkreving, for eksempel dager utestående salg, forfalt saldo, kreditteksponering og kunder som har overskredet kredittgrensen. Det bruker transaksjonsdata og gir aggregerte visninger av kredit og innkreving på tvers av alle firmaer. Det gir også en analyse per firma, kundegruppe og kunde.

Power BI-innholdet består av 10 rapportsider:

- To oversiktssider (én side for en kreditoversikt og én side for en innkrevingsoversikt)
- Åtte detaljsider med detaljer for mål for kredit og innkreving som er delt opp på tvers av ulike dimensjoner

Alle beløpene vises i systemvalutaen. Du kan definere systemvalutaen på **Systemparametere**-siden.

Som standard vises kredit- og innkrevingsdataene for gjeldende firma. Hvis du vil se dataene på tvers av alle firmaer, tilordner du plikten **CustCollectionsBICrossCompany** til rollen.

## Tilgang til Power BI-innhold
<a id="accessing-the-power-bi-content" class="xliff"></a>
Hvis du bruker oppdateringen for juli 2017 av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, vises Power BI-innholdet **Behandling av kreditt og innkrevinger** i arbeidsområdet **Kundekreditt og innkrevinger**.

## Rapporter som er inkludert i Power BI-innholdet
<a id="reports-that-are-included-in-the-power-bi-content" class="xliff"></a>

Power BI-innholdet **CustCollectionsBICrossCompany** omfatter en rapport som består av et sett med mål. Disse målene vises som diagrammer, fliser og tabeller. Tabellen nedenfor gir en oversikt over visualiseringer i Power BI-innholdet **CustCollectionsBICrossCompany**.

| Rapportside                 | Visualisering |
|-----------------------------|---------------|
| Innkrevingsoversikt        | <ul><li>Forfalte kunder</li><li>Kunder over kredittgrense</li><li>DSO 30 dager</li><li>Åpne tilfeller</li><li>Gjennomsnitt dager til lukking av sak</li><li>Åpne aktiviteter</li><li>Gjennomsnitt dager til lukking av aktiviteter</li><li>Åpne rentenotaer</li><li>Åpne purringer</li><li>Kundesperre</li><li>Salgssperre</li><li>Aldersfordelte saldoer</li><li>Purrestatusbeløp</li><li>Purrekodebeløp</li><li>Avskrivning etter årsak</li><li>Forfalt saldo etter område</li><li>Forventede betalinger</li></ul> |
| Kreditoversikt             | <ul><li>Forfalte kunder</li><li>Kredittgrense i forhold til forfalt saldo</li><li>Rutenett for kunder over kredittgrense</li><li>Kunder over kredittgrense per firma</li><li>Kreditt brukt i forhold til total kredittgrense</li><li>Kredittgrense i forhold til kreditt brukt etter område</li><li>Kunder per kredittvurdering</li></ul> |
| Kredittgrense                | <ul><li>Kredittgrense</li><li>Detaljer om kredittgrense</li><li>Kredittgrense per kunde</li><li>Kredittgrense per kundegruppe</li><li>Kredittgrense per kredittvurdering per firma</li><li>Kredittgrense vs kreditt brukt etter område</li></ul> |
| Kunder over kredittgrense | <ul><li>Kunder over kredittgrense</li><li>Detaljer om kunder over kredittgrense</li><li>Kunder over kredittgrense per firma</li><li>Kunde over kredittgrense per kundegruppe</li><li>Kunder over kredittgrense etter område</li></ul> |
| Forfalte kunder          | <ul><li>Forfalte kunder</li><li>Detaljer om forfalt kunde</li><li>Forfalt kunde per firma</li><li>Forfalt kunde per kundegruppe</li><li>Forfalt kunde etter område</li></ul> |
| Aldersfordelte saldoer               | <ul><li>Aldersfordelte saldoer</li><li>Detaljer om aldersfordelte saldoer</li><li>Aldersfordelte saldoer per firma</li><li>Aldersfordelte saldoer per kundegruppe</li></ul> |
| Forventede betalinger           | <ul><li>Forventede betalinger</li><li>Detaljer om forventede betalinger</li><li>Forventede betalinger per firma</li><li>Forventede betalinger per kundegruppe</li><li>Forventede betalinger etter område</li></ul> |
| Avskrivninger                  | <ul><li>Avskrivninger etter område</li><li>Detaljer om avskrivninger</li><li>Avskrivninger etter hovedkonto</li><li>Avskrivninger per firma</li><li>Avskrivninger per kundegruppe</li><li>Avskrivninger etter område</li></ul> |
| Purrestatus          | <ul><li>Tvist</li><li>Brutt løfte om betaling</li><li>Løfte om betaling</li><li>Detaljer om purrestatus</li><li>Purrestatusbeløp</li><li>Åpne tilfeller</li><li>Åpne aktiviteter</li></ul> |
| Purringer         | <ul><li>Purrekodebeløp</li><li>Detaljer om purrekodebeløp</li><li>Purrebeløp per firma</li><li>Purrebeløp per kundegruppe</li><li>Purrebeløp etter område</li></ul> |

Diagrammer og fliser for alle disse rapportene kan filtreres og festes på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruke funksjonen for eksport av underliggende data til å eksportere underliggende data som oppsummeres i en visualisering.

## Utvide Power BI-innholdet
<a id="extending-the-power-bi-content" class="xliff"></a>
Hvis du bruker innholdspakkene som er tilgjengelige i Microsoft Dynamics Lifecycle Services (LCS), kan du gi personer som ikke logger på Finance and Operations, gode analyser. Du kan endre disse innholdspakkene slik at de inneholder andre rapporter eller visuelle hjelpemidler, og deretter publisere innholdspakkene på Power BI.com-leieren for analyse.

Du kan finne Power BI-innholdet **Behandling av kreditt og innkrevinger** i det delte aktivabiblioteket i LCS. Hvis du vil ha mer informasjon om hvordan du laster ned innholdet og implementerer det i organisasjonen, kan du se [Power BI-innhold i LCS fra Microsoft og partnerne](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners). Hvis du vil se en demo som viser hvordan du implementerer Power BI-innholdet, kan du se [Power BI-innhold fra Microsoft og partnerne i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

Pass på at du laster ned Power BI-innholdet **Behandling av kreditt og innkrevinger** som gjelder for versjonen av Finance and Operations du bruker.

## Forstå datamodellen og enheter
<a id="understanding-the-data-model-and-entities" class="xliff"></a>

Følgende data brukes til å fylle ut rapporten i Power BI-innholdet **Behandling av kreditt og innkrevinger**. Disse dataene vises som aggregerte mål som er oppsamlet i enhetslageret. Enhetslageret er en Microsoft SQL Server-database som er optimalisert for analyse. Hvis du vil ha mer informasjon, se [Oversikt over Power BI-integrering med enhetslager](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-integration-entity-store).

| Enhet                                      | Aggregerte nøkkelmålinger           | Datakilde                                 | Felt                                                      | beskrivelse |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | Antall lukkede aktiviteter og gjennomsnittlig lukketid for disse aktivitetene. |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | Antall åpne aktiviteter. |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | Summen av aldersfordelte saldoer. |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | Beløpene som er forfalt. |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | Antall lukkede saker og gjennomsnittlig lukketid for disse sakene. |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | Antall åpne saker. |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | Antall åpne purringer. |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Saldoen for posterte purringer. |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | Saldoen for transaksjoner med purrestatus. |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | Summen av kreditteksponering og -beløp som kunder er over kredittgrensen. |
| CustCollectionsBICustOnHold                 | Blokkert                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | Antall kunder som er på vent. |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | Dager utestående salg i 30 dager. |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | Summen av forventede betalinger innen neste år. |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | Antallet rentenotaer som har blitt opprettet. |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | Antall salgsordrer totalt som er på vent. |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | Summen av transaksjoner som er avskrevet. |

