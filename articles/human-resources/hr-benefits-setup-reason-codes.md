---
title: Definer årsakskoder
description: Dynamics 365 Human Resources bruker årsaks koder til å forklare hvorfor en ansatts fordeler blir endret.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a30a59a648d54eda771845b8bee52df43987d3d1
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068290"
---
# <a name="set-up-reason-codes"></a>Definer årsakskoder


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources bruker årsaks koder til å forklare hvorfor en ansatts fordeler blir endret.

> [!NOTE]
> Per januar 2021 ble årsakskoder migrert til arbeidsområdet for **Personaladministrasjon** i stedet for arbeidsområdet for **Fordelsbehandling**. Hvis du vil ha mer informasjon, kan du se [Migrere årsakskoder manuelt til Personaladministrasjon](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Opprette årsakskoder

1. I arbeidsområdet **Personaladministrasjon** (eller **Fordelsbehandling** hvis årsakskodene ikke er migrert), velger du **Koblinger**, og deretter velger du **Årsakskoder**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Årsakskode** | Et unikt navn som identifiserer årsaken til at en ansatt ville endre en fordelsplanregistrering. |
   | **Beskrivelse** | En beskrivelse av årsakskoden. |

4. Under **Gjeldende scenarier** angir du **Fordelsbehandling** til **Ja**. (Gjelder ikke hvis årsakskodene ikke er migrert til **Personaladministrasjon**-arbeidsområdet.)

5. Velg **Lagre**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Migrere årsakskoder manuelt til Personaladministrasjon

I januar 2021 ble årsakskoder migrert til arbeidsområdet for **Personaladministrasjon** i stedet for arbeidsområdet for **Fordelsbehandling**. De fleste årsakskodedata migreres automatisk i miljøet ditt. Det kan hende at enkelte årsakskodedata ikke migreres. Årsakskoder har for eksempel nå en maksimumsgrense på 15 tegn, slik at alle årsakskoder som er lengre enn 15 tegn, ikke migrerer automatisk.

Du vil se et banner på **Koblinger**-siden i arbeidsområdet **Fordelsadministrasjon** som informerer deg om migrering og om årsakskoder ikke migreres.

1. Velg **Årsakskoder** for å få detaljer om migreringsstatus.

   [![Årsakskoder.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Velg en årsakskode som ikke kan migreres.

   [![Årsakskode for migreringsstatus.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Velg **Migrer årsakskode**.

   [![Overfør årsakskode.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. I ruten **Migrering av fordelsårsakskode** har du to alternativer for tilordning av en årsakskode for Personaladministrasjon:

   - Hvis du vil bruke en eksisterende årsakskode i Personaladministrasjon, velger du en fra rullegardinlisten **Bruk eksisterende årsakskode**.
     > [!NOTE]
     > Du kan bare bruke en eksisterende årsakskode i Personaladministrasjon hvis en annen årsakskode for fordelsadministrasjon ikke allerede har migrert til den.
   - Hvis du vil opprette en ny årsakskode i Personaladministrasjon, angir du en ny i **Ny årsakskode**, og deretter skriver inn en beskrivelse i **Ny beskrivelse**.

   [![Tilordne til en årsakskode for personaladministrasjon.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Etter at årsakskoder er migrert til Personaladministrasjon, blir alternativet for å bruke dem i Fordelsbehandling automatisk satt til **Ja**.

[![Bruke årsakskode i Fordelsbehandling.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
