---
title: Vedlikeholde stykkliste for en produktkonfigurasjonsmodell
description: Kjører du denne prosedyren krever det en eksisterende produktmodellkonfigurasjon.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577294"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Vedlikeholde stykkliste for en produktkonfigurasjonsmodell

[!include [banner](../../includes/banner.md)]

Kjører du denne prosedyren krever det en eksisterende produktmodellkonfigurasjon. Modellen for High-end-høyttaler i demofirmaet USMF brukes til å opprette denne fremgangsmåten.

## <a name="add-a-bom-line"></a>Legge til en stykklistelinje

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.
1. Finn og velg ønsket post i listen.
    * Velg High-end-høyttaleren for denne prosedyren.  
1. Velg koblingen i den valgte raden i listen.
1. Utvid delen **Stykklistelinjer**.
1. Velg **Legg til**.
1. Skriv inn en verdi i **Navn**-feltet.
1. Skriv inn en verdi i **Beskrivelse**-feltet.
1. Velg **Lagre**.

## <a name="add-bom-line-details"></a>Legge til detaljer om stykklistelinje

1. Velg **Stykklistelinjedetaljer**.
2. Angi eller velg en verdi i **Varenummer**-feltet.
    * Du kan for eksempel velge varen M0055.  
    * For hver Stykklistelinjeegenskap kan du velge om den tar en fast verdi eller er tilordnet til et attributt.  
3. Merk av for **Sett**.
4. Velg *Ja* i feltet **Beregning**.
    * Når du setter **Beregning**-egenskapen til *Ja*, sikrer du at stykklistelinjen er inkludert i kostnadsberegning.  
5. Velg **Oppsett**-fanen.
6. Merk av for **Sett**.
7. Angi et tall i **Antall**-feltet.
    * Antall-feltet bestemmer hvor mye av varen som inngår i stykklisten. Dette kan være en opplagt kandidat for en attributtilordning.  
8. Velg fanen **Dimensjon**.
    * Verifiser om noen av produktdimensjonene er aktive, og derfor må ha en verdi eller et attributt tilordnet.  
9. Velg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]