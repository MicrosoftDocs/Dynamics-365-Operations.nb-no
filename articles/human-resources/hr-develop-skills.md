---
title: Konfigurere kompetanse
description: Du kan spore arbeiderens kompetanse i Dynamics 365 Human Resources. Du kan også angi kompetansen som kreves for en bestemt jobb.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076565"
---
# <a name="configure-skills"></a>Konfigurere kompetanse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan spore arbeiderens kompetanse i Dynamics 365 Human Resources. Du kan også angi kompetansen som kreves for en bestemt jobb.

Eksempler på kompetanser du kan spore:

- Tilsyn – Evne til å overvåke andres arbeid.
- Ledelse – Evne til å lede ansatte og forretningsområder.
- Planlegging – Evne til å tenke fremover, forme fremtidsplaner og gjennomføre dem.
- HTML – Evne til å skrive HTML-kode.

Hvis du ikke allerede har definert kompetansetyper og vurderingsmodeller, må du legge til noen før du kan opprette kompentanser.

Følgende personer kan angi kompetanser for en arbeider:

- Arbeidere kan registrere kompetanser for seg selv i Ansattselvbetjening. Disse kompetansene krever ledergodkjenning.
- Ledere kan angi kompetanser for arbeiderne sine. Du kan opprette en arbeidsflyt som godkjenner disse kompetansene automatisk.

## <a name="create-a-skill-type"></a>Opprette en kompetansetype

Kompetansetyper er kategorier som individuelle kompetanser faller under, for eksempel Administrasjon eller Salg.

1. Velg **Koblinger** i arbeidsområdet for **Ansattutvikling**.

2. Velg **Kompetansetyper** under **Kompetanseoppsett**.

3. Velg **Ny**.

4. Fyll ut følgende felt:

   - **Kompetansetype**: Angi et navn på kompetansetypen.
   - **Beskrivelse**: Skriv inn en beskrivelse av kompetansetypen.

5. Velg **Lagre**.

## <a name="create-a-rating-model"></a>Opprette en vurderingsmodell

Vurderingsmodeller bidrar til å vurdere en persons faktiske kompetansenivå, nivået de bør arbeide for å oppnå, eller kompetansenivået som kreves for en jobb. Hvert nivå i en vurderingsmodell tilordnes en faktor.

1. Velg **Koblinger** i arbeidsområdet for **Ansattutvikling**.

2. Velg **Vurderingsmodeller** under **Kompetanseoppsett**.

3. Velg **Ny**.

4. Fyll ut følgende felt:

   - **Vurdering**: Angi et navn på vurderingsmodellen, for eksempel **Kompetanser**.
   - **Beskrivelse** : Angi en beskrivelse av vurderingsmodellen, for eksempel **Kompetansevurderinger**.

5. Velg **Ny** i **Nivåer**-delen. Fyll ut følgende felt for hvert nivå du vil legge til:

   - **Nivå**: Angi et navn på nivået.
   - **Beskrivelse**: Angi en beskrivelse av nivået.
   - **Faktor** : Angi en faktorverdi fra 0-9. Faktorer bidrar til å normalisere resultatene av kompetanser som bruker ulike vurderingsmodeller. Hvert nivå må ha en unik faktor. Nivåer med høyere faktorverdier vektlegges mer i en vurderingsmodell.

   Fortsett å legge til nivåer etter behov. Du kan angi opptil 10 nivåer for hver vurderingsmodell.

6. Velg **Lagre**.

## <a name="create-a-skill"></a>Opprette en kompetanse

Før du kan tilordne en kompetanse eller opprette et kompetansesøk eller en kompetanseprofil, må du angi informasjon om kompetansen på **Kompetanse**-siden. Du kan velge en ferdighetstype og en vurderingsmodell for hver kompetanse.

1. Velg **Koblinger** i arbeidsområdet for **Ansattutvikling**.

2. Velg **Kompetanser** under **Kompetanseoppsett**.

3. Velg **Ny**.

4. Fyll ut følgende felt:

   - **Kompetanse**: Angi et navn på kompetansen.
   - **Beskrivelse**: Skriv inn en beskrivelse av kompetansen.
   - **Vurdering**: Velg vurderingsmodellen du vil bruke for denne kompetansen.
   - **Kompetansetype** – Velg fra listen over kompetansetyper.

5. Velg **Lagre**.

## <a name="see-also"></a>Se også

[Angi ferdigheter](hr-develop-enter-skills.md)<br>
[Kompetansesøk](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]