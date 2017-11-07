--- 
title: Tilordne en datamodell til utvalgte datakilder for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan tilordne en elektronisk rapportering (ER)-datamodell til valgte Dynamics 365 for Finance and Operations, Enterprise Edition-datakilder."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96974d7c1597db4ac31168be40cecbc7e12d6edd
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a>Tilordne en datamodell til utvalgte datakilder for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan tilordne en elektronisk rapportering (ER)-datamodell til valgte Dynamics 365 for Finance and Operations, Enterprise Edition-datakilder. Denne modelltilordningen brukes senere som datakilde i en formatkonfigurasjon som skal brukes til å administrere elektroniske betalingsdokumenter. I dette eksemplet tilordner du en datamodell for eksempelfirmaet Litware, Inc. til datakilder. Når du skal fullføre disse trinnene, må du først fullføre trinnene i fremgangsmåten Velg datakildene for tilordning av modell.


## <a name="open-er-configurations-tree"></a>Åpne ER-konfigurasjonstreet
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Konfigurasjoner.

## <a name="select-created-model-mapping"></a>Velg opprettet modelltilordning
1. Velg Betalinger (forenklet model) i treet.
    * Kontroller at modellkonfigurasjonen Betalinger (forenklet modell) er opprettet på forhånd. Ellers stopper du nå og går tilbake etter at du har fullført oppgaveveiledningen Opprette en ny konfigurasjon med datamodellen for det valgte domenet.  
2. Velg Modellutforming.
3. Klikk Tilordne modell til datakilde.
4. Velg posten Tilordning for kredittoverføring.
    * Tilordning for kredittoverføring  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Bind opprettede datakilder til datamodellelementer
1. Klikk Utforming.
2. I konsolltreet velger du Dato og klokkeslett for behandling(ProcessingDateTime).
3. I konsolltreet velger du Behandlingsdato(ProcessingDateTime).
4. Klikk Bind.
5. Velg Betalingsmeldingsidentifikasjon(MessageIdentification) i treet.
6. Utvid Transaksjoner i treet.
7. Velg Transaksjoner\Journalpartinummer(JournalNum) i treet.
8. Klikk Bind.
9. Velg Betalinger i treet.
10. Velg Transaksjoner i treet.
11. Klikk Bind.
12. Utvid Betalinger= Transaksjoner i treet.
13. Utvid Betalinger= Transaksjoner\Kreditor i treet.
14. Utvid Betalinger= Transaksjoner\Kreditor\Konto i treet.
15. I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\Valutakode(Valuta).
16. I treet utvider du Transaksjoner\vendBankAccountInTransactionCompany().
17. I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Valuta(CurrencyCode).
18. Klikk Bind.
19. I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\IBAN-kode(IBAN).
20. I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\IBAN(BankIBAN).
21. Klikk Bind.
22. I treet velger du Betalinger = Transaksjoner\Kreditor\Konto\Nummer.
23. I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Bankkontonummer(AccountNum).
24. Klikk Bind.
25. Utvid Betalinger= Transaksjoner\Kreditor\Agent i treet.
26. I treet velger du Betalinger = Transaksjoner\Kreditor\Agent\Navn.
27. I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Navn.
28. Klikk Bind.
29. I treet velger du Betalinger= Transaksjoner\Kreditor\Agent\Rutingsnummer(RoutingNumber).
30. I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\Rutingsnummer(RegistrationNum).
31. Klikk Bind.
32. I treet velger du Betalinger = Transaksjoner\Kreditor\Agent\SWIFT-kode(SWIFT).
33. I treet velger du Transaksjoner\vendBankAccountInTransactionCompany()\SWIFT-kode(SWIFTNo).
34. Klikk Bind.
35. I treet velger du Betalinger = Transaksjoner\Kreditor\Navn.
36. Utvid Transaksjoner\findVendTable() i treet.
37. I treet velger du Transaksjoner\findVendTable()\name().
38. Klikk Bind.
39. I treet velger du Betalinger = Transaksjoner\Valutakode(Valuta).
40. Utvid Transaksjoner\>Relasjoner i treet.
41. I treet utvider du Transaksjoner\>Relasjoner\Valutatabell(Valuta).
42. I treet velger du Transaksjoner\>Relasjoner\Valutatabell(Valuta)\Valutakode(CurrencyCodeISO).
43. Klikk Bind.
44. Utvid Betalinger= Transaksjoner\Debitor i treet.
45. Utvid Betalinger= Transaksjoner\Debitor\Konto i treet.
46. I treet velger du Betalinger = Transaksjoner\Debitor\Konto\Valutakode(Valuta).
47. Velg Bankkonto(BankAccount) i treet.
48. Utvid Bankkonto(BankAccount) i treet.
49. I treet velger du Bankkonto(BankAccount)\Valuta(CurrencyCode).
50. Klikk Bind.
51. I treet velger du Bankkonto(BankAccount)\IBAN.
52. I treet velger du Betalinger = Transaksjoner\Debitor\Konto\IBAN-kode(IBAN).
53. Klikk Bind.
54. I treet velger du Betalinger = Transaksjoner\Debitor\Konto\Nummer.
55. I treet velger du Bankkonto(BankAccount)\Bankkontonummer(AccountNum).
56. Klikk Bind.
57. Utvid Betalinger= Transaksjoner\Debitor\Agent i treet.
58. I treet velger du Betalinger = Transaksjoner\Debitor\Agent\Navn.
59. Velg Bankkonto(BankAccount)\Navn i treet.
60. Klikk Bind.
61. I treet velger du Betalinger= Transaksjoner\Debitor\Agent\Rutingsnummer(RoutingNumber).
62. I treet velger du Bankkonto(BankAccount)\Rutingsnummer(RegistrationNum).
63. Klikk Bind.
64. I treet velger du Betalinger = Transaksjoner\Debitor\Agent\SWIFT-kode(SWIFT).
65. I treet velger du Bankkonto(BankAccount)\SWIFT-kode(SWIFTNo).
66. Klikk Bind.
67. I treet velger du Betalinger = Transaksjoner\Debitor\Navn.
68. Velg Firmainformasjon (Firma) i treet.
69. Utvid Firmainformasjon (Firma) i treet.
70. Velg Firmainformasjon (Firma)\Navn i treet.
71. Klikk Bind.
72. I treet velger du Betalinger = Transaksjoner\Beskrivelse.
73. I treet velger du Transaksjoner\Beskrivelse(Txt).
74. Klikk Bind.
75. I treet velger du Betalinger = Transaksjoner\Ende-til-ende-identifikasjonskode(End2EndID).
76. I treet velger du Transaksjoner\$EndToEndID.
77. Klikk Bind.
78. I treet velger du Betalinger = Transaksjoner\Instruert beløp(InstructedAmount).
79. I treet velger du Transaksjoner\$Amount.
80. Klikk Bind.
81. I treet velger du Betalinger = Transaksjoner\Transaksjonsdato(TransactionDate).
82. I treet velger du Transaksjoner\Dato(TransDate).
83. Klikk Bind.

## <a name="validate-created-mapping"></a>Valider opprettet tilordning
1. Klikk Valider.
    * Valider den nye tilordningen for å sikre at alle bindinger er i orden.  
2. Klikk pilen for å vise eller skjule delen Feilliste.
3. Klikk Lagre.
4. Lukk siden.
5. Lukk siden.
6. Lukk siden.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Endre statusen til gjeldende versjon av modellkonfigurasjon
1. Klikk Endre status.
    * Endre statusen for utformet modellkonfigurasjon – fra Utkast til Fullført for å gjøre den tilgjengelig for utforming av betalingsformat.  
2. Klikk Fullført.
    * Velg Fullført.  
3. Skriv inn en verdi i feltet Beskrivelse.
    * For eksempel versjon 1.  
4. Klikk OK.
5. Velg den fullførte versjonen av den gjeldende konfigurasjonen.
    * Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.  


