--- 
title: " Konfigurere en arbeider"
description: "Denne fremgangsmåten beskriver hvordan du konfigurerer en detaljhandelarbeider som en selger som er kvalifisert for provisjon på salg i salgsstedet."
author: jblucher
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 27b075cf1152f16fc4726b224e877eacb2f2572c
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---
# <a name="configure-a-worker"></a> Konfigurere en arbeider

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du konfigurerer en detaljhandelarbeider som en selger som er kvalifisert for provisjon på salg i salgsstedet. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Opprette en provisjonssalgsgruppe for arbeideren
1. Gå til Salg og markedsføring > Provisjoner > Salgsgrupper.
    * Arbeidere kan tilordnes til én eller flere salgsgrupper. På salgsstedet kan du velge enhver salgsgruppe som inneholder arbeidere fra butikkens adressebok.  
2. Klikk Ny.
3. Skriv inn en verdi i feltet Gruppe.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk Lagre.
6. Klikk Generelt i handlingsruten.
7. Klikk Selger.
    * En salgsgruppe kan inneholde mer enn én arbeider. Provisjoner kan deles mellom arbeidere basert på hvordan du definerer provisjonsandelen.  
8. Angi eller velg en verdi i Navn-feltet.
9. Angi et tall i feltet Provisjonsandel.
10. Klikk Lagre.
11. Lukk siden.
12. Lukk siden.

## <a name="assign-the-workers-default-sales-group"></a>Tilordne standard salgsgruppe til arbeiderne
1. Gå til Detaljhandel og handel > Ansatte > Arbeidere.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk kategorien Handel.
    * En arbeider kan tilordnes til en standard salgsgruppe. Standard salgsgruppe legges automatisk til salgslinjer i salgsstedet hvis alternativet er aktivert i funksjonalitetsprofilen for butikken.  
5. Klikk Rediger.
6. Angi eller velg en verdi i Standardgruppe-feltet.
7. Klikk Lagre.


