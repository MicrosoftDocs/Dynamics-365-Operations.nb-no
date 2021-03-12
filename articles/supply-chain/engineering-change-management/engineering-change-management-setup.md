---
title: Opprett felles verdier for behandling av teknisk endring
description: Dette emnet beskriver hvordan du kan opprette vanlige verdier som brukes for parametere i forskjellige deler av behandling av teknisk endring.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b46bc10f8b75a58b8baefd88aa6a0b79c59d6544
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005408"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Opprett felles verdier for behandling av teknisk endring

[!include [banner](../includes/banner.md)]

Når du konfigurerer behandling av teknisk endring, må du opprette flere samlinger med verdier som skal brukes til å fylle ut rullegardinlister i andre deler av brukergrensesnittet (UI). Du bør angi disse verdiene i henhold til produkttypene du produserer og dine spesifikke forretningsbehov.

## <a name="engineering-change-categories"></a>Kategorier for teknisk endring

Du bruker katergorier for teknisk endring til å organisere ordrer om teknisk endring slik at de er enklere å behandle og se gjennom. Det kan for eksempel være nyttig å sette opp en arbeidsflyt der, avhengig av kategorien, og en bestemt avdeling må se gjennom de foreslåtte endringene. Derfor inkluderer ordren om teknisk endring et **Kategori**-felt.

Hvis du vil opprette en samling med kategori for teknisk endring som brukes i firmaet, går du til **Behandling av teknisk endring \> Oppsett \> Behandling av teknisk endring \> Kategorier for teknisk endring**. Du kan deretter bruke knappene i handlingsruten til å legge til, fjerne og redigere verdier, og til å ordne dem i den rekkefølgen de skal vises i, i rullegardinlistene der de vises.

## <a name="engineering-change-priorities"></a>Prioriteter for teknisk endring

Du bruker prioriteter for teknisk endring til å angi viktigheten av en ordre om teknisk endring. De kan hjelpe deg med å holde rede på viktigheten av en ordre om teknisk endring, slik at du enkelt kan identifisere hvilke ordrer som skal behandles først, og hvor raskt.

Hvis du vil opprette en samling med prioriteter for teknisk endring som brukes i firmaet, går du til **Behandling av teknisk endring \> Oppsett \> Behandling av teknisk endring \> Prioriteter for teknisk endring**. Du kan deretter bruke knappene i handlingsruten til å legge til, fjerne og redigere verdier, og til å ordne dem i den rekkefølgen de skal vises i, i rullegardinlistene der de vises.

## <a name="engineering-change-reasons"></a>Årsaker til teknisk endring

Årsaker til teknisk endring angir årsaken til eller typen endringen i endringsordren.

Hvis du vil opprette en samling med årsaker til teknisk endring som brukes i firmaet, går du til **Behandling av teknisk endring \> Oppsett \> Behandling av teknisk endring \> Årsaker til teknisk endring**. Du kan deretter bruke knappene i handlingsruten til å legge til, fjerne og redigere verdier, og til å ordne dem i den rekkefølgen de skal vises i, i rullegardinlistene der de vises.

## <a name="material-disposal-codes"></a>Koder for materialavhending

Du bruker koder for materialavhending til å kategorisere materialer som brukes i ferdigvarer, eller komponenter som må fjernes på en bestemt måte, eller krever behandling før de kan legges i det vanlige avfallet. Når du legger til et relevant produkt i en ordre om teknisk endring, kan du tilordne en avhendingskode som del av endringsdetaljene.

Hvis du vil opprette en samling med koder for materialavhending som brukes i firmaet, går du til **Behandling av teknisk endring \> Oppsett \> Behandling av teknisk endring \> Koder for materialavhending**. Du kan deretter bruke knappene i handlingsruten til å legge til, fjerne og redigere verdier, og til å ordne dem i den rekkefølgen de skal vises i, i rullegardinlistene der de vises.

## <a name="received-customer-approval"></a>Mottatt kundegodkjenning

Når du utformer produkter for en bestemt kunde, må du ofte validere utformingen og spesifikasjonene før produktet kan settes til klar. Med feltet **Mottatt kundegodkjenning** kan du angi hvor langt frem i kundens godkjenningsprosess produktet er, eller om godkjenningen er mottatt.

Hvis du vil opprette en samling med verdier for mottatt kundegodkjenning som brukes i firmaet, går du til **Behandling av teknisk endring \> Oppsett \> Behandling av teknisk endring \> Mottatt kundegodkjenning**. Du kan deretter bruke knappene i handlingsruten til å legge til, fjerne og redigere verdier, og til å ordne dem i den rekkefølgen de skal vises i, i rullegardinlistene der de vises.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Teknisk endring – koder for helse, miljø og sikkerhet

Hvis standardbestemmelser for helse, miljø og sikkerhet, eller firmaspesifikke bestemmelser eller prosedyrer, må vurderes i produksjon av et produkt, kan du bruke koder for helse, miljø og sikkerhet for å definere dem. I ordren om teknisk endring kan du angi hvilke koder som skal gjelde for produksjonen av et produkt, mens du redigerer detaljene for det berørte produktet.

Hvis du vil opprette en samling med verdier for helse og sikkerhet som brukes i firmaet, går du til **Behandling av teknisk endring \> Oppsett \> Behandling av teknisk endring \> Teknisk endring – koder for helse, miljø og sikkerhet**. Du kan deretter bruke knappene i handlingsruten til å legge til, fjerne og redigere verdier, og til å ordne dem i den rekkefølgen de skal vises i, i rullegardinlistene der de vises.

## <a name="engineering-change-severities"></a>Alvorsgrader for teknisk endring

Du bruker alvorsgrader for teknisk endring til å angi hvilket innvirkningsnivå som gjelder for produktene i en ordren om teknisk endring.

Hvis du vil opprette en samling med alvorsgrader for teknisk endring som brukes i firmaet, går du til **Behandling av teknisk endring \> Oppsett \> Behandling av teknisk endring \> Alvorsgrader for teknisk endring**. Du kan deretter bruke knappene i handlingsruten til å legge til, fjerne og redigere verdier, og til å ordne dem i den rekkefølgen de skal vises i, i rullegardinlistene der de vises.

Du kan opprette regler som gjelder for hver alvorsgrad du oppretter. Hvis du vil ha mer informasjon om hvordan du tilordner disse reglene, kan du se neste del.

## <a name="engineering-change-severity-rule-sets"></a>Regelsett for alvorsgrad for teknisk endring

Du bruker regelsett for alvorsgrad for teknisk endring til å opprette en gruppe regler som du kan bruke til automatisk å beregne alvorsgrad for endringsordren, basert på typen endringer i de berørte produktene. Hvis du vil bruke reglene for alvorsgrad, åpner du siden **Parametere for behandling av teknisk endring** og angir feltet **Alvorsgrad** til *Beregn* eller *Beregn automatisk*.

Når systemet vurderer alvorsgraden, behandles reglene i den rekkefølgen de vises på siden, fra øverst til nederst. For at en regel skal kunne velges og ha prioritet opprettet, må alle reglene i et regelsett oppfylles.

Hvis du vil angi hvilke regler som skal gjelde for hver alvorsgrad for endring som du har definert, kan du gå til **Behandling av teknisk endring \> Oppsett \> Behandling av teknisk endring \> Regelsett for alvorsgrad for teknisk endring**. Følg deretter ett av disse trinnene.

- Hvis du vil opprette et nytt regelsett, velger du **Nytt** i handlingsruten, og deretter angir du feltene som beskrevet senere i denne delen.
- Hvis du vil redigere et eksisterende regelsett, velger du det i listeruten, velger **Rediger** i handlingsruten og angir deretter feltene som beskrevet senere i denne delen.
- Hvis du vil slette et eksisterende regelsett, velger du det i listeruten, og deretter velger du **Slett** i handlingsruten.
- Hvis du vil omorganisere listen over regelsett, velger du et regelsett i listeruten, og deretter bruker du **opp**- og **ned**-knappene i handlingsruten til å omplassere det.

For hvert regelsett angir du feltet nedenfor:

- **Alvorsgrad** – Velg alvorsgraden du vil opprette regler for. Du bruker siden **Alvorsgrader for teknisk endring** til å opprette og gi gradene navn. (Se forrige del hvis du vil ha mer informasjon.)

Bruk knappene på **Regler**-hurtigfanen til å legge til eller fjerne en regel for gjeldende innstilling for alvorsgrad. Hver regel har et **Regel**-felt og et **Navn**-felt. Reglene etableres av systemet og angir hvilke typer endringer et produkt kan ha. Navnet angir endringstypen.
