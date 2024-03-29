---
title: Deaktivere en produksjonsflytversjon
description: Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1691dc644e2e191a9e74980784d6dcf741dcd598
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576766"
---
# <a name="deactivate-a-production-flow-version"></a>Deaktivere en produksjonsflytversjon

[!include [banner](../../includes/banner.md)]

Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres. Du bør bare bruke dette alternativet hvis alle Kanban-regler og aktiviteter er avsluttet og ikke skal aktiveres igjen. Vær oppmerksom på at utløpsdatoen for alle Kanban-regler som er knyttet til denne produksjonsflytversjonen, vil bli oppdatert med gjeldende dato og klokkeslett. 

Hvis du vil endre en aktiv produksjonsflytversjon, bør du vurdere å angi en utløpsdato for den aktive versjonen og opprette en ny versjon. Dette gjør at du kan fortsette produksjonsoperasjonene mens den nye versjonen og relaterte Kanban-regler klargjøres. 

Du må angi en utløpsdato for å utløpe en aktiv produksjonsflytversjon. I den forstand er deaktivering mer et unntak enn en regel. 

Til denne prosedyren trenger du en produksjonsflyt med en versjon som kan deaktiveres. Ikke prøv dette i et produksjonsmiljø med mindre du er 100% sikker på at versjonen er fullstendig utdatert.


## <a name="deactivate-a-production-flow-version"></a>Deaktivere en produksjonsflytversjon
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.
4. Finn og velg ønsket post i listen.
5. Klikk på Deaktiver.
    * Ikke fortsett hvis du ikke er 100 % sikker på at denne produksjonsflytversjonen er foreldet. Når du klikker OK, utløper alle aktive Kanban-regler og alle produksjons- og etterfyllingsaktiviteter for denne produksjonsflytversjonen opphører umiddelbart.  
6. Klikk på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]