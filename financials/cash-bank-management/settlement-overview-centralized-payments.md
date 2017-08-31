---
title: Oversikt over utligning for sentraliserte betalinger
description: "Organisasjoner som omfatter flere juridiske enheter, kan opprette og administrere betalinger ved hjelp av en juridisk enhet som håndterer alle betalinger. Dette eliminerer behovet for å legge inn den samme transaksjonen i flere juridiske enheter, og sparer tid ved å strømlinjeforme betalingsforslagsprosessen, utligningsprosessen, redigering av åpne transaksjoner og redigering av lukkede transaksjoner for sentraliserte betalinger."
author: abruer
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 222414
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: dd8e6fb1100cdbb8f0b5ad778b322243c72529ba
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="settlement-overview-for-centralized-payments"></a>Oversikt over utligning for sentraliserte betalinger

[!include[banner](../includes/banner.md)]


Organisasjoner som omfatter flere juridiske enheter, kan opprette og administrere betalinger ved hjelp av en juridisk enhet som håndterer alle betalinger. Dette eliminerer behovet for å legge inn den samme transaksjonen i flere juridiske enheter, og sparer tid ved å strømlinjeforme betalingsforslagsprosessen, utligningsprosessen, redigering av åpne transaksjoner og redigering av lukkede transaksjoner for sentraliserte betalinger. 

Når en kunde- eller leverandørbetaling blir lagt inn i en juridisk enhet og blir utlignet mot en faktura som ble lagt inn i en annen juridisk enhet, blir den nødvendige utligningen, forfall til- og forfall fra-transaksjonene generert automatisk for hver juridiske enhet. Det blir opprettet en utligningspost for hver kombinasjon av faktura og betaling i transaksjonen. Hver utligningspost blir tilordnet et nytt bilagsnummer, som er basert på betalingsbilag-nummerserien som er angitt på siden **Kundeparametere** for kunder og siden **Leverandørparametere** for leverandører. 

Hvis det blir generert tilleggsutligningsposter for rabatter, revalueringer av utenlandsk valuta, øredifferanser, overbetalinger eller underbetalinger, blir de tilordnet den seneste datoen på betalings- eller fakturatransaksjonen. Hvis utligningen skjer etter at betalingen er postert, bruker utligningspostene den utligningsposteringsdatoen som er angitt på siden **Utlign åpne transaksjoner**.
Posteringstyper, transaksjonstyper og standardbeskrivelser
----------------------------------------------------------

Konsernintern utligning av bilagstransaksjoner bruker posteringstypen utligning mellom firmaer, konsernintern kundeutligning og transaksjonstypene konsernintern leverandørutligning. Du kan definere informasjon for transaksjonstypen på siden **Standardbeskrivelser**. 

Følgende transaksjonstyper er tilgjengelige for bruk i utligninger for enkeltfirmaer og på tvers av firmaer:

-   Utligning
-   Kontantrabatt
-   Revalueringer av utenlandsk valuta (inkluderer realiserte og urealiserte revalueringer av utenlandsk valuta)
-   Øredifferanse
-   Overbetaling/underbetaling

Du kan også definere standardbeskrivelser for bilagene for utligning på tvers av firmaer.

<a name="currency-exchange-gains-or-losses"></a>Valutakursgevinst eller -tap
---------------------------------

Valutakursen som brukes for kunde- og leverandørtransaksjoner blir lagret med transaksjonen. Realiserte gevinster eller tap av valutakurser blir postert til den juridiske enheten for fakturaen eller den juridiske enheten for betalingen, avhengig av hvilket alternativ som er valgt i feltet **Poster valutakursgevinst eller -tap** på **Konserninternt regnskap**-siden for den juridiske enheten for betalingen. Følgende eksempler bruker disse valutaene:
-   Regnskapsvaluta for betaling: EUR
-   Regnskapsvaluta for faktura: USD
-   Transaksjonsvaluta for betaling: DKK
-   Transaksjonsvaluta for faktura: CAD

#### <a name="currency-calculations"></a>Valutaberegninger

Når du utligner en faktura som er lagt inn i en juridisk enhet med en betaling som er lagt inn i en annen juridisk enhet, blir transaksjonsvalutaen for betalingen (DKK) omregnet i tre trinn:
1.  Omregnet til regnskapsvalutaen for betalingen (EUR) med valutakursene fra den jurdiske enheten for betalingen.
2.  Omregnet til regnskapsvalutaen for fakturaen (USD).
3.  Omregnet til transaksjonsvalutaen for fakturaen (CAD) med valutakursene fra den jurdiske enheten for fakturaen.

Omregningsprosessen bruker valutakursene per betalingsdato. Hvis resultatbetalingsbeløpet i transaksjonsvalutaen til fakturaen (CAD) er lik fakturabeløpet (CAD), anses fakturaen som fullt betalt. 

Når siden **Utlign åpne transaksjoner** blir åpnet fra en betalingsjournal der betalingsbeløpet ikke er lagt inn, blir utligningsbeløpet beregnet basert på fakturaene som er valgt for utligning på siden **Utlign åpne transaksjoner**. Beløpet som skal utlignes, blir omregnet i tre trinn:
1.  Omregnet til regnskapsvalutaen for fakturaen (USD) med valutakursene fra den juridiske enheten for fakturaen per betalingsdatoen.
2.  Omregnet til regnskapsvalutaen for betalingen (EUR) med valutakursene fra den juridiske enheten for fakturaen per betalingsdatoen.
3.  Omregnet til transaksjonsvalutaen for betalingen (DKK).

Resultatbetalingsbeløpet blir overført til betalingsjournallinjen når du lukker siden **Utlign åpne transaksjoner**.

#### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Postere gevinst eller tap på grunn av ulike regnskapsvalutaer

Hvis det finnes valutakursgevinst eller -tap, blir gevinsten eller tapet postert til den juridiske enheten som er angitt for feltet **Poster valutakursgevinst eller -tap** på siden **Konserninternt regnskap**  for den juridiske enheten for betalingen. Gevinst- eller tapsbeløpet blir omregnet til regnsapsvalutaen for den juridiske enheten det gevinst- eller tapsbeløpet blir postert, med valutakursen som er definert for den juridiske enheten.

<a name="cash-discounts"></a>Kontantrabatt
--------------

Kontantrabatter som genereres under utligningsprosessen mellom firmaer, blir postert enten til den juridiske enheten for fakturaen eller den juridiske enheten for betalingen, avhengig av hvilket alternativ som er valgt i feltet **Poster kontantrabatt** på **Konserninternt regnskap**-siden for den juridiske enheten for betalingen. En tilsvarende utligningstransaksjon blir generert i den juridiske enheten for fakturaen.

<a name="overpayments-and-underpayments"></a>Overbetalinger og underbetalinger
------------------------------

Toleranse for overbetalinger/underbetalinger og øredifferanse blir bestemt basert på den juridiske enheten til betalingen av overbetalingene, og på den juridiske enheten til fakturaen av underbetalingene. Posteringskontoen som brukes, avhenger av innstillingen i feltet **Håndtering av kontantrabatt** på **Kundeparametere**-siden for kunder, og feltet **Håndtering av kontantrabatt** på  **Leverandørparametere**-siden for leverandører.

-   Hvis innstillingen for behandling av kontantrabatt er Spesifikk, eller hvis innstillingen er Løs og gjeldende kontantrabatt blir postert i en annen juridisk enhet enn for overbetalingen, brukes den automatiske kontoen for kundekontantrabatt, leverandørkontantrabatt eller øredifferanse i regnskapsvalutaen. Du kan angi disse kontoene på siden **Kontoer for automatiske transaksjoner**.
-   Hvis innstillingen for behandling av kontantrabatt er Løs og kontantrabatten blir postert i den samme juridiske enheten som for overbetalingen (den juridiske enheten for betalingen og den juridiske enheten fakturaen er det samme), blir kontantrabattbeløpet justert. Hvis det for eksempel utlignes en faktura på 100,00, med en tilgjengelig kontantrabatt på 3,00 og en betaling på 98,00, blir kontantrabattbeløpet justert med 1,00. Nettorabattbeløpet er 2,00.
-   Hvis innstillingen for behandling av kontantrabatt er Løs, blir kontantrabatten postert i den samme juridiske enheten som for overbetalingen, og overbetalingen eller underbetalingen blir utlignet med flere fakturaer med kontantrabatter, blir kontantrabattkontoen for den siste fakturaen justert.

Hvis innstillingen for behandling av kontantrabatt er Løs, gjelder reglene for uspesifisert betalingsutligning bare i følgende situasjoner:
-   Det finnes en overbetaling.
-   Overbetalingen utlignes med en eller flere fakturaer som har kontantrabatt.
-   Kontantrabatten posteres i den samme juridiske enheten som overbetalingen.

I alle andre situasjoner posteres overbetalinger eller underbetalinger til den automatiske kontoen for Kundekontantrabatt Leverandørkontantrabatt eller Øredifferanse i regnskapsvalutaen.

## <a name="sales-tax"></a>Merverdiavgift
Merverdiavgiftstransaksjoner blir værende i den juridiske enheten der de opprinnelig ble postert. 

Hvis det ble postert merverdiavgift for en forhåndsbetaling, tilbakefører utligningen mellom firmaer merverdiavgiften for forhåndsbetalingen til den juridiske enheten. Merverdiavgiften i den juridiske enheten for fakturaen blir værende i den juridiske enheten for fakturaen.

## <a name="financial-dimensions"></a>Finansdimensjoner
For kundebetalinger bruker forfall til- og forfall fra-transaksjonene i den juridiske enheten for betalingen de finansdimensjonene som er angitt for kundesamlekontoen fra betalingen som utlignes. I den juridiske enheten for fakturaen bruker forfall til- og forfall fra-transaksjoner de finansdimensjonene som er angitt for kundesamlekontoen fra fakturaen som utlignes. 

For leverandørbetalinger bruker forfall til- og forfall fra-transaksjonene i den juridiske enheten for betalingen de finansdimensjonene som er angitt for leverandørsamlekontoen fra betalingen som utlignes. I den juridiske enheten for fakturaen bruker forfall til- og forfall fra-transaksjoner de finansdimensjonene som er angitt for leverandørsamlekontoen fra fakturaen som utlignes.

## <a name="withholding-tax"></a>Kildeskatt
Leverandørkontoen som er knyttet til fakturaen, brukes til å bestemme om kildeskatt skal beregnes. Hvis det brukes kildeskatt, blir den beregnet i den juridiske enheten som er knyttet til fakturaen. Hvis de juridiske enhetene bruker forskjellige valutaer, brukes valutakursen fra den juridiske enheten som er knyttet til fakturaen.






