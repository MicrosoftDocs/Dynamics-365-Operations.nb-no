---
title: Opprette en teamkalender
description: Du kan vise og opprette teamkalendere i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2ec767a868d5c76b57465c451b8cc893b8b0a56b
ms.sourcegitcommit: ffb5998e611b83c2e4f98323f39e3e8f6419c652
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/02/2020
ms.locfileid: "4419981"
---
# <a name="view-team-and-company-calendars"></a>Vise team- og firmakalendere

Du kan vise team- og firmakalendere i Dynamics 365 Human Resources. Teamkalendere viser bare direkte underordnede, som definert i linjehierarkiet.

## <a name="view-your-team-calendar-as-an-employee"></a>Vise teamkalenderen som en ansatt

1. I arbeidsområdet **Ansattselvbetjening** velger du **Fraværskalender for team** under **Sammendrag**.

## <a name="view-your-team-calendar-as-a-manager"></a>Vise teamkalenderen som en leder

1. I arbeidsområdet **Ansattselvbetjening** velger du **Mitt team**.

2. Velg **Permisjon og fravær**, og velg deretter **Vis fraværskalender for ledere**.

Ledere kan også få tilgang til teamkalenderen fra **Ventende fritidsforespørsler for teamet mitt**, **Godkjent avspasering** og **Avspaseringsforespørsler**. 

## <a name="view-a-company-calendar"></a>Vise en firmakalender

Personer som er i Human Resources-roller, kan vise firmakalendere. Firmakalendere viser alle ansatte. Som standard viser kalenderen dagens dato pluss 28 dager, men du kan endre datointervallet. Du kan også filtrere kalenderen etter **Navn**, **Personalnummer** og **Permisjonstype**.

1. I arbeidsområdet **Permisjon og fravær** velger du **Koblinger**.

2. Velg **Permisjons- og fraværskalender**.

Human Resources-roller kan også få tilgang til firmakalenderen fra **Permisjons- og fraværsforespørsler**, **Godkjent avspasering** og **Avspaseringsforespørsler**. 

Kalendere inneholder nå flere filtre og alternativer. Alle kalendere inneholder visningsalternativer for:

- Godkjente forespørsler
- Ventende forespørsler
- Ansatte med permisjonsforespørsler
- Ansatte uten permisjonsforespørsler
- Ansattes fødselsdager
- Forespørsler om fridager 
- Permisjonsforespørsler

Kalenderkonfigurasjon med permisjons- og fraværsparametere bestemmer tilgjengelige visningsalternativer.

Du kan også filtrere kalendere etter leder eller avdeling. Den primære stillingstilordningen bestemmer hvilke ansatte som vises når disse filtrene stilles inn. 

>[!IMPORTANT]
>Visning av permisjon og fravær på tvers av firmaer er for øyeblikket i forhåndsversjon. Du må aktivere den i **sandkassemiljøet**. Hvis du vil ha mer informasjon om aktivering av evalueringsfunksjonalitet, kan du se [Behandle funksjoner](hr-admin-manage-features.md).<br><br>
>Deretter må du aktivere funksjonen i **delte parametere for Human Resources** for å vise filteret for juridisk enhet i kalendere. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværsparametere](hr-leave-and-absence-parameters.md).<br><br>
>Du kan filtrere kalenderen etter juridisk enhet. Hvis du vil se alle ansatte uavhengig av juridisk enhet, fjerner du filterboksen og velger Enter. 

Hvis du vil ha informasjon om kalenderinnstillinger, kan du se [Konfigurere kalenderparametere](hr-leave-and-absence-parameters.md?configure-calendar-parameters).



[!INCLUDE[footer-include](../includes/footer-banner.md)]