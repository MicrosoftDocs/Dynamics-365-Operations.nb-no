---
title: Oversikt over SEPA-avtalegiro
description: "Felles eurobetalingsområde (SEPA) er satt opp av EU-kommisjonen, og angir at alle elektroniske betalinger betraktes som innenlandsbetalinger, uavhengig av landet/regionen der personen, virksomheten eller organisasjonen, og banken befinner seg. Det er ingen forskjell mellom nasjonale betalinger og betalinger over grenser. SEPA omfatter de 28 EU-medlemslandene pluss Island, Liechtenstein, Norge, Sveits, Monaco og San Marino. SEPA bidrar til å danne ett marked for betalingstransaksjoner i EØS. I siste instans forventes det at SEPA til slutt reduserer antall betalingsformater som banker, bedrifter og enkeltpersoner må arbeide med."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f3b20b033fc701204cbb3f62468a421b3bdd6a80
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="sepa-direct-debit-overview"></a>Oversikt over SEPA-avtalegiro

[!include[banner](../includes/banner.md)]


Felles eurobetalingsområde (SEPA) er satt opp av EU-kommisjonen, og angir at alle elektroniske betalinger betraktes som innenlandsbetalinger, uavhengig av landet/regionen der personen, virksomheten eller organisasjonen, og banken befinner seg. Det er ingen forskjell mellom nasjonale betalinger og betalinger over grenser. SEPA omfatter de 28 EU-medlemslandene pluss Island, Liechtenstein, Norge, Sveits, Monaco og San Marino. SEPA bidrar til å danne ett marked for betalingstransaksjoner i EØS. I siste instans forventes det at SEPA til slutt reduserer antall betalingsformater som banker, bedrifter og enkeltpersoner må arbeide med.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>Hva er formålet med SEPA-avtalegiroer?
---------------------------------------

Med en SEPA-avtalegiro kan kreditor kreve inn penger fra kundens bankkonto, forutsatt at kunden har gitt kreditoren et signert mandat. Kunden signerer en mandat som tillater kreditor å kreve betaling og instruerer kundens bank om å betale purringen. 

SEPA-avtalegiro oppretter, for første gang, et betalingsmiddel som kan brukes for både nasjonale og internasjonale avtalegiroer i euro i alle de 32 SEPA-landene/-områdene. 

Det finnes to oppsett: hovedskjemaet for SEPA-avtalegiro og SEPA-avtalegiroskjemaet for bedrifter (B2B). Begge planene bruker samme filformat.

## <a name="what-is-the-core-direct-debit-scheme"></a>Hva er hovedskjemaet for avtalegiro?
Hovedskjemaet for SEPA-avtalegiro er det grunnleggende skjemaet. Det har følgende attributter:
-   Overføring av kapital skjer i euro (selv om bankkontoene kan inneholde midler i andre valutaer).
-   Kunden og kreditoren må begge ha en konto hos en kredittinstitusjon som ligger i SEPA.
-   Kunden må gi en signert mandat til kreditor.
-   Mandater utløper 36 måneder etter siste startede samling.
-   Kreditor må lagre mandater så lenge mandatet er gyldig og i minst 14 måneder etter siste trekk.
-   Skjemaet kan brukes for én (engangs) avtalegiro eller gjentakende avtalegirosamlinger.
-   Kunder har rett til refusjon "uten at det stilles spørsmål" i inntil åtte uker etter at kontoen ble debitert.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Hva er et SEPA-avtalegiroskjemaet for bedrifter (B2B)?
B2B-SEPA-avtalegiroskjemaet gjelder for bedriftstransaksjoner og bygger på hovedskjemaet for SEPA-avtalegiro. De viktigste forskjellene er:
-   B2B-SEPA-avtalegiroskjemaeter er ikke tillatt når kunden er en privatperson (forbruker).
-   Kunden har ikke rett til å få refundert ent godkjent transaksjon.
-   Kundebanker må kontrollere at trekket er godkjent, ved å kontrollere trekket mot informasjon om mandatet. Kundebanker og kunder må bli enige om kontrollen som skal utføres for hver enkelt avtalegiro.
-   Skjemaet har en kortere tidslinje for å vise avtalegiroer og reduserer returperioden.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Kan jeg bruke COR1-planen for avtalegiromandater?
Ja. Du kan bruke skjemaet COR1 for SEPA-avtalegiromandater i Østerrike, Belgia, Tyskland, Frankrike, Italia, Spania og Nederland. Skjemaet gir en kortere forhåndsvarsling for avtalegirosamlingen for kreditoren.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Hva er internasjonale bankkontonumre (IBAN) og bankidentifiseringskoder (BIC)?
IBAN (International Bank Account Number) og BIC (Bank Identifier Code) brukes til å identifisere kontoer i 32 SEPA-land/-områder. Angi BIC i SWIFT-kodefeltet og IBAN i IBAN-feltet. Begge feltene er plassert i hurtigfanen Tilleggsidentifikasjon i fanen Bankkonto på Bankkonto-siden. Dette gjelder for både kreditorens bankkonto og kundens bankkonto.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Hvor angir jeg kreditor-ID-er (Direkte debet-ID-er)?
I SEPA identifiseres hver kreditor av en unik kreditor-ID. Denne identifikatoren lar kunden og kundebanken filtrere hver avtalegiro, og behandler eller avviser deretter eller direkte debet i henhold til instruksjoner for kunden. Kreditorer må be om denne identifikatoren gjennom banken. Angi denne identifikatoren i Direkte debet-ID-feltet for bankkontoen for den juridiske enheten.

## <a name="what-are-mandates"></a>Hva er mandater?
Kunden signerer en mandat som tillater kreditor å kreve betaling og instruerer kundens bank om å betale purringen. Kunden kan utstede mandatet i papirform eller elektronisk. Mandatet utløper som standard 36 måneder etter at avtalegiroen sist ble startet.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Hvor angir jeg filformatet SEPA-avtalegiro (ISO 20022)
SEPA-dataformater er basert på meldingsstandardene i ISO 20022. Merk av for Generell elektronisk rapportering, og velg formatet SEPA-avtalegiro som eksportformatkonfigurasjon når du konfigurerer betalingsmåte for leverandører. Du bruker denne betalingsmåten når du genererer en betalingsfil i en kundebetalingsjournal.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>I hvilke filformater kan jeg generere betalingsfiler for SEPA-avtalegiro?
Du kan generere elektroniske betalingsfiler for SEPA-avtalegiroer i følgende formater:
-   Betalingsfiler for SEPA-avtalegiro i PAIN.008.001.02 XML-filformatet for Belgia, Tyskland, Spania, Frankrike, Italia og Nederland.
-   Betalingsfiler i SEPA-avtalegiro i PAIN.008.001.02 XML-filformatet for Østerrike, og i PAIN.008.003.02 XML-filformatet for Tyskland.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Hvordan fungerer refunderinger og returer med SEPA-avtalegiroer?
I henhold til begge SEPA-avtalegiroskjemaer har kunder bestemte rettigheter til refusjoner. Kunden kan tilbakekalle autoriserte transaksjoner i løpet av en periode på åtte uker etter forfallsdato, uten å måtte oppgi årsak. Når det gjelder uautoriserte transaksjoner, utvides perioden til 13 måneder etter forfallsdatoen. Tilbakeføringer av betalinger som er utført, gjøres manuelt ved hjelp av Avbryt betaling-knappen på Kundetransaksjoner-siden.






