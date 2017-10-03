--- 
title: Opprette valgkriterier for salgspris
description: "Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 633628e6250baa74df544e814ce6e9656a2f0b06
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-price-selection-criteria"></a>Opprette valgkriterier for salgspris

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller. Denne prosedyren krever at minst én salgsprismodell er tilgjengelig. Dette eksemplet bruker prismodellen for salgsprismodellen for høyttalerløsningen i demonstrasjonsdatafirmaet USMF. Produktsjefen bruker vanligvis denne fremgangsmåten.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Legge til et nytt kriterium for en eksisterende salgsprismodell
1. Klikk Definisjon av produktvariantmodell.
2. Klikk Produktkonfigurasjonsmodeller.
3. I listen velger du raden for produktmodellen for høyttalerløsningen, men ikke klikk koblingen for modellnavnet.
4. Klikk Modell i handlingsruten.
5. Klikk Prismodellkriterier.
6. Klikk Ny.
7. I Navn-feltet skriver du inn Kundegruppe 10.
    * Navnet på prismodellkriteriet brukes til å identifisere de underliggende valgkriteriene.  
8. Angi eller velg en verdi i feltet Prismodell.
9. Velg Salgsordre i feltet Ordretype.
    * Ordretypen bestemmer databasefeltene som vil være tilgjengelige for valgspørringen.  
10. Angi en dato i Gyldig fra-feltet.
11. Angi en dato i Utløp innen-feltet.
12. Klikk Lagre.

## <a name="create-the-query-for-the-selection-criteria"></a>Opprette spørringen for valgkriteriene
1. Klikk Rediger.
2. Velg Kunder i feltet Tabell. 
3. Velg Kundegruppe i Felt-feltet.
    * I dette eksemplet bruker vi en spesifikk kundegruppe for valgkriteriene.  
4. Velg Kundegruppe 10 i Kriterier-feltet. 
5. Klikk OK.


