---
title: Diagnosetyper for avvik
description: Dette emnet beskriver hvordan du bruker og oppretter diagnosetyper som kan brukes med avvik.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022282"
---
# <a name="diagnostic-types-for-nonconformances"></a>Diagnosetyper for avvik

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du bruker og oppretter diagnosetyper som kan brukes med avvik.

Du bruker **Diagnosetyper**-siden til å definere en klassifisering av diagnosehandlinger. Når du deretter oppretter en korrigering for et avvik, velger du en diagnose. En rettelse angir hvilken type diagnosehandling som skal utføres for et godkjent avvik, og hvem som skal utføre denne handlingen. Den angir også den ønskede fullføringsdatoen og den planlagte fullføringsdatoen.

## <a name="examples-of-diagnostic-types"></a>Eksempler på diagnosetyper

Du jobber for et produksjonsfirma, og flere varer har mislykkede kvalitetstester. Disse varene flyttes inn i et karanteneområde og merkes som produkter med avvik. En avvikspost opprettes i Microsoft Dynamics 365 Supply Chain Management for å spore detaljene ved hjelp av problemløsning.

I dette tilfellet oppstår kvalitetsproblemene fordi lagre i maskinen som pakker varene har blitt overopphetet. Løsningen på dette problemet er å erstatte delene i maskinen.

Når du konfigurerer diagnosetypene, kan du opprette flere poster, som hver representerer en forskjellig type problem som maskinen kan ha. Du kan også opprette en generisk diagnosetype som representerer maskinreparasjon.

## <a name="create-a-diagnostic-type"></a>Opprette en diagnosetype

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Diagnosetyper**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Diagnose** – Angi en unik identifikator eller et unikt navn for diagnosetypen.
    - **Beskrivelse** – Angi en detaljert beskrivelse av diagnosetypen.

1. Lukk siden.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](enable-quality-management.md)
- [Arbeidere som er ansvarlige for å godkjenne avvik](quality-responsible-workers.md)
- [Karantenesoner for avvik](quality-quarantine-zones.md)
- [Problemtyper for avvik](quality-problem-types.md)
- [Kvalitetsendringer for avvik](quality-charges.md)
- [Operasjoner for avvik](quality-operations.md)
- [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
