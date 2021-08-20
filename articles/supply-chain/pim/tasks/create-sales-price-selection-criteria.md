---
title: Opprette valgkriterier for salgspris
description: Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47ea7ea2093c540a88d9fd7249b470009c7595d40e2a727d8fcd3bb4b5d74bac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750082"
---
# <a name="create-sales-price-selection-criteria"></a>Opprette valgkriterier for salgspris

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller. Denne prosedyren krever at minst én salgsprismodell er tilgjengelig. Dette eksemplet bruker prismodellen for salgsprismodellen for høyttalerløsningen i demonstrasjonsdatafirmaet USMF. Produktsjefen bruker vanligvis denne fremgangsmåten.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Legge til et nytt kriterium for en eksisterende salgsprismodell

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.
1. I listen velger du raden for produktmodellen for høyttalerløsningen, men ikke velg koblingen for modellnavnet.
1. Velg **Modell** i handlingsruten.
1. Velg **Prismodellkriterier**.
1. Velg **Ny**.
1. I **Navn**-feltet skriver du inn Kundegruppe 10.
    * Navnet på prismodellkriteriet brukes til å identifisere de underliggende valgkriteriene.  
1. Angi eller velg en verdi i feltet **Prismodell**.
1. Velg **Salgsordre** i feltet *Ordretype*.
    * Ordretypen bestemmer databasefeltene som vil være tilgjengelige for valgspørringen.  
1. Angi en dato i **Gyldig fra**-feltet.
1. Angi en dato i **Utløp innen**-feltet.
1. Velg **Lagre**.

## <a name="create-the-query-for-the-selection-criteria"></a>Opprette spørringen for valgkriteriene

1. Velg **Rediger**.
2. Velg **Kunder** i feltet *Tabell*.
3. Velg **Kundegruppe** i *Felt*-feltet.
    * I dette eksemplet bruker vi en spesifikk kundegruppe for valgkriteriene.  
4. Velg **Kundegruppe 10** i *Kriterier*-feltet.
5. Velg **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]