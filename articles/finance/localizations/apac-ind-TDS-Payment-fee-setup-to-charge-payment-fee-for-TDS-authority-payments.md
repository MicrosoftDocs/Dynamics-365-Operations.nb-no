---
title: Konfigurere betalingsgebyrer for TDS-myndighetsbetalinger
description: Dette emnet forklarer hvordan du konfigurerer betalingsgebyrer som belastes for TDS-myndighetsbetalinger (Tax Deducted at Source).
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
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023493"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Konfigurere betalingsgebyrer for TDS-myndighetsbetalinger

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer betalingsgebyrer som belastes for TDS-myndighetsbetalinger (Tax Deducted at Source).

1. Gå til **Leverandører \> Betalingsoppsett \> Betalingsgebyr**.

    [![Siden Betalingsgebyr](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Velg **Nytt** for å opprette et betalingsgebyr, og angi de nødvendige detaljene.
3. Velg typen betalingsgebyr i **Gebyrtype**-feltet:

    - **None**
    - **Rente** – Rente belastes for sene betalinger til TDS-myndighetsleverandøren.
    - **Andre** – Andre tillegg belastes for sene betalinger til TDS-myndighetsleverandøren.

    Hvis du velger **Rente** eller **Andre**, settes **Tillegg**-feltet automatisk til **Finans**.

4. Hvis du valgte **Rente** eller **Andre** i **Felttype**-feltet, velger du finanskontoen du vil postere renten eller andre tillegg på, i **Hovedkonto**-feltet.
5. Angi de andre nødvendige opplysningene.
6. Velg **Oppsett av betalingsgebyr** i handlingsruten for å åpne siden **Oppsett av betalingsgebyr**, der du kan konfigurere betalingsgebyrer for ulike kombinasjoner av banker, betalingsmåter, betalingsspesifikasjoner, valutaer og datointervaller.

    [![Siden Oppsett av betalingsgebyr](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Angi hvilke banker du vil definere betalingsgebyret for, i **Grupperinger**-feltet i **Oversikt**-fanen:

    - **Tabell** – Gebyret er gyldig for en bestemt bankkonto.
    - **Gruppe** – Gebyret er gyldig for en bestemt bankgruppe.
    - **Alle** – Gebyret er gyldig for alle bankkontoene.

8. Hvis du valgte **Tabell** eller **Gruppe** i **Grupperinger**-feltet, velger du den bestemte bankkontoen eller bankgruppen du definerer betalingsgebyret for, i **Bankrelasjon**-feltet.
9. Velg betalingsmåten for betaling av gebyrer i **Betalingsmåte**-feltet.
10. Velg eller angi betalingsspesifikasjonskoden som er generert på siden **Betalingsspesifikasjon**, i feltet **Betalingsspesifikasjon**.
    - Betalingsspesifikasjonen brukes med betalingsmåter for elektronisk pengeoverføring.
12. Velg valutaen som aktiverer gebyret, i **Betalingsvaluta**-feltet. Bare transaksjoner som bruker den valgte valutaen, kan aktivere gebyret. Hvis du lar dette feltet stå tomt, aktiverer alle valutaer gebyret.
13. Velg beregningsmetoden i feltet **Prosent/beløp**. Alternativene er **Beløp**, **Prosent** og **Intervall**.
14. I **Gebyrbeløp**-feltet angir du gebyrbeløpet som enten en prosent av betalingen eller beløpet for én betaling.
15. Angi valutakoden for gebyret i **Gebyrvaluta**-feltet.
16. Velg **Generelt**-fanen for å vise eller endre detaljene for den valgte bankkontoen.

    [![Fanen Generelt](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. I **Minimum**-feltet angir du minimumsbeløpet for transaksjonen som skal aktivere gebyret.
17. I **Maksimum**-feltet angir du maksimumsbeløpet for transaksjonen som skal aktivere gebyret.
18. I feltene **Fra-dato** og **Til-dato** definerer du et datointervall for beregning av gebyrer.
19. I **Minimumsgebyr**-feltet angir du gebyrbeløpet som enten en prosent av betalingen eller beløpet for én betaling.
20. I feltet **Mva-gruppe** velger du mva-gruppen som skal brukes til å beregne mva for avgiftsbeløpet.
21. I feltet **Vare, mva-gruppe** velger du mva-gruppen for vare som skal brukes til å beregne mva for vare for avgiftsbeløpet.
22. Velg **Intervall**-fanen. 

    [![Intervall-fanen](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Angi antall dager mellom posteringsdatoen (diskonteringsdato) for betalingen og forfallsdatoen for egenvekselen i **Dager**-feltet.
24. I feltet **Prosent/beløp** velger du om spesifikasjonen er en prosent eller et angitt beløp.
25. I **Gebyrbeløp**-feltet angir du gebyrbeløpet som enten en prosent av betalingen eller beløpet for én betaling.
26. Lukk siden **Oppsett av betalingsgebyr**.
27. Lukk **Betalingsgebyr**-siden.
