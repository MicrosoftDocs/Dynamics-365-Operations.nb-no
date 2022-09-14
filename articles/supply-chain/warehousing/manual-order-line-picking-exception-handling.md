---
title: Håndtere plukkunntak for salgs- og overføringslinjer manuelt
description: Denne artikkelen beskriver hvordan administratorer kan plukke (eller legge tilbake) lagertransaksjoner manuelt for å løse problemer som forårsakes av skadede salgs- og overføringsordredata.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403673"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Håndtere plukkunntak for salgs- og overføringslinjer manuelt

[!include [banner](../includes/banner.md)]

Manuell håndtering av plukkunntak for salgs- og overføringslinjer gjør at administratorer kan løse problemer som forårsakes av skadede salgs- og overføringsordredata. Den gjør at klarerte brukerne manuelt kan plukke (eller legge tilbake) lagertransaksjoner som er knyttet til salgs- og overføringsordrelinjer mens lagerprosesser allerede er i gang.

Funksjonaliteten som beskrives her, bør bare brukes i tilfeller der systemet ikke kan fullføre behandlingen av lagerprosesstakken på vanlig måte. Den kan som standard bare brukes av brukere med systemadministratorrolle. Du kan imidlertid gi tilgang til den ved å tilordne rettigheten *Plukk salgslinjer manuelt* til andre roller etter behov.

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funksjonen for systemet

Før du kan bruke funksjonene som beskrives i denne artikkelen, må du aktivere dem i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonene og aktivere dem. I arbeidsområdet **Funksjonsbehandling** er funksjonene oppført med følgende navn:

- *Plukktjeneste for manuell salgslinje for administrator eller lignende klarerte brukere*<br>(Denne funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.25 og kan ikke deaktiveres.)
- *Plukktjeneste for manuell overføringslinje for administrator eller lignende klarerte brukere*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Korriger transaksjoner knyttet til salgs- eller overføringsordrelinjer

Bruk fremgangsmåten nedenfor til å rette transaksjoner som er knyttet til salgs- eller overføringsordrelinjer.

1. Følg et av disse trinnene, avhengig av ordretypen du må rette:

    - Hvis du vil rette en transaksjon som er knyttet til en salgsordre, kan du gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Plukk salgslinjer manuelt**.
    - Hvis du vil rette en transaksjon som er knyttet til en overføringsordre, kan du gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Plukk overføringslinjer manuelt**.

1. På siden **Plukk salgslinjer manuelt** eller **Plukk overføringslinjer manuelt** bruker du filtrene øverst i rutenettet til å finne linjen du ser etter, og deretter velger du målordrelinjen i det øvre rutenettet.
1. Bruk fanene **Lagertransaksjoner**, **Lastlinjer**, **Arbeidslinjer** og **Containerlinjer** i den nedre delen for å vise mer informasjon om den valgte linjen. Informasjonen i disse fanene gir en grunnleggende oversikt over de tilknyttede lagerprosessene og statusene deres.
1. Velg **Plukk** i handlingsruten for å åpne den valgte ordrelinjen på **Plukk**-siden for lagertransaksjoner. Du kan fullføre dette trinnet, til og med for ordrelinjer som allerede er frigitt til lageret. (Vanligvis kan ikke ordrelinjer som er frigitt til lageret, åpnes på **Plukk**-siden.)

    > [!NOTE]
    > Det kan hende at du får ulike advarsler når du åpner **Plukk**-siden. Gjør det som disse advarslene anbefaler. Du kan for eksempel få en advarsel om ordrelinjer som er knyttet til lagerarbeid. I dette tilfellet kan du prøve å avbryte arbeidet ved å bruke standardfunksjonen for å [avbryte arbeid](cancel-warehouse-work.md) før du foretar manuell korrigering.

1. Velg linjen i rutenettet **Transaksjoner**, og velg deretter **Legg til plukklinje** på verktøylinjen **Transaksjoner**.
1. Den valgte linjen flyttes til rutenettet **Plukklinjer**. Angi aktuelle verdier for alle kolonner som mangler nødvendig informasjon. (Du kan for eksempel angi lokasjonen og nummerskiltet som varen skal plukkes / legges tilbake fra.)
1. Velg **Bekreft plukking av alle** på verktøylinjen **Plukklinjer**.

## <a name="correct-load-line-quantities"></a>Korriger lastlinjeantall

Bruk fremgangsmåten nedenfor til å korrigere et lastlinjeantall.

1. Følg et av disse trinnene, avhengig av ordretypen du må rette:

    - Hvis du vil rette en transaksjon som er knyttet til en salgsordre, kan du gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Plukk salgslinjer manuelt**.
    - Hvis du vil rette en transaksjon som er knyttet til en overføringsordre, kan du gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Plukk overføringslinjer manuelt**.

1. På siden **Plukk salgslinjer manuelt** eller **Plukk overføringslinjer manuelt** bruker du filtrene øverst i rutenettet til å finne linjen du ser etter, og deretter velger du målordrelinjen i det øvre rutenettet.
1. Velg **Korriger lastlinjer manuelt** på verktøylinjen i **Lastlinjer**-fanen i den nedre delen.
1. I rutenettet **Lagertransaksjoner** på siden **Korriger lastlinjer manuelt** går du gjennom lagertransaksjonene som er knyttet til den valgte lastlinjen.
1. I det øvre rutenettet korrigerer du lastlinjeantallet i følgende kolonner etter behov:

    - **Arbeidsopprettet antall**
    - **Plukket antall**
    - **Planlagt direkteoverføringsantall**

    Systemet vil validere eventuelle endringer du gjør i disse kolonnene.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
