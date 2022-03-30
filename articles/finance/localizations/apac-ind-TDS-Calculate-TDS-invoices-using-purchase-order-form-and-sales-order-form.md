---
title: Beregne TDS-fakturaer ved hjelp av bestillingsskjema og salgsordreskjema
description: Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for ulike fakturatyper.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 28f83b3d5aa028d819b837350fe69c2a9c9833ea
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407875"
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

   - **Kilde****skatt****beløp** **tot****talt** – Det totale TDS-beløpet som ble beregnet for transaksjonen for TDS-gruppen.

   - **Verdi** – Den totale prosentsatsen som brukes til å beregne TDS for transaksjonen. Den totale prosentsatsen er basert på formelen som er definert for TDS-avgiftskoder knyttet til TDS-gruppen.

   - **Justert kildeskattbeløp totalt** – Det totale justerte TDS-beløpet for alle avgiftskodene i TDS-gruppen.

   - **TDS** – Hvis dette er valgt, knyttes en TDS-gruppe til transaksjonen.

Feltene i fanen **Oversikt**, **Generelt** og **Justering** på siden **Midlertidige kildeskattransaksjoner** viser det beregnede TDS-beløpet og de justerte TDS-beløpsdetaljene for hver TDS-avgiftskode som er knyttet til TDS-gruppen.

8. Velg **Terskel** for å åpne **Terskel**-siden. Vis terskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til en bestemt TDS-avgiftskode på denne siden.

9. Velg **Formeldesigner** for å åpne **Formeldesigner**-siden. Vis formelen som er definert for en bestemt TDS-avgiftskode på denne siden. 

10. Poster fakturaen. TDS-beløpet som beregnes for innkjøpsfakturaer, posteres på leverandørreskontroen, og TDS-beløpet som beregnes for salgsfakturaer, posteres på kundereskontroen som er definert for hver TDS-avgiftskode i TDS-gruppen. Leverandørreskontroene eller kundereskontroene for TDS-avgiftskoder defineres på siden **Kildeskattkoder**.

11. Velg **Forespørsel**-knappen **> Faktura > Postert kildeskatt**-knappen for å åpne siden **Kildeskattransaksjoner**. Du kan vise den totale prosentsatsen som brukes til å beregne TDS for transaksjonen, i **Verdi**-feltet.

Feltene i fanene **Oversikt**, **Generelt** og **Beløp** på siden **Kildeskattransaksjoner** viser informasjon om TDS som er beregnet for transaksjonen. Vis TDS-beregningsinformasjonen for hver TDS-avgiftskode knyttet til TDS-gruppen.
