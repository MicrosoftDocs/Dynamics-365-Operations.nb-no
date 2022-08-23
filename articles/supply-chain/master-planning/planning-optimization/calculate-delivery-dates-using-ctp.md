---
title: Beregn leveringsdatoer for salgsordrer ved hjelp av CTP
description: Med leveringskapasitetsfunksjonalitet (CTP) kan du gi kunder realistiske datoer for når du kan love bestemte varer. Denne artikkelen beskriver hvordan du definerer og bruker CTP for hver planleggingsmotor (planleggingsoptimalisering og den innebygde motor).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 9a2d8a66fe7e68ebd5729a401af3f0efe04051b1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229941"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Beregn leveringsdatoer for salgsordrer ved hjelp av CTP

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Med leveringskapasitetsfunksjonalitet (CTP) kan du gi kunder realistiske datoer for når du kan love bestemte varer. For hver salgslinje kan du angi en dato som tar hensyn til eksisterende lagerbeholdning, produksjonskapasitet og transporttider.

CTP utvider funksjonen [tilgjengelig for ordre](../../sales-marketing/delivery-dates-available-promise-calculations.md) (ATP) ved å vurdere kapasitetsinformasjon. Mens ATP bare vurderer materialtilgjengelighet og antar ubegrenset kapasitetsressurser, vurderer CTP tilgjengelighet for både materialer og kapasitet. Derfor gir det et mer realistisk bilde av om behovet kan oppfylles innenfor en gitt tidsramme.

CTP fungerer litt annerledes, avhengig av hovedplanleggingsmotoren du bruker (planleggingsoptimalisering eller den innebygde hovedplanleggingsmotoren). Denne artikkelen beskriver hvordan du setter opp den for hver motor. CTP for planleggingsoptimalisering støtter for øyeblikket bare et delsett av CTP-scenarioene som støttes av den innebygde motoren.

## <a name="turn-on-ctp-for-planning-optimization"></a>Aktiver CTP for planleggingsoptimalisering

CTP for den innebygde hovedplanleggingsmotoren er alltid tilgjengelig. Hvis du imidlertid vil bruke CTP for planleggingsoptimalisering, må den aktiveres for systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Hovedplanlegging*
- **Funksjonsnavn:** *(Forhåndsversjon) CTP for planleggingsoptimalisering*

## <a name="how-ctp-compares-to-atp"></a>Hvordan CTP sammenlignes med ATP

CTP og ATP er like, men CTP kan ofte gi et mer nøyaktig resultat, som følgende eksempel viser.

Vare A er en vare som består av vare B og C, og beholdning av vare A er 0 (null). Hvis du gjør en ATP-kontroll som bare tar hensyn til materialer, vil ATP-antallet også være 0 (null). Hvis du imidlertid foretar en CTP-kontroll, kontrollerer systemet tilgjengeligheten av varer B og C, kontrollerer ressursene som kreves for å gjøre dem til vare A, og beregner hvor mange av vare A som kan gjøres. I tillegg kan CTP-beregningen kontrollere ressursene og materialene som kreves for å lage flere varer B og C, og bruke dem til å gjøre mer av vare A.

En CTP-beregning som tar hensyn til både materialer og ressurser, kan vise et større antall enn en beregning som bare kontrollerer materialer, spesielt når varen som kontrolleres, er en vare som skal settes sammen etter ordre. CTP-funksjonaliteten er med andre ord basert på nedbrytingsfunksjonen, og kan kjøres for en valgt salgsordrelinje for å beregne forventet leveringsdato.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Hvordan CTP varierer avhengig av hovedplanleggingsmotoren du bruker

Tabellen nedenfor summerer forskjellene mellom CTP for planleggingsoptimalisering og CTP for den innebygde hovedplanleggingsmotoren.

| Element | Planleggingsoptimalisering | Innebygd hovedplanleggingsmotor |
|---|---|---|
| Innstillingen for **leveringsdatokontroll** for ordrer, ordrelinjer og produkter | *CTP for planleggingsoptimalisering* | *CTP* |
| Beregningstidspunkt | Beregningen utløses ved å kjøre en dynamisk plan som en planlagt oppgave. | Beregningen utløses umiddelbart hver gang du angir eller oppdaterer en salgsordrelinje. |
| Feltverdi **CTP for planleggingsoptimalisering** | <p>Verdien *Ikke klar* vises for ordrer og ordrelinjer der den dynamiske planen ikke har kjørt siden ordrene og linjene ble opprettet eller sist oppdatert.</p><p>En verdi av *Klar* vises for ordrer og linjer der CTP er brukt til å beregne bekreftede leveringsdatoer ved å kjøre den dynamiske planen.</p> | Verdien *Klar* vises alltid. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>Angi standard kontrollmetoder for leveringsdato

Systemet kan bruke en av flere metoder for å beregne leveringsdatoestimater for hver ordre og ordrelinje. Du bør angi metoden for leveringsdatokontroll som du vil bruke oftest som global standardmetode. Du kan også angi individuelle overstyring for hvert produkt. Senere kan du overstyre standardmetodene for hver ordre eller ordrelinje etter behov.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>Angi global standard leveringsdatokontroll

Standard kontrollmetode for leveringsdato brukes på alle nye ordrelinjer der en overstyring ikke gjelder. Følg denne fremgangsmåten for å velge en.

1. Gå til **Kunder \> Oppsett \> Kundeparametere**.
1. Velg metoden du vil bruke som standardmetode for firmaet, i feltet **Leveringsdatokontroll** i fanen **Forsendelser** på hurtigfanen **Leveringskontroll**:

    - *Ingen* – Ikke beregn bekreftede leveringsdatoer.
    - *Salgsleveringstid* – Salgsleveringstiden er tiden mellom opprettelsen av salgsordren og leveringen av varene. Beregningen av leveringsdato er basert på et standard antall dager, og vurderer ikke lagertilgjengelighet, kjente behov eller planlagt forsyning.
    - *ATP* – ATP er antallet av en vare som er tilgjengelig og kan loves til en kunde på en bestemt dato. ATP-beregningen inkluderer ikke igangsatt lager, leveringstider, planlagte mottak, og avganger.
    - *ATP + Avgang-margin*– Forsendelsesdatoen er lik ATP-datoen pluss antall sikkerhetsdager for varen. Sikkerhetsdager er tiden det tar å klargjøre varene for forsendelse.
    - *CTP* – Bruk CTP-beregningen som leveres av den innebygde hovedplanleggingsmotoren. Hvis du bruker planleggingsoptimalisering, er ikke *CTP*-leveringsdatokontrollmetoden tillatt, og hvis dette er valgt, vil det forårsake en feil når beregningen kjøres.
    - *CTP for planleggingsoptimalisering* – Bruk CTP-beregningen som tilbys ved planleggingsoptimalisering. Dette alternativet har ingen innvirkning hvis du bruker den innebygde hovedplanleggingsmotoren.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Angi overstyringer av leveringsdatokontroll for individuelle produkter

Du kan tildele overstyringer for bestemte produkter der du vil bruke en annen leveringsdatokontrollmetode enn den som er angitt som den globale standardmetoden.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg produktet du vil opprette.
1. På handlingsruten, i fanen **Administrer lager** i gruppen **Ordreinnstillinger**, velger du **Standard ordreinnstillinger**.
1. Angi alternativet **Overstyr leveringskontroll** til **Ja** på siden **Standard ordreinnstillinger** i hurtigfanen *Salgsordre*.
1. Velg metoden som skal brukes for det valgte produktet, i feltet **Leveringsdatokontroll**. De samme alternativene som beskrives under delen [Angi global standard leveringsdatokontroll](#global-default), er tilgjengelige.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>Planlegge CTP for beregninger av planleggingsoptimalisering

Når du bruker CTP for planleggingsoptimalisering, må du kjøre en dynamisk plan for å utløse systemet til å utføre CTP-beregningene og deretter angi de bekreftede leverings- og mottaksdatoene for alle relevante ordrer. Planen må inneholde alle varer som bekreftede forsendelses- og mottaksdatoer er nødvendige for. (Når du bruker CTP for den innebygde planleggingsmotoren, utføres CTP-beregningene umiddelbart lokalt. Derfor trenger du ikke å kjøre en dynamisk plan for å se CTP-resultatene.)

For å sikre at datoene er tilgjengelige i god tid for alle brukere, anbefaler vi at du setter opp satsvise jobber for å kjøre de relevante planene regelmessig. En satsvis jobb som er konfigurert til å kjøre en dynamisk plan hvert 30. minutt, vil for eksempel angi det bekreftede forsendelses- og mottaksdatoen hvert 30. minutt. Derfor må brukere som legger inn og importordrer, vente maksimalt 30 minutter for å hente bekreftede forsendelses- og mottaksdatoer.

Følg denne fremgangsmåten for å sette opp en satsvis jobb for å kjøre en dynamisk plan med jevne mellomrom.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Hovedplanlegging**.
1. I dialogboksen **Hovedplanlegging** angir du **Hovedplan**-feltet til den dynamiske planen du vil kjøre, i hurtigfanen **Parametere**.
1. På hurtigfanen **Kjør i bakgrunnen** setter du **Satsvis behandling** til *Ja*.
1. Velg **Regelmessighet**, og definer planen etter behov.
1. Velg **OK** for å lagre planen.
1. Velg **OK** for å opprette den satsvise jobben og lukke dialogboksen.

## <a name="use-ctp-for-built-in-master-planning"></a>Bruk CTP for innebygd hovedplanlegging

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Opprett en ny ordre ved å bruke CTP til innebygd hovedplanlegging

Hver gang du legger til en ny salgsordre eller ordrelinje, tildeler systemet en standard kontrollmetode for leveringsdato til den. Ordrehodet starter alltid med den globale standardmetoden. Hvis en overstyring tildeles til en bestilt vare, bruker den nye ordrelinjen denne overstyringen. Ellers vil den nye ordrelinjen også bruke den globale standardmetoden. Derfor bør du angi standardmetodene slik at de samsvarer med leveringsdatokontroll som du vil bruke oftest. Når du har opprettet en ordre, kan du overstyre standardmetoden på ordrehode- eller ordrelinjenivået etter behov. Hvis du vil ha mer informasjon , kan du se [Angi standard kontrollmetoder forleveringsdato](#default-methods) og [Endre eksisterende salgsordrer for å bruke CTP](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Vis bekreftede leveringsdatoer når du bruker CTP for innebygd hovedplanlegging

Hvis du bruker den innebygde hovedplanleggingsmotoren, brukes CTP-beregninger for ordrer eller ordrelinjer der feltet **Leveringsdatokontroll** er satt til *CTP*.

Når det gjelder salgslinjer som bruker CTP for innebygd hovedplanlegging, definerer systemet automatisk feltene **Bekreftet forsendelsesdato** og **Bekreftet mottaksdato** hver gang du lagrer en salgslinje. Hvis du senere gjør en relevant endring i en salgslinje (for eksempel ved å endre antall eller område), blir datoene omberegnet umiddelbart.

- Hvis du vil vise bekreftede leveringsdatoer for en salgsordrelinje, åpner du salgsordren og velger salgslinjen. Deretter på hurtigfanen **Linjedetaljer** i fanen **Levering** ser du gjennom verdiene **Bekreftet forsendelsesdato** og **Bekreftet mottaksdato**.
- Hvis du vil vise bekreftede leveringsdatoer for en hel ordre, åpner du salgsordren og velger visningen **Hode**. Deretter på hurtigfanen **Levering** ser du gjennom verdiene **Bekreftet forsendelsesdato** og **Bekreftet mottaksdato**.

## <a name="use-ctp-for-planning-optimization"></a>Bruk CTP for planleggingsoptimalisering

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Opprett en ny ordre ved å bruke CTP for planleggingsoptimalisering

Hver gang du legger til en ny salgsordre eller ordrelinje, tildeler systemet en standard kontrollmetode for leveringsdato til den. Ordrehodet starter alltid med den globale standardmetoden. Hvis en overstyring tildeles til en bestilt vare, bruker den nye ordrelinjen denne overstyringen. Ellers vil den nye ordrelinjen også bruke den globale standardmetoden. Derfor bør du angi standardmetodene slik at de samsvarer med leveringsdatokontroll som du vil bruke oftest. Når du har opprettet en ordre, kan du overstyre standardmetoden på ordrehode- eller ordrelinjenivået etter behov. Hvis du vil ha mer informasjon , kan du se [Angi standard kontrollmetoder forleveringsdato](#default-methods) og [Endre eksisterende salgsordrer for å bruke CTP](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Vis bekreftede leveringsdatoer ved bruk av CTP for planleggingsoptimalisering

Hvis du bruker planleggingsoptimalisering, brukes CTP-beregninger for ordrer eller ordrelinjer der feltet **Leveringsdatokontroll** er satt til *CTP for planleggingsoptimalisering*.

For salgslinjer som bruker CTP for planleggingsoptimalisering, er feltene **Bekreftet forsendelsesdato** og **Bekreftet mottaksdato** tomt til du kjører den riktige dynamiske planen (vanligvis ved å bruke en periodisk satsvis jobb). Deretter angis de automatisk. Hvis du vil ha mer informasjon, kan du se [Planlegg beregninger for CTP for planleggingsoptimalisering](#batch-job).

Feltet **CTP for planleggingsoptimaliseringsstatus** angir om bekreftede datoer ennå er beregnet for hver linje som bruker CTP for planleggingsoptimalisering. Feltet viser verdien *Ikke klar* for linjer og ordrer der de bekreftede leveringsdatoene enten ikke er beregnet ennå eller ikke lenger er gyldige på grunn av andre endringer. Den viser verdien *Klar* til linjer og ordrer som er beregnet. Du kan vise statusen for hver linje og for hele ordren.

- Hvis du vil vise statusen for en salgsordrelinje, åpner du salgsordren og velger salgslinjen. I hurtigfanen **Linjedetaljer** på fanen **Levering** går du gjennom verdien **CTP for planleggingsoptimaliseringsstatus**. Feltene **Bekreftet forsendelsesdato** og **Bekreftet mottaksdato** for linjen vises også i denne fanen etter at de er beregnet.
- Hvis du vil vise statusen for en hel ordre, åpner du salgsordren og velger visningen **Hode**. I hurtigfanen **Levering** går du gjennom verdien **CTP for planleggingsoptimaliseringsstatus**. Feltene **Bekreftet forsendelsesdato** og **Bekreftet mottaksdato** for ordren vises også i denne fanen etter at de er beregnet.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Hvis du oppdaterer en salgsordrelinje etter at CTP for planleggingsoptimalisering har beregnet bekreftede datoer for den, vil systemet fjerne datoene til neste gang den aktuelle dynamiske planen kjøres.
> - Hvis du redigerer en relatert innstilling som kan påvirke eksisterende bekreftede datoer (for eksempel ved å endre leveringstid, reserveringer eller merkinger), bør du fjerne de bekreftede datoene for de relevante eksisterende ordrene. Denne handlingen fører til at statusen for hver relevante linje endres til *Ikke klar*. Denne endringen fører i sin tur til at systemet beregner de bekreftede datoene på nytt neste gang den kjører den dynamiske planen.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>Endre eksisterende salgsordrer slik at de bruker CTP

Du kan endre verdien **Leveringsdatokontroll** for en hvilken som helst åpen ordre når som helst. Du kan endre verdien på overskriftsnivå eller for hver linje etter behov.

### <a name="change-to-ctp-at-the-order-header-level"></a>Endre til CTP på ordrehodenivå

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Følg denne fremgangsmåten for å endre en ordre slik at den bruker CTP på ordrehodenivå.

1. Gå til **Kunde \> Ordrer \> Alle salgsordrer**.
1. Åpne salgsordren du vil definere, eller opprett en ny.
1. Velg **Hode** for å åpne hodeinformasjonen på siden **Salgsordredetaljer**.
1. I hurtigfanen **Levering** angir du en av følgende verdier i feltet **Leveringsdatokontroll**, avhengig av planleggingsmotoren du bruker:

    - *CTP* – Bruk CTP-beregningen som leveres av den innebygde hovedplanleggingsmotoren. Hvis du bruker planleggingsoptimalisering, er ikke *CTP*-leveringsdatokontrollmetoden tillatt. Hvis du velger denne verdien, vil det derfor oppstå en feil når beregningen kjører.
    - *CTP for planleggingsoptimalisering* – Bruk CTP-beregningen som tilbys ved planleggingsoptimalisering. Denne innstillingen har ingen innvirkning hvis du bruker den innebygde hovedplanleggingsmotoren.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Velg **OK** for å bruke endringene.

### <a name="change-to-ctp-at-the-order-line-level"></a>Endre til CTP på ordrelinjenivået

Hvis du opprettet en ordrelinje ved hjelp av en annen leveringsdatokontrollmetode, kan du når som helst endre til CTP. Endringer som foretas på linjenivå, påvirker ingen andre linjer. De kan imidlertid føre til at de samlede ordreleveringsdatoene flyttes fremover eller bakover, avhengig av hvordan hver oppdaterte linjeberegning endres. <!-- KFM: Confirm this intro at next revision -->

Følg denne fremgangsmåten for å endre en ordre slik at den bruker CTP for innebygd hovedplanlegging på linjenivå.

1. Gå til **Kunde \> Ordrer \> Alle salgsordrer**.
1. Åpne salgsordren du vil definere, eller opprett en ny.
1. Velg salgsordrelinjen du vil definere, i fastfanen **Salgsordrelinje** på siden **Salgsordredetaljer**.
1. På hurtigfanen **Linjedetaljer** på fanen **Levering** angir du en av følgende verdier i feltet **Leveringsdatokontroll**, avhengig av planleggingsmotoren du bruker:

    - *CTP* – Bruk CTP-beregningen som leveres av den innebygde hovedplanleggingsmotoren. Hvis du bruker planleggingsoptimalisering, er ikke *CTP*-leveringsdatokontrollmetoden tillatt. Hvis du velger denne verdien, vil det derfor oppstå en feil når beregningen kjører.
    - *CTP for planleggingsoptimalisering* – Bruk CTP-beregningen som tilbys ved planleggingsoptimalisering. Denne innstillingen har ingen innvirkning hvis du bruker den innebygde hovedplanleggingsmotoren.

    Dialogboksen **Tilgjengelige leverings- og mottaksdatoer** vises, og viser tilgjengelige forsendelses- og mottaksdatoer. Denne dialogboksen fungerer på samme måte for ordrelinjer som for ordrehodet, som beskrevet i forrige del.

1. Velg **Lagre** i handlingsruten.
