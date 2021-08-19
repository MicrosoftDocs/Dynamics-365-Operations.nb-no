---
title: Lageroppslag på salgsstedet
description: Dette emnet beskriver hvordan du bruker lageroppslagsoperasjonen på Dynamics 365 Commerce-salgsstedet til å vise tilgjengelighet av lagerbeholdning av produkter på tvers av butikker og lagre.
author: boycezhu
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: b697583f2ebf9950ad805d4f415dafb2c891de8052d4a47563b048059475030f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745338"
---
# <a name="inventory-lookup-operation-in-pos"></a>Lageroppslag på salgsstedet

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du bruker lageroppslagsoperasjonen på Dynamics 365 Commerce-salgsstedet til å vise tilgjengelighet av lagerbeholdning av produkter på tvers av butikker og lagre.

En nøyaktig visning av lageret i en organisasjon hjelper butikkansatte med å gi en rask og effektiv kundeservice. Øyeblikket som betyr mest, er når en kunde er klar til å ta en kjøpsbeslutning. Det er viktig at kasserere i en detaljhandel har nær sanntid- eller sanntidsinformasjon om lageret lett tilgjengelig, slik at de kan gi riktig informasjon om produktlevering og plukking.

Ved hjelp av lageroppslagsoperasjonen i Commerce POS kan forhandlerne oppnå god driftskvalitet og få innsikt ved å koble butikker til Commerce Headquarters. Denne funksjonaliteten gir en lagertilgjengelighetsvisning av produkter på tvers av butikker og lagre. Den hjelper også forhandlerne med å øke effektiviteten og kostnadsbesparelsene ved å forbedre lagerplanlegging i sanntid.

Når lageroppslagsoperasjonen startes fra POS-programmet, bruker POS-kassereren det numeriske tastaturet til å angi et produktnummer til spørringer i lagerinformasjonen. Hvis produktet som er angitt, har varianter, kan kassereren velge dimensjoner eller andre verdier for å kontrollere lagerinformasjon for en bestemt produktvariant.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Lageroppslagslistevisning for individuelle produkter

For et enkeltprodukt gir lageroppslagsoperasjonen en lageroppslagsliste som viser følgende produktinformasjon for en liste over lokasjoner:

- **Lager** - Refererer til det "fysisk tilgjengelige" antallet for et produkt.
- **Reservert** - Refererer til det "fysisk reserverte" antallet som hentes fra hovedkontoret.
- **Bestilt** - Refererer til det "bestilt i alt"-antallet som hentes fra hovedkontoret.
- **Enhet** – Refererer til lagermåleenheten som er konfigurert i hovedkontoret.

Listevisningen over lokasjoner omfatter alle butikker og lagre som er konfigurert i innfrielsesgruppene som den gjeldende butikken er koblet til, som vist i eksempelet nedenfor.

![Listevisning for lageroppslag.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Kontroller at gjeldende butikk er inkludert i de tilknyttede innfrielsesgruppene.

Følgende handlinger er tilgjengelige på applinjen for salgsstedet:

- **Sortering** – Denne handlingen gjørdet mulib for salgsstedsbrukeren å sortere dataene i listevisningen basert på ulike kriterier. Lokasjonsbasert sortering er standard sorteringsalternativ. 
  - **Geolokasjon** (fra lokasjonen som ligger nærmest, til lokasjonen som ligger lengst borte, sammenlignet med den gjeldende butikken)
  - **Navn** (i stigende eller synkende rekkefølge)
  - **Butikknummer** (i stigende eller synkende rekkefølge)
  - **Lager** (i synkende rekkefølge)
  - **Reservert** (i synkende rekkefølge)
  - **Bestilt** (i synkende rekkefølge)
- **Filter** – Ved hjelp av denne handlingen kan POS-brukeren vise filtrerte data for en bestemt plassering.
- **Vis butikktilgjengelighet** – Denne handlingen gjør det mulig for POS-brukeren å vise ATP-antallene (available-to-promise) for et produkt i den valgte butikken.
- **Vis butikklokasjon** – Denne handlingen åpner en egen side for å vise kartvisning, adresse og åpningstider for den valgte butikken.
- **Hent i butikk** - Denne handlingen oppertter en kundeordre for produktvarianten som plukkes fra den valgte butikken, og omdirigerer brukeren til skjermbildet for transaksjonen.
- **Send produkt** - Denne handlingen oppretter en kundeordre for produktet som skal sendes fra den valgte butikken, og omdirigerer brukeren til skjermbildet for transaksjonen.
- **Vis alle varianter** – For et produkt med varianter bytter denne handlingen fra en listevisning til en matrisevisning som viser lagerinformasjon for alle varianter av produktet.
- **Legg til transaksjon** – Denne handlingen legger til produktet i handlekurven og sender brukeren videre til transaksjonsskjermbildet.

> [!NOTE]
> Når det gjelder en lokasjonsbasert sortering, bestemmes avstanden mellom en lokasjon og den gjeldende butikken av koordinatene (bredde og lengde) som er definert i Commerce Headquarters. For en butikk er lokasjonsinformasjonen definert i primæradressen til driftsenheten som er tilknyttet butikken. For et lager som ikke er butikk, defineres lokasjonsinformasjonen i lageradressen. Hvis den gjeldende butikken ikke har definerte koordinater, vil det lokasjonsbaserte sorteringsalternativet vise den gjeldende butikken øverst i listen, og deretter sortere andre lokasjoner etter navn.

> [!NOTE]
> **Vis butikktilgjengelighet**, **Vis butikklokasjon**, **Hent i butikk** og **Send produkt** er ikke tilgjengelig for ikke-butikklokasjoner.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Matrisevisning av lageroppslag for varianter

For et hovedprodukt med varianter gir lageroppslagsoperasjonen også en dimensjonsbasert matrisevisning som viser informasjon om lagertilgjengelighet for alle varianter av hovedproduktet på en valgt lokasjon. Som standard viser matrisevisningen data for inneværende butikk. Du kan bruke **Butikk**-handlingen på applinjen til å slå opp lagerinformasjon i andre butikker som er konfigurert i innfrielsesgruppene som den gjeldende butikken er koblet til.

Følgende eksempelbilde viser matrisevisningen for lageroppslag på salgsstedet.

![Matrisevisning for lageroppslag.](media/inventory-lookup-matrix-view.png)

I matrisevisningen representerer hver celle en individuell variant, og viser en lagerbeholdningsverdi (fysisk tilgjengelig) nederst i høyre hjørne i tillegg til **reserverte** (fysisk reserverte) og **bestilte** verdier (bestilt i total) i øvre venstre hjørne. Tabellen nedenfor forklarer betydningen av ulike lagerbeholdningsverdier.

| Beholdningsverdi                            | beskrivelse |
|------------------------------------------|-------------|
| Numerisk verdi som er større enn 0 (null) | En variant er frigitt til den valgte plasseringen, og du kan utføre flere handlinger i cellen. |
| **0** (null)                             | En variant er frigitt til den valgte plasseringen, men varen er ikke tilgjengelig på den valgte plasseringen. Du kan utføre flere handlinger i cellen. |
| **i/t** eller en inaktiv celle              | En variant er ikke frigitt til den valgte plasseringen, og du kan ikke utføre flere handlinger i cellen. |

Visningsrekkefølgen for dimensjonsverdiene i matrisevisningen er basert på konfigurasjonen for dimensjonsvisningsordren i Commerce Headquarters. Du kan endre konfigurasjonen for dimensjonsvisningsordren ved å velge en ny dimensjon som skal brukes. 

Følgende handlinger er tilgjengelige i matrisevisningscellen:

- **Selg nå** – Denne handlingen legger til den valgte varianten i handlekurven og sender brukeren videre til transaksjonsskjermbildet.
- **Hent i butikk** - Denne handlingen oppertter en kundeordre for den valgte varianten som plukkes fra den valgte butikken, og omdirigerer brukeren til skjermbildet for transaksjonen.
- **Send produkt** - Denne handlingen oppretter en kundeordre for den valgte varianten som skal sendes fra den valgte butikken, og omdirigerer brukeren til skjermbildet for transaksjonen.
- **Tilgjengelighet** - Denne handlingen tar brukeren til en egen side som viser ATP-antallene for den valgte varianten i den valgte butikken.
- **Vis alle lokasjoner** - Denne handlingen bytter til standard lagertilgjengelighetslistevisning som viser lagerinformasjon for den valgte varianten.
- **Vis produktdetaljer** - Denne handlingen omdirigerer brukeren til produktdetaljersiden (PDP) for den valgte varianten.

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Få tilgang til lageroppslag fra andre sider på salgsstedet

Salgsstedsbrukere kan få tilgang til lageroppslagsoperasjonen fra andre sider på salgsstedet.

Følgende eksempelbilde viser matrisevisningresultatene fra en PDP på salgsstedet.

![Lageroppslag fra produktdetaljerside.](media/inventory-lookup-from-product-details-page.png)

På PDP-en til et hovedprodukt kan du bruke handlingen **Vis alle varianter** på applinjen for å starte matrisevisningen for lageroppslag som viser informasjon om lagertilgjengelighet for den gjeldende butikken for alle varianter av et produkt. For et enkelt produkt viser PDP-verdien lagerbeholdningen (fysisk tilgjengelig) for dette produktet for den gjeldende butikken. I tillegg kan du velge koblingen **Annet butikklager** for å starte lageroppslagsoperasjonen for å kontrollere lagertilgjengeligheten for et produkt på tvers av andre butikker eller lagre.

> [!NOTE]
> **Vis alle varianter**-handlingen på PDP er bare tilgjengelig for hovedprodukter som har varianter. Den er ikke tilgjengelig for spesifikke produkter eller pakker.

Du kan konfigurere lageroppslagsoperasjonen til å vises som en kobling i knappegruppen på salgsstedets transaksjonsskjermbilde. Når brukeren etter konfigurasjon velger en handlekurvlinje og deretter velger **Lageroppslag**-knappen, vises lageroppslagslistevisningen for det valgte produktet. Hvis du vil ha mer informasjon om hvordan du konfigurerer knappegruppene ved hjelp av verktøyet for utforming av POS-skjermoppsett, kan du [Visuelle konfigurasjoner av brukergrensesnittet for salgssted](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Lageroppslag med beregning på kanalsiden

I Commerce versjon 10.0.9 og tidligere hentes **tilgjengelig fysisk** verdi i lageroppslagsoperasjonen fra Commerce Headquarters via en servicekall i sanntid. I Commerce versjon 10.0.10 og senere kan du konfigurere salgsstedslageroppslagsoperasjonen til å bruke kanalsideberegning på Commerce-serveren for å fastslå den tilgjengelige fysiske verdien, som kan gi et mer pålitelig og mer nøyaktig estimat over lagerbeholdningen ved å beregne transaksjonsdataene som ennå ikke er synkronisert mot hovedkontoret. Hvis du vil ha mer informasjon om lagerberegning på kanalsiden og relatert salgsstedskonfigurasjon i hovedkontoret, kan du se [Beregne lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Visuelle konfigurasjoner av brukergrensesnittet for salgssted](pos-screen-layouts.md)

[Beregne lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
