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
ms.openlocfilehash: dfdffc1ff0e0541cfad5669d0787abfafbd424ddf0807c61b957e7f330f21af7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717322"
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
