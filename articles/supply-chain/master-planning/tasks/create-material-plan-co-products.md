--- 
title: Opprette en materialplan for koprodukter
description: Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Opprette en materialplan for koprodukter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel. Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne fremgangsmåten.


## <a name="create-requirement-for-a-co-product"></a>Opprett behov for et koprodukt
1. Gå til standard instrumentbord.
2. Klikk Salgsordrebehandling og -spørring.
3. Klikk Ny.
4. Klikk Salgsordre.
5. Angi en verdi i Kundekonto-feltet.
    * Eksempel: US-001  
6. Klikk OK.
7. Skriv inn en verdi i Varenummer-feltet.
    * Eksempel: P6003  
8. Angi et tall i feltet Antall.
    * Eksempel: 50000  
9. Klikk Lagre.

## <a name="create-a-material-plan-for-co-products"></a>Opprette en materialplan for koprodukter
1. Klikk Hovedplanlegging.
2. Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.
3. Klikk koblingen i den valgte raden i listen.
    * Eksempel: Hovedplan  
4. Klikk Kjør.
5. Vis eller skjul delen Poster som skal inkluderes.
6. Klikk Filter.
7. I listen merker du raden for felt = varenummer.
8. Skriv inn en verdi i Kriterier-feltet.
    * Eksempel: P6003  
9. Klikk OK.
10. Klikk OK.
11. Klikk Planlagte bestillinger.
12. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.
    * Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.  
13. Merk den valgte raden i listen.
    * Velg en av radene som returneres av filteret.  
14. Klikk koblingen i den valgte raden i listen.
15. Vis eller skjul delen Utligning.
16. Klikk koblingen i den valgte raden i listen.
    * Den planlagte bestillingen er knyttet til salgsordren for koproduktet.  
17. Lukk siden.


