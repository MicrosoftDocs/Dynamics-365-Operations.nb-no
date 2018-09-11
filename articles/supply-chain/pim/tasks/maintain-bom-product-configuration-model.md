--- 
title: Vedlikeholde stykkliste for en produktkonfigurasjonsmodell
description: "Kjører du denne prosedyren krever det en eksisterende produktmodellkonfigurasjon."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c017d7719ac6af43b0c8a162080bb753587df030
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Vedlikeholde stykkliste for en produktkonfigurasjonsmodell

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kjører du denne prosedyren krever det en eksisterende produktmodellkonfigurasjon. Modellen for High-end-høyttaler i demofirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="add-a-bom-line"></a>Legge til en stykklistelinje
1. Klikk Definisjon av produktvariantmodell.
2. Klikk Produktkonfigurasjonsmodeller.
3. Finn og velg ønsket post i listen.
    * Velg High-end-høyttaleren for denne prosedyren.  
4. Klikk koblingen i den valgte raden i listen.
5. Utvid delen Stykklistelinjer.
6. Klikk Legg til.
7. Skriv inn en verdi i Navn-feltet.
8. Skriv inn en verdi i feltet Beskrivelse.
9. Klikk Lagre.

## <a name="add-bom-line-details"></a>Legge til detaljer om stykklistelinje
1. Klikk Detaljer om stykklistelinje.
2. Angi eller velg en verdi i Varenummer-feltet.
    * Du kan for eksempel velge varen M0055.  
    * For hver Stykklistelinjeegenskap kan du velge om den tar en fast verdi eller er tilordnet til et attributt.  
3. Merk av for Sett.
4. Velg Ja i feltet Beregning.
    * Når du setter Beregning-egenskapen til Ja, sikrer du at stykklistelinjen er inkludert i kostnadsberegning.  
5. Klikk kategorien Oppsett.
6. Merk av for Sett.
7. Angi et tall i feltet Antall.
    * Antall-feltet bestemmer hvor mye av varen som inngår i stykklisten. Dette kan være en opplagt kandidat for en attributtilordning.  
8. Klikk kategorien Dimensjon.
    * Verifiser om noen av produktdimensjonene er aktive, og derfor må ha en verdi eller et attributt tilordnet.  
9. Klikk OK.


