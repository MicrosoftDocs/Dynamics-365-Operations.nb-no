---
title: Vedlikeholde rute for en produktmodell
description: Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921271"
---
# <a name="maintain-route-for-a-product-model"></a>Vedlikeholde rute for en produktmodell

[!include [banner](../../includes/banner.md)]

Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes. Denne fremgangsmåten bruker modellen for High-end-høyttaler i demofirmaet USMF til å lede deg gjennom prosessen.

## <a name="add-a-route-operation"></a>Legge til en ruteoperasjon

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.
1. Finn og velg ønsket post i listen.
    * Velg High-end-høyttalermodellen for denne øvelsen.  
1. Velg koblingen i den valgte raden i listen.
1. Utvid delen **Ruteoperasjoner**.
1. Velg **Legg til**.
1. Skriv inn en verdi i **Navn**-feltet.
1. Skriv inn en verdi i **Beskrivelse**-feltet.
1. Velg **Lagre**.

## <a name="enter-route-operation-details"></a>Angi detaljer om ruteoperasjon

1. Velg **Detaljer om ruteoperasjon**.
1. Angi eller velg en verdi i feltet **Operasjon**.
1. I feltet **Oper.nr.** angir du et nummer.
    * Operasjonsnumre fastsetter rutesekvensen.  
    * Hver egenskap for en ruteoperasjon kan få en statisk verdi eller tilordnes til et attributt. Tilordning til et attributt fører til at verdien blir definert som en del av konfigurasjonen.  
1. Angi eller velg en verdi i **Rutegruppe**-feltet.
    * Rutegruppen bestemmer grunnleggende virkemåte for etterkalkulering, forbruk og oppsett.  
1. Velg **Oppsett**-fanen.
1. Velg **Tider**-fanen.
1. I feltet **Prosessantall** angir du et nummer.
    * Bestem hvor mange som skal bli behandlet i løpet av én operasjon.  
1. Angi et tall i feltet **Timer/tid**.
    * Angi tidsforholdet.  
1. Merk av for **Sett**.
1. Angi et tall i feltet **Kjøretid**.
    * Bestem behandlingstiden for antallet som du har angitt.  
1. Velg fanen **Ressursbehov**.
1. Velg **Legg til**.
1. Merk den valgte raden i listen.
1. Velg et alternativ i feltet **Behovstype**.
    * Bestem om du vil angi bestemte ressurser eller egenskaper som de må inneha.  
1. Angi eller velg en verdi i feltet **Behov**.
1. Velg **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]