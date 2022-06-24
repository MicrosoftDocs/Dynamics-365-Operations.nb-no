---
title: Feilsøke konfigurasjon av kontantstrømprognose
description: Denne artikkelen inneholder svar på spørsmål du kan ha når du konfigurerer kontantstrømprognoser. Den omhandler ofte stilte spørsmål om oppsettet for kontantstrøm, oppdateringer for kontantstrøm og Power BI-kontantstrøm.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0e3438bc07fde28d5d9d2d5b3d83bbe70692c0bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878077"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Feilsøke konfigurasjon av kontantstrømprognose

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder svar på spørsmål du kan ha når du konfigurerer kontantstrømprognoser. Den omhandler ofte stilte spørsmål om oppsettet for kontantstrøm, oppdateringer for kontantstrøm og Power BI-kontantstrøm.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Hvorfor vises kontantstrøm bare for én juridisk enhet?

Kontantstrømprognoser konfigureres og beregnes per juridisk enhet. Power BI-rapporter og kontantstrømprognosefunksjonene i Finance Insights viser resultatene.

Kontantstrømprognoser må defineres for hver juridiske enhet du vil se en prognose for. Gå gjennom konfigurasjonen av kontantstrømprognoser i alle juridiske enheter. Du kan også se gjennom konfigurasjonen til alle juridiske enheter for kontantstrømprognoser, og kontrollere at de er angitt slik du ønsker.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Hvorfor vises ikke Power BI alle kontantstrømdataene?

Flere trinn må fullføres før kontantstrømprognoser kan vises i Power BI-visninger. Gå gjennom følgende kontrolliste, og kontroller at hvert trinn er fullført:

- Definere kontantstrøm for hver juridiske enhet.
- Angi systemvalutaen og systemvalutakurstypen i parametere for økonomimodul.
- Angi finansregnskapsvalutaen og valutakurstypen.
- Angi valutakursen mellom transaksjonsvalutaen og regnskapsvalutaen.
- Angi valutakursen mellom regnskapsvalutaen og systemvalutaen.
- Angi valutakursen mellom regnskapsvalutaen og hver bankvaluta.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Hvorfor fungerte Power BI-kontantstrøm i tidligere versjoner, men er nå tom?

Kontroller at målingene for "kontantstrømmåling V2" og "LedgerCovLiquidityMeasurement" fra enhetslager er konfigurert. Hvis du vil ha mer informasjon om hvordan du arbeider med data i enhetsbutikk, kan du se [Power BI-integrering med enhetslager](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Kontroller at alle trinnene som kreves for å vise Power BI-innhold, er fullført. Hvis du vil ha mer informasjon, kan du se [Power BI-innholdet Kontantstrømoversikt](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Er enhetslagerenhetene oppdatert?

Du må oppdatere enhetene regelmessig for å sikre at dataene er oppdatert og nøyaktige. Hvis du vil oppdatere en bestemt enhet manuelt, kan du gå til **Systemadministrasjon \> Oppsett \> Enhetslager**, velge enheten og deretter velge **Oppdater**. Dataene kan også oppdateres automatisk. Sett alternativet **Automatisk oppdatering aktivert** til **Ja** på siden **Enhetslager**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Hvilken beregningsmetode skal brukes når kontantstrømprognoser beregnes?

Beregningsmetoden for kontantstrømprognose har to viktige valgalternativer. Alternativet **Ny** vil beregne kontantstrømprognoser for nye dokumenter og dokumenter som er endret siden den siste satsvise jobben ble kjørt. Dette alternativet går raskere, fordi det behandler et mindre delsett med dokumenter. Alternativet **Totalt** beregner kontantstrømprognoser på nytt for hvert dokument i systemet. Dette alternativet tar mer tid, fordi det har mer arbeid å fullføre.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Hvordan forbedrer jeg ytelsen til kontantstrømprognosene for gjentakende satsvis jobb?

Vi anbefaler at du kjører kontantstrømprognosen én gang hver dag i perioder med mindre trafikk ved hjelp av **Ny beregning**-metoden. Vi anbefaler at du bruker denne fremgangsmåten seks dager i uken. Deretter kjører du en kontantstrømprognose én gang i uken med beregningsmetoden **Totalt** på dagen med minst aktivitet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

