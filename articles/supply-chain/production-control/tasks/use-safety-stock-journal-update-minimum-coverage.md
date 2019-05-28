---
title: Bruke sikkerhetslagerjournalen til å oppdatere minste dekning
description: Denne fremgangsmåten viser hvordan du beregner minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571433"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Bruke sikkerhetslagerjournalen til å oppdatere minste dekning

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du beregner minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene. Dette gjøres ved hjelp av sikkerhetslagerjournalen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven. Denne oppgaven er ment for produksjonsplanleggeren for å bidra til å opprettholde minste dekning.


## <a name="create-a-new-safety-stock-journal-name"></a>Opprette en nytt journalnavn for sikkerhetslager
1. Gå til Journalnavn for sikkerhetslager.
2. Klikk Ny.
3. Skriv inn Materiale i Navn-feltet.
4. Skriv inn Materiale i Beskrivelse-feltet.
5. Lukk siden.

## <a name="create-a-safety-stock-journal"></a>Opprette en sikkerhetslagerjournal
1. Gå til Beregning av sikkerhetslager.
2. Klikk Ny.
3. Angi eller velg en verdi i Navn-feltet.
    * Velg journalnavnet for sikkerhetslageret som du opprettet, for eksempel Materiale.  
4. Klikk Opprett linjer.
5. Angi en dato i Fra dato-feltet.
    * Sett datoen til 2015-01-02.  
6. Angi en dato i Til dato-feltet.
    * Sett datoen til 2015-12-30.  
7. Klikk OK.
    * Dette vil opprette linjer for dimensjonene som har lagertransaksjoner.  

## <a name="calculate-proposal"></a>Beregn forslag
1. Klikk Beregn forslag.
2. Velg alternativet Bruk gjennomsnittlig avgang i leveringstid.
3. Sett Multiplikasjonsfaktor til 10.
    * Multiplikasjonsfaktoren brukes til å justere forslaget. Siden demonstrasjonsdataene bare har noen få transaksjoner, må du angi faktoren for å få et realistisk forslag.  
4. Klikk OK.
    * Bla nedover for å finne M0002 og M0003. Vis kolonnen Beregnet minimumsantall.   

## <a name="update-minimum-quantity"></a>Oppdatere minimumsantall
1. Angi et tall i feltet Nytt minimumsantall.
    * Oppdater Nytt minimumsantall slik at det samsvarer med verdien i Beregnet minimumsantall. Hvis Beregnet minimumsantall er null, kan du angi ønsket fremtidig verdi. Du kan for eksempel angi Beregnet minimumsantall i dette feltet for M0002, som har lager 12.  
2. Finn og velg ønsket post i listen.
    * Du kan for eksempel velge M0002, som har lager 12.  
3. Angi et tall i feltet Nytt minimumsantall.
    * Oppdater Nytt minimumsantall slik at det samsvarer med verdien i Beregnet minimumsantall. Hvis Beregnet minimumsantall er null, kan du angi ønsket fremtidig verdi.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Postere det nye minimumsantallet og validere resultatet
1. Klikk Poster.
2. Klikk OK.
3. Klikk for å følge koblingen i Varenummer-feltet.
4. Klikk for å følge koblingen i Varenummer-feltet.
5. Klikk Plan i handlingsruten.
6. Klikk Varedekning.
    * Legg merke til at Minimumsantall er oppdatert med det nye minimumsantallet fra sikkerhetslagerjournalen.  

