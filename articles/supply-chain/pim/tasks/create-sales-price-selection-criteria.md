---
title: Opprette valgkriterier for salgspris
description: Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84cef2cbf6f9783f0629fe068a4779a99dca9711
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258596"
---
# <a name="create-sales-price-selection-criteria"></a>Opprette valgkriterier for salgspris

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller. Denne prosedyren krever at minst én salgsprismodell er tilgjengelig. Dette eksemplet bruker prismodellen for salgsprismodellen for høyttalerløsningen i demonstrasjonsdatafirmaet USMF. Produktsjefen bruker vanligvis denne fremgangsmåten.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Legge til et nytt kriterium for en eksisterende salgsprismodell
1. Klikk på Definisjon av produktvariantmodell.
2. Klikk på Produktkonfigurasjonsmodeller.
3. I listen velger du raden for produktmodellen for høyttalerløsningen, men ikke klikk koblingen for modellnavnet.
4. Klikk på Modell i handlingsruten.
5. Klikk på Prismodellkriterier.
6. Klikk på Ny.
7. I Navn-feltet skriver du inn Kundegruppe 10.
    * Navnet på prismodellkriteriet brukes til å identifisere de underliggende valgkriteriene.  
8. Angi eller velg en verdi i feltet Prismodell.
9. Velg Salgsordre i feltet Ordretype.
    * Ordretypen bestemmer databasefeltene som vil være tilgjengelige for valgspørringen.  
10. Angi en dato i Gyldig fra-feltet.
11. Angi en dato i Utløp innen-feltet.
12. Klikk på Lagre.

## <a name="create-the-query-for-the-selection-criteria"></a>Opprette spørringen for valgkriteriene
1. Klikk på Rediger.
2. Velg Kunder i feltet Tabell. 
3. Velg Kundegruppe i Felt-feltet.
    * I dette eksemplet bruker vi en spesifikk kundegruppe for valgkriteriene.  
4. Velg Kundegruppe 10 i Kriterier-feltet. 
5. Klikk på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]