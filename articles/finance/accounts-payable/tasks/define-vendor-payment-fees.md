---
title: Definere leverandørbetalingsgebyrer
description: Definer leverandørbetalingsgebyrer.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109837"
---
# <a name="define-vendor-payment-fees"></a>Definere leverandørbetalingsgebyrer

[!include [banner](../../includes/banner.md)]

Definer leverandørbetalingsgebyrer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Leverandører > Betalingsoppsett > Betalingsgebyr**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Gebyr-ID**.
    * **Gebyr-ID** må beskrive når dette gebyret skal brukes, for eksempel «EFT_gebyr».  
4. Skriv inn en verdi i **Navn**-feltet.
5. Skriv inn en verdi i **Gebyrbeskrivelse**-feltet.
    * Legg til en beskrivelse for å gi flere detaljer om når gebyret blir vurdert.  
6. I **Tillegg**-feltet velger du **Leverandør** eller **Finans**.
    * **Finans** brukes når gebyret skal oppføres som utgift for organisasjonen. **Leverandør** brukes når gebyret vurderes til leverandøren.  
7. Angi en hovedkonto for der gebyret skal utgiftsføres.
    * Dette alternativet er bare tilgjengelig når **Finans** er valgt som alternativet for **Tillegg**.  
8. Velg journalen som dette gebyret kan brukes i. 
    * For betalingsgebyr for en leverandør velger du journalen Leverandørbetaling.  
9. Klikk på **Lagre**.
10. Klikk på **Oppsett av betalingsgebyr**.
    * Fortsett til **Oppsett av betalingsgebyr** for å definere når gebyret skal brukes i den valgte journalen.  
11. Velg enten **Tabell**, **Gruppe** eller **Alle**.
    * **Tabell** brukes til å velge én bankkonto, **Gruppe** brukes til å velge en bankgruppe, og **Alle** er for å bruke dette gebyroppsettet for alle bankkontoer.  
12. Velg en bankkonto eller en bankgruppe.
    * Oppslaget viser bankgruppen hvis du valgte **Gruppe**, og viser bankkontoer hvis du valgte **Tabell**.  
13. Velg betalingsmåten for når dette gebyret skal vurderes.
14. Velg **Betalingsspesifikasjon** for gjeldende betalingsmetode.
    * **Betalingsspesifikasjon** brukes med betalingsmetoder for elektronisk pengeoverføring.  
15. Velg om gebyret skal være en prosent, beløp eller intervall.
16. Angi prosenten eller beløpet til gebyret.
    * Hvis **Gebyr** er en prosent, kan du angi prosenten. Hvis **Gebyr** er et beløp, kan du angi beløpet til gebyret. Hvis **Gebyr** er et intervall, kan du bruke **Intervall**-fanen til å definere trinnvise gebyrer.  
17. Velg valutaen som gebyret vurderes i, i **Gebyrvaluta**-feltet.
    * Denne valutaen er for gebyret. Betalingsvalutaen brukes til å angi når gebyrregelen skal vurderes basert på betalingsvalutaen. Banken kan for eksempel belaste deg med et gebyr når en betaling foretas i euro, men alle andre betalinger er uten gebyr.  
18. Klikk på **Lagre**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
