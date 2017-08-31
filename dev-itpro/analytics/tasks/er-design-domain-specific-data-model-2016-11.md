--- 
title: Utforme en domenespesifikk datamodell for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en datamodell for elektroniske betalingsdokumenter."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bf727b63ed86e7cc26d4fca630d97af88abb1804
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a>Utforme en domenespesifikk datamodell for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en datamodell for elektroniske betalingsdokumenter. Denne datamodellen brukes senere som en datakilde når du oppretter formatet for betalingsdokumentene.



I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom alle firmaer. For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Velg konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".  
2. Klikk Rapporteringskonfigurasjoner.
    * Du vil opprette en konfigurasjon som inneholder en datamodell for elektroniske betalingsdokumenter. Denne datamodellen brukes senere som en datakilde når du oppretter formatet for betalingsdokumentene.  

## <a name="create-a-new-data-model-configuration"></a>Opprett en ny datamodellkonfigurasjon
1. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I Navn-feltet skriver du inn Betalinger (forenklet modell).
    * Betalinger (forenklet modell)  
3. Skriv inn Konfigurasjon for betalingsmodell i Beskrivelse-feltet.
    * Konfigurasjon for betalingsmodell  
    * Den aktive konfigurasjonsleverandøren angis automatisk her. Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen. Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.  
4. Klikk Opprett konfigurasjon for å fullføre oppgaven for konfigurasjonsopprettelse

## <a name="create-a-data-model"></a>Opprett en datamodell
    * Du oppretter en ny datamodell for den valgte konfigurasjonen. Denne konfigurasjonsversjonen får statusen Utkast.  
1. Klikk Utforming.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Definere strukturen for en part som deltar i en betalingsprosessen
1. Klikk Ny for å åpne nedtrekksdialogen.
2. I Navn-feltet skriver du inn Part.
    * Part  
3. Klikk Legg til.
4. Klikk Ny for å åpne nedtrekksdialogen.
5. I Navn-feltet skriver du inn Navn.
    * Navn  
6. Velg Streng i Varetype-feltet.
7. Klikk Legg til.
8. I Søk-feltet skriver du inn Part.
    * Part  
9. Klikk Søk etter forrige.

## <a name="define-the-bank-structure-for-this-model"></a>Definer bankstrukturen for denne modellen
1. Klikk Ny for å åpne nedtrekksdialogen.
2. Skriv inn Agent i Navn-feltet.
    * Agent  
3. Velg Post i Varetype-feltet.
4. Klikk Legg til.
5. Angi Finansinstitusjon (for eksempel en bank) som betjener en konto for parten (debitoren/kreditoren), i Beskrivelse-feltet.
    * Finansinstitusjon (for eksempel en bank) som betjener en konto for parten (debitoren/kreditoren).  
6. Klikk Ny for å åpne nedtrekksdialogen.
7. I Navn-feltet skriver du inn Navn.
    * Navn  
8. Velg Streng i Varetype-feltet.
9. Klikk Legg til.
10. Klikk Ny for å åpne nedtrekksdialogen.
11. I Navn-feltet skriver du inn SWIFT.
    * SWIFT  
12. Klikk Legg til.
13. Skriv inn Bankidentifikasjonskode i Beskrivelse-feltet.
    * Bankens identifikasjonskode  
14. Klikk Ny for å åpne nedtrekksdialogen.
15. Skriv inn RoutingNumber i feltet Navn.
    * RoutingNumber  
16. Klikk Legg til.
17. Skriv inn Registreringsnummer i Beskrivelse-feltet.
    * Organisasjonsnummer  
18. Klikk Søk etter forrige.

## <a name="define-the-bank-account-structure-for-this-model"></a>Definer bankkontostrukturen for denne modellen
1. Klikk Ny for å åpne nedtrekksdialogen.
2. I Navn-feltet skriver du inn Konto.
    * Konto  
3. Velg Post i Varetype-feltet.
4. Klikk Legg til.
5. I Beskrivelse-feltet skriver du inn Identifikasjon av en konto for en part i en finansinstitusjon (for eksempel en bank).
    * Identifikasjon av en konto for en part i en finansinstitusjon (for eksempel en bank).  
6. Klikk Ny for å åpne nedtrekksdialogen.
7. I Navn-feltet skriver du inn Valuta.
    * Valuta  
8. Velg Streng i Varetype-feltet.
9. Klikk Legg til.
10. Skriv inn Valutakode i Beskrivelse-feltet.
    * Valutakode  
11. Klikk Ny for å åpne nedtrekksdialogen.
12. I Navn-feltet skriver du inn Nummer.
    * Tall  
13. Klikk Legg til.
14. Klikk Ny for å åpne nedtrekksdialogen.
15. I Navn-feltet skriver du IBAN.
    * IBAN  
16. Klikk Legg til.
17. Angi Internasjonalt bankkontonummer i Beskrivelse-feltet.
    * Internasjonalt bankkontonummer  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Definere betalingsmeldingsstrukturen for betalingstype for kredittoverføring
1. Klikk Ny for å åpne nedtrekksdialogen.
2. I feltet Ny node som en for angir du Modellrot.
3. I Navn-feltet skriver du inn CustomerCreditTransferInitiation.
    * CustomerCreditTransferInitiation  
4. Klikk Legg til.
5. I Søk-feltet skriver du inn CustomerCreditTransferInitiation.
    * CustomerCreditTransferInitiation  
6. Klikk Søk etter forrige.
7. Klikk Ny for å åpne nedtrekksdialogen.
8. Skriv inn MessageIdentification i Navn-feltet.
    * MessageIdentification  
9. Klikk Legg til.
10. I Beskrivelse-feltet angir du Punkt-til-punkt-referansen, som tilordnet av instruksjonsparten (og sendt til den neste parten) for å identifisere en melding.
    * Punkt-til-punkt-referansen, som tilordnet av instruksjonsparten (og sendt til den neste parten) for å identifisere en melding.  
11. Klikk Ny for å åpne nedtrekksdialogen.
12. Skriv inn ProcessingDateTime i Navn-feltet.
    * ProcessingDateTime  
13. Velg DateTime i Varetype-feltet.
14. Klikk Legg til.
15. I Beskrivelse-feltet angir du Datoen og klokkeslettet da betalingsmeldingen ble opprettet.
    * Datoen og klokkeslettet da betalingsmeldingen ble opprettet.  
16. Klikk Ny for å åpne nedtrekksdialogen.
    * Definer betalingstransaksjonsstrukturen for denne modellen.  
17. Skriv inn Betalinger i Navn-feltet.
    * Betalinger  
18. Velg Postliste i Varetype-feltet.
19. Klikk Legg til.
20. I Beskrivelse-feltet angir du Betalingslinjer for gjeldende melding.
    * Betalingslinjer for gjeldende melding  
21. Klikk Ny for å åpne nedtrekksdialogen.
22. I Navn-feltet skriver du inn Kreditor.
    * Kreditor  
23. Velg Post i Varetype-feltet.
24. Klikk Legg til.
25. I Beskrivelse-feltet angir du Parten som et pengebeløp forfaller for.
    * Parten som et pengebeløp forfaller for.  
26. Klikk Bytt varereferanse.
27. I Søk-feltet skriver du inn Part.
    * Part  
28. Klikk Søk etter neste.
29. Klikk OK.
30. Skriv inn Betalinger i Søk-feltet.
    * Betalinger  
31. Klikk Søk etter neste.
32. Klikk Ny for å åpne nedtrekksdialogen.
33. I Navn-feltet skriver du inn Debitor.
    * Debitor  
34. Klikk Legg til.
35. I Beskrivelse-feltet angir du Part som skylder et pengebeløp til den (ultimate) kreditoren.
    * Part som skylder et pengebeløp til den (ultimate) kreditoren.  
36. Klikk Bytt varereferanse.
37. I Søk-feltet skriver du inn Part.
    * Part  
38. Klikk Søk etter neste.
39. Klikk OK.
40. Klikk Søk etter neste.
41. Klikk Ny for å åpne nedtrekksdialogen.
42. Skriv inn Beskrivelse i Navn-feltet.
    * beskrivelse  
43. Velg Streng i Varetype-feltet.
44. Klikk Legg til.
45. Klikk Ny for å åpne nedtrekksdialogen.
46. I Navn-feltet skriver du inn Valuta.
    * Valuta  
47. Klikk Legg til.
48. Skriv inn Valutakode i Beskrivelse-feltet.
    * Valutakode  
49. Klikk Ny for å åpne nedtrekksdialogen.
50. Skriv inn TransactionDate i Navn-feltet.
    * TransactionDate  
51. Velg Dato i Varetype-feltet.
52. Klikk Legg til.
53. Angi Transaksjonsdato i Beskrivelse-feltet.
    * Transaksjonsdato  
54. Klikk Ny for å åpne nedtrekksdialogen.
55. Skriv inn InstructedAmount i Navn-feltet.
    * InstructedAmount  
56. Velg Faktisk i Varetype-feltet.
57. Klikk Legg til.
58. I Beskrivelse-feltet angir du Beløpet som skal flyttes mellom debitor og kreditor før fradrag av tillegg. Beløpet bør uttrykkes i valutaen som er bestilt av den første parten.
    * Beløpet som skal flyttes mellom debitor og kreditor før fradrag av tillegg. Beløpet bør uttrykkes i valutaen som er bestilt av den første parten.  
59. Klikk Ny for å åpne nedtrekksdialogen.
60. I Navn-feltet skriver du inn End2EndID.
    * End2EndID  
61. Velg Streng i Varetype-feltet.
62. Klikk Legg til.
63. I Beskrivelse-feltet skriver du Den unike identifikasjonen som er tilordnet av initialiseringsparten. Denne identifikasjonen sendes, forblir uendret, gjennom hele kjeden ende-til-ende.
    * Den unike identifikasjonen som er tilordnet av initialiseringsparten. Denne identifikasjonen sendes, forblir uendret, gjennom hele kjeden ende-til-ende.  
64. Skriv inn PaymentModel i feltet Navn.
    * Navnet på PaymentModel justerer med forhåndsdefinerte grensesnitt for betalingsskjemaer.  
65. Klikk Lagre.
66. Lukk siden.


