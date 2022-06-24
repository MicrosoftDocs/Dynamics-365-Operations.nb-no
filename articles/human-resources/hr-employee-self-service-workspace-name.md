---
title: Endre navn på arbeidsområde for selvbetjening for ansatte
description: Denne artikkelen beskriver hvordan du endrer visningsnavnet for arbeidsområdet for selvbetjening for ansatte i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8f0ee9981d1c02e0fb114976955d406ba74afb0a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886138"
---
# <a name="change-employee-self-service-workspace-name"></a>Endre navn på arbeidsområde for selvbetjening for ansatte


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Hvis du har frivillige eller andre ikke-ansatte, kan det hende du vil endre navnet på arbeidsområdet **Ansattselvbetjening**. I stedet kan du endre dette arbeidsområdet til **Selvbetjening**.

> [!NOTE]
> Hvis du endrer navnet på arbeidsområdet **Ansattselvbetjening**, endres også menyelementet som brukes internt av Dynamics 365 Human Resources. Hvis du tidligere har brukt sikkerhetstilpassinger på menyelementet **HcmEmployeeSelfServiceWorkspace**, anbefaler vi at du bruker de samme endringene på **HcmSelfServiceWorkspace** for å opprettholde paritet.

1. I Human Resources velger du **Personaladministrasjon**, **Koblinger** og deretter **Personalparametere**.

2. Velg kategorien **Ansattselvbetjening**.

3. Under **Visningsnavn** velger du **Selvbetjening**.

   ![Endre navn på arbeidsområde for selvbetjening til Selvbetjening.](./media/hr-employee-self-service-workspace-name.png)

4. Velg **Lagre**.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over selvbetjening for ansatte og ledere](hr-employee-manager-self-service-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
