---
title: Konfigurere alle nødvendige nummerserier ved hjelp av en veiviser
description: Dette emnet beskriver hvordan du definerer alle nødvendige nummerserier samtidig ved å bruke en veiviser.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
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
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179301"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>Konfigurere alle nødvendige nummerserier ved hjelp av en veiviser

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem. En hoveddata- eller transaksjonspost som krever en ID kalles en referanse. Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse. Dette emnet beskriver hvordan du definerer alle nødvendige nummerserier samtidig ved å bruke en veiviser. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til **Navigasjon > Moduler > Organisasjonsadministrasjon > Nummerserier > Nummerserier**.
2. Velg **Generer**.
3. Velg **Neste**.

   - På denne siden kan du endre ID-koden, den laveste verdien og den høyeste verdien. Du kan i tillegg angi om nummerserien må være sammenhengende.   
   - Ikke velg **Fortløpende**-alternativet hvis du må forhåndstildele numre for nummerserien. Hvis du vil legge til et omfangssegment for formatet for en nummerserie, velger du formatet i listen og velger deretter **Ta med omfang i format**. Hvis du vil fjerne et omfangssegment fra formatet for en nummerserie, velger du formatet i listen og velger deretter **Fjern omfang fra format**. Hvis du vil utelukke en nummerserie fra automatisk generering, velger du nummerserien i listen og velger deretter **Slett**.  

4. Velg **Neste**.
5. Velg **Fullfør**.

