---
title: Opprette valgkriterier for salgspris
description: Denne fremgangsmåten viser hvordan du oppretter et valgkriterium for salgspris for attributtbaserte salgsprismodeller.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568453"
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