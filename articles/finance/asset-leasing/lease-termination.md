---
title: Forslag til leieavslutning
description: Dette emnet beskriver hvordan du foreslår oppsigelse av leie.
author: moaamer
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e303821bd41751cb0a07442613b8b20e8061b052
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819872"
---
# <a name="propose-a-lease-for-termination"></a>Foreslå oppsigelse av leie

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Hvis en leieavtale avsluttes tidlig, kan aktivaleie registrere en oppsigelsesjournaloppføring for å skrive av leieforpliktelsen, aktiva for bruksrettighet og akkumulert avskrivning, og bokføre gevinst eller tap. Prosessen med tidlig avslutning avslutter en leieavtale og de tilhørende leietablåene. Den stopper ikke enkeltstående leietablåer. Dette emnet beskriver funksjonaliteten som lar deg foreslå en leieavtale for oppsigelse og behandle journaloppføringen for oppsigelse av leie.

Hvis en leieavtale ikke klassifiseres som en utsatt leie, og tilknytning til et anleggsmiddel ikke finnes, produserer Aktivaleie følgende oppsigelsesjournaloppføring.

| Transaksjon                           | Debet (Dr.) | Kredit (Kred.) |
|---------------------------------------|-------------|--------------|
| Dr. Leieforpliktelse                   | X           |              |
| Dr. akkumulert avskrivning          | X           |              |
| Deb. Fortjeneste (tap) ved endring av leie | X           |              |
| Kred. Leieaktivum                       |             | X            |
| Kred. Fortjeneste (tap) ved endring av leie |             | X            |

Hvis leietablået klassifiseres som tablå for utsatt leie, skriver oppføringen av saldoen for utsatt leie før oppsigelsen til gevinst- eller tapskontoen, som vist her.

| Transaksjon                           | Debet (Dr.) | Kredit (Kred.) | 
|---------------------------------------|-------------|--------------|
| Dr. Utsatt leie                     | X           |              |
| Kred. Fortjeneste (tap) ved endring av leie |             | X            |
| Kred. Utsatt leie                     |             | X            |
| Deb. Fortjeneste (tap) ved endring av leie | X           |              |

Hvis leietablået er knyttet til et anleggsmiddel, glir bruksrettseiendel gjort rede for i Anleggsmidler. Dette regnskapet omfatter regnskapet for tidlige oppsigelser. Aktivaleie produserer følgende journaloppføring for å skrive av leieforpliktelse.

| Transaksjon                           | Debet (Dr.) | Kredit (Kred.) |
|---------------------------------------|-------------|--------------|
| Dr. Leieforpliktelse                   | X           |              |
| Kred. Fortjeneste (tap) ved endring av leie |             | X            |

Hvis du vil ha informasjon om riktig måte å avhende en bruksrettseiendel på, kan du se [Fjerne et anleggsmiddel som svinn](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Foreslå oppsigelse av leie

1. Gå til leieavtalen som må avsluttes, og velg deretter **Oppsigelsesforslag** i handlingsruten.

    > [!NOTE]
    > Knappen **Oppsigelsesforslag** er ikke tilgjengelig hvis det finnes uposterte journaloppføringer mot noen tablåer. Før du kan avslutte leieavtalen, må du postere eller slette eventuelle journaloppføringer som er opprettet mot leieavtalen.

2. I dialogboksen som vises, angir du feltene **Gyldighetsdato** og **Posteringsdato** for oppsigelsesjournaloppføringen.
3. Velg **Oppsigelsesforslag** for å foreslå leieoppsigelsen.
4. Velg **Poster leieoppsigelse** for å postere journaloppføringen for leieoppsigelse automatisk.
5. Velg leie-IDen for leieavtalen du foreslår for oppsigelse, på siden **Leieoppsigelser**, for å vise oppsigelseslinjene. Oppsigelseslinjene viser bærende verdier for bruksrettseiendel, leieforpliktelse, akkumulert avskrivning, utsatt leie (hvis aktuelt) og gevinst eller tap som må anerkjennes ved avslutning av leieavtalen.

Leieavtalen er nå klar til oppsigelse. Verdien til **Oppsigelsesstatus**-feltet for leietablået endres til **Klar til oppsigelse**. På dette tidspunktet kan du ikke lenger postere journaloppføringer mot leieavtalen eller justere eller verdiforringe den. 

## <a name="process-leases-that-are-ready-for-termination"></a>Behandle leieavtaler som er klare til oppsigelse

Følg denne fremgangsmåten for å behandle leie som er klar til oppsigelse, og poster journaloppføringen for oppsigelsen.

1. På siden **Leieoppsigelser** velger du leieavtalen du vil behandle, og deretter velger du **Avslutt**.
2. I dialogboksen som vises, velger du **OK**.

Systemet posterer journaloppføringen for oppsigelse. Feltet **Leiestatus** for leietablået er satt til **Avsluttet**, og feltet **Status for oppsigelsesforslag** er satt til **Fullført**.

## <a name="reverse-a-lease-termination"></a>Tilbakeføre en leieoppsigelse

Følg dette trinnet for å tilbakeføre en journaloppføring for oppsigelse og åpne en avsluttet leie.

- På siden **Leieoppsigelser** velger du den avsluttede leieavtalen som skal tilbakeføres, og deretter velger du **Tilbakefør oppsigelse**.

Systemet reverserer journaloppføringen for oppsigelse. Feltet **Leiestatus** for leietablåët er satt til **Åpen**. Leieavtalen vises ikke lenger på siden **Leieoppsigelser** og kan foreslås på nytt for oppsigelse.

## <a name="example-of-a-lease-termination"></a>Eksempel på oppsigelse av leie

I dette eksemplet er leieavtalen tilknyttet et ikke-spesialisert aktiva og overfører ikke eierskap for aktivaet eller gir leier muligheten til å kjøpe aktivaet.

### <a name="setup"></a>Installasjon

Tabellene nedenfor viser verdiene som er angitt i fanene **Generelt** og **Linjer i betalingsplan** for leieavtalen som brukes i dette eksemplet.

**Fanen Generelt**

| Felt                      | Verdi            |
|----------------------------|------------------|
| Aktivaets gjennomsnittsverdi    | 600,000          |
| Valuta.                   | USD              |
| Opprinnelige direkte kostnader       | 1 000            |
| Trinnvis lånerente | 7 %               |
| Sammensetningsintervall       | Årlig         |
| Aktivalevetid (måneder) | 600              |
| Annuitetstype               | Vanlig annuitet |
| Iverksettelsesdato          | 1/1/2019         |

**Fanen Linjer i betalingsplan**

| Felt             | Verdi      |
|-------------------|------------|
| Startdato        | 1/1/2019   |
| Periodeintervall   | Månedlig    |
| Perioder           | 120        |
| Sluttdato          | 12/31/2028 |
| Betalingsfrekvens | Årlig   |
| Betalingsbeløp    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Trinn for å avslutte leieavtalen

1. Når du har opprettet en leieavtale som beskrevet tidligere i dette emnet, går du til leietablået og bekrefter betalingsplanen. Poster deretter journaloppføringen for opprinnelig føring. Det første bruksrettseiendelen er USD 71 235,81, og leieforpliktelsen skal være USD 70 235,81. I dette eksemplet ble leieavtalen klassifisert som en gjeldende leie under ASC-emne 842 (Accounting Standards Codification).
2. Kjør prosessen for satsvis journal tre ganger for å simulere at det er gått tre år for leiebetalingene, renteutgiftene og avskrivningsutgiftene.
3. Når du er ferdig med å kjøre alle tre kjørslene, går du tilbake til leietablået og åpner tabellene for Gjeld- og Aktiva-transaksjoner for å vise gjeldende bokførte verdi for bruksrettseiendel og leieforpliktelse. Etter tre år skal avstandsverdien være omtrent $53.893,00, og verdien for aktivaet skal være ca. $54.593,00.

    Etter at de tre årene er gått, blir forretningsenheten og utleieren gjensidig enige om å avslutte leieavtalen. Derfor må du nå avslutte leieavtalen.

4. Gå til leieavtalen som må avsluttes, og velg deretter **Oppsigelsesforslag** i handlingsruten. 
5. I dialogboksen som vises, angir du **1/1/2021** i feltet **Gyldighetsdato** og **Posteringsdato**.
6. Velg **Oppsigelsesforslag** for å foreslå leieoppsigelsen.

    Siden **Leieoppsigelser** vises, og viser leieavtalen som vil bli avsluttet.

7. For å vise oppsigelseslinjene velger du leie-IDen for leieavtalen du foreslo for oppsigelse. Oppsigelseslinjene viser bærende verdier for leieavtalen. Følgende tabell viser hva disse verdiene bør være for dette eksemplet. 

    | Felt                                                 | Verdi      |
    |-------------------------------------------------------|------------|
    | Overføre saldo for gjeld i transaksjonsvaluta | USD 53 892,89 |
    | Bruksrettseiendel i transaksjonsvaluta            | USD 71 235,81 |
    | Akkumulert avskrivning i transaksjonsvaluta      | USD 16 642,92 |
    | Gevinst (tap) i transaksjonsvaluta                   | USD-700,00   |

8. For å postere journaloppføringen for oppsigelse, velger du leieavtalen på siden **Leieoppsigelser**, og deretter velger du **Avslutt**.
9. I dialogboksen som vises, velger du **OK**.
10. Hvis du vil vise avslutningsjournaloppføringen som er opprettet og postert, kan du gå til leietablået for aktivaet i leieboken. Følgende tabell viser hva denne oppføringen skal se ut som for dette eksemplet.

    | Transaksjon                           | Debet (Dr.) | Kredit (Kred.) |
    |---------------------------------------|-------------|--------------|
    | Dr. Leieforpliktelse                   | 53,892.89   |              |
    | Dr. akkumulert avskrivning          | 16,642.92   |              |
    | Deb. Fortjeneste (tap) ved endring av leie | 700.00      |              |
    | Kred. Leieaktivum                       |             | 71,235.81    |

11. Hvis du vil se nettoeffekten av oppsigelsen, der bruksrettseiendelen og leieforpliktelsen er 0 (null), åpner du tabellene Gjeld- og Aktiva-transaksjoner.

Leiestatusen skal nå være **Avsluttet**. Ingen flere journaloppføringer blir postert mot denne leieavtalen med mindre oppsigelsen tilbakeføres.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]