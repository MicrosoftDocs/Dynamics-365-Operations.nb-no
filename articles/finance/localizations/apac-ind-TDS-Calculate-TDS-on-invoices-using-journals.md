---
title: Beregne TDS for fakturaer ved hjelp av journaler
description: Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for journaler.
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
ms.openlocfilehash: 5e7654a4e593ab5328077deb571d6e2220fd1385
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407617"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>Beregne TDS for fakturaer ved hjelp av journaler

[!include [banner](../includes/banner.md)]

Dette emnet viser fremgangsmåten for beregning av TDS (Tax Deducted at Source) for journaler.

Begynn ved å åpne **Økonomijournaler**-siden (**Økonomimodul > Journaloppføringer > Økonomijournaler**).

[![Økonomijournaler.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Opprett journallinjer ved hjelp av journalskjemaene som vises i tabellen. Velg kontotypen og motkontotypen, og angi beløpet for transaksjonen. 

   > [!NOTE]
   > Velg **Finn bilag** på siden **Fakturagodkjenningsjournal**, og velg fakturaer du vil beregne TDS for. Vis fakturaene som er opprettet på siden **Ankomstregistrering** eller **Finn bilag**-siden.  

2. Vis eller endre standard TDS-gruppe som er definert for leverandøren eller kunden, i feltet **TDS-gruppe** i **Oversikt**-fanen på **Journalbilag**-siden. TDS-beløpet som beregnes på journallinjer, er basert på formelen som er definert for TDS-avgiftskodene i feltet **TDS-gruppe**. 

   > [!NOTE]
   > Feltene **Kildeskattgruppe** og **TCS-gruppe** blir utilgjengelige når du velger en TDS-gruppe i feltet **TDS-gruppe**. Feltet **Kildeskattgruppe** er bare tilgjengelig på siden **Økonomijournal**. TDS beregnes bare hvis det er merket av for **Beregn kildeskatt** for leverandøren eller kunden på siden **Alle leverandører** eller **Alle kunder**.   

3. Velg fanen **Avgiftsinformasjon**. Velg de alternative adressene til et selskap som er konfigurert for selskapet i dette feltet, hvis det er nødvendig. Du kan vise selskapsnavnet i **Navn**-feltet, som er i feltgruppen **Selskapsopplysninger**. 

4. Vis kategorien for skattebetalertype for leverandøren eller kunden i feltet **Skattebetalertype**, som er i feltgruppen **Kildeskatt**. Vis TAN-nummeret til det valgte selskapsnavnet som vises, i feltet **TAN-nummer** (**Tax Account Number**).  

5. Velg **Kildeskatt** på **Kildeskatt**-menyen for å åpne siden **Midlertidige kildeskattransaksjoner**. Følgende felter vises i den øvre ruten på siden **Midlertidige kildeskattransaksjoner**.

   - **Kildeskattbeløp totalt** – Det totale TDS-beløpet som ble beregnet for transaksjonen for TDS-gruppen.

   - **Verdi** – Den totale prosentsatsen som brukes til å beregne TDS for transaksjonen. Den totale prosentsatsen er basert på formelen som er definert for TDS-avgiftskoder knyttet til TDS-gruppen.

   - **Justert kildeskattbeløp totalt** – Det totale justerte TDS-beløpet for alle avgiftskodene i TDS-gruppen.

   - **TDS** – Hvis dette er valgt, knyttes en TDS-gruppe til transaksjonen.

  Feltene i fanen **Oversikt**, **Generelt** og **Justering** på siden **Midlertidige kildeskattransaksjoner** viser det beregnede TDS-beløpet og de justerte TDS-beløpsdetaljene for hver TDS-avgiftskode som er knyttet til TDS-gruppen.

6. Velg **Terskel** for å åpne **Terskel**-siden. Vis terskelgrensen og unntaksterskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til en bestemt TDS-avgiftskode på denne siden.

   Velg **Formeldesigner** for å åpne **Formeldesigner**-skjemaet. Vis formelen som er definert for en bestemt TDS-avgiftskode på denne siden. Lukk sidene **Formeldesigner** og **Midlertidige kildeskattransaksjoner** for å gå tilbake til **Journalbilag**-siden.

8. Angi de andre nødvendige opplysningene. Valider og poster journalen. TDS-beløpet som er beregnet for innkjøpsfakturaer, posteres på leverandørreskontroen. TDS-beløpet som beregnes for salgsfakturaer, posteres på kundereskontroen som er definert for hver TDS-avgiftskode i TDS-gruppen. Leverandørreskontroene eller kundereskontroene for TDS-avgiftskoder defineres på siden **Kildeskattkoder**.

9. Velg **Postert kildeskatt** for å åpne siden **Kildeskattransaksjoner**. I **Verdi**-feltet vises den totale prosentsatsen som brukes til å beregne TDS for transaksjonen.

   Feltene i fanene **Oversikt**, **Generelt** og **Beløp** på siden Kildeskattransaksjoner viser det beregnede TDS-beløpet og de justerte TDS-beløpsdetaljene for hver TDS-avgiftskode som er knyttet til TDS-gruppen.
