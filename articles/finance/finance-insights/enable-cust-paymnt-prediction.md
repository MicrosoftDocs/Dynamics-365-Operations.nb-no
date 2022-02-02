---
title: Aktiver kundebetalingsprognoser
description: Dette emnet forklarer hvordan du aktiverer og konfigurerer funksjonen for kundebetalingsprognoser i Finance Insights.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: 5002fc79842bef150892347a7ff4702b07cfe5be
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968893"
---
# <a name="enable-customer-payment-predictions"></a>Aktiver kundebetalingsprognoser

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du aktiverer og konfigurerer funksjonen for kundebetalingsprognoser i Finance Insights. Du aktiverer funksjonen i arbeidsområdet **Funksjonsbehandling** og angir konfigurasjonsinnstillinger på siden **Finance Insights-konfigurasjon**. Dette emnet inneholder også informasjon som kan hjelpe deg å bruke funksjonen på en effektiv måte.

> [!NOTE]
> Før du fullfører trinnene nedenfor, må du fullføre de nødvendige trinnene i emnet [Konfigurere for Finance Insights](configure-for-fin-insites.md).

1. Slik aktiverer du funksjonen for kundebetalingsforutsigelser:

    1. Åpne arbeidsområdet **Funksjonsbehandling**.
    2. Velg **Se etter oppdateringer**.
    3. Gå til **Alle**-fanen, og søk etter **Kundebetalingsforutsigelser**. Hvis du ikke funner denne funksjonen, søker du etter **(Forhåndsversjon) Kundebetalingsforutsigelser**. 
    4. Aktivere funksjonen.

    Funksjonen Kundebetalingsforutsigelser er nå aktivert og klar til å konfigureres.

2. Slik konfigurerer du funksjonen for innsikt i kundebetaling:

    1. Gå til **Kreditt og innkreving \> Oppsett \> Finance Insights \> Kundebetalingsforutsigelser**.
    2. Velg koblingen **Vis datafeltene som brukes i prognosemodellen** på fanen **Kundebetalingsforutsigelser** på siden **Finance Insights-konfigurasjon** for å åpne siden **Datafelter for prognosemodell**. Der kan du vise standardlisten over felt som brukes til å opprette en prognosemodell basert på kunstig intelligens (AI) for kundebetalingsprognoser.

        Hvis du vil bruke standardlisten over felt til å opprette en prognosemodell, lukker du siden **Datafelter for prognosemodell**, og deretter setter du alternativet **Aktiver funksjon** til **Ja** på siden **Finance Insights-konfigurasjon**.

    3. Angi transaksjonsperioden «svært sent» for å definere hva prognosesamlingen **Svært sent** betyr for firmaet.

        For hver åpne faktura forutsier systemet sannsynligheten for betaling i tre samlinger: **Til planlagt tid**, **For sent** og **Svært sent**.

        - **Til planlagt tid** – Denne samlingen inneholder betalinger som forutsies å bli betalt på eller før forfallsdatoen for transaksjonen.
        - **For sent** – Denne samlingen inneholder betalinger som forutsies å bli betalt etter forfallsdatoen for transaksjonen, men før starten på transaksjonsperioden Svært sent.
        - **Svært sent** – Denne samlingen inneholder betalinger som forutsies å bli betalt etter starten på transaksjonsperioden Svært sent.

        > [!NOTE]
        > Hvis du endrer transaksjonsperioden Svært sent og velger **Endre terskel for For sent** etter at AI-prognosemodellen for kundebetalinger er opprettet, slettes den eksisterende prognosemodellen, og det opprettes en ny modell. Den nye prognosemodellen flytter transaksjoner til Svært sent-perioden, basert på innstillingene som ble angitt for å definere den.

    4. Når du er ferdig å definere transaksjonsperioden Svært sent, velger du **Opprett prognosemodell** for å opprette en prognosemodell. **Prognosemodell**-delen på siden **Finance Insights-konfigurasjon** viser statusen for prognosemodellen.

        > [!NOTE]
        > Når du oppretter en prognosemodell, kan du når som helst velge **Tilbakestill modellopprettelse** for å starte prosessen på nytt.

    Funksjonen er nå konfigurert og klar til bruk.

Etter at funksjonen er aktivert og konfigurert, og prognosemodellen er opprettet og fungerer, viser **Prognosemodell**-delen på siden **Finance Insights-konfigurasjon** nøyaktigheten til modellen, som vist i illustrasjonen nedenfor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
