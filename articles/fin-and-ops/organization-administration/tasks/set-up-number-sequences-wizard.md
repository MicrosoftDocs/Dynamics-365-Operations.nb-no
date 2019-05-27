---
title: Konfigurere alle nødvendige nummerserier ved å bruke en veiviser
description: Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1808ab9240ab291f9d203893a634bd390f16e2e7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560550"
---
# <a name="set-up-number-sequences-by-using-a-wizard"></a>Konfigurere alle nødvendige nummerserier ved å bruke en veiviser

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem. En hoveddata- eller transaksjonspost som krever en ID kalles en referanse. Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse. Denne fremgangsmåten beskriver hvordan du definerer alle nødvendige nummerserier samtidig ved å bruke en veiviser. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til Organisasjonsadministrasjon > Nummerserier > Nummerserier.
2. Klikk Generer.
3. Klikk Neste.
    * På denne siden kan du endre ID-koden, den laveste verdien og den høyeste verdien. Du kan i tillegg angi om nummerserien må være sammenhengende.   
    * Ikke velg Fortløpende-alternativet hvis du må forhåndstildele numre for nummerserien.     Hvis du vil legge til et omfangssegment for formatet for en nummerserie, velger du formatet i listen og klikker deretter Ta med omfang i format.     Hvis du vil fjerne et omfangssegment fra formatet for en nummerserie, velger du formatet i listen og klikker deretter Fjern omfang fra format.     Hvis du vil utelukke en nummerserie fra automatisk generering, velger du nummerserien i listen og klikker deretter Slett.  
4. Klikk Neste.
5. Klikk Finish.

