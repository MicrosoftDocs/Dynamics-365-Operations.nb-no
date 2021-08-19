---
title: Aktivere kvalitets- og avviksstyring
description: Dette emnet gir en oversikt over prosessen for å definere og konfigurere funksjoner for kvalitets- og avviksstyring i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b202d76e4b5bc0dfe9f0572274b3453abca58a435b70e96874155f867114a2aa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717346"
---
# <a name="enable-quality-and-nonconformance-management"></a>Aktivere kvalitets- og avviksstyring

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over prosessen for å definere og konfigurere funksjoner for kvalitets- og avviksstyring i Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Aktivere kvalitets- og avviksstyring

Følg denne fremgangsmåten for å aktivere kvalitetsstyring på systemet.

1. Gå til **Lagerstyring \> Oppsett \> Parametere for beholdnings- og lagerstyring**.
1. I kategorien **Kvalitetsstyring** setter du alternativet **Bruk kvalitetsstyring** til *Ja*.
1. I **Timepris**-feltet angir du en timepris for arbeid i lokal valuta. Timeprisen brukes til å beregne kostnader for operasjoner som er knyttet til et avvik. Timeprisen og de beregnede kostnadene gir referanseinformasjon for et avvik. De samhandler ikke med annen funksjonalitet.
1. Velg **Rapportoppsett**.
1. Legg til nye linjer for de ulike rapporttypene, og velg dokumenttypen som skal brukes for hver rapport.
1. Lukk siden.
1. Lukk siden.

## <a name="quality-management-configuration-process"></a>Konfigurasjonsprosess for kvalitetsstyring

Før du kan begynne å bruke kvalitetsstyringsfunksjonene og generere kvalitetsordrer, må du konfigurere systemet og forutsetningene. Her er en liste over trinnene som kreves for å konfigurere kvalitetsstyring.

1. [Aktivere kvalitets- og avviksstyring](#enable-qm).
1. Valgfritt: [Konfigurere testinstrumenter](quality-test-instruments.md).
1. [Konfigurere tester](quality-tests.md).
1. [Konfigurere testvariabler og -resultater](quality-test-variables.md).
1. [Konfigurere testgrupper](quality-test-groups.md).
1. Valgfritt: [Konfigurere kvalitetsgrupper, og koble til produkter](quality-groups.md).
1. Valgfritt: [Konfigurere kvalitettilordninger](quality-associations.md).

Når konfigurasjonen er fullført, kan du begynne å opprette og behandle kvalitetsordrer. Hvis du vil ha mer informasjon om hvordan du oppretter og jobber med kvalitetsordrer, kan du [Kvalitetsordrer](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Konfigurasjonsprosess for avviksstyring

Før du kan begynne å bruke avviksstyringsfunksjonene og generere avvik, må du konfigurere systemet og forutsetningene. Her er en liste over trinnene som kreves for å konfigurere avviksstyring.

1. [Aktivere kvalitets- og avviksstyring](#enable-qm).
1. [Konfigurere arbeidere som er ansvarlige for å godkjenne avvik](quality-responsible-workers.md).
1. [Konfigurere problemtyper](quality-problem-types.md).
1. [Konfigurere karantenesoner](quality-quarantine-zones.md).
1. [Konfigurere diagnosetyper](quality-diagnostic-types.md).
1. [Konfigurere operasjoner](quality-operations.md).
1. Valgfritt: [Konfigurere kvalitetsgebyrer](quality-charges.md).

Når konfigurasjonen er fullført, kan du begynne å opprette og behandle avvik. Hvis du vil ha mer informasjon om hvordan du oppretter og arbeider med avvik, kan du se [Opprette og behandle avvik](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over kvalitetsstyring](quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](enable-quality-management.md)
- [Kvalitetsstyring for lagerprosesser](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
