---
title: ER Generere elektroniske dokumenter for betalinger ved hjelp av en formatkonfigurasjon
description: Dette emnet beskriver hvordan du bruker en ny formatkonfigurasjon for elektronisk rapportering (ER) til å generere elektroniske dokumenter til behandling av betalinger.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05295ff36ffd194b3f50fcdd9d7528c787c80f39104f46f9c51890a75a852735
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712670"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>ER Generere elektroniske dokumenter for betalinger ved hjelp av en formatkonfigurasjon

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan bruke en ny formatkonfigurasjon for elektronisk rapportering (ER) til å generere elektroniske betalingsdokumenter for behandling av betalinger. Denne fremgangsmåten kan utføres i GBSI-eksempelfirmaet.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjon med formatet betalingsdokument".


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Endre konfigurasjonen for den elektroniske betalingsmåten
1. Gå til Leverandører > Betalingsoppsett > Betalingsmåter.
2. Aktiver/deaktiver filformatdelen for å vise den ved behov.
3. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien Elektronisk.
4. Klikk på Rediger.
5. Sett feltet Generell elektronisk rapportering til Ja.
    * Velg Ja hvis du vil bruke det generelle elektroniske rapporteringsmønsteret for generering av betalingsfiler.  
6. Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.
7. Velg formatkonfigurasjonen BACS (Storbritannia fiktivt).
8. Klikk på Lagre.
9. Lukk siden.

## <a name="test-the-format-of-generated-payment-files"></a>Teste formatet for genererte betalingsfiler
1. Gå til Leverandører > Betalinger > Betalingsjournal.
2. Klikk på Ny.
3. Merk den valgte raden i listen.
4. Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.
5. Klikk på koblingen i den valgte raden i listen.
    * Velg VendPay.  
6. Klikk på Lagre.
7. Klikk på Linjer.
8. Skriv DEMF i feltet Firma.
    * DEMF  
9. Angi verdiene DE-01001 i Konto-feltet.
    * DE - 01001  
10. Skriv inn Betaling i Beskrivelse-feltet.
    * Betaling  
11. Angi et tall i Debet-feltet.
    * 1 000  
12. Klikk på fanen Betaling.
13. Klikk på rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.
14. Finn og velg ønsket post i listen.
    * Velg den elektroniske verdien.  
15. Klikk på koblingen i den valgte raden i listen.
16. Klikk på Lagre.
17. Klikk på Generer betalinger.
18. Klikk på rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.
19. Finn og velg ønsket post i listen.
    * Velg den elektroniske verdien.  
20. Klikk på koblingen i den valgte raden i listen.
    * Velg den elektroniske verdien.  
21. Skriv inn en verdi i feltet Filnavn.
    * Skriv for eksempel betalinger.  
22. Klikk på rullegardinknappen i Bankkonto-feltet for å åpne oppslaget.
23. Klikk på koblingen i den valgte raden i listen.
    * Velg verdien GBSI OPER.  
24. Klikk på OK.
25. Klikk på OK.
    * Analyser den opprettede betalingsfilen i XML-format. Sammenligne den med det utformede dokumentoppsettet og de definerte attributtene for betalingtransaksjonen.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]