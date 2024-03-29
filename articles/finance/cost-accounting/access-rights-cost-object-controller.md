---
title: Tilgangsrettigheter til kontrollere for kostnadsobjekt
description: Denne artikkelen inneholder informasjon om tilgangsrettigheter for kontrollere for kostnadsobjekt.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c40be758c5e5d1d1fb025630ed8321ae46251892
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903196"
---
# <a name="access-rights-for-cost-object-controllers"></a>Tilgangsrettigheter til kontrollere for kostnadsobjekt

[!include [banner](../includes/banner.md)]

Arbeidsområdet **Kostnadskontroll** er et sentralt punkt der ledere kan vise ytelsen til kostnadsobjektene sine. Dette arbeidsområdet lar ledere forbruke kostnadsregnskapsdata selv om de ikke er regnskapsførere. Av sikkerhetsmessige årsaker må ledere bare kunne se kostnadsregnskapsdataene som er knyttet til de bestemte kostnadsobjektene de har ansvaret for.

Det er fire unike roller i kostnadsregnskap.

| Rollenavn               | Lisens      |
|-------------------------|--------------|
| Behandling av kostnadsregn | Aktivitet     |
| Regnskapsfører lager         | Operations   |
| Assisterende lagerregnskapsfører   | Operations   |
| Kontroller for kostnadsobjekt  | Teammedlemmer |

Denne artikkelen forklarer hvordan du tilordner rollen **Kontroller for kostnadsobjekt** til en leder.

Når rollen **Kontroller for kostnadsobjekt** er tilordnet en leder, kan lederen utføre følgende oppgaver:

- Gå til arbeidsområdet **Kostnadskontroll** (i klienten).

    - Gå gjennom og få visningstilgang til sidene som støtter gjennomgangsopplevelsen.

- Gå til arbeidsområdet **Kostnadskontroll** (i mobilprogrammet).

> [!NOTE]
> Rollen **Kontroller for kostnadsobjekt** styrer ikke hvilke objekter brukeren kan få tilgang til og vise data for. Radnivåsikkerhet oppnås via dimensjonshierarkier og hierarkiet for tilgangsliste.

## <a name="grant-access-rights"></a>Gi tilgangsrettigheter
Følgende eksempel viser hvordan et dimensjonshierarki kan se ut.

**Detaljer for dimensjonshierarki**

| Dimensjonshierarkinavn | Dimensjon    | Navn på dimensjonshierarkitype      | Hierarki for tilgangsliste |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisasjon             | Kostsentre | Hierarki for dimensjonsklassifisering | **Ja**               |

Du kan bruke hurtigfanen **Brukere** i hierarkidesigner til å sette inn én eller flere bruker-ID-er for hver node.

|             Noder                 | Brukere            | Fra-dimensjonsmedlem     |   Til-dimensjonsmedlem   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| Organisasjon                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Administrator                 | April            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans   | Charlotte           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personale        | Magnus            | CC001                     | CC001                   |
| &nbsp;&nbsp;Produksjon            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Innpakning | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Samling  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Regnskapsførere må tilordnes det øverste nivået i hierarkiet, slik at de kan se alle oppføringene i kostnadsregnskap.

Før hierarkiet for tilgangsliste og sikkerhetsinnstillingene for det kan brukes, må alternativet **Aktiver visningstilgang for dimensjonsmedlemmer for kostnadsobjekt** settes til **Ja** i **Generelt**-fanen på siden **Kostnadsregnskapsparametere** (**Kostnadsregnskap** > **Oppsett** > **Parametere**).

Innstillingene for hierarkiet for tilgangsliste brukes til å styre dataene som vises på følgende områder:

- Arbeidsområdet **Kostnadskontroll** (i klienten):

    - Data på sidene som brukes til gjennomgang

- Arbeidsområdet **Kostnadskontroll** (i mobilprogrammet):

    - Saldoer i kort

- Microsoft Power BI:

    - Data som vises i Power BI-visualiseringer
    - Power BI-datavisualiseringer som er innebygd i Dynamics 365 Finance-klienten

> [!IMPORTANT]
> - Før hierarkiet for tilgangsliste kan påvirke data i Power BI, må hierarkiet for tilgangsliste og radnivåsikkerhet i Power BI sammenkobles. Hvis du vil ha mer informasjon, kan du se [Definere sikkerhet for innholdspakken Kostnadsregnskap](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Denne artikkelen viser forutsetningene som må være på plass før du kan bruke arbeidsområdet **Kostnadskontroll**.

Tilleggsressurser

- [Arbeidsområde for kostnadskontroll](cost-control-workspace.md)
- [Dimensjonshierarki](dimension-hierarchy.md)
- [Definere sikkerhet for innholdspakken Kostnadsregnskap](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
