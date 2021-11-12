---
title: Datoer for leverandørfaktura
description: Dette emnet beskriver datoene som vises på leverandørfakturaer. Det forklarer også hvordan du konfigurerer systemet slik at posteringsdatoen justeres automatisk.
author: sunfzam
ms.date: 08/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: a066f828b47f297b8ad520b9eb0f4f311d49b111
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647904"
---
# <a name="vendor-invoice-dates"></a>Datoer for leverandørfaktura

[!include [banner](../includes/banner.md)]

Dette emnet beskriver datoene som vises på leverandørfakturaer. Det forklarer også hvordan du konfigurerer systemet slik at posteringsdatoen justeres automatisk.

På siden for **detaljer om ventende leverandørfakturaer** viser fakturahodet fire datoer: mottatt fakturadato, fakturadato, posteringsdato og forfallsdato. Når det opprettes en leverandørfaktura, angis følgende datoer som standard:

- **Mottatt fakturadato** – Dette feltet er satt til gjeldende systemdato.
- **Posteringsdato** – Dette feltet er satt til gjeldende systemdato. 
- **Forfallsdato** – Datoen i dette feltet beregnes på grunnlag av posteringsdatoen og betalingsbetingelsene.
- **Fakturadato** – Som standard er dette feltet tomt. Du kan imidlertid angi en verdi etter behov. I dette tilfellet beregnes **Forfallsdato**-feltet på nytt på grunnlag av fakturadatoen og betalingsbetingelsene.

Noen ganger kan en leverandørfaktura være i ventende tilstand i lang tid etter at perioden er avsluttet. Når postering er klar, brukes den gamle posteringsdatoen for den tidligere posteringsperioden fremdeles. Perioden er imidlertid nå lukket. Derfor må en AP-ekspeditør manuelt endre alle posteringsdatoene til den nye posteringsperioden for alle ventende fakturaer som allerede er opprettet.

Ved hjelp av funksjonen som beskrives i dette emnet, kan du konfigurere systemet slik at posteringsdatoen justeres automatisk i henhold til forretningskravene.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parameter for automatisk justering av posteringsdato for leverandørfaktura

Følg denne fremgangsmåten for å aktivere systemet for automatisk justering av posteringsdatoen for leverandørfakturaer.

1.  Gå til **Leverandører \> Oppsett \> Leverandørparametere**.
2.  Velg en av følgende verdier i fanen **Finans og merverdiavgift** i feltet **Juster posteringsdato automatisk**:

    - **Ingen endring** – Systemet endrer ikke automatisk posteringsdatoen under posteringen. Denne verdien er valgt som standard.
    - **Endre alltid posteringsdatoen til systemdato** – Systemet endrer automatisk posteringsdatoen til systemdatoen under postering.
    - **Endre posteringsdato til systemdato når posteringsdatoperioden er lukket eller på vent** – Systemet endrer posteringsdatoen til systemdatoen under postering, men bare hvis den tilsvarende perioden for posteringsdatoen har statusen **Lukket** eller **På vent**.
    - **Endre posteringsdato til den første dagen i den nye perioden når posteringsdatoperioden er lukket eller på vent** – Systemet endrer posteringsdatoen til den første dagen i den nye perioden, men bare hvis den tilsvarende perioden for posteringsdatoen har statusen **Lukket** eller **På vent**.

## <a name="impact-of-posting-date-changes"></a>Virkningen av posteringsdatoendringer

Når posteringsdatoen på en ventende leverandørfaktura endres, har endringen følgende virkning:

- **Forfallsdato**

    - Hvis **Forfallsdato**-feltet er tomt, beregnes forfallsdatoen på nytt på grunnlag av den nye posteringsdatoen og betalingsbetingelsene.
    - Hvis **Fakturadato**-feltet tidligere er angitt, påvirker ikke endringen av posteringsdatoen forfallsdatoen.

- **Kontantrabattdato**

    - Hvis **Fakturadato**-feltet er tomt, brukes den nye posteringsdatoen til å beregne kontantrabatten.
    - Hvis **Fakturadato**-feltet er angitt tidligere, er ikke kontantrabatten endret.

- **Valutakurs** – Valutakursen bestemmes av innstillingen i alternativet **Oppdater leverandørregnskap ved hjelp av fakturadatoen** i **Faktura**-fanen på siden **Leverandørparametere** (**Leverandører \> Oppsett \> Leverandørparametere**).

    - Hvis du setter alternativet til **Ja**, brukes fakturadatoen, og posteringsdatoendringen påvirker ikke valutakursen.
    - Hvis du setter dette alternativet til **Nei**, brukes posteringsdatoen til å beregne valutakursen. Når posteringsdatoen oppdateres, beregnes regnskaps- og rapporteringsbeløpene på nytt. Samsvarsvalideringen må derfor utføres på nytt.

## <a name="validation"></a>Validering

To andre felt i **Faktura**-fanen på siden **Leverandørparametere** (**Leverandører \> Oppsett \> Leverandørparametere**) påvirker fakturabehandling:

- Hvis feltet **Kontroller fakturanummeret som brukes** er satt til **Avvis duplikater i regnskapsåret**, bruker systemet posteringsdatoen til å kontrollere om det finnes dupliserte fakturaer under fakturapostering.
- Hvis alternativet **Krev dokumentdato på leverandørfaktura** er satt til **Feil**, kreves feltet **Fakturadato på ventende fakturahode**. Hvis fakturadatoen er senere enn posteringsdatoen, viser systemet en feilmelding.
