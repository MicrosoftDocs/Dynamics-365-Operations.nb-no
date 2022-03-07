---
title: Avgift posteres til feil finanskonto i bilaget
description: Dette emnet gir feilsøkingsinformasjon som kan hjelpe når skatt posteres til feil finanskonto i bilaget.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020097"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Avgift posteres til feil finanskonto i bilaget

[!include [banner](../includes/banner.md)]

Under postering kan avgift posteres til feil finanskonto i bilaget. Hvis du vil feilsøke dette problemet, følger du trinnene i de følgende delene etter behov. Eksemplene i dette emnet bruker en salgsordre som forretningsdokument.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Finn mva-koden til den feil posterte mva-transaksjonen

1. Velg transaksjonen du vil arbeide med, på **Bilagstransaksjoner**-siden, og velg deretter **Postert merverdiavgift**.

    [![Postert merverdiavgift-knappen på bilagstransaksjonssiden](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Se gjennom verdien i **Mva-kode**-feltet. I dette eksemplet er den **Mva 19**.

    [![Mva-kode-feltet på siden Postert merverdiavgift](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Kontroller finansposteringsgruppen for mva-koden

1. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.
2. Søk etter og velg avgiftskoden, og gå deretter gjennom verdien i feltet **Finansposteringsgruppe**. I dette eksemplet er den **Mva**.

    [![Feltet Finansposteringsgruppe på siden Mva-koder](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. Verdien i feltet **Finansposteringsgruppe** er en kobling. Hvis du vil vise detaljer om gruppens konfigurasjon, velger du koblingen. Du kan også velge og holde (eller høyreklikke) i feltet og velge **Vis detaljer**.

    [![Vis detaljer-kommando](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. I feltet **Utgående merverdiavgif** må du kontrollere at kontonummeret er riktig i henhold til transaksjonstypen. Hvis ikke velger du riktig konto. I dette eksemplet skal merverdiavgiften for salgsordren posteres til betalingskonto for merverdiavgift 222200.

    [![Feltet Konto, utgående mva på siden Finansposteringsgrupper](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png).

    Følgende tabell inneholder informasjon om hvert felt på siden **Finansposteringsgrupper**.

    | Felt                  | beskrivelse |
    |------------------------|-------------|
    | Konto, utgående mva      | Hovedkontoen for utgående merverdiavgift som skal betales til skattemyndighetene. |
    | Innkommende merverdiavgift   | Hovedkontoen for inngående mva som mottas fra skattemyndighetene. |
    | Use tax-utgift        | Hovedkontoen som brukes til å postere fradragsberettiget use tax som leverandører ikke krever eller rapporterer til skattemyndighetene som en del av GST/HST (Goods and Services Tax / Avstemt mva) for Den europeiske union. Alternativet **Use tax** må velges for mva-koden i mva-gruppen som skal brukes i transaksjonen. Dette feltet er ikke tilgjengelig hvis **Bruk avgiftsregler for merverdiavgift** er valgt på siden **Økonomiparametere**. |
    | Forfalt use tax        | Hovedkontoen som brukes til å postere innkommende use tax som betales til skattemyndighetene. |
    | Utligningskonto     | Hovedkontoen som brukes til å postere nettosaldoen for finanskontoene som er angitt i feltene **Forfalt use tax** og **Inngående merverdiavgift**. |
    | Leverandørkontantrabatt   | Hovedkontoen som brukes til å postere en kontorabatt for mva-koder knyttet til denne finansposteringsgruppen. |
    | Kundekontantrabatt | Hovedkontoen som brukes til å postere en kontorabatt for mva-koder knyttet til denne finansposteringsgruppen. |

    Hvis du vil ha mer informasjon, kan du se [Definere finansposteringsgrupper for merverdiavgift](tasks/set-up-ledger-posting-groups-sales-tax.md).

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Feilsøke i kode for å kontrollere finansdimensjoner

I koden bestemmes posteringskontoen av finansdimensjonen. Finansdimensjonen lagrer post-IDen til en konto i databasen.

1. Legg til et stoppunkt ved metodene **Tax::saveAndPost()** og **Tax::post()** for en salgsordre. Vær oppmerksom på verdien til **\_LedgerDimension**.

    [![Eksempel på salgsordrekode som har et stoppunkt](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Legg til et stoppunkt ved metodene **TaxPost::saveAndPost()** og **TaxPost::postToTaxTrans()** for en bestilling. Vær oppmerksom på verdien til **\_LedgerDimension**.

    [![Eksempel på bestillingskode som har et stoppunkt](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Kjør følgende SQL-spørring for å finne visningsverdien til kontoen i databasen, basert på post-IDen som er lagret av finansdimensjonen.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Visningsverdi for post-IDen](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Undersøk kallstakken for å finne ut hvor **_ledgerDimension**-verdien er tilordnet. Vanligvis kommer verdien fra **TmpTaxWorkTrans**. I dette tilfellet bør du legge til et stoppunkt ved **TmpTaxWorkTrans::insert()** og **TmpTaxWorkTrans::update()** for å finne hvor verdien er tilordnet.

## <a name="determine-whether-customization-exists"></a>Fastslå om det finnes tilpasning

Hvis du har fullført trinnene i de forrige delene, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning. Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
