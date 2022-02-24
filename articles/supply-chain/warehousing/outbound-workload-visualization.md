---
title: Visualisering av utgående arbeidsmengde
description: Dette emnet inneholder informasjon om visualisering av utgående arbeidsmengde. Denne funksjonaliteten gjør at lagerledere og ledere kan opprette egendefinerte arbeidsmengdediagrammer som kan brukes til å overvåke fremdriften av gjeldende arbeid og hvor mye som gjenstår. Lagerledere kan opprette flere visninger og konfigurere automatisk oppdatering etter behov.
author: Mirzaab
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2515a71297df7213f93a4c619f7eebf1c2411b39
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965558"
---
# <a name="outbound-workload-visualization"></a>Visualisering av utgående arbeidsmengde

[!include [banner](../includes/banner.md)]

Med avanserte installasjonsfunksjoner som er tilgjengelige fra funksjonen **Visualisering av utgående arbeidsmengde**, kan lagerledere og ledere opprette egendefinerte arbeidsmengdediagrammer som kan brukes til å overvåke fremdriften til gjeldende arbeid og hvor mye som gjenstår. Lagerledere kan opprette flere visninger og konfigurere automatisk oppdatering etter behov. Visualiseringer av utgående arbeidsmengde er passende for visning på lagerytelsessider.

Denne funksjonaliteten kan brukes til å spore fremdriften ved plukkarbeid. Funksjonen er integrert med arbeidsstyring, og hvis arbeidsadministrasjon er definert, kan visualiseringer av utgående arbeidsmengde vise en beregning av antall timer som gjenstår for plukkarbeidet som vises (filtrert).

## <a name="turn-on-the-outbound-workload-visualization-feature"></a>Aktivere funksjonen Visualisering av utgående arbeidsmengde

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Visualisering av utgående arbeidsmengde*

## <a name="set-up-outbound-workload-visualizations"></a>Konfigurer visualiseringer av utgående arbeidsmengde

Når du skal konfigurere visualiseringer, oppretter du en samling filtre (visninger) og utformer hvert filter slik at det viser en annen type analyse. Du bruker **Konfigurer filtre**-siden til å utforme filtrene.

Følg denne fremgangsmåten for å konfigurere visualisering av utgående arbeidsmengde:

1. Gå til **Lagerstyring \> Lagerovervåkingsrapporter \> Visualisering av utgående arbeidsmengde**.

    Siden **Visualisering av utgående arbeidsmengde** vises. Når du har opprettet noen filtre, vil denne siden vise visualiseringen. Du kan opprette så mange filtre som du vil. Alle filtrene du oppretter, lagres under brukerkontoen slik at du kan bruke dem senere. Med andre ord får hver bruker sitt eget sett med filtre de har opprettet. Disse filtrene deles ikke med andre brukere.

1. På siden **visualisering av utgående arbeidsmengde** velger du **Konfigurer filtre** i fanen **Filtre** i handlingsruten.
1. Velg **Ny** for å legge til et filter i handlingsruten på **Konfigurer filtre**-siden , og angi deretter følgende felter for den:

    - **X-aksegruppetabell** – Velg tabellen som inneholder feltet som skal brukes til å gruppere X-akseverdiene.
    - **X-aksegruppefelt** – Blant feltene i tabeller som du valgte i feltet **X-aksegruppetabell**, velger du feltet som skal brukes til å gruppere X-akseverdiene.
    - **X-akseverditabell** – Velg tabellen som inneholder feltet som skal brukes til ytterligere å analysere gruppene.
    - **X-akseverdifelt** – Blant feltene i tabeller som du valgte i feltet **X-akseverditabell**, velger du feltet som skal gi verdiene som skal analyseres for hver gruppe.
    - **Automatisk oppdatering** – Velg om visualiseringen skal oppdateres automatisk.
    - **Oppdateringsintervall (minutter)** – Angi antall minutter mellom automatiske oppdateringer.
    - **Visningsnivå** – Velg om diagrammet skal vise åpne linjer eller åpne antall overskrifter.
    - **Plukktype** – Hvis du angir feltet **Visningsnivå** til _Åpne linjer_, må du velge om antallet åpne arbeidslinjer i diagrammet skal omfatte innledende plukking, oppsamlede plukkinger eller både innledende og oppsamlede plukkinger.
    - **Område** – Velg området du vil laste diagrammet for.
    - **Lager** – Velg lageret du vil laste diagrammet for.
    - **Dager som skal tas med** – Angi hvor mange dager det skal gå før diagrammet skal genereres.
    - **Arbeidsordretype** – Velg de utgående arbeidsordretypene du vil filtrere på.

    ![Konfigurer filtrer-side](media/work-viz-filters-1.png "Konfigurer filtrer-side")

1. Lukk **Konfigurer filtre**-siden for å gå tilbake til siden **Visualiseringer av utgående arbeidsmengde**.

    Siden **Visualiseringer av utgående arbeidsmengde** viser nå data basert på de nye filterinnstillingene. Det nye filteret er nå tilgjengelig og valgt i **Filter**-feltet. Følgende felter er tilgjengelige øverst i diagrammet:

    - **Filter** – Dette feltet inneholder alle filtrene du har opprettet så langt. Velg et filter for å vise dataene i diagrammet.
    - **Sist oppdatert** – Dette feltet viser datoen og klokkeslettet da informasjonen i diagrammet sist ble oppdatert.
    - **Estimert/faktisk tid** – Hvis arbeidsstandarder er konfigurert i systemet, setter du dette alternativet til *Ja* for å vise akkumulerte, estimerte plukktider øverst i hver kolonne i diagrammet. Hvis du ikke bruker arbeidsstandarder, er ikke dette alternativet tilgjengelig.

    ![Eksempelvisualisering](media/work-viz-chart.png "Eksempelvisualisering")

1. Velg en stolpe i diagrammet for å vise informasjonen i den tilknyttede arbeidslinjen.

    ![Detaljer for arbeidslinje](media/work-viz-work-details.png "Detaljer for arbeidslinje")

## <a name="example-outbound-workload-visualization-for-zones"></a>Eksempel: Visualisering av utgående arbeidsmengde for soner

I dette eksemplet vil du konfigurere en visualisering som viser arbeidslinjer for hver sone, og statusen for hver arbeidslinje (_Åpen_, _Lukket_ eller _Avbrutt_). I dette tilfellet kan du konfigurere et filter som har følgende innstillinger:

- **Filternavn** – Angi et navn på dette filteret (for eksempel _Sone kontra arbeidsstatus_).
- **Beskrivelse** – Angi en kort beskrivelse for dette filteret (for eksempel _Sone kontra arbeidsstatus_).
- **X-aksegruppetabell** – Velg _Lokasjoner._
- **X-aksegruppe** – Velg _Sone-ID_.
- **X-akseverditabell** – Velg _Arbeid_, fordi du vil vise arbeid per sone.
- **X-akseverdifelt** – Velg _Arbeidsstaus_, fordi du vil vise arbeidsstatus.
- **Automatisk oppdatering** – Velg om visualiseringen skal oppdateres automatisk.
- **Plukktype** – Velg _Innledende plukkinger og oppsamlede plukkinger_, fordi du vil ta med både innledende plukkinger og plukkinger fra oppsamlingslokasjoner. Med andre ord vil du stort sett ta med alle plukkarbeidslinjene du har.
- **Visningsnivå** – Velg _Åpne linjer_ fordi du vil vise informasjonen per linje, ikke per arbeidshode.

Illustrasjonen nedenfor viser et eksempel på resulterende diagram.

![Visualisering av sone kontra arbeidsstatus](media/work-viz-chart.png "Visualisering av sone kontra arbeidsstatus")

Dette diagrammet viser to soner som heter **GULV** og **PARTI**, pluss en sone som har navnet **Tom**. Den **tomme** sonen representerer alle arbeidslinjer som ikke er medlemmer av noen soner. Diagrammet viser alltid alle ikke-relaterte filtrerte data som **tomme**, for å gi så mye synlighet som mulig. I **GULV**-sonen viser diagrammet tre lukkede linjer og fire åpne linjer. I **PARTI**-sonen viser diagrammet fire lukkede linjer, én åpen linje og 24 avbrutte linjer. Til slutt viser diagrammet åtte lukkede linjer som ikke er en del av en sone, og er derfor oppført som **tomme**.
