---
title: Importere remburs
description: Denne prosedyren hjelper deg med å importere en remburs.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9f9c73ec1347e72f8cd4ae8eec580bb8fe3df8ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446464"
---
# <a name="import-letter-of-credit"></a>Importere remburs

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg med å importere en remburs. Følgende må defineres før du fullfører denne prosedyren: bankfasiliteter, posteringsprofiler, en bankfasilitetsavtale og leverandørbankdetaljer.

Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Opprette en bestilling med remburs
1. Gå til Leverandører > Bestillinger > Alle bestillinger.
2. Klikk Ny.
3. Angi eller velg en verdi i Leverandørkonto-feltet.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Utvid delen Generelt.
7. Angi eller velg en verdi i Område-feltet.
8. Klikk koblingen i den valgte raden i listen.
9. Angi eller velg en verdi i feltet Lager.
10. Klikk koblingen i den valgte raden i listen.
11. Angi en dato i feltet Regnskapsdato.
12. Angi en dato i Leveringsdato-feltet.
    * Obs!  Feltet Bankdokumenttype må velges med verdien Remburs.  
13. Klikk OK.
14. Angi eller velg en verdi i Varenummer-feltet.
15. Finn og velg ønsket post i listen.
16. Klikk koblingen i den valgte raden i listen.
17. Vis delen Linjedetaljer.
18. Velg kategorien Levering.
19. Angi en dato i Leveringsdato-feltet.
20. Angi en dato i Bekreftet leveringsdato-feltet.
21. Angi et tall i feltet Enhetspris.
    * Definer rembursdetaljene.  
22. Klikk Administrer i handlingsruten.
23. Klikk Remburs/importinkasso.
24. Angi dato og klokkeslett i Søknadsdato-feltet.
    * Kontroller at Bankkonto-feltet har en standard aktiv bankkonto, som er basert på programdatoen.  
25. Angi en verdi i feltet Bankdokumentnummer.
26. Angi dato og klokkeslett i Mottaksdato-feltet.
27. Vis delen Bankdokument.
28. Angi dato og klokkeslett i feltet Utløpsdato.
29. Vis delen Bankdetaljer.
30. Angi eller velg en verdi i Advisbank-feltet.
31. Klikk koblingen i den valgte raden i listen.
32. Klikk Lagre.
33. Klikk Hent bestillingsforsendelser.
34. Lukk siden.
35. Klikk Kjøp i handlingsruten.
36. Klikk Bekreft.
37. Klikk Administrer i handlingsruten.
38. Klikk Remburs/importinkasso.
39. Velg Behandle.
40. Klikk Bekreft.
    * Kontroller at fasilitetssaldoen reduserer bestillingsbeløpet.  I dette eksemplet: innkjøpsbeløp = 500,00, fasilitetsgrense = 10000,00, derfor fasilitetssaldo = 9500,00.  
41. Lukk siden.
42. Angi et tall i feltet Enhetspris.
43. Klikk Lagre.
44. Klikk Kjøp i handlingsruten.
45. Klikk Bekreft.
    * Endre rembursen på grunn av endringen i enhetspris.  
46. Klikk Administrer i handlingsruten.
47. Klikk Remburs/importinkasso.
    * Endre rembursen på grunn av endringen i innkjøpsenhetspris.  
48. Velg Behandle.
49. Klikk Endre.
50. Klikk Fjern.
51. Klikk Ja.
52. Klikk Hent bestillingsforsendelser.
53. Velg Behandle.
54. Klikk Bekreft.
    * Kontroller at fasilitetssaldoen reduserer bestillingsbeløpet.  I dette eksemplet: redigert innkjøpsbeløp = 600,00, fasilitetsgrense = 10000,00, derfor fasilitetssaldo = 9400,00.  
55. Lukk siden.

## <a name="post-packing-slip"></a>Postere følgeseddel
1. Klikk Motta i handlingsruten.
2. Klikk Produktkvittering.
3. Skriv inn en verdi i feltet PurchParmTable_Num.
    * Velg forsendelsesnummeret som ble opprettet med referanse til rembursen.  
4. Klikk koblingen i den valgte raden i listen.
5. Angi en dato i feltet Produktkvitteringsdato.
6. Klikk OK.
7. Lukk siden.
8. Lukk siden.

## <a name="verify-import-letter-of-credit-status"></a>Kontrollere statusen for rembursimporten
1. Gå til Kontant- og bankbehandling > Purringer > Importer remburs og importinkasso.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
    * Kontroller statusen for rembursimporten.     
4. Lukk siden.
5. Lukk siden.

## <a name="post-purchase-invoice"></a>Postere innkjøpsfaktura
1. Gå til Leverandører > Bestillinger > Alle bestillinger.
    * Velg bestillingen som ble opprettet med rembursen.  
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Faktura i handlingsruten.
5. Klikk Faktura.
6. Skriv inn en verdi i Nummer-feltet.
7. Angi eller velg en verdi i feltet Forsendelsesnummer.
8. Klikk koblingen i den valgte raden i listen.
9. Angi en dato i feltet Fakturadato.
10. Klikk Oppdater samsvarsstatus.
11. Klikk Poster.
12. Lukk siden.
13. Lukk siden.

## <a name="verify-import-letter-of-credit-status"></a>Kontrollere statusen for rembursimporten
1. Gå til Kontant- og bankbehandling > Purringer > Importer remburs og importinkasso.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
    * Kontroller rembursimporten.  
    * Valider: Forsendelsesstatus = fakturerte bankfasilitetsdetaljer  
4. Klikk Vis.
5. Klikk Skriv ut søknad.
6. Klikk OK.
    * Kontroller at remburssøknaden blir skrevet ut.  
7. Lukk siden.
8. Lukk siden.
9. Lukk siden.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Postere leverandørbetalingsjournalen for den opprettede innkjøpsfakturaen med remburs
1. Gå til Leverandører > Betalinger > Betalingsjournal.
2. Klikk Ny.
3. Angi eller velg en verdi i Navn-feltet.
4. Klikk koblingen i den valgte raden i listen.
5. Klikk Linjer.
6. Angi en dato i Dato-feltet.
7. Angi de ønskede verdiene i Konto-feltet.
8. Klikk Utlign transaksjoner.
9. Vis delen Totaler.
10. Velg et alternativ i feltet Vis.
    * Kontroller at feltet Bankdokumentnummer og Forsendelsesnummer er oppdatert.  
11. Merk av for Merk.
12. Klikk OK.
13. Klikk kategorien Betaling.
    * Kontroller at feltet Bankdokumentnummer og Forsendelsesnummer er oppdatert.  
14. Klikk Poster.
15. Lukk siden.
16. Lukk siden.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Kontrollere statusen for rembursimporten etter fakturaen er betalt
1. Gå til Kontant- og bankbehandling > Purringer > Importer remburs og importinkasso.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
    * Kontroller statusen for rembursimporten.   
4. Lukk siden.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Kontrollere bankfasilitetsgrensen og utnyttelsesrapporten
1. Gå til Kontant- og bankbehandling > Forespørsler og rapporter > Purringer eller garanti > Rapport om bankfasiliteter og bruk.
2. Utvid delen Poster som skal inkluderes.
3. Klikk Filter.
    * Definer Kriterier-feltet med den påkrevde bankkontoen.  
4. Angi eller velg en verdi i Kriterier-feltet.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk OK.
7. Klikk OK.
    * Kontroller rapporten som viser transaksjonene.  
    * Kontroller at rapporten angir transaksjonene med bankdokumentnummer, fasilitetsgrense, brukt beløp og fasilitetssaldobeløp.  
8. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]