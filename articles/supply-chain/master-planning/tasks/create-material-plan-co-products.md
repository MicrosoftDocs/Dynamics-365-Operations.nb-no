---
title: Opprette en materialplan for koprodukter
description: Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27bba54db915b7ccc31fda43a00a8c9435493e07
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469540"
---
# <a name="create-a-material-plan-for-co-products"></a>Opprette en materialplan for koprodukter

[!include [banner](../../includes/banner.md)]

Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel. Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne fremgangsmåten.

## <a name="create-requirement-for-a-co-product"></a>Opprett behov for et koprodukt

1. Gå til **Salg og markedsføring \> Arbeidsområder \> Salgsordrebehandling og -spørring**.
1. Velg **Ny**.
1. Velg **Salgsordre**.
1. Skriv inn en verdi i **Kundekonto**-feltet.
    * Eksempel: US-001  
1. Velg **OK**.
1. Skriv inn en verdi i **Varenummer**-feltet.
    * Eksempel: P6003  
1. Angi et tall i **Antall**-feltet.
    * Eksempel: 50000  
1. Velg **Lagre**.

## <a name="create-a-material-plan-for-co-products"></a>Opprette en materialplan for koprodukter

1. Lukk siden.
1. Lukk siden.
1. Velg **Hovedplanlegging**.
1. Velg rullegardinknappen i **Plan**-feltet for å åpne oppslaget.
1. Velg koblingen i den valgte raden i listen.
    * Eksempel: Hovedplan  
1. Velg **Kjør**.
1. Vis eller skjul delen **Poster som skal inkluderes**.
1. Velg **Filter**.
1. I listen merker du raden for **Felt** = *Varenummer*.
1. Skriv inn en verdi i **Kriterier**-feltet.
    * Eksempel: P6003  
1. Velg **OK**.
1. Velg **OK**.
1. Velg **Planlagte ordrer**.
1. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på **Varenummer**-feltet med verdien P6000.
    * Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.  
1. Merk den valgte raden i listen.
    * Velg en av radene som returneres av filteret.  
1. Velg koblingen i den valgte raden i listen.
1. Vis **Utligning**-delen.
1. Velg koblingen i den valgte raden i listen.
    * Den planlagte bestillingen er knyttet til salgsordren for koproduktet.  
1. Lukk siden.

## <a name="create-a-second-requirement-for-a-co-product"></a>Opprette et nytt behov for et koprodukt

1. Gå til **Salg og markedsføring \> Arbeidsområder \> Salgsordrebehandling og -spørring**.
1. Velg **Ny**.
1. Velg **Salgsordre**.
1. Skriv inn en verdi i **Kundekonto**-feltet.
    * Eksempel: US-001  
1. Velg **OK**.
1. Skriv inn en verdi i **Varenummer**-feltet.
    * Eksempel: P6003  
1. Angi et tall i **Antall**-feltet.
    * Eksempel: 50000  
1. Velg **Lagre**.

## <a name="create-a-second-material-plan-for-co-products"></a>Opprette en ny materialplan for koprodukter

1. Velg rullegardinknappen i **Plan**-feltet for å åpne oppslaget.
2. Velg koblingen i den valgte raden i listen.
    * Eksempel: Hovedplan  
3. Velg **Kjør**.
4. Vis eller skjul delen **Poster som skal inkluderes**.
5. Velg **Filter**.
6. I listen merker du raden for **Felt** = *Varenummer*.
7. Skriv inn en verdi i *Kriterier*-feltet.
    * Eksempel: P6003  
8. Velg **OK**.
9. Velg **OK**.
10. Velg **Planlagte ordrer**.
11. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på **Varenummer**-feltet med verdien P6000.
    * Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.  
12. Merk den valgte raden i listen.
    * Velg en av radene som returneres av filteret.  
13. Velg koblingen i den valgte raden i listen.
14. Vis eller skjul delen **Utligning**.
15. Velg koblingen i den valgte raden i listen.
    * Den planlagte bestillingen er knyttet til salgsordren for koproduktet.  
16. Lukk siden.
17. Velg **Hovedplanlegging**.
18. Gå til **Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**.
19. Velg *Nei* i feltet **Deaktiver alle planleggingsprosesser**.
20. Lukk siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]