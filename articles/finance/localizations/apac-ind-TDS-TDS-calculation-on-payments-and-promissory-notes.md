---
title: TDS-beregning for betalinger og egenveksler
description: Dette emnet gir referanseinformasjon om de ulike betalingstransaksjonene som TDS (Tax Deducted at Source) beregnes ut fra.
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
ms.openlocfilehash: d5c9822c2e4f71fb89776d1c1c76056bad85d484
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407667"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>TDS-beregning for betalinger og egenveksler

[!include [banner](../includes/banner.md)]

Dette emnet gir referanseinformasjon om de ulike betalingstransaksjonene som TDS (Tax Deducted at Source) beregnes ut fra.

| Serienummer | Transaksjonstype | Transaksjonsbeløp | Sidenavn og -bane | Kontotype og motkontotype |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Forskuddsbetaling/betaling mot faktura (TDS skyldig) | Debet eller kredit | <ul><li>Økonomijournal (**Økonomimodul \> Journaloppføringer \> Økonomijournaler**)</li><li>Fakturajournal (**Leverandører \> Fakturaer \> Fakturajournal**)</li><li>Betalingsjournal (**Leverandører \> Betalinger \> Leverandørbetalingsjournal**)</li></ul> | Leverandør (debet), Bank (kredit) |
| 2             | Forskuddsbetaling/betaling mot faktura (innkjøp fra kunde – TDS skyldig) | Debet eller kredit | <ul><li>Økonomijournal (**Økonomimodul \> Journaloppføringer \> Økonomijournaler**)</li><li>Fakturajournal (**Leverandører \> Fakturaer \> Fakturajournal**)</li><li>Betalingsjournal (**Leverandører \> Betalinger \> Leverandørbetalingsjournal**)</li></ul> | Kunde (debet), Bank (kredit) |
| 3             | Egenveksler | Debet | Journal for egenvekseltrekking (**Leverandører \> Betalinger \> Egenveksler \> Journal for egenvekseltrekking**) | Leverandør (debet), Finans (kredit) |
| 4             | Diverse inntekt (TDS til gode) | Debet eller kredit | Økonomijournal (**Økonomimodul \> Journaloppføringer \> Økonomijournaler**) | Bank (debet), Finans (kredit) |
| 5             | Andre utgifter (TDS skyldig) | Debet eller kredit | Økonomijournal (**Økonomimodul \> Journaloppføringer \> Økonomijournaler**) | Bank (debet), Finans (kredit) |

Følg denne fremgangsmåten for å beregne TDS for betalinger og egenveksler.

1. Opprett journallinjer på journalsidene. Velg kontotypen og motkontotypen.
2. Velg **Funksjoner \> Utligning** for å åpne siden **Åpen transaksjonsredigering**. Velg deretter en bestemt faktura som må utlignes. Hvis TDS allerede er beregnet på fakturanivået, inneholder feltet **Beløpsgrunnlag** grunnlagsbeløpet som TDS ble beregnet på. Feltet **TDS-beløp** viser TDS-beløpet som ble beregnet for transaksjonen. **Beløp**-feltet viser netto betalingsbeløp (det vil si betalingsbeløpet etter at TDS er trukket fra).

    > [!NOTE]
    > Følgende betingelser gjelder for en betaling som ble foretatt mot en faktura:
    >
    > - Hvis betalingsbeløpet og fakturabeløpet er like, beregnes ikke TDS hvis den allerede er beregnet på fakturanivået.
    > - Hvis fakturabeløpet er større enn betalingsbeløpet etter at TDS-beløpet er trukket fra, beregnes ikke TDS.
    > - Hvis fakturabeløpet er mindre enn betalingsbeløpet etter at TDS-beløpet er trukket fra, beregnes TDS for beløpet som overskrider fakturabeløpet.

3. Gå gjennom eller endre standard TDS-gruppe som er definert for leverandøren eller kunden, i feltet **TDS-grupper** i **Oversikt**-fanen på **Journalbilag**-siden. TDS som beregnes på journallinjer, er basert på formelen som er definert for TDS-avgiftskodene i TDS-gruppen.

    > [!NOTE]
    > TDS beregnes bare hvis alternativet **Beregn kildeskatt** er satt til **Ja** for leverandøren på **Leverandør**-siden.

4. Du kan velge et selskapsnavn for alternative adresser som er konfigurert for selskapet, i **Navn**-feltet i delen **Selskapsopplysninger** i fanen **Avgiftsinformasjon**.

    Feltet **Skattebetalertype** i **Kildeskatt**-delen viser kategorien for skattebetalertype for leverandøren eller kunden. Feltet **TAN-nummer (Tax Account Number)** viser TAN-nummeret (Tax Account Number) for det valgte selskapet.

5. Velg **Kildeskatt-knappen \> kildeskatt** for å åpne siden **Midlertidige kildeskattransaksjoner**. Den øvre delen av denne siden inneholder følgende felter:

    - **Kildeskattbeløp totalt** – Det totale TDS-beløpet som ble beregnet for transaksjonen for TDS-gruppen.
    - **Verdi** – Den totale prosentsatsen som ble brukt til å beregne TDS for transaksjonen. Den totale prosentsatsen er basert på formelen som er definert for TDS-avgiftskodene og er knyttet til TDS-gruppen.
    - **Justert kildeskattbeløp totalt** – Det totale justerte TDS-beløpet for alle avgiftskodene i TDS-gruppen.
    - **TDS** – En avmerket avmerkingsboks angir at en TDS-gruppe er knyttet til transaksjonen.

    Feltene i fanen **Oversikt**, **Generelt** og **Justering** viser det beregnede TDS-beløpet og detaljene for det justerte TDS-beløpet for hver TDS-avgiftskode som er knyttet til TDS-gruppen.

6. Velg **Terskel** for å åpne **Terskel**-siden, der du kan gå gjennom terskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til en bestemt TDS-avgiftskode.
7. Velg **Formeldesigner** for å åpne **Formeldesigner**-siden, der du kan gå gjennom formelen som er definert for en bestemt TDS-avgiftskode.
8. Lukk sidene **Formeldesigner** og **Midlertidige kildeskattransaksjoner** for å gå tilbake til **Journalbilag**-siden.
9. Valider og poster journalen. TDS-beløpet som ble beregnet, posteres på leverandørreskontroen som er definert for hver TDS-avgiftskode i TDS-gruppen. Kundereskontroene for TDS-avgiftskoder defineres på siden **Kildeskattkoder**.
10. Velg **Postert kildeskatt** for å åpne siden **Kildeskattransaksjoner**. **Verdi**-feltet viser den totale prosentsatsen som ble brukt til å beregne TDS for transaksjonen.

    Feltene i fanene **Oversikt**, **Generelt** og **Beløp** viser TDS-beløpene som ble beregnet for TDS-gruppen som er knyttet til transaksjonen.

11. Gå gjennom TDS-beregningsinformasjonen for hver TDS-avgiftskode som er knyttet til TDS-gruppen.

## <a name="generate-payments"></a>Opprett betalinger

Følg denne fremgangsmåten for å generere betalinger.

1. Følg ett av disse trinnene:

    - Gå til **Leverandører \> Betalinger \> Leverandørbetalingsjournal**.
    - Gå til **Kunder \> Betalinger \> Kundebetalingsjournal**.
    - Gå til **Leverandører \> Betalinger \> Egenveksler \> Journal for egenvekseltrekking**.
    - Gå til **Kunder \> Betalinger \> Veksel \> Journal for vekseltrekking**.
    - Gå til **Kunder \> Betalinger \> Veksel \> Journal for ny vekseltilbaketrekking**.

2. Velg **Linjer**.
3. Velg **Funksjoner \> Generer betalinger**.
