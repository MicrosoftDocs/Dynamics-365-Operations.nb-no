---
title: Tidsvinduer
description: "Du kan bruke tidsvinduer for å optimalisere planleggingen av serviceordrelinjene."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: b7268870aa9065e4e52d936e819107094bad3663
ms.contentlocale: nb-no
ms.lasthandoff: 02/20/2018

---

# <a name="time-windows"></a>Tidsvinduer  

[!include[banner](../includes/banner.md)]

Du kan bruke tidsvinduer for å optimalisere planleggingen av serviceordrelinjene. Du kan konfigurere systemet slik at serviceordrer opprettes automatisk. Basert på kriteriene som er definert i et tidsvindu, kan du koble til så mange serviceordrelinjer som mulig til så få serviceordrer som mulig.

Tidsvinduer definerer hvor langt en serviceordrelinje kan flyttes fra den beregnede datoen. Den beregnede datoen er datoen som serviceordrelinjen skulle forekomme på. Datoen er basert på intervallinnstillingen og serviceperioden du definerte på **Opprett serviceordrer**-siden. Du definerer et tidsvindu ved hjelp av verdiene i følgende tabell.

| Metode | beskrivelse                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uke   | Datoen som serviceordrelinjen kan flyttes til en hvilken som helst åpen dag i den samme uken som den opprinnelig beregnede datoen.                                                                                                                                                                                    |
| Måned  | Datoen som serviceordrelinjen kan flyttes til en hvilken som helst åpen dag i den samme måneden som den opprinnelig beregnede datoen. Den beregnede datoen for en serviceordrelinje er for eksempel 15. februar 2017. Serviceordrelinjen kan planlegges for en ukedag mellom 1. februar og 28. februar 2017. |
| Manuell | Du kan definere det maksimale antallet dager før eller etter den opprinnelig beregnede datoen som serviceordrelinjen kan flyttes til.                                                                                                                                                                           |

Hvis du ikke angir et tidsvindu for en serviceavtalelinje, må serviceordrelinjen som utledes av serviceavtalelinjen, være på nøyaktig samme dato som den opprinnelig ble planlagt for.

## <a name="related-topics"></a>Relaterte emner

[Opprette tidsvinduer](create-time-windows.md)


