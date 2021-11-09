---
title: Generer varianter for tekniske produkter
description: Dette emnet beskriver hvordan du genererer varianter for tekniske produkter
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e24bceac9457212ecaafda876d19ba62df049371
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/27/2021
ms.locfileid: "7471842"
---
# <a name="generate-variants-for-engineering-products"></a>Generer varianter for tekniske produkter

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du genererer varianter for tekniske produkter.

## <a name="turn-on-variant-generation-for-engineering-products"></a>Slå på variantgenerering for tekniske produkter

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Behandling av teknisk endring*
- **Funksjonsnavn:** *Variantgenerering for tekniske produkter*

> [!IMPORTANT]
> Funksjonen *Variantgenerering for tekniske produkter* vil bare være synlig i systemet etter at du har aktivert konfigurasjonsnøkkelen *Behandling av teknisk endring*. Hvis du vil ha mer informasjon, kan du se [Oversikt over behandling av teknisk endring](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Generere en eller flere nye varianter av et teknisk produkt

Du kan opprette en eller flere nye varianter av et produkt uten å kopiere informasjon fra et eksisterende produkt. Dette er nyttig når du skal opprette flere produktvarianter samtidig.

Følgende fremgangsmåte gir et eksempel på hvordan du oppretter flere varianter som inneholder fargedimensjonen.

1. Åpne **Frigitte produkter**-siden (for eksempel gå til **Styring av teknisk endring \> Felles \> Frigitte produkter**).
1. I handlingsruten åpner du **Produkt**-fanen og fra **Ny**-gruppen velger du **Teknisk produkt**.
1. Dialogboksen **Nytt produkt** åpnes. Velg den aktuelle **tekniske kategorien**.
1. Hvis den valgte tekniske kategorien inneholder variantdimensjoner, kan du angi verdier for dem nå. Hvis kategorien har en **fargedimensjon**, kan du for eksempel sette den til *Blå*.
1. Gjør andre innstillinger etter behov. Velg **OK** for å opprette produktet.
1. Produktet og den blå V-1-varianten er opprettet, og det nye produktet åpnes nå.
1. Legg til en stykkliste og rute til varianten etter behov.
1. I handlingsruten åpner du **Produkt**-fanen og fra **Produktstandard**-gruppen, velger du **Produktdimensjoner**.
1. Siden **Produktdimensjoner** åpnes. Denne siden inneholder en fane for hver tilgjengelige dimensjon. Legg til en rad for hver verdi du vil støtte for hver relevante dimensjon, i hver fane. (I dette eksemplet kan du legge til rader i fanen **Farge** for *hvit*, *gul* og *grønn*).
1. Lukk siden, og velg deretter **Frigitte produktvarianter**. Legg merke til at den første varianten du har opprettet (blå V-1), vises.
1. Velg **Variantforslag** i fanen **Produktvariant** i handlingsruten.
1. Følg et av disse trinnene i dialogboksen **Variantforslag**:

    - Øverst i dialogboksen finner du en del for hver tilgjengelige dimensjon. For hver dimensjon merker du av for hver verdi du vil generere et variantforslag for, og deretter velger du **Foreslå** på verktøylinjen. Relevante forslag legges til i **Foreslåtte varianter**-delen.
    - Velg **Foreslå alle** på verktøylinjen for å generere variantforslag for alle tilgjengelige kombinasjoner av dimensjonsverdier. Forslagene legges til i **Foreslåtte varianter**-delen.

1. Merk av for hver variant du vil opprette, i delen **Foreslåtte varianter**. Velg deretter **Opprett** for å generere og frigi de valgte variantene til det tekniske firmaet. Følgende betingelser gjelder:

    - Ingen av de opprettede variantene vil ha en stykkliste eller rute.
    - Attributtene for disse variantene hentes som standard fra den tekniske kategorien, og kopieres ikke fra den forrige varianten.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Generer en variant som en kopi av en annen produktvariant

Du kan opprette en variant av et produkt basert på en annen produktvariant. Stykklisten og ruten fra kildeproduktvarianten kopieres til den nye varianten. Dette kan være nyttig for atskilte produksjonsprodukter der det kan være nyttig å opprette stykklisten basert på en startstykkliste og holde oversikt over endringene fra den forrige varianten. For å vedlikeholde sporbarhet registrerer systemet hvilken variant som ble kopiert til å opprette en ny kopi.

Følgende fremgangsmåte gir et eksempel på hvordan du oppretter en ny variant som inkluderer fargedimensjonen, ved å opprette en kopi av en eksisterende variant

1. Åpne **Frigitte produkter**-siden (for eksempel gå til **Styring av teknisk endring \> Felles \> Frigitte produkter**).
1. I handlingsruten åpner du **Produkt**-fanen og fra **Ny**-gruppen velger du **Teknisk produkt**.
1. Dialogboksen **Nytt produkt** åpnes. Velg den aktuelle **tekniske kategorien**.
1. Hvis den valgte tekniske kategorien inneholder variantdimensjoner, kan du angi verdier for dem nå. Hvis kategorien har en **fargedimensjon**, kan du for eksempel sette den til *Blå*.)
1. Gjør andre innstillinger etter behov. Velg **OK** for å opprette produktet.
1. Produktet og den blå V-1-varianten er opprettet, og det nye produktet åpnes nå.
1. Legg til en stykkliste og rute til varianten etter behov.
1. Legg til attributter i produktvarianten etter behov.
1. Legg til den blå V-1-produktvarianten i en ordre om teknisk endring.
1. Angi **Innvirkning** på *Ny variant*.
1. Velg den nye fargeverdien (for eksempel *Hvit*). Vær oppmerksom på at følgende betingelser gjelder: 
    - Den nye varianten har en stykkliste og rute som er kopiert fra den forrige varianten.
    - Den nye varianten har attributtene kopiert fra den forrige varianten.
1. Godkjenn endringsordren.
1. Behandle endringsordren. Når ordren er behandlet, opprettes og frigis den nye V-1-varianten til det tekniske firmaet.
