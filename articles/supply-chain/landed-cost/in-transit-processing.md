---
title: Behandling av varer i transitt
description: Dette emnet beskriver hvordan du arbeider med ordrer for varer i transitt. Når en ordre eller sjøreise er satt opp til å bruke behandling av varer i transitt, kan varer faktureres før de er mottatt på lageret for forbruk.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: fff3c3cfe5d0628fd4df6e719b72bc134c9d9c0a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909457"
---
# <a name="goods-in-transit-processing"></a>Behandling av varer i transitt

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du arbeider med ordrer for varer i transitt. Denne typen ordre brukes bare av modulen **Netto innkjøpspris**. Når en ordre eller sjøreise er satt opp til å bruke behandling av varer i transitt, trenger du ikke vente til varer er mottatt på lager før du kan fakturere dem. I stedet faktureres varene når de går ut av leverandørens lager eller opprinnelseshavn, og de økonomiske kostnadene gjenkjennes når sjøreisen starter. Ved hjelp av denne funksjonaliteten kan du ta eierskap av lageret på riktig måte, ettersom varer ofte blir eiendommen til organisasjonen din når de forlater forsendelseshavnen.

Når det brukes ordrer for varer i transitt, mottas de økonomisk oppdaterte varene i et midlertidig lager som kalles et transittlager for varer. Varene forblir deretter i dette lageret til de kan mottas ved det endelige mållageret (det vil si lageret som er definert på innkjøpslinjen). De kan ikke fjernes manuelt.

Så lenge varene er i transitt, er de ikke tilgjengelige på lageret og kan ikke plukkes fra lageret for en levering. Du kan imidlertid vise lagerbeholdningen for varer i transitt. Du kan også bruke varene til hovedplanlegging. I dette tilfellet bruker du bekreftet leveringsdato på bestillingslinjen som forventet dato når lageret vil være tilgjengelig for forbruk.

Delene nedenfor beskriver oppsettet som kreves for å behandle lager og sjøreiser ved hjelp av konseptet og funksjonaliteten for varer i transitt.

## <a name="terms-of-delivery"></a>Leveringsbetingelser

Når du aktiverer modulen **Netto innkjøpspris**, utvides enheten *Leveringsbetingelser* for å støtte funksjonen for varer i transitt.

Når alternativet **Varer i transittstyring** er satt til *Ja* for gjeldende leveringsbetingelser, settes varene til lageret for varer i transitt. Denne handlingen utløses bare hvis lagermottaket ikke behandles før en faktura behandles. Når leveringsbetingelsene for en ordre er satt til å bruke varer i transitt, kan ikke brukere lenger postere en produktkvittering for bestillingen. Hvis de prøver, oppstår det en feil. Feilmeldingen angir at de må bruke funksjonaliteten for varer i transitt for å fortsette.

Hvis du vil arbeide med leveringsbetingelser for varer i transitt, kan du gå til **Innkjøp og leverandører \> Oppsett \> Distribusjon \> Leveringsbetingelser**. Tabellen nedenfor beskriver feltene som modulen **Netto innkjøpspris** legger til på siden **Leveringsbetingelser** for å støtte funksjonaliteten for varer i transitt. Begge feltene er i hurtigfanen **Generelt**. Hvis du vil ha mer informasjon om de andre feltene på denne siden, kan du se [Leveringsbetingelser (skjema)](/dynamicsax-2012//terms-of-delivery-form).

| Felt | beskrivelse |
|---|---|
| Forsendelseshavn obligatorisk | Sett dette alternativet til *Ja* hvis en forsendelseshavn er obligatorisk når leveringsbetingelsene gjelder. |
| Styring av varer i transitt | Sett dette alternativet til *Ja* for å bruke håndtering av varer i transitt når leveringsbetingelsene gjelder. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Lagre for varer i transitt og underlevering

Når du aktiverer modulen **Netto innkjøpspris**, utvides standardenheten *Lagere* for å gjøre det mulig å fakturere bestillinger mens varene er i et transittlager for varer.

Netto innkjøpspris legger til to nye lagertyper: *varer i transitt* og *underlevering*. Lagre av begge typer kan velges som standardlagre. Vellykket behandling av varer for ordrer i transitt krever at både lageret for varer i transitt og underleveringslageret konfigureres på siden **Lagre**. For hvert standardlager som skal brukes med landede kostnader og varer i transitt, må deretter lageret for varer i transitt og underleveringslager velges for de tilgjengelige lagrene av hver type.

Lagertypen *Varer i transitt* vil bli tilknyttet lageret for varer i transitt, og dette lageret vil bli brukt til å behandle varene i transittordrer for varer i transitt før de mottas ved det endelige destinasjonslageret. Vanligvis er ett lager for varer i transitt nok for hvert område hvis Område og Lager er de eneste lagerdimensjonene som brukes til lagerstyring. Hvis lagerlokasjonsdimensjonen også brukes, må det defineres et lager for varer i transitt for hver kombinasjon av et område og et lager, slik at standardlokasjonen også kan angis.

Hvis du vil arbeide med innstillinger for varer i transitt for lagrene, kan du gå til **Lagerstyring \> Oppsett \> Lageroppdeling \> Lagre**. Tabellen nedenfor beskriver feltene som modulen **Netto innkjøpspris** legger til på siden **Lagre** for å støtte funksjonaliteten for varer i transitt. Begge feltene vises i hurtigfanen **Generelt**. Hvis du vil ha informasjon om andre felter på siden, kan du se [Lagre (skjema)](/dynamicsax-2012//warehouses-form).

| Felt | beskrivelse |
|---|---|
| Varer i transitt-lager | Identifiser lageret for varer i transitt som er knyttet til hovedlageret. |
| Underleveringslager | Identifiser lageret for underlevering som er knyttet til hovedlageret. |

## <a name="posting-rules-for-landed-cost"></a>Posteringsregler for netto innkjøpspris

Netto innkjøpspris legger til to nye posteringsregler som du kan konfigurere. Disse posteringsreglene brukes til å postere fakturabeløpene for direkte bestillinger økonomisk for å identifisere eierskap av varene når de forlater opprinnelsesstedet. Denne prosessen erstatter konseptet med *mottatte varer som ikke er fakturert*, fordi varene faktureres før de mottas. <!-- KFM: Add a link to the related scenario when available. -->

Hvis du vil arbeide med posteringsprofiler, kan du gå til **Lagerstyring \> Oppsett \> Postering \> Postering**. Følgende nye posteringsregler er tilgjengelige i fanen **Bestilling**:

- **Netto innkjøpspris, varer i transitt** – Angi posteringsreglene for håndtering av varer i transitt.
- **Netto innkjøpspris, avregning for kostnadsavsetning** – Angi posteringsreglene for avregning av avsetningskonto.

## <a name="goods-in-transit-orders"></a>Ordrer for varer i transitt

Du kan gå gjennom og administrere ordrer for varer i transitt i modulen **Netto innkjøpspris**. Du kan behandle ordrer for varer i transitt fra siden **Ordrer for varer i transitt**. Alternativt kan du gå til sjøreisen som er knyttet til ordrene for varer i transitt og behandle hele sjøreisen, forsendelsescontaineren eller folioen. Når du fakturerer en sjøreise og oppretter ordrer for varer i transitt, opprettes det en ny ordre for vare i transitt for hver kombinasjon av lager- og lagerdimensjoner som er knyttet til bestillingslinjen.

Når du skal administrere varer i transitt, bruker Netto innkjøpspris en fremgangsmåte i to trinn:

1. En vare mottas når en lagerfaktura behandles og tilordnes statusen *I transitt*.
1. Bestillingen for varer i transitt behandles på siden **Ordrer for varer i transitt**, og mottas deretter i lageret som er angitt på bestillingen. På dette tidspunktet endres statusen til *Mottatt*.

Hvis du vil arbeide med ordrer for varer i transitt, går du til **Netto innkjøpspris \> Periodiske oppgaver \> Ordrer for varer i transit**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Mottaksbeholdning fra lageret for varer i transitt

Du kan motta varer fra en ordre for varer i transitt på mange måter, avhengig av hvordan systemet er satt opp.

### <a name="in-transit-receiving"></a>Mottak i transitt

Du kan gjøre transittmottak fra en av følgende sider:

- På siden **Ordrer for varer i transitt** velger du linjen, og deretter velger du **Motta** i handlingsruten.
- Velg eller åpne en sjøreise på siden **Alle sjøreiser**. I handlingsruten i gruppen **Varer i transitt** i fanen **Behandle** velger du **Motta varer i transitt** i handlingsruten.
- På siden **Alle forsendelsescontainere** velger eller åpner du en forsendelsescontainer. I handlingsruten i gruppen **Varer i transitt** i fanen **Behandle** velger du **Motta varer i transitt** i handlingsruten.
- Velg eller åpne en folio på siden **Alle folioer**. I handlingsruten i gruppen **Varer i transitt** i fanen **Behandle** velger du **Motta varer i transitt** i handlingsruten.

> [!NOTE]
> Mottak i transitt brukes vanligvis i situasjoner der lokasjoner og parti-/seriesporing ikke brukes.

### <a name="arrival-journal"></a>Ankomstjournal

Du kan også motta varer ved å opprette en ankomstjournal. Du kan opprette en ankomstjournal direkte fra sjøreisesiden. Anbefalte fremgangsmåter som organisasjonen har fastsatt, fastslår om ankomstjournalen brukes til å motta varer.

1. Åpne sjøreisen, containeren eller folioen.
1. Velg **Opprett ankomstjournal** i gruppen **Funksjoner** i fanen **Behandle** i handlingsruten.
1. I dialogboksen **Opprett ankomstjournal** angir du følgende verdier:
    - **Initialiser antall** – Sett dette alternativet til *Ja* for å angi antallet fra transittantallet. Hvis du setter dette alternativet til *Nei*, angis det ikke noe standard antall fra linjene i transitt for varer.
    - **Opprett fra varer i transitt** – Sett dette alternativet til *Ja* for å ta antall fra de valgte transittlinjene for den valgte sjøreisen, containeren eller folioen.
    - **Opprett fra ordrelinjer** – Sett dette alternativet til *Ja* for å angi standardantallet i ankomstjournalen fra bestillingslinjene. Standardantallet i ankomstjournalen kan bare defineres på denne måten hvis antallet på bestillingslinjen samsvarer med antallet på ordren for varer i transitt.

1. Behandle ankomstjournalen som beskrevet i [Registrere varemottak med en vareankomstjournal](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal).

> [!NOTE]
> Ankomstjournalen brukes vanligvis i situasjoner der det brukes lokasjoner og parti-/seriesporing, men lagerstyring brukes ikke.
>
> Det må ikke angis standard mottakslokasjoner på ordrelinjene hvis en stedsankomst blir angitt i ankomstjournalen.

## <a name="warehouse-management"></a>Lagerstyring

Når du aktiverer modulen **Netto innkjøpspris**, endres flere sider i modulen **Lagerstyring** slik at ordrebehandling (spesielt behandling av varer i transitt) kan gjøres via modulen **Netto innkjøpspris**. Denne delen beskriver feltene og prosessene som er lagt til i modulen **Lagerstyring**.

### <a name="mobile-device-menu-items"></a>Menyelementer på mobilenheten

Varer kan mottas ved hjelp av en mobilenhet, forutsatt at mobilenhetsmenyen og modulen **Lagerstyring** er satt opp til å motta varer på en transittordre for varer. Denne delen beskriver oppsettet som er knyttet til mottak av varer i transitt.

Hvis du vil konfigurere mobilenheter for behandling av varer i transitt, kan du gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.

Netto innkjøpspris legger til følgende arbeidsopprettingsprosesser i menyelementene for mobilenheten for å støtte behandling av varer i transitt:

- Mottak av varer i transitt-vare
- Mottak og plassering av vare for varer i transitt

Konfigurasjonsinnstillingene for disse prosessene ligner innstillingene for [arbeidsopprettingsprosessene for mottak og plassering av bestillinger](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work). Prosessen *Mottak og plassering av vare for varer i transitt* legger også til følgende felt.

- **Aktiver forsendelsescontainer fullført** – Hvis dette alternativet er satt til *Ja*, gir mobilappen Lagerstyring et tilleggsalternativ som kalles **Forsendelsescontainer fullført** når plasseringsarbeidet er fullført. Når det er merket av for dette alternativet, blir arbeideren bedt om å bekrefte at containeren er fullført. På dette tidspunktet behandles alle korte mottak som en undertransaksjon.

### <a name="location-directives"></a>Lokasjonsdirektiver

Netto innkjøpspris legger til en ny arbeidsordretype med navnet *Varer i transitt* på siden **Lokasjonsdirektiver**. Denne arbeidsordretypen må konfigureres på samme måte som [arbeidsordretypene for bestillinger](/dynamicsax-2012/appuser-itpro/create-a-work-template).

### <a name="work-templates"></a>Arbeidsmaler

Netto innkjøpspris legger til en ny arbeidsordretype med navnet *Varer i transitt* på siden **Arbeidsmaler**. Denne arbeidsordretypen må konfigureres på samme måte som [arbeidsmaler for bestilling](/dynamicsax-2012/appuser-itpro/create-a-work-template).