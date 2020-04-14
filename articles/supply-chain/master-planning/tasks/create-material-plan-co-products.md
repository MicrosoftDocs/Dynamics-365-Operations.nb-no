---
title: Opprette en materialplan for koprodukter
description: Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148084"
---
# <a name="create-a-material-plan-for-co-products"></a>Opprette en materialplan for koprodukter

[!include [banner](../../includes/banner.md)]

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
1. Lukk siden.
2. Lukk siden.
3. Klikk Hovedplanlegging.
4. Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
    * Eksempel: Hovedplan  
6. Klikk Kjør.
7. Vis eller skjul delen Poster som skal inkluderes.
8. Klikk Filter.
9. I listen merker du raden for felt = varenummer.
10. Skriv inn en verdi i Kriterier-feltet.
    * Eksempel: P6003  
11. Klikk OK.
12. Klikk OK.
13. Klikk Planlagte bestillinger.
14. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.
    * Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.  
15. Merk den valgte raden i listen.
    * Velg en av radene som returneres av filteret.  
16. Klikk koblingen i den valgte raden i listen.
17. Vis eller skjul delen Utligning.
18. Klikk koblingen i den valgte raden i listen.
    * Den planlagte bestillingen er knyttet til salgsordren for koproduktet.  
19. Lukk siden.

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
1. Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.
2. Klikk koblingen i den valgte raden i listen.
    * Eksempel: Hovedplan  
3. Klikk Kjør.
4. Vis eller skjul delen Poster som skal inkluderes.
5. Klikk Filter.
6. I listen merker du raden for felt = varenummer.
7. Skriv inn en verdi i Kriterier-feltet.
    * Eksempel: P6003  
8. Klikk OK.
9. Klikk OK.
10. Klikk Planlagte bestillinger.
11. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.
    * Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.  
12. Merk den valgte raden i listen.
    * Velg en av radene som returneres av filteret.  
13. Klikk koblingen i den valgte raden i listen.
14. Vis eller skjul delen Utligning.
15. Klikk koblingen i den valgte raden i listen.
    * Den planlagte bestillingen er knyttet til salgsordren for koproduktet.  
16. Lukk siden.
17. Klikk Hovedplanlegging.
18. Gå til Hovedplanlegging > Oppsett > Parametere for hovedplanlegging.
19. Velg Nei i feltet Deaktiver alle planleggingsprosesser.
20. Lukk siden.

