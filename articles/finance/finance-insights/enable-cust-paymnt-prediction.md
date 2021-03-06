---
title: Aktivere kundebetalingsprognoser (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer og konfigurerer funksjonen for kundebetalingsprognoser i Finance Insights.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222592"
---
# <a name="enable-customer-payment-predictions-preview"></a>Aktivere kundebetalingsprognoser (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet forklarer hvordan du aktiverer og konfigurerer funksjonen for kundebetalingsprognoser i Finance Insights. Du aktiverer funksjonen i arbeidsområdet **Funksjonsbehandling** og angir konfigurasjonsinnstillinger på siden **Parametere for økonomisk innsikt**. Dette emnet inneholder også informasjon som kan hjelpe deg å bruke funksjonen på en effektiv måte.

> [!NOTE]
> Før du fullfører trinnene nedenfor, må du fullføre de nødvendige trinnene i emnet [Konfigurere for Finance Insights](configure-for-fin-insites.md).

1. Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet. Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet. (Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > Hopp over dette trinnet hvis du bruker versjon 10.0.20 eller nyere, eller hvis du bruker en Service Fabric-distribusjon. Finance Insights-teamet skal allerede ha aktivert testversjonen for deg. Hvis du ikke ser funksjonen i arbeidsområdet **Funksjonsbehandling** eller får problemer når du prøver å aktivere den, kontakter du <fiap@microsoft.com>. 

2. Slik aktiverer du funksjonen for innsikt i kundebetaling:

    1. Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**.
    2. Finn funksjonen kalt **Innsikt i kundebetaling (forhåndsversjon)**.
    3. Velg **Aktiver nå**.

    Funksjonen for innsikt i kundebetaling er nå aktivert og klar til å konfigureres.

3. Slik konfigurerer du funksjonen for innsikt i kundebetaling:

    1. Gå til **Kreditt og innkreving \> Oppsett \> Finance Insights \> Parametere for økonomisk innsikt**.

        [![Siden Parametere for økonomisk innsikt før funksjonen er konfigurert](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Velg koblingen **Vis datafeltene som brukes i prognosemodellen** i fanen **Innsikt i kundebetaling** på siden **Parametere for økonomisk innsikt** for å åpne siden **Datafelter for prognosemodell**. Der kan du vise standardlisten over felt som brukes til å opprette en prognosemodell basert på kunstig intelligens (AI) for kundebetalingsprognoser.

        Hvis du vil bruke standardlisten over felt til å opprette en prognosemodell, lukker du siden **Datafelter for prognosemodell**, og deretter setter du alternativet **Aktiver funksjon** til **Ja** på siden **Parametere for økonomisk innsikt**.

    3. Angi transaksjonsperioden «svært sent» for å definere hva prognosesamlingen **Svært sent** betyr for firmaet.

        For hver åpne faktura forutsier systemet sannsynligheten for betaling i tre samlinger: **Til planlagt tid**, **For sent** og **Svært sent**.

        - **Til planlagt tid** – Denne samlingen inneholder betalinger som forutsies å bli betalt på eller før forfallsdatoen for transaksjonen.
        - **For sent** – Denne samlingen inneholder betalinger som forutsies å bli betalt etter forfallsdatoen for transaksjonen, men før starten på transaksjonsperioden Svært sent.
        - **Svært sent** – Denne samlingen inneholder betalinger som forutsies å bli betalt etter starten på transaksjonsperioden Svært sent.

        > [!NOTE]
        > Hvis du endrer transaksjonsperioden Svært sent og velger **Endre terskel for For sent** etter at AI-prognosemodellen for kundebetalinger er opprettet, slettes den eksisterende prognosemodellen, og det opprettes en ny modell. Den nye prognosemodellen flytter transaksjoner til Svært sent-perioden, basert på innstillingene som ble angitt for å definere den.

    4. Når du er ferdig å definere transaksjonsperioden Svært sent, velger du **Opprett prognosemodell** for å opprette en prognosemodell. **Prognosemodell**-delen på siden **Parametere for økonomisk innsikt** viser statusen for prognosemodellen.

        > [!NOTE]
        > Når du oppretter en prognosemodell, kan du når som helst velge **Tilbakestill modellopprettelse** for å starte prosessen på nytt.

    Funksjonen er nå konfigurert og klar til bruk.

Etter at funksjonen er aktivert og konfigurert, og prognosemodellen er opprettet og fungerer, viser **Prognosemodell**-delen på siden **Parametere for økonomisk innsikt** nøyaktigheten til modellen, som vist i illustrasjonen nedenfor.

[![Nøyaktigheten til prognosemodellen på siden Parametere for økonomisk innsikt](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Frigivelsesdetaljer

Den offentlige forhåndsversjonen av Finance Insights er tilgjengelig for prøvedistribusjoner i USA, Europa og Storbritannia. Microsoft legger gradvis til støtte for flere områder.

Funksjoner i offentlige forhåndsversjoner kan og bør bare aktiveres i sandkassemiljøer på lag 2. Oppsett og modeller for kunstig intelligens som er opprettet i et sandkassemiljø, kan ikke overføres til et produksjonsmiljø. Hvis du vil ha mer informasjon, kan du se [Ekstra vilkår for bruk for Microsoft Dynamics 365-forhåndsversjoner](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
