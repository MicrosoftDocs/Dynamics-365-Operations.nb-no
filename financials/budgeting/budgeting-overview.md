---
title: Startside for budsjettering
description: "Dette emnet gir en oversikt over budsjettering funksjonalitet komponentene, budsjettering verktøy og rapportering funksjoner i Microsoft Dynamics 365 for operasjoner."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: f7b4efc06b8e64c05da026850b41cb5b68c33ec3
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-home-page"></a>Startside for budsjettering

Dette emnet gir en oversikt over budsjettering funksjonalitet komponentene, budsjettering verktøy og rapportering funksjoner i Microsoft Dynamics 365 for operasjoner.

<a name="components-of-budgeting-functionality"></a>Komponenter i budsjetteringsfunksjonaliteten
-------------------------------------

Ressursplanleggingssyklusen for et selskap består vanligvis av planlegging, budsjettering og prognoseaktiviteter.
[![Budsjettering funksjonalitet komponenter](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg) prosesser for både langsiktig strategisk planlegging og årlige budsjettplanlegging støttes gjennom budsjettplandokument. Budsjettplandokumenter er tett integrert med Microsoft Excel. Brukere kan konfigurere et ubegrenset antall monetære og kvantitative scenarier og kan også definere et organisasjonshierarki for budsjettering for å støtte metoder for budsjettering ovenfra og nedenfra. Når et budsjett er opprettet og godkjent i Microsoft Dynamics 365 for Operations, kan du konvertere budsjettplanen til en budsjettregisteroppføring. Budsjettregisteroppføringer har verktøy for å vedlikeholde budsjettet og holde beløp sporbare via budsjettkoder. Budsjettregisteroppføringer gjør at du kan endre opprinnelige budsjetter, utføre overføringer og overføre budsjettbeløp fra forrige år. Et firma kan aktivere budsjettkontroll basert på det etablerte budsjettet. Nivået av kontroll avhenger av organisasjonskulturen og modenhetsnivået for organisasjonen. Organisasjoner som har et lavt modenhetsnivå, kan la budsjettet være "som det er" og være mer reaktive enn proaktive hvis et budsjett ikke oppfyller forventningene. Andre organisasjoner kan aktivere policyer for budsjettkontroll som hindrer brukere fra å foreta kjøp hvis budsjettmidler ikke er tilgjengelige. Til slutt, meget Moden organisasjoner kan opprette en organisatorisk kultur der ansatte er utdannet om organisasjonens mål og følger disse målene gjennom policyer som for eksempel "Kanskje du bør elektronisk møte i stedet for en reise." Dynamics 365 for operasjoner omfatter et rammeverk for budsjett-kontroll som lar firmaets management velger enten harde kontroll (som hindrer posteringer som vil gå over budsjettet) eller myke kontroll (der brukerne blir advart om at de vil overskride tilgjengelig budsjettmidlene, men kan bestemme for seg selv til å fortsette). Du kan bruke rullende prognoser. En rullende prognose er en vanlig sammenligning av budsjettet med faktiske data, og brukes til å definere hvor bra firmaet opererer mot budsjettet. En rullerende prognose brukes også til å identifisere trender. I Microsoft Dynamics 365 for Operations støttes rullerende prognoser – via et budsjettplandokument – som innledende planleggingsaktiviteter. Rullerende prognoser kan utføres parallelt med planleggingen for den kommende budsjettsyklusen.

-   [Grunnleggende budsjettering: Oversikt og konfigurasjon](basic-budgeting-overview-configuration.md)
-   [Budsjettkontroll: Oversikt og konfigurasjon](budget-control-overview-configuration.md)
-   [Budsjettplanlegging: Oversikt og konfigurasjon](budget-planning-overview-configuration.md)
-   [Stillingsprognoser](position-forecasting.md)
-   [Budsjett planleggingsdokumenter justering](budget-planning-justification-docs.md)
-   [Microsoft Excel-maler for budsjettplanlegging](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Budsjetteringsverktøy i Dynamics 365 for Operations
[![Budsjettering verktøy](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Ytterligere funksjoner for planlegging og budsjettering er tilgjengelige i hele Dynamics 365 for Operations og er integrert med finansbudsjetter.

-   **Arbeidsstyrkebudsjetter** – Arbeidsstyrkebudsjettering inneholder detaljert planlegging av budsjettkostnadskomponent for stillinger, kompensasjonsgrupper og så videre.
-   **Anleggsmiddelbudsjetter** – Basert på anleggsmiddelinformasjon kan du beregne planlagt avskrivning og registrere andre planlagte transaksjoner som er relaterte til anleggsmidler.
-   **Prosjektbudsjetter** – I prosjektmodulen kan du opprette detaljert prosjektprognoser. Prosjektprognosene vil inneholde informasjon om planlagte timer, utgifter, avgifter og varer.
-   ** Krever prognostisering ** – basert på historiske transaksjonsdata, kan du beregne behov for fremtidige lager og opprette behovsprognoser.

Hvis du vil ha informasjon om hvordan du kobler planlegging data fra andre moduler i budsjettplaner, kan du se [Integrasjon av budsjettplanlegging med andre moduler](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Brukergrensesnitt og rapporteringsfunksjonalitet
I Microsoft Dynamics 365 for Operations kan brukere kan opprette budsjettplaner direkte i Microsoft Dynamics 365 for Operations-klienten (ved hjelp av en konfigurerbar side for budsjettplandokument) eller via Excel. Excel har flere tilleggsfunksjoner. Du kan for eksempel bruke eksterne data som en kilde for en budsjettplan, foreta egendefinerte beregninger og bruke Microsoft pivottabeller og -diagrammer. Du kan konfigurere de fleste variablene i budsjettplanleggingsprosessen. Du kan for eksempel definere hvem som skal foreta budsjettering, hva som skal budsjetteres, og hvordan prosessen skal se ut. Selv om du kan bruke Excel til budsjettplanlegging, brukes Dynamics 365 for Operations som eneste faktakilde og bidrar til å forhindre problemer med budsjettkontroll. Periodiske prosesser kan brukes til å hente inn innledende data for budsjettering i budsjettplanen. Når det gjelder rapportering, tilbyr Dynamics 365 for Operations et sett med standard forespørselssider der du kan vise og analysere budsjetteringsdata. Du kan få tilgang til budsjettplandata via Management Reporter, og separate budsjettplanscenarier kan vises som kolonner i Management Reporter-rapporten.





