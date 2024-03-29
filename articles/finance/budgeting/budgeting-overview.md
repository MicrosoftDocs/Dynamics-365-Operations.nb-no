---
title: Startside for budsjettering
description: Denne artikkelen gir en oversikt over komponenter i budsjetteringsfunksjonaliteten, budsjetteringsverktøy og rapporteringsfunksjoner i Microsoft Dynamics 365 Finance.
author: panolte
ms.date: 04/29/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom:
- "106043"
- intro-internal
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db15c52ddde08bcc9d390c51efc676c20aac0a7e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067441"
---
# <a name="budgeting-home-page"></a>Startside for budsjettering

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over komponenter i budsjetteringsfunksjonaliteten, budsjetteringsverktøy og rapporteringsfunksjoner. 

## <a name="components-of-budgeting-functionality"></a>Komponenter i budsjetteringsfunksjonaliteten

Ressursplanleggingssyklusen for et selskap består vanligvis av planlegging, budsjettering og prognoseaktiviteter.

[![Komponenter i budsjetteringsfunksjonaliteten.](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

Prosessene for både langsiktig strategisk planlegging og årlig budsjettplanlegging støttes gjennom et budsjettplandokument. Budsjettplandokumenter er tett integrert med Microsoft Excel. Brukere kan konfigurere et ubegrenset antall monetære og kvantitative scenarier og kan også definere et organisasjonshierarki for budsjettering for å støtte metoder for budsjettering ovenfra og nedenfra. Når et budsjett er opprettet og godkjent i programmet, kan du konvertere budsjettplanen til en budsjettregisteroppføring. Budsjettregisteroppføringer har verktøy for å vedlikeholde budsjettet og holde beløp sporbare via budsjettkoder. Budsjettregisteroppføringer gjør at du kan endre opprinnelige budsjetter, utføre overføringer og overføre budsjettbeløp fra forrige år. Et firma kan aktivere budsjettkontroll basert på det etablerte budsjettet. Nivået av kontroll avhenger av organisasjonskulturen og modenhetsnivået for organisasjonen. Organisasjoner som har et lavt modenhetsnivå, kan la budsjettet være "som det er" og være mer reaktive enn proaktive hvis et budsjett ikke oppfyller forventningene. Andre organisasjoner kan aktivere policyer for budsjettkontroll som hindrer brukere fra å foreta kjøp hvis budsjettmidler ikke er tilgjengelige.

Svært modne organisasjoner kan opprette en organisasjonskultur der ansatte har kunnskap om organisasjonsmål og følger disse målene gjennom policyer, for eksempel «Vurder nettmøte i stedet for en reise». Programmet omfatter et rammeverk for budsjettkontroll som lar ledelsen i firmaet velge hard kontroll (som forhindrer at posteringer går over budsjettet) eller myk kontroll (der brukere blir varslet om at de kommer til å overskride de tilgjengelige budsjettmidlene, men kan selv avgjøre hvordan de vil gå frem). Du kan også bruke rullerende prognoser. En rullerende prognose er en vanlig sammenligning av budsjettbeløp kontra faktiske beløp og brukes til å definere hvor bra firmaet gjør det med hensyn til budsjettet. En rullerende prognose brukes også til å identifisere trender. I økonomi og drift støttes rullerende prognoser – via et budsjettplandokument – som innledende planleggingsaktiviteter. Rullerende prognoser kan utføres parallelt med planleggingen for den kommende budsjettsyklusen.

-   [Oversikt over budsjettering](basic-budgeting-overview-configuration.md)
-   [Oversikt over budsjettkontroll](budget-control-overview-configuration.md)
-   [Oversikt over budsjettplanlegging](budget-planning-overview-configuration.md)
-   [Stillingsprognose](position-forecasting.md)
-   [Justeringsdokumenter for budsjettplanlegging](budget-planning-justification-docs.md)
-   [Budsjettplanleggingsmaler for Excel](budget-planning-excel-templates.md)

## <a name="budgeting-tools"></a>Budsjetteringsverktøy
[![Budsjetteringsverktøy.](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Ytterligere funksjoner for planlegging og budsjettering er tilgjengelige og er integrert med finansbudsjetter.

-   **Arbeidsstyrkebudsjetter** – Arbeidsstyrkebudsjettering inneholder detaljert planlegging av budsjettkostnadskomponent for stillinger, kompensasjonsgrupper og så videre.
-   **Anleggsmiddelbudsjetter** – Basert på anleggsmiddelinformasjon kan du beregne planlagt avskrivning og registrere andre planlagte transaksjoner som er relaterte til anleggsmidler.
-   **Prosjektbudsjetter** – I prosjektmodulen kan du opprette detaljert prosjektprognoser. Prosjektprognosene vil inneholde informasjon om planlagte timer, utgifter, avgifter og varer.
-   **Behovsprognose** – Du kan beregne fremtidig beholdningsbehov og opprette behovsprognoser basert på historiske transaksjonsdata.

Hvis du vil ha informasjon om hvordan du kobler planlegging data fra andre moduler i budsjettplaner, kan du se [Integrasjon av budsjettplanlegging med andre moduler](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Brukergrensesnitt og rapporteringsfunksjonalitet
Brukere kan opprette budsjettplaner direkte i klienten (ved hjelp av en konfigurerbar side for budsjettplandokument) eller via Excel. Excel har flere tilleggsfunksjoner. Du kan for eksempel bruke eksterne data som en kilde for en budsjettplan, foreta egendefinerte beregninger og bruke Microsoft pivottabeller og -diagrammer. Du kan konfigurere de fleste variablene i budsjettplanleggingsprosessen. 

Du kan for eksempel definere hvem som skal foreta budsjettering, hva som skal budsjetteres, og hvordan prosessen skal se ut. Selv om du kan bruke Excel til budsjettplanlegging, brukes programmet som eneste faktakilde og bidrar til å forhindre problemer med budsjettkontroll. Periodiske prosesser kan brukes til å hente inn innledende data for budsjettering i budsjettplanen. Når det gjelder rapportering, tilbyr programmet et sett med standard forespørselssider der du kan vise og analysere budsjetteringsdata. Du kan få tilgang til budsjettplandata via [Finansrapportering](../general-ledger/financial-reporting-getting-started.md), og separate budsjettplanscenarier kan vises som kolonner i finansrapporten.








[!INCLUDE[footer-include](../../includes/footer-banner.md)]

