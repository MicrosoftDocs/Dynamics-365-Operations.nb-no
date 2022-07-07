---
title: Opprette en bestilling som styres av budsjett
description: Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016195"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Opprette en bestilling som styres av budsjett

[!include [banner](../../includes/banner.md)]

Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.

## <a name="review-the-budget-control-configuration"></a>Gå gjennom budsjettkontrollkonfigurasjonen

1. Gå til **Budsjettering > Oppsett > Budsjettkontroll > Budsjettkontrollkonfigurasjon**.
1. Velg fanen **Budsjettmidler tilgjengelig**.
1. Velg fanen **Dokumenter og journaler**.
1. Velg fanen **Definer budsjettkontrollregler**.
1. Velg fanen **Definer budsjettgrupper**.
1. Lukk siden.

## <a name="create-a-purchase-order"></a>Opprette en bestilling

1. Gå til **Innkjøp og leverandører > Bestillinger > Alle bestillinger**.
1. Velg **Ny**.
1. Angi eller velg en verdi i **Leverandørkonto**-feltet.
1. Vis hurtigfanen **Generelt**.
1. Angi datoen i feltet **Regnskapsdato**.
1. Velg **OK** for å lukke dialogboksen og åpne den nye bestillingen.
1. Velg **Legg til linje** på verktøylinjen i hurtigfanen **Bestillingslinjer** for å legge til en ny linje, og fyll deretter ut linjen etter behov for å legge til en vare i ordren.
1. Velg **Finans \> Fordel beløp** på verktøylinjen i hurtigfanen **Bestillingslinjer**.
1. Angi en konto i **Finanskonto**-feltet.
1. Lukk siden.

## <a name="perform-budget-checking"></a>Utfør budsjettkontroll

1. Fortsett å arbeide med bestillingen du nettopp la til en linje i.
1. Velg **Finans \> Utfør budsjettkontroll** på verktøylinjen i hurtigfanen **Bestillingslinjer**.
1. Velg **Finans \> Feil eller advarsler for budsjettkontroll** på verktøylinjen i hurtigfanen **Bestillingslinjer**.
1. Dialogboksen **Feil eller advarsler for budsjettkontroll** åpnes. Sjekk resultatene av kontrollen, og velg deretter **Lukk** for å lukke dialogboksen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]