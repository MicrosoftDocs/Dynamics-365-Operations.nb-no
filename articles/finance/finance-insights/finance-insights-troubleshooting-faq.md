---
title: Feilsøke konfigurasjonsproblemer for Finance Insights
description: Dette emnet viser problemer som kan oppstå når du bruker Finance Insights-funksjoner. Det forklarer også hvordan du retter disse problemene.
author: panolte
ms.date: 08/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512896"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Feilsøke konfigurasjonsproblemer for Finance Insights

[!include [banner](../includes/banner.md)]

Dette emnet viser problemer som kan oppstå når du bruker Finance Insights-funksjoner. Det forklarer også hvordan du retter disse problemene.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Symptom: Hvorfor kan jeg ikke tilordne målkolonnen for kundebetalingsinnsikt for dataintegrering?

### <a name="resolution"></a>Oppløsning

Det kan hende at du bruker en mal for en tidligere versjon. Før frigivelsen av versjon 10.0.17, konfigurerte forhåndsversjonskundene malen **Resultater av innsikt i kundebetaling (CDS til Fin and Ops)** Dataintegrering (DI) ved å bruke enheten **Resultat av betalingsprediksjon (forhåndsversjon)**. Etter en oppgradering til 10.0.17 og senere, bør du bruke DI-malen for **Resultater av innsikt i kundebetaling (CDS til Fin and Ops 10.0.17 og senere)** til å fullføre tilordningen. Det er ikke sikkert at du kan tilordne målkolonnen for ID-mal før enhetslisten over dataadministrasjon oppdateres og enheten for **Resultat av betalingsprediksjon** vises i den. Hvis du vil oppdatere enhetslisten og vise resultatet av betalingsforutsigelsen, fullfører du trinn i både Microsoft Dynamics 365 Finance og Dataverse (tidligere kjent som Common Data Service \[CDS\]-administratorportalen).

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

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Symptom: Hvorfor viser ikke kategorien Kontantprognose i arbeidsområdet for kontantstrømprognoser noen data?

### <a name="resolution"></a>Oppløsning

Kontantstrømprognosefunksjonen i Kontant- og bankbehandling og kontantstrømprognosefunksjonen i Finance Insights må være konfigurert og aktivert for at det skal vises data på riktig måte i arbeidsområdet **Kontantstrømprognose**.

Først setter du opp og aktiverer kontantstrømprognosene og likviditetskontoene. Hvis du vil ha mer informasjon, kan du se [Kontantstrømprognose](../cash-bank-management/cash-flow-forecasting.md). Hvis dette oppsettet er fullført, men du ikke ser resultatene du forventer, kan du se [Feilsøke konfigurasjon av kontantstrømprognose](../cash-bank-management/cash-flow-forecasting-tsg.md) for å få mer informasjon.

Deretter bekrefter du at kontantstrømprognosefunksjonen i Finance Insights (**Kontant- og bankbehandling \> Oppsett \> Finance Insights \> Kontantstrømprognoser**) er aktivert, og at opplæring av AI-modellen er fullført. Hvis opplæringen ikke er fullført, velger du **Prognose nå** for å starte modellopplæringsprosessen.
