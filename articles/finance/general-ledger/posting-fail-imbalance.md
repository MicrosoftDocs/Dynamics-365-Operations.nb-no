---
title: Feil ved journalpostering på grunn av ubalanse
description: Dette emnet beskriver hvorfor debet og kredit kanskje ikke er balansert i bilagstransaksjoner, slik at transaksjonene ikke kan posteres. Emnet inneholder også trinn for å løse problemet.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fc413f8230849653aef8c2951f1749823edded6e
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605435"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Feil ved journalpostering på grunn av ubalanse

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvorfor debet og kredit kanskje ikke er balansert i bilagstransaksjoner, slik at transaksjonene ikke kan posteres. Emnet inneholder også trinn for å løse problemet.

## <a name="symptom"></a>Symptom

I noen tilfeller kan ikke en journal posteres, og følgende melding vises: "Transaksjonene på et bestemt bilag er ikke i balanse på en bestemt dato (regnskapsvaluta: 0.01 - rapporteringsvaluta: 0.06)." Hvorfor kan ikke journalen posteres?

## <a name="resolution"></a>Løsning

Under postering til økonomimodulen må hvert bilag balanseres i transaksjonsvalutaen, regnskapsvalutaen og rapporteringsvalutaen, hvis disse valutaene er definert på siden **Finansoppsett**. (Bilag balanseres når de total debet er lik total kredit.)

Nederst på journallinjesiden vises totaler i regnskapsvalutaen og rapporteringsvalutaen. De vises **ikke** i transaksjonsvalutaen for transaksjoner med utenlandsk valuta. I tillegg viser feilmeldingen som brukere mottar under simulering eller postering, forskjellene bare i regnskapsvalutaen og rapporteringsvalutaen. Den viser dem ikke i transaksjonsvalutaen, fordi et enkelt bilag kan ha mer enn én transaksjonsvaluta, og journalen kan inkludere bilag i forskjellige transaksjonsvalutaer. Det er derfor viktig at du manuelt kontrollerer at transaksjonsvalutabeløpene for hvert bilag som bare har én transaksjonsvaluta, er balansert.

### <a name="transaction-currency"></a>Transaksjonsvaluta

Under simulering og postering kontrollerer systemet at hvert bilag som bare har én transaksjonsvaluta, er balansert i transaksjonsvalutaen. For hvert bilag som er angitt, kan det være én eller flere valutaer for transaksjonsvalutaen. Et bilag som for eksempel angis i den generelle journalen, kan ha to transaksjonsvalutaer når det overføres kontanter fra en bankkonto som bruker euro (EUR) til en bankkonto som bruker kanadiske dollar (CAD).

Hvis et bilag bare har én transaksjonsvaluta, må totaldebetene tilsier det totale kreditbeløpet i transaksjonsvalutaen for dette bilaget. Kundene har oppstått følgende scenarier der posteringen mislyktes fordi transaksjonsvalutabeløpene ikke var i balanse:

- Total debet og total kredit var **ikke** balansert i transaksjonsvalutaen, men de ble balansert for regnskapsvalutaen og rapporteringsvalutaen. En kunde antok at bilaget fremdeles ville bli postert. Denne forutsetningen var imidlertid feil. **Transaksjonsvalutabeløpene på et bilag må alltid balanseres når alle linjene i bilaget har samme transaksjonsvaluta.**
- Bilaget ble importert med en dataenhet gjennom Data Management Framework (DMF), og brukeren mente at transaksjonsvalutabeløpene ble balansert. I importfilen hadde noen av beløpene mer enn to desimalplasser, og mer enn to desimalplasser ble inkludert da beløpene ble importert. Derfor er ikke debetverdiene lik kreditverdiene, fordi de var i ubalanse med en brøkdel av et øre. Journalen gjenspeiler ikke denne forskjellen på linjene i bilaget, fordi beløpene som vises, bare har to desimaler.
- Bilaget ble importert med en dataenhet via DMF, og brukeren trodde at transaksjonsvalutabeløpene ble balansert. Selv om **bilaget** ble balansert, hadde noen linjer på bilaget forskjellige transaksjonsdatoer. Hvis du la til total debet og total kredit i transaksjonsvalutaen per **bilags- og transaksjonsdato**, ble de ikke balansert. Dette kravet håndheves når du angir et bilag via økonomijournalen i systemet. Det håndheves imidlertid ikke når et bilag importeres med en dataenhet via DMF.

I ett støttet scenario kan et bilag ha mer enn én transaksjonsvaluta. I dette tilfellet verifiserer **ikke** systemet at debet er lik kredit i transaksjonsvalutaen, fordi valutaene stemmer ikke. I stedet kontrollerer systemet at regnskapsvalutabeløpene og rapporteringsvalutabeløpene er balansert.

### <a name="accounting-currency"></a>Regnskapsvaluta

Hvis alle linjene i et bilag har samme transaksjonsvaluta, og hvis transaksjonsvalutabeløpene er balansert, bekrefter systemet at regnskapsvalutabeløpene er balansert. Hvis bilaget er angitt i en fremmed valuta, brukes valutakursen på bilagslinjene til å regne om transaksjonsvalutabeløpene til regnskapsvalutaen. Først oversettes og avrundes hver linje i bilaget til to desimalplasser. Deretter blir linjene summert for å bestemme total debet og totale kredit. Fordi hver linje er omregnet, er det ikke sikkert at total debet og total kredit er balansert. Men hvis absoluttverdien for forskjellen er innenfor verdien for **Maksimal øredifferanse** som er definert på siden **Parametere for økonomimodul**, posteres bilaget, og differansen posteres automatisk til øredifferansekontoen.

Hvis bilaget har mer enn én transaksjonsvaluta, blir hver linje i bilaget omregnet til regnskapsvalutaen og avrundet til to desimalplasser, og linjene summeres for å fastsette total debet og total kredit. Hvis de skal anses som balansert, må debetbeløpene og kredittbeløpene balanseres, enten som omregning eller når avrundingsdifferansen for regnskapsvalutaen er inkludert.

### <a name="reporting-currency"></a>Rapporteringsvaluta

Hvis alle linjene i et bilag har samme transaksjonsvaluta, og hvis transaksjonsvalutabeløpene er balansert, bekrefter systemet at rapporteringsvalutabeløpene er balansert. Hvis bilaget er angitt i en fremmed valuta, brukes valutakursen på bilagslinjene til å regne om transaksjonsvalutabeløpene til rapporteringsvalutaen. Først oversettes og avrundes hver linje i bilaget til to desimalplasser. Deretter blir linjene summert for å bestemme total debet og totale kredit. Fordi hver linje er omregnet, er det ikke sikkert at total debet og total kredit er balansert. Men hvis forskjellen er innenfor verdien for **Maksimal øresavrunding i rapporteringsvaluta** som er definert på siden **Parametere for økonomimodul**, posteres bilaget, og differansen posteres automatisk til øredifferansekontoen.

Hvis bilaget har mer enn én transaksjonsvaluta, blir hver linje i bilaget omregnet til rapporteringsvalutaen og avrundet til to desimalplasser, og linjene summeres for å fastsette total debet og total kredit. Hvis de skal anses som balansert, må debetbeløpene og kredittbeløpene balanseres, enten som omregning eller når avrundingsdifferansen for rapporteringsvalutaen er inkludert.

### <a name="example-for-an-accounting-currency-imbalance"></a>Eksempel på ubalanse i regnskapsvaluta

> [!NOTE]
> Rapporteringsvalutabeløpet beregnes fra transaksjonsvalutabeløpet på samme måte som regnskapsvalutabeløpet.

Valutakurs: 1,5

| Linje | Bilag | Konto | Valuta | Debet (transaksjon) | Kredit (transaksjon) | Debet (regnskap) | Kredit (regnskap) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10,00 | | 15.00 |
| **Totalsum** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Regnskapsvalutaen er ikke i balanse med 0,01. Men så lenge maksimal øreavrunding i regnskapsvalutaen er minst 0,01, posteres differansen automatisk til øredifferansekontoen, og bilaget posteres.
