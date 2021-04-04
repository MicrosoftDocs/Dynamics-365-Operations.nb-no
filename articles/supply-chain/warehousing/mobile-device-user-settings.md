---
title: Brukinnstillinger for mobilenhet
description: Dette emnet beskriver hvordan du kan administrere brukerinnstillinger for mobilenhet for lagerarbeidere.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mafoge
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8090305c1b296d8a8a64df444abb1d1f2235aeee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501204"
---
# <a name="mobile-device-user-settings"></a>Brukinnstillinger for mobilenhet

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Den nye Lagerstyring-mobilappen har et sett med appspesifikke innstillinger som gjør det en mulig å tilpasse brukeropplevelsen. Ettersom appen kan brukes på enheter med ulike skjermstørrelser og -konfigurasjoner (for eksempel nettbrett, telefon eller armholdt), kan det være nyttig å administrere disse innstillingene sentralt fra Microsoft Dynamics 365 Supply Chain Management.

Ved hjelp av funksjonen for *brukerinnstillinger for mobilenheter* kan du definere globale brukerinnstillinger som skal brukes på alle enheter. Du kan også definere flere detaljerte brukerinnstillinger for individuelle enhetsmerker, enhetsmodeller og/eller arbeidere. Når en arbeider logger på mobilappen Lagerstyring, henter og bruker appen den mest spesifikke innstillingsprofilen som er lagret i Supply Chain Management for samsvarende merke, enhet og/eller bruker-ID.

Denne funksjonen kan hjelpe arbeidere med å komme i gang raskere hver gang de begynner å bruke en ny enhet. Her er noen eksempler:

- Administratorer kan etablere et standard sett med innstillinger som fungerer best for enheter fra en bestemt produsent og/eller for bestemte enhetsmodeller. Dermed kan arbeidere komme i gang med en ny enhet uten nødvendigvis å måtte endre innstillingene.
- Hvis firmaet har et utvalg med identiske enheter som deles mellom arbeidere, vil arbeiderne se sitt foretrukne oppsett hver gang de logger på, selv om de aldri har brukt den spesifikke fysiske enheten de valgte på en bestemt dag.
- I Supply Chain Management kan administratorer vise og redigere alle lagrede innstillinger, også for enkeltarbeidere. Denne funksjonen kan hjelpe dem med å feilsøke eller finjustere nye funksjoner.

> [!IMPORTANT]
> Funksjonen for *brukerinnstillinger for mobilenhet* gjelder bare for den nye mobilappen Lagerstyring. Den fungerer ikke med den gamle lagerappen.

## <a name="turn-on-the-mobile-device-user-settings-feature"></a>Aktivere funksjonen for brukerinnstillinger for mobilenhet

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Brukerinnstillinger, ikoner og trinntitler for den nye lagerappen*

## <a name="create-and-manage-user-settings"></a>Opprette og administrere brukerinnstillinger

Bruk siden **Brukerinnstillinger for mobilenhet** til å opprette, vise og administrere innstillingsprofiler på alle nivåer av detaljnivå. Første gang en arbeider redigerer brukerinnstillingene på en ny enhet, blir en ny profil automatisk lagt til på denne siden, hvis den ikke allerede finnes. Profilen blir deretter oppdatert hver gang den arbeideren gjør en endring.

Du kan også definere en innstillingsprofil som gjelder for alle enhetsmerker, enhetsmodeller og/eller arbeidere. Du kan deretter øke detaljene ved å bruke mer spesifikke innstillinger for individuelle merker, modeller og/eller arbeidere.

Følg denne fremgangsmåten for å opprette og administrere brukerinnstillinger for mobilenhetene.

1. Gå til **Lagerstyring \> Mobil enhet \> Brukerinnstillinger for mobil enhet**.
1. Velg en eksisterende brukerinnstillingerprofil i listeruten for å åpne posten. Du kan også velge **Ny** i handlingsruten for å opprette en ny profil.

    Hver profil i listeruten kalles for å angi merket, modellen og/eller bruker-IDen som profilen gjelder for. Mer generelle profiler har verdien *Alle* for noen av eller alle disse egenskapene.

1. I hodedelen av posten for den nye eller valgte innstillingsprofilen angir du følgende felt:

    - **Enhetsmerkenavn** – Velg enhetsmerkenavnet som profilen skal gjelde for. La feltet stå tomt hvis profilen skal gjelde for alle merker. Listen over verdier omfatter alle merkene som er definert i systemet. Hvis du vil ha informasjon om hvordan du definerer listen over merker, kan du se neste del.
    - **ID for enhetsmodell** – Velg enhetsmodellen som profilen skal gjelde for. La feltet stå tomt hvis profilen skal gjelde for alle modeller for det valgte varemerket. Listen over verdier omfatter alle modellene som er definert for merket som er valgt i feltet **Enhetsmerkenavn**. Hvis du vil ha informasjon om hvordan du definerer listen over modeller for hvert merke, kan du se neste del.
    - **Bruker-ID** – Velg bruker-ID-en til lagerarbeideren som innstillingsprofilen skal gjelde for. La feltet stå tomt hvis profilen skal gjelde for alle arbeidere.

1. Angi følgende felt i hurtigfanen **Generelt**:

    - **Knappeposisjon** – Velg hvordan knapper skal plasseres på enheten. Elementer i appen flyttes for å tilpasses arbeiderens ønsker og praktiske kunnskaper. De tilgjengelige alternativene er *Nederst til høyre (standard)*, *Nederst til venstre*, *Øverst til høyre* og *Øverst til venstre*.
    - **Visningsretning** – Velg visningsretningen som skal brukes som standard i appen.
    - **Skann med kamera** – Sett dette alternativet til *Ja* for å bruke enhetsboksen til å skanne inndatafelt der den foretrukne inndatamodusen er satt til *Skanning*. Hvis enheten har en innebygd skanner, angir du dette alternativet til *Nei* for å bruke skanneren i stedet.
    - **Vis produktbilde** – Velg om produktserien skal vises hvis de er tilgjengelige for det frigitte produktet. Hvis du vil ha mer informasjon om hvordan du legger til produktbilder, kan du se [Legge til et bilde i et produkt](../pim/tasks/add-image-product.md).
    - **Vis fargetema** – Velg et fargetema for enheten.
    - **Lydnivå** – Velg lydnivået for enheten. Velg en verdi mellom 0 (null) og 10. En verdi på *0* representerer ingen lyd, og en verdi på *10* representerer maksimalt volum. Standardverdien er *4*.
    - **Vibrasjonsnivå** – Velg vibrasjonsnivået for enheten. Velg en verdi mellom 0 (null) og 5. En verdi på *0* representerer ingen vibrasjon, og en verdi på *5* representerer maksimal vibrasjon. Standardverdien er *1*.
    - **Tekstskaleringsprosent** – Angi tekststørrelsen som en prosent av standardstørrelsen. Angi en verdi mellom 70 og 400. En verdi på *70* representerer den minste tekstskaleringen, og en verdi på *400* representerer den største tekstskaleringen. Standardverdien er *100*.
    - **Knappeskaleringsprosent** – Angi knappestørrelsen som en prosent av standardstørrelsen. Angi en verdi mellom 50 og 200. En verdi på *50* representerer den minste knappeskaleringen, og en verdi på *200* representerer den største knappeskaleringen. Standardverdien er *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Opprette og administrere mobilenhetsmerker

Bruk siden **Mobilenhetsmerker** til å vise, opprette og administrere enhetsmerkene og modellene som kan brukes sammen med innstillingsprofilene dine. Mobilappen henter automatisk og sender inn det lokale merkenavnet og modell-ID-en første gang en arbeider redigerer innstillingene sine på en gitt enhet. Derfor blir de fleste av disse postene vanligvis generert automatisk. Du kan imidlertid også behandle alle postene på denne siden. Du kan for eksempel gi mer nyttige beskrivelser av hvert merke og hver modell for å bidra til å skille like eller kryptiske modell-ID-er.

Følg denne fremgangsmåten for å opprette og administrere mobilenhetsmerker og -modeller.

1. Gå til **Lagerstyring \> Mobilenhet \> Mobilenhetsmerker**.
1. I listeruten velger du et mobilenehtsmerke for å åpne dets post. Du kan også velge **Nytt** i handlingsruten for å opprette et nytt merke.
1. I hodedelen av posten for den nye eller valgte enhetsmerke angir du følgende felt:

    - **Enhetsmerkenavn** – Enhetsmerkenavnet, for eksempel *Microsoft Corporation*.
    - **Beskrivelse** – Du kan angi en beskrivelse for å skille merkenavn.

1. Hurtigfanen **Mobilenhetsmodeller** viser alle modellene for det valgte enhetsmerket. Bruk knappene på verktøylinjen til å legge til rader i rutenettet eller fjerne rader. For hver rad kan du angi du følgende felt:

    - **Enhetsmodell-ID** – Enhetsmodell-ID-en, for eksempel *Surface Book 2*.
    - **Beskrivelse** – Du kan angi en beskrivelse for å skille modell-ID-ene.
