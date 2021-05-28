---
title: Konfigurere avgiftskomponenter for TDS-avgiftstypen
description: Dette emnet forklarer hvordan du konfigurerer komponenter for kildeskatt for TDS-avgiftstypen (Tax Deducted at Source). Det forklarer også hvordan du definerer terskelgrensen som skal brukes til å beregne TDS for hver TDS-komponent.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023473"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Konfigurere avgiftskomponenter for TDS-avgiftstypen

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer komponenter for kildeskatt for TDS-avgiftstypen (Tax Deducted at Source). TDS-komponentene er TDS, tilleggsavgift, PE-Cess og SHE Cess. Dette emnet forklarer også hvordan du definerer terskelen som skal brukes til å beregne TDS for hver TDS-komponent. Du kan i tillegg definere en unntaksterskel som skal brukes til å beregne TDS for hver TDS-komponent.

Følg trinnene nedenfor for å konfigurere TDS-komponenter.

1. Gå til **Avgift \> Oppsett \> Kildeskatt \> Komponenter for kildeskatt**.

    [![Siden Komponenter for kildeskatt](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. Velg **TDS** i **Avgiftstype**-feltet for å definere komponenter for kildeskatt for TDS-avgiftstypen.
3. I handlingsruten velger du **Ny** for å opprette en linje.
4. Angi et navn for TDS-komponenten i feltet **Komponent for kildeskatt**.
5. Velg komponentgruppen for kildeskatt for TDS som TDS-komponenten skal knyttes til, i feltet **Komponentgruppe for kildeskatt**.
6. Skriv inn en beskrivelse av TDS-komponenten i **Beskrivelse**-feltet i hurtigfanen **Generelt**.
7. Velg **Terskel** i handlingsruten for å åpne **Terskel**-siden, slik at du kan definere terskelen som skal brukes til å beregne TDS for TDS-komponenten.
8. Bruk feltene **Fra-dato** og **Til-dato** til å definere perioden som terskelen skal gjelde for.
9. Angi terskelbeløpet som skal brukes til å beregne TDS for TDS-komponenten, i **Terskel**-feltet i **Generelt**-fanen. Avgiften trekkes bare fra ved kilden når det kumulative fakturabeløpet krysser terskelen.

    Hvis terskelbeløpet for eksempel er 10 000, beregnes TDS etter at det kumulative fakturabeløpet overskrider 10 000 (med andre ord når det er 10 001 eller mer).

10. Angi unntaksterskelbeløpet som skal brukes til å beregne TDS for TDS-komponenten, i **Unntaksterskel**-feltet. Avgiften på en fakturalinje trekkes bare fra ved kilden når beløpet krysser unntaksterskelen.

    Hvis unntaksterskelbeløpet for eksempel er 5 000, beregnes TDS for en bestemt fakturalinje hvis fakturalinjebeløpet overskrider 5 000 (det vil si hvis det er 5 001 eller mer).

    [![Terskel-siden](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Unntaksterskelbeløpet må være mindre enn eller likt terskelbeløpet.
    >
    > Avgiften trekkes fra for en transaksjon hvis transaksjonsbeløpet krysser unntaksterskelen, selv om det kumulative fakturabeløpet ikke krysser terskelen som er angitt i **Terskel**-feltet.

11. Lukk **Terskel**-siden for å gå tilbake til siden **Komponenter for kildeskatt**.
12. Velg **Kopier** i handlingsruten for å åpne dialogboksen **Kopier komponenter for kildeskatt**, slik at du kan kopiere TDS-komponentene som er konfigurert for én TDS-komponentgruppe, til en annen TDS-komponentgruppe.
13. I **Fra**-feltet velger du TDS-komponentgruppen du vil kopiere TDS-komponentene fra. I **Til**-feltet velger du komponentgruppen for kildeskatt du vil kopiere TDS-komponentene til.

    > [!NOTE]
    > Vanlige TDS-komponenter som er knyttet til begge TDS-komponentgruppene, kopieres ikke.

14. Velg **OK** for å kopiere og opprette TDS-komponenter for den andre TDS-komponentgruppen på siden **Komponenter for kildeskatt**.

    [![Dialogboksen Kopier komponenter for kildeskatt](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Lukk siden.
