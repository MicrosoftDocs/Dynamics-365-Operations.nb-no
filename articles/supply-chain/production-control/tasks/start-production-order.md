---
title: Starte en produksjonsordre
description: "Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 3b5657e5eb2719702eae3a3c5178b3a04f7545e3
ms.contentlocale: nb-no
ms.lasthandoff: 02/06/2018

---
# <a name="start-a-production-order"></a>Starte en produksjonsordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor. Tid og materialforbruk blir rapportert i denne prosessen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den femte fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.


## <a name="start-a-production-order"></a>Starte en produksjonsordre
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
    * Velg en produksjonsordre med statusen Frigitt.  
2. Klikk Produksjonsordre i handlingsruten.
3. Klikk Start.
    * På denne siden kan du bekrefte starten på produksjonsordren.  
4. Klikk kategorien Generelt.
5. I Fra oper. Nr. -feltet skriver du inn 10.
6. Velg "Alltid" i feltet Automatisk ruteforbruk.
7. Merk av for Poster rutekort nå.
8. Velg "Alltid" i feltet Automatisk stykklisteforbruk.
9. Klikk avmerkingsboksen Poster plukkliste nå.
10. Klikk avmerkingsboksen Skriv ut plukkliste.
11. Klikk OK.
    * Dette er den utskrevne plukklisten som viser materialene som ble brukt for produksjonsordren.  
12. Lukk siden.

## <a name="validate-the-picking-list"></a>Validere plukklisten
1. Klikk Vis i handlingsruten.
2. Klikk Plukkliste.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Klikk Rediger.
6. Skriv inn et tall i Forbruk-feltet.
7. Klikk Poster.
8. Klikk OK.
    * I plukklistejournalen posteres materialene som forbrukes av produksjonsordren. Før du posterer journalen, kan du gjøre justeringer hvis det er forskjell mellom det estimerte antallet og det faktiske forbrukte antallet.  
9. Klikk kategorien GridPanel.
10. Lukk siden.

## <a name="verify-the-route-card-journal"></a>Verifisere rutekortjournalen
1. Klikk Vis i handlingsruten.
2. Klikk Rutekort.
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Klikk Rediger.
6. Angi et tall i feltet Timer.
7. Klikk Poster.
8. Klikk OK.
    * Tiden som brukes på de enkelte operasjonene er registrert i rutekortjournalen. Antall korrekte og feil kan også rapporteres.  

