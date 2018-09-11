--- 
title: "Spore en vare eller råvare"
description: "Denne fremgangsmåten beskriver hvordan du bruker varesporing til å identifisere hvor varer eller råmaterialer er brukt, eller er i bruk."
author: pjacobse
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d7eb282ddf9597385d6660a3fc0ef73f403ab898
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="trace-an-item-or-raw-material"></a>Spore en vare eller råvare

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du bruker varesporing til å identifisere hvor varer eller råmaterialer er brukt, eller er i bruk. Du kan identifisere en vare, spore den tilbake til kilden, og deretter spore fremover gjennom produksjon og salg av det ferdige produktet med denne fremgangsmåten. Prosessen kan brukes til å undersøke kundene berørt, salgsordrene påvirket og mer. Denne prosedyren bruker demonstrasjonsdatafirmaet USP2.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Spore en vare bakover ved hjelp av et kjent partinummer
1. Gå til Lagerstyring > Forespørsler og rapporter > Sporingsdimensjoner > Varesporing.
2. Velg P9100 i feltet Varenummer.
3. Klikk koblingen i den valgte raden i listen.
4. Velg "Bakover" i feltet Forover eller bakover.
5. Velg som-12-344-01 i Partinummer-feltet
6. Klikk koblingen i den valgte raden i listen.
7. Klikk OK.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Identifisere en vare, spore den fremover og gjøre en analyse
    * Toppnoden i treet representerer beholdningen for den valgte varen og partiet. Du må vise nodene i treet for å finne varen som fremoversporingen skal utføres på.   
1. I treet viser du nodene som er beskrevet nedenfor, og velger deretter den siste noden.
    * Vis: P9100 / 1 / 10 / som-12-344-01 ● 2 keg ● 7,00 gal \P9100 ● Plukket ● Salgsordre 000072 ● 12/22/2015 ● -1 keg ● -4,00 gal ● Område = 1, Lager=10, Partinummer=som-12-344-01 \P9100 ● Produksjon B-000050 ● 12/9/2015● 7 keg ● 27,00 gal ● Område=1, Lager=10, Partinummer=som-12-344-01 ● Koprodukter: P9101, og velg deretter noden.     
2. I treet viser du noden som er beskrevet nedenfor, og velger deretter denne noden.
    * Fra og med noden som du akkurat har valgtviser du M9103 ● Produksjonslinje B-000050 ● 12/9/2015 ● -160,00 lb ● Størrelse=70, Farge=OK, Område=1, Lager=10, Partinummer=App01, og velg deretter denne noden.  
3. Klikk Spor fra node.
4. Klikk Forover.
5. Klikk Sporing i handlingsruten.
    * Det finnes flere sporingsalternativer som gir informasjon om hvilke kunder som berøres av varen som du sporer og salgsordrene som er knyttet til varen som har blitt og ikke er levert.   
6. Klikk Kunder.
7. Lukk siden.
8. Klikk Sporing i handlingsruten.
9. Klikk Leverte salgsordrer.
10. Lukk siden.


