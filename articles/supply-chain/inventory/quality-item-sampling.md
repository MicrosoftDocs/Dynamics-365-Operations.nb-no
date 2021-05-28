---
title: Vareprøve for kvalitetsstyring
description: Dette emnet beskriver hvordan du setter opp vareprøver.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022234"
---
# <a name="quality-management-item-sampling"></a>Vareprøve for kvalitetsstyring

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
