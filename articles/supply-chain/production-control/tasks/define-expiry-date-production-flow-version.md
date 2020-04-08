---
title: Angi en utløpsdato for en produksjonsflytversjon
description: For å avslutte gyldigheten og behandlingen av en produksjonsflytversjon på en gitt dato, eller planlegge erstatning av en aktiv versjon med en ny versjon, må du angi en utløpsdato for versjonen.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d8df396abc3ac4a2c3920e6bf2b21d8a4463df2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146865"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>Angi en utløpsdato for en produksjonsflytversjon

[!include [banner](../../includes/banner.md)]

For å avslutte gyldigheten og behandlingen av en produksjonsflytversjon på en gitt dato, eller planlegge erstatning av en aktiv versjon med en ny versjon, må du angi en utløpsdato for versjonen. Det er ikke nødvendig å deaktivere versjonen.


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>Angi en utløpsdato for å avslutte en produksjonsflytversjon
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Finn og velg ønsket post i listen.
    * Velg en produksjonsflyt som har en versjon som allerede er definert.  
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Rediger.
5. Merk den valgte raden i listen.
6. Angi dato og klokkeslett i feltet Utløpsdato.
    * For utløpsdatoen, vil ikke en ny versjon starte eller bli aktivert. Det vil heller ikke lenger være mulig å opprette eller starte jobber for denne produksjonsflyten. Du kan fortsatt fullføre startede jobber etter utløpsdatoen.  

