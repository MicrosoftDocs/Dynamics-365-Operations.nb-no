--- 
title: Generere elektroniske dokumenter for betalinger ved hjelp av en formatkonfigurasjon for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan bruke en ny formatkonfigurasjon for elektronisk rapportering (ER) til å generere elektroniske betalingsdokumenter for behandling av betalinger."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 95da806cc2844dc946e809f1afecef25a7b520e5
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>Generere elektroniske dokumenter for betalinger ved hjelp av en formatkonfigurasjon for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan bruke en ny formatkonfigurasjon for elektronisk rapportering (ER) til å generere elektroniske betalingsdokumenter for behandling av betalinger. Denne fremgangsmåten kan utføres i GBSI-eksempelfirmaet.

For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjon med formatet betalingsdokument".


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Endre konfigurasjonen for den elektroniske betalingsmåten
1. Gå til Leverandører > Betalingsoppsett > Betalingsmåter.
2. Aktiver/deaktiver filformatdelen for å vise den ved behov.
3. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien Elektronisk.
4. Klikk Rediger.
5. Sett feltet Generell elektronisk rapportering til Ja.
    * Velg Ja hvis du vil bruke det generelle elektroniske rapporteringsmønsteret for generering av betalingsfiler.  
6. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
7. Velg formatkonfigurasjonen BACS (Storbritannia fiktivt).
8. Klikk Lagre.
9. Lukk siden.

## <a name="test-the-format-of-generated-payment-files"></a>Teste formatet for genererte betalingsfiler
1. Gå til Leverandører > Betalinger > Betalingsjournal.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
    * Velg VendPay.  
6. Klikk Lagre.
7. Klikk Linjer.
8. Skriv DEMF i feltet Firma.
    * DEMF  
9. Angi verdiene DE-01001 i Konto-feltet.
    * DE - 01001  
10. Skriv inn Betaling i Beskrivelse-feltet.
    * Betaling  
11. Angi et tall i Debet-feltet.
    * 10 000  
12. Klikk kategorien Betaling.
13. Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.
14. Finn og velg ønsket post i listen.
    * Velg den elektroniske verdien.  
15. Klikk koblingen i den valgte raden i listen.
16. Klikk Lagre.
17. Klikk Generer betalinger.
18. Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.
19. Finn og velg ønsket post i listen.
    * Velg den elektroniske verdien.  
20. Klikk koblingen i den valgte raden i listen.
    * Velg den elektroniske verdien.  
21. Skriv inn en verdi i feltet Filnavn.
    * Skriv for eksempel betalinger.  
22. Klikk rullegardinknappen i Bankkonto-feltet for å åpne oppslaget.
23. Klikk koblingen i den valgte raden i listen.
    * Velg verdien GBSI OPER.  
24. Klikk OK.
25. Klikk OK.
    * Analyser den opprettede betalingsfilen i XML-format. Sammenligne den med det utformede dokumentoppsettet og de definerte attributtene for betalingtransaksjonen.  

