---
title: Suspendere permisjon
description: Du kan suspendere en permisjon for en ansatt i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c8262fb34175f6f9326d6be82c922b2170fc5a7
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805267"
---
# <a name="suspend-leave"></a>Suspender permisjon

>[!Important]
>Funksjonaliteten som er nevnt i denne artikkelen, er for øyeblikket tilgjengelig for kunder i frittstående Dynamics 365 Human Resources. Noe av eller all funksjonaliteten vil være tilgjengelig som en del av en fremtidig versjon av Finance-infrastrukturen etter Finance versjon 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan suspendere en permisjon for en ansatt for å stoppe permisjonsavsetninger fra å bli behandlet for utvalgte permisjonstyper.

## <a name="suspend-leave-and-absence-for-an-employee"></a>Suspendere permisjon og fravær for en ansatt

1. Velg **Permisjon** i posten for den ansatte.

2. Velg **Suspender permisjon**.

3. Velg **Ny**.

4. I dialogboksen **Suspender permisjonsavsetning** velger du **Permisjonstype** sammen med **Startdato** og **Sluttdato** for suspensjonen.

5. Du kan også legge til en **Kommentar** for suspensjonen. 

Hvis avsetninger behandles når den ansattes permisjoner blir suspendert, vil det ikke bli utført noen avsetning for permisjonstypene.

> [!NOTE]
> Permisjonsforespørsler suspenderer fritidsforespørsler, men fritidsforespørsler vil ikke suspendere permisjonsforespørsler.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)
- [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md)
- [Avsette permisjons- og fraværsplaner](hr-leave-and-absence-accrue.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
