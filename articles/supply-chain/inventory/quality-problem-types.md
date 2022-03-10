---
title: Problemtyper for avvik
description: Dette emnet beskriver hvordan du oppretter og bruker problemtyper for avvik.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26705dd12f478f4ca6046c7265d4ae3cb1d08c69
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568813"
---
# <a name="problem-types-for-nonconformances"></a>Problemtyper for avvik

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter og bruker problemtyper for avvik.

Du bruker **Problemtyper**-siden til å definere en klassifisering av kvalitetsproblemer som kan oppstå for de ulike avvikstypene. For hver problemtype du oppretter må du angi avvikstypene som problemtypen kan brukes med. Du kan definere følgende avvikstyper:

- **Intern**– Avvik av denne typen er knyttet til lagerbeholdning (for eksempel kvalitetsordrer eller karanteneordrer).
- **Kunde** – Avvik av denne typen er knyttet til salgsordrer.
- **Leverandør** – Avvik av denne typen er knyttet til bestillinger.
- **Tjenesteforespørsel** – Avvik av denne typen er knyttet til serviceordrer.
- **Produksjon** – Avvik av denne typen er knyttet til parti- eller produksjonsordrer.
- **Koproduktproduksjon** – Avvik av denne typen er knyttet til partiordrer for koprodukter.

Når du oppretter en ny problemtype, velger du **Avvikstyper** i handlingsruten for å opprette en liste over én eller flere avvikstyper som er autorisert for problemtypen. Problemtyper som er knyttet til feilkoder, kan for eksempel gjelde for alle avvikstyper. En problemtype som er knyttet til klager fra kunder, kan imidlertid bare gjelde for avvikstypene **Kunde** og **Tjenesteforespørsel**.

## <a name="examples-of-problem-types"></a>Eksempler på problemtyper

Her er noen eksempler på scenarier for problemtyper som kan brukes med de forskjellige avvikstypene:

- **Kunde:** En kunde rapporterte en klage, en kunde returnerte en vare, eller kvalitetsspesifikasjoner ble ikke oppfylt.
- **Leverandør:** Produktet ble skadet, kvalitetsspesifikasjoner ble ikke oppfylt eller feil produkt ble mottatt.
- **Tjenesteforespørsel:** Kvalitetsspesifikasjoner ble ikke oppfylt, en kunde la inn en klage eller vedlikehold på maskinen er nødvendig.
- **Produksjon:** Kvalitetsspesifikasjoner ble ikke oppfylt, maskinvedlikehold er nødvendig eller produktet ble skadet.
- **Koproduktproduksjon:** Kvalitetsspesifikasjoner ble ikke oppfylt, maskinvedlikehold er nødvendig eller produktet ble skadet.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Opprette en problemtype og tilordne den til avvikstyper

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Problemtyper**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Problemtype** – Angi en unik ID eller et unikt navn for problemtypen.
    - **Beskrivelse** – Angi en detaljert beskrivelse av problemtypen.

1. Mens den nye raden fremdeles er valgt, velger du **Avvikstyper** i handlingsruten.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. For den nye raden setter du deretter **Avvikstype**-feltet til avvikstypen som du vil tillate for problemtypen.
1. Gjenta det forrige trinnet for hver ekstra avvikstype du vil autorisere for problemtypen.
1. Lukk sidene.

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
