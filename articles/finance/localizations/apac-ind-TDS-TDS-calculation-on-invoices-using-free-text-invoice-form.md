---
title: TDS-beregning for fakturaer fra siden Fritekstfaktura
description: Dette emnet forklarer hvordan du beregner TDS (Tax Deducted at Source) for fakturaer ved hjelp av siden Fritekstfaktura.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023484"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>TDS-beregning for fakturaer fra siden Fritekstfaktura

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du beregner TDS (Tax Deducted at Source) for fakturaer ved hjelp av siden **Fritekstfaktura**.

1. Gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer**.

    [![Siden Fritekstfaktura](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Velg **Ny** for å opprette en fritekstfaktura, og angi de nødvendige detaljene.
3. Velg **Faktura**-fanen. Feltet **Skattebetalertype** i delen **Kildeskattgruppe** viser kategorien for skattebetalertype for leverandøren eller kunden.
4. Gå gjennom eller endre standard TDS-gruppe som er definert for kunden, i feltet **TDS-gruppe**.

    > [!NOTE]
    > Når du velger en verdi i feltet **TDS-gruppe**, blir feltet **TCS-gruppe** utilgjengelig. TDS beregnes bare hvis alternativet **Beregn kildeskatt** er satt til **Ja** for kunden på siden **Alle kunder**.

5. Velg selskapsnavnet for en alternativ adresse som er konfigurert for selskapet, i **Navn**-feltet i delen **Selskapsopplysninger** i fanen **Avgiftsinformasjon**.

    Feltet **TAN-nummer (Tax Account Number)** i **Kildeskatt**-delen viser TAN-nummeret for det valgte selskapet.

6. Opprett fakturalinjer i **Fakturalinjer**-fanen, og angi de nødvendige detaljene.

    Feltet **TAN-nummer (Tax Account Number)** i delen **Kildeskattgruppe** viser TAN-nummeret, og feltet **TDS-gruppe** viser TDS-gruppen.

7. Velg **Kildeskatt** for å åpne siden **Midlertidige kildeskattransaksjoner**. Den øvre delen av denne siden inneholder følgende felter:

    - **Kildeskattbeløp totalt** – Det totale TDS-beløpet som ble beregnet for transaksjonen for TDS-gruppen.
    - **Verdi** – Den totale prosentsatsen som ble brukt til å beregne TDS for transaksjonen. Den totale prosentsatsen er basert på formelen som er definert for TDS-avgiftskodene og er knyttet til TDS-gruppen.
    - **Justert kildeskattbeløp totalt** – Det totale justerte TDS-beløpet for alle avgiftskodene i TDS-gruppen.
    - **TDS** – En avmerket avmerkingsboks angir at en TDS-gruppe er knyttet til transaksjonen.

    Feltene i fanen **Oversikt**, **Generelt** og **Justering** viser det beregnede TDS-beløpet og detaljene for det justerte TDS-beløpet for hver TDS-avgiftskode som er knyttet til TDS-gruppen.

8. Velg **Terskel** for å åpne **Terskel**-siden, der du kan gå gjennom terskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til en bestemt TDS-avgiftskode.
9. Velg **Formeldesigner** for å åpne **Formeldesigner**-siden, der du kan gå gjennom formelen som er definert for en bestemt TDS-avgiftskode.
10. Poster fritekstfakturaen. TDS-beløpet som beregnes for fritekstfakturaen, posteres på kundereskontroen som er definert for hver TDS-avgiftskode i TDS-gruppen. Kundereskontroene for TDS-avgiftskoder defineres på siden **Kildeskattkoder**.
11. Velg **Postert kildeskatt** for å åpne siden **Kildeskattransaksjoner**. **Verdi**-feltet viser den totale prosentsatsen som ble brukt til å beregne TDS for transaksjonen.

    Feltene i fanene **Oversikt**, **Generelt** og **Beløp** viser TDS-beløpene som ble beregnet på fakturalinjene.

12. Gå gjennom TDS-beregningsinformasjonen for hver TDS-avgiftskode som er knyttet til TDS-gruppen.
