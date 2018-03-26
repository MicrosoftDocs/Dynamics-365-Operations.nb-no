---
title: Cenerer rapporter om Affordable Care Act
description: "Funksjonalitet er tilgjengelig for å hjelpe arbeidsgivere som trenger å spore opplysningene som er rapportert på skjema 1095-B og 1095-C til støtte for Employer Mandate-delen av Affordable Care Act. Merk at denne funksjonaliteten bare er aktivert for juridiske personer i USA."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 1994edc5d6c932be3a285f9bb328a05504c90f07
ms.contentlocale: nb-no
ms.lasthandoff: 03/08/2018

---
# <a name="generate-affordable-care-act-reports"></a>Cenerer rapporter om Affordable Care Act

[!include[banner](includes/banner.md)]

Funksjonalitet er tilgjengelig for å hjelpe arbeidsgivere som trenger å spore opplysningene som er rapportert på skjema 1095-B og 1095-C til støtte for **Employer Mandate**-delen av Affordable Care Act. Merk at denne funksjonaliteten bare er aktivert for juridiske personer i USA.

## <a name="getting-started"></a>Komme i gang
Når du begynner å spore informasjon som skal rapporteres på 1095-B-og 1095-C, må du først opprette én eller flere rimelig dekningsgrupper for Affordable Care. Disse Affordable Care-dekningsgruppene brukes til å angi tilbudet om dekning som ble gitt til en ansatt, den ansattes andel av det rimeligste månedlige premien (hvis kostnaden er høyere enn den føderale fattigrensen) i tillegg Safe Harbor som brukes av arbeidsgiveren, dersom det er aktuelt. Ved å bruke Affordable Care Act-grupper kan du behandle informasjonen for disse feltene uten å måtte røre hver ansattpost der betingelsene er de samme. I tillegg kan Affordable Care-dekningsgrupper lett tilordnes til én eller flere ansatte ved hjelp av massetilordningsfunksjonen på siden.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Vedlikeholde flere versjoner av en dekningsgruppe
Du kan vedlikeholde flere versjoner av en dekningsgruppe, noe som gjør det mulig å gjøre endringer som holder gruppens informasjonen oppdatert, uten å måtte opprette en ny gruppe og tilordne ansatte til denne når noe endres i organisasjonen eller i fordelene som tilbys. 

Når du har opprettet Affordable Care-dekningsgruppene du trenger, kan du velge å massetilordne gruppene til ansatte ved hjelp av funksjonen **Massetilordning** på siden, eller du kan gå til hver ansatt og angi om ACA-informasjon må spores og rapporteres for den ansatte samt tilordne den ansatte til en Affordable Care-dekningsgruppe.

Hvis Affordable Care-dekningsinformasjonen ikke må spores eller rapporteres for en ansatt, for eksempel hvis de er deltidsansatt, kan feltet **Rapporter dekning** settes til Nei. Selv om hver ansatt som det må spores ACA-informasjon for, må tilordnes til en Affordable Care-dekningsgruppe, kan du likevel endre alternativene **Tilbud om dekning**, **Ansattdel av kostnad** og **Safe Harbor** for en hvilken som helst måned – eller måneder – som kan trenge andre verdier enn de som er angitt i Affordable Care-dekningsgruppen.

Hvis du vil angi unntak for noen av Affordable Care-dekningsgruppenes verdier, klikker du på koblingen Affordable Care-dekning på informasjonssiden for arbeidere, som er under delen mer informasjon i kategorien ansettelse.

## <a name="reporting-health-care-coverage"></a>Rapportere helsedekning
I tillegg til å spore hva skjer hvis en hvilken som helst helseforsikringsdekning ble tilbudt en heltidsansatt, hvis arbeidsgiveren arbeidsgiversponset selvforsikret helsedekning som den ansatte dekkes under (uavhengig av om de jobber fulltid eller deltid), må tilleggsinformasjon rapporteres på 1095-C. Hver ansatt (inkludert avhengige) som er dekket av arbeidsgiver-sponsede fordelsplaner, må tas med i rapporten for månedene de var dekket. 

Du kan angi om hver fordelsplan må rapporteres eller ikke, ved å merke av for **ACA-rapporterbar**.

Dessuten, hvis ansatte har valgt å dekke noen av sine avhengige under en fordel, kan du angi datoene den avhengige ble dekket, for hver ansatt, på siden Vedlikehold fordeler. Du angir at den avhengige dekkes inn under fordelen ved å velge Rediger i handlingsruten på hurtigfanen Avhengige.

På siden **Behandling for dekningsdato for avhengig** kan du angi datoene da den avhengige ble dekket av fordelen. Når det angis datoer på denne siden, merkes det automatisk av for **Dekket** på **Vedlikehold fordeler**-siden.

## <a name="generate-1095b-and-1095c-forms"></a>Generere skjemaene 1095B og 1095C
Du kan også generere 109-B- og 1095-C-skjemaer fra produktet, og levere dem til alle ansatte. Elektronisk generering av 1095-C og tilhørende 1094-C-overføringsfiler som kan brukes til å sende til Skattemyndighetene, kan også genereres fra systemet.  

Når du genererer 1095-C-skjemaet, angir i kalenderen eller skatteåret samt om du vil skrive ut skjemaet med to sider eller skjemaer med tre sider. Skjemaet med tre sider er bare nødvendig hvis arbeidsgiveren ga selvforsikret dekning og en ansatt har mer en seks dekkede avhengig, inkludert seg selv. Når skjemaet med to sider genereres, finner systemet automatisk ut om en ansatt har mer enn 6 avhengige dekket, og vil ikke ta med den ansatte når skjemaet genereres. Når skjemaet med tre sider genereres, vil systemet dessuten bare ta med bare de ansatte som har mer enn seks avhengige dekket.

## <a name="viewing-information"></a>Vise informasjon
Du kan bruke siden **Affordable Care-dekning for arbeidere** hvis du vil se hvilke ansatte som er tilordnet til hver dekningsgruppe, hvilke ansatte som ikke trenger å være med i en rapport, og hvilke ansatte som ikke er tilordnet.

Hvis noen av standardverdiene fra Affordable Care-dekningsgruppen har blitt overstyrt, vises en stjerne ved siden av verdien som ble endret. Hvis verdiene for alle tolv månedene er de samme, og ikke har blitt overstyrt, skrives verdien ut i **Alle 12 måneder**-kolonnen.

Du kan også bruke vinduet for forespørsel for å forstå hvilke ansatte som er flagget som ikke ACA-rapporterbare, noe som betyr at du ikke trenger å analysere dekningen de ble tilbudt og at du ikke trenger ikke å utstede et 1095-C til dem på slutten av året. Ved å velge **Ikke ACA-rapporterbar** i **Filtrer**-feltet kan du generere en liste over alle ansatte som er flagget til ikke å motta 1095-C.

I tillegg til å vise en liste over ansatte som ikke er ACA-rapporterbare, kan du også vise alle ansatte som ikke er tilordnet (**ACA-rapportens dekningsfelt** er tomt) eller som er knyttet til en Affordable Care-dekningsgruppe som er utløpt for året som er valgt i **år**-feltet.

Du kan eksportere lister over ansatte som ble generert ved hjelp av noen av alternativene for filtrering til Excel.

Hvis du har behov for å rapportere dekkede enkeltpersoner fordi du gir selforsikret dekning, kan du også vise alle avhengige som dekkes under fordelsplaner som er merket som **ACA-rapporterbare** ved å velge handlingen Vis avhengig dekning i handlingsrutestripen.

**Merk:** Bare fordeler i en plan som er merket som **ACA-rapporterbar**, vises i forespørselsvinduet.

