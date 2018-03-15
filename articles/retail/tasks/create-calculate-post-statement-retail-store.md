--- 
title: " Opprette, beregne og postere et utdrag for en detaljhandel"
description: "Denne prosedyren hjelper deg gjennom de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 33ebb28196baa9ae944dbd124274b05cb587fea4
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Opprette, beregne og postere et utdrag for en detaljhandel

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg gjennom de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk. Det finnes også satsvise jobber som kan konfigureres for de samme oppgavene. Du finner fremgangsmåten for å konfigurere og kjøre de satsvise jobbene i andre emner. Hvis du vil fullføre denne prosedyren, må du ha transaksjoner som ble fullført i POS, og deretter overført til Dynamics AX. Denne registreringen bruker firmaet USRT i demonstrasjonsdataene. Denne fremgangsmåten kan referere til Microsoft Dynamics AX. Legg merke til at Dynamics AX nå kalles Microsoft Dynamics 365 for Operations.

1. Gå til Alle arbeidsområder > .. > Finans for detaljhandelsbutikk.
2. Klikk Nytt utdrag.
3. Klikk rullegardinknappen i feltet Butikknummer for å åpne oppslaget.
4. Klikk koblingen i den valgte raden i listen.
5. Klikk OK.
    * Oppsett-gruppen inneholder innstillingene som styrer hvilke transaksjoner som inkluderes i utdraget, og hvordan de grupperes i utdragslinjene. Du kan åpne Oppsett-gruppen og endre disse innstillingene, eller du kan bruke standardinnstillingene.  
    * Feltet Utdragsmetode angir hvordan utdragslinjene skal grupperes.  
    * Velg et stabsmedlem eller en kasse hvis du vil beregne et utdrag bare for bestemte stabsmedlemmer eller kasser.  
6. Velg et alternativ i Avslutningsmetode-feltet.
7. Klikk Beregn utdrag.
8. Klikk Ja.
    * Når du har beregnet utdraget, skal det være opprettet linjer med totalbeløp for hver betalingsmåte og utdragsmetode som ble brukt.  
    * Angi et opptelt beløp i hver linje hvis den må angis eller oppdateres. Telt opp-feltet fylles ut med beløp fra kasseoppgjør i POS.  
9. Klikk Poster utdrag.
10. Klikk Lukk.
11. Gå til Detaljhandel og handel > Kanaler > Finans for detaljhandelsbutikk.
12. Klikk kategorien Posterte utdrag.


