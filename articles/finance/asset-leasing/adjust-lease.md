---
title: Justere leieavtaler
description: Emnet beskriver hvordan du justerer en leieavtale. Det kan hende at justering kreves hvis leievilkårene endres, leieavtalen utvides eller andre omstendigheter endres.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1016b69fd59bbe90924996f5c931cb5d0f779253de66f5f3821a8c3001d3313b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729660"
---
# <a name="adjust-leases"></a>Justere leieavtaler

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Emnet beskriver hvordan du justerer en leieavtale. Det kan hende at justering kreves hvis leievilkårene endres, leieavtalen utvides eller andre omstendigheter endres. Aktivaleie følger retningslinjene som Accounting Standards Codification-emne 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16) gir om leieavtaleendringer. ASC 842-20-15-1 definerer en leieavtaleendring som enhver endring i vilkårene og betingelsene for en kontrakt som forårsaker endring i omfanget av, eller betalingen for, en leieavtale. Avsnitt 39 i IFRS 16 angir at en leier må revaluere leieforpliktelsen, slik at den gjenspeiler endringer i leiebetalingene.

Når det gjelder organisasjoner som følger ASC 842 eller IFRS 16, måles en leieavtale på nytt for å gjenspeile en endring i den gjeldende verdien til de fremtidige minimumsleiebetalingene (PVFMLP). Hvis PVFMLP øker, blir journaloppføringen som opprettes, en debitering for aktivakontoen for bruksrettseiendelen og en kreditering for leieforpliktelsskontoen for differansen mellom den nye PVFMLP og den forrige PVFMLP. Hvis PVFMLP reduseres, vil journaloppføringen være en debitering for leieforpliktelseskontoen og en kreditering for bruksrettseiendelskontoen for differansen.

Hvis justeringen reduserer bruksrettseiendelen forbi 0 (null), blir resten kreditert fortjenesten på posteringskontoen for leieavtaleendringer som er angitt på siden **Posteringskontoer for leieavtale**. Systemet gjør rede for disse transaksjonene og andre justeringsoppføringer, for eksempel klassifiseringsendringer, opprinnelige direkte kostnader, leieinsentiver, forskuddsbetalinger og avviklingskostnader som oppstår fra leieavtaleendringer.

Hvis du vil ha spesifikk veiledning om leiejusteringstransaksjoner, anbefaler vi at du ser på IFRS 16 og ASC 842.

## <a name="lease-adjustment-wizard"></a>Leiejusteringsveiviser

For å justere en leieavtale fullfør fremgangsmåten nedenfor. De endrede dataene oppdaterer leieplaner etter at du har postert fra veiviseren for **Leiejustering**. Du kan lagre arbeidet og lukke veiviseren når som helst, og deretter gå tilbake senere for å gjenoppta arbeidet ditt.

Følg denne fremgangsmåten for å åpne veiviseren for **Leiejustering** fra leiesammendraget.

1. Gå til **Aktivaleie \> Leieavtaler \> Leiesammendrag**. 
2. Velg leieperioden som skal justeres, og velg deretter **Justeringsveiviser**.
3. Følg instruksjonene i veiviseren for å angi de nødvendige endringene.

Følg denne fremgangsmåten for å åpne veiviseren for **Leiejustering** fra siden **Leiejusteringer** for en justering som allerede pågår.

1.  Gå til **Leie \> Leieavtaler \> Leiejusteringer**.
2.  Velg en leieavtale med justeringsstatusen **Pågår**, og velg deretter **Justeringsveiviser**.
3.  Angi passende datoer i feltene **Startdato for endring** og **Posteringsdato**.
4.  Velg **Neste**.

    Leieavtalen legges nå til på siden for **Leiejusteringer**, der du kan angi ny informasjon om den.

    Når leieperioden er justert, gjelder feltene for bruksretthensyn. Hvis ingen opprinnelige direkte kostnader, leieinsentiver, forskuddsbetalinger eller avviklingskostnader er knyttet til den endrede leieavtalen, lar du de tilsvarende feltene stå tomme. De opprinnelige beløpene gjelder ikke for den oppdaterte leieavtalen. 

    En utleier gir for eksempel et insentiv på USD 1 000 for å godta en forlengelse av leieavtalen. I dette tilfellet angir du **1 000** i feltet **Leieinsentiver som oppstår fra justeringer** når du justerer leieavtalen for å gjøre rede for forlengelsen.

    Betalingsplanlinjene viser nå alle betalinger fra måneden og senere måneder, i feltet **Startdato for endring**. Fordi endringer er potensielle, kan ikke betalingsplanlinjer starte før endringen starter. Hvis du vil vise betalingsplanlinjer fra før startdatoen for endring, kan du gå til siden **Historikk for leieavtaleversjon**.

8.  Velg **Neste**.

    Den neste siden viser nøkkeldetaljer om den forventede leiejusteringen, for eksempel bærende verdier av leieforpliktelsen før endringen, og den nye forventede utleieplikten etter endringen. Siden viser også en forhåndsvisning av journaloppføringen for forventet leiejustering.

9.  Merk av for **Send til arbeidsflyt** for å sende leiejusteringen til arbeidsflytsystemet hvis arbeidsflyten for leiejusteringen er aktiv og justeringen ennå ikke er godkjent. Hvis du vil ha mer informasjon om hvordan du bruker arbeidsflyten for leiejustering, kan du se [Bruke arbeidsflyter for leieavtaler](use-create-lease-wrkflw.md).

    > [!NOTE]
    > På dette tidspunktet omberegner systemet justeringsvariablene for å kontrollere at det ikke er postert noen transaksjoner mot leieavtalen siden justeringsoversikten og justeringsjournaloppføringen først ble beregnet. Hvis noen verdier endres, oppdateres rutenettet for justeringsoversikten, og du kan se gjennom informasjonen før du sender leiejusteringer til arbeidsflytsystemet på nytt.

10. Hvis en arbeidsflyt ikke er aktiv, eller hvis leiejusteringen er godkjent, velger du **Fullfør** for å behandle endringene og postere justeringsjournaloppføringen.

    > [!NOTE] 
    > På dette tidspunktet omberegner systemet justeringsvariablene for å kontrollere at det ikke er postert noen transaksjoner mot leieavtalen siden justeringsoversikten og justeringsjournaloppføringen først ble beregnet. Hvis noen verdier endres, oppdateres rutenettet for justeringsoversikt, og du kan gå gjennom endringene før du velger **Fullfør**. Hvis arbeidsflyten er aktiv og leiejusteringen er godkjent, vil eventuelle endringer i justeringsoversikten føre til at godkjenningsstatusen settes til **Ikke sendt**. I dette tilfellet bør du sende leiejusteringen til arbeidsflytsystemet på nytt.

    På siden **Leiejustering** er justeringsstatusen nå satt til **Fullført**.

    På siden **Leiejusteringer** kan du fremdeles se hurtigfanene **Justeringsoversikt** og **Forhåndsvisning av justeringsoppføring**. Leiedetaljene og datoinformasjonen vises i versjonshistorikken for leieavtalen.

    Nå opprettes det en ny leieversjon og et nytt sett med planer med den endrede informasjonen. 

13. Hvis du vil vise de nye planene, kan du gå til leieperioden og deretter velge **Bøker**.
14. Hvis du vil vise den nygenererte betalingsplanen, velger du **Betalingsplan**.
15. Hvis du vil vise den nye nedbetalingsplanen for leieforpliktelse som genereres fra den nye informasjonen, lukker du **Betalingsplan**-siden og åpner siden **Nedbetalingsplan for gjeld**.
16. Hvis du vil vise den nylig genererte avskrivningsplanen for aktiva, åpner du siden **Avskrivningsplan for aktiva** fra siden **Tablådetaljer**.
17. Du viser justeringsjournaloppføringen ved å velge **Journaler \> Journal for aktivaleie**.

## <a name="cancel-a-lease-adjustment"></a>Avbryte en leiejustering

Følg denne fremgangsmåten for å slette en leiejustering som pågår.

1.  Gå til **Leie \> Leieavtaler \> Leiejusteringer**.
2.  Velg den pågående leiejusteringen du vil annullere.
3.  Velg **Avbryt justering**. 
4.  Velg **OK**.

    > [!NOTE] 
    > Hvis du velger **Avbryt** i veiviseren for **Leiejustering**, tilbakerullerer du den siste endringen du fullførte i veiviseren, men du fjerner ikke en justering som pågår.

## <a name="use-the-lease-adjustment-workflow"></a>Bruke arbeidsflyten for leiejustering

Denne delen forklarer hvordan du bruker arbeidsflyten for leiejustering. Med arbeidsflyten for leiejustering kan du administrere leiejusteringer på en konsekvent måte ved å angi et sett med godkjenningstrinn og tilordne dem til bestemte brukere som godkjenner en leiejustering før den blir endelig. Når leiejusteringen er godkjent i arbeidsflyten, kan du bruke veiviseren for leiejustering til fullføre **Leiejusteringen**.

1.  Hvis du vil sende en leiejustering til godkjenning, kan du gå til **Leie \> Leieavtaler \> Leiejusteringer**.
2.  Velg leie-ID-en for leiejusteringen, velg deretter **Justeringsveiviser**.
3.  På den siste siden i veiviseren velger du **Send til godkjenning**.
4.  Angi en kommentar om justeringen, og velg deretter **OK**.

    Arbeidsflytstatusen endres til **Ventende godkjenning**, og alle feltene i veiviseren er låst for redigering.

5.  Hvis du vil godkjenne leiejustering, kan du gå til **Leie \> Leieavtaler \> Leiejusteringer**.
6.  Velg leie-ID-en for leiejusteringen, og se gjennom hurtigfanene **Justeringsoversikt** og **Forhåndsvisning av justeringsoppføring**.
7.  Velg **Arbeidsflyt \> Godkjent**.

    På siden **Leiejustering** er arbeidsflytstatusen nå satt til **Godkjent**. På dette tidspunktet er leiejusteringen klar til å posteres via justeringsjournaloppføringen.

8.  Hvis du vil fortsette å behandle leiejusteringen og postere justeringsoppføringen, kan du gå til **Leie \> Leieavtaler \> Leiejusteringer**.
9.  Velg leie-ID-en for leiejusteringen, velg deretter **Justeringsveiviser**.
10. Velg **Neste** til du kommer til den siste siden i veiviseren, og velg deretter **Fullfør**.

Systemet omberegner de bærende verdiene av leieperioden for å sikre at justeringsvariablene som ble godkjent, er gjeldende. Hvis det er noen endringer, settes godkjenningsstatusen tilbake til **Utkast**, og du bør sende leiejusteringen til arbeidsflytsystemet på nytt.

## <a name="view-lease-versions"></a>Vise leieavtaleversjoner

Hvis en leieavtale er justert, kan du vise de ulike versjonene av den. Du kan også vise de historiske tidsplanene og tidligere leieavtaledetaljer.

1. På siden **Leiesammendrag** velger du leieavtalen, og deretter velger du **Historikk for leieavtaleversjon** i handlingsruten.

    Hvis den valgte leieavtalen er justert, viser siden **Historikk for leieavtaleversjon** de ulike versjonene. Den opprinnelige leieavtalen er merket med **1**, og påfølgende versjoner er i stigende numerisk rekkefølge.

    For en valgt leieavtaleversjon kan du vise finansdimensjoner, kontraktdetaljer, sted og betalingsplanlinjer.

2. Hvis du vil vise historiske tidsplaner, åpner du den endrede leieavtalen fra siden **Leiesammendrag**, velger det ønskede tablået og deretter **Historikk for tablåversjon** i handlingsruten.
3. På **Tablåversjon**-siden velger du en versjon og en tidsplan du vil vise.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]