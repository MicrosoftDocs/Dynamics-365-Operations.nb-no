---
title: Rapportere en produksjonsordre som avsluttet
description: Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa27691942b27886e85c52b7b3a736a62db7b7bd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580606"
---
# <a name="report-a-production-order-as-finished"></a>Rapportere en produksjonsordre som avsluttet

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den sjette fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.


## <a name="report-a-production-order-as-finished"></a>Rapportere en produksjonsordre som avsluttet
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
    * Velg en produksjonsordre med statusen Startet.  
2. Klikk på Produksjonsordre i handlingsruten.
3. Klikk på Rapporter som fullført.
    * På denne siden kan du bekrefte antallet av det ferdige produktet som skal rapporteres som fullført.  
4. Klikk på fanen Generelt.
5. Angi Antall korrekte til "18".
6. Angi Antall feil til 2.
7. Velg "Materiale" i Feilårsak-feltet.
8. Merk av eller fjern merket i avmerkingsboksen Avslutt jobb.
9. Merk av eller fjern merket i boksen Godtar feil.
10. Klikk på OK.

## <a name="verify-the-report-as-finished-journal"></a>Verifisere ferdigmeldingsjournalen
1. Klikk på Vis i handlingsruten.
2. Klikk på Ferdigmeldt.
3. Merk den valgte raden i listen.
4. Klikk på koblingen i den valgte raden i listen.
    * Ferdigmeldingsjournalen er postert. Hvis du vil foreta justeringer i journalen, kan du manuelt opprette en ny journal der du kan gjøre endringer.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]