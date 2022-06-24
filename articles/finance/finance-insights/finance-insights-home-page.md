---
title: Startside for Finance Insights
description: Finance Insights gir konfigurerbare og utvidbare modeller som hjelper deg med å forutse firmaets kontantstrøm nøyaktig og intelligent, forutser når du skal motta betaling for utestående fordringer, og genererer et budsjettforslag som kan gjøre budsjettprosessen raskere. Alle disse funksjonene er basert på intelligente maskinlæringsmodeller.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 42ea8884c357bcb26ac96df8dca75e7ff449d4f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881969"
---
# <a name="finance-insights-home-page"></a>Startside for Finance Insights

[!include [banner](../includes/banner.md)]

Finance Insights gir konfigurerbare og utvidbare løsninger som hjelper deg med å forutse firmaets kontantstrøm på en intelligent måte, forutser når du skal motta betaling for utestående fordringer, og genererer et budsjettforslag som kan gjøre budsjettprosessen raskere. Disse funksjonene bruker intelligente maskinlæringsmaler for å bygge modeller ved hjelp av data du tilbyr (inkludert data fra en tredjepart, for eksempel informasjon om forbrukerrapport fra et byrå). Disse intelligente funksjonene informerer beslutningstakere, og hjelper deg med å gjøre noe for å respondere effektivt på aktuelle og forventede forretningsutfordringer. Du er ansvarlig for alle data som brukes med, eller utdata fra, Finance Insights.

> [!NOTE]
> Finance Insights er tilgjengelig for distribusjoner i USA, Canada, Storbritannia, Europa, Asia/Stillehavskysten, Japan, Australia og New Zealand. Microsoft legger gradvis til støtte for flere områder.

## <a name="prerequisites"></a>Forutsetninger

Denne delen viser kravene til bruk av Finance Insights. Når det er mulig, finner du koblinger til kilder med tilleggsinformasjon.

### <a name="system-requirements"></a>Systemkrav

Et lag 2-miljø (flerboks) kreves for å forhåndsvise Finance Insights. Hvis du vil ha bakgrunnsinformasjon om miljøene, se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

### <a name="version-requirements"></a>Versjonskrav

Denne artikkelen gjelder for Microsoft Dynamics 365 Finance versjon 10.0.21 og nyere.

### <a name="license-requirements"></a>Lisenskrav

Finance Insights bruker AI Builder-kreditter for å opprette økonomiske prognoser. Alle nødvendige lisenser for dette følger med leierlisensen. Hver Dynamics 365 Finance-leier får 20 000 AI Builder-kreditter hver måned. Hvis det kreves flere kreditter for forretningsbehov, kan de kjøpes direkte fra AI Builder.

### <a name="historical-data-requirements"></a>Historiske datakrav

Minst ett års med kundefakturaer kreves for å lære opp maskinlæringsmodellen som brukes for funksjonen for kundebetalingspredisjoner. Det anbefales tre år med historiske data for kontantstrømprognoser. Det anbefales at du bruker tre år med historisk budsjett og/eller faktiske budsjettforslag.

## <a name="configure-finance-insights"></a>Konfigurer Finance Insights

Du må fullføre noen konfigurasjonstrinn før du kan bruke Finance Insights. Hvis du vil ha mer informasjon om hvordan du konfigurerer Finance Insights, kan du se [Konfigurasjon for Finance Insights](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Opprette et dataintegreringsprosjekt

Du må opprette et dataintegreringsprosjekt, slik at data som maskinlæringsmodellen genererer, kan flyte inn i Dynamics 365 Finance. Hvis du vil ha en fremgangsmåte for å opprette prosjektet, se [Opprette et dataintegreringsprosjekt](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Aktivere Finance Insights-funksjoner

Når du har fullført konfigurasjonstrinnene og konfigurert demodata, må du aktivere og definere hver funksjon du planlegger å bruke: kundebetalingsprediksjoner, kontantstrømprognoser og budsjettforslag.

### <a name="enable-customer-payment-predictions"></a>Aktivere kundebetalingsprognoser
Hvis du bruker demodata til å teste kundebetalingsprediksjoner, må du kanskje importere flere demodata for å opprette AI-modellen på en vellykket måte. 

Hvis du vil aktivere kundebetalingsprediksjoner, må du fullføre et sett med trinn for å bygge en maskinlæringsmodell som bruker organisasjonens data til å generere prediksjoner om når kunder sannsynligvis vil betale utestående fakturaer, og når bestemte fakturaer sannsynligvis vil bli betalt. Hvis du vil ha mer informasjon og de spesifikke trinnene som skal fullføres, kan du se [Aktivere kundebetalingsprognoser](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Aktivere kontantstrømprognose
Hvis du vil aktivere kontantstrømprognoser, må du fullføre et sett med trinn for å bygge en maskinlæringsmodell som bruker organisasjonens data til å generere kontantstrømprognoser. Hvis du vil ha mer informasjon og de spesifikke trinnene som skal fullføres, kan du se [Aktivere kontantstrømprognose](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Aktivere budsjettforslag

Budsjettforslagsfunksjonen bruker en maskinlæringsmodell sammen med organisasjonens historiske data til å generere et budsjettforslag. Det genererte forslaget kan hjelpe deg med å begynne en budsjettprosess som er mer effektiv enn en manuell prosess. Hvis du vil ha de spesifikke trinnene for å aktivere denne funksjonen, kan du se [Aktivere budsjettforslag](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Bruke Finance Insights-funksjoner

### <a name="using-customer-payment-predictions"></a>Bruke kundebetalingsforutsigelser

- Hvis du vil vite hvordan kundebetalingsprediksjoner kan gi informasjonen som kreves for proaktivt å samle inn kundebetalinger, se [Bruke kundebetalingsprediksjoner](use-customer-payment-predictions.md).
- Hvis du vil ha informasjon som kan hjelpe deg med å vurdere effektiviteten av forutsigelsesmodellen etter at du har begynt å bruke funksjonen, kan du se [Evaluere den opprinnelige forutsigelsesmodellen for kundebetaling](evaluate-payment-prediction.md).
- Hvis du vil ha informasjon som kan hjelpe deg med å justere dataene som brukes til å bygge opp forutsigelsen, og dermed forbedre effektiviteten, kan du se [Forbedre forutsigelsesmodellen](improve-model.md).
- Hvis du vil ha mer informasjon om resultatene av AI-prediksjonsmodellene, kan du se [Resultat av maskinlæringsmodeller](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Bruke kontantstrømprognoser

Funksjonen for kontantstrømprognose kan hjelpe deg å anslå likviditetsbeholdningen på en mer nøyaktig måte. Intelligent kontantstrømprognose er bygd på toppen av eksisterende funksjonalitet for kontantstrømprognose i Dynamics 365 Finance. Hvis du vil se gjennom den eksisterende muligheten, se [Kontantstrømprognose](../cash-bank-management/cash-flow-forecasting.md).

- Hvis du vil ha informasjon om de nye funksjonene i kontantstrømprognoser, kan du se [Kontantstrømprognose](cash-flow-forecast-intro.md).
- Hvis du vil ha informasjon om hvordan du importerer eksterne data som skal inkluderes i kontantstrømprognosen her, kan du se [Bruke eksterne data i kontantstrømprognoser](external-data-in-cash-flow.md). 
- Hvis du vil ha informasjon om hvordan du bruker en AI-modell til å projisere kortsiktig kontantstrøm, kan du se [Likviditetsbeholdning](cash-position.md).
- Hvis du vil ha informasjon om hvordan du lagrer kontantstrømbeholdninger og kontantstrømprognoser som øyeblikksbilder og sammenligner øyeblikksbilder med faktiske data, kan du se [Oversikt over øyeblikksbilder](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Bruke budsjettforslag

Hvis du vil ha informasjon om hvordan du gjør opprettelsen av et budsjett raskere, kan du se [Budsjettforslag](budget-proposals.md). 

## <a name="feedback-and-support"></a>Tilbakemelding og støtte

Hvis du er interessert i å gi tilbakemelding eller trenger kundestøtte, kan du sende en e-postmelding til [Finance Insights](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
