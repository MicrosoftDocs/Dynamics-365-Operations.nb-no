---
title: Forringe bruksrettseiendeler
description: Dette emnet beskriver funksjonaliteten som registrerer en verdiforringelse og justerer avskrivningsplanen for aktiva for et Accounting Standards Codification-emne 842 (ASC 842) for gjeldende leie.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 3b648075a681fb01720149aac4f479dccf963489
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229532"
---
# <a name="impair-right-of-use-assets"></a>Forringe bruksrettseiendeler

[!include [banner](../includes/banner.md)]

Hvis det ikke er mulig å gjenopprette det indirekte beløpet for en bruksrettseiendel, må du kanskje teste om aktivaet er forringet. Hvis du mener at aktivaet er forringet, kan aktivaleie registrere forringelsen og justere avskrivningsplanen i henhold til dette. Dette emnet beskriver funksjonaliteten som registrerer verdiforringelsen og justerer avskrivningsplanen for et Accounting Standards Codification-emne 842 (ASC 842) for gjeldende leie. Den samme metoden gjelder også for International Financial Reporting Standard 16 (IFRS 16) for leieavtaler.

Den gjenstående saldoen for bruksrettseiendelen vil bli nedbetalt lineært for antall perioder som gjenstår, uansett om leieavtalen er klassifisert som en finansiell leie under IFRS 16 eller en leieavtale under ASC 842.

## <a name="impair-an-rou-asset"></a>Forringe en bruksrettseiendel

1. Gå til forringede leieavtalen, og velg **Tablåer**.
2. Velg **Verdiforringelse** i handlingsruten.
3. I dialogboksen som vises, i feltet **Verdiforringelsesbeløp**, angir du beløpet for verdiforringelse. Hvis du vil redusere bruksrettseiendelen, bør du angi en positiv verdi.
4. I feltet **Transaksjonsdato** angir du datoen da verdiforringelsen skal posteres.
5. I feltet **Gjenstående perioder** angir du det gjenstående antallet måneder som skal nedbetales.
6. Aktiver parameteren **Post** hvis du vil at systemet automatisk skal postere journaloppføringen for verdiforringelsesutgiften. Hvis du lar denne parameteren være deaktivert, oppretter systemet posten, men posterer den ikke. Du kan deretter bokføre posten fra siden **Journaler for leie av anleggsmidler**.
7. Sett alternativet **Forhåndsvis for postering** til **Ja** for å vise den foreslåtte posten før den opprettes eller posteres.
8. Sett alternativet for **Lukk bok** til **Ja** for å lukke leietablået. Du kan ikke angre denne handlingen. Oppføringer kan ikke posteres mot lukkede leieavtaler, og lukkede leieavtaler kan ikke justeres.
9. Velg **OK** for å opprette eller postere verdiforringelsen.
10. Hvis du vil vise avskrivningsplanen for det forringede aktivaet, åpner du avskrivningsplanen for aktivaet for leietablået. Aktivaet blir nå avskrevet på et lineært grunnlag over det antallet måneder du har angitt i feltet **Gjenstående perioder**.
11. Hvis du vil vise journaloppføringen for verdiforringelsesutgiften, velger du **Journal for aktivaleie** i handlingsruten i tablået for forringet leieavtale. Systemet oppretter en journaloppføring som debiterer posteringskontoen for verdiforringelsesutgiften og krediterer posteringskontoen for leieaktiva.
12. Hvis du vil vise den bokførte verdien for bruksrettseiendelen, velger du **Aktivatransaksjoner** i handlingsruten for leietablået.

## <a name="example-of-rou-asset-impairment"></a>Eksempel på verdiforringelse for bruksrettseiendel

I dette eksemplet er leieavtalen et ikke-spesialisert aktiva som ikke overfører eierskap eller gir leier muligheten til å kjøpe.

### <a name="setup"></a>Installasjon

Tabellene nedenfor viser verdiene som er angitt i fanene **Generelt** og **Linjer i betalingsplan** for leieavtalen som brukes i dette eksemplet.

**Fanen Generelt**

| Felt                      | Verdi            |
|----------------------------|------------------|
| Aktivaets gjennomsnittsverdi    | 600,000          |
| Trinnvis lånerente | 7 %               |
| Sammensetningsintervall       | Årlig         |
| Aktivalevetid (måneder) | 600              |
| Annuitetstype               | Vanlig annuitet |
| Iverksettelsesdato          | 01/01/2019       |

**Fanen Linjer i betalingsplan**

| Felt             | Verdi      |
|-------------------|------------|
| Startdato        | 1/1/2019   |
| Periodeintervall   | Månedlig    |
| Perioder           | 120        |
| Sluttdato          | 12/31/2028 |
| Betalingsfrekvens | Årlig   |
| Betalingsbeløp    | 10,000     |

### <a name="steps"></a>Trinn

1. Når du har opprettet en leieavtale som beskrevet tidligere i dette emnet, går du til leietablået og bekrefter betalingsplanen. Poster deretter journaloppføringen for opprinnelig føring. Det første bruksrettseiendelen og leieforpliktensen skal være $70.235,81. I dette eksemplet ble leieavtalen klassifisert som en gjeldende leie under ASC 842.
2. Kjør prosessen for satsvis journal tre ganger for å simulere at det er gått tre år for leiebetalingene, renteutgiftene og avskrivningsutgiftene.
3. Når du er ferdig med å kjøre alle tre kjørslene, går du tilbake til leietablået og åpner tabellene for gjeld og anleggsmiddeltransaksjoner for å vise gjeldende bokførte verdi for bruksrettseiendel og leieforpliktelse. Etter tre år skal avstandsverdien være omtrent $53.893,00, og verdien for aktivaet skal være ca. $53.893,00. 

    Etter tre år kan virksomheten utføre verdiforringelsestester, og det fastsettes om bruksrettseiendelen har en verdiforringelse på $35.000. Du må nå registrere denne verdiforringelsen.
    
4. Gå til leietablået, og deretter, i handlingsruten, velger du **Verdiforringelse**.
5. På siden **Parametere for verdiforringelse** angir du følgende detaljer.

    | Felt                  | Verdi    |
    |------------------------|----------|
    | Verdiforringelsesbeløp      | 35,000   |
    | Transaksjonsdato       | 1/1/2022 |
    | Gjenstående perioder      | 84       |
    | Poster                   | Ja      |
    | Forhåndsvis for postering | Nr.       |
    | Lukk tablå             | Nr.       |

6. En journaloppføringen for verdiforringelsesutgift er opprettet og postert. For å vise det går du til journalen for aktivaleie i leietablået. Legg merke til at beløpet for verdiforringelsen ble debitert til posteringskontoen for verdiforringelsesutgift, og at posteringskontoen for bruksrettseiendel ble kreditert.
7. Hvis du vil vise nettoinnvirkning for verdiforringelsen, går du til tabellene for gjeld og anleggsmiddeltransaksjoner. Legg merke til at verdiforringelseutgiften har redusert bruksrettseiendelen, men det indirekte beløpet for leieforpliktelse er ikke endret.

Verdiforringelsen har én annen effekt som du bør vurdere. Fordi beløpet for bruksrettseiendelen nå er mye mindre enn leieforpliktelsen, må beløpet avskrives på en annen måte enn før. Spesielt avskrives aktivaet nå på en lineær måte i løpet av de gjenværende 84 månedene i leieavtalen, som begynner på transaksjonsdatoen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]