---
title: Opprette en driftstidskalender
description: Definer en driftstidskalender, helligdager og fritid i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 641f66c75875cfba51af3753223a070d7cb7dc50
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010109"
---
# <a name="create-a-working-time-calendar"></a>Opprette en driftstidskalender

En driftstidskalender i Dynamics 365 Human Resources viser antall dager og timer som ansatte arbeider i organisasjonen. Når en ansatt sender en avspaseringsforespørsel, trenger de ikke å bekymre seg for helligdager og lukking.

Hvis du vil effektivisere avspaseringsforespørsler, konfigurerer du disse elementene for organisasjonen:

- Driftstidskalender
- Helligdager og lukkinger
- Fritid

Du kan legge til de to siste elementene mens du definerer en driftstidskalender. Du kan også konfigurere eller oppdatere dem separat.

## <a name="set-up-a-working-time-calendar"></a>Definere en driftskalender

Definer minst én driftstidskalender som viser driftsdager og driftstimer. Hvis du har steder i flere land og områder, kan det være lurt å definere en driftstidskalender for hvert område.

1. På siden **Organisasjonsstyring** velger du **Kalendere**.

2. Velg **Ny**, og angi et navn og en beskrivelse for kalenderen.

3. Under **Genereringsalternativer** velger du arbeidsdagene for organisasjonen og angir arbeidstider. 
   - Hvis du vil legge til en helligdag eller lukking, velger du **Legg til**-knappen ved siden av **Helligdager og lukkinger**.
   - Hvis du vil legge til fritid, som lunsjer eller pauser, velger du **Legg til** under **Fritid** og angir navnet og tidsperioden.

4. Under **Dager** velger du **Generer** for å generere dagene i kalenderen. Angi datoområdet for kalenderen, og velg deretter **Generer dager**.

5. Hvis du vil legge til arbeidsplaner, går du til **Arbeidsplan**, velger **Legg til** og angir deretter tidene for hver arbeidsplan.

## <a name="configure-holidays-and-closures"></a>Konfigurere helligdager og lukkinger

Du kan legge til eller endre helligdager og lukkinger separat fra en driftstidskalender.

1. På siden **Organisasjonsstyring** velger du **Helligdager og lukkinger**.

2. Velg **Ny**, og angi et navn og en dato for helligdagen eller lukkingen.

## <a name="configure-non-work-time"></a>Konfigurere fritid

Du kan legge til eller endre tidspunkt for fritid separat fra en driftstidskalender.

1. På siden **Organisasjonsstyring** velger du **Fritid**.

2. Velg **Ny**, og angi et navn og et tidsomfang for fritiden.

## <a name="leave-and-absence-preview-feature"></a>Forhåndsversjonsfunksjon for permisjon og fravær

[!include [banner](includes/preview-feature-leave-absence.md)]

Hvis du har aktivert forhåndsversjonsfunksjonen for korreksjon for helligdager for permisjon og fravær, bruker Human Resources helligdager og lukkingsdatoer til å bestemme hvor mange dager det skal justeres for ansatte som er registrert i kalenderen.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)
- [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md)
