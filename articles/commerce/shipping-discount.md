---
title: Leveringsrabatt
description: Denne artikkelen beskriver funksjoner for leveringsrabatter i Microsoft Dynamics 365 Commerce og oppsettet som kreves for å bruke dem.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: 74cfe5246ad72cbdedd0ed4e3b3394bf7277919e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473857"
---
# <a name="shipping-discount"></a>Leveringsrabatt

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver funksjoner for leveringsrabatter i Microsoft Dynamics 365 Commerce og oppsettet som kreves for å bruke dem.

Gratis eller rabattert forsendelse er en faktor som påvirker kundenes kjøpsavgjørelser på nettet. For å øke inntekten per transaksjon bruker mange forhandlere en gratis forsendelsesfordel for å motivere kundene til å øke handlekurvstørrelsen.

Commerce støtter en forsendelsesrabattfunksjon som gjør det mulig for forhandlerne å konfigurere en rabattprosent på forsendelseskostnadene for en bestemt forsendelsesmetode når det totale salgsbeløpet for kvalifiserte varer i transaksjonen oppfyller bestemte kriterier. Et eksempel på et scenario som bruker funksjonen for forsendelsesrabatt, er «Bruk $ 50 eller mer til å få gratis frakt over natten».

## <a name="prerequisites"></a>Forutsetninger

Funksjoner for forsendelsesrabatt støttes av Commerce-funksjonene for [avanserte automatiske gebyrer for omnikanal](/dynamics365/unified-operations/retail/omni-auto-charges). Hvis du vil at forsendelsesrabattfunksjonene skal fungere, må du aktivere **Bruk avanserte automatisk tillegg** i fanen **Kundeordrer** på siden **Commerce-parametere** i Commerce headquarters. Forhandlere kan bruke funksjonen for avanserte automatiske gebyrer til å definere ulike typer tillegg, for eksempel håndtering, installasjon og avhending.

Forsendelsesrabattene brukes bare på forsendelseskostnader. Derfor må en forhandler angi hvilke gebyrer som er forsendelseskostnadene. Hvis du vil angi forsendelsesgebyrer, kan du gå til **Kanaloppsett \> Tillegg \> Tilleggskoder** i Commerce headquarters og angi alternativet **Forsendelsestillegg** til **Ja** for de ønskede tilleggene.

![Angivelse av et gebyr som en forsendelseskostnad.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Konfigurasjon

Funksjonen for forsendelsesrabatt er lagbasert og støtter bare beregningstypen **Rabattprosent**. Hvis du vil definere en forsendelsesrabatt, går du til **Priser og rabatter \> Forsendelsesterskelrabatt** i Commerce headquarters. Du kan deretter angi leveringsmåten rabatten gjelder, definere en eller flere beløpsterskler og angi rabattprosenten for hver terskel. Du kan også konfigurere en liste over kategorier eller produkter som kvalifiserte varer. På den måten vil bare salgsbeløpet mot varene i en transaksjon telles når prissettingsmotoren evaluerer om totalbeløpet for transaksjonen når terskelen.

> [!NOTE]
> I motsetning til andre rabattyper oppretter ikke forsendelsesrabatten rabattlinjer. I stedet redigerer den direkte forsendelseskostnaden og legger til navnet på rabatten i beskrivelsen av tillegget.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
