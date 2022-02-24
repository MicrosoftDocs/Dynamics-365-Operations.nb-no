---
title: Intelligente anbefalinger i Attract
description: Denne artikkelen forklarer hvordan maskinopplæring kan brukes til å gi anbefalinger for jobber og jobbkandidater i Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: fa06821c98e42dcd8590a764db9beb4a5c33fca2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462068"
---
# <a name="intelligent-recommendations-in-attract"></a>Intelligente anbefalinger i Attract

[!include [banner](includes/banner.md)]

Maskinopplæring kan hjelpe rekrutteringspersoner og ansettelsesansvarlige med å finne kandidater til en stilling raskt. Det kan også hjelpe kandidater med å finne stillingene som passer best til deres profil og interesser. Etterhvert som disse funksjonene brukes, og det gis tilbakemelding, forbedres anbefalinger.

> [!NOTE] 
> - De intelligente anbefalingsfunksjonene er bare tilgjengelige med [tillegget for omfattende ansettelse](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Funksjonalitet som er nevnt i dette emnet, er tilgjengelig som en del av en forhåndsversjon. Innholdet og funksjonaliteten kan bli endret. Hvis du vil bruke denne funksjonen, kan du be administratoren om å aktivere den ved hjelp av **Administrasjonssenter** i Attract. Sett **Kandidatanbefaling**, **Jobbanbefaling** og **Kundeemneanbefaling** til **På**. Hvis du vil ha mer informasjon, se [Tilgang til forhåndsvisningsfunksjoner i Microsoft Dynamics 365 Talent](./access-preview-feature.md). 


## <a name="candidate-recommendations"></a>Kandidatanbefalinger

Fordi ledige stillinger kan trekke til seg hundrevis av søkere, kan det være vanskelig for rekrutteringspersoner og ledere som ansetter, å finne kandidatene med kompetansen og bakgrunnen som samsvarer best med stillingen. Ved å analysere sammenhengen mellom jobbeskrivelsen og krav, og data fra kandidaters CV-er og profiler, kan maskinlæring brukes til å produsere kandidatanbefalinger. Kandidatanbefalinger kan hjelpe rekrutteringspersoner og ansettelsesansvarlige med å finne de beste talentene og flytte dem raskere til intervjustadiet. Hvis det er mer enn ti kandidater som har CV-er eller fullstendige profiler, kan kandidatene som nærmest oppfyller jobbkravene, vises i delen **Søkere som bør vurderes** på siden **Jobb**.

For hvilken som helst anbefalt kandidat kan du velge **Vis kandidat** på kandidatkortet for å gå gjennom kandidatens profil og iverksette handling på vedkommendes søknad. Du kan bruke ellipseknappen (**...**) til å åpne kandidatens profil i en ny kategori. Du kan også bruke ellipseknappen til å gi tilbakemelding om anbefalingen. På denne måten kan bidra du til å finjustere anbefalingsmotoren og forbedre fremtidige anbefalinger. Anbefalinger som du ikke liker, fjernes fra delen **Søkere som bør vurderes** når du oppdaterer **Jobb**-siden. Du kan bruke tilbakemeldingskortet til å angi hvorfor du ikke synes at anbefalingen var nyttig.

## <a name="job-recommendations"></a>Jobbanbefalinger 

Når en potensiell ansatt bruker karriereområdet til å søke på en jobb, anbefaler Attract andre ledige stillinger i organisasjonen. Anbefalingene er basert på tidligere søknader og CV-en eller profilen til kandidaten. Derfor hjelper jobbanbefalinger kandidater med å raskt identifisere jobbene som passer best for disse. Jobbanbefalinger gis til kandidater hvis mer enn ti jobber er postert på karriereområdet. Kandidater kan åpne detaljer for en jobbpostering fra anbefalingskortet. De kan også gi tilbakemelding om en anbefaling for å forbedre fremtidige anbefalinger.

## <a name="prospect-recommendations"></a>Kandidatanbefalinger 

Når en ny stilling blir tilgjengelig, kan det ta litt tid å søke gjennom alle tidligere søkere og hele talentnettverket. For å la Attract hjelpe deg med dette kan du bruke intelligente maskinlæringsalgoritmer. Dette betyr at Attract går gjennom alle kandidater og foreslår de som er en god match, så snart du oppretter prosjektet. Hvis du vil vise disse anbefalingene, kan du aktivere **Jobbkandidat**-stadiet for jobben. Det kan ta opptil ett minutt for Attract å skanne hele kandidatdatabasen for å gjøre anbefalinger.

Anbefalingene vises som kort i **Jobbkandidat**-kategorien for alle jobber som har **Jobbkandidat**-trinnet aktivert. Disse kortene viser ferdighetene i jobbkandidatens profil i tillegg til eventuell utdanninginformasjon. Hvis du finner en anbefaling du liker, kan du legge til kandidaten som en jobbkandidat for denne jobben.

> [!NOTE]
> Hvis du nylig startet ved hjelp av Attract, må du vente til du har 10 eller flere søkere som har fulle profiler eller CVer, før du kan bruke denne funksjonen.

Hvis du vil unngå potensielle avvik i anbefalingene, skanner Attract bare kandidatprofiler for ferdigheter, kvalifikasjoner og andre nøkkelord som samsvarer med jobbeskrivelsen. I tillegg fjerner Attract personlig identifiserbar informasjon fra kandidatprofiler før evaluering.
