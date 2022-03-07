---
title: Operasjoner for avvik
description: Dette emnet beskriver hvordan du oppretter og bruker operasjoner for avvik.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6454a56323ea66369696dd6e3310a41b4eb9ee58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956780"
---
# <a name="operations-for-nonconformances"></a>Operasjoner for avvik

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter og bruker operasjoner for avvik.

Du kan bruke **Operasjoner**-siden til å definere klassifiseringer av arbeidet som kan utføres for et godkjent avvik. Når du tilordner en relatert operasjon til et avvik, kan du også gi detaljert informasjon, for eksempel informasjon om tilknyttede materialer, arbeidstimer og tillegg som kreves for å utføre operasjonen. Denne informasjonen brukes til å beregne en estimert kostnad for operasjonen. Den detaljerte informasjonen og de estimerte kostnadene er til referanse. De relaterte operasjonene for kvalitet er annerledes enn operasjonene som kan defineres for en produksjonsrute.

> [!NOTE]
> Selv om du kan spore kostnader, tid og varene som brukes i en operasjon som er relatert til et avvik, er dataene du angir, bare til informasjon. De er ikke automatisk integrert med økonomimodulen, underfinans for beholdning eller **Timeregistrering**-modulen.

## <a name="examples-of-operations"></a>Eksempler på operasjoner

Du jobber for et produksjonsfirma. Et avvik ble opprettet og godkjent for varer som mislyktes i en kvalitetstest. Det ble opprettet en korrigering for å angi at problemet var knyttet til dårlige lagre på en maskin. Det kreves flere trinn for å erstatte lagrene, og ansvarsområdet for hver operasjon spores. Dette kan for eksempel være nødvendig:

1. Produksjonslinjen stoppes og ryddingsrutinen utføres.
1. Vedlikeholdspersonalet erstatter lageret.
1. Kvalitetssikringspersonell kontrollerer maskinen før den slås på igjen.

I dette eksemplet kan følgende operasjoner opprettes for å representere arbeidet som må utføres:

- Stopp produksjonslinjen.
- Rydd opp i produksjonslinjen.
- Utfør maskinvedlikehold.
- Inspiser maskinen.

## <a name="create-an-operation"></a>Opprette en operasjon

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Operasjoner**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Operasjon** – Angi en unik ID eller et unikt navn for operasjonen.
    - **Beskrivelse** – Angi en detaljert beskrivelse av operasjonen.
    - **Type** – Hvis operasjonen bare kan brukes med avvik som er knyttet til en bestemt ordretype, velger du ordretypen (*Bestilling* eller *Salgsordre*).

1. Lukk siden.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](enable-quality-management.md)
- [Opprette og behandle avvik](tasks/create-process-non-conformance.md)
- [Arbeidere som er ansvarlige for å godkjenne avvik](quality-responsible-workers.md)
- [Karantenesoner for avvik](quality-quarantine-zones.md)
- [Diagnosetyper for avvik](quality-diagnostic-types.md)
- [Kvalitetsendringer for avvik](quality-charges.md)
- [Problemtyper for avvik](quality-operations.md)
- [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
