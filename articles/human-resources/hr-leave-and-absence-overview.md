---
title: Oversikt
description: I Dynamics 365 Human Resources gir arbeidsområdet **Permisjon og fravær** et fleksibelt rammeverk for å opprette nye permisjonsplaner, arbeidsflyter for behandling av forespørsler og en intuitiv, selvbetjent side der ansatte kan be om avspasering.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 493bc3abe82103541125914896252b2eae596b38
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091754"
---
# <a name="overview"></a>Oversikt

Dynamics 365 Human Resources hjelper deg med å gi arbeiderne flotte fordeler. Arbeidsområdet **Permisjon og fravær** gir et fleksibelt rammeverk for å opprette nye permisjonsplaner, arbeidsflyter for behandling av forespørsler og en intuitiv, selvbetjent side der ansatte kan be om avspasering. Analyse hjelper organisasjonen din med å måle og overvåke permisjonssaldoer og forbruk for permisjonsplaner.

## <a name="set-up-leave-and-absence"></a>Konfigurere permisjon og fravær

Før du kan opprette permisjonsplaner for de ansatte, må du utføre noen få konfigurasjonstrinn:

- [Konfigurere permisjons- og fraværsparametere](hr-leave-and-absence-parameters.md)
- [Opprette en driftstidskalender](hr-leave-and-absence-working-time-calendar.md)
- [Opprette en arbeidsflyt for permisjonsforespørsel](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Opprette og administrere permisjonsplaner

Før du oppretter permisjonsplaner for arbeiderne, må du opprette permisjons- og fraværstyper. Når du har opprettet en permisjonsplan, kan du deretter registrere arbeidere i planen. Du kan også kjøre avsetningsprosessen, opprette varsler og vise analyse for planene dine.

- [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md)
- [Opprette en permisjons- og fraværsplan](hr-leave-and-absence-plans.md)
- [Tilordne arbeidere til en permisjonsplan](hr-leave-and-absence-enroll.md)
- [Avsette permisjons- og fraværsplaner](hr-leave-and-absence-accrue.md)
- [Vise analyse for permisjon og fravær](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Be om avspasering og administrere forespørsler

De ansatte kan sende inn avspaseringsforespørsler, og du kan behandle dem i arbeidsområdet **Ansattselvbetjening**.

- [Be om avspasering](hr-employee-self-service-request-time-off.md)
- [Administrere permisjons- og fraværsforespørsler](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>Forhåndsversjonsfunksjoner for permisjon og fravær

Du kan prøve ut nye forhåndsversjonsfunksjoner for permisjon og fravær i et **sandkassemiljø**. Hvis du vil ha informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md). Forhåndsversjonsfunksjonene omfatter:

- **Permisjons- og fraværskalender** – Permisjons- og fraværsparametere flyttes fra **Personalparametere** til en ny skjerm kalt for **Permisjons- og fraværsparametere**. Den nye skjermen inneholder en ny **Kalender**-kategori. Denne forhåndsversjonen aktiverer bare et delsett av parameterne. Du får tilgang til den nye skjermen fra kategorien **Koblinger** i arbeidsområdet **Permisjon og fravær**. Kalenderne omfatter:
  - **Firmakalender** – viser alle fritidsforespørsler for ansatt. Personer med **Personal**-rollen kan få tilgang til denne kalenderen fra kategorien **Koblinger** i arbeidsområdet **Permisjon og fravær**.
  - **Kalender for lederteam** – viser alle fritidsforespørsler i direkterapporter. Ledere kan få tilgang til kalenderen fra kategorien **Mitt team** i Ansattselvbetjening under **Permisjon og fravær**. 

- **Feriekalendere i Permisjon og fravær** – Permisjonstyper inkluderer et nytt **Ferid**-alternativ, brukt i sammenheng med arbeidstidskalenderen. Dager som er definert av ferier og lukkinger, er nå angitt som **Ferie** når arbeidsdager genereres. Når avsetninger behandles, gjøres justeringer i ansatte som er tilordnet kalenderen, for å planlegge for helligdager som faller på arbeidsdager.

- **Revisjon av permisjonsavsetning** – En ny skjerm lar deg seg gjennom når avsetninger er behandlet og slettet, både av alle ansatte og enkeltansatte. Du får tilgang til denne nye skjermen fra kategorien **Koblinger** i arbeidsområdet **Permisjon og fravær**.

- **Sletting av permisjonsavsetning** – Du kan nå slette avsetningsposter for bestemte permisjonsplaner. Du får tilgang til dette nye alternativet fra kategorien **Koblinger** i arbeidsområdet **Permisjon og fravær**. For enkeltansatte vises dette alternativet i gruppen **Permisjon og fravær** i ansattprofilen. 

- **Avrunding for permisjonsavsetning** – Nye alternativer for **Permisjonstype** definerer hvilken type avrunding som avsetningen skal bruke, pluss desimalpresisjonen for avrundingen under avsetningsprosessen. Når avsetninger behandles, brukes avrundingen og presisjonen på avsetningspostene. 

- **Konfigurer flere permisjonstyper i en enkelt permisjonsplan** – En ny kolonne i tidsplanen for permisjonsavsetning lar deg definere flere permisjonstyper for en permisjons- og fraværsplan med forskjellige avsetningsplaner. Det forrige **Permisjonstype**-feltet er fjernet. I den ansattes registrering vises saldoene for permisjonstypene nå i en tabell i stedet for øverst på skjermen.

  > [!IMPORTANT]
  > Du kan ikke deaktivere denne funksjonen etter at du har aktivert den.

- **Bruk en ansatts fulltidsekvivalens (FTE) for avsetning** – En ny kolonne i tidsplanen for permisjonsavsetning tillater bruk av FTE for avsetning. Når avsetninger behandles, bruker programmet den ansattes primære stilling og FTE-en som er definert, til å bestemme avsetningsbeløpet som er fordelt.

  > [!NOTE]
  > Denne funksjonen er bare tilgjengelig hvis du aktiverer **Konfigurer flere permisjonstyper per permisjonsplan**. 
