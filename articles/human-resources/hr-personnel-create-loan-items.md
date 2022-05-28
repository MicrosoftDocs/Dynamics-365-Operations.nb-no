---
title: Opprett utlånsvarer
description: Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26bf5a83a6d25e99996ec4219c5fbbeed806e22d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693731"
---
# <a name="create-loan-items"></a>Opprett utlånsvarer


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere. Hver fysiske vare må ha en tilsvarende utlånsvare. Hver utlånsvarepost må beskrive hva som lånes ut, hvem som er ansvarlig for utlånet og antall dager varen kan lånes ut. Du kan opprette flere utlånsvarer, for eksempel nøkler, adgangskort eller uniformer, samtidig. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-loan-types"></a>Opprette utlånstyper
1. Gå til **Personale** > **Arbeidere** > **Utlånsvarer** > **Utlånstyper**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Utlånstype**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Definer antall dager som varer som er tilordnet til denne utlånstypen, kan være forfalt med. 
6. Klikk på **Lagre**.
7. Lukk siden.
8. Oppdater siden.

## <a name="create-loan-items"></a>Opprette utlånsvarer
1. Gå til **Personale** > **Arbeidere** > **Utlånsvarer** > **Utlånsvarer**.
2. Klikk **Opprett utlånsvarer**.
3. Angi et tall i **Antall**-feltet.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Klikk på rullegardinknappen i **Utlånstype**-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Angi antallet dager varen kan være på utlån.
    * Standardverdien for Planlagt retur-feltet på siden Lånt utstyr blir beregnet som gjeldende dato pluss dette antallet.  
9. Klikk på rullegardinknappen i **Ansvarlig**-feltet for å åpne oppslaget.
10. Klikk på **Velg**.
11. Angi et tall i **Startverdi**-feltet.
12. Angi et tall i **Intervall**-feltet.
13. Skriv inn en verdi i **Format**-feltet.
    * Hvis startnummeret for en utlånsvare for eksempel er 10, angir du to nummersymboler i **Format**-feltet.  
14. Klikk på **OK**.
15. Oppdater siden.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
