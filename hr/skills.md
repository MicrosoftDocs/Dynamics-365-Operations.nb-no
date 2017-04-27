---
title: Justere kompetansen til arbeidsstyrken etter bedriftens behov
description: "Du kan følge opp ferdighetene som ansatte, søkere eller kontaktpersoner har eller bør ha for å oppfylle rollen effektivt. Du kan også angi kompetansen som kreves for en bestemt jobb."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 720a1f272948eb310dc3cd02588aeec40b556d20
ms.openlocfilehash: 31dda85ff2e4a4e5380401b031b2dd74acff394b
ms.lasthandoff: 03/31/2017


---

# <a name="align-workforce-skills-with-business-needs"></a>Justere kompetansen til arbeidsstyrken etter bedriftens behov

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

<table>
<thead>
<tr class="header">
<th><strong>Obs! </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bare arbeidere, søkere eller kontaktpersoner som er valgt for inkludering i kompetansesøk, kan vises i resultatlisten for kompetansesøk eller inkluderes i en kompetanseprofil. Hvis du vil ta med en arbeider, søker eller kontaktperson i kompetansesøk, angir du valget <strong>Inkluder i kompetansesøk</strong> til Ja i de følgende sidene:
<ul>
<li>Arbeider</li>
<li>Ansatt</li>
<li>Søker</li>
<li>Kontakter</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>Kompetansegapanalyse og kompetanseprofilanalyse
Du kan opprette en analyse av kompetanseprofil for å vise en kompetanseliste for en arbeider, søker eller kontaktperson fra en bestemt dato. Du kan opprette en kompetansegapanalyse hvis du vil sammenligne kompetansen til en person med kompetansen som kreves for en bestemt jobb.  



<a name="see-also"></a>Se også
--------

[Personale](index.md)


