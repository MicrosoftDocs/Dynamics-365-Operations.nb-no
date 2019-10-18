---
title: Justere kompetansen til arbeidsstyrken etter bedriftens behov
description: Du kan følge opp ferdighetene som ansatte, søkere eller kontaktpersoner har eller bør ha for å oppfylle rollen effektivt. Du kan også angi kompetansen som kreves for en bestemt jobb.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: d5fe56c949975f8cd07b54308cec43f833cc9d69
ms.sourcegitcommit: 0dd8d0510214f92936a9dd214b404c5c8103587b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2419229"
---
# <a name="align-workforce-skills-with-business-needs"></a>Justere kompetansen til arbeidsstyrken etter bedriftens behov

[!include [banner](includes/banner.md)]

Du kan følge opp ferdighetene som ansatte, søkere eller kontaktpersoner har eller bør ha for å oppfylle rollen effektivt. Du kan også angi kompetansen som kreves for en bestemt jobb.

Eksempler på kompetanser du kan spore, omfatter følgende:
-   Tilsyn – Evne til å overvåke andres arbeid.
-   Ledelse – Evne til å lede ansatte og forretningsområder.
-   Planlegging – Evne til å tenke fremover, forme fremtidsplaner og gjennomføre dem.
-   HTML – Evne til å skrive HTML-kode.

Før du kan tilordne en kompetanse til en person eller en jobb, opprette et kompetansesøk eller opprette en kompetanseprofil, må du angi informasjon om kompetansen på **Kompetanse**-siden. Du kan velge en ferdighetstype og en vurderingsmodell for hver kompetanse.

## <a name="rating-models"></a>Vurderingsmodeller
Vurderingsmodeller bidrar til å vurdere en persons faktiske kompetansenivå, nivået de bør arbeide for å oppnå, eller kompetansenivået som kreves for en jobb. Du kan angi opptil ti nivåer for en vurderingsmodell.  Hvert nivå i en vurderingsmodell tilordnes en faktor.  Omregningsverdien brukes til å normalisere resultatene for kompetanse som bruker forskjellige vurderingsmodeller.  Faktoren må være et tall mellom 0-9 og hvert nivå må ha en unik faktor  Nivåer med høyere faktorverdier vektlegges mer i en vurderingsmodell.

## <a name="specify-job-skills"></a>Angi jobbkompetanse
Når du angir informasjon om en jobb, kan du angi kompetansen som en person skal ha for å utføre arbeidet som kreves for jobben.  I tillegg kan du angi ønsket nivå for hver type kompetanse samt betydningsnivåer til kompetansen. Forskjellige jobber kan kreve forskjellige betydningsnivåer for den sammen kompetansen.

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>Angi kompetanse for ansatte, søkere eller kontakter
Du kan angi målkompetanse eller faktisk kompetanse for arbeidere, søkere eller kontakter. En målkompetanse er en kompetanse en person ønsker å oppnå. En faktisk kompetanse er en kompetanse en person har.

## <a name="skill-mapping-and-skill-mapping-profiles"></a>Kompetansetilordning og kompetansetilordningsprofiler
Du kan opprette et kompetanesøk for å finne en arbeider, søker eller kontaktperson som er kvalifisert til å utføre en bestemt type oppgave. Kompetanesøk søker på tvers av ferdigheter, utdanning, sertifikater, tillitsverv og prosjekterfaring, og returnerer et resultat som samsvarer med kriteriene som er angitt.  Det kan for eksempel være nyttig å vite hvilke ansatte i organisasjonen som har opptjent deres CPA.

Med profiler for kompetansesøk kan du søke etter nåværende ansatte eller kandidater med kvalifikasjoner som direkte samsvarer med bedriftens behov.  Du kan for eksempel opprette en profil for kompetansesøk for en åpen stilling i organisasjonen. Ved å opprette en profil for en bestemt jobb og kopiere kompetanse, utdanning og sertifikater fra denne jobben til profilen, kan du raskt søke arbeidere, søkere og kontaktpersoner som samsvarer med ett eller flere av kriteriene som er angitt på profilen, og vise en liste over kandidater som har kvalifikasjoner som nærmest oppfyller kompetansen som kreves for jobben.

> **Obs!** Bare arbeidere, søkere eller kontaktpersoner som er valgt for inkludering i kompetansesøk, kan vises i resultatlisten for kompetansesøk eller inkluderes i en kompetanseprofil. Hvis du vil ta med en arbeider, søker eller kontaktperson i kompetansesøk, angir du valget **Inkluder i kompetansesøk** til Ja i de følgende sidene:
> 
> + Arbeider
> + Ansatt
> + Søker
> + Kontakter

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>Kompetansegapanalyse og kompetanseprofilanalyse
Du kan opprette en analyse av kompetanseprofil for å vise en kompetanseliste for en arbeider, søker eller kontaktperson fra en bestemt dato. Du kan opprette en kompetansegapanalyse hvis du vil sammenligne kompetansen til en person med kompetansen som kreves for en bestemt jobb.  



<a name="additional-resources"></a>Tilleggsressurser
--------

[Personale](index.yml)



