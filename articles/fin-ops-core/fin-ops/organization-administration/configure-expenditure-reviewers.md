---
title: Konfigurere utgiftskontrollører
description: Denne artikkelen beskriver hvordan du bruker gjennomganger av utgifter til å velge brukeren som en arbeidsflytoppgave, godkjenning eller manuell beslutning er tilordnet, dynamisk.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: 110edf4c2733f899368069c7d215ae5b0882f5cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863230"
---
# <a name="configure-expenditure-reviewers"></a>Konfigurere utgiftskontrollører
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Du kan definere dynamiske utgiftskontrollører for å rute utgifter til gjennomgang basert på brukeren som er tilordnet til en prosjektrolle eller finansdimensjonen der utgiften belastes. Arbeidsflytprosessen bruker den angitte eieren av prosjektrollen eller finansdimensjonen til å avgjøre hvem utgiften skal sendes til.

Du kan definere én eller flere konfigurasjoner for utgiftskontrollør og deretter velge en konfigurasjon når du oppretter en arbeidsflyt. Du kan konfigurere verdiene for utgiftskontrollør for hver juridisk enhet i organisasjonen. Når du har definert konfigurasjonene for utgiftskontrollør, tilordner du konfigurasjonen. Gjennomgang av utgifter kan tilordnes arbeidsflytoppgaver, -godkjenninger og manuelle avgjørelser.

> [!NOTE]
> Selv om utgiftskontrollører ikke er obligatoriske, kan de forenkle konfigurasjonen av arbeidsflyten. Du må for eksempel ikke opprette én betinget beslutning for å se etter hver kostsenterdimensjon, og deretter opprette et nytt element for å tilordne godkjenningen eller oppgaven til en bestemt bruker eller brukergruppe. I stedet kan du konfigurere eieren av kostsenterdimensjonen og bruke en utgiftskontrollører til å velge riktig bruker dynamisk. Når eierskap eller tilordning av kostsentre endres, trenger du da bare oppdatere **Eier**-feltet for finansdimensjonen.

## <a name="types-of-expenditure-reviewers"></a>Typer utgiftskontrollører

Ikke alle arbeidsflyter støtter konseptet med utgiftskontrollører. Som standard kan du konfigurere utgiftskontrollører for innkjøpsrekvisisjoner, bestillinger, leverandørfakturaer og reiseregningsrapporter. Hver av disse arbeidsflyttypene krever at du konfigurerer utgiftskontrollører på en egen side som er spesifikk for funksjonen og modulen. For hvert dokument som støttes, kan utgiftskontrollører brukes med enten arbeidsflyter på overskriftsnivå eller arbeidsflyter på linjenivå.

Tabellen nedenfor viser hvor du går for å konfigurere en utgiftskontrollør for hvert dokument som støttes.

| Dokument | Navigasjonsrute |
|----------|-----------------|
| Reiseregninger | Reiseregning og utlegg \> Oppsett \> Policyer \> Utgiftskontrollører |
| Bestillinger | Innkjøp og leverandører \> Oppsett \> Policyer \> Kontrollører av bestillingsutgifter |
| Innkjøpsrekvisisjoner | Innkjøp og leverandører \> Oppsett \> Policyer \> Kontrollører av innkjøpsrekvisisjonsutgifter |
| Leverandørfakturaer | Leverandører \> Policyoppsett \> Utgiftskontrollører for leverandørfaktura |

## <a name="expenditure-reviewer-assignments"></a>Tilordninger av utgiftskontrollør

To tilordningstyper er tilgjengelige for hver utgiftskontrollør: *prosjektdistribusjoner* og *organisasjonsdistribusjoner*. For en prosjektdistribusjon kan du velge mellom prosjektmyndigheter og finansdimensjoner. For en organisasjonsdistribusjon kan du velge finansdimensjoner.

Prosjektmyndighetene omfatter prosjektleder, prosjektkontroller og prosjektleder. Du definerer disse myndighetene direkte i prosjektet ved å velge en arbeider i de aktuelle feltene.

Finansdimensjoner styres av kontostrukturene i hver juridiske enhet. For hver juridiske enhet kan du velge hvilke finansdimensjoner som skal brukes med utgiftskontrolløren. Dimensjonene kan komme fra enten prosjektet (i dette tilfellet velger du dimensjonene i kategorien **Prosjektdistribusjoner**) eller dokumentet (i dette tilfellet velger du dimensjonene i kategorien **Organisasjonsdistribusjoner**). I **Eier**-feltet på siden **Finansdimensjonsverdier** kan du velge arbeideren for hver finansdimensjon.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Eksempel 1: Utgiftskontrollører basert på organisasjonsdistribusjoner

Du jobber for Contoso Appliances, og organisasjonen har seks avdelinger og 10 kostsentre. Når en ny innkjøpsrekvisisjon sendes, må godkjenningen først komme fra avdelingssjefen og deretter fra kostsentersjefen.

I dette eksemplet konfigurerer du to *kontrollører av innkjøpsrekvisisjonsutgifter*:

- For den første kontrolløren gir du et navn til avdelingen og velger deretter **Avdeling**-finansdimensjonen på fanen **Organisasjonsdistribusjoner**. 
- For den andre kontrolløren gir du et navn til kostsentert og velger deretter **Kostsenter**-finansdimensjonen på fanen **Organisasjonsdistribusjoner**.

Når du konfigurerer arbeidsflyten, oppretter du to godkjenningstrinn. Den første er for avdelingen, og den andre er for kostsenteret. For hvert godkjenningselement velg **Deltaker** i **Tilordningstype**-feltet på fanen **Rollebasert**, velg **Utgiftsdeltakere** i **Type deltaker**-feltet, og velg deretter den riktige deltakeren i **Deltaker**-feltet.

Når innkjøpsrekvisisjonen opprettes, tilordnes finansdimensjonene for avdeling og kostsenter til linjene i innkjøpsrekvisisjonen. Når arbeidsflyten er sendt, evaluerer systemet først avdelingen i innkjøpsrekvisisjonen og tilordner godkjenningselementet til brukeren som er knyttet til arbeideren du valgte for avdelingen. Når det første godkjenningstrinnet er fullført, evaluerer systemet det andre godkjenningstrinnet og tilordner det andre godkjenningselementet til brukeren som er knyttet til arbeideren du valgte for kostsenteret.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Eksempel 2: Utgiftskontrollører basert på prosjektdistribusjoner

Du jobber for serviceavdelingen i Contoso Appliances. Organisasjonen krever at prosjektlederen for hver bestilling må godkjenne utgiften. I tillegg må kostsenterlederen for prosjektet godkjenne det. Godkjenningene kan utføres samtidig. Begge brukerne må i så fall godkjenne bestillingen før arbeidsflyten kan fortsette.

For dette eksemplet oppretter du én *kontrollør av bestillingsutgifter* med navnet **PL og kostsenter**. Du merker av for **Prosjektleder** og angir **Kostsenterdimensjon** til **Ja** på fanen **Prosjektdistribusjoner** på siden **Kontrollør av bestillingsutgifter**. Som en del av konfigurasjonen må du sørge for at **Prosjektleder**-feltet er definert for alle prosjekter, og at en eier angis for alle kostsentre på **Finansdimensjonsverdier**-siden.

Når du konfigurerer arbeidsflyten, må du godkenne ett element. Du velger **Deltaker** i **Tilordningstype**-feltet. På fanen **Rollebasert** velger du deretter **Utgiftsdeltakere** i **Type deltaker**-feltet, og velger prosjektlederen og kostsenteret i **Deltaker**-feltet. Hvis du vil sikre at arbeidsflyten ikke kan fortsette før både prosjektlederen og kostsentereieren godkjenner arbeidsflyten, angir du **Fullføringspolicy**-feltet til **Alle godkjennere**.

Når bestillingen er opprettet, må **Prosjekt**-feltet angis. Hvis du ikke krever et prosjekt for alle bestillingene, bør du legge til en betinget beslutning i arbeidsflyten for å se etter et prosjekt før godkjenningstrinnet kjøres. Systemet evaluerer deretter prosjektet som er angitt for bestillingen, og tilordner godkjenningselementet til brukeren som er knyttet til arbeideren i **Prosjektleder**-feltet. I tillegg oppretter systemet en oppgave og tilordner den til brukeren som er knyttet til arbeideren du velger i **Eier**-feltet for kostsenteret fra prosjektet. Legg merke til at dette eksemplet bruker kostsenteret for prosjektet, ikke kostsenteret for bestillingen.

## <a name="set-up-expenditure-reviewers"></a>Definere utgiftskontrollører

Dette eksemplet viser hvordan du konfigurerer en kontrollør av innkjøpsrekvisisjonsutgifter: Hvis du vil konfigurere andre typer utgiftskontrollører, erstatter du navigasjonsbanen i trinn 1 med den riktige banen fra tabellen i delen [Typer utgiftskontrollører](configure-expenditure-reviewers.md#types-of-expenditure-reviewers), tidligere i denne artikkelen.

1. Gå til **Innkjøp og leverandører \> Oppsett \> Policyer \> Kontrollører av innkjøpsrekvisisjonsutgifter**.
2. På siden **Kontrollører av innkjøpsrekvisisjonsutgifter** velger du **Ny**.
3. I **Navn**-feltet angir du et navn for konfigurasjonen for utgiftskontrollør, for eksempel **kostsenter**.
4. Velg den juridiske enheten du vil konfigurere, i hurtigfanen **Utgiftskontrollører etter juridisk enhet**.
5. For en prosjektdistribusjon merker du av for hver prosjektmyndighet, og velger **Ja** for hver finansdimensjon du vil aktivere. 
6. For en organisasjonsdistribusjon velger du **Ja** på fanen **Organisasjonsdistribusjoner** for hver finansdimensjon du vil aktivere.
7. Gjenta trinn 4 til og med 6 for hver ekstra juridiske enhet.

## <a name="assign-owners-to-financial-dimensions"></a>Tilordne eiere til finansdimensjoner

Hvis du vil tilordne en eier til en finansdimensjon, gjør du følgende.

1. Gå til **Økonomimodul \> Kontoplan \> Dimensjoner \> Finansdimensjoner**.
2. I listen velger du finansdimensjonen du vil tilordne eiere til.
3. Velg **Dimensjonsverdier**.
4. Velg **Rediger** for å gjøre endringer i dimensjonsverdiene.
5. I listen velger du dimensjonsverdien du vil tilordne en eier til.
6. I **Eier**-feltet velger du arbeideren du vil tilordne dimensjonsverdien til.

## <a name="configure-project-distributions"></a>Konfigurere prosjektdistribusjoner

Gjør følgende for å tilordne prosjektmyndigheter til et prosjekt.

1. Gå til **Prosjektstyring og regnskap \> Prosjekter \> Alle prosjekter**.
2. Velg prosjektet som myndighetene skal tilordnes.
3. Velg **Rediger** for å gjøre endringer i prosjektet.
4. I hurtigfanen **Generelt**, i **Ansvarlig**-delen, velger du en arbeider for **Salgssjef**, **Prosjektleder** og **Prosjektkontroller** etter behov.
5. I hurtigfanen **Finansdimensjoner** velger du de nødvendige finansdimensjonene for prosjektet.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Tilordne utgiftskontrollører til en arbeidsflytoppgave

Dette eksemplet viser hvordan du konfigurerer en arbeidsflyt for innkjøpsrekvisisjon slik at den bruker en kontrollør av innkjøpsrekvisisjonsutgifter. Hvis du vil konfigurere andre typer arbeidsflyter, kan arbeidsflytsiden du må åpne i trinn 1, være i modulen **Reiseregning og utlegg** eller **Leverandør**-modulen i stedet for modulen **Innkjøp og leverandører**.

Hvis du vil tilordne kontrollører av innkjøpsrekvisisjonsutgifter til en arbeidsflytoppgave, følger du trinnene nedenfor.

1. Gå til **Innkjøp og leverandører \> Oppsett \> Arbeidsflyter for innkjøp og leverandører**.
2. Dobbeltklikk en eksisterende arbeidsflyt eller opprett en ny arbeidsflyt.
3. Velg oppgaven du vil tilordne konfigurasjon for utgiftskontrollør til, i **Arbeidsflyt**-ruten i arbeidsflytredigeringsprogrammet. I **handlingsruten** i **Vis**-gruppen velger du deretter **Egenskaper**.
4. I venstre rute på **Egenskaper**-siden velger du **Tilordning**.
5. Velg **Deltaker** i kategorien **Tilordningstype**.
6. På fanen **Rollebasert** i **Type deltaker**-feltet velger du **Utgiftsdeltakere**. I **Deltaker**-feltet velger du deretter konfigurasjonen for utgiftskontrollør du vil bruke for arbeidsflytoppgaven.
