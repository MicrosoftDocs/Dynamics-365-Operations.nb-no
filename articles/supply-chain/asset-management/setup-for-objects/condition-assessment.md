---
title: Tilstandsvurdering
description: Dette emnet forklarer hvordan du oppretter en mal for tilstandsvurdering og registrerer deg for et aktivum i Aktivumbehandling.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5294325f67f0484b39194b5bd9784a2e612001a4
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783480"
---
# <a name="condition-assessment"></a>Tilstandsvurdering

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet forklarer hvordan du oppretter en mal for tilstandsvurdering og registrerer deg for et aktivum i Aktivumbehandling. Tilstandsvurdering utføres med jevne mellomrom, og det primære målet er å opprette og vedlikeholde tilstandsdata for aktiva. Sett fra et forebyggende vedlikeholdsperspektiv er det viktig å overvåke viktig informasjon som nåværende tilstand, og gjenværende levetid. Videre, hvis du utfører tilstandsvurdering med jevne mellomrom, vil du være i stand til å overvåke og sammenligne forholdene på maskineriet i fabrikken.

Tilstandsvurdering kan brukes til å måle og overvåke mange forhold på utstyret ditt. Eksempel: Du kan måle vibrasjoner på maskineriet. Etter at du har registrert vibrasjonsmålinger i Aktivumbehandling på ulike typer utstyr, kan du søke etter den siste registrerte vurderingen og vise vibrasjonsmålinger.

Tilstandsvurderingen opprettes på aktiva. Du definerer en mal for tilstandsvurdering for en aktivatype før du utfører tilstandsvurderingsprosedyren. Grunnen til å bruke maler for tilstandsvurdering er å unngå variasjon av tilstandsdata for lignende aktiva. Sekvensen for å definere og bruke tilstandsvurdering i Aktivumbehandling er: Først oppretter du de nødvendige malene for tilstandsvurdering. Deretter knytter du maler til ressurstyper i skjemaet **Aktivatyper**. Til slutt kan du opprette tilstandsvurderingsregistreringer for et aktivum i **Aktivum**-skjemaet.

## <a name="create-a-condition-assessment-template"></a>Opprette en mal for tilstandsvurdering

1. Velg **Aktivastyring** > **Oppsett** > **Aktivatyper** > **Tilstandsvurdering**.
2. Velg **Ny** for å opprette en ny mal.
3. Sett inn en ID for malen i **Mal**-feltet.
4. Sett inn et navn på malen i **Navn**-feltet.
5. På hurtigfanen **Tilstandsvurderingslinjer** legger du til linjene som kreves for tilstandsvurderingen, inkludert valg av riktig tilstandstype og målenhet.
6. På hurtigfanen **Aktivatyper** legger du til aktivatypene som skal bruke malen for tilstandsvurdering.
7. I feltene **Linjer** og **Aktivatyper** i **Detaljer**-gruppen øverst på skjermen ser du antallet tilstandslinjer og aktivatypene som er knyttet til den valgte malen for tilstandsvurdering.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Opprette tilstandsvurderingsregistrering på et aktivum

1. Velg **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.
2. I listen velger du aktivumet du vil opprette en tilstandsvurderingsregistrering for.
3. Gå til kategorien **Generelt**, og klikk **Tilstandsvurdering**.
4. Klikk **Ny** for å lage en ny registrering.
5. Velg datoen for tilstandsvurderingen i **Dato**-feltet.
6. Velg navnet på arbeideren som utførte tilstandsregistreringen, i **Arbeider**-feltet.
7. I **linjer**-feltet ser du antallet vurderingslinjer som er definert for tilstandsvurderingen.
8. Velg en mal for tilstandsvurderingen i **Mal**-feltet. Navnet på malen settes inn automatisk inn i **Navn**-feltet, og de relaterte registreringslinjene settes inn på hurtigfanen **Tilstandsvurderingslinjer**.
9. Du kan sette inn merknader knyttet til den valgte tilstandsvurderingen på hurtigfanen **Notater**.
10. For hver tilstandsvurderingslinje setter du inn målingsdata i **Verdi**-feltet.
11. Du kan sette inn en merknad knyttet til den valgte registreringslinjen på hurtigfanen **Tilstandsvurderingslinjer** > **Kommentarer**-feltet. Hvis du legger til en kommentar på en linje, merkes det det automatisk av for **Kommentar**.

Når du har foretatt en tilstandsvurderingsregistrering på et aktivum, kan du skrive ut en tilstandsvurderingsrapport.

>[!NOTE]
>Du kan også registrere en tilsynsvurdering på en arbeidsordre (**Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** > **Tilstandsvurdering**-knappen.)