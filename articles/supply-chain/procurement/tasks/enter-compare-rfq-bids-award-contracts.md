--- 
title: "Angi og sammenligne tilbudsforespørsler og inngå kontrakter"
description: "Denne fremgangsmåten viser hvordan du registrerer svar på en tilbudsforespørsel, poengsum og sammenligner bud, og deretter gir budet til én av leverandørene."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Angi og sammenligne tilbudsforespørsler og inngå kontrakter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du registrerer svar på en tilbudsforespørsel, poengsum og sammenligner bud, og deretter gir budet til én av leverandørene. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Før du begynner, må du ha en tilbudsforespørsel med to linjer som er sendt til minst to leverandører. Du kan kjøre prosedyren "Opprett en tilbudsforespørsel" for å opprette dette. Du må ha definert poengsumkriterier før du kan kjøre denne prosedyren.


## <a name="enter-a-reply-from-a-vendor"></a>Angi et svar fra en leverandør
1. Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.
2. Velg en tilbudsforespørsel som har statusen Sendt, og klikk koblingen for saksnummeret for tilbudsforespørsel.
    * Tilbudsforespørselen skulle ha vært sendt til minst to leverandører.  
3. Klikk overskriften for å gå til listen over leverandører.
4. Velg leverandøren du vil angi et svar for i tilbudsforespørselen.
5. Klikk Angi svar.
6. Klikk Svar i handlingsruten.
7. Klikk Kopier data for å svare.
    * Denne handlingen vil kopiere merkede data, for eksempel antallet fra saken for tilbudsforespørselen som svar på tilbudsforespørsel. Du kan også hoppe over denne handlingen og fylle ut alle svarfeltene manuelt når du redigerer svaret.  
8. Klikk Rediger.
9. Angi et tall i feltet Enhetspris.
10. Velg den andre tilbudslinjen.
11. Angi et tall i feltet Enhetspris.

## <a name="score-the-bid"></a>Gi budet poengsum
1. Klikk overskriften for å gå til poengsummen for budet.
2. Vis delen for poengsum for bud.
3. Angi et nummer for ett av poengsumkriteriene i poengsumfeltet.
    * Hvis du holder musepekeren over ett av poengkriteriene, viser et verktøytips området du må holde poengsummen innenfor. Du kan legge til et tall mellom 1 og 5 i et av kriteriene i denne demoen.  
4. Velg et annet poengsumkriterium.
5. Angi et nummer i poengsumfeltet.
6. Vis delen for spørreskjemaer.
    * Hvis saken for tilbudsforespørsel har et spørreskjema som ble sendt til leverandørene, kan du skrive inn svarene i spørreskjemadelen.  
7. Lukk siden.

## <a name="enter-a-reply-for-another-vendor"></a>Skriv inn et svar for en annen leverandør
1. Velg den neste leverandøren ved å fjerne leverandøren du akkurat har angitt for svaret, og deretter velge raden for den neste leverandøren.
2. Finn og velg ønsket post i listen.
3. Klikk Angi svar.
4. Klikk Kopier data for å svare.
5. Klikk Rediger.
6. Angi et tall i feltet Enhetspris.
7. Velg den andre tilbudslinjen.
8. Angi et tall i feltet Enhetspris.

## <a name="score-the-second-bid"></a>Gi den andre budet poengsum
1. Klikk overskriften for å gå til poengsummen for budet.
2. Angi et nummer i poengsumfeltet.
3. Finn og velg ønsket post i listen.
4. Angi et nummer i poengsumfeltet.

## <a name="compare-the-replies"></a>Sammenligne svarene
1. Klikk Generelt i handlingsruten.
2. Klikk Sammenlign svar.
3. Angi et tall i rangeringsfeltet.
    * Denne siden viser bud med overskrift og linjer, og den samlede poengsummen på overskriftsnivå. Du kan sammenligne linjene ved å sortere i rutenettet, slik at tilsvarende linjer er ved siden av hverandre. Informasjonen inneholder også: Antall: Antallet som er angitt av leverandøren. Dette kan være ulikt antallet angitt i tilbudsforespørselen.   Nettobeløp: Totalprisen en leverandør tilbyr, etter fratrekk for rabatter for varene på linjen.   Avvik: Antall dager som leveringsdatoen i budhodet eller -linjen avviker fra den ønskede leveringsdatoen i tilbudsforespørselshodet eller -linjen.   Du kan angi en rangering for hvert bud.  
4. Velg overskriftslinjen for det andre budet du vil rangere.
5. Angi et tall i rangeringsfeltet.
6. Klikk Lagre.

## <a name="reject-a-bid"></a>Avvise et bud
1. Velg overskriftslinjen for budet du vil avvise.
    * Du kan bare godta, avvise eller returnere ett bud eller én linje i ett bud om gangen.  
2. Merk av for Merk.
    * Hvis du merker av for Merk i overskriften til budet, vil alle linjene også merkes av. Du kan også velge å merke av et delsett av linjene i budet for å avvise eller godkjenne dem. Det er mulig å godta budet til én leverandør for noen av linjene i en tilbudsforespørsel, og deretter gi andre linjer i tilbudsforespørselen til en annen leverandør, du må imidlertid gjøre dette i trinn 2, og for ett bud om gangen. Hvis det finnes alternative linjer, kan du bare godta enten den opprinnelige budlinjen eller den alternative, men ikke begge.  
3. Klikk Avvis.
4. Klikk Parametre for å åpne nedtrekksdialogskjemaet.
5. Angi eller velg en verdi i Avvisningsårsak-feltet.
    * Årsaken til avvisningen lagres i svaret.  
6. Klikk OK.
7. Klikk OK.
8. Lukk siden.
9. Lukk siden.
10. Oppdater siden.

## <a name="accept-a-bid"></a>Godta et bud
1. Velg budet du vil godta, og deretter klikker du koblingen i Tilbudsforespørsel-feltet.
2. Klikk Svar i handlingsruten.
3. Klikk Godta.
    * Hvis du har merket av for bestemte linjer og ikke andre, vil godtahandlingen bare inneholder de merkede linjene. Hvis du vil godta alle linjer i budet, trenger du ikke merke av for linjene.  
4. Klikk Parametre for å åpne nedtrekksdialogskjemaet.
    * Dette lar deg registrere en årsak for å godta budet. Årsaken lagres i budet.  
5. Angi eller velg en verdi i Årsak til aksept-feltet.
6. Klikk OK.
7. Klikk OK.
    * Dette genererer en bestilling basert på linjene som er inkludert i godkjenning av tilbudsforespørselen når du klikker OK. Hvis det finnes andre bud som ikke er behandlet (godkjent, avvist eller returnerte), vil systemet be deg om å avvise de gjenværende budene.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Vise bestillingen som er generert
1. Klikk Generelt i handlingsruten.
2. Klikk Bestilling.
    * Her kan du se bestillingen som ble generert da du godtok budet.  
3. Lukk siden.
4. Lukk siden.
5. Lukk siden.
6. Lukk siden.


