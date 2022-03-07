---
title: Deaktivere en produksjonsflytversjon
description: Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0664dd40464000abef0041ef32863a3c9494d9b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975141"
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

