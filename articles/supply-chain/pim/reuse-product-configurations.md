---
title: Gjenbruk av produktkonfigurasjoner
description: "Du kan angi at du vil bruke en eksisterende konfigurasjon for et produkt på nytt automatisk. Deretter, når en bruker har fullført en konfigurasjonsøkt, kontrollerer systemet om det allerede finnes en konfigurasjon som tilsvarer brukerens valg. Hvis en tilsvarende konfigurasjon blir funnet, brukes konfigurasjons-IDen, den tilsvarende stykklisten og ruten på nytt."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: c447440c33c1f80c6056974086b90d3b43e8499e
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---

# <a name="reuse-product-configurations"></a>Gjenbruk av produktkonfigurasjoner

[!include [banner](../includes/banner.md)]

Du kan angi at du vil bruke en eksisterende konfigurasjon for et produkt på nytt automatisk. Deretter, når en bruker har fullført en konfigurasjonsøkt, kontrollerer systemet om det allerede finnes en konfigurasjon som tilsvarer brukerens valg. Hvis en tilsvarende konfigurasjon blir funnet, brukes konfigurasjons-IDen, den tilsvarende stykklisten og ruten på nytt.

<a name="requirements-for-reusing-configurations"></a>Krav for gjenbruk av konfigurasjoner
---------------------------------------

Hvis du vil muliggjøre gjenbruk av konfigurasjoner, må du angi følgende informasjon for komponentene og attributtene på siden **Detaljer om produktkonfigurasjonsmodell**:

-   **Komponenter og delkomponenter** – I hurtigfanen **Generelt**, i feltet **Bruk konfigurasjoner på nytt**, velger du **Ja**.
-   **Attributter** – I hurtigfanen **Attributter** velger du alternativet **Ta med i gjenbruk**. Dette alternativet vises bare når den tilknyttede komponenten er aktivert for gjenbruk. Hvis du ikke velger noen attributter for gjenbruk, brukes konfigurasjonen alltid på nytt, uavhengig av brukerens valg under en konfigurasjonsøkt. Attributtverdier i den eksisterende konfigurasjonen må samsvare med brukerens valg. Hvis brukeren for eksempel velger **Blå** som fargen under en konfigurasjonsøkt, kontrollerer systemet om en eksisterende konfigurasjon av komponenten har fargen blå.

## <a name="resetting-configuration-reuse"></a>Tilbakestilling av gjenbruk av konfigurasjon
Når du tilbakestiller gjenbruk av konfigurasjon, tas det ikke lenger hensyn til tidligere opprettede konfigurasjoner. Du bør tilbakestille gjenbruk av konfigurasjon hvis stykklisten eller ruten ble endret, men ingen attributter ble endret. Du tilbakestiller gjenbruk av konfigurasjon for hurtigfanen **Generelt** for komponenten.




