---
title: Beregne forslag til Kanban-antall
description: Denne prosedyren fokuserer på å optimalisere kanban-størrelse og -antall for en bestemt Kanban-regel ved hjelp av Kanban-antallsberegningen.
author: johanhoffmann
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18d2a8dd2a8c132873744ba890ca6b1eb1fd34b6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570136"
---
# <a name="calculate-kanban-quantity-suggestions"></a>Beregne forslag til Kanban-antall

[!include [banner](../../includes/banner.md)]

Denne prosedyren fokuserer på å optimalisere kanban-størrelse og -antall for en bestemt Kanban-regel ved hjelp av Kanban-antallsberegningen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for verdistrømsbehandling. Det er en forutsetning at du har fullført prosedyren Legg til en ny policy for Kanban-antallsberegning i en Kanban-regel.


## <a name="create-a-kanban-quantity-calculation"></a>Opprett en beregning av Kanban-antall
1. Gå til Produksjonskontroll > Periodiske oppgaver > Kanban-antallsberegning > Beregn Kanban-antall.
2. Klikk på Ny.
3. I Navn-feltet skriver du inn Speaker2016.
4. Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.
    * Velg policyen som du har opprettet i prosedyren Legg til en ny policy for Kanban-antallsberegning i en Kanban-regel. For eksempel Speaker2016.  
5. Klikk på koblingen i den valgte raden i listen.
6. I feltet Aktiveringsdato for regel setter du datoen og klokkeslettet til 2012-12-17T08:00:00.
    * Denne datoen fungerer som grunnlaget for å bestemme hvilke faste Kanban-regler som skal inngå i beregningen av Kanban-antall.  
7. I feltet Startdato for innfridd behovsperiode setter du datoen og klokkeslettet til 2012-11-17T09:00:00.
    * Fra-datoen for å inkludere transaksjoner for tidligere behov i beregning av Kanban-antall.  
8. I feltet Sluttdato for innfridd behovsperiode setter du datoen og klokkeslettet til 2012-12-17T07:59:59.
    * Til-datoen for å inkludere transaksjoner for tidligere behov i beregning av Kanban-antall.  
9. I feltet Startdato for behovsperiode setter du datoen og klokkeslettet til 2012-12-17T08:00:00.
    * Fra-datoen for å inkludere transaksjoner for nåværende behov i beregning av Kanban-antall.  
10. I feltet Sluttdato for behovsperiode setter du datoen og klokkeslettet til 2013-01-16T07:59:59.
    * Til-datoen for å inkludere transaksjoner for nåværende behov i beregning av Kanban-antall.  

## <a name="generate-kanban-quantity-proposal"></a>Generer Kanban-antallsforslag
1. Klikk på Lagre.
2. Klikk på Generer.
    * Dette genererer en forslagslinje for kanban-antall for kanban-regelen 000020.  

## <a name="run-kanban-quantity-calculation"></a>Kjør Kanban-antallsberegning
1. Klikk på Beregn.
    * Den beregner forslaget for kanban-antall.  
2. Klikk på OK.
3. Merk den valgte raden i listen.
    * Legg merke til at det foreslåtte kanban-antallet er 2.  

## <a name="change-product-quantity-and-calculate-again"></a>Endre produktantallet og beregne på nytt
1. Sett Produktantall til 5.
2. Klikk på Beregn.
3. Klikk på OK.
    * Legg merke til at med et kanban-antall på 5, endres forslaget til et kanban-antall på 4.  
    * Dette skyldes det faktum at med et lavere produktantall trenger vi flere Kanbaner som skal dekke behovet.  

## <a name="update-kanban-rule"></a>Oppdater Kanban-regel
1. Angi dato og klokkeslett i feltet Ikrafttredelsesdato for regel.
    * Angi Aktiveringsdato for regel til en dato i fremtiden. For eksempel i dag + ett år.  
2. Klikk på Oppdater.
3. Klikk på OK.
4. Lukk siden.

## <a name="validate-change-on-kanban-rule"></a>Valider endring i kanban-regel
1. Gå til Behandling av produktinformasjon > Lean manufacturing > Kanban-regler.
2. Klikk på koblingen i den valgte raden i listen.
    * Velg kanban-regelen som ble opprettet i den forrige underoppgaven. Dette bør være den første kanban-regelen i listen sortert etter nummer.  
3. Aktiver/deaktiver utvidelsen av delen Detaljer.
    * Legg merke til den gyldige datoen, som betyr at denne regelen ikke aktiveres før denne datoen.  
4. Aktiver/deaktiver utvidelsen av delen Antall.
    * Legg merke til at dette er standardantallet som du angav i beregningen av kanban-antall.  
    * Legg merke til dette er det faste kanban-antallet på 4 fra beregningen av kanban-antall.  
5. Klikk på fanen ListPanel.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]