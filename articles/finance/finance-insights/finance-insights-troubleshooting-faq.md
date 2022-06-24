---
title: Feilsøke konfigurasjonsproblemer for Finance Insights
description: Denne artikkelen viser problemer som kan oppstå når du bruker Finance Insights-funksjoner. Det forklarer også hvordan du retter disse problemene.
author: panolte
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 1ee354a1c3d9b45eb12eeb3a6a29f2a6d5e4c34c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846922"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Feilsøke konfigurasjonsproblemer for Finance Insights

[!include [banner](../includes/banner.md)]

Denne artikkelen viser problemer som kan oppstå når du bruker Finance Insights-funksjoner. Det forklarer også hvordan du retter disse problemene.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Symptom: Hvorfor kan jeg ikke tilordne målkolonnen for kundebetalingsinnsikt for dataintegrering?

### <a name="resolution"></a>Oppløsning

Det kan hende at du bruker en mal for en tidligere versjon. Før frigivelsen av versjon 10.0.17, konfigurerte forhåndsversjonskundene malen **Resultater av innsikt i kundebetaling (CDS til Fin and Ops)** Dataintegrering (DI) ved å bruke enheten **Resultat av betalingsprediksjon (forhåndsversjon)**. Etter en oppgradering til 10.0.17 og senere, bør du bruke DI-malen for **Resultater av innsikt i kundebetaling (CDS til Fin and Ops 10.0.17 og senere)** til å fullføre tilordningen. Det er ikke sikkert at du kan tilordne målkolonnen for ID-mal før enhetslisten over dataadministrasjon oppdateres og enheten for **Resultat av betalingsprediksjon** vises i den. Hvis du vil oppdatere enhetslisten og vise resultatet av betalingsforutsigelsen, fullfører du trinn i både Microsoft Dynamics 365 Finance og Dataverse (tidligere kalt Common Data Service \[CDS\]-administratorportalen).

### <a name="in-finance"></a>I Finance

Følg denne fremgangsmåten i Finance etter at du har oppgradert.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Dataadministrasjon**.
2. I **Dataadministrasjon**-arbeidsområdet velger du flisen **Rammeverkparametere**.
3. På siden **Rammeverkparametere for dataimport/-eksport** velger du **Enhetsinnstillinger**, og deretter velger du **Oppdater enhetsliste**.
4. Lukk siden **Rammeverkparametere for dataimport/-eksport**.
5. I **Dataadministrasjon**-arbeidsområdet velger du flisen **Dataenheter**.
6. Søk etter "Resultat av betalingsprediksjon." Kontroller at enheten **Resultat av betalingsprediksjon** ikke er forhåndsversjonen. Navnet på forhåndsvisningsversjonen slutter på "(forhåndsvisning)." Hvis du bare ser forhåndsvisningsversjonen av enheten, kan du kontakte Microsoft Kundestøtte.

### <a name="in-dataverse"></a>I Dataverse

Følg denne fremgangsmåten i [Power Platform administrasjonssenteret](https://admin.powerplatform.microsoft.com/environments) for å oppdatere dataintegreringsprosjektene.

1. Hvis du bruker en forhåndsvisningsversjon av Finance Insights, fjerner du DI-prosjektet som er knyttet til malen **Resultater av innsikt i kundebetaling (CDS til Fin and Ops)**.
2. Følg trinnene i [Opprett et dataintegratorprosjekt](create-data-integrate-project.md). Bruk malen **Resultater av innsikt i kundebetaling (CDS til Fin and Ops 10.0.17 og senere)**.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>Symptom: Når jeg prøver å åpne AI Builder ved hjelp av koblingene på konfigurasjonssiden for kundebetalingsforutsigelser, hvorfor får jeg følgende feilmelding: "Beklager, det har vært en frakobling"?

### <a name="resolution"></a>Oppløsning

Dynamics 365 Finance-brukere må ha en Microsoft Power Apps-brukerkonto for miljøet, og denne brukerkontoen må ha rollen Systemtilpasser. Microsoft Power Apps-systemadministratoren kan opprette brukerkontoen og tilordne rollen. Deretter kan du gå til <https://make.preview.powerapps.com/>, logge deg på ved hjelp av denne brukerkontoen og prøve koblingene på nytt.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Symptom: Hvorfor viser ikke kategorien Kontantprognose i arbeidsområdet for kontantstrømprognoser noen data?

### <a name="resolution"></a>Oppløsning

Kontantstrømprognosefunksjonen i Kontant- og bankbehandling og kontantstrømprognosefunksjonen i Finance Insights må være konfigurert og aktivert for at det skal vises data på riktig måte i arbeidsområdet **Kontantstrømprognose**.

Først setter du opp og aktiverer kontantstrømprognosene og likviditetskontoene. Hvis du vil ha mer informasjon, kan du se [Kontantstrømprognose](../cash-bank-management/cash-flow-forecasting.md). Hvis dette oppsettet er fullført, men du ikke ser resultatene du forventer, kan du se [Feilsøke konfigurasjon av kontantstrømprognose](../cash-bank-management/cash-flow-forecasting-tsg.md) for å få mer informasjon.

Deretter bekrefter du at kontantstrømprognosefunksjonen i Finance Insights (**Kontant- og bankbehandling \> Oppsett \> Finance Insights \> Kontantstrømprognoser**) er aktivert, og at opplæring av AI-modellen er fullført. Hvis opplæringen ikke er fullført, velger du **Prognose nå** for å starte modellopplæringsprosessen.

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>Symptom: Hvorfor trenger du ikke installere en ny tilleggsknapp som vises i Microsoft Dynamics Lifecycle Services?

### <a name="resolution"></a>Oppløsning

Bekreft først at rollen **Miljøleder** eller **Prosjekteier** er tilordnet den påloggede brukeren i feltet **Prosjektsikkerhetsrolle** i Microsoft Dynamics Lifecycle Services (LCS). Installasjon av de nye tilleggene krever en av disse prosjektsikkerhetsrollene.

Hvis du har fått tildelt den riktige prosjektsikkerhetsrollen, må du kanskje oppdatere webleservinduet for å se knappen **Installer nytt tillegg**.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>Symptom: Finance Insights-tillegget virker ikke som det installeres. Hvorfor det?

### <a name="resolution"></a>Oppløsning

Trinnene nedenfor bør være fullført.

- Bekreft at du har **Systemadministrator** og **Systemtilpasser** tilgang i administrasjonssenteret for Power Portal.
- Bekreft at en Dynamics 365 Finance eller tilsvarende lisens brukes for brukeren som installerer tillegget.
- Kontroller at følgende Azure AD app er registrert i Azure AD: 

  | Program                  | App-ID           |
  | ---------------------------- | ---------------- |
  | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>Symptom: Feil: "Vi fant ingen data for det valgte filterområdet. Velg et annet filterområde, og prøv på nytt." 

### <a name="resolution"></a>Oppløsning

Kontroller oppsettet for dataintegratoren for å validere at det fungerer som forventet og oppdatere dataene fra AI Builder tilbake til Finance.  
Hvis du vil ha mer informasjon, kan du se [Opprett et dataintegreringsprosjekt](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>Symptom: Opplæring av kundebetalingsprognose mislyktes, og AI Builder-feilen fastslår: "Prognosen kan bare ha 2 distinkte resultatverdier for å lære opp modellen. Tilordne de to resultater og lær opp på nytt," "Opplæringsrapportproblem: IsNotMinRequiredDistinctNonNullValues".

### <a name="resolution"></a>Oppløsning

Denne feilen viser at det ikke er nok historiske transaksjoner i det siste året som representerer hver kategori som er beskrevet i kategoriene **Til planlagt tid**, **Forsinket** og **Svært sent**. Du kan løse denne feilen ved å justere transaksjonsperioden **Svært sent**. Hvis justering av transaksjonsperioden **Svært sent** ikke løser opp feilen, er ikke **Kundebetalingsforutsigelser** den beste løsningen å bruke, siden den trenger data i hver kategori til opplæringsformål.

Hvis du vil ha mer informasjon om hvordan du justerer kategoriene **Til planlagt tid**, **Forsinket** og **Svært sent**, kan du se [Aktiver kundebetalingsprognoser](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>Symptom: Modellopplæring mislyktes

### <a name="resolution"></a>Oppløsning

Modellopplæringen **Kontantstrømprognose** krever data som inneholder flere enn 100 transaksjoner og strekker seg over mer enn et år. Vi anbefaler at du har minst to år med data med flere enn 1 000 transaksjoner.

Funksjonen **Kundebetalingsforutsigelser** krever flere enn 100 transaksjoner i de siste seks til ni månedene. Transaksjonene kan omfatte fritekstfakturaer, salgsordrer og kundebetalinger. Disse dataene må være spredt på tvers av innstillingene **Til planlagt tid**, **Forsinket** eller **Svært sent** som er definert på **Konfigurasjon**-siden.    

Funksjonen **Budsjettforslag** krever minst tre år med budsjettdata eller faktiske data. Denne løsningen bruker tre til ti år med data i prognosene. Mer enn tre år kommer til å gi bedre resultater. Selve dataene fungerer best når det er variasjon i verdiene. Hvis dataene bare omfatter konstante data, for eksempel en leieutgift, kan opplæringen mislykkes siden kunstig intelligens ikke trengs for å prosjektere beløpene ved manglende variasjon.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>Symptom: Du får feilmeldingen «Tabellen med navnet msdyn_paypredpredictionresultentities finnes ikke. Den eksterne serveren returnerte feilen (404) Ikke funnet…»

### <a name="resolution"></a>Oppløsning

Miljøet har nådd maksimumsgrensen for tabeller for Data Lake-tjenester. Hvis du vil vite mer om denne grensen, kan du se delen **Aktivere dataendringer med minimal forsinkelse** i artikkelen [Oversikt over Eksporter til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md).
