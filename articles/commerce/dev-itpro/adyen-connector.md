---
title: Oversikt over Dynamics 365 Payment Connector for Adyen
description: Denne artikkelen inneholder en oversikt over Microsoft Dynamics 365 Payment Connector for Adyen.
author: rassadi
ms.date: 10/27/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 931fc69cda8daa2e06b6f1155fbf0369fd2bca55
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728309"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>Oversikt over Dynamics 365 Payment Connector for Adyen

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder en oversikt over Microsoft Dynamics 365 Payment Connector for Adyen og en omfattende liste over funksjoner og funksjonalitet som støttes. Beslektede artikler tar for seg registrering for Adyen, konfigurasjon av koblingen, vanlige spørsmål og feilsøkingsveiledning for enkelte vanlige problemer.

## <a name="key-terms"></a>Viktige termer

| Semester | Beskrivelse |
|---|---|
| Betalingskobling | En utvidelse som legger til rette for kommunikasjon mellom Microsoft Dynamics 365 Commerce (og tilknyttede komponenter) og en betalingstjeneste. Koblingen som beskrives i denne artikkelen, ble implementert ved hjelp av SDK for standard betalinger. |
| Kort forevises | Refererer til betalingstransaksjoner der et fysisk kort forevises og brukes på en betalingsterminalkobling til Dynamics 365 Point of Sale. |
| Kort forevises ikke | Refererer til betalingstransaksjoner der et fysisk kort ikke forevises, for eksempel i scenarioer med e-handel eller telefonsenter. I disse scenarioene angis den betalingsrelaterte informasjonen manuelt på et nettsted for e-handel, i en telefonsenterflyt eller på salgsstedet eller betalingsterminalen. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Funksjoner, funksjonalitet, versjoner og terminaler som støttes

Den bruksklare Dynamics 365 Payment Connector for Adyen bruker SDK for standard betaling. Den har derfor ikke spesialfunksjoner som ikke også er tilgjengelige for andre betalingskoblinger.

### <a name="supported-versions"></a>Støttede versjoner

#### <a name="microsoft-dynamics-365-supported-versions"></a>Versjon er som støttes av Microsoft Dynamics 365
Det er støtte for den bruksklare førstepartskoblingen Dynamics 365 Payment Connector for Adyen i Microsoft Dynamics 365 Finance versjon 8.1.3 (januar 2019) eller senere, og i Microsoft Dynamics 365 Retail versjon 8.1.3 eller nyere. Tredjeparter kan imidlertid fortsatt utvikle andre betalingskoblinger for Adyen for tidligere versjoner av Microsoft Dynamics 365.

#### <a name="supported-adyen-firmware-versions"></a>Støttede Adyen-fastvareversjoner

Listen nedenfor beskriver den eldste og nyeste Adyen-fastvareversjonen som støttes for hver versjon av Microsoft Dynamics 365 Retail POS.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail POS versjon 10.0.25
| Eldste Adyen-fastvareversjon | Nyeste Adyen-fastvareversjon |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail POS versjon 10.0.26
| Eldste Adyen-fastvareversjon | Nyeste Adyen-fastvareversjon |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail POS versjon 10.0.27
| Eldste Adyen-fastvareversjon | Nyeste Adyen-fastvareversjon |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail POS versjon 10.0.28
| Eldste Adyen-fastvareversjon | Nyeste Adyen-fastvareversjon |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail POS versjon 10.0.29
| Eldste Adyen-fastvareversjon | Nyeste Adyen-fastvareversjon |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail POS versjon 10.0.30
| Eldste Adyen-fastvareversjon | Nyeste Adyen-fastvareversjon |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen kan gi ut underordnede versjonsoppdateringer etter at Microsoft har testet hovedversjonen. Så lenge en hovedversjon støttes, er det OK å ha underordnede versjonsoppdateringer i samme hovedversjon. Disse oppdateringene er vanligvis svært målrettede rettelser og oppfyller ikke kriteriene for ny testing så lenge den samme fastvarehovedversjonen ble testet tidligere. Oppdateringer skal ikke overskride den nyeste Adyen-fastvareversjonen som er oppført i dokumentasjonen. 
>
> Hvis du vil gå over fra en Adyen-fastvareversjon som er eldre enn versjon 53, til versjon 53, må du ha POS KB **4577957** for månedlige oppdateringer av Commerce, versjoner 10.0.11 til og med 10.0.14. Hvis en av disse versjonene er i bruk og ikke omfatter hurtigreparasjonen, tillates bare betalinger via NFC etter oppgraderingen av betalingsterminalen. Hvis du bruker hurtigreparasjonen på POS, løses dette problemet. Hvis POS-versjonen er eldre enn versjon 10.0.11, kan du sende en støtteforespørsel der du gir beskjed om at en rettelse for KB **4577957** kreves for en MPOS som er ute av drift.
> 
> Når det gjelder Adyen-fastvareversjonene 59p7 til og med 62p9, ber operasjonen **innløsing av gavekort i kontanter** om PIN-koden to ganger i scenarioer der gavekortet angis manuelt. Dette problemet oppstår ikke når gavekortet leses. Adyen undersøker problemet. 

### <a name="supported-payment-terminals"></a>Støttede betalingsterminaler
Dynamics 365 Payment Connector for Adyen drar nytte av den enhetsagnostiske [API-en for Adyen Payment Terminal](https://www.adyen.com/blog/introducing-the-terminal-api). Den støtter alle betalingsterminaler som denne API-en (programmeringsgrensesnitt) støtter. Hvis du vil ha en fullstendig liste over betalingsterminaler som støttes, kan du gå til siden [Adyen POS-terminaler](https://www.adyen.com/pos-payments/terminals).

### <a name="supported-payment-instruments"></a>Støttede betalingsmåter

#### <a name="supported-debit-and-credit-cards"></a>Debet- og kredittkort som støttes

| Merke | Variant | Kort forevises | e-handel | Telefonsenter |
|---|---|:-:|:-:|:-:|
| MasterCard | Kreditt | ✔ | ✔ | ✔ |
| MasterCard | Debet | ✔ | ✔ | ✔ |
| MasterCard | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| MasterCard | Apple Pay | ✔ |  |  |
| MasterCard | Samsung Pay | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Maestro Samsung Pay | ✔ |  |  |
| MasterCard | Maestro UK | ✔ | ✔ | ✔ |
| VISA | Kreditt | ✔ | ✔ | ✔ |
| VISA | Debet | ✔ | ✔ | ✔ |
| VISA | Alpha Bank Bonus | ✔ | ✔ | ✔ |
| VISA | Android Pay | ✔ |  |  |
| VISA | Apple Pay | ✔ |  |  |
| VISA | Samsung Pay | ✔ |  |  |
| VISA | VISA Checkout | ✔ | ✔ | ✔ |
| VISA | VISA Dankort | ✔ | ✔ | ✔ |
| VISA | VISA Hipotecario | ✔ | ✔ | ✔ |
| VISA | VISA Aravia Card | ✔ | ✔ | ✔ |
| AMEX | Kreditt | ✔ | ✔ | ✔ |
| AMEX | Debet | ✔ | ✔ | ✔ |
| AMEX | Android Pay | ✔ |  |  |
| AMEX | Apple Pay | ✔ |  |  |
| AMEX | Samsung Pay | ✔ |  |  |
| AMEX | AMEX Commercial | ✔ | ✔ | ✔ |
| AMEX | AMEX Consumer | ✔ | ✔ | ✔ |
| AMEX | AMEX Corporate | ✔ | ✔ | ✔ |
| AMEX | AMEX Small Business | ✔ | ✔ | ✔ |
| Discover Card | Standard | ✔ | ✔ | ✔ |
| Discover Card | Android Pay | ✔ |  |  |
| Discover Card | Apple Pay | ✔ |  |  |
| Discover Card | Samsung Pay | ✔ |  |  |
| Diners   | Standard | ✔ | ✔ | ✔ |
| Dineromail | Standard | ✔ | ✔ | ✔ |
| JCB | Standard | ✔ | ✔ | ✔ |
| Union Pay\* | Standard | ✔ |  |  |
| Interac Debit\* | Standard | ✔ |  |  |

\*Regelmessige korttokener fra Interac og Union Pay leveres ikke av Adyen, så de kan ikke støttes ved transaksjoner der kort ikke forevises.

#### <a name="supported-gift-cards"></a>Støttede gavekort
| Skjema | Kort forevises | Kort forevises ikke |
|---|:-:|---|
| Givex | ✔ | ✔ |
| SVS | ✔ | ✔ |

For å kunne støtte disse eksterne gavekortordningene via Dynamics 365 Payment Connector for Adyen må du fullføre ytterligere trinn. Hvis du vil ha mer informasjon, kan du se [Støtte for eksterne gavekort](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Støttede lommebøker

| Ordning | Kort forevises | Kort forevises ikke |
|---|---|---|
| Alipay | Støtte legges til i en fremtidig versjon. | Nei |
| WeChat | Støtte legges til i en fremtidig versjon. | Nei |

#### <a name="supported-card-present-input-methods"></a>Støttede inndatametoder for kort som forevises
| Inndatametode | Støttes | Notater |
|---|:-:|---|
| Sett inn | ✔ | |
| Dra | ✔ | |
| Tæpp | ✔ | |
| Manuell registrering via POS-grensesnitt. |  | Støttes ikke for øyeblikket |
| Manuell registrering via betalingsterminal. | ✔ | Støtter manuell registrering av kreditt-, debet- og gavekort med angivelse av PIN-kode. | 


#### <a name="supported-card-present-countries"></a>Støttede land for kort som forevises

Følgende land har Commerce-komponenter tilgjengelige og støtte for kort som forevises, fra Adyen. Hvis du vil ha gjeldende internasjonale tilgjengelighet for Commerce, kan du gå til [siden for internasjonal tilgjengelighet](/dynamics365/get-started/availability).

| Land | Støttes |
| --- | :-: |
| Australia | ✔ |
| Østerrike | ✔ |
| Belgia | ✔ |
| Canada | ✔ |
| Tsjekkia | ✔ |
| Danmark | ✔ |
| Estland | ✔ |
| Finland | ✔ |
| Frankrike | ✔ |
| Tyskland | ✔ |
| Hongkong SAR | ✔ |
| Ungarn | ✔ |
| Island | ✔ |
| Irland | ✔ |
| Italia | ✔ |
| Japan | Fremtidig versjon |
| Latvia | ✔ |
| Litauen | ✔ |
| Malaysia | ✔ |
| Nederland | ✔ |
| New Zealand | ✔ |
| Norge | ✔ |
| Polen | ✔ |
| Singapore | ✔ |
| Sveits | ✔ |
| Spania | ✔ |
| Sverige | ✔ |
| Sveits | ✔ |
| Storbritannia | ✔ |
| USA | ✔ |
| Brasil | Fremtidig versjon |

#### <a name="supported-card-not-present-countries"></a>Støttede land for kort som ikke forevises

Følgende land støttes av Adyen for transaksjoner der kort ikke forevises. [Kontakt Adyen](https://www.adyen.com/contact/sales) hvis du vil ha informasjon om støtte for et bestemt land. Hvis du vil ha gjeldende internasjonale tilgjengelighet for Commerce, kan du gå til [siden for internasjonal tilgjengelighet](/dynamics365/get-started/availability).

| Land | 
| --- |
| Argentina |
| Armenia |
| Australia |
| Østerrike |
| Bahrain |
| Belgia |
| Brasil |
| Bulgaria |
| Canada |
| Chile |
| Kina |
| Colombia |
| Kroatia |
| Kypros |
| Tsjekkia  |
| Danmark |
| Egypt |
| Estland |
| Finland |
| Frankrike |
| Georgia |
| Tyskland |
| Gibraltar |
| Hellas |
| Guernsey |
| Hongkong SAR |
| Ungarn |
| Island |
| India |
| Indonesia |
| Irland |
| Isle of Man |
| Israel |
| Italia |
| Japan |
| Jersey |
| Sør-Korea |
| Kuwait |
| Latvia |
| Litauen |
| Luxemburg |
| Malaysia |
| Malta |
| Mexico |
| Marokko |
| Nederland |
| New Zealand |
| Norge |
| Peru |
| Polen |
| Portugal |
| Qatar |
| Romania |
| Saudi-Arabia |
| Serbia |
| Singapore |
| Slovakia |
| Slovenia |
| Sør-Afrika |
| Spania |
| Sverige |
| Sveits |
| Taiwan |
| Tanzania |
| Thailand |
| Tyrkia |
| De forente arabiske emirater (UAE) |
| Storbritannia |
| USA, inkludert Puerto Rico  |

#### <a name="supported-dynamics-365-payment-features"></a>Støttede Dynamics 365-betalingsfunksjoner

Følgende tabell viser funksjonssettet som Dynamics 365 Payment Connector for Adyen støtter. Disse funksjonene bruker forbedringer som ble innført i SDK for betalinger og enkelte komponenter i desember 2018. De er ikke utelukkende for Dynamics 365 Payment Connector for Adyen. Hvis du vil ha mer informasjon om hvordan du tar i bruk disse forbedringene for en annen betalingskobling, kan du se [Opprett en komplett betalingsintegrering for en betalingsterminal](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Ordning | Kort forevises | Kort forevises ikke |
|---|:-:|:-:|
| [Balanse for innløsing av gavekort i kontanter](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Duplisert betalingsbeskyttelse](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Tokenisering av omnikanal | ✔ | ✔ |
| Sammenkoblede refunderinger | ✔<br>(Fra og med 10.0.1) | ✔<br>(Fra og med 10.0.1) |
| [Lagre nettbetalinger](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Fra og med 10.0.2) | 
| [Eksterne gavekort for telefonsenter og e-handel](./gift-card.md) | ✔<br>(Fra og med 10.0.10) | 
| [Omdirigering av SCA-betaling](../adyen_redirect.md) | | ✔<br>(Fra og med 10.0.12) |
| [Dedikerte betalingsterminaler og ledetekster for en skriver og kassaskuff](../pos-multi-hws.md) | ✔<br>(Fra og med 10.0.12) | |
| [Støtte for tipsing på SDK-nivå via Adyen-koblingen](tipping.md) | ✔<br>(Fra og med 10.0.14) | |
| [Trinnvis lagring av ordrefakturering](incremental-capture.md) |  | ✔<br>(Fra og med 10.0.18) |
| [Lommebokbetalinger](../wallets.md) |  | ✔<br>(Fra og med 10.0.20) |
| [Google Pay med Adyen](google-pay-adyen.md) |  | ✔<br>(Fra og med 10.0.27) |

## <a name="next-steps"></a>Neste trinn

Hvis du vil ha informasjon om hvordan du registrerer deg for og konfigurerer Dynamics 365 Payment Connector for Adyen, kan du se [Konfigurasjon av Dynamics 365 Payment Connector for Adyen](adyen-connector-setup.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurer Dynamics 365 Payment Connector for Adyen](adyen-connector-setup.md)

[Vanlige spørsmål om Dynamics 365 Payment Connector for Adyen](adyen-connector-faq.md)

[Feilsøk problemer med Dynamics 365 Payment Connector for Adyen](adyen-connector-troubleshoot.md)

[Vanlige spørsmål om betalinger](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
