--- 
title: Definere attributtbasert prissetting for konfigurerbare produkter
description: Denne prosedyren viser hvordan du setter opp attributtbasert prising.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 88402bef6fd5dad38a74795cd31a4046085d6db7
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Definere attributtbasert prissetting for konfigurerbare produkter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du setter opp attributtbasert prising. Det er en forutsetning at du har en produktkonfigurasjonsmodell som har én eller flere komponenter og attributter. Dette eksemplet bruker produktmodellen for High-end-høyttaler i demonstrasjonsdatafirmaet USMF. Produktsjefen bruker vanligvis denne fremgangsmåten.


## <a name="create-a-new-price-model"></a>Opprette en ny prismodell
1. Klikk Definisjon av produktvariantmodell.
2. Klikk Produktkonfigurasjonsmodeller.
3. I listen velger du linjen med High-end-høyttaler, men ikke klikk koblingen for navnet.
4. Klikk Modell i handlingsruten.
5. Klikk Prismodeller.
6. Klikk Ny.
7. Skriv inn en verdi i feltet Prismodellnavn.
    * Bruk et navn som gjør det enkelt å identifisere modellen.  
8. Skriv inn en verdi i feltet Beskrivelse.
9. Klikk Lagre.

## <a name="add-price-elements"></a>Legge til priselementer
1. Klikk Rediger.
    * Hver komponent i en produktmodell kan ha et basispriselement og et hvilket som helst antall prisuttrykksregler. Du kan også legge til priser i ulike valutaer.  
2. Skriv inn en verdi i feltet Basisprisuttrykk.
    * Skriv for eksempel 100.   Et basisprisuttrykk kan være en numerisk verdi, eller det kan bestå av den aritmetiske beregningen som omfatter ett eller flere attributter.  
3. Klikk Legg til.
4. I Navn-feltet skriver du inn Rosewood.
    * Prisuttrykksnavnet identifiserer hva priselementet representerer. I dette eksemplet oppretter vi et priselement for alternativet høyttalerkabinett med Rosewood-finish.  
5. Klikk Rediger betingelse.
    * En prisbetingelse bidrar til å garantere at prisuttrykkselementet er inkludert i salgsprisen bare hvis det finnes en bestemt kombinasjon av attributter.  
6. I ConstraintBody-feltet skriver du inn CabinetFinish=="Rosewood".
7. Klikk OK.
8. Skriv inn en verdi i feltet Uttrykk.
    * Skriv for eksempel 50.  
9. Lukk siden.
10. Lukk siden.


