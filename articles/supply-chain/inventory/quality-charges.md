---
title: Tillegg for avviksoperasjoner
description: Dette emnet beskriver hvordan du oppretter kvalitetsgebyrer som kan brukes sammen med operasjoner for et avvik.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956772"
---
# <a name="charges-for-nonconformance-operations"></a>Tillegg for avviksoperasjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter kvalitetsgebyrer som kan brukes sammen med operasjoner for et avvik.

Du bruker siden **Kvalitetsstyringstillegg** til å definere typene tillegg som kan legges til i operasjoner for et avvik. Med tillegg kan du spore detaljer om gebyrer eller tillegg som du skylder en kunde for produkter med avvik, eller som en leverandør skylder deg for produkter med avvik som du har mottatt. Du kan også bruke tillegg til å spore kostnader som kreves for at eksterne leverandører eller tjenester kan utføre en operasjon.

## <a name="examples-of-quality-charges"></a>Eksempler på kvalitetsgebyrer

Du jobber for et produksjonsfirma. Firmaet har kontrakter med flere leverandører. Disse kontraktene beskriver standarder for forsendelser i tide, skader og produktkvalitet for varer. På samme måte har flere av kundene dine avtaler med firmaet om returer, skade og produktkvalitet.

Det defineres og angis en gebyrstruktur for hvert tilfelle i kontrakten. Du kan konfigurere kvalitetstillegg for å vise de ulike typene tillegg, for eksempel *Skader*, *Forsinket levering* og *Kvalitet*. Når du deretter oppretter et avvik, legger du til én eller flere operasjoner. For hver operasjon velger du **Tillegg** for å definere detaljene for gebyrene.

## <a name="create-a-quality-charge"></a>Opprette et kvalitetstillegg

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Kvalitetsstyringstillegg**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Tilleggskode** – Angi en unik ID eller et navn for kvalitetstillegget.
    - **Beskrivelse** – Angi en detaljert beskrivelse av kvalitetstillegget.

1. Lukk siden.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>Legge til et kvalitetstillegg i en operasjon for et avvik

Hvis du vil ha mer informasjon om hvordan du legger til operasjoner i et avvik og beregner tillegg for dem, kan du se [Operasjoner for avvik](quality-operations.md).

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](enable-quality-management.md)
- [Arbeidere som er ansvarlige for å godkjenne avvik](quality-responsible-workers.md)
- [Karantenesoner for avvik](quality-quarantine-zones.md)
- [Diagnosetyper for avvik](quality-diagnostic-types.md)
- [Kvalitetsendringer for avvik](quality-charges.md)
- [Operasjoner for avvik](quality-operations.md)
- [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
