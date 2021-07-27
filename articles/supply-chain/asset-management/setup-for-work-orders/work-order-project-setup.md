---
title: Prosjektoppsett for arbeidsordre
description: Dette emnet forklarer prosjektoppsett for arbeidsordre i Aktivastyring.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 19cdc33fcc9d1293b235facbaffd1ccf62875217
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360059"
---
# <a name="work-order-project-setup"></a>Prosjektoppsett for arbeidsordre

[!include [banner](../../includes/banner.md)]

 

I modulen **Aktivastyring** kreves det en prosjektrelasjon for hver arbeidsordrejobb. Prosjektet som er knyttet til en arbeidsordrejobb, lar deg spore kostnader på forskjellige prosjekter som er relatert til Aktivastyring, for eksempel interne vedlikeholdsprosjekter, servicestyringsprosjekter og investeringsprosjekter. 

## <a name="project-setup-for-a-work-order-job"></a>Prosjektoppsett for en arbeidsordrejobb

Når du oppretter en arbeidsordrejobb i en arbeidsordre, bestemmer prosjektoppsettet i modulen **Prosjektstyring og regnskap** og prosjektoppsettet for arbeidsordre i modulen **Aktivastyring** hvordan prosjekter kan brukes til kostnadskontroll for anleggsmidlet som er valgt for denne arbeidsordrejobben. Denne delen beskriver følgende deler i prosjektoppsettet som brukes for en arbeidsordre: det overordnede prosjektet (prosjekt-ID), prosjekttype, prosjektaktiviteter og finansdimensjoner:

- Når du oppretter en arbeidsordrejobb i en arbeidsordre, opprettes det automatisk en unik prosjekt-ID og en relatert prosjektaktivitet for den. Hvis imidlertid flere arbeidsordrejobber i en arbeidsordre inkluderer samme anleggsmiddel, brukes den samme prosjekt-ID-en for dem. Med andre ord opprettes det én prosjekt-ID for hvert anleggsmiddel i en arbeidsordre.

    - Du finner hovedprosjektet (prosjekt-ID) for en arbeidsordrejobb i det overordnede prosjektoppsettet. (Hvis du vil ha mer informasjon om hovedprosjektoppsettet, kan du se neste del.) Hvis du for eksempel knytter en kunde eller et arbeidssted til et bestemt overordnet prosjekt, brukes det overordnede prosjektet hver gang du oppretter arbeidsordrer for denne kunden eller dette arbeidsstedet. Hvis du ikke knytter en bestemt prosjekt-ID til for eksempel et arbeidssted, brukes det neste relevante overordnede prosjektet i prosjektoppsettet for arbeidsordren.
    - En prosjekttype kreves for hver prosjekt-ID. Prosjekttypen finnes i oppsettet av prosjektgruppeoppsettet. (Hvis du vil ha mer informasjon om prosjektgruppeoppsettet, kan du se neste del.) Hvis det ikke blir funnet noen treff for prosjektgruppeoppsettet, brukes prosjektgruppeoppsettet for det overordnede prosjektet.
    - Oppsettet for å kreve prosjektaktiviteter i prognoser og journaler kopieres fra hovedprosjektet til arbeidsordreprosjektet. Hvis alternativene **Time**, **Utgift** og **Vare** er satt til **Ja** for prosjektet som brukes som et hovedprosjekt, er en prosjektaktivitet obligatorisk på prognoser og journaler. (Hvis du vil ha tilgang til disse alternativene, velger du **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**, og deretter velger du prosjektet som brukes som et overordnet prosjekt. Alternativene er i delen **Krev aktivitet i journaler** i hurtigfanen **Oppsett**.)

- Finansdimensjoner kopieres fra aktivumet og slås sammen med det overordnede prosjektet.

Den neste delen forklarer hvordan du definerer overordnede prosjekter og prosjektgrupper. Overordnede prosjekter og overordnede grupper brukes til å kontrollere arbeidsordrer. De brukes også til å rapportere om arbeidsordrer.

## <a name="set-up-work-order-projects"></a>Definere prosjekter for arbeidsordrer

Før du begynner å opprette arbeidsordrer, må du opprette arbeidsordreprosjekter. Siden **Prosjektoppsett for arbeidsordre** (**Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Prosjektoppsett**) inneholder to kategorier: **Overordnet prosjekt** og **Prosjektgruppe**.

I fanen **Overordnet prosjekt** kan du definere prosjektrelasjoner som kan brukes hvis det ikke er definert et prosjekt for anleggsmidlet som er valgt i arbeidsordrejobben. Det kreves ikke et overordnet prosjektoppsett hvis firmaet ditt bruker anleggsmiddelprosjekter. Det er bare relevant hvis du vil bruke arbeidsordreprosjekter i stedet for anleggsmiddelprosjekter. I så fall må du definere minst ett overordnet prosjekt.

I fanen **Prosjektgruppe** kan du definere prosjektgrupper som kan knyttes til arbeidsordretyper, anleggsmiddeltyper og anleggsmidler.

Prosjektgrupper kan brukes til å opprette bestemte kategorier (grupper) som brukes i kostnadskontroll. Ved å opprette prosjektgrupper for bestemte anleggsmiddeltyper eller arbeidsordretyper, kan du for eksempel utføre detaljert sporing av vedlikeholdskostnader etter type.

Prosjektgrupper er ikke obligatorisk. Hvis du ikke definerer prosjektgrupper, brukes det overordnede prosjektet til å fastsette prosjektgruppen, og et underordnet prosjekt opprettes fra prosjektgruppen for det overordnede prosjektet.

Oppsettet tillater fullstendig integrasjon med **Prosjektstyring og regnskap**-modulen. Du kan derfor spore kostnadene som er knyttet til arbeidsordrer, i de tilknyttede prosjektene. Følgende fremgangsmåte beskriver oppsettet av arbeidsordreprosjekter.

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Prosjektoppsett**.
2. I fanen **Overordnet prosjekt**, velg **Legg til**.
3. Velg verdier etter behov i feltene **Arbeidsordretype**, **Arbeidssted**, **Aktivumtype** og **Aktivum**. For hver linje du legger til, kan du bare angi ett felt eller flere felt. Antallet felt du angir, bestemmer kombinasjonen som brukes når en prosjekt-ID velges i Aktivastyring. 

    Hvis du velger et arbeidssted, inkluderes de tilknyttede underordnede stedene automatisk. Hvis du velger et aktivum, kan du opprette flere linjer for arbeidsordreprosjektoppsett for samme anleggsmiddel, men du kan velge forskjellige prosjekter for dette anleggsmidlet.

4. I **Prosjekt-ID**-feltet velger du prosjektet som skal knyttes til oppsettet du opprettet i trinn 3.
5. Hvis prosjektoppsettet bare skal være gyldig i en begrenset periode, velger du en sluttdato i **Sluttdato**-feltet. Ellers velger du **Ingen**.

    Som standard er startdatoen datoen da du legger til arbeidsordreprosjektet på siden. Den styres av feltet **Gyldig fra**, som er skjult som standard. Hvis du vil vise **Gyldig fra**-feltet, velger du **Vis** \> **Alle**. Du kan deretter bruke **Gyldig fra**-feltet sammen med **Sluttdato**-feltet til å definere en begrenset gyldighetsperiode for arbeidsordreprosjektet.

    ![Siden for prosjektoppsett for arbeidsordre.](media/17-setup-for-work-orders.png)

6. I fanen **Prosjektgruppe**, velg **Legg til**.
7. Velg en arbeidsordretype i feltet **Arbeidsordretype**.
8. Hvis du vil at prosjektgruppetilknytningen skal være mer spesifikk, velger du en aktivumtype i **Aktivumtype**-feltet eller et aktivum i **Aktivum**-feltet.
9. I **Prosjektgruppe**-feltet velger du prosjektgruppen som skal knyttes til arbeidsordretypen. En arbeidsordretype med navnet **Forebyggende vedlikehold** kan for eksempel knyttes til en prosjektgruppe med navnet **Tidl vedl** eller **Intern**. Eventuelt kan arbeidsordretypen **Investering** som brukes for arbeidsordrer som er knyttet til investeringer og anleggsmidler, knyttes til en prosjektgruppe som heter **Invest** eller **Investering**.
10. Velg **Lagre**.

![Siden for oppsett av arbeidsordrer, legg til arbeidsordre.](media/18-setup-for-work-orders.png)

> [!NOTE]
> Hver gang det opprettes en arbeidsordrelinje, søker Aktivastyring etter en prosjektgruppe som skal knyttes til arbeidsordrejobbprosjektet. Søket er basert på oppsettet som er beskrevet i dette emnet. Hver prosjektgruppe har en tilknyttet prosjekttype. Prosjektgrupper som har prosjekttypen **Tid og materialer** eller **Fast pris**, er bare gyldige for anleggsmidler som er knyttet til en kundekonto.
>
> For overordnede prosjekter og prosjektgrupper, når systemet velger tilgjengelig arbeidsordreprosjekt eller prosjektgruppe, baseres valget på postene du opprettet ved hjelp av fremgangsmåten ovenfor. Aktivastyring går gjennom poster som er knyttet til arbeidsordreprosjektet for å søke etter mulig samsvar. Den kontrollerer alltid den mest spesifikke kombinasjonen først. Med andre ord, for det overordnede prosjektet for arbeidsordre ser Aktivastyring først etter et mulig treff i **Aktivum**-feltet. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Aktivumtype**-feltet. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Arbeidssted**-feltet, og så videre. Som du kan se i oppsettet av siden **Prosjektoppsett for arbeidsordre**, betyr dette at for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff. Hvis det ikke blir funnet samsvar, brukes standardposten der bare prosjekt-ID-en er valgt. Prosessen for å finne den tilknyttede prosjektgruppen er lik. Aktivastyring søker først etter et mulig treff i **Aktivum**-feltet, deretter **Aktivumtype**-feltet og deretter **Arbeidsordretype**-feltet. Hvis det ikke blir funnet samsvar, brukes standardposten der bare en prosjektgruppe er valgt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]