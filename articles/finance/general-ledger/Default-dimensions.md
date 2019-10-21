---
title: Finansdimensjoner og postering
description: Når du planlegger og definerer kontoplanen, må du vurdere hvordan de ulike komponentene fungerer sammen når du posterer et dokument eller en journal. Disse komponentene inkluderer kontostrukturer, avanserte regler og belastningsfordeling og faste dimensjoner. Dette emnet beskriver hva hver enkelt komponent er og hvordan komponentene fungerer sammen.
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 76fd305ce0f0f073648339d1de969981693f1da5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186814"
---
# <a name="financial-dimensions-and-posting"></a>Finansdimensjoner og postering 

[!include [banner](../includes/banner.md)]

Når du planlegger og definerer kontoplanen, må du vurdere hvordan de ulike komponentene fungerer sammen når du posterer et dokument eller en journal. Disse komponentene inkluderer kontostrukturer, avanserte regler og belastningsfordeling og faste dimensjoner. Dette emnet beskriver hva hver enkelt komponent er og hvordan komponentene fungerer sammen.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Kontoplaner og finansdimensjonskomponenter

Et omfattende regelbasert system brukes til å definere gyldige kombinasjoner av hovedkontoer og finansdimensjonsverdier. Denne delen gir en kort oversikt over funksjonaliteten for hver komponent, og forklarer hvor du kan finne komponenten.

### <a name="account-structures"></a>Kontostrukturer

Det kreves en kontostruktur når du definerer i finans. Du må definere og aktivere minst én kontostruktur, og du må tilordne den til finans. Kontostrukturen må inneholde hovedkontoen. Du kan definere rekkefølgen på segmenter som passer best for bedriften. Når hovedkontoen er definert, kan systemet bestemme kontostrukturen som brukes. Ved å sette inn hovedkontoen først eller nær begynnelsen av en struktur, kan du bidra til begrense verdiene og også bidra til at systemet bruker den siste kjente gyldige verdien som en standardverdi. Du kan ha opptil 10 ekstra finansdimensjoner i kontostrukturen. Kontostrukturen definerer hvilke dimensjonsverdier som er gyldige i kombinasjon med andre verdier. Den definerer også om dimensjonsverdier må angis.

### <a name="advanced-rules"></a>Avanserte regler

Avanserte regler er en valgfri komponent når du setter opp kontoplanen. Du kan legge til så mange avanserte regler som du vil i en kontostruktur. Avanserte regler brukes ofte til å håndtere scenarier der flere finansdimensjoner må spores når bestemte kriterier er oppfylt. Hvis du for eksempel bruker en utgiftskonto for reise, kan det hende at du vil spore tilleggsinformasjon, for eksempel hendelsen knyttet til den ansattes reise. Hvis det finnes flere avanserte regler, brukes de i alfabetisk rekkefølge, basert på navnene på reglene. Segmentene som legger til en regel, kan bare brukes etter segmentene i kontostrukturen.

### <a name="balancing-dimension"></a>Saldofinansdimensjon

Du kan også definere en saldofinansdimensjonen. På **Finans**-siden kan du definere hvilken finansdimensjon som skal balanseres. Deretter, når transaksjoner posteres til den finansdimensjonen, vil systemet automatisk opprette og legge inn oppføringer for å balansere finansdimensjonen.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Standard/faste finansdimensjoner for hovedkontoen

Standarddimensjoner kommer fra ulike steder, for eksempel hovedposter (kunde- eller leverandørposter), dokumenthoder og hovedkontoen. Dette emnet beskriver standarddimensjoner på hovedkontoen etter juridisk enhet. Du kan definere om en hovedkonto har en **Ikke fast** eller **Fast** verdi for hver finansdimensjon som brukes på tvers av alle kontostrukturer for finans. Hvis en finansdimensjon er **Ikke fast**, brukes en standardverdi, men denne verdien kan overskrives. Dette gjelder for alle standardverdier i systemet, også standardverdier som kommer fra hovedposter. Hvis en finansdimensjon er satt til en **Fast** verdi, brukes alltid denne verdien, uansett om den kom fra et sted som en standardverdi eller brukeren registrerte den.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Rekkefølgen som dimensjoner brukes i ved postering

Folk har ofte spørsmål om rekkefølgen de forskjellige komponentene kjører i. Det er svært viktig at du forstår rekkefølgen som standarddimensjoner brukes i, siden dette påvirker tilnærmingen din til oppsettet.

> [!NOTE]
> Denne informasjonen gjelder bare for bruk av standarddimensjoner i programmet. Hvis du importerer data ved hjelp av Microsoft Excel eller Data Management Framework, er virkemåten forskjellig.

### <a name="example-1"></a>Eksempel 1

**Kontostruktur**

| Hovedkonto            | Forretningsenhet           | Avdeling              | Kostsenter             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Alle verdier er tillatt. | Alle verdier er tillatt. | Alle verdier er tillatt. | Alle verdier er tillatt. |

**Hovedkonto**

| Hovedkonto | Navn          | Juridisk enhet | Avdeling                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Produktsalg | USMF         | Fast – 022 Salgs- og markedsføringsavdeling |

Illustrasjonen nedenfor viser den faste standarddimensjonen som er angitt for hovedkontoen 401100.

[![Standard finansdimensjoner](./media/default-dimensions.png)](./media/default-dimensions.png)

I dette svært enkle eksemplet skal vi registrere en økonomijournal der avdelingsdimensjonen er satt til å bruke standardverdien **023** (Operasjoner). Vi vil registrere og postere en finanskonto. Illustrasjonen nedenfor viser standard finansdimensjonen i økonomimodulhodet.

[![Økonomijournaler](./media/general-journal.png)](./media/general-journal.png)

Standarddimensjonen i journalhodet fører til at avdeling 023 brukes som standard på salgskontolinjen. Illustrasjonen nedenfor viser den økonomijournallinjen, der standarddimensjonsverdien **023** fra hodet brukes.

[![Journalbilag](./media/journal-voucher.png)](./media/journal-voucher.png)

Når linjen posteres, brukes imidlertid den faste dimensjonen, og linjen posteres til avdeling 022. Illustrasjonen nedenfor viser det posterte bilaget, der den faste dimensjonen brukes for salgskontoen.

[![Bilagstransaksjoner](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Eksempel 2

Dette eksemplet bruker samme oppsett som det første eksemplet. Vi vil imidlertid legge til en annen komponent og bruke avdelingsdimensjonen som balansedimensjon. I illustrasjonen nedenfor er **Avdeling** angitt som den balanserende finansdimensjonen for USMF-finans.

[![Finans](./media/ledger.png)](./media/ledger.png)

Når det samme journalhodeoppsettet brukes, og den samme transaksjonen posteres, brukes den faste dimensjonen først. Balanseringslogikken brukes deretter for å garantere at hver avdeling har en balansert oppføring. Illustrasjonen nedenfor viser bilagstransaksjonene som inkluderer balanseoppføringen etter at den faste dimensjonen er brukt.

[![Bilagstransaksjoner](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Eksempel 3

I dette eksemplet skal vi legge til en avansert regel. Den avanserte regelen angir at hvis salgskonto 401100 og avdeling 022 (salg og markedsføring) brukes, skal systemet spore et ekstra segment kalt kunde.

Dette eksemplet er viktig på grunn av rekkefølgen. Kontostrukturen bestemmes når hovedkontoen er angitt. Hvis du refererer til kontostrukturoppsettet, kan systemet fastslå at hovedkontoen, forretningsenheten, avdelingen og kostsenteret er relevante. Den avanserte regelen er ennå ikke utløst fordi faste dimensjoner ikke brukes før standarddimensjoner er brukt for journalbilaget under postering. I illustrasjonen nedenfor vies ikke kundesegmentet fordi kriteriene for den avanserte regelen ikke er oppfylt.

[![Finanskonto](./media/drop-down.png)](./media/drop-down.png)

Posteringen vil ikke lykkes fordi den faste dimensjonen ble brukt på slutten av prosessen. Dimensjonsvalidering bestemmer at kundesegmentet er nødvendig hvis hovedkontoen er 401100 og avdelingen 022. Postering kan ikke skje på grunn av valideringsfeilen. Illustrasjonen nedenfor viser meldingen som vises når dimensjonsvalidering angir at kunde er et nødvendig segment.

[![Meldingsdetaljer](./media/message.png)](./media/message.png)

I dette eksemplet må du overskrive standardverdien slik at den avanserte regelen utløses og du kan angi kundesegmentet. Denne løsningen er imidlertid ikke alltid mulig, og noen brukere er ikke en gang klar over posteringsreglene. Det er derfor viktig at du forstår rekkefølgen som standarddimensjoner brukes i når du setter opp kontoplanen.

For å oppnå det du vil i dette eksemplet, kan du endre konfigurasjonen på flere måter. Du kan for eksempel opprette en ny kontostruktur for salgskontoer og inkludere kundesegment i strukturen. Du kan også legge til flere rader i en eksisterende kontostruktur, og angi hovedkontoen og gyldige avdelingsverdier. Deretter, i den ekstra kundestrukturen, kan det være nyttig å ha en egen kontostruktur for salgskontoer der kundesegmentet er til stede.

## <a name="additional-resources"></a>Tilleggsressurser 

Noen av følgende ressurser refererer til en tidligere versjon av programvaren. Mye av informasjonen om bruken av standarddimensjoner og mange av begrepene er imidlertid de samme i den tidligere versjonen, og referansene er fremdeles gyldige.

[Balanserte journaler for interenhetsregnskap](example-balanced-journals-interunit-accounting.md)

[Planlegge kontoplanen](plan-chart-of-accounts.md) 

[Planlegging av kontoplanen i AX 2012 (blogg)](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – Denne koblingen går til del 1 av en serie på sju deler.

[Dimensjonen som fører til regnskapsdistribusjoner](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Dimensjonen som fører til dimensjonsrammeverk](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2014/09/)
