--- 
title: Opprette kundebetalingsgebyrer
description: Opprett betalingsgebyrer for kundebetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 659f4560747cea73c61a9b748a980946ca252bd6
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-fees"></a>Opprette kundebetalingsgebyrer

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Opprett betalingsgebyrer for kundebetalinger.

Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til Kunder > Betalingsoppsett > Betalingsgebyr.
2. Klikk Ny.
3. Angi en gebyr-ID i Gebyr-ID-feltet.
    * Gebyr-IDen vises i betalingsjournaler, så gjør den beskrivende for å forstå hvilket gebyr som vurderes.  
4. Angi et gebyrnavn i Navn-feltet.
5. I feltet Gebyrbeskrivelse skriver du inn en beskrivelse for gebyret.
6. Velg om gebyret skal belastes kunden eller en finanskonto.
    * Hvis kunden blir vurdert gebyret, velger du Kunde. Hvis gebyret skal vurderes for organisasjonen som en utgift, velger du Finans. Velg Kunde for denne aktiviteten.  
7. Velg journaltypen som kan bruke dette betalingsgebyret.
    * Hvis disse gebyrene brukes for betalinger fra kunder, blir sannsynligvis journaltypen Kundebetaling.  
8. Klikk Lagre.
9. Klikk Oppsett av betalingsgebyr.
    * Betalingsgebyroppsettet brukes til å definere kriteriene for når betalingsgebyret vurderes.  Du kan for eksempel definere at avgiften beregnes hvis bankkontoen er USMF OPER og betalingsmåten er Sjekk.  
10. Velg Tabell, Gruppe eller Alle for å definere hvilke bankkontoer som skal vurderes for dette gebyret.
    * Hvis du velger alle, kan alle bankkontoer bli vurdert for denne avgiften.  Hvis du velger Tabell, kan bare bankkontoen du velger, vurderes for denne avgiften. Hvis du velger Gruppe, kan bare bankkontoene i den valgte bankgruppen vurderes for denne avgiften.  
11. Velg en bankkonto eller en bankgruppe.
    * Hvis du valgte Tabell, vil oppslaget vise bankkontoer. Hvis du valgte Gruppe, vil oppslaget vise bankgrupper.  
12. Klikk koblingen i den valgte raden i listen.
13. Velg betalingsmåten som dette gebyret skal vurderes for.
    * Du kan for eksempel vurdere et gebyr til kunder hvis de sender betalinger som en sjekk, i stedet for elektronisk betaling.  
14. Finn og velg ønsket post i listen.
15. Hvis relevant, angi en betalingsvaluta.
    * Betalingsvalutaen brukes som et tilleggskriterium for om gebyret vurderes.  Banken kan for eksempel betale en ekstra avgift for betalinger som er mottatt i USD som valuta, siden de vanligvis bare overfører i Euro-valutaen.  
16. Velg om gebyret skal være en prosent, beløp eller intervall.
17. Angi prosenten eller beløpet til gebyret.
    * Hvis Prosent/beløp-feltet er Prosent, vil verdien du angir her, være en prosent. Hvis Prosent/beløp-feltet er Beløp, vil verdien du angir her, være et beløp. Hvis Prosent/beløp-feltet er Intervall, bruker du kategorien Intervall til å definere lagene.  
18. Velg valutaen for gebyret i Gebyrvaluta-feltet.
    * Dette er valutaen som gebyret skal opprettes i.  
19. Klikk Lagre.


