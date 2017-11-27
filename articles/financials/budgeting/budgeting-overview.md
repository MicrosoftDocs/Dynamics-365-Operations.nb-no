---
title: Startside for budsjettering
description: "Dette emnet gir en oversikt over komponenter i budsjetteringsfunksjonaliteten, budsjetteringsverktøy og rapporteringsfunksjoner i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: twheeloc
manager: AnnBe
ms.date: 08/09/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 953c79b134b82ce2a3e0adc05dc3bdf3ce583482
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="budgeting-home-page"></a>Startside for budsjettering

[!include[banner](../includes/banner.md)]


Dette emnet gir en oversikt over komponenter i budsjetteringsfunksjonaliteten, budsjetteringsverktøy og rapporteringsfunksjoner i Finance and Operations. 

<a name="components-of-budgeting-functionality"></a>Komponenter i budsjetteringsfunksjonaliteten
-------------------------------------

Ressursplanleggingssyklusen for et selskap består vanligvis av planlegging, budsjettering og prognoseaktiviteter.

[![Komponenter i budsjetteringsfunksjonaliteten](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

Prosessene for både langsiktig strategisk planlegging og årlig budsjettplanlegging støttes gjennom et budsjettplandokument. Budsjettplandokumenter er tett integrert med Microsoft Excel. Brukere kan konfigurere et ubegrenset antall monetære og kvantitative scenarier og kan også definere et organisasjonshierarki for budsjettering for å støtte metoder for budsjettering ovenfra og nedenfra. Når et budsjett er opprettet og godkjent i Finance and Operations, kan du konvertere budsjettplanen til en budsjettregisteroppføring. Budsjettregisteroppføringer har verktøy for å vedlikeholde budsjettet og holde beløp sporbare via budsjettkoder. Budsjettregisteroppføringer gjør at du kan endre opprinnelige budsjetter, utføre overføringer og overføre budsjettbeløp fra forrige år. Et firma kan aktivere budsjettkontroll basert på det etablerte budsjettet. Nivået av kontroll avhenger av organisasjonskulturen og modenhetsnivået for organisasjonen. Organisasjoner som har et lavt modenhetsnivå, kan la budsjettet være "som det er" og være mer reaktive enn proaktive hvis et budsjett ikke oppfyller forventningene. Andre organisasjoner kan aktivere policyer for budsjettkontroll som hindrer brukere fra å foreta kjøp hvis budsjettmidler ikke er tilgjengelige.

Svært modne organisasjoner kan opprette en organisasjonskultur der ansatte har kunnskap om organisasjonsmål og følger disse målene gjennom policyer, for eksempel «Vurder nettmøte i stedet for en reise». Finance and Operations omfatter et rammeverk for budsjettkontroll som lar ledelsen i firmaet velge hard kontroll (som forhindrer at posteringer går over budsjettet) eller myk kontroll (der brukere blir varslet om at de kommer til å overskride de tilgjengelige budsjettmidlene, men kan selv avgjøre hvordan de vil gå frem). Du kan også bruke rullerende prognoser. En rullerende prognose er en vanlig sammenligning av budsjettbeløp kontra faktiske beløp og brukes til å definere hvor bra firmaet gjør det med hensyn til budsjettet. En rullerende prognose brukes også til å identifisere trender. I Finance and Operations støttes rullerende prognoser – via et budsjettplandokument – som innledende planleggingsaktiviteter. Rullerende prognoser kan utføres parallelt med planleggingen for den kommende budsjettsyklusen.

-   [Grunnleggende budsjettering: Oversikt og konfigurasjon](basic-budgeting-overview-configuration.md)
-   [Budsjettkontroll: Oversikt og konfigurasjon](budget-control-overview-configuration.md)
-   [Budsjettplanlegging: Oversikt og konfigurasjon](budget-planning-overview-configuration.md)
-   [Stillingsprognose](position-forecasting.md)
-   [Justeringsdokumenter for budsjettplanlegging](budget-planning-justification-docs.md)
-   [Microsoft Excel-maler for budsjettplanlegging](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-finance-and-operations"></a>Budsjetteringsverktøy i Finance og Operations
[![Budsjetteringsverktøy](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Ytterligere funksjoner for planlegging og budsjettering er tilgjengelige i hele Finance and Operations og er integrert med finansbudsjetter.

-   **Arbeidsstyrkebudsjetter** – Arbeidsstyrkebudsjettering inneholder detaljert planlegging av budsjettkostnadskomponent for stillinger, kompensasjonsgrupper og så videre.
-   **Anleggsmiddelbudsjetter** – Basert på anleggsmiddelinformasjon kan du beregne planlagt avskrivning og registrere andre planlagte transaksjoner som er relaterte til anleggsmidler.
-   **Prosjektbudsjetter** – I prosjektmodulen kan du opprette detaljert prosjektprognoser. Prosjektprognosene vil inneholde informasjon om planlagte timer, utgifter, avgifter og varer.
-   **Behovsprognose** – Du kan beregne fremtidig beholdningsbehov og opprette behovsprognoser basert på historiske transaksjonsdata.

Hvis du vil ha informasjon om hvordan du kobler planlegging data fra andre moduler i budsjettplaner, kan du se [Integrasjon av budsjettplanlegging med andre moduler](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Brukergrensesnitt og rapporteringsfunksjonalitet
I Finance and Operations kan brukere kan opprette budsjettplaner direkte i Finance and Operations-klienten (ved hjelp av en konfigurerbar side for budsjettplandokument) eller via Excel. Excel har flere tilleggsfunksjoner. Du kan for eksempel bruke eksterne data som en kilde for en budsjettplan, foreta egendefinerte beregninger og bruke Microsoft pivottabeller og -diagrammer. Du kan konfigurere de fleste variablene i budsjettplanleggingsprosessen. 

Du kan for eksempel definere hvem som skal foreta budsjettering, hva som skal budsjetteres, og hvordan prosessen skal se ut. Selv om du kan bruke Excel til budsjettplanlegging, brukes Finance and Operations som eneste faktakilde og bidrar til å forhindre problemer med budsjettkontroll. Periodiske prosesser kan brukes til å hente inn innledende data for budsjettering i budsjettplanen. Når det gjelder rapportering, tilbyr Finance and Operations et sett med standard forespørselssider der du kan vise og analysere budsjetteringsdata. Du kan få tilgang til budsjettplandata via Management Reporter, og separate budsjettplanscenarier kan vises som kolonner i Management Reporter-rapporten.







