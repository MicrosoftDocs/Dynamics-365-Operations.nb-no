---
title: Starte en produksjonsordre
description: Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9822dd66876ef8ed6bbcd5846a39d69d2446d7a7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981086"
---
# <a name="start-a-production-order"></a>Starte en produksjonsordre

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du starter en produksjonsordre i shop floor. Tid og materialforbruk blir rapportert i denne prosessen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den femte fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.


## <a name="start-a-production-order"></a>Starte en produksjonsordre
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
    * Velg en produksjonsordre med statusen Frigitt.  
2. Klikk på Produksjonsordre i handlingsruten.
3. Klikk på Start.
    * På denne siden kan du bekrefte starten på produksjonsordren.  
4. Klikk på fanen Generelt.
5. I Fra oper. Nei. -feltet skriver du inn 10.
6. Velg "Alltid" i feltet Automatisk ruteforbruk.
7. Merk av for Poster rutekort nå.
8. Velg "Alltid" i feltet Automatisk stykklisteforbruk.
9. Klikk på avmerkingsboksen Poster plukkliste nå.
10. Klikk på avmerkingsboksen Skriv ut plukkliste.
11. Klikk på OK.
    * Dette er den utskrevne plukklisten som viser materialene som ble brukt for produksjonsordren.  
12. Lukk siden.

## <a name="validate-the-picking-list"></a>Validere plukklisten
1. Klikk på Vis i handlingsruten.
2. Klikk på Plukkliste.
3. Finn og velg ønsket post i listen.
4. Klikk på koblingen i den valgte raden i listen.
5. Klikk på Rediger.
6. Skriv inn et tall i Forbruk-feltet.
7. Klikk på Poster.
8. Klikk på OK.
    * I plukklistejournalen posteres materialene som forbrukes av produksjonsordren. Før du posterer journalen, kan du gjøre justeringer hvis det er forskjell mellom det estimerte antallet og det faktiske forbrukte antallet.  
9. Klikk på fanen GridPanel.
10. Lukk siden.

## <a name="verify-the-route-card-journal"></a>Verifisere rutekortjournalen
1. Klikk på Vis i handlingsruten.
2. Klikk på Rutekort.
3. Finn og velg ønsket post i listen.
4. Klikk på koblingen i den valgte raden i listen.
5. Klikk på Rediger.
6. Angi et tall i feltet Timer.
7. Klikk på Poster.
8. Klikk på OK.
    * Tiden som brukes på de enkelte operasjonene er registrert i rutekortjournalen. Antall korrekte og feil kan også rapporteres.  
