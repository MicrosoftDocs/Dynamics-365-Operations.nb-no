---
title: Datoer for leverandørfaktura
description: Denne artikkelen beskriver datoene som vises på leverandørfakturaer. Det forklarer også hvordan du justerer posteringsdatoen automatisk.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775279"
---
# <a name="vendor-invoice-dates"></a>Datoer for leverandørfaktura

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver datoene som vises på leverandørfakturaer. Det forklarer også hvordan du justerer posteringsdatoen automatisk.

På siden for **ventende leverandørfakturaer** viser fakturahodet fire datoer: **Dato for mottatt faktura**, **Fakturadato**, **Posteringsdato** og **Forfallsdato**. Når det opprettes en leverandørfaktura, angis følgende datoer som standard:

- **Mottatt fakturadato** – Dette feltet er satt til gjeldende systemdato.
- **Posteringsdato** – Dette feltet er satt til gjeldende systemdato. 
- **Forfallsdato** – Datoen i dette feltet beregnes på grunnlag av posteringsdatoen og betalingsbetingelsene.
- **Fakturadato** – Som standard er dette feltet tomt. Du kan imidlertid angi en verdi etter behov. I dette tilfellet beregnes **Forfallsdato**-feltet på nytt på grunnlag av fakturadatoen og betalingsbetingelsene.

Noen ganger kan en leverandørfaktura være i ventende tilstand i lang tid etter at perioden er avsluttet. Når postering er klar, brukes den gamle posteringsdatoen for den tidligere posteringsperioden fremdeles. Perioden er imidlertid nå lukket. Derfor må en AP-ekspeditør manuelt endre alle posteringsdatoene til den nye posteringsperioden for alle ventende fakturaer som allerede er opprettet.

Ved hjelp av funksjonen som beskrives i denne artikkelen, kan du justere posteringsdatoen automatisk i henhold til forretningskravene.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parameter for automatisk justering av posteringsdato for leverandørfaktura

Følg denne fremgangsmåten for å justere posteringsdatoen for leverandørfakturaer automatisk.

1.  Gå til **Leverandører \> Oppsett \> Leverandørparametere**.
2.  Velg en av følgende verdier i fanen **Finans og merverdiavgift** i feltet **Juster posteringsdato automatisk**:

    - **Ingen endring** – Systemet endrer ikke automatisk posteringsdatoen under posteringen. Denne verdien er valgt som standard.
    - **Endre alltid posteringsdatoen til systemdato** – Posteringsdatoen endres automatisk til systemdatoen under postering.
    - **Endre posteringsdato til systemdato når posteringsdatoperioden er lukket eller på vent** – Posteringsdatoen endres automatisk til systemdatoen under postering, men bare hvis den tilsvarende perioden for posteringsdatoen har statusen **Lukket** eller **På vent**.
    - **Endre posteringsdato til den første dagen i den nye perioden når posteringsdatoperioden er lukket eller på vent** – Posteringsdatoen endres til den første dagen i den nye åpne perioden, men bare hvis den tilsvarende perioden for posteringsdatoen har statusen **Lukket** eller **På vent**.

> [!NOTE]
> Hvis den nye posteringsdatoen som ble justert automatisk, er i et nytt regnskapsår, blir ikke posteringsdatoen for fakturaen oppdatert. Brukeren får feilmeldingen «Regnskapsåret er endret. Kontroller og angi posteringsdatoen på nytt.» Posteringsdatoen for faktura må oppdateres til den nye datoen for regnskapsår for at posteringen skal kunne utføres.

## <a name="impact-of-posting-date-changes"></a>Virkningen av posteringsdatoendringer

Når posteringsdatoen på en ventende leverandørfaktura endres, har endringen følgende virkning:

- **Forfallsdato**

    - Hvis **Forfallsdato**-feltet er tomt, beregnes forfallsdatoen på nytt på grunnlag av den nye posteringsdatoen og betalingsbetingelsene.
    - Hvis **Fakturadato**-feltet tidligere er angitt, påvirker ikke endringen av posteringsdatoen forfallsdatoen.

- **Kontantrabattdato**

    - Hvis **Fakturadato**-feltet er tomt, brukes den nye posteringsdatoen til å beregne kontantrabatten.
    - Hvis **Fakturadato**-feltet er angitt tidligere, er ikke kontantrabatten endret.

- **Valutakurs** – Valutakursen bestemmes av innstillingen i alternativet **Oppdater leverandørregnskap ved hjelp av fakturadatoen** i **Faktura**-fanen på siden **Leverandørparametere** (**Leverandører \> Oppsett \> Leverandørparametere**).

    - Hvis du setter alternativet til **Ja**, brukes **Fakturadato**, og **Posteringsdato**-endringen påvirker ikke valutakursen.
    - Hvis du setter dette alternativet til **Nei**, brukes posteringsdatoen til å beregne valutakursen. Når posteringsdatoen oppdateres, beregnes regnskaps- og rapporteringsbeløpene på nytt. Samsvarsvalideringen må derfor utføres på nytt.

## <a name="validation"></a>Validering

To andre felt i **Faktura**-fanen på siden **Leverandørparametere** (**Leverandører \> Oppsett \> Leverandørparametere**) påvirker fakturabehandling:

- Hvis feltet **Kontroller fakturanummeret som brukes** er satt til **Avvis duplikater i regnskapsåret**, bruker systemet posteringsdatoen til å kontrollere om det finnes dupliserte fakturaer under fakturapostering.
- Hvis alternativet **Krev dokumentdato på leverandørfaktura** er satt til **Feil**, kreves feltet **Fakturadato på ventende fakturahode**. Hvis fakturadatoen er senere enn posteringsdatoen, vises en feilmelding.
