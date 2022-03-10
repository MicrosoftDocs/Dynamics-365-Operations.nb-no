---
title: Definere attributtbasert prissetting for konfigurerbare produkter
description: Dette emnet forklarer hvordan du setter opp attributtbasert prising.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4acd7b423396124dd1059602f5aa6460ec5e259
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578158"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Definere attributtbasert prissetting for konfigurerbare produkter

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du setter opp attributtbasert prising. Det er en forutsetning at du har en produktkonfigurasjonsmodell som har én eller flere komponenter og attributter. Dette eksemplet bruker produktmodellen for High-end-høyttaler i demonstrasjonsdatafirmaet USMF. Produktsjefen bruker vanligvis denne fremgangsmåten.


## <a name="create-a-new-price-model"></a>Opprette en ny prismodell

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.
1. I listen velger du linjen med **High-end-høyttaler**, men ikke velg koblingen for navnet.
1. Velg **Modell** i handlingsruten.
1. Velg **Prismodeller**.
1. Velg **Ny**.
1. Skriv inn en verdi i feltet **Prismodellnavn**. Bruk et navn som gjør det enkelt å identifisere modellen.  
1. Skriv inn en verdi i **Beskrivelse**-feltet.
1. Velg **Lagre**.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]