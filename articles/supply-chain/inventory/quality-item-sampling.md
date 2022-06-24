---
title: Vareprøve for kvalitetsstyring
description: Denne artikkelen beskriver hvordan du setter opp vareprøver.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 644eae4fbd9f82027c1cb69efba00dc893f8fc66
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865157"
---
# <a name="quality-management-item-sampling"></a>Vareprøve for kvalitetsstyring

[!include [banner](../includes/banner.md)]

Vareprøve brukes som del av en kvalitetskontroll. Den definerer mengden gjeldende fysisk lager som må kontrolleres. Prøver kan være basert på faste antall, en prosentdel, eller et fullstendig nummerskilt.

## <a name="set-up-item-sampling"></a>Definere vareprøver

Gjør følgende for å konfigurere vareprøve.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Vareprøve**.
1. Velg **Ny**.
1. Skriv inn en verdi i **Vareprøve**-feltet.
1. Angi en verdi i feltet **Beskrivelse**.
1. Angi et tall i **Verdi**-feltet. Denne verdien er knyttet til spesifikasjonen av antall som er valgt i feltet ved siden av.
1. I **Prosess**-delen merker du av for **Full blokkering** hvis hele partiet eller ordrelinjeantallet skal blokkeres hvis en test mislykkes. Hvis du fjerner merket i boksen, blokkeres bare varene i kvalitetsordren hvis en test mislykkes.
1. Velg **Lagre**.
1. Lukk siden.

> [!NOTE]
> Funksjonen *Kvalitetsstyring for lagerprosesser* gir flere vareprøvefunksjoner. Den legger til begrepet *vareprøveområde* og muligheten til å definere et fullstendig nummerskilt som spesifikasjon av antall. Hvis du har aktivert denne funksjonen, se [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
