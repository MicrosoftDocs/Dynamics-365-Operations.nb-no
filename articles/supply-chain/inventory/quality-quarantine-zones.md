---
title: Karantenesoner for avvik
description: Denne artikkelen beskriver hvordan du oppretter og bruker karantenesoner for avvik.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e556d2aa078a76ff4f81b6763535c38ce1cca0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857728"
---
# <a name="quarantine-zones-for-nonconformances"></a>Karantenesoner for avvik

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter og bruker karantenesoner for avvik.

Du kan bruke **Karantenesoner**-siden til å definere soner som kan tilordnes til et avvik. Når du oppretter et avvik, kan du definere feltene **Karantenesone** og **Karantenetype** i kategorien **Generelt** på **Avvik**-siden. Feltet **Karantenesone** angir vanligvis området eller lokasjonen der varen finnes. **Karantenetype**-feltet definerer varen som enten *Begrenset bruk* eller *Kan ikke brukes*.

Når du skriver ut en avviks- eller rettelsesrapport for et avvik, kan du vise karantenesonen der varen finnes.

Du kan også skrive ut en avviksbrikke for et avvik. Denne rapporten viser den tilordnede karantenesonen og informasjon om bruk, for å gi veiledning om hvordan materialer med defekter skal håndteres. Karantenesonene kan tilsvare lagerlokasjoner eller operasjonsressurser.

## <a name="examples-of-quarantine-zones"></a>Eksempler på karantenesoner

### <a name="example-1"></a>Eksempel 1

Du jobber i et produksjonsfirma for elektronikk, som produserer og distribuerer TV-er, høyttalere og mediespillere. I dette tilfellet kan du konfigurere en karantenesone til å representere hver produkttype.

### <a name="example-2"></a>Eksempel 2

Tre bokser og to reoler brukes til å lagre varer som er avvik. I dette tilfellet kan du konfigurere fem karantenesoner, én for hver boks og hver reol.

## <a name="create-a-quarantine-zone"></a>Opprette en karantenesone

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Karantenesoner**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Karantenesone** – Angi en unik ID eller et navn for karantenesonen.
    - **Beskrivelse** – Angi en detaljert beskrivelse av karantenesonen.

1. Lukk siden.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](enable-quality-management.md)
- [Arbeidere som er ansvarlige for å godkjenne avvik](quality-responsible-workers.md)
- [Problemtyper for avvik](quality-quarantine-zones.md)
- [Diagnosetyper for avvik](quality-diagnostic-types.md)
- [Kvalitetsendringer for avvik](quality-charges.md)
- [Operasjoner for avvik](quality-operations.md)
- [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
