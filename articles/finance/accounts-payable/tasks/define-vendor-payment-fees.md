---
title: Definere leverandørbetalingsgebyrer
description: Definer leverandørbetalingsgebyrer.
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0871e0889b078c08e4bcbd86bf749bcfe39463
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837276"
---
# <a name="define-vendor-payment-fees"></a>Definere leverandørbetalingsgebyrer

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]