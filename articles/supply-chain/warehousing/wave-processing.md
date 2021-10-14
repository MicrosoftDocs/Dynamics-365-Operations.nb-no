---
title: Bølgeoppretting og -behandling
description: Dette emnet beskriver hvordan du oppretter, behandler og frigir en bølge for å opprette plukkarbeid for en last, forsendelse, produksjonsordre eller Kanban-ordre.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4b7c01a21dcbe7543332439ee6fd371b426851f4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579934"
---
# <a name="wave-creation-and-processing"></a>Bølgeoppretting og -behandling

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter, behandler og frigir en bølge for å opprette plukkarbeid for en last, forsendelse, produksjonsordre eller Kanban-ordre. Du kan opprette bølger for følgende typer ordrer:

- **Salgsordrer** – Bruk forsendelsesbølger til å ta med linjer fra salgsordrer. Når en salgsordre frigis til lageret, kan ordrelinjene tas med i bølgen.
- **Produksjonsordrer** – Bruk produksjonsbølger for å inkludere linjer fra stykklister for et produkt.
- **Kanban-ordrer** – Kanban-bølger inkluderer plukklistelinjer fra Kanban-ordrer.

Når det gjelder salgsordrer og Kanban-bestillinger, må beholdning reserveres før ordren frigis til lageret. Hvis ikke, varer eller tildelingslinjer kan ikke behandles i en bølge. Produksjonsordrer er imidlertid litt mer fleksible. For produksjonsordrer kan du velge ett av følgende alternativer:

- Krev at alle materialer reserveres før en ordre kan frigis til lageret.
- Tillat at produksjonsordrer frigis til lageret, selv om ikke alle materialer kan reserveres. Hvis du velger dette alternativet, må du gjenta prosessen med frigivelse til lager manuelt når tilleggsmaterialene flere blir tilgjengelige. Dette er for eksempel nyttig hvis du har materialene du trenger for å starte en produksjon, og du kan vente til tilleggsmaterialene bli tilgjengelige.

Du kan angi hvilke av disse produksjonsordrealternativene som skal brukes som standard ved hjelp av feltet **Krav for reservasjon av materialer** på siden **Parametere for produksjonskontroll**. Du kan imidlertid endre innstillingen for hver spesifikke produksjonsordre etter behov. Hvis du vil ha mer informasjon, kan du se [Lagerparametere for bølgebehandling](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Opprette og behandle en bølge

Diagrammet nedenfor viser flyten for hvordan forsendelsesbølger opprettes, behandles og frigis. Numrene tilsvarer avsnittene senere i denne seksjonen.

![Prosess for å opprette en bølge.](media/wave-processing-diagram.png "Prosess for å opprette en bølge")

### <a name="prerequisites"></a>Forutsetninger

Før du begynner, må en bølgemal være tilgjengelig for bølgetypen du vil opprette (forsendelse, produksjon eller Kanban). Bølgemalen fastsetter mange innstillinger for hvordan bølgen skal genereres og behandles, inkludert hvilke trinn som må gjøres manuelt og hvilke som gjøres automatisk. Hvis du vil ha mer informasjon, kan du se [Bølgemaler](wave-templates.md).

### <a name="create-a-wave"></a>Opprett en bølge

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Automatisk opprette bølger basert på lager og ordretype

Hvis du vil opprette bølger automatisk, konfigurerer du [Bølgemaler](wave-templates.md) som gjelder for hver relevante ordretype og lager. Kontroller at hver mal har alternativet **Automatisk oppretting av bølge** satt til *Ja*.

#### <a name="manually-create-waves"></a>Opprett bølger manuelt

Hvis du vil opprette en bølge manuelt, gjør du følgende:

1. Kontroller at de relevante [bølgemalene](wave-templates.md) ikke er angitt til å automatisk oppprette en bølge for lageret og ordretypene, der du heller vil gjøre dette manuelt.
1. Avhengig av hvilken type bølge du vil opprette, gjør du ett av følgende:

    - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**. Velg **Bølge** i handlingsruten.
    - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Produksjonsbølger** \> **Alle produksjonsbølger**. Velg **Produksjonsbølge** i handlingsruten.
    - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Kanban-bølger** \> **Alle Kanban-bølger**. Velg **Opprett bølge** i handlingsruten.

1. Skriv inn en kort beskrivelse av bølgen i **Beskrivelse**-feltet. Dette bør vise hva du behandler i bølgen.

1. I feltet **Navn på bølgemal** velger du bølgemalen for bølgetypen du vil opprette. Bølgemalen inneholder bølgemetodene som utfører handlinger, for eksempel oppretting av arbeid for bølgen. Bølgenmalen for forsendelsesbølger kan for eksempel inneholde metoder for å opprette laster, tildele linjer til bølger, etterfylle, og opprette plukkarbeid for bølgen.

1. Hvis du vil bruke bølgeattributter som ytterligere spørringskriterier for bølgen, velger du attributtene i **Bølgeattributter**-feltene.

### <a name="specify-what-to-include-in-a-wave"></a>Angi hva som skal være med i en bølge

Etter at en bølge er opprettet, er du klar til å begynne å legge til innhold i den.

> [!NOTE]
> Om nødvendig kan du legge til linjer i en bølge selv etter at den er behandlet så lenge den ikke er frigitt.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Angi automatisk hva som skal være med i en bølge

Hvis du vil opprette bølger automatisk, konfigurerer du [Bølgemaler](wave-templates.md) som gjelder for hver relevante ordretype og lager. Kontroller at hver mal har alternativet **Automatisk oppretting av bølge** satt til *Ja*. Malen kan eventuelt automatisk tilordne linjer til en hvilken som helst kvalifiserende åpen bølge hvis alternativet **Tilordne til åpne bølger** er satt til *Ja*.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Angi manuelt hva som skal være med i en bølge

Når en bølge er opprettet, men ennå ikke frigitt, kan du manuelt angi hva som skal inkluderes i den. Slik legger du til linjer i en bølge manuelt:

1. Avhengig av hvilken type bølge du vil legge til linjer for, gjør du ett av følgende:

    - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**. Velg **Bølge** i handlingsruten.
    - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Produksjonsbølger** \> **Alle produksjonsbølger**. Velg **Produksjonsbølge** i handlingsruten.
    - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Kanban-bølger** \> **Alle Kanban-bølger**. Velg **Opprett bølge** i handlingsruten.

1. Velg bølgen. Velg ett av følgende i handlingsruten:

      - **Oppretthold forsendelser**
      - **Vedlikehold produksjoner**
      - **Vedlikehold plukklister for Kanban-jobb**

1. I den øvre delen av vinduet velger du linjen som skal legges til bølgen, og deretter klikker du på **Legg til for bølge**. Linjen flyttes til hurtigfanen **Bølgelinjer**.

    Gjenta dette trinnet for hver linje du vil legge til. Hvis du vil legge til alle linjer, velger du **Legg til alle**.

    > [!TIP]
    > Når det gjelder forsendelsesbølger, kan du raskt finne en bestemt ordre ved å velge et egendefinert filter i feltet **Bølgefilterkode**. Bølgefilterkoder inneholder spørrekriterier for forsendelser som er opprettet i skjemaet **Bølgefiltre**. Dette feltet er ikke tilgjengelig for produksjonsbølger eller Kanban-bølger.
    > En grønn hake i **I bølge**-kolonnen viser at forsendelsen er lagt til i bølgen.

### <a name="process-the-wave-to-create-the-picking-work"></a>Behandle bølgen for å opprette plukkarbeidet

Når en bølge er opprettet og inneholder alle de nødvendige linjene, er du klar til å behandle den for å opprette tilsvarende plukkarbeid.

#### <a name="automatically-process-a-wave"></a>Behandle en bølge automatisk

Hvis du vil behandle en bølge automatisk, konfigurerer du de relevante [bølgemalene](wave-templates.md) med de automatiske behandlingsalternativene som kreves.

#### <a name="manually-process-a-wave"></a>Behandle en bølge manuelt

Du kan bare behandle en bølge når **Bølgestatus** er *Opprettet*. Når du har behandlet en bølge, endres **Bølgestatus** til *Holdt*.

Følg denne fremgangsmåten for å behandle en bølge manuelt med alt det nødvendige innholdet:

1. Avhengig av hvilken type bølge du vil behandle, gjør du ett av følgende:

    - Velg **Lagerstyring** \> **Felles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**. Velg **Bølge** i handlingsruten.
    - Velg **Lagerstyring** \> **Felles** \> **Bølger** \> **Produksjonsbølger** \> **Alle produksjonsbølger**. Velg **Produksjonsbølge** i handlingsruten.
    - Velg **Lagerstyring** \> **Felles** \> **Bølger** \> **Kanban-bølger** \> **Alle Kanban-bølger**. Velg **Opprett bølge** i handlingsruten.

1. Velg bølgen som skal behandles. Klikk på **Prosess** i handlingsruten.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Frigi bølgen til lageret for å starte plukking og pakking

Du må behandle en bølge før du kan frigi den. Når du frigir bølgen, blir plukkarbeidet tilgjengelig på lageret. Du kan avbryte en bølge etter at den er frigitt, og legge til flere linjer, men du kan ikke endre linjene.

#### <a name="automatically-release-a-wave"></a>Frigi en bølge automatisk

Hvis du vil behandle en bølge automatisk, konfigurerer du de relevante [bølgemalene](wave-templates.md) med de automatiske behandlingsalternativene som kreves.

#### <a name="manually-release-a-wave"></a>Frigi en bølge manuelt

Hvis du vil frigi en bølge manuelt, gjør du følgende:

1. Avhengig av hvilken type bølge du vil frigi, gjør du ett av følgende:

      - Velg **Lagerstyring** \> **Felles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**. Velg **Bølge** i handlingsruten.
      - Velg **Lagerstyring** \> **Felles** \> **Bølger** \> **Produksjonsbølger** \> **Alle produksjonsbølger**. Velg **Produksjonsbølge** i handlingsruten.
      - Velg **Lagerstyring** \> **Felles** \> **Bølger** \> **Kanban-bølger** \> **Alle Kanban-bølger**. Velg **Opprett bølge** i handlingsruten.

1. Velg bølgen som skal frigis. Velg **Frigi bølge** i handlingsruten.

## <a name="containerize-a-wave"></a>Plassere en bølge i container

Automatisert containerbruk oppretter containere og plukkarbeidet for forsendelser når en bølge behandles. Hvis du vil ha mer informasjon om hvordan du konfigurerer det, kan du se [Containerbruk](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Arbeide med opprettingen av planlagt arbeid

Når funksjonen *Planlegg arbeidsopprettelse* er aktivert, oppretter bølgebehandling planlagt arbeid, som til slutt blir brukt av den nye prosessen for arbeidsopprettelse. Under arbeidsopprettelse blir arbeidet blokkert ved hjelp av funksjonen *Organisasjonsomfattende arbeidsblokkering*. Hvis du vil ha mer informasjon, kan du se [Planlegge arbeidsopprettelse under bølge](configure-wave-schedule-work-creation.md).

Følgende flytdiagram viser hvordan planlagt arbeid blir opprettet under bølgebehandling.

![Planlegg arbeidsoppretting.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Planlagt arbeid

Siden **Detaljer om planlagt arbeid** (**Lagerstyring \> Arbeid \> Detaljer om planlagt arbeid**) viser informasjon om det planlagte arbeidet, som opprinnelig ble opprettet under bølgebehandling. Følgende verdier for **Prosesstatus** er tilgjengelige:

- **Satt i kø** – Det planlagte arbeidet venter på å bli brukt til å opprette arbeid.
- **Fullført** – Det planlagte arbeidet har blitt brukt til å opprette arbeid.
- **Mislykket** – Bølgebehandlingen har mislyktes. Merk at det planlagte arbeidet kan være i tilstanden **Mislykket** med eller uten tilknyttet faktisk arbeid. Når den faktiske prosessen for arbeidsopprettelse mislykkes, forblir statusen for faktisk arbeid *Avbrutt*.

### <a name="batch-job-for-the-work-creation-process"></a>Satsvis jobb for prosessen for arbeidsopprettelse

Hvis du vil vise de satsvise jobbene for bølgebehandling, velger du **Satsvise jobber** i handlingsruten på **Alle bølger**-siden.

Her kan du vise alle detaljene om den satsvise oppgaven for hver ID for satsvis jobb.

## <a name="cancel-a-wave"></a>Avbryt en bølge

Om nødvendig kan du avbryte en bølge som er behandlet. Hvis du vil avbryte en bølge og plukkarbeidet som ble opprettet, følger du denne fremgangsmåten:

1. Avhengig av hvilken type bølge du vil avbryte, gjør du ett av følgende:

      - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Forsendelsesbølger** \> **Alle bølger**.
      - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Produksjonsbølger** \> **Alle produksjonsbølger**.
      - Gå til **Lagerstyring** \> **Felles** \> **Bølger** \> **Kanban-bølger** \> **Alle Kanban-bølger**.

1. Velg bølgen som skal avbrytes. Velg **Avbryt** i **Arbeid**-fanen i handlingsruten.

## <a name="review-wave-batch-job-details"></a>Gå gjennom detaljer om satsvis jobb for bølge

Bruk siden **Detaljer om satsvis jobb for bølge** til å inspisere de satsvise joggene og relaterte oppgaver knyttet til en bølge. Dette er særlig nyttig for feilsøking av en bølge som har mislyktes. Uten denne funksjonen vil bare administratorer vanligvis ha tilgang til detaljer om satsvise jobber. Siden **Detaljer om satsvis jobb for bølge** kan bli gjort tilgjengelig for ikke-administratorbrukere og fungerer som en skrivebeskyttet vising av satsvise jobber og relaterte oppgaver.

### <a name="enable-the-wave-batch-job-details-page"></a>Aktiver siden Detaljer om satsvis jobb for bølge

Hvis systemet ikke allerede inkluderer siden **Detaljer om satsvis jobb for bølge**, kan du gå til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Detaljer om satsvis jobb for bølge*.

### <a name="use-the-wave-batch-job-details-page"></a>Bruk siden Detaljer om satsvis jobb for bølge

Siden **Detaljer om satsvis jobb for bølge** kombinerer satsvise jobber og oppgaver i satsvise jobber, slik at du kan undersøke alle bølgetrinnene uten å måtte gå frem og tilbake mellom én enkelt satsvis jobb og listen over satsvise jobber. Siden gir også tilgang til den satsvise loggen, og hvis du har de nødvendige tillatelsene, kan du opprette en kobling til siden **Satsvise jobber**.

Hvis du vil åpne denne siden, velger du en bølge på en av flere ulike bølgesider, og velger deretter **Detaljer om satsvis jobb for bølge** fra handlingsruten.

## <a name="review-load-validation-and-error-messages"></a>Gå gjennom lastvalidering og feilmeldinger

Under bølgebehandlingen validerer og viser systemet statusen for hver lastlinje i bølgen. Hvis det ikke forekommer noen advarsler, går den videre til neste bølgetrinn. Hvis advarsler forekommer, viser den i stedet følgende feil etter at den er fullført med å validere hele bølgen:

> Funnet ugyldige lastlinjer i bølge. Fjern de ugyldige lastlinjene.

Du kan da gå gjennom den endelige statusen til hver lastlinje i bølgen og rette alle advarselene før du prøver på nytt. På denne måten kan du håndtere alle advarselene samtidig før du håndterer bølgen på nytt. (I tidligere versjoner stoppet systemet behandling av bølgen etter den første advarselen, så du kunne bare korrigere én advarsel om gangen.)

Hvordan systemet viser meldinger om bølgebehandlingsstatus, avhenger av hvordan du har angitt alternativet **Opprett historikklogg for bølgebehandling** på siden **Lagerstyringsparametere**.

- Når **Opprett historikklogg for bølgebehandling** er satt til *Nei*, vises statusmeldinger for lastlinjer i **Infologg**.
- Når **Opprett historikklogg for bølgebehandling** er satt til *Ja*, vises statusmeldinger for lastlinjer på siden **Historikklogg for bølgebehandling**. Hvis du vil vise loggen, kan du gå til **Lagerstyring \> Utgående bølger \> Historikklogg for bølgebehandling**.

## <a name="additional-resources"></a>Tilleggsressurser

- [Konfigurere bølgebehandlingseksempel](tasks/configure-wave-processing.md)
- [Bølgemaler](wave-templates.md)
- [Containerbruk](wave-containerization.md)