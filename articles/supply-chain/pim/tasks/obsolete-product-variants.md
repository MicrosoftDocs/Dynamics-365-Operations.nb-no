---
title: Finne utdaterte produktvarianter
description: Denne prosedyren viser hvordan du finner foreldede frigitte produkter og produktvarianter og hvordan du knytter en produktlivssyklustilstand til de foreldede produktene.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33f16cf8c731dc1a954ed94229b2a833510dac4f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245185"
---
# <a name="find-obsolete-product-variants"></a>Finne utdaterte produktvarianter 

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du finner foreldede frigitte produkter og produktvarianter og hvordan du knytter en produktlivssyklustilstand til de foreldede produktene. Forutsetning: Du må definere minst én produktlivssyklustilstand som er inaktiv for planlegging før du kan spille av denne oppgaveveiledningen.


## <a name="run-a-simulation"></a>Kjøre en simulering
1. Gå til Behandling av produktinformasjon > Periodiske oppgaver > Endre livssyklustilstand for utdaterte produkter.
2. Angi eller velg en verdi i feltet Ny livssyklustilstand for produkt.
3. Velg Ja i Kjør simulering uten å oppdatere produktdata-feltet.
4. Angi et tall i Utelat produkter som er opprettet innen dette antallet dager.
5. Angi et tall i feltet Utelat produkter som brukes i transaksjoner (i antall dager).
6. Utvid delen Poster som skal inkluderes.
7. Klikk på Filter.
8. Merk den valgte raden i listen.
9. Skriv inn en verdi i Kriterier-feltet.
10. Klikk på OK.
11. Klikk på OK.

> [!NOTE]
> Det anbefales å kjøre simuleringen satsvis hvis du forventer å søke etter et stort antall produkter. Kontroller også at simuleringen ikke kjøres i den mest aktive arbeidstiden i firmaet.  

## <a name="review-the-simulation-results"></a>Se gjennom simuleringsresultatene
1. Gå til Behandling av produktinformasjon > Forespørsler og rapporter > Vedlikeholdshistorikk for livssyklustilstand for produkt.
   
> [!NOTE]
> På denne siden kan du gå gjennom simuleringsresultatene og vurdere hvor mange produkter og produktvarianter som skal være tilknyttet en ny produktlivssyklustilstand når du kjører oppdateringen uten simulering.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Kjøre oppdateringen av produktlivssyklustilstanden for utdaterte produkter
1. Lukk siden.
2. Gå til Behandling av produktinformasjon > Periodiske oppgaver > Endre livssyklustilstand for utdaterte produkter.
3. Utvid delen Poster som skal inkluderes.

> [!NOTE]
> Legg merke til at det siste valget er lagret.  

4. Velg Nei i Kjør simulering uten å oppdatere produktdata-feltet.
5. Utvid Kjør i bakgrunnen.

> [!NOTE]
> Avhengig av hvor mange produkter og produktvarianter som berøres, bør du vurdere å kjøre denne jobben satsvis. Pass på at du ikke kjører en stor oppdateringsjobb i den mest aktive arbeidstiden i firmaet.  

6. Klikk på OK.
7. Gå til Behandling av produktinformasjon > Forespørsler og rapporter > Vedlikeholdshistorikk for livssyklustilstand for produkt.

> [!NOTE]
> Se gjennom de endrede frigitte produktene og produktvariantene.  

8. Finn og velg ønsket post i listen.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]