--- 
title: Opprette og tilordne en kostnadsfordelingspolicy til en kostnadskontrollenhet
description: "Bruk denne fremgangsmåten til å opprette og tilordne en policy for tildeling av kostnader og de tilsvarende til en enhet for kontroll av kostnaden."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 82319d8d9c7b567f98dfd0e591cb99079fb577b7
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Opprette og tilordne en kostnadsfordelingspolicy til en kostnadskontrollenhet

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bruk denne fremgangsmåten til å opprette og tilordne en policy for tildeling av kostnader og de tilsvarende til en enhet for kontroll av kostnaden. Denne registreringen bruker USP2-demodatafirmaet.


## <a name="create-a-policy"></a>Opprette en policy
1. Gå til Kostnadsregnskap > Policyer > Kostnadsfordelingspolicyer.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Policynavn.
4. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.
    * Velg Organisasjon.  
5. Angi eller velg en verdi i feltet Statistisk dimensjon.
6. Klikk Lagre.

## <a name="create-allocation-rules"></a>Opprette fordelingsregler
1. Klikk Ny.
2. Merk den valgte raden i listen.
3. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
4. Velg "Total" i feltet Kostnadsatferd.
5. Angi eller velg en verdi i feltet Tildelingsgrunnlag.
6. Klikk Ny.
7. Merk den valgte raden i listen.
8. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
9. Velg "Total" i feltet Kostnadsatferd.
10. Angi eller velg en verdi i feltet Tildelingsgrunnlag.
11. Klikk Ny.
12. Merk den valgte raden i listen.
13. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
14. Velg "Total" i feltet Kostnadsatferd.
15. Angi eller velg en verdi i feltet Tildelingsgrunnlag.
    * Fortsett til du har opprettet alle reglene.  
16. Klikk Lagre.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Tilordne policyen til en kostnadskontrollenhet
1. Klikk Policytilordninger for kostnadskontrollenhet.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Angi en dato i feltet Gyldig fra regnskapsdato.
    * Reglene er datoeffektive. En bruker eller systemet kan utløpe reglene hvis det opprettes en nyere versjon.  
5. Angi eller velg en verdi i feltet Kostnadskontrollenhet
6. Klikk Lagre.


