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
ms.openlocfilehash: 76dc32f2254ffd2a2e33eef594d6e602092bcb6f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140510"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>Konfigurere alle nødvendige nummerserier ved hjelp av en veiviser

[!include [banner](../../includes/banner.md)]

Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem. En hoveddata- eller transaksjonspost som krever en ID kalles en referanse. Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse. Dette emnet beskriver hvordan du definerer alle nødvendige nummerserier samtidig ved å bruke en veiviser. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til **Navigasjon > Moduler > Organisasjonsadministrasjon > Nummerserier > Nummerserier**.
2. Velg **Generer**.
3. Velg **Neste**.

   - På denne siden kan du endre ID-koden, den laveste verdien og den høyeste verdien. Du kan i tillegg angi om nummerserien må være sammenhengende.   
   - Ikke velg **Fortløpende**-alternativet hvis du må forhåndstildele numre for nummerserien. Hvis du vil legge til et omfangssegment for formatet for en nummerserie, velger du formatet i listen og velger deretter **Ta med omfang i format**. Hvis du vil fjerne et omfangssegment fra formatet for en nummerserie, velger du formatet i listen og velger deretter **Fjern omfang fra format**. Hvis du vil utelukke en nummerserie fra automatisk generering, velger du nummerserien i listen og velger deretter **Slett**.  

4. Velg **Neste**.
5. Velg **Fullfør**.

