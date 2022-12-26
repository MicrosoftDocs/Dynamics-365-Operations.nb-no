---
title: Utligningsforespørsel
description: Denne artikkelen beskriver vinduet Utligningsforespørsel
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ae49d9503c0a83bda7e0093ab6ef69fb4aef0a
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853142"
---
# <a name="ledger-settlement-inquiry"></a>Utligningsforespørsel

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver vinduet **Utligningsforespørsel** som kan brukes til å vise utlignede, opphevet utligning eller både utlignede og opphevet utligning finanstransaksjoner for en regnskapsperiode.

## <a name="view-ledger-settlement-transactions"></a>Vis utligningstransaksjoner
1.  Gå til **Økonomimodul > Forespørsler og rapporter > Utligningsforespørsel**.
2.  Bruk feltene **Fra dato** og **Til dato** eller **Datointervall**-feltet til å angi et datoområde. Som for råbalansen må datoområdet falle innenfor ett enkelt regnskapsår.
3.  Velg en eller flere hovedkontoer du vil vise finanstransaksjoner for, i **Hovedkonto**-feltet. Rullegardinlisten viser bare hovedkontoer som er definert for utligning på siden **Økonomimodulparametere**.
4.  Bruk feltet **Finansdimensjonssett** til å vise finansdimensjonene i rutenettet. **Hovedkonto**-feltet blir alltid vist som den første kolonnen, fordi hovedkontoen er påkrevd, selv om du velger et finansdimensjonssett som ikke omfatter hovedkontoen.
5.  Velg følgende i **Status**-feltet:
-   **Alle** hvis du vil vise både utlignede og opphevet utlignede transaksjoner
-   **Ikke utlignet** hvis du vil vise bare ikke utlignede transaksjoner 
-   **Utlignet** hvis du vil vise bare utlignede transaksjoner
6.  Velg **Vis transaksjoner**. Finanstransaksjoner vises i rutenettet, basert på kriteriene du angav. Du kan eksportere resultatene fra forespørselen til Microsoft Excel for ytterligere analyse. Velg og hold (eller høyreklikk) i rutenettet.

### <a name="column-details"></a>Kolonnedetaljer
Rutenettet på **Utligningsforespørsel**-siden inneholder følgende kolonner:
-   **Hovedkonto** – Dette feltet er obligatorisk og vises alltid.
-   **Finansdimensjoner** – Finansdimensjoner vises basert på finansdimensjonssettet som er valgt.
-   **Transaksjonsdato** – Posteringsdatoen for finanstransaksjonen.
-   **Opprinnelig transaksjonsdato** – Hvis årsavslutningen er kjørt, og utligning er definert slik at den beholder detaljer for en hovedkonto, blir de ikke utlignede transaksjonene hentet inn i detalj som en åpningssaldo. Den opprinnelige posteringsdatoen for finanstransaksjonen vedlikeholdes i feltet **Opprinnelig transaksjonsdato**.
-   **Transaksjonsalder** – Verdien er 0 (null) for alle utlignede transaksjoner. For transaksjoner som ikke er utlignet, beregnes verdien som antall dager fra enten den opprinnelige transaksjonsdatoen eller transaksjonsdatoen til datoen da forespørselen kjøres.
En finanstransaksjon har for eksempel transaksjonsdatoen 1. januar 2022 (01.01.2022) og en opprinnelig transaksjonsdato på 30. desember 2021 (30.12.2021). Hvis forespørselen kjøres 2. januar 2022 (02.01.2022) for regnskapsåret 2022, vil verdien av **Transaksjonsalder** være 4. Denne verdien beregnes som antall dager mellom den opprinnelige transaksjonsdatoen (30.12.2021) og 02.01.2022.

Hvis det ikke finnes en opprinnelig transaksjonsdato, brukes transaksjonsdatoen i stedet.
-   **(Annen transaksjonsinformasjon)** – Tilleggskolonner viser informasjon som bilagsnummer, beskrivelse og debet- og kreditbeløp i alle tre valutaer (transaksjon, regnskap og rapportering).
-   **Status** – Denne verdien er enten **Utlignet** eller **Ikke utlignet**.
-   **Utlignings-ID** – ID-en som er tildelt de utlignede transaksjonene.

[![Utligningsforespørsel-side](./media/Inquiry1.png)](./media/Inquiry1.png)

 
Totaler kan vises under rutenettet.
1.  Merk ellipsen (...) til høyre for rutenettet, og velg deretter **Vis bunntekst**.
2.  Velg og hold (eller høyreklikk) i hver beløpskolonne og velg **Grupper etter denne kolonnen** for å vise totalene. Totalene vises i bunnteksten. Hvis forespørselen er filtrert slik at den bare viser transaksjoner som ikke er utlignet, kan du bruke totalene til å avstemme beløpene med råbalansen.







