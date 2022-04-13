---
title: 'Veiledning: Endre en behovsprognose manuelt'
description: Dette emnet viser hvordan du endrer prognosen for en vare.
author: t-benebo
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e5030bf97bee8dc475f22473ecc87e900298b6f
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469413"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Veiledning: Endre en behovsprognose manuelt

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du endrer prognosen for en vare. Denne fremgangsmåten er ment for produksjonsplanleggeren.

## <a name="modify-the-forecast-for-a-selected-item"></a>Endre prognosen for en utvalgt vare

Slik endrer du prognosen for en utvalgt vare:

1. Gå til **Moduler \> Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Finn og velg ønsket post i listen. Velg varen du vil endre prognosen for.
1. Åpne Kategorien **Plan** i handlingsruten, og velg **Behovsprognose**.
1. Velg en rad i listen. Hvis det ikke finnes noen prognoselinjer, kan du opprette en ny linje ved å velge **Ny** i handlingsruten.  
1. Angi et positivt tall i **Salgsantall**-feltet. Dette tallet representerer det prognoseberegnede antallet for varen. Det vises en feil hvis du angir et negativt tall.
1. Fyll ut de andre feltene etter behov.
1. Velg **Lagre** i handlingsruten.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Endre prognosen for én eller flere varer med Microsoft Excel

Slik endrer du prognosen for én eller flere varer med Microsoft Excel:

1. Gjør ett av følgende:
    - Åpne **Behovsprognose**-siden for en hvilken som helst vare (det spiller ingen rolle hvilken), som beskrevet i forrige del.
    - Gå til **Hovedplanlegging \> Prognose \> Manuell prognoseregistrering \> Behovsprognoselinjer**.
1. I handlingsruten velger du **Åpne i Microsoft Office \> Behovsprognoseoppføringer**.
1. Velg en nedlastingsplassering, lagre og åpne deretter den nedlastede filen i Excel.
1. Hvis du får en advarsel, velger du **Aktiver redigering**.
1. I Excel logger du deg på Supply Chain Management ved å bruke oppgaveruten i Microsoft Dynamics. Du må logge på med alternativet **La meg være pålogget** aktivert, og du må klarere datatilkoblingsappen.
1. Excel-regnearket viser nå alle gjeldende behovsprognoselinjer for firmaet.  Du kan legge til, slette og redigere behovsprognoselinjer etter behov.
1. Velg **Publiser** i Microsoft Dynamics-oppgaverute for å laste opp endringene tilbake til Supply Chain Management.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
