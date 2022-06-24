---
title: Objektprioritet
description: Denne artikkelen beskriver tjenestenivåer for aktiva i Aktivastyring.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7429b30253f540925e67ff9239667a0a404f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908692"
---
# <a name="asset-service-levels"></a>Objektprioritet

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen beskriver tjenestenivåer for aktiva i Aktivastyring. Tjenestenivåer for aktiva er knyttet til aktiva og overføres til meldinger og arbeidsordrer. De brukes til å beregne prioriteten for arbeidsordrer under planlegging av arbeidsordrer. Servicenivåer for aktiva kan endres hvis det er nødvendig med endringer.

Hvis du vil ha mer informasjon om oppsettet som er knyttet til beregning av poengsummer for arbeidsordreplanlegging, kan du se [Parametere i Aktivastyring](../setup-for-objects/enterprise-asset-management-parameters.md). Du må definere minst én standardpost for servicenivået for aktivumet. Denne standardposten brukes hvis ingen andre treff blir funnet under planleggingen av arbeidsordren.

**Eksempel 1:** Standard tjenestenivå som brukes hvis ingen andre treff blir funnet. I denne oppføringen velger du bare et tjenestenivå.

**Eksempel 2:** Et høyt servicenivå som brukes til å planlegge jobber for en Volvo-lastebilmotor. I denne oppføringen velger du en relevant aktivatype (for eksempel **Lastebilmotor**), en produsent (**Volvo**) og et servicenivå.

## <a name="set-up-asset-service-levels"></a>Definere tjenestenivåer for aktiva

1. Velg **Aktivastyring** \> **Oppset** \> **Tjenestenivåer for aktiva**.
2. Velg **Ny** for å opprette en oppføring.
3. Avhengig av detaljnivået som kreves for tjenestenivået for aktiva, kan du foreta relevante valg i feltene **Arbeidssted**, **Aktivatype**, **Produsent**, **Modell**, **Aktivum**, **Arbeidsordretype** og **Tjenestenivå**.

    > [!NOTE]
    > Når servicenivået for aktiva brukes til meldinger og arbeidsordrer, går Aktivastyring gjennom alle poster på servicenivå for aktiva for å kontrollere om det finnes et mulig samsvar. Den kontrollerer alltid den mest spesifikke kombinasjonen først. Med andre ord ser Aktivastyring først etter et treff i **Arbeidsordretype**-feltet. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Aktivum**-feltet, og så videre. Som du kan se i oppsettet av siden **Tjenestenivåer for aktiva**, betyr dette at for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff. Hvis det ikke blir funnet noen treff, brukes standardoppføringen, der det ikke er noen valg i disse feltene.

4. I feltet **Servicenivå** velger du et tall som angir servicenivået (prioriteten).


> [!NOTE]
> Hvis du endrer en post for servicenivå for aktiva på siden **Servicenivåer for aktiva** etter at du allerede har brukt den på en arbeidsordre, oppdateres ikke servicenivået på meldinger og arbeidsordrer i henhold til dette.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]