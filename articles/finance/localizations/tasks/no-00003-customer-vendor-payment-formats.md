---
title: NO-00003 Betalingsformater for kunde og leverandør
description: Denne oppgaven hjelper deg med å konfigurere og vedlikeholde norske betalings-ID-er.
author: EricWangChen
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: wangchen
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- BankCustPaymIdTable, LogisticsCountryRegionPaymentIdType_NO, CustTable, CustPaymMode, CustGroup
- CustInvoiceJournal
ms.openlocfilehash: 521e23ea944425e43c45f4813c387f099d1f4445
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292172"
---
# <a name="no-00003-customer-and-vendor-payment-formats"></a>NO-00003 Betalingsformater for kunde og leverandør

[!include [banner](../../includes/banner.md)]

Denne oppgaven hjelper deg med å konfigurere og vedlikeholde norske betalings-ID-er. 



En betalingsidentifikasjon (ID) er en unik identifikator for kundebetalinger som utlignes elektronisk. Den kan deles inn i ulike deler, for eksempel kundekontonummer, fakturanummer, prefiks, suffiks og ekstern referanse. Når du mottar en betaling fra en kunde, identifiserer betalings-IDen betalingstransaksjonen for en salgsfaktura som er mottatt fra en bank.



Denne oppgaven ble opprettet med demodatafirmaet DEMF med land/område for primæradresse for juridisk enhet oppdatert til å være Norge.


## <a name="set-up-payment-ids"></a>Definer betalings-IDer
1. Gå til Kunder > Betalingsoppsett > Betalings-ID.
2. Klikk Ny.
3. Skriv inn en verdi i Betalings-ID-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Angi en verdi i feltet Lengde på betalings-ID.
6. Angi et tall i feltet Konto fra posisjon.
7. Angi et tall i feltet Konto til posisjon.
8. Angi et tall i feltet Faktura fra posisjon.
9. Angi et tall i feltet Faktura til posisjon.
10. Velg et Modulus 10 i feltet Modulus.
    * Velg moduluskontrollmetoden som skal beregne sjekknummeret. Det siste sifferet i en betalings-ID er reservert for sjekknummeret for å verifisere at betalings-IDen er gyldig. Følgende alternativer er tilgjengelige: - Modulus 10 – Samlet lengde på betalings ID-en deles på 10. Resten blir sjekknummeret.   - Modulus 11 – Samlet lengde på betalings-ID-en deles på 11. Resten blir sjekknummeret.   - (Ingen) – Sjekknummer beregnes ikke.  
11. Klikk Lagre.
    * Når du har lagret posten, kan du forhåndsvise den valgte betalings-ID-en i feltet Betalings-ID-test.  
12. Gå til Kunder > Betalingsoppsett > Betalings-ID per land/område.
13. Klikk Ny.
14. Angi eller velg en verdi i Land/område-feltet.
15. Angi eller velg en verdi i feltet Betalings-ID-type.
16. Klikk Lagre.

## <a name="attach-the-payment-id"></a>Tilknytte betalings-ID-en
1. Gå til Kunder > Kunder > Alle kunder.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Konto-feltet med verdien DE-010.
3. Klikk koblingen i den valgte raden i listen.
4. Utvid delen Betalingstandarder.
5. Klikk Rediger.
6. Angi eller velg en verdi i feltet Betalings-ID-type.
7. Klikk Lagre.
8. Gå til Kunder > Betalingsoppsett > Betalingsmåter.
9. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien ELEKTRONISK.
10. Klikk Rediger.
11. Utvid delen Betalingskontroll.
12. Angi eller velg en verdi i feltet Betalings-ID-type.
13. Klikk Lagre.
14. Gå til Kunder > Oppsett > Kundegrupper.
15. Klikk Rediger.
16. Angi eller velg en verdi i feltet Betalings-ID-type.
17. Klikk Lagre.

## <a name="update-the-payment-id"></a>Oppdatere betalings-ID-en
1. Gå til Kunder > Periodiske oppgaver > Oppdater betalings-ID for faktura.
2. Merk av for Slett betalings-ID hvis du vil slette betalings-ID-informasjon fra alle dokumenter.
    * Dette alternativet bør bare brukes når du vil fjerne eller oppdatere betalings-ID-er for dokumenter som fikk tilordnet betalings-ID-er. Du vil se en dialogboks der du kan slette betalings-ID fra bestemte dokumenttyper.  
3. Velg Ja i feltet Oppdater betalings-ID for faktura.
4. Klikk OK.
5. Klikk Ja.
6. Klikk Ja.
7. Klikk Ja.
8. Klikk Ja.

## <a name="view-the-payment-id"></a>Vise betalings-ID-en
1. Gå til Kundereskontro > Forespørsler og rapporter > Fakturaer > Fakturajournal.
2. Klikk Vis filtre.
3. Bruk følgende filtre: Angi en filterverdi for "" i feltet "Betalings-ID" ved hjelp av filteroperatoren "er ikke".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
