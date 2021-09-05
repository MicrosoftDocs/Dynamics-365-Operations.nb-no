---
title: Opprette et dataintegreringsprosjekt
description: Dette emnet forklarer hvordan du oppretter et dataintegratorprosjekt.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: b08af906c18f6c0790ca56c69a833733f48cd88c
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386368"
---
# <a name="create-a-data-integrator-project"></a>Opprette et dataintegreringsprosjekt

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter et dataintegratorprosjekt.

1. Logg på Microsoft Dynamics 365 Finance.
2. Gå til **Arbeidsområder \> Databehandling**, og velg **Dataenheter**. Vent til alle dataenhetene er oppdatert før du går videre til neste trinn.
3. Åpne [Power Apps-portalen](https://make.powerapps.com/), og følg denne fremgangsmåten:

    1. Velg det aktuelle miljøet.
    2. Velg **Data \> Tilkoblinger** i venstre navigasjonsrute.
    3. Koble til riktige forekomster av følgende elementer:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. Åpne [Power Apps-miljøene](https://admin.powerapps.com/environments), og følg denne fremgangsmåten:

    1. Velg **Dataintegrator**.
    2. Velg **Tilkoblingssett**.
    3. Velg **Nytt tilkoblingssett**.
    4. Skriv inn et navn for tilkoblingen.
    5. Velg de riktige tilkoblingene for følgende elementer:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. Velg den aktuelle organisasjonstilordningen.
    7. Velg **Opprett**.

5. Åpne [Power Apps-miljøene](https://admin.powerapps.com/environments), og følg denne fremgangsmåten:  

    1. Opprett dataintegrasjonsprosjekter for følgende maler ved hjelp av tilkoblingssettet du nettopp opprettet:

        - Resultater av innsikt i kundebetaling (CDS til Fin and Ops)
            - Hvis du bruker versjon 10.0.17 eller senere, må du bruke malen med navnet Resultater av innsikt i kundebetaling (CDS til Fin and Ops 10.0.17+).
        - Resultater av tidsserie for kontantstrøm (CDS til Fin and Ops)
        - Resultater av tidsserie for budsjett (CDS til Fin and Ops)

    2. Angi den riktige planleggingen for hvert prosjekt.

> [!NOTE]
> Hvis du ikke ser de nødvendige enhetene i CDS, kan du gå til **Kreditt og innkreving > Oppsett > Finance Insights > Parametere for økonomisk innsikt**, aktivere funksjonen for kundebetalingsprognoser og klikke på knappen **Opprett prognosemodell**. Når distribusjonen av modell for kunstig intelligens er fullført (vellykket eller mislykket), vil CDS-enhetene som kreves for å opprette integrering, bli distribuert i CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
