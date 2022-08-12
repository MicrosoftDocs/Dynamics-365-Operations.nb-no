---
title: Rett opp feil med at planleggingsmotoren ikke finner nok kapasitet og begrenset kapasitet
description: Denne artikkelen gir informasjon om årsakene og løsningene for "Produksjonsordre %1 kan ikke planlegges. Feilmeldingen om at planleggingsmotoren ikke finner nok kapasitet.
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135607"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Rett opp feil med at planleggingsmotoren ikke finner nok kapasitet

[!include [banner](../includes/banner.md)]

Når du kjører planlegging, kan du få følgende feilmelding:

> Kan ikke planlegge produksjonsordren %1. Fant ikke nok kapasitet.

Det er flere årsaker til hvorfor planleggingsmotoren kan mislykkes og utstede denne feilmeldingen. Denne artikkelen gir retningslinjer som vil hjelpe deg med å finne roten til feilen og deretter redusere den.

## <a name="review-the-applicable-resources"></a>Se gjennom de aktuelle ressursene

Feilen kan oppstå hvis ingen gjeldende ressurser oppfyller operasjonskravene på produksjonsordreområdet.

Følg denne fremgangsmåten for å se gjennom gjeldende ressurser.

1. Gå til **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer**, og åpne eller velg produksjonsordren som ikke kan planlegges.
1. I handlingsruten, i fanen **Produksjonsordre**, i **Produksjonsdetaljer**-gruppen, velger du **Rute**.
1. Velg operasjonen på **Produksjonsrute**-siden, og velg deretter **Gjeldende ressurser** i handlingsruten.
1. I dialogboksen **Gjeldende ressurser** setter du feltet **Bruk krav for** til *Grovplanlegging* eller *Finplanlegging*, avhengig av hvilken type planlegging du bruker.
1. Kontroller at det finnes ressurser i produksjonsordreområdet.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Se gjennom kalenderne som er knyttet til ressurser

Feilen kan oppstå hvis ingen kalender er knyttet til ressursen eller ressursgruppen, eller hvis den tilknyttede kalenderen ikke er riktig definert (den har for eksempel ingen arbeidstider, eller effektiviteten som en prosent er 0 \[null\]).

Følg denne fremgangsmåten for å bekrefte at en kalender er knyttet til ressursen eller ressursgruppen.

1. Gå til **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer**, og åpne eller velg produksjonsordren som ikke kan planlegges.
1. I handlingsruten, i fanen **Produksjonsordre**, i **Produksjonsdetaljer**-gruppen, velger du **Rute**.
1. Velg operasjonen på **Produksjonsrute**-siden, og velg deretter **Gjeldende ressurser** i handlingsruten.
1. Velg ressursen i dialogboksen **Gjeldende ressurser**, og velg deretter **Vis ressurs**. Du kan også velge og holde (eller høyreklikke) i feltet **Ressursgruppe** og deretter velge **Vis detaljer**.
1. På siden **Ressurser** eller **Ressursgrupper** i hurtigfanen **Kalendere** kontrollerer du at kalenderen er knyttet til ressursen eller ressursgruppen.

> [!NOTE]
> Hvis feilen oppstår under grovplanlegging, må du kontrollere at en kalender er knyttet til alle gjeldende ressursgrupper.

Følg denne fremgangsmåten for å gå gjennom oppsettet av kalenderen.

1. Gå til **Organisasjonsstyring \> Oppsett \> Kalendere \> Kalendere**, og velg kalenderen som er knyttet til ressursen eller ressursgruppen.
1. Velg **Driftstider** i handlingsruten.
1. På **Driftstider**-siden må du kontrollere at siden ikke er tom. I tillegg må du for dagene du er interessert i, kontrollere at **Kontroll**-feltet ikke er satt til *Lukket*, driftstider finnes, og at feltet **Effektivitet er prosent** ikke er satt til *0* (null).

Hvis kalenderen er knyttet til basiskalenderen, må du også se gjennom oppsettet for basiskalenderen.

> [!NOTE]
> I grovplanlegging brukes ressursgruppens kalender til å fastslå start- og sluttidspunktene og datoene for hver operasjon. Det begrenser også tiden systemet kan planlegge for en bestemt operasjon for en bestemt dag i en bestemt ressursgruppe. Hvis for eksempel arbeidstidene for en ressursgruppe på en bestemt dag er fra 8:00 til 16:00, vil belastningen som en operasjon setter på ressursgruppen, ikke overskride belastningen som kan passe på åtte timer, uansett hvor mye tilgjengelig kapasitet ressursgruppen har på den dagen. Tilgjengelig kapasitet kan imidlertid begrense belastningen ytterligere.

## <a name="review-the-scheduling-parameters"></a>Gå gjennom planleggingsparametere

For å sikre god ytelse vil planleggingsmotoren bare søke etter en ressurs i en bestemt tid og et bestemt antall planleggingskonflikter.

Følg denne fremgangsmåten for å gå gjennom planleggingsparameterne.

1. Gå til **Organisasjonsstyring \> Oppsett \> Planleggingsparametere**.
1. Følg ett av disse trinnene:

    - Hvis alternativet **Tidsavbrudd for planlegging er aktivert** er satt til *Nei*, kan du gå videre til trinn 3.
    - Hvis alternativet **Tidsavbrudd for planlegging er aktivert** er satt til *Ja*, øker du volumet for feltet **Maksimal planleggingstid per serie** for å gi behandlingen mer tid til å fullføres.

1. Følg ett av disse trinnene:

    - Hvis alternativet **Tidsavbrudd for planleggingsoptimalisering er aktivert** er satt til *Nei*, kan du gå videre til trinn 4.
    - Hvis alternativet **Tidsavbrudd for planleggingsoptimalisering** er satt til *Ja*, øker du volumet for feltet **Tidsavbrudd for optimaliseringsforsøk** for å gi behandlingen mer tid til å fullføres.

1. Hvis du endret noen av innstillingene på siden, kan du planlegge ordren på nytt for å prøve på nytt.

## <a name="review-capacity"></a>Gå gjennom kapasitet

Feilen kan oppstå når du utfører begrenset planlegging, men det ikke er ledig kapasitet.

Følg denne fremgangsmåten for å utføre ubegrenset kapasitetsplanlegging.

1. Gå til **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer**, og åpne eller velg produksjonsordren som ikke kan planlegges.
1. I handlingsruten i **Tidsplan**-fanen i **Produksjonsordre**-gruppen velger du **Planlegg operasjoner** eller **Planlegg jobber**.
1. I dialogboksen **Grovplanlegging** eller **Finplanlegging** setter du alternativet **Begrenset kapasitet** til *Nei*.
1. Velg **OK** for å planlegge ordren.

Følg denne fremgangsmåten for å se gjennom tilgjengelig kapasitet på ressursen.

1. Gå til **Organisasjonsstyring \> Ressurser \> Ressurser**, og velg en ressurs som er gjeldende for ordren som ikke kan planlegges.
1. I handlingsruten i **Ressurs**-fanen i **Vis**-gruppen velger du **Kapasitetsbelastning** eller **Kapasitetsbelastning, grafisk**, og kontrollerer at det finnes tilgjengelig kapasitet.

Følg denne fremgangsmåten for å se gjennom tilgjengelig kapasitet på ressursgruppen.

1. Gå til **Organisasjonsstyring \> Ressurser \> Ressursgrupper**, og velg en ressursgruppe som er gjeldende for ordren som ikke kan planlegges.
1. I handlingsruten i **Ressursgruppe**-fanen i **Vis**-gruppen velger du **Kapasitetsbelastning** eller **Kapasitetsbelastning, grafisk**, og kontrollerer at det finnes tilgjengelig kapasitet.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Hovedplanlegging bestiller en ressurs når ressurskalenderen er lukket

Ved bruk av driftsplanlegging vil hovedplanleggingen planlegge kapasitet i henhold til kalenderen for den primære ressursgruppen. Det bestiller den sekundære operasjonen samtidig som den primære operasjonen, og tar ikke hensyn til kalenderne eller kapasiteten til den sekundære operasjonen. Dette kan føre til at produksjonsordren planlegges i en lukket kalender eller på et tidspunkt da den sekundære operasjonen ikke er tilgjengelig (kalender lukket, ingen kapasitet).

Når jobbplanlegging brukes, vil hovedplanleggingen ta hensyn til kapasiteten og kalenderen for både den primære og den sekundære operasjonen ved planlegging av ordren. For at ordren skal kunne planlegges, må kalendere for ressursene i begge operasjonene være åpne og ha tilgjengelig kapasitet.

## <a name="maximum-job-lead-time-is-too-short"></a>Den maksimale jobbleveringstiden er for kort

Planleggingsmotoren kan ikke planlegge en ordre hvis **Maksimal jobbleveringstid** som er angitt for nettstedet ditt, er mindre enn leveringstiden som er angitt for en vare i standardordreinnstillingene eller dekningsinnstillingene.

Hvis du vil vise eller redigere innstillingen **Maksimal jobbleveringstid** for nettstedet ditt, går du til **Produksjonskontroll \> Oppsett \> Parametere for produksjonskontroll** og åpner **Generelt**-fanen.

Følg denne fremgangsmåten for å vise eller redigere standard ordreinnstillinger for en vare:

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Finn og velg det relevante produktet i listen.
1. Åpne fanen **Administrer lager** i handlingsruten, og velg **Standard ordreinnstillinger**.
1. Utvid hurtigfanen **Lager**, og vis eller rediger innstillingen **Leveringstid for lager** etter behov.

Følg denne fremgangsmåten for å vise eller redigere dekningsinnstillingene for en vare:

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Finn og velg det relevante produktet i listen.
1. Åpne Kategorien **Plan** i handlingsruten, og velg **Varedekning**.
1. Åpne **Leveringstid**-fanen, og vis eller rediger verdien for **Produksjonstid** etter behov.

## <a name="excessive-quantity-of-required-resources"></a>For store mengder ressurser som kreves

Under planlegging prøver motoren å samsvare det nødvendige ressursantallet som er angitt for en ruteoperasjon, med de aktuelle ressursene i henhold til operasjonsressurskravene. Hvis ressursantallet er for høyt, kan det føre til at en rute blir umulig, noe som vil føre til en planleggingsfeil.

Bruk følgende fremgangsmåte til å kontrollere både det angitte antallet og gjeldende ressurser for et valgt produkt, en rute og en ruteoperasjon:

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Finn og velg det relevante produktet i rutenettet.
1. Åpne **Utvikle**-fanen, og velg **Rute**.
1. Finn og velg den relevante ruten i rutenettet.
1. Åpne **Oversikt**-fanen nederst på siden.
1. Velg en operasjon fra listen over de valgte ruteoperasjonene.
1. Velg **Gjeldende ressurser** for å åpne en dialogboks der du kan vise de aktuelle ressursene for den valgte ruteoperasjonen.
1. Åpne **Ressursbelastning**-fanen. **Antall**-feltet her viser ressursantallet som kreves for den valgte ruteoperasjonen. Vis og/eller rediger det etter behov.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
