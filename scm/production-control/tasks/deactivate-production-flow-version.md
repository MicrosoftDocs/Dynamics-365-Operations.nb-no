--- 
title: Deaktivere en produksjonsflytversjon
description: "Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 06daa5e7d2b8e88bca281dc9bcaa73927253553c
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="deactivate-a-production-flow-version"></a>Deaktivere en produksjonsflytversjon

[!include[task guide banner](../../includes/task-guide-banner.md)]

Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres. Du bør bare bruke dette alternativet hvis alle Kanban-regler og aktiviteter er avsluttet og ikke skal aktiveres igjen. Vær oppmerksom på at utløpsdatoen for alle Kanban-regler som er knyttet til denne produksjonsflytversjonen, vil bli oppdatert med gjeldende dato og klokkeslett. 

Hvis du vil endre en aktiv produksjonsflytversjon, bør du vurdere å angi en utløpsdato for den aktive versjonen og opprette en ny versjon. Dette gjør at du kan fortsette produksjonsoperasjonene mens den nye versjonen og relaterte Kanban-regler klargjøres. 

Du må angi en utløpsdato for å utløpe en aktiv produksjonsflytversjon. I den forstand er deaktivering mer et unntak enn en regel. 

Til denne prosedyren trenger du en produksjonsflyt med en versjon som kan deaktiveres. Ikke prøv dette i et produksjonsmiljø med mindre du er 100% sikker på at versjonen er fullstendig utdatert.


## <a name="deactivate-a-production-flow-version"></a>Deaktivere en produksjonsflytversjon
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Finn og velg ønsket post i listen.
5. Klikk Deaktiver.
    * Ikke fortsett hvis du ikke er 100 % sikker på at denne produksjonsflytversjonen er foreldet. Når du klikker OK, utløper alle aktive Kanban-regler og alle produksjons- og etterfyllingsaktiviteter for denne produksjonsflytversjonen opphører umiddelbart.  
6. Klikk OK.

