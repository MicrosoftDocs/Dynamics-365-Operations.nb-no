---
title: Behandle eksempel på purring
description: Dette emnet går gjennom et eksempel som viser prosessen med å opprette, skrive ut og postere purringer.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e813b4f0c6408a8046fa8203007a0a356ca2c794
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347814"
---
# <a name="process-collection-letters-example"></a>Behandle eksempel på purring

[!include [banner](../../includes/banner.md)]

Dette emnet går gjennom et eksempel som viser prosessen med å opprette, skrive ut og postere purringer. Eksemplet er basert på alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** i Kreditt og purringer. Den bruker data i USOGRAFI-demofirmaet og en ny kunde, US-045.

Du begynner ved å gå til **Kunder \> Kunder \> Alle kunder**, velg **Ny**, og angi deretter den obligatoriske inforamsjonen for å opprette US-045.

Når du er ferdig, gjør du følgende.

1. Gå til **Kreditt og innkrevinger \> Purring \> Definer purreforløp**, og definer purreforløpet som vist i tabellen nedenfor som er tilordnet kundeposteringsprofilen.

|     Purrekode      |     beskrivelse                           |     Valuta.      |     Hovedkonto        |     Gebyr i valuta     |     Minimum over        |     Dager   Blokker      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     Purring   brev 1         |     Andre   varsling med gebyr        |     USD           |                           |     0.00                  |     0.00                  |     2                 |
|     Purring   brev 2         |     Andre   varsling med gebyr        |     USC           |     403150                |     20.00                 |     10,00                 |     3                 |
|     Inkasso                    |     Siste   varsling med gebyr         |     USD           |     403150                |     50.00                 |     100.00                |     15                |

Illustrasjonen nedenfor viser informasjonen i tabellen slik den vil se ut på **purresiden**. 

[![Definere en purresekvens.](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Nå må du definere de to parameterne som kreves for dette eksemplet.

2. Gå til **Kreditt og innkreving \> Oppsett \> Kundeparametere** og gjør følgende:

    1. I hurtigfanen **Innkrevinger** setter du alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** til **Ja**.
    2. Kontroller at feltet **Opprett en purring per** er satt til **Kunde**.

    [![Angi Kundeparametere for kredittinnkrevinger.](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer**, velg **Ny**, og gjør deretter følgende:

    1. Velg **US-045** i feltet **Kundekonto**.
    2. I feltet **Fakturadata** angir du **15.01.2021**.
    3. Angi **16.01.2021** i feltet **Forfallsdato**.
    4. Angi **401100** i feltet **Hovedkonto** i hurtigfanen **Fakturalinjer**.
    5. Angi **500.00** i **Enhetspris**-feltet.
    6. Velg **Poster**.

    Du må nå angi to kreditnotaer for kunden.

4. Velg **Ny**, og følg deretter denne fremgangsmåten:

    1. Velg **US-045** i **Kundekonto**-feltet.
    2. I feltet **Fakturadata** angir du **15.01.2021**.
    3. Angi **16.01.2021** i feltet **Forfallsdato**.
    4. Angi **401100** i feltet **Hovedkonto** i hurtigfanen **Fakturalinjer**.
    5. Angi **-100,00** i feltet **Enhetspris**.
    6. Velg **Poster**.

5. Gjenta trinn 4, men angi **-200,00** i feltet **Enhetspris**.
6. Gå til **Kunder \> Kunder \> Alle kunder** og velg kunde **US-045**. I handlingsruten velger du deretter **Transaksjoner \> Transaksjoner** for å gå gjennom kundetransaksjonene du posterte tidligere.

    [![Gå gjennom de posterte kundetransaksjonene.](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Du må nå opprette purringer for en kunde US-045.

7. Gå til **Kreditt og innkreving \> Purring \> Opprett purringer**, og gjør følgende:

    1. Sett alternativene **Faktura** og **Kreditnota** til **Ja**.

        Som standrd må feltet **Purring** settes til **Purring per kunde**.

    2. I feltet **Purredato** angir du **19.01.2021**.
    3. I hurtigkategorien **Poster som skal inkluderes** velger du **Filter**, og deretter legger du til kunde **US-045** i feltet **Kundekonto**.
    4. Velg **OK**.
    5. Velg **OK** for å opprette purrebrev.

8. Gå til **Kreditt og innkreving \> Purring \> Gjennomgå og behandle purrebrev**, og gjør følgende:

    1. Legg merke til at purrekoden i både hodet og transaksjonslinjene er **Purring 1**, ettersom denne purringen er den første purringen i serien. (Hvis du vil vise transaksjonslinjene, må du kanskje velge hurtigfanen **Transaksjoner**.)

   [![Kontrollere at samme purrekode vises i hodet og på linjene.](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Velg **Poster** i handlingsruten.
    3. I feltet **Posteringsdata** angir du **19.01.2021**.

    Du må nå opprette purringer på nytt for kunde US-045.

9. Gå til **Kreditt og innkreving \> Purring \> Opprett purringer**, og gjør følgende:

    1. Sett alternativene **Faktura** og **Kreditnota** til **Ja**.

        Som standrd må feltet **Purring** settes til **Purring per kunde**.

    2. I feltet **Purredato** angir du **23.01.2021**.
    3. I hurtigkategorien **Poster som skal inkluderes** velger du **Filter**, og deretter legger du til kunde **US-045** i feltet **Kundekonto**.
    4. Velg **OK**.
    5. Velg **OK** for å opprette purrebrev.

10. Gå til **Kreditt og innkreving \> Purring \> Gjennomgå og behandle purrebrev**, og gjør følgende:

    1. Legg merke til at purrekoden i hodet er **Purring 1**. Koden på transaksjonslinjene er imidlertid **Purring 2**.

   [![Kontrollerer at forskjellige purrekoder vises i hodet og på linjene.](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Kodene varierer fordi alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** er satt til **Ja**.

  2. Ikke poster dette purrebrevet.

11. Gå til **Kreditt og innkreving \> Oppsett \> Kundeparametere**, og deretter setter du alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** til **Nei** i fanen **Purringer**.

    [![Setter alternativet Ignorer betalinger og kreditnotaer ved beregning av purrekoden til Nei.](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Du må nå opprette purringer på nytt for kunde US-045.

12. Gå til **Kreditt og innkreving \> Purring \> Opprett purringer**, og gjør følgende:

    1. Sett alternativene **Faktura** og **Kreditnota** til **Ja**.

        Som standrd må feltet **Purring** settes til **Purring per kunde**.

    2. I feltet **Purredato** angir du **23.01.2021**.
    3. I hurtigkategorien **Poster som skal inkluderes** velger du **Filter**, og deretter legger du til kunde **US-045** i feltet **Kundekonto**.
    4. Velg **OK**.
    5. Velg **OK** for å opprette purrebrev.

13. Gå til **Kreditt og innkrevinger \> Purring \> Gå gjennom og behandle purrebrev**, og legg merke til at purrebrevkoden på både hodet og transaksjonslinene **Purrebrev 2**.

    [![Viser på nytt at samme purrekode vises i hodet og på linjene.](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Den samme koden vises begge steder fordi alternativet **Ignorer betalinger og kreditnotaer ved beregning av purrekode** nå er satt til **Nei**.
