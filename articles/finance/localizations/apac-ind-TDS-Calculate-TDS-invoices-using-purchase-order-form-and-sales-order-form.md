---
title: Beregne TDS-fakturaer ved hjelp av bestillingsskjema og salgsordreskjema
description: Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for ulike fakturatyper.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023468"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Beregne TDS-fakturaer ved hjelp av bestillingsskjema og salgsordreskjema

[!include [banner](../includes/banner.md)]

Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for ulike fakturatyper ved hjelp av sidene **Bestilling**, **Innkjøpsjournal**, **Rammebestilling** og **Salgsordre**.

1. Opprett en bestilling, innkjøpsjournal, rammebestilling eller salgsordre ved hjelp av siden som vises. Angi de nødvendige detaljene.

2. Velg **Oppsett**-fanen for å vise skattebetalertypen for leverandøren eller kunden. Denne informasjonen vises i feltet **Skattebetalertype** i feltgruppen **Kildeskattgruppe**.

3. Vis eller endre standard TDS-gruppe som er definert for leverandøren eller kunden, i feltet **TDS-gruppe**.

   > [!NOTE]
   > Feltet **TCS-gruppe** er ikke tilgjengelig når du velger en TDS-gruppe i feltet **TDS-gruppe**. TDS beregnes bare hvis det er merket av for **Beregn kildeskatt** for leverandøren eller kunden på siden **Alle leverandører** eller **Alle kunder**.  

4. Opprett varelinjer i **Linjer**-fanen, og angi de nødvendige detaljene.

5. Velg **Oppsett**-fanen (linjenivå) for å vise eller endre TDS-gruppen som er definert på hodenivået. TDS-gruppen vises i feltet **TDS-gruppe**, som er i feltgruppen **Kildeskattgruppe**.

6. Velg fanen **Avgiftsinformasjon**, og velg alternative adresser som er konfigurert for selskapsnavnet som vises i dette feltet. Selskapsnavnet vises i **Navn**-feltet, som er i feltgruppen **Selskapsopplysninger**. 

   TAN-nummeret for det valgte selskapsnavnet vises i feltet **TAN-nummer** (**Tax Account Number**) i feltgruppen **Kildeskatt**. 

7. Velg **Kildeskatt** for å åpne siden **Midlertidige kildeskattransaksjoner**. Vis følgende felter i den øvre ruten på siden **Midlertidige kildeskattransaksjoner**.

   - **Kildeskattbeløp** **totalt** – Det totale TDS-beløpet som ble beregnet for transaksjonen for TDS-gruppen.

   - **Verdi** – Den totale prosentsatsen som brukes til å beregne TDS for transaksjonen. Den totale prosentsatsen er basert på formelen som er definert for TDS-avgiftskoder knyttet til TDS-gruppen.

   - **Justert kildeskattbeløp totalt** – Det totale justerte TDS-beløpet for alle avgiftskodene i TDS-gruppen.

   - **TDS** – Hvis dette er valgt, knyttes en TDS-gruppe til transaksjonen.

Feltene i fanen **Oversikt**, **Generelt** og **Justering** på siden **Midlertidige kildeskattransaksjoner** viser det beregnede TDS-beløpet og de justerte TDS-beløpsdetaljene for hver TDS-avgiftskode som er knyttet til TDS-gruppen.

8. Velg **Terskel** for å åpne **Terskel**-siden. Vis terskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til en bestemt TDS-avgiftskode på denne siden.

9. Velg **Formeldesigner** for å åpne **Formeldesigner**-siden. Vis formelen som er definert for en bestemt TDS-avgiftskode på denne siden. 

10. Poster fakturaen. TDS-beløpet som beregnes for innkjøpsfakturaer, posteres på leverandørreskontroen, og TDS-beløpet som beregnes for salgsfakturaer, posteres på kundereskontroen som er definert for hver TDS-avgiftskode i TDS-gruppen. Leverandørreskontroene eller kundereskontroene for TDS-avgiftskoder defineres på siden **Kildeskattkoder**.

11. Velg **Forespørsel**-knappen **> Faktura > Postert kildeskatt**-knappen for å åpne siden **Kildeskattransaksjoner**. Du kan vise den totale prosentsatsen som brukes til å beregne TDS for transaksjonen, i **Verdi**-feltet.

Feltene i fanene **Oversikt**, **Generelt** og **Beløp** på siden **Kildeskattransaksjoner** viser informasjon om TDS som er beregnet for transaksjonen. Vis TDS-beregningsinformasjonen for hver TDS-avgiftskode knyttet til TDS-gruppen.
