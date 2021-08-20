---
title: Arbeidere som er ansvarlige for å godkjenne avvik
description: Dette emnet beskriver hvordan du konfigurerer arbeidere som er ansvarlige for godkjenning av avvik.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b764baf0983dbca75d52ea9cdd063cebda80a08d39cf3a5c929f15858e2597c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768173"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Arbeidere som er ansvarlige for å godkjenne avvik

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer arbeidere som er ansvarlige for godkjenning av avvik.

Avvik må godkjennes før brukere kan begynne å angi detaljer som rettelser eller operasjoner. Før brukere kan godkjenne eller avvise avvik, må bruker-IDen (brukerposten) være knyttet til en arbeiderpost. Du kan velge å konfigurere arbeidere som er ansvarlige for kvalitet, og deretter tillate at én arbeider godkjenner arbeid på vegne av en annen arbeider.

## <a name="enable-a-user-for-nonconformance-processing"></a>Aktivere en bruker for behandling av avvik

Før en bruker kan godkjenne eller avvise avvik, må du knytte brukerposten til en arbeiderpost. Godkjenningsfeltene kan deretter angis automatisk, og gjeldende bruker kan fylles ut automatisk for timeregistreringen. Før brukeren kan bruke merknader i dokumentet, må du også aktivere dokumenthåndtering i brukeralternativene deres.

1. Gå til **Systemadministrasjon \> Brukere \> Brukere**.
1. Finn og åpne brukeren som skal kunne godkjenne eller avvise avvik.
1. Sett **Person**-feltet til navnet på arbeideren som er knyttet til den gjeldende brukerposten.
1. Velg **Brukeralternativer** i handlingsruten.
1. På **Alternativer**-siden for den gjeldende brukerposten, i kategorien **Innstillinger**, setter du alternativet **Aktiver dokumentbehandling** til *Ja*.
1. Lukk sidene.

## <a name="define-workers-that-are-responsible-for-quality"></a>Definere arbeidere som er ansvarlige for kvalitet

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Arbeidere som er ansvarlige for kvalitet**.
2. Velg **Ny** i handlingsruten.
3. Velg arbeideren som angir kvalitetsdata, i **Arbeider**-feltet.
4. I feltet **Ansvarlig arbeider** velger du arbeideren som den valgte arbeideren angir arbeid på vegne av. Når avvikene opprettes og oppdateres, angis denne arbeideren som standard i **Arbeider**-felt.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](enable-quality-management.md)
- [Kvalitetsstyringstillegg](quality-charges.md)
- [Karantenesoner for avvik](quality-quarantine-zones.md)
- [Diagnosetyper for avvik](quality-diagnostic-types.md)
- [Kvalitetsendringer for avvik](quality-charges.md)
- [Operasjoner for avvik](quality-operations.md)
- [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
