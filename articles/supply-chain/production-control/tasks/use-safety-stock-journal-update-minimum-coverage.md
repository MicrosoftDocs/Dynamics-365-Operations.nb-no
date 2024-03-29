---
title: Bruke sikkerhetslagerjournalen til å oppdatere minste dekning
description: Denne fremgangsmåten viser hvordan du beregner minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene.
author: johanhoffmann
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ae2209fc2412a4a67b46d6eb82ecb70aafc0159
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573615"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Bruke sikkerhetslagerjournalen til å oppdatere minste dekning

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du beregner minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene. Dette gjøres ved hjelp av sikkerhetslagerjournalen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne oppgaven er ment for produksjonsplanleggeren for å bidra til å opprettholde minste dekning.


## <a name="create-a-new-safety-stock-journal-name"></a>Opprette en nytt journalnavn for sikkerhetslager
1. I **navigasjonsruten** går du til **Hovedplanlegging > Oppsett > Journalnavn for sikkerhetslager**.
2. Klikk på **Ny**.
3. Skriv inn Materiale i **Navn**-feltet.
4. Skriv inn Materiale i **Beskrivelse**-feltet.
5. Lukk siden.

## <a name="create-a-safety-stock-journal"></a>Opprette en sikkerhetslagerjournal
1. I **navigasjonsruten** går du til **Hovedplanlegging > Hovedplanlegging > Kjør > Beregning av sikkerhetslager**.
2. Klikk på **Ny**.
3. Angi eller velg en verdi i **Navn**-feltet. Velg journalnavnet for sikkerhetslageret som du opprettet, for eksempel Materiale.  
4. Klikk på **Opprett linjer**.
5. Angi en dato i **Fra dato**-feltet.  
6. Angi en dato i **Til dato**-feltet.
7. Klikk på **OK**. Dette vil opprette linjer for dimensjonene som har lagertransaksjoner.  

## <a name="calculate-proposal"></a>Beregn forslag
1. Klikk på **Beregn forslag.**
2. Velg alternativet **Bruk gjennomsnittlig avgang i leveringstid**.
3. Sett **Multiplikasjonsfaktor** til 10. Multiplikasjonsfaktoren brukes til å justere forslaget. Siden demonstrasjonsdataene bare har noen få transaksjoner, må du angi faktoren for å få et realistisk forslag.  
4. Klikk på **OK**. Bla nedover for å finne M0002 og M0003. Vis kolonnen **Beregnet minimumsantall**.   

## <a name="update-minimum-quantity"></a>Oppdatere minimumsantall
1. Angi et tall i feltet **Nytt minimumsantall**. Oppdater Nytt minimumsantall slik at det samsvarer med verdien i Beregnet minimumsantall. Hvis Beregnet minimumsantall er null, kan du angi ønsket fremtidig verdi. Du kan for eksempel angi Beregnet minimumsantall i dette feltet for M0002, som har lager 12.  
2. Finn og velg ønsket post i listen. Du kan for eksempel velge M0002, som har lager 12.  
3. Angi et tall i feltet **Nytt minimumsantall**. Oppdater Nytt minimumsantall slik at det samsvarer med verdien i Beregnet minimumsantall. Hvis Beregnet minimumsantall er null, kan du angi ønsket fremtidig verdi.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Postere det nye minimumsantallet og validere resultatet
1. Klikk på **Poster**.
2. Klikk på **OK**.
3. Klikk på for å følge koblingen i **Varenummer**-feltet.
4. Klikk på for å følge koblingen i **Varenummer**-feltet.
5. Klikk på Plan i **handlingsruten**.
6. Klikk på **Varedekning**. Legg merke til at **Minimumsantall** er oppdatert med det nye minimumsantallet fra sikkerhetslagerjournalen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]