---
title: Bølgemaler
description: Dette emnet beskriver hvordan du definerer vilkår som bestemmer om bølger behandles manuelt eller automatisk, og hvor mye arbeid som genereres for et lager når en bølge behandles.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 61fbcad572bbb69ab8a4eb2cd309cdf8a6328391
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686604"
---
# <a name="wave-templates"></a>Bølgemaler

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du definerer vilkår som bestemmer om bølger behandles manuelt eller automatisk, og hvor mye arbeid som genereres for et lager når en bølge behandles. Du angir vilkårene ved å definere bølgemaler og spørringer som samsvarer med en bølge med frigitte linjer i bestillinger, produksjonsordrer og Kanbaner.

## <a name="settings-for-wave-templates"></a>Innstillinger for bølgemaler

Når du definerer en bølgemal, angir du følgende:

- **Området** og **lageret** som malen skal opprette arbeid for.
- Rekkefølgen som malene skal evalueres i. Sekvensen der malene samsvares med frigitte linjer på salgsordrer, produksjonsordrer og Kanbaner. Når en linje frigis, bruker systemet den første bølgemalen som linjen oppfyller kriteriene for. Jo bredere kriteriene er, jo mer sannsynlig er det at en linje oppfyller kriteriene, så du bør plassere malene med de mest spesifikke kriteriene øverst på listen. Bruk knappene **Flytt opp** og **Flytt ned** i handlingsruten til å ordne malene i listen.
- Handlingene som utføres av hver mal. **Bølgemetodene** som utfører handlingene som opprettes av malen, for eksempel oppretting eller fordeling av arbeid for hver type bølgemal.
- Bølgeattributtene (filtre) som må gjelde for at bølgemalen skal brukes.

> [!NOTE]
> Om nødvendig kan en utvikler opprette flere metoder. Du kan vise den fullstendige listen over metoder på siden **Bølgebehandlingsmetoder**.

Noen innstillinger representerer strategiske beslutninger for bølgebehandling, på følgende måte:

- Hvis malen brukes til å sende varer for salgsordrer og overføringsordrer eller til å flytte varer til produksjon for produksjonsordrer eller Kanbaner.
- Hvis en bølge behandles manuelt eller automatisk på følgende måte:

  - **Manuell behandling** – linjen legges til en bølge, og lageret reserveres. Du må imidlertid velge **Prosess** på **Alle bølger**-siden for å opprette plukkarbeidet for ordren.
  - **Automatisk behandling** – Du kan automatisere bølgebehandling fullstendig eller delvis. Hvis du automatiserer bølgebehandling fullstendig, opprettes en bølge som omfatter linjen fra salgsordren, produksjonsordren eller Kanbanen når en salgsordre, produksjonsordre eller Kanban opprettes. Varene trekkes fra lagerbeholdningen, og plukkarbeidet opprettes. Hvis du automatiserer bølgebehandling delvis, kan du angi verdier som utløser bølgebehandling. Du kan for eksempel angi en maksimal vekt for forsendelser, som utløser bølgebehandling når totalvekten for linjene i bølgen når verdien.

- Hvis du tilordner forsendelser til en åpen bølgen. Hvis du for eksempel lover kunder at en ordre som er lagt inn før 12:00, skal sendes innen 24 timer, kan du definere bølgemalen til automatisk å knytte ordrelinjer til en åpen bølgen frem til klokken 12:00. På dette tidspunktet behandles bølgen automatisk.

Når en bølge behandles, vil plukkarbeidet som opprettes bli basert på arbeidsmalen og lokasjonsdirektivet som er angitt for lageret. Arbeidsmalen angir hvordan plukkarbeidet opprettes, og lokasjonsdirektivet angir lokasjoner for plukking- og plassering.

## <a name="create-a-wave-template"></a>Opprette en bølgemal

Hvis du vil konfigurere en bølgemal, gjør du følgende:

1. Gå til **Lagerstyring** \> **Oppsett** \> **Bølger** \> **Bølgemaler**.
1. Velg **Ny** for å opprette en ny bølgemal.
1. I **Bølgemaltype**-feltet velger du ett av følgende alternativer:

    - *Forsendelse* – Bruk bølgemalen for forsendelse av varer for salgsordrer og overføringsordrer.
    - *Produksjonsordrer* – Bruk bølgemalen for å flytte varer for produksjonsordrer.
    - *Kanban* – Bruk bølgemalen for å flytte varer for Kanban-ordrer.

1. I feltene **Navn på bølgemal** og **Beskrivelse av bølgemal** angir du et navn på og en beskrivelse av bølgemalen.

    > [!NOTE]
    > Hvis flere maler opprettes for et lager, angir tallet i feltet **Bølgemalsekvens** posisjonen til malen i sekvensen der malene brukes, når malens kriterier er oppfylt. Du kan velge **Flytt opp** eller **Flytt ned** for å endre rekkefølgen på malene.

1. I feltene **Område** og **Lager** velger du området og lageret som bølgemalen skal opprette bølger og plukkarbeid for.
1. Hvis du vil automatisere bølgebehandlingen, må du gjøre følgende innstillinger etter behov:

    - **Automatisk oppretting av bølge** – Sett dette til *Ja* for å opprette en bølge automatisk når en salgsordre, produksjonsordre eller kanban frigis til lageret.
    - **Tilordne til åpne bølger** – Sett dette til *Ja* hvis du automatisk vil tilordne linjer til en åpen bølge når linjene frigis. Linjer tilordnes bølger basert på spørringsfilteret for bølgemalen.
    - **Behandle bølge ved frigivelse til lager** – Sett dette til *Ja* for automatisk behandling av bølgen, og opprett arbeid når en linje frigis til lageret.
    - **Behandle bølge automatisk ved terskel** – Sett dette til *Ja* for å behandle bølgen automatisk når verdiene når tersklene for vekt, forsendelse og linjer som er angitt i **Bølgeterskler**-feltgruppen. Denne innstillingen er bare aktiv hvis *Forsendelse* er valgt i **Bølgemaltype**-feltet.
    - **Frigi bølge automatisk** – Sett dette til *Ja* for å frigjøre bølgen automatisk. Plukkarbeidet opprettes og gjøres tilgjengelig på mobilenheter.
    - **Automatiser frigivelse av etterfyllingsarbeid** – Sett dette til *Ja* for å opprette behovsbasert etterfyllingarbeid og frigi det automatisk. Du må legge til etterfyllingsbølgemetoden i bølgemalen og opprette en mal for etterfylling ved å bruke typen *Bølgebehov*. Angi en mal for etterfylling på siden **Etterfyllingsmaler**. Dette krever at du legger til etterfyll-metoden i bølgemalen.
    - **Fortsett bølgebehandling når oppretting av arbeid mislykkes** – Når dette er satt til *Ja*, bruker systemet en tom lokasjon hvis det ikke kan reservere beholdningen på lokasjonen som foreslås av lokasjonsdirektivet (for eksempel fordi beholdningen ikke lenger er tilgjengelig). Når det er satt til *Nei*, vil bølgen mislykkes hvis systemet ikke kan reservere beholdningen.

1. Angi feltgruppen **Bølgeterskler** etter behov:
    - **Terskel for bølgevekt** – Angi maksimal vekt en bølge kan inneholde.
    - **Forsendelsesterskel** – Angi maksimalt antall forsendelser som kan inkluderes i en bølge.
    - **Linjeterskel** – Angi maksimalt antall linjer som kan inkluderes i en bølge.

1. I feltgruppen **Standardverdier** velger du bølgeattributtene du vil bruke som ytterligere spørringskriterier for bølgemalen. Bølgeattributter er nyttige for å tilordne flere kriterier, for eksempel navnet på en bestemt kunde, for en bølgemal. Du oppretter disse attributtene på siden **Bølgeattributter**. 

1. Angi **Bølgevarslingspolicy** for policyen du vil bruke til å generere varslinger relatert til bølger som bruker denne malen. Hvis du vil ha et eksempel på en bølgevarslingspolicy, kan du se [Varslinger for bølgekjøring](wave-execution-notifications.md).

1. På hurtigfanen **Metoder** viser ruten **Valgte metoder** metodene for den valgte bølgemalen. Bølgemetodene som utfører handlingene som opprettes av malen, for eksempel oppretting eller fordeling av arbeid. Disse handlingene kalles også bølgetrinn. Bølgemetoder er forhåndsdefinert for hver type bølgemal. Du kan ikke fjerne de forhåndsdefinerte bølgemetodene, men du kan endre rekkefølgen på metoder og legge flere metoder. Hvis du for eksempel oppretter en bølgemal for levering, kan du for eksempel legge til metoder for etterfylling, og containerbruk. Bølgecontainerbruk kan legges til en rekke bølgemetoder for å definere containerbruk for linjene som behandles i en bølgemal. Hvis du vil legge til en metode til, gjør du følgende:

    - Velg en metode i ruten **Gjenværende metoder**, og velg deretter pilen til **venstre** for å legge den til i ruten **Valgte metoder**.
    - Hvis du vil endre rekkefølgen, velger du en metode og velger deretter pil **opp** eller **ned**.

    > [!NOTE]
    > Når du legger til en metode, vises den automatisk på riktig sted i trinnrekkefølgen.

1. Hvis du vil angi spørringen som skal samsvare med frigitte linjer til en passende bølge, velger du **Rediger spørring** i handlingsruten.
1. Hvis du vil kontrollere at innstillingene for malbølgen er gyldige, velger du **Valider mal**.
