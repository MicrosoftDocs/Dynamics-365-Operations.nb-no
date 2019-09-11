---
title: Definere attributtbasert prissetting for konfigurerbare produkter
description: Dette emnet forklarer hvordan du setter opp attributtbasert prising.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 534e9c9332c107afebd814cf2090ecbdf0ec6459
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914705"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Definere attributtbasert prissetting for konfigurerbare produkter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet forklarer hvordan du setter opp attributtbasert prising. Det er en forutsetning at du har en produktkonfigurasjonsmodell som har én eller flere komponenter og attributter. Dette eksemplet bruker produktmodellen for High-end-høyttaler i demonstrasjonsdatafirmaet USMF. Produktsjefen bruker vanligvis denne fremgangsmåten.


## <a name="create-a-new-price-model"></a>Opprette en ny prismodell
1. Velg **Definisjon av produktvariantmodell** på startsiden.
2. Velg **Produktkonfigurasjonsmodeller** i **koblinger**-delen.
3. I listen velger du linjen med **High-end-høyttaler**, men ikke velg koblingen for navnet.
4. Velg **Modell** i handlingsruten.
5. Velg **Prismodeller**.
6. Velg **Ny**.
7. Skriv inn en verdi i feltet **Prismodellnavn**. Bruk et navn som gjør det enkelt å identifisere modellen.  
8. Skriv inn en verdi i **Beskrivelse**-feltet.
9. Velg **Lagre**.

## <a name="add-price-elements"></a>Legge til priselementer
1. Velg **Rediger**. Hver komponent i en produktmodell kan ha et basispriselement og et hvilket som helst antall prisuttrykksregler. Du kan også legge til priser i ulike valutaer.  
2. Skriv inn en verdi i feltet **Basisprisuttrykk**. Skriv for eksempel 100. Et basisprisuttrykk kan være en numerisk verdi, eller det kan bestå av den aritmetiske beregningen som omfatter ett eller flere attributter.  
3. Velg **Legg til**.
4. I **Navn**-feltet skriver du inn `Rosewood`. Prisuttrykksnavnet identifiserer hva priselementet representerer. I dette eksemplet oppretter vi et priselement for alternativet høyttalerkabinett med Rosewood-finish.  
5. Velg **Rediger betingelse**. En prisbetingelse bidrar til å garantere at prisuttrykkselementet er inkludert i salgsprisen bare hvis det finnes en bestemt kombinasjon av attributter.  
6. I feltet **ConstraintBody** angir du `CabinetFinish=="Rosewood"`.
7. Velg **OK**.
8. Skriv inn en verdi i feltet **Uttrykk**. Skriv for eksempel `50`. 
9. Lukk siden.

