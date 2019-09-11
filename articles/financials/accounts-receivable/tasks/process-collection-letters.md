---
title: Behandle purrebrev
description: Dette emnet viser hvordan du oppretter, skriver ut og posterer purringer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867661"
---
# <a name="process-collection-letters"></a>Behandle purrebrev

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du oppretter, skriver ut og posterer purringer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Angi et purreforløp på posteringsprofilen
1. Gå til **navigasjonsruten > Moduler > Kreditt og innkreving > Oppsett > Kundeposteringsprofiler**.
2. Klikk **Rediger**.
3. Velg et purreforløp fra rullegardinlisten. Hvis du ikke vil generere purringer for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt.  
4. Utvid fanen **Tabellrestriksjoner** for å endre måten purringer behandles på. Hvis dette feltet er satt til **Ja**, opprettes purringer for denne posteringsprofilen.  

## <a name="create-collection-letters"></a>Opprett purringer
1. Gå til **navigasjonsruten > Moduler > Kreditt og innkreving > Purring > Opprett purringer**.
2. Velg transaksjonstypene for purringene. Alle åpne transaksjoner for disse typene inkluderes i beregningen.  
3. Velg et alternativ for **Purring**-feltet.
4. I feltet **Purredato** angir du datoen for purringen.
5. Velg en posteringsprofil hvis du har endret **Bruk posteringsprofil fra** til **Velg**. Det finnes to alternativer for posteringsprofil:   

   - **Konto** – Bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota.   
   - **Velg** – Bruk posteringsprofilen som du velger i **Posteringsprofil**-feltet.  

6. Utvid delen **Poster som skal inkluderes**.
7. Velg **Filter**.
8. Angi en kunde-ID i **Kriterier**-feltet. Skriv for eksempel inn US-001.
9. Velg **OK**.
10. Velg **OK**.

## <a name="print-collection-letters"></a>Skrive ut purringer
1. Gå til **navigasjonsruten > Moduler > Kreditt og innkreving > Purring > Gjennomgå og behandle purrebrev**.
2. Velg **Opprettet** i **Status**-feltet.
3. Velg **Ikke skrevet ut** i feltet **Utskrevet**.
4. Velg **Skriv ut**.
5. Velg **Purrenota**.
6. I **Parametere**-delen angir du fristen for posteringer.
7. Utvid delen **Poster som skal inkluderes**, og angi detaljene for purrenotaen.
8. Velg **OK** for å skrive ut purringen.
9. Poster purringen.

    1. Velg **Poster**.
    1. Angi posteringsdatoen for purringen.
    1. Utvid delen **Poster som skal inkluderes**.
    1. Velg **OK**.
    1. Velg **Postert** i **Status**-feltet.
    1. Velg et alternativ i feltet **Utskrevet**.

## <a name="control-collection-letters-at-the-customer-level"></a>Kontrollere purringer på kundenivå
Du kan også definere purringer på kundenivået slik at purrekoden for hver transaksjon spores, men behandlingen av purringer baseres på ett purrenivå som lagres for kunden. Enkeltpurringen vil inneholde alle transaksjoner som er forfalt for kunden. Fordi respittdagene nå spores på kundenivået, sendes ikke den neste purringen før antallet respittdager har gått for neste purring i sekvensen, selv om transaksjoner forfaller etter den siste purringen ble sendt. Dette alternativet reduserer antall purringer som sendes per kunde. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Definere kunden for å kontrollere purringer på kundenivå
1.  Gå til **Navigasjonsrute > Moduler > Kreditt og innkreving > Oppsett > Kundeparametere**, og velg **Innkrevinger**-kategorien. 
2.  Endre verdien for **Opprett en purring per** til **Kunde**. 
3.  Gå til **navigasjonsruten > Moduler > Kreditt og innkreving > Purring > Gjennomgå og behandle purrebrev**. Bare én purring genereres for en kunde med alle forfalte transaksjoner.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Ignorere betalinger og kreditnotaer ved beregning av purrekoden
Hvis du tar med betalinger og kreditnotaer i transaksjonene som skal inkluderes i purringene, har du kanskje betalinger eller kreditnotaer som skal utløse en purring. Du kan styre hvordan betalinger og kreditnotaer kontrollerer purrekoden ved å endre verdien for parameteren **Ignorer betalinger og kreditnotaer for beregning av purrekode**. 

Når du skal ignorere betalinger og kreditnotaer ved beregning av purrekoden, gjør du følgende:

1. Gå til **Navigasjonsrute > Moduler > Kreditt og innkreving > Oppsett > Kundeparametere**, og klikk på **Innkrevinger**-kategorien. 
2. Ende verdien for **Ignorer betalinger og kreditnotaer for beregning av purrekode** til **Ja**.
