---
title: Avgiftskode kan ikke bestemmes
description: Denne artikkelen beskriver hvordan du feilsøker feilmeldingen Avgiftskode kan ikke bestemmes i avgiftsberegningstjenesten.
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
ms.openlocfilehash: 6a74724de38cf362900277ab9addc8e6894f7689
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877866"
---
# <a name="tax-code-cannot-be-determined"></a>Avgiftskode kan ikke bestemmes

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver fremgangsmåten for å feilsøker feilmeldingen Avgiftskode kan ikke bestemmes i avgiftsberegningstjenesten.

## <a name="symptom"></a>Symptom

Du får følgende feilmelding: Topptekst/linjer – 1, avgiftskode kan ikke bestemmes. Du finner eventuelt feilen i feilsøkingsfilen som vist i følgende eksempel. Hvis du vil ha mer informasjon, kan du se [Aktiver feilsøkingsmodus for feilsøking](tcs-troubleshooting-enable-debug-mode.md).

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
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
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

Problemet oppstår sannsynligvis fordi avgiftsgruppen og avgiftsgruppen for vare ikke overlapper.

## <a name="troubleshoot"></a>Feilsøking

Følg fremgangsmåten nedenfor for å feilsøke problemet.

1. I feilsøkingsfilen må du kontrollere at avgiftsgruppen og avgiftsgruppen for vare er bestemt. Hvis verdiene for **Avgiftsgruppe** og **Avgiftsgruppe for vare** er tomme, er ikke avgiftsgruppen og avgiftsgruppen for vare bestemt. Hvis de er bestemt, kan resultatene bli feil.

    Her er et eksempel på en feilsøkingsfil.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
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

2. Kontroller at alternativet **Overstyr merverdiavgift** i fanen **Oppsett** i salgsordrelinjedetaljene, er aktivert.

    - Hvis dette er aktivert, bestemmes avgiftskoder av verdiene for **Avgiftsgruppe** og **Avgiftsgruppe for vare** som du angir på transaksjonslinjen. Kontroller at disse verdiene er riktig angitt.
    - Hvis dette ikke er aktivert, må du kontrollere at riktige verdier er angitt for feltene **Avgiftsgruppe** og **Anvendelse av vareavgiftsgruppe**. Hvis du vil ha mer informasjon, kan du se [Ingen samsvarende resultat](tcs-troubleshooting-no-matching-result.md).

3. Hvis avgiftsgruppen og avgiftsgruppen for vare er riktig bestemt, må du fastslå om det er noe kryss for dem.

    1. I RCS går du til **Avgiftsfunksjoner** \> **Avgiftskoder og -grupper** \> **Avgiftsgruppe**.

        | Linjeavgiftsgruppe | Avgiftskoder |
        |----------------|-----------|
        | Gruppe A        | A         |

    2. Gå til **Avgiftsfunksjoner** \> **Avgiftskoder og -grupper** \> **Avgiftsgruppe for vare**.

        | Avgiftsgruppe for linjevare | Avgiftskoder |
        |---------------------|-----------|
        | Gruppe B             | T         |

    Hvis det ikke er noe kryss for avgiftsgruppen og avgiftsgruppen for vare, bestemmes ikke avgiftskoden.

## <a name="mitigation"></a>Reduksjon

1. Gå gjennom hvert trinn i delen [Feilsøk](#troubleshoot) i denne artikkelen, og rett oppsettet etter behov. Hvis avgiftsgruppen og avgiftsgruppen for vare ikke er riktig bestemt, kan du se [Ingen samsvarsresultater blir funnet](tcs-troubleshooting-no-matching-result.md).
2. Hvis det ikke er noe kryss for avgiftsgruppen og avgiftsgruppen for vare, oppretter du en ny funksjonsversjon i RCS og ordner oppsettet.

    - Gå til **Avgiftsfunksjoner** \> **Avgiftskoder og -grupper** > **Avgiftsgruppe for vare**.

        | Avgiftsgruppe for linjevare | Mva-koder |
        |---------------------|-----------|
        | Gruppe B             | A,B       |

    Avgiftskoden bestemmes som **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
