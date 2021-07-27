---
title: Parametere for lønnsintegrering
description: Dette emnet beskriver parameterne for lønnsintegrering i Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f76ce395d7f5a82ab622dd323aee52a39b09847
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314460"
---
# <a name="payroll-integration-parameters"></a>Parametere for lønnsintegrering

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Før du bruker Dynamics 365 Human Resources lønnsintegrering, må du definere parameterne som er beskrevet i dette emnet.

## <a name="enable-payroll-address"></a>Aktivere lønnsadresse

Hvis du vil bruke lønnsadressen, må du aktivere den fra de [delte parameterskjemaene](hr-setup-shared-parameters.md) i kategorien lønnsintegrering.

## <a name="define-the-identification-type"></a>Definere identifikasjonstypen

Hvis du vil vise identifikasjonstype-IDen i [lønnsansattenheten](hr-admin-integration-payroll-api-payroll-employee.md), må du konfigurere [parametere for Human Resources](hr-setup-shared-parameters.md) for hvert firma.

1. I arbeidsområdet **Kompensasjonsstyring**, under koblinger, velger du **Parametere for Human Resources**. 
2. Angi verdien for følgende felt i kategorien **Lønnsintegrering**.

| Felt | beskrivelse |
| --- | --- |
| Bruk identifikasjonstyper i lønnsbehandling | Når dette alternativet er valgt, vises den valgte type-IDen i lønnsansattenheten. |
| Identifikasjonstype | Identifikasjonstypen som vises i feltet **mshr_payrollemployeeentityid** i [lønnsansattenheten](hr-admin-integration-payroll-api-payroll-employee.md) |

## <a name="see-also"></a>Se også

[Innføring i API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
