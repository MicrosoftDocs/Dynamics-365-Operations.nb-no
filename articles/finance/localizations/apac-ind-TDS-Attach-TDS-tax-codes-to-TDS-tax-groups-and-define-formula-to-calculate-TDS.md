---
title: Knytte TDS-avgiftskoder til TDS-avgiftsgrupper og definere formelen for beregning av TDS
description: Dette emnet forklarer hvordan du konfigurerer TDS-avgiftsgrupper (Tax Deducted at Source) og knytter TDS-avgiftskoder til TDS-avgiftsgrupper. For å kunne beregne TDS for en TDS-avgiftsgruppe må du definere formelen for TDS-avgiftskoder som er knyttet til den.
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
ms.openlocfilehash: 81aac53cca91a75cde811c314bd6f7039852d32505fe6540921e17f3d1bbc7ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739316"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>Knytte TDS-avgiftskoder til TDS-avgiftsgrupper og definere formelen for beregning av TDS

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer TDS-avgiftsgrupper (Tax Deducted at Source) og knytter TDS-avgiftskoder til TDS-avgiftsgrupper. For å kunne beregne TDS for en TDS-avgiftsgruppe må du definere formelen for TDS-avgiftskoder som er knyttet til den.

Følg denne fremgangsmåten for å konfigurere en TDS-avgiftsgruppe, knytte TDS-avgiftskoder til den og definere formelen for beregning av TDS.

1. Gå til **Avgift \> Indirekte avgifter \> Kildeskatt \> Kildeskattgrupper**.

    [![Siden Kildeskattgrupper.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Velg **Ny** i handlingsruten for å opprette en kildeskattgruppe for TDS, og angi de nødvendige detaljene.
3. I feltet **Avgiftstype** velger du **TDS**.
4. I hurtigfanen **Oppsett** velger du **Legg til** for å opprette en linje.
5. Velg TDS-avgiftskoden for TDS-avgiftsgruppen i feltet **Kildeskattkode**. Feltet **Navn på kildeskatt** viser navnet på TDS-avgiftskoden, og **Verdi**-feltet viser verdien.
6. Hvis du vil ignorere terskelgrensen og unntaksterskelgrensen som er definert for TDS-avgiftskomponenten som er knyttet til TDS-avgiftskoden i TDS-transaksjoner, merker du av for **Overse terskel**.
7. Merk av for **Avgiftsfri** hvis du vil unngå at avgiftsgruppen beregnes i transaksjoner.
8. Velg **Utforming** i handlingsruten for å åpne formeldesigneren, slik at du kan definere formelen for beregning av TDS for TDS-avgiftsgruppen. **Avgifter**-fanen på **Utforming**-siden viser TDS-avgiftskodene som er valgt for TDS-avgiftsgruppen.

    [![Utforming-siden.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Trykk på **ALT+N** i **Beregning**-fanen for å opprette en linje. **ID**-feltet viser den automatisk genererte prioritets-ID-en for TDS-beregningen.
10. Velg TDS-avgiftskoden som formelen skal defineres for, i **Avgiftskode**-feltet. Alle TDS-avgiftskodene som er valgt for TDS-avgiftsgruppen, kan velges i dette feltet.
11. I feltet **Skattbart grunnlag** velger du grunnlaget for beregning av TDS:

    - **Bruttobeløp** – Beregn TDS basert på bruttotransaksjonsbeløpet (det vil si fakturabeløpet) ved hjelp av beregningsuttrykket som er definert for avgiftskoden.
    - **Ekskl. bruttobeløp** – Beregn TDS basert på beregningsuttrykket som er definert for avgiftskoden.

    > [!NOTE]
    > Feltet **Skattbart grunnlag** kan ikke settes til **Ekskl. bruttobeløp** for TDS-avgiftskoden som har prioritets-ID-en **1**.

12. TDS-beregningen er basert på formelen som er definert i feltet **Beregningsuttrykk** for hver avgiftskode som er knyttet til TDS-avgiftsgruppen. Velg plusstegnet (**+**), minustegnet (**-**), multiplikasjonstegnet (**\**_) eller divisjonstegnet (_*/**) for å angi beregningsuttrykket for den valgte TDS-avgiftskoden i feltet **Beregningsuttrykk**.

    > [!NOTE]
    > Ingen beregningsuttrykk kan defineres for TDS-avgiftskoden som har prioritets-ID-en **1**.

13. Hvis du vil definere beregningsuttrykk for TDS-avgiftskoden i feltet **Beregningsuttrykk**, legger du til TDS-avgiftskoder som er tilgjengelige i **Avgifter**-fanen. Hvis du vil legge til TDS-avgiftskoder i feltet **Beregningsuttrykk**, kan du bruke en av følgende metoder:

    - Dra den nødvendige avgiftskoden fra **Avgifter**-fanen til feltet **Beregningsuttrykk**.
    - Dobbelttrykk (eller dobbeltklikk) på den nødvendige avgiftskoden i **Avgifter**-fanen.
    - Velg og hold (eller høyreklikk på) den nødvendige avgiftskoden i **Avgifter**-fanen, og velg deretter **Legg til avgiftskode**.

    > [!NOTE]
    > Sett inn et beregningsuttrykk før hver TDS-avgiftskode. TDS-avgiftskodene som er lagt til i beregningsuttrykket, vises i hakeparenteser (\[...\]).

14. Hvis du vil fjerne beregningsuttrykket som er definert for en avgiftskode i feltet **Beregningsuttrykk**, velger du **C**-knappen.
15. Hvis du vil slette en post i **Beregning**-fanen, velger du **Slett**.
16. Lukk siden.
