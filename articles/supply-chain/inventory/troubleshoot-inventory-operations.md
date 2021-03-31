---
title: Feilsøke lageroperasjoner
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med lageroperasjoner.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: ee1bfbf1b5aa736e1ee5bd38403b6c94c2bd036b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225008"
---
# <a name="troubleshoot-inventory-operations"></a>Feilsøke lageroperasjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med lageroperasjoner.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Jeg finner ikke rullegardinboksen Arbeidsflyt for lagerjournaler.

### <a name="issue-description"></a>Problembeskrivelse

Du finner ikke rullegardinboksen **Arbeidsflyt** på journalsiden, eller relaterte arbeidsflytoperasjoner er ikke tilgjengelige.

Dette problemet kan oppstå av tre årsaker, som beskrevet i underdelene nedenfor.

### <a name="issue-resolution-1"></a>Problemløsning 1

Hvis problemet gjelder alle brukere, kan årsaken være at godkjenningsarbeidsflyten ikke er tilordnet til journalnavnet. Følg fremgangsmåten nedenfor for å løse problemet.

1. Gå til **Lagerstyring &gt; Oppsett &gt; Journalnavn &gt; Beholdning**.
1. I listeruten velger du et journalnavn for å åpne innstillingene for den.
1. I hurtigfanen **Generelt** angir du *Ja* for alternativet **Arbeidsflyt for godkjenning**. Hvis du blir bedt om å bekrefte endringen, velger du **Ja**.
1. Velg arbeidsflyten du vil bruke for det valgte journalnavnet, i **Arbeidsflyt**-feltet.

### <a name="issue-resolution-2"></a>Problemløsning 2

Hvis arbeidsflyten bruker tilpasset kode, kan det oppstå problemer etter at du har oppgradert systemet. **Send inn**-knappen kan for eksempel være nedtonet i journalarbeidsflyten, slik at du ikke kan velge den for å godkjenne en innsending.

Hvis **Send inn**-knappen er nedtonet, kan arbeidsflyten ha blitt tilpasset, som betyr at metoden for arbeidsflyten, `canSubmitToWorkflow()` i `FormDataUtil`, har blitt utvidet. Du kan rette dette problemet ved å endre hvordan du utvider metoden for `canSubmitToWorkflow()`, slik at den bruker strukturen i følgende eksempel.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Problemløsning 3

Hvis problemet bare gjelder noen få bestemte brukere, kan det hende at disse brukerne ikke har sikkerhetsrettighetene som kreves for å kjøre arbeidsflytoperasjoner på lagerjournaler. Kontroller at hver berørte bruker har sikkerhetsrettigheten *Vedlikehold lagerjournalarbeidsflyt*. Denne rettigheten er som standard tilordnet til en plikt med samme navn, og denne plikten brukes på rollene *Lagerarbeider* og *Lagersjef*.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Lagerjournalen forblir låst av systemet, og den satsvise arbeidsflytjobben fungerer ikke.

### <a name="issue-description"></a>Problembeskrivelse

En av lagerjournalene er låst av en eller annen operasjon og blir ikke frigitt. Hvis det for eksempel oppstår en ukjent feil under postering (som er en systemlåst operasjon), kan det hende at journalen forblir låst av systemet. I dette tilfellet vil behandlingsprogrammet for arbeidselement for arbeidsflyt generere en feil mens det foretar låsvalidering.

### <a name="issue-resolution"></a>Problemløsning

Logg deg på SQL Server-forekomsten for Supply Chain Management, og kontroller om **InventJournalTable.SystemBlocked** er satt til *1*. Hvis den er det, må du kontrollere at journalen ikke er låst, og deretter tilbakestille **InventJournalTable.SystemBlocked** til *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Lagerjournalarbeidsflyten min blir aldri fullført, og journalen kan ikke redigeres eller posteres.

### <a name="issue-description"></a>Problembeskrivelse

Når du har sendt inn en arbeidsflyt for journalgodkjenning, slutter arbeidsflytbehandlingen å svare, og du kan ikke redigere eller behandle journalene.

### <a name="issue-resolution"></a>Problemløsning

Det er flere årsaker til at arbeidsflytbehandling kanskje ikke fullføres. Se etter følgende problemer:

- Gå til **Lagerstyring &gt; Oppsett &gt; Arbeidsflyter for lagerstyring**, og gå gjennom konfigurasjonen til den berørte arbeidsflyten. Hvis du vil ha mer informasjon, kan du se [Godkjenningsarbeidsflyter for lagerjournal](inventory-journal-workflow.md).
- Arbeidsflyten kan bli utsatt for et unntak eller en feil. Gå gjennom loggen for arbeidselement i den berørte arbeidsflyten for å se om den omfatter en programfeil som avslutter arbeidsflyten.
- Lagerjournalen kan bare oppdateres eller redigeres hvis den er godkjent. Hvis tilbakekalling er aktiv, kan du prøve å tilbakekalle journalen. Kjøring av den satsvise arbeidsflytjobben kan bli avbrutt av flere årsaker. Noen av disse årsakene kan være forårsaket av problemer med arbeidsflytrammeverket.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Betingelser for lagerjournalarbeidsflyt gjelder bare på journalnivå, ikke på linjenivå

### <a name="issue-description"></a>Problembeskrivelse

Du kan få dette problemet hvis du for eksempel prøver å definere en betingelse for lagerjournalarbeidsflyt for kostbeløpet. Du definerer betingelsen slik at trinn 1 bare kjøres når kostbeløpet er mindre enn 100. Deretter definerer du en ny betingelse slik at trinn 2 bare kjøres når kostbeløpet er større enn eller lik 100. Når arbeidsflyten deretter kjøres, viser arbeidsflytloggen deretter bare én linje, og den første betingelsen evalueres alltid som *sann*, uavhengig av verdien som sendes.

### <a name="issue-workaround"></a>Problemløsning

I gjeldende utgivelse gjelder betingelser for lagerarbeidsflyt bare på journalnivå, ikke på linjenivå. Denne virkemåten er standard. Det anbefales at du bare angir betingelseskriteriene for attributter på journalnivå.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Filterruten på siden Beholdningsliste filtrerer ikke resultatene slik jeg forventer.

### <a name="issue-description"></a>Problembeskrivelse

Filtrene i filterruten på siden **Beholdningsliste**  filtrerer ikke resultater slik du forventer.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard.

Siden  **Beholdningsliste**  er satt sammen fra en detaljert lagerbeholdningstabell som inkluderer alle tilgjengelige dimensjoner. Listen på denne siden er imidlertid et sammendrag. Derfor kan den kombinere rader fra kildetabellen ved å samle verdier i henhold til dimensjonene som vises.

Filtre som er definert i filterruten, gjelder for kildetabellen, ikke for den aggregerte listen. Denne virkemåten kan av og til gi uventede resultater, som vist i [disse eksemplene](inventory-on-hand-list.md#examples).

 [Filtrene som oppgis i rutenettet](inventory-on-hand-list.md#grid-filters), *gjelder* imidlertid for den aggregerte listen. Disse filtrene inkluderer både hurtigfilteret øverst i rutenettet og filteret for hver kolonneoverskrift.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Enheten og enhetsantallet fungerer ikke riktig i lagerjournalen.

### <a name="issue-description"></a>Problembeskrivelse

Ett eller begge av følgende problemer kan oppstå når du arbeider med enheter og antall i en lagerjournal:

- Du ser ikke enheter eller enhetsantall i lagerjournalen mens en omregningsenhet er definert for det frigitte produktet, og du kan ikke endre enheten i lagerjournalen.
- Du ser feltene **Antall** og **Enhet** i lagerjournalen, men ikke feltet **Enhetsantall**. Hvis du endrer enheten, angir et antall og posterer journalen, viser journalen fortsatt den opprinnelige måleenheten for dette antallet.

### <a name="issue-resolution"></a>Problemløsning

Følg fremgangsmåten nedenfor for å løse problemet.

1. I arbeidsområdet **Funksjonsbehandling** må du kontrollere at funksjonen *Bruke måleenhet og enhetsantall i lagerjournaler* er aktivert. Denne funksjonen legger til feltene **Enhet** og **Enhetsantall** i journalen.
1. Etter at funksjonen er aktivert, bruker du feltene **Antall**, **Enhetsantall** og **Enhet** på følgende måte:

    - **Antall** – Angi antallet ved å bruke standardenheten som er definert for det frigitte produktet. Selve standardenheten vises imidlertid ikke her. Hvis det defineres en omregning mellom standardenheten og enheten som er valgt i **Enhet**-feltet, oppdateres **Antall**-feltet automatisk basert på valgene i feltene **Enhetsantall** og **Enhet**.
    - **Enhetsantall** – Angi antallet ved å bruke enheten som er valgt i **Enhet**-feltet.
    - **Enhet** – Velg enheten som skal brukes på verdien i **Enhetsantall**-feltet.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Jeg får følgende feilmelding: «Maksimalt antall desimaler for lagerføringsenheten er 0.»

### <a name="issue-description"></a>Problembeskrivelse

Når du prøver å postere en lagertransaksjon eller lagerreservasjon, får du følgende feilmelding: «Maksimalt antall desimaler for lagerføringsenheten er 0.»

Dette problemet oppstår når lagertransaksjonsantallet er angitt som en desimalverdi som er under presisjonsnivået som feltet støtter. Et antall på *0,5* er for eksempel angitt for en lagertransaksjon, men bare heltallsantall støttes. Verdien må derfor være *1* i stedet for *0,5*.

### <a name="issue-resolution"></a>Problemløsning

1. Kjør følgende skript på SQL Server-forekomsten for å avrunde antall i lagertransaksjonene. Dette skriptet retter verdiene i **inventTrans**-tabellen.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Kjør en konsekvenskontroll for lagerbeholdning der alternativet **Rett feil** er aktivert. Denne kontrollen retter verdiene i **inventSum**-tabellen.

> [!IMPORTANT]
> Det anbefales på det sterkeste at du redigerer skriptet nøye etter behov for miljøet, tester det i et testmiljø og kontrollerer de resulterende dataene før du kjører skriptet i et produksjonsmiljø.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]