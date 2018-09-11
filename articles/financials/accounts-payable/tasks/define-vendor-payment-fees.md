--- 
title: "Definere leverandørbetalingsgebyrer"
description: "Definer leverandørbetalingsgebyrer."
author: abruer
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f62d07ffa1ee4a525f0f266922bc88e5ac8d5ada
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="define-vendor-payment-fees"></a>Definere leverandørbetalingsgebyrer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Definer leverandørbetalingsgebyrer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til Leverandører > Betalingsoppsett > Betalingsgebyr.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Gebyr-ID.
    * Gebyr-IDen må beskrive når dette gebyret skal brukes, for eksempel "EFT_gebyr".  
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i Gebyrbeskrivelse-feltet.
    * Legg til en beskrivelse for å gi flere detaljer om når gebyret blir vurdert.  
6. I Tillegg-feltet velger du Leverandør eller Finans.
    * Finans brukes når gebyret skal oppføres som utgift for organisasjonen.  Leverandør brukes når gebyret vurderes til leverandøren.  
7. Angi en hovedkonto for der gebyret skal utgiftsføres.
    * Dette alternativet er bare tilgjengelig når Finans er valgt som Tillegg-alternativet.  
8. Velg journalen som dette gebyret kan brukes i. 
    * For betalingsgebyr for en leverandør velger du journalen Leverandørbetaling.  
9. Klikk Lagre.
10. Klikk Oppsett av betalingsgebyr.
    * Fortsett til betalingsgebyroppsettet for å definere når gebyret skal brukes i den valgte journalen.  
11. Velg enten Tabell Gruppe eller Alle.
    * Tabell brukes til å velge én bankkonto, Gruppe brukes til å velge en bankgruppe, og Alle er for å bruke dette gebyroppsettet for alle bankkontoer.  
12. Velg en bankkonto eller en bankgruppe.
    * Oppslaget viser bankgruppen hvis du valgte Gruppe, og viser bankkontoer hvis du valgte Tabell.  
13. Velg betalingsmåten for når dette gebyret skal vurderes.
14. Velg betalingsspesifikasjonen for gjeldende betalingsmåte.
    * Betalingsspesifikasjonen brukes med betalingsmåter for elektronisk pengeoverføring.  
15. Velg om gebyret skal være en prosent, beløp eller intervall.
16. Angi prosenten eller beløpet til gebyret.
    * Hvis gebyret er en prosent, kan du angi prosenten. Hvis gebyret er et beløp, kan du angi beløpet til gebyret. Hvis gebyret er et intervall, kan du bruke kategorien Intervall til å definere trinnvise gebyrer.  
17. Velg valutaen som gebyret vurderes i, i Gebyrvaluta-feltet.
    * Denne valutaen er for gebyret. Betalingsvalutaen brukes til å angi når gebyrregelen skal vurderes basert på betalingsvalutaen. Banken kan for eksempel belaste deg med et gebyr når en betaling foretas i euro, men alle andre betalinger er uten gebyr.  
18. Klikk Lagre.


