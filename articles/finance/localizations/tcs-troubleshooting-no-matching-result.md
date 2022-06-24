---
title: Finner ingen samsvarende resultater
description: Denne artikkelen beskriver hvordan du feilsøker feilmeldingen Finner ingen samsvarende resultater i avgiftsberegningstjenesten.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845151"
---
# <a name="no-matching-result-could-be-found"></a>Finner ingen samsvarende resultater

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver fremgangsmåten for å feilsøker feilmeldingen Finner ingen samsvarende resultater i avgiftsberegningstjenesten.

## <a name="symptom"></a>Symptom

Du får følgende feilmelding: Topptekst/linjer – 1, avgiftsgruppe, finner ingen samsvarende resultater.

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Årsak

Problemet oppstår når funksjonsoppsettet i RCS (Regulatory Configuration Service) er feil.

## <a name="troubleshoot"></a>Feilsøking

1. Last ned feilsøkingsfilen. Hvis du vil ha mer informasjon, kan du se [Aktiver feilsøkingsmodus for feilsøking](tcs-troubleshooting-enable-debug-mode.md).
2. Sammenlign inndataene for avgiftstjenesteberegningen med funksjonsoppsettet for å løse oppsettet.

    Følgende eksempel viser inndata for avgiftstjenesteberegning.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    I tabellen nedenfor finner du en oversikt over avgiftsgrupper som gjelder i RCS.

    | Topptekst.Forretningsprosess | Linjer.Forretningsenhet | Topptestk.Send fra postnummer | Mva-gruppe |
    |-------------------------|---------------------|---------------------------|-----------|
    | Journal                 |                     |                           | Gruppe A   |
    | Salg                   |                     | 30160                     | Gruppe B   |

    I henhold til inndataene for avgiftstjensteberegningen er **Forretningsprosess**-verdien på toppteksten **Salg**,og verdien for **Send fra postnummer** på toppteksten er **30159**. Denne inndataen er basert på oppsettet for gjeldende regler i RCS. Fordi det ikke finnes noen samsvarende linje, oppstår feilen.

    > [!NOTE]
    > Hvis verdien i funksjonsregelen er tom, gjelder regelen en hvilken som helst verdi.

## <a name="mitigation"></a>Reduksjon

Følg denne fremgangsmåten for å rette feilen.

1. I RCS kan du gå til **Globaliseringsfunksjoner** \> **Avgiftsberegning**.
2. Opprett en ny versjon av funksjonen.
3. Legg til en linje for tilsvarende informasjon.

    | Topptekst.Forretningsprosess | Linjer.Forretningsenhet | Topptestk.Send fra postnummer| Mva-gruppe |
    |-------------------------|---------------------|--------------------------|-----------|
    | Journal                 |                     |                          | Gruppe A   |
    | Salg                   |                     | 30160                    | Gruppe B   |
    | Salg                   |                     | 30159                    | Gruppe B   |

4. Publiser versjonen for funksjonsoppsettet.
5. I Microsoft Dynamics 365 Finance går du til **Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Parametere for avgiftsberegning** og velger den nye versjonen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
