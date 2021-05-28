---
title: Utligne TDS-betalinger mot TDS-myndighetsleverandører og generere TDS-challan
description: Dette emnet forklarer hvordan du utligner TDS-betalinger (Tax Deducted at Source) mot TDS-myndighetsleverandører.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023485"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>Utligne TDS-betalinger mot TDS-myndighetsleverandører og generere TDS-challan

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du utligner TDS-betalinger (Tax Deducted at Source) mot TDS-myndighetsleverandører.

1. Gå til **Leverandører \> Betalinger \> Leverandørbetalingsjournal**.

    [![Siden Leverandørbetalingsjournal](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Velg **Ny** for å opprette en journallinje på siden **Leverandørbetalingsjournal**.
3. I **Konto**-feltet velger du TDS-myndighetsleverandøren som TDS-betalinger skal utlignes mot.
4. Velg **Utligningstransaksjoner** for å åpne siden **Utligningstransaksjoner**, der du kan vise de utlignede TDS-transaksjonene for TDS-myndighetsleverandøren.

    De utlignede TDS-transaksjonene for en utligningsperiode vises på følgende måte:

    - TDS-transaksjoner der kategorien for skattebetalertype er **Selskap**, vises som én transaksjonslinje.
    - TDS-transaksjoner der kategorien for skattebetalertype er **HUF**, **Firma**, **Enkeltperson**, **AOP**, **BOI**, **Lokale myndigheter** eller **Andre** vises som én transaksjonslinje.
    - **Beløp**-feltet inneholder det totale TDS-beløpet som skal betales til TDS-myndighetsleverandøren.

5. Velg **Kildeskattransaksjoner** for å vise de ulike TDS-transaksjonene som er tatt med for utligningsposten. Du kan vise delingen av hver TDS-transaksjon som er tatt med i utligningsprosessen for utligningsperioden på denne siden.
6. I **Oversikt**-fanen merker du av for **Merk** for TDS-transaksjonene som skal utlignes mot TDS-myndighetsleverandøren.

    **Oversikt**-fanen viser følgende informasjon for hver åpne TDS-transaksjon:

    - **Dato** – TDS-transaksjonsdatoen.
    - **Bilag** – Bilagsnummeret.
    - **Kilde** – Modulen som TDS-transaksjonen posteres i.
    - **Leverandør/kunde** – Leverandør- eller kundekontonummeret som TDS trekkes fra.
    - **Navn på deductee/part** – Navnet på leverandøren eller kunden som TDS trekkes fra.
    - **Skattebetalertype** – Kategorien for skattebetalertype som deductee hører til i.
    - **Beløp** – Fakturabeløpet som TDS ble beregnet for.
    - **Avgiftsbeløp** – TDS-beløpet som ble beregnet for transaksjonen.

    > [!NOTE]
    > Fjern merket for **Merk** for alle TDS-transaksjoner som ikke skal utlignes mot TDS-myndighetsleverandøren.

    I kategorien **Generelt** viser **PAN**-feltet det permanente kontonummeret (PAN) til deductee. **Dato**-feltet viser datoen for TDS-beregningen, og **Verdi**-feltet viser den totale prosentsatsen som ble brukt ved TDS-beregningen.

7. Velg **Bilag** for å vise bilagsoppføringene for TDS-transaksjonen.
8. Lukk siden.
10. Velg **Komponenter for kildeskatt** for å åpne siden **Komponenter for kildeskatt**, der du kan vise TDS-beløpet som ble beregnet per TDS-avgiftskomponent for en bestemt TDS-avgiftskode.

    Feltet **Avgiftskomponent** i **Oversikt**-fanen viser TDS-avgiftskomponenten som ble brukt for transaksjonen. **Beløp**-feltet viser TDS-beløpet som ble beregnet for TDS-avgiftskomponenten, i basisvalutaen. Feltet **Akkumulert beløp** viser det totale TDS-beløpet som ble beregnet for TDS-avgiftskomponenten for alle utlignede transaksjoner.

    **Standardvaluta**-delen i **Beløp**-fanen viser TDS-beløpet som ble beregnet for TDS-avgiftskomponenten, i standardvalutaen. Delen **Alternativ valuta** viser beløpet i den alternative valutaen.

11. Lukk siden **Komponenter for kildeskatt**.
12. Merk deg at det totale beløpet som skal utlignes mot TDS-myndighetsleverandøren for utligningsperioden, oppdateres i **Beløp**-feltet på siden **Åpen transaksjonsredigering**.
13. Hvis du vil utligne TDS-transaksjonene for ulike TDS-utligningsperioder mot TDS-myndighetsleverandøren, merker du av for **Merk** for transaksjonene.
14. Lukk siden **Åpen transaksjonsredigering**.

    > [!NOTE]
    > Hvis det bare er valgt noen få transaksjoner for utligning på siden **Kildeskattransaksjoner**, oppdateres det totale TDS-beløpet for de valgte transaksjonene i **Rettelse**-feltet på siden **Åpen transaksjonsredigering**. Rettelsesbeløpet oppdateres på journallinjen på **Journalbilag**-siden, og siden **Åpen transaksjonsredigering** lukkes.

    **Debet**-feltet på **Journalbilag**-siden viser totalbeløpet som skal betales til TDS-myndighetsleverandøren.

15. Angi motkontodetaljene.

    > [!NOTE]
    > Hvis TDS-transaksjoner har ulike TAN-numre (Tax Account Number), opprettes det journallinjer per TAN på **Journalbilag**-siden.

16. Velg en gebyr-ID som har gebyrtypen **Rente** eller **Andre** i feltet **Gebyr-ID** på **Betalingsgebyr**-siden, for å belaste betalingsgebyret for forsinkede betalinger til TDS-leverandøren.

    **Navn**-feltet i delen **Selskapsopplysninger** i fanen **Avgiftsinformasjon** viser selskapsnavnet. Feltet **TAN-nummer (Tax Account Number)** i **Kildeskatt**-delen viser TAN-nummeret som er knyttet til transaksjonslinjen.

17. Valider og poster journalen.
18. Velg **Kildeskatt \> Challan-informasjon** for å angi challan-detaljene for transaksjonen.

    **Bilag**-feltet viser bilagsnummeret for transaksjonen.
    
19. Merk av for **TDS innbetalt ved bokoppføring** hvis TDS-beløpet betales inn ved hjelp av bokoppføring.
20. Angi challan-nummeret som brukes til å betale TDS-myndighetsleverandøren, i feltet **Challan-nummer**.
21. Angi challan-datoen i **Dato**-feltet.
22. I **Banknavn**-feltet velger du navnet på banken som TDS-beløpet som skal betales til TDS-myndighetsleverandøren, skal betales inn i. Dette feltet viser alle bankkontoene som ble konfigurert for TDS-myndighetsleverandøren i **Leverandør \> Alle leverandører \> Konfigurer \> Bankkontoer**.
23. Angi BSR-koden (Basic Statistical Return) for banken i feltet **BSR-kode**.
24. Lukk siden.

### <a name="example"></a>Eksempel

Perioden 01.04.2009 utlignes mot TDS-komponentgruppen **Leie** ved hjelp av den periodiske TDS-utligningsprosessen. Det totale TDS-beløpet på 141 625,00 posteres på kontoen til TDS-myndighetsleverandøren for TDS-utligningsperioden. Du kan vise dette beløpet i **Beløp**-feltet på siden **Åpen transaksjonsredigering** for TDS-myndighetsleverandøren.

Hvis du velger **Kildeskattransaksjoner** for å vise de ulike TDS-transaksjonene som ble utlignet for perioden, vises informasjonen nedenfor.

| TDS-beløp |
|------------|
| 16 995,00  |
| 22 660,00  |
| 28 325,00  |
| 16 995,00  |
| 28 325,00  |
| 16 995,00  |
| 11 330,00  |

Du kan velge **Komponenter for kildeskatt** for et bestemt TDS-beløp for å vise TDS-beløpet som ble beregnet per TDS-avgiftskomponent for en bestemt TDS-avgiftskode. I dette eksemplet velger du **Komponenter for kildeskatt** for TDS-beløpet 16 995,00. Avgiftsbeløpet som ble beregnet per komponent for transaksjonen, vises.

| Avgiftskomponent | Beløp    | Akkumulert beløp |
|---------------|-----------|--------------------|
| TDS           | 15 000,00 | 125 000,00         |
| Tillegg     | 1 500,00  | 12 500,00          |
| PE-Cess       | 330,00    | 2 750,00           |
| SHE Cess      | 165,00    | 1 375,00           |

Hvis du bare valgte TDS-beløpene 16 995,00, 22 660,00 og 28 325,00 for utligning på siden **Kildeskattransaksjoner**, vises totalbeløpet for utligning som **67 980,00** i **Rettelse**-feltet på siden **Åpen transaksjonsredigering**. Hvis denne transaksjonen er merket for utligning og siden **Åpen transaksjonsredigering** er lukket, vises beløpet **67 980,00** i **Debet**-feltet på **Journalbilag**-siden.

Du kan nå postere journalen og generere TDS-challan.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>Justering av forskuddsbetalinger til TDS-myndighetsleverandører

Hvis du vil justere en forskuddsbetaling til TDS-myndighetsleverandøren til en faktisk betaling, kan du gå til **Leverandører \> Leverandører \> Alle leverandører \> Transaksjonsredigering**. Hvis den faktiske betalingen som foretas, overskrider forskuddsbetalingen, genereres to challan-numre for transaksjonen. Det er imidlertid bare det første challan-nummeret som vises i TDS-forespørselen.
