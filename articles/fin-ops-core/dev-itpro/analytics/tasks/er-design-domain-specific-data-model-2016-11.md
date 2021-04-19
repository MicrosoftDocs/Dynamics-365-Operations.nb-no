---
title: ER Utforme domenespesifikk datamodell
description: Dette emnet beskriver hvordan du oppretter en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en datamodell for elektroniske betalingsdokumenter.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351c5a6624f7ee912c507a9f74324f4c8f61166b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755040"
---
# <a name="er-design-domain-specific-data-model"></a>ER Utforme domenespesifikk datamodell

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny konfigurasjon for elektronisk rapportering (ER) som inneholder en datamodell for elektroniske betalingsdokumenter. Denne datamodellen brukes senere som en datakilde når du oppretter formatet for betalingsdokumentene.

I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom alle firmaer. For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.

    Velg konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. Hvis du ikke ser denne konfigurasjonsleverandøren, må du først fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".  
    
2. Klikk på Rapporteringskonfigurasjoner.

    Du vil opprette en konfigurasjon som inneholder en datamodell for elektroniske betalingsdokumenter. Denne datamodellen brukes senere som en datakilde når du oppretter formatet for betalingsdokumentene.  

## <a name="create-a-new-data-model-configuration"></a>Opprett en ny datamodellkonfigurasjon
1. Klikk på Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I Navn-feltet skriver du inn Betalinger (forenklet modell).
3. Skriv inn Konfigurasjon for betalingsmodell i Beskrivelse-feltet.

    Den aktive konfigurasjonsleverandøren angis automatisk her. Denne leverandøren vil kunne vedlikeholde denne konfigurasjonen. Andre leverandører kan bruke denne konfigurasjonen, men kan ikke vedlikeholde den.  

4. Klikk på Opprett konfigurasjon for å fullføre oppgaven for konfigurasjonsopprettelse

## <a name="create-a-data-model"></a>Opprett en datamodell
Du oppretter en ny datamodell for den valgte konfigurasjonen. Denne konfigurasjonsversjonen får statusen Utkast.  
1. Klikk på Utforming.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Definere strukturen for en part som deltar i en betalingsprosessen
1. Klikk på Ny for å åpne nedtrekksdialogen.
2. I Navn-feltet skriver du inn Part.
3. Klikk på Legg til.
4. Klikk på Ny for å åpne nedtrekksdialogen.
5. I Navn-feltet skriver du inn Navn.
6. Velg Streng i Varetype-feltet.
7. Klikk på Legg til.
8. I Søk-feltet skriver du inn Part.
9. Klikk på Søk etter forrige.

## <a name="define-the-bank-structure-for-this-model"></a>Definer bankstrukturen for denne modellen
1. Klikk på Ny for å åpne nedtrekksdialogen.
2. Skriv inn Agent i Navn-feltet.
3. Velg Post i Varetype-feltet.
4. Klikk på Legg til.
5. Angi Finansinstitusjon (for eksempel en bank) som betjener en konto for parten (debitoren/kreditoren), i Beskrivelse-feltet.

    Finansinstitusjon (for eksempel en bank) som betjener en konto for parten (debitoren/kreditoren).  

6. Klikk på Ny for å åpne nedtrekksdialogen.
7. I Navn-feltet skriver du inn Navn. 
8. Velg Streng i Varetype-feltet.
9. Klikk på Legg til.
10. Klikk på Ny for å åpne nedtrekksdialogen.
11. I Navn-feltet skriver du inn SWIFT.
12. Klikk på Legg til.
13. Skriv inn Bankidentifikasjonskode i Beskrivelse-feltet. 
14. Klikk på Ny for å åpne nedtrekksdialogen.
15. Skriv inn RoutingNumber i feltet Navn.
16. Klikk på Legg til.
17. Skriv inn Registreringsnummer i Beskrivelse-feltet.
18. Klikk på Søk etter forrige.

## <a name="define-the-bank-account-structure-for-this-model"></a>Definer bankkontostrukturen for denne modellen
1. Klikk på Ny for å åpne nedtrekksdialogen.
2. I Navn-feltet skriver du inn Konto. 
3. Velg Post i Varetype-feltet.
4. Klikk på Legg til.
5. I Beskrivelse-feltet skriver du inn Identifikasjon av en konto for en part i en finansinstitusjon (for eksempel en bank).

    Identifikasjon av en konto for en part i en finansinstitusjon (for eksempel en bank).  

6. Klikk på Ny for å åpne nedtrekksdialogen.
7. I Navn-feltet skriver du inn Valuta. 
8. Velg Streng i Varetype-feltet.
9. Klikk på Legg til.
10. Skriv inn Valutakode i Beskrivelse-feltet.
11. Klikk på Ny for å åpne nedtrekksdialogen.
12. I Navn-feltet skriver du inn Nummer. 
13. Klikk på Legg til.
14. Klikk på Ny for å åpne nedtrekksdialogen.
15. I Navn-feltet skriver du IBAN. 
16. Klikk på Legg til.
17. Angi Internasjonalt bankkontonummer i Beskrivelse-feltet.

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Definere betalingsmeldingsstrukturen for betalingstype for kredittoverføring
1. Klikk på Ny for å åpne nedtrekksdialogen.
2. I feltet Ny node som en for angir du Modellrot.
3. I Navn-feltet skriver du inn CustomerCreditTransferInitiation.
4. Klikk på Legg til.
5. I Søk-feltet skriver du inn CustomerCreditTransferInitiation. 
6. Klikk på Søk etter forrige.
7. Klikk på Ny for å åpne nedtrekksdialogen.
8. Skriv inn MessageIdentification i Navn-feltet. 
9. Klikk på Legg til.
10. I Beskrivelse-feltet angir du Punkt-til-punkt-referansen, som tilordnet av instruksjonsparten (og sendt til den neste parten) for å identifisere en melding.

    Punkt-til-punkt-referansen, som tilordnet av instruksjonsparten (og sendt til den neste parten) for å identifisere en melding.  

11. Klikk på Ny for å åpne nedtrekksdialogen.
12. Skriv inn ProcessingDateTime i Navn-feltet.
13. Velg DateTime i Varetype-feltet.
14. Klikk på Legg til.
15. I Beskrivelse-feltet angir du Datoen og klokkeslettet da betalingsmeldingen ble opprettet. 
16. Klikk på Ny for å åpne nedtrekksdialogen.

    Definer betalingstransaksjonsstrukturen for denne modellen.  

17. Skriv inn Betalinger i Navn-feltet.
18. Velg Postliste i Varetype-feltet.
19. Klikk på Legg til.
20. I Beskrivelse-feltet angir du Betalingslinjer for gjeldende melding.
21. Klikk på Ny for å åpne nedtrekksdialogen.
22. I Navn-feltet skriver du inn Kreditor. 
23. Velg Post i Varetype-feltet.
24. Klikk på Legg til.
25. I Beskrivelse-feltet angir du Parten som et pengebeløp forfaller for. 
26. Klikk på Bytt varereferanse.
27. I Søk-feltet skriver du inn Part.
28. Klikk på Søk etter neste.
29. Klikk på OK.
30. Skriv inn Betalinger i Søk-feltet.
31. Klikk på Søk etter neste.
32. Klikk på Ny for å åpne nedtrekksdialogen.
33. I Navn-feltet skriver du inn Debitor. 
34. Klikk på Legg til.
35. I Beskrivelse-feltet angir du Part som skylder et pengebeløp til den (ultimate) kreditoren.
36. Klikk på Bytt varereferanse.
37. I Søk-feltet skriver du inn Part.
38. Klikk på Søk etter neste.
39. Klikk på OK.
40. Klikk på Søk etter neste.
41. Klikk på Ny for å åpne nedtrekksdialogen.
42. Skriv inn Beskrivelse i Navn-feltet.
43. Velg Streng i Varetype-feltet.
44. Klikk på Legg til.
45. Klikk på Ny for å åpne nedtrekksdialogen.
46. I Navn-feltet skriver du inn Valuta.
47. Klikk på Legg til.
48. Skriv inn Valutakode i Beskrivelse-feltet.
49. Klikk på Ny for å åpne nedtrekksdialogen.
50. Skriv inn TransactionDate i Navn-feltet. 
51. Velg Dato i Varetype-feltet.
52. Klikk på Legg til.
53. Angi Transaksjonsdato i Beskrivelse-feltet. 
54. Klikk på Ny for å åpne nedtrekksdialogen.
55. Skriv inn InstructedAmount i Navn-feltet.  
56. Velg Faktisk i Varetype-feltet.
57. Klikk på Legg til.
58. I Beskrivelse-feltet angir du Beløpet som skal flyttes mellom debitor og kreditor før fradrag av tillegg. Beløpet bør uttrykkes i valutaen som er bestilt av den første parten.

    Beløpet som skal flyttes mellom debitor og kreditor før fradrag av tillegg. Beløpet bør uttrykkes i valutaen som er bestilt av den første parten.  

59. Klikk på Ny for å åpne nedtrekksdialogen.
60. I Navn-feltet skriver du inn End2EndID. 
61. Velg Streng i Varetype-feltet.
62. Klikk på Legg til.
63. I Beskrivelse-feltet skriver du Den unike identifikasjonen som er tilordnet av initialiseringsparten. Denne identifikasjonen sendes, forblir uendret, gjennom hele kjeden ende-til-ende. 
64. Skriv inn PaymentModel i feltet Navn.

    Navnet på PaymentModel justerer med forhåndsdefinerte grensesnitt for betalingsskjemaer.  

65. Klikk på Lagre.
66. Lukk siden.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]