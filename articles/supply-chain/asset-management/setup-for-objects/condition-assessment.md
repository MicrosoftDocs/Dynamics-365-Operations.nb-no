---
title: Tilstandsvurdering
description: Denne artikkelen forklarer hvordan du oppretter en mal for tilstandsvurdering og registrerer deg for et aktivum i Aktivumbehandling.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c43424a0955d7a046186e8a4120c050990df6060
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015063"
---
# <a name="condition-assessment"></a>Tilstandsvurdering

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen forklarer hvordan du oppretter en mal for tilstandsvurdering og registrerer deg for et aktivum i Aktivumbehandling. Tilstandsvurdering utføres med jevne mellomrom, og det primære målet er å opprette og vedlikeholde tilstandsdata for aktiva. Sett fra et forebyggende vedlikeholdsperspektiv er det viktig å overvåke viktig informasjon som nåværende tilstand, og gjenværende levetid. Videre, hvis du utfører tilstandsvurdering med jevne mellomrom, vil du være i stand til å overvåke og sammenligne forholdene på maskineriet i fabrikken.

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

1. Velg **Aktivastyring** > **Aktiva** > **Alle aktiva**.
2. I listen velger du aktivumet du vil opprette en tilstandsvurderingsregistrering for.
3. Gå til fanen **Generelt**, og klikk **Tilstandsvurdering**.
4. Klikk på **Ny** for å lage en ny registrering.
5. Velg datoen for tilstandsvurderingen i **Dato**-feltet.
6. Velg navnet på arbeideren som utførte tilstandsregistreringen, i **Arbeider**-feltet.
7. I **linjer**-feltet ser du antallet vurderingslinjer som er definert for tilstandsvurderingen.
8. Velg en mal for tilstandsvurderingen i **Mal**-feltet. Navnet på malen settes inn automatisk inn i **Navn**-feltet, og de relaterte registreringslinjene settes inn på hurtigfanen **Tilstandsvurderingslinjer**.
9. Du kan sette inn merknader knyttet til den valgte tilstandsvurderingen på hurtigfanen **Notater**.
10. For hver tilstandsvurderingslinje setter du inn målingsdata i **Verdi**-feltet.
11. Du kan sette inn en merknad knyttet til den valgte registreringslinjen på hurtigfanen **Tilstandsvurderingslinjer** > **Kommentarer**-feltet. Hvis du legger til en kommentar på en linje, merkes det det automatisk av for **Kommentar**.

Når du har foretatt en tilstandsvurderingsregistrering på et aktivum, kan du skrive ut en tilstandsvurderingsrapport.

>[!NOTE]
>Du kan også registrere en tilsynsvurdering på en arbeidsordre (**Aktivastyring** > **Arbeidsordrer** > **Alle arbeidsordrer** > **Tilstandsvurdering**-knappen.)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]