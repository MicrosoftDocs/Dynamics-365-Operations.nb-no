--- 
title: "Konfigurere alle nødvendige nummerserier ved å bruke en veiviser"
description: "Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5fe6e54b4ebcf6cd611af54e7066a3e39d0e677d
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a>Konfigurere alle nødvendige nummerserier ved å bruke en veiviser

[!include[task guide banner](../../includes/task-guide-banner.md)]

Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem. En hoveddata- eller transaksjonspost som krever en ID kalles en referanse. Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse. Denne fremgangsmåten beskriver hvordan du definerer alle nødvendige nummerserier samtidig ved å bruke en veiviser. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til Organisasjonsadministrasjon > Nummerserier > Nummerserier.
2. Klikk Generer.
3. Klikk Neste.
    * På denne siden kan du endre ID-koden, den laveste verdien og den høyeste verdien. Du kan i tillegg angi om nummerserien må være sammenhengende.   
    * Ikke velg Fortløpende-alternativet hvis du må forhåndstildele numre for nummerserien.     Hvis du vil legge til et omfangssegment for formatet for en nummerserie, velger du formatet i listen og klikker deretter Ta med omfang i format.     Hvis du vil fjerne et omfangssegment fra formatet for en nummerserie, velger du formatet i listen og klikker deretter Fjern omfang fra format.     Hvis du vil utelukke en nummerserie fra automatisk generering, velger du nummerserien i listen og klikker deretter Slett.  
4. Klikk Neste.
5. Klikk Finish.


