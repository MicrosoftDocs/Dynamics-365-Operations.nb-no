---
title: Definere ER-modelltilordninger og velge datakilder for dem
description: De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan velge datakilder for en elektronisk rapporteringsdatamodell.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46dc13416aa094f33879c017c1a1815fc791409d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185112"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>Definere ER-modelltilordninger og velge datakilder for dem

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan velge datakilder for en elektronisk rapportering (ER)-datamodell. Datakildene bindes til individuelle komponenter for den valgte datamodellen under utformingen og fyller ut forretningsdata til denne datamodellen under kjøring. I dette eksemplet velger du datakilder for en eksisterende datamodell som er opprettet for eksempelfirmaet Litware, Inc. For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren Opprett en ny datamodell.


## <a name="open-the-electronic-reporting-configurations-tree"></a>Åpne konfigurasjonstreet for elektronisk rapportering
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Rapporteringskonfigurasjoner.

## <a name="insert-a-new-model-mapping"></a>Sette inn en ny modell-tilordning
1. Velg Betalinger (forenklet model) i treet.
2. Klikk Utforming.
3. Klikk Tilordne modell til datakilde.
4. Klikk Ny.
    * Dette vil opprette en ny post som tilordner datamodellen til datakilder. I dette eksemplet tilordner du datamodellen til datakilder for ønsket betalingstype: kredittoverføring.     Det er mulig å utforme flere tilordningen for en bestemt datamodell. Du kan for eksempel opprette en tilordning for ulike typer betalinger, som for direkte debitering eller kredittoverføringer. I dette eksemplet skal du opprette en tilordning for kredittoverføringer.  
5. Skriv inn Beskrivelse i feltet Tilordning for kredittoverføring.
    * Tilordning for kredittoverføring  
6. Skriv inn Betalingsmodell for tilordning for kredittoverføring i Beskrivelse-feltet.
    * Betalingsmodell for tilordning for kredittoverføring  
7. I Definisjon-feltet skriver du inn CustomerCreditTransferInitiation.
    * CustomerCreditTransferInitiation  
8. ResolveChanges definisjonen.
9. Klikk Lagre.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Definer nødvendige datakilder for den gjeldende modelltilordningen
1. Klikk Utforming.
2. Velg Dynamics 365 for Operations\Tabellposter i treet.
3. Klikk Legg til rot.
    * Angi denne datakilden hvis du vil åpne betalingstransaksjoner.  
4. Skriv inn Transaksjoner i Navn-feltet.
    * Transaksjoner  
5. Angi Transaksjoner i Etikett-feltet.
    * Transaksjoner  
6. Angi Finansjournallinjer i Hjelp-feltet.
    * Finansjournallinjer  
7. Velg Ja i feltet Be om spørring.
    * Velg Ja.  
8. Skriv inn 'LedgerJournalTrans' i Tabell-feltet.
    * LedgerJournalTrans  
9. Klikk OK.
    * Velg tabellen LedgerJournalTrans som datakilde for gjeldende datamodell.  
10. Velg Funksjoner\Beregnet felt i treet.
11. Klikk Legg til.
    * Klikk Legg til for å legge til et nytt beregnet felt.  
12. I Navn-feltet skriver du inn $EndToEndID.
    * $EndToEndID  
13. Klikk Rediger formel.
14. I treet velger du Streng\CONCATENATE.
15. Klikk Legg til funksjon.
16. Utvid Transaksjoner i treet.
17. I treet velger du Transaksjoner\Bilag.
18. Klikk Legg til datakilde.
19. I Formel-feltet skriver du inn 'CONCATENATE(Transactions.Voucher, "-", '.
    * Skriv inn [ , “-“, ] på slutten av formelen.  
20. I treet velger du Streng\TEXT.
21. Klikk Legg til funksjon.
22. Velg Transactions\Record-ID(RecId) i treet.
23. Klikk Legg til datakilde.
24. I Formel-feltet skriver du inn CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId)).
    * Skriv inn [))] på slutten av formelen.  
25. Klikk Lagre.
    * Kontroller at det ikke er oppdaget noen feil for formelen som er opprettet. Se kategorien FEIL under kontrollen for formelredigeringen.  
26. Lukk siden.
27. Klikk OK.
    * Legg til det beregnede feltet i denne datakilden.  
28. Klikk Legg til.
    * Klikk Legg til for å legge til et nytt beregnet felt.  
29. I Navn-feltet skriver du inn $Amount.
    * $Amount  
30. Klikk Rediger formel.
31. Utvid Transaksjoner i treet.
32. I treet velger du Transaksjoner\Debit(AmountCurDebit).
33. Klikk Legg til datakilde.
34. I Formel-feltet skriver du inn 'Transactions.AmountCurDebit - '.
    * Skriv inn [ - ] ved slutten av formelen.  
35. I treet velger du Transaksjoner\Credit(AmountCurCredit).
36. Klikk Legg til datakilde.
37. Klikk Lagre.
38. Lukk siden.
39. Klikk OK.
    * Det beregnede feltet $Amount legges til i den valgte datakilden for den gjeldende datamodellen.  
40. I treet velger du Transaksjoner\$Amount.
41. Utvid Transaksjoner i treet.
42. I treet viser eller skjuler du Transaksjoner\$Amount.
43. Vis eller skjul Transaksjoner i treet.
44. Velg Dynamics 365 for Operations\Tabellposter i treet.
45. Klikk Legg til rot.
    * Angi denne datakilden for å vise detaljer for firmaets bankkonto.  
46. Skriv inn BankAccount i Navn-feltet.
    * BankAccount  
47. Angi BankAccount i Etikett-feltet.
    * Bankkonto  
48. Angi Bankkonto i Hjelp-feltet.
    * Bankkonto  
49. Velg Ja i feltet Be om spørring.
    * Velg Ja.  
50. Skriv inn BankAccountTable i Tabell-feltet.
    * BankAccountTable  
51. Klikk OK.
    * Velg tabellen BankAccountTable som datakilde for gjeldende datamodellen.  
52. Klikk Legg til rot.
    * Angi denne datakilden for å vise detaljer for firmaets forutsetninger.  
53. I Navn-feltet skriver du inn Firma.
    * Firma  
54. Skriv inn en verdi i feltet Etikett.
    * Firmainformasjon  
55. Angi Firmainformasjon i Hjelp-feltet.
    * Firmainformasjon  
56. Velg Ja i feltet Be om spørring.
    * Velg Ja.  
57. Skriv inn CompanyInfo i Tabell-feltet.
    * CompanyInfo  
58. Klikk OK.
    * Velg tabellen CompanyInfo som en datakilde for gjeldende datamodellen.  
59. Velg Funksjoner\Beregnet felt i treet.
60. Klikk Legg til rot.
    * Sett inn et beregnet felt som en ny datakilde.  
61. Skriv inn ProcessingDateTime i Navn-feltet.
    * ProcessingDateTime  
62. I Etikett-feltet skriver du inn Dato og klokkeslett for behandling.
    * Dato og klokkeslett for behandling  
63. Klikk Rediger formel.
64. I treet velger du Dato/klokkeslett\SESSIONNOW.
65. Klikk Legg til funksjon.
66. Klikk Lagre.
67. Lukk siden.
68. Klikk OK.
    * Legg til det beregnede feltet ProcessingDateTime som en datakilde for gjeldende datamodellen.  
69. Klikk Lagre.
70. Lukk siden.
71. Lukk siden.
72. Lukk siden.

