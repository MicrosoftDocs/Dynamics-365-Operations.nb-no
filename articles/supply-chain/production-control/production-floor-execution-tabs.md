---
title: Utform grensesnittet for produksjonsutførelse
description: Denne artikkelen beskriver hvordan du utformer innholdet i brukergrensesnittet for hver konfigurasjon.
author: johanhoffmann
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 66190ab261d19c718e13801c17a34b915ccf158c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852251"
---
# <a name="design-the-production-floor-execution-interface"></a>Utform grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]

Du kan utforme innholdet i brukergrensesnittet for hver konfigurasjon som brukes av grensesnittet for produksjonsutførelse. Arbeidere i én arbeidscelle kan for eksempel trenge å åpne jobbinstruksjoner i produksjonen, mens det ikke er nødvendig med instruksjoner i en annen arbeidscelle. I dette tilfellet bør det opprettes to konfigurasjoner, en med en knapp for å åpne dokumentvedlegg og en uten denne knappen.

## <a name="design-a-tab"></a>Utform en fane

På siden **Konfigurere produksjonsutførelse** kan du opprette og konfigurere faner ved å velge **Utform faner** i handlingsruten.

Hver fane er delt inn i fire deler, som vist i følgende illustrasjon.

![Faneoppsett.](media/pfe-tab-layout.png "Faneoppsett")

Følgende elementer vises i illustrasjonen:

1. Primær verktøylinje
1. Sekundær verktøylinje
1. Hovedvisning
1. Detaljert visning

Hvis du vil opprette og konfigurere en ny fane, gjør du følgende:

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurere produksjonsutførelse**.

1. Velg **Utform faner** i handlingsruten for å åpne siden **Utform faner**.

    ![Utform faner-siden.](media/pfe-design-tabs.png "Utform faner-siden")

1. Velg **Ny** i handlingsruten.

1. Velg følgende innstillinger i toppteksten på siden:

    - **Fanenavn** – Angi et navn på fanen.
    - **Hovedvisning** – Velg mellom de forhåndsdefinerte jobblistene (*Aktive jobber*, *Alle jobber*, *Mine jobber* og *Min maskin*).
    - **Detaljvisning** – Velg mellom en tom verdi eller **Jobbdetaljer**. Hvis du velger den tomme verdien, vil det ikke være noen detaljert visning i fanen. Hvis du velger **Jobbdetaljer**, vil den detaljerte visningen inneholde en detaljert beskrivelse av jobben som er valgt i jobblisten i hovedvisningen.

1. Under **Primær verktøylinje** velger du hvilke knapper som skal være tilgjengelige på den primære verktøylinjen. Kolonnen **Tilgjengelige handlinger** viser en liste over alle knappene som kan legges til. Kolonnen **Valgte handlinger** viser en liste over alle knappene som er inkludert i den gjeldende konfigurasjonen. Bruk knappene mellom kolonnene til å flytte valgte elementer mellom kolonnene etter behov. Bruk opp- og ned-knappene ved siden av kolonnen **Valgte handlinger** til å angi i hvilken rekkefølge knappene skal vises i, i brukergrensesnittet.

1. Under **Sekundær verktøylinje** velger du hvilke knapper som skal være tilgjengelige på den sekundære verktøylinjen. Kolonnen **Tilgjengelige handlinger** viser en liste over alle knappene som kan legges til. Kolonnen **Valgte handlinger** viser en liste over alle knappene som er inkludert i den gjeldende konfigurasjonen. Bruk knappene mellom kolonnene til å flytte valgte elementer mellom kolonnene etter behov. Bruk opp- og ned-knappene ved siden av kolonnen **Valgte handlinger** til å angi i hvilken rekkefølge knappene skal vises i, i brukergrensesnittet.

## <a name="associate-a-tab-with-a-configuration"></a>Knytt en fane til en konfigurasjon

Etter at du har utformet alle fanene du trenger, kan du knytte dem til en konfigurasjon.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurere produksjonsutførelse**.

    ![Konfigurer produksjonsutførelse.](media/pfe-config-prod-floor-execution.png "Konfigurer produksjonsutførelse")

1. Velg **Legg til** på hurtigfanen **Fanevalg**.

1. Det blir lagt til en ny rad i rutenettet. For denne nye raden velger du navnet på en fane du vil legge til i konfigurasjonen.

1. Fortsett å legge til flere faner etter behov.

1. Bruk knappene **Flytt opp** og **Flytt ned** på verktøylinjen til å ordne fanene etter behov. Fanene blir vist fra venstre mot høyre i den rekkefølgen som vises i skjermbildet ovenfor (fanen øverst vises til venstre).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
