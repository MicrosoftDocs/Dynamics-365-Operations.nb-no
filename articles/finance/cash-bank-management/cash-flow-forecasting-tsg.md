---
title: Feilsøke konfigurasjon av kontantstrømprognose
description: Dette emnet inneholder svar på spørsmål du kan ha når du konfigurerer kontantstrømprognoser. Den omhandler ofte stilte spørsmål om oppsettet for kontantstrøm, oppdateringer for kontantstrøm og Power BI-kontantstrøm.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985293"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Feilsøke konfigurasjon av kontantstrømprognose

[!include [banner](../includes/banner.md)]

Dette emnet inneholder svar på spørsmål du kan ha når du konfigurerer kontantstrømprognoser. Den omhandler ofte stilte spørsmål om oppsettet for kontantstrøm, oppdateringer for kontantstrøm og Power BI-kontantstrøm.

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

Kontroller at målingene for "kontantstrømmåling V2" og "LedgerCovLiquidityMeasurement" fra enhetslager er konfigurert. Hvis du vil ha mer informasjon om hvordan du arbeider med enhetslager, kan du se [Power BI-integrering med enhetslager](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Kontroller at alle trinnene som er nødvendige for å vise Power BI-innhold, er fullført. Hvis du vil ha mer informasjon, kan du se [Power BI-innholdet Kontantstrømoversikt](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Er enhetslagerenhetene oppdatert?

Du må oppdatere enhetene regelmessig for å sikre at dataene er oppdatert og nøyaktige. Hvis du vil oppdatere en bestemt enhet manuelt, kan du gå til **Systemadministrasjon \> Oppsett \> Enhetslager**, velge enheten og deretter velge **Oppdater**. Dataene kan også oppdateres automatisk. Sett alternativet **Automatisk oppdatering aktivert** til **Ja** på siden **Enhetslager**.
