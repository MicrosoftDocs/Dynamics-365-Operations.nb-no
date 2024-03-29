---
title: Postering av elektroniske salg og betalinger
description: Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.
author: jashanno
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
ms.openlocfilehash: 0db3414a41a27b5c383eddd4c3e7650fb828b422
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285693"
---
# <a name="posting-of-online-sales-and-payments"></a>Postering av elektroniske salg og betalinger

[!include [banner](../includes/banner.md)]

Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.

Postering av elektroniske salg og betalinger er en prosess i to trinn.

- Henter de elektroniske handelstransaksjonsdataene i HK.
- Synkroniserer ordrer for å opprette salgsordrer på hovedkontoret.

Å hente elektroniske transaksjonsdata kan gjøres manuelt ved å kjøre P-jobben eller ved å opprette en gjentakende satsvis jobb.

### <a name="manually-running-the-p-job"></a>Kjøre P-jobben manuelt

1. Gå til Alle arbeidsområder > IT for Retail og Commerce.
2. Klikk på Distribusjonsplan.
3. Velg P-0001.
4. Juster kanaldatabasegrupper hvis det er nødvendig.
5. Klikk Kjør nå.
6. Klikk Ja.

### <a name="scheduling-a-recurring-p-job"></a>Planlegge en regelmessig P-jobb

1. Gå til Alle arbeidsområder > IT for Retail og Commerce.
2. Klikk på Distribusjonsplan.
3. Velg P-0001.
4. Klikk på Opprett satsvis jobb.
5. Klikk på Kjør i bakgrunnen.
5. Aktiver satsvis behandling.
6. Klikk på Regelmessighet.
7. Velg Ingen sluttdato.
8. I Antall-feltet angir du intervallet mellom kjøringer i minutter. Vanligvis vil dette være 5-10.
9. Klikk OK.
10. Klikk OK.

Ordrer kan synkroniseres enten ved å kjøre Synkroniser ordrer-jobben manuelt, eller ved å opprette en gjentakende satsvis jobb.

### <a name="manually-running-order-synchronization"></a>Kjøre ordresynkronisering manuelt 

Følg denne fremgangsmåten for å kjøre jobben Synkroniser ordrer manuelt én gang.

1. Gå til Alle arbeidsområder > Finans for butikk.
2. Klikk Synkroniser ordrer.
3. Velg Butikker etter område i Organisasjonshierarki-feltet.
    * Velg en bestemt nettbutikk eller velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.  
    * Klikk pilen for å legge til valget.  
4. Klikk fanen Kjør i bakgrunnen.
5. Deaktiver satsvis behandling.
6. Klikk Regelmessighet.
7. Velg Avslutt etter-alternativet.
8. Angi 1 i feltet Avslutt etter.
9. Klikk OK.
10. Klikk OK.

### <a name="scheduling-recurring-order-synchronization"></a>Planlegge regelmessig ordresynkronisering

Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner. Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.

1. Gå til Alle arbeidsområder > Finans for butikk.
2. Klikk Synkroniser ordrer.
3. Velg Butikker etter område i Organisasjonshierarki-feltet.
    * Velg en bestemt nettbutikk eller velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.  
    * Klikk pilen for å legge til valget.  
4. Klikk fanen Kjør i bakgrunnen.
5. Aktiver satsvis behandling.
6. Klikk Regelmessighet.
7. Velg Ingen sluttdato.
8. I Antall-feltet angir du intervallet mellom kjøringer i minutter. Vanligvis vil dette være 2-20.
9. Klikk OK.
10. Klikk OK.

## <a name="data-entities-involved-in-the-process"></a>Dataenheter som er involvert i prosessen

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
