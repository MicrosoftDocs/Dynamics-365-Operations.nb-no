---
title: Opprette kundebetalingsgebyrer
description: Opprett betalingsgebyrer for kundebetalinger.
author: ShivamPandey-msft
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 15151987bb398de404994cdd416916c00a8dd1773bbf6d654f6a40160a2f4a49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768369"
---
# <a name="establish-customer-payment-fees"></a>Opprette kundebetalingsgebyrer

[!include [banner](../../includes/banner.md)]

Opprett betalingsgebyrer for kundebetalinger.

Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. I **navigasjonsruten** går du til **Moduler > Kunder > Betalingsoppsett > Betalingsgebyr**.
2. Klikk på **Ny**.
3. Angi en gebyr-ID i **Gebyr-ID**-feltet. Gebyr-IDen vises i betalingsjournaler, så gjør den beskrivende for å forstå hvilket gebyr som vurderes.  
4. Angi et gebyrnavn i **Navn**-feltet.
5. I feltet **Gebyrbeskrivelse** skriver du inn en beskrivelse for gebyret.
6. Velg om gebyret skal belastes kunden eller en finanskonto, i **Gebyr**-feltet. Hvis kunden blir vurdert gebyret, velger du Kunde. Hvis gebyret skal vurderes for organisasjonen som en utgift, velger du Finans. Velg Kunde for denne aktiviteten.  
7. I **Journaltype**-feltet velger du journaltypen som kan bruke dette betalingsgebyret. Hvis disse gebyrene brukes for betalinger fra kunder, blir sannsynligvis journaltypen Kundebetaling.  
8. Klikk **Lagre**.
9. Klikk **Oppsett av betalingsgebyr**. Betalingsgebyroppsettet brukes til å definere kriteriene for når betalingsgebyret vurderes.  Du kan for eksempel definere at avgiften beregnes hvis bankkontoen er USMF OPER og betalingsmåten er Sjekk.  
10. I **Grupperinger**-feltet velger du Tabell, Gruppe eller Alle for å definere hvilke bankkontoer som skal vurderes for dette gebyret. Hvis du velger alle, kan alle bankkontoer bli vurdert for denne avgiften.  Hvis du velger Tabell, kan bare bankkontoen du velger, vurderes for denne avgiften. Hvis du velger Gruppe, kan bare bankkontoene i den valgte bankgruppen vurderes for denne avgiften.  
11. I **Bankrelasjon**-feltet velger du enten en bankgruppe eller en bankkonto. Hvis du valgte Tabell, vil oppslaget vise bankkontoer. Hvis du valgte Gruppe, vil oppslaget vise bankgrupper.  
12. Klikk koblingen i den valgte raden i listen.
13. I **Betalingsmåte**-feltet velger du betalingsmåten dette gebyret skal vurderes for. Du kan for eksempel vurdere et gebyr til kunder hvis de sender betalinger som en sjekk, i stedet for elektronisk betaling.  
14. Finn og velg ønsket post i listen.
15. Angi en betalingsvaluta i **Betalingsvaluta**-feltet hvis det er relevant. Betalingsvalutaen brukes som et tilleggskriterium for om gebyret vurderes.  Banken kan for eksempel betale en ekstra avgift for betalinger som er mottatt i USD som valuta, siden de vanligvis bare overfører i Euro-valutaen.  
16. Velg om gebyret skal være en prosent, beløp eller intervall.
17. I **Prosent/beløp-feltet** angir du enten prosent- eller gebyrbeløpet. Hvis Prosent/beløp-feltet er Prosent, vil verdien du angir her, være en prosent. Hvis Prosent/beløp-feltet er Beløp, vil verdien du angir her, være et beløp. Hvis Prosent/beløp-feltet er Intervall, bruker du kategorien Intervall til å definere lagene.  
18. Velg valutaen for gebyret i **Gebyrvaluta**-feltet. Dette er valutaen som gebyret skal opprettes i.  
19. Klikk **Lagre**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]