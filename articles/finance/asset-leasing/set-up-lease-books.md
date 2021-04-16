---
title: Definere leietablåer
description: Dette emnet beskriver informasjonen som vedlikeholdes i leietablåer. Leietablåer inneholder regnskapsretningslinjer som bestemmer hvordan en leieavtale gjøres rede for i systemet.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0aac682c66bef51c802efcb1c5e34dd60c38f9fe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819680"
---
# <a name="set-up-lease-books"></a>Definere leietablåer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Leietablåer inneholder regnskapsretningslinjer som bestemmer hvordan en leieavtale gjøres rede for i systemet. I tillegg til kontantprinsippregnskap støtter aktivaleie følgende standarder:

- Generally Accepted Accounting Principles i USA (amerikansk GAAP)
- Accounting Standards Codification-emne 842 (ASC 842)
- ASC 840
- International Financial Reporting Standard 16 (IFRS 16)
- International Accounting Standard 17 (IAS 17)

Hvis du vil opprette et leietablå, følger du disse trinnene.

1. Gå til **Aktivaleie \> Oppsett \> Leietablåer**.
2. Velg **Ny** for å legge til et tablå.
3. Angi følgende felt.

    | Navn                                     | beskrivelse |
    |------------------------------------------|-------------|
    | Posteringslag                            | Velg posteringslaget som skal brukes. Hver bok som er knyttet til en leieavtale, defineres for et bestemt posteringslag. Hvert posteringslag har forskjellige posteringsformål. |
    | Leietype                               | Velg om leieavtalen skal klassifiseres automatisk, eller om den skal forhåndsdefineres som finansiell leie eller gjeldende leie. |
    | Regnskapsrammeverk                     | Velg rammeverket som er tilknyttet tablået. |
    | Konfigurasjon av leieperiode/levetid          | Systemet klassifiserer leieavtalen som finansiell leie hvis leietypen er satt til **Automatisk**, og hvis leieperioden for levetiden for aktivaet er større enn eller lik prosentdelen som er angitt i dette feltet.  |
    | Konfigurasjon av nåværende verdi / virkelig verdi på aktivum   | Angi et helttall for å definere terskelen som skal fastsette leietypen. Hvis nå-verdien av fremtidige minimumsbetalinger for leie er mer enn den brukerdefinerte verdien fra tablåoppsettet, og hvis tablåets leieklassifisering er satt til automatisk, vil systemet klassifisere leieavtalen som en finansiell leie. |
    | Korttidsterskel                     | Angi antall måneder som skal brukes som en terskel for kortsiktige leieavtaler. Hvis leieperioden er mindre enn eller lik antallet måneder du angir her, vil systemet klassifisere leieavtalen som en kortsiktig leieavtale, og utsatt leie vil bli brukt. |
    | Terskel for lav verdi                      | Angi et beløp som skal brukes som terskel for lavverdileie. Hvis virkelig verdi for aktivumet er mindre enn eller lik verdien du angir her, vil systemet klassifisere leieavtalen som en lavverdileie, og utsatt leie vil bli brukt. |
    | Betal til leverandør                            | Sett dette alternativet til **Ja** for å tillate at leiebetalinger kan posteres, som en faktura, til leverandørkontoen som er angitt for hver leieavtale. Når en leiebetaling posteres, vil leverandørkontoen bli kreditert. Hvis dette alternativet er satt til **Nei**, vil kontoen som er angitt for **Leiebetaling**-posteringstypen på siden **Parametere for leiepostering**, bli kreditert i stedet. |
    | Leiekonvensjon                       | Velg konvensjonen for startdatoen for leieavtalen:<ul><li><b>Ingen</b> – Bruk startdatoen for leieavtalen som startdato.</li><li><b>Hele måneden</b> – Bruk den første dagen i måneden som startdatoen for leieavtalen faller på, som startdato.</li></ul><p>Hvis du velger <b>Ingen</b>, er det en risiko for at planene for nedbetaling av gjeld og avskrivning av aktiva vil avsette og postere utgifter midt i måneden i stedet for på slutten av måneden. Hvis du velger <b>Hele måneden</b>, sikrer du at systemet vil begynne å ta hensyn til utleieavtalen på den første dagen i måneden, og at hele månedens utgift blir avsatt og postert på den siste dagen i måneden.</p><p><strong>Merk: </strong>Funksjonen for leiekonvensjoner må aktiveres ved hjelp av funksjonsadministrasjon. I arbeidsområdet for <b>Funksjonsbehandling</b> finner og velger du funksjonen for <b>Leiekonvensjon for aktivaleie</b>, og deretter velger du <b>Aktiver nå</b>.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]