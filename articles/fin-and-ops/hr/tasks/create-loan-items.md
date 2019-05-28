---
title: Opprett utlånsvarer
description: Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75b2f17eb41ead7422276f72429eb6ede2ef4759
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507895"
---
# <a name="create-loan-items"></a>Opprett utlånsvarer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Utlånsvarer er poster som hjelper deg med å spore fysiske varer, for eksempel telefoner eller datamaskiner, som firmaet låner ut til arbeidere. Hver fysiske vare må ha en tilsvarende utlånsvare. Hver utlånsvarepost må beskrive hva som lånes ut, hvem som er ansvarlig for utlånet og antall dager varen kan lånes ut. Du kan opprette flere utlånsvarer, for eksempel nøkler, adgangskort eller uniformer, samtidig. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-loan-types"></a>Opprette utlånstyper
1. Gå til Personale > Arbeidere > Utlånsvarer > Utlånstyper.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Utlånstype.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Definer antall dager som varer som er tilordnet til denne utlånstypen, kan være forfalt med. 
6. Klikk Lagre.
7. Lukk siden.
8. Oppdater siden.

## <a name="create-loan-items"></a>Opprette utlånsvarer
1. Gå til Personale > Arbeidere > Utlånsvarer > Utlånsvarer.
2. Klikk Opprett utlånsvarer.
3. I Antall-feltet angir du et nummer.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk rullegardinknappen i Utlånstype-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Angi antallet dager varen kan være på utlån.
    * Standardverdien for Planlagt retur-feltet på siden Lånt utstyr blir beregnet som gjeldende dato pluss dette antallet.  
9. Klikk rullegardinknappen i Ansvarlig-feltet for å åpne oppslaget.
10. Klikk Velg.
11. Angi et tall i Startverdi-feltet.
12. Angi et tall i Intervall-feltet.
13. Skriv inn en verdi i Format-feltet.
    * Hvis startnummeret for en utlånsvare for eksempel er 10, angir du to nummersymboler i Format-feltet.  
14. Klikk OK.
15. Oppdater siden.

