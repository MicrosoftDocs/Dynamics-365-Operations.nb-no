---
title: Strømlinjeformet ansattoppføring og navigasjon
description: Dataregistrering for arbeidere i Dynamics 365 for Talent er forbedret for å tillate rask registrering for alle ansatte, tidligere, aktive eller fremtidige. En forenklet/konsolidert navigasjonsmodell er oppdatert for å finne relatert informasjon raskt og vise og foreta eventuelle nødvendige oppdateringer.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: be0253ffc4396f36050ef02c51a20d378e44473d
ms.sourcegitcommit: 4176c333ce3f88c5c68e95bd47e5791d32365dd2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1918215"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Strømlinjeformet ansattoppføring og navigasjon

[!include [banner](includes/banner.md)]

Dynamics 365 for Talent muliggjør effektiv registrering av ansatte og ansettelsesdata. Du kan raskt oppdatere arbeidshistorikkinformasjon for tidligere, aktive og fremtidige ansatte og oppdragstakere.

Du kan også aktivere en forenklet navigasjonsopplevelse for å finne relatert informasjon raskt og foreta eventuelle nødvendige endringer. Denne funksjonaliteten er nå tilgjengelig i sandkassemiljøer. Hvis du vil aktivere denne funksjonen, går du til **Systemadministrasjon > Koblinger > Oppsett > Systemparametere> Forhåndsvisningsfunksjoner**. Velg **Utvidet arbeiderskjema og navigering**. Dette vil aktivere disse endringene for alle brukere. Du kan når som helst deaktivere dette alternativet.

## <a name="view-options"></a>Visningsalternativer

Du kan bruke **Visningsalternativer** i arbeiderskjemaet til å velge en kombinasjon av ansatte og oppdragstakere fra én liste. Med disse alternativene kan du vise arbeidere på tvers av juridiske enheter eller for den juridiske enheten du er pålogget for øyeblikket. Du kan også vise aktive, ventende og arbeidere som har sluttet, og du kan begrense resultater basert på typen arbeider (ansatt eller oppdragstaker). Hvis avansert sikkerhet er aktivert, vil du bare se ansatte og oppdragstakere i de juridiske enhetene du har tilgang til.

Kolonner i listevisningen endres basert på valgene dine. Når du for eksempel viser ansatte som har sluttet, vises sluttdatoen og årsakskodene som tilleggskolonner i listen. 

[![Visningsalternativer](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>Navigasjon og banner

Et banner viser nøkkelinformasjon for hver arbeider. Banneret for aktive arbeidere viser følgende felt:

- **Stillingstittel**
- **Avdeling**
- **Stillingstype**
- **Arbeidertype**
- **Leder**
- **Juridisk enhet**

Banneret for arbeidere som har sluttet, viser følgende felt:

- **Sluttdato**
- **Årsak**

Banneret for ventende ansatte viser følgende felt:

- **Stillingstittel**
- **Avdeling**
- **Stillingstype**
- **Leder**
- **Startdato**
- **Juridisk enhet**

Handlingsruten på siden for arbeideren er omorganisert for å inkludere færre alternativer. Informasjonen er nå organisert i følgende kategorier: 

- Arbeid
- Person
- Permisjon
- Kompensasjon
- Fordeler
- Samsvar

I tillegg gir den nye kategorien **Koblinger** på hovedsiden for arbeideren brukerne en sentral plassering der de kan få tilgang til all relatert informasjon for en arbeider.

På grunn av disse endringene kan informasjon vises på et annet sted enn du er vant til. Lønnsinformasjon som tidligere ble vist i arbeiderskjemaet, vises for eksempel nå i handlingsruten under **Kompensasjon > Lønn**, og kategorien **Personlige opplysninger** har nå en **Mer informasjon**-knapp for å skjule felt som ikke brukes så ofte.

[![Banner](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>Arbeidshistorikk

Kategorien **Arbeidshistorikk** viser arbeidshistorikken for alle juridiske enheter og er tilgjengelig for aktive og ventende ansatte og oppdragstakere samt de som har sluttet. Du kan nå vise all arbeidshistorikk samtidig for de juridiske enhetene du har tilgang til. I tillegg kan du redigere informasjon for hver av arbeidshistorikkoppføringene uten å endre datakonteksten. Du kan oppdatere all informasjon direkte på siden. 

[![Arbeidshistorikk](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Stillingshistorikk

Kategorien **Stillinger** på hovedsiden for arbeidere gir en full oversikt over alle stillinger i organisasjonen, inkludert tidligere, nåværende og fremtidige utnevnelser. Du kan fortsatt navigere direkte til arbeiderens stillingshistorikk i handlingsruten også.

[![Stillinger](./media/Worker-position-history.png)](./media/Worker-position-history.png)

