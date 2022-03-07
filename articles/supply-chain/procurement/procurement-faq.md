---
title: Vanlige spørsmål om innkjøp
description: Dette emnet gir svar på vanlige spørsmål om innkjøpsfunksjonaliteten til Supply Chain Management
author: kamaybac
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 09c99b88bc47609158805cdba1291ae462cda178
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477149"
---
# <a name="procurement-faq"></a>Vanlige spørsmål om innkjøp

[!include [banner](../includes/banner.md)]

Dette emnet gir svar på vanlige spørsmål om innkjøpsfunksjonaliteten til Supply Chain Management.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kan jeg bare vise bestillinger som jeg har opprettet?

Denne funksjonen er ikke tilgjengelig nå.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kan jeg reservere lager og opprette transaksjoner mot registrert lager i en bestilling?

### <a name="issue-description"></a>Problembeskrivelse

Selv når varene er i en *Registrert*-tilstand på en bestilling, kan du likevel reservere lageret. Du kan med andre ord opprette transaksjoner mot det registrerte lageret.

### <a name="reproduce-the-issue"></a>Reprodusere problemet

Følgende prosedyre viser én måte å reprodusere problemet på.

1. Opprett en bestilling.
2. Registrere bestillingslinjen.
3. Legg merke til at du kan generere reservasjoner eller transaksjoner mot det registrerte lageret.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard. Forventningen er at de registrerte varene fysisk har ankommet på lageret, og at de derfor er tilgjengelige for reservasjon.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kan jeg finne brukeren som annullerte en bestilling?

Denne informasjonen spores bare hvis bestillingen er underlagt endringsstyring. Hvis du bruker endringsstyring, kan du se hvem som sendte inn endringen (annulleringen), og hvem som godkjente den.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Hvorfor kan jeg ikke koble en innkjøpsavtale til en eksisterende bestilling?

En kjøpsavtale må knyttes til en bestilling når bestillingen opprettes. Hvis ikke kan ikke bestillingslinjer knyttes til kjøpsavtalelinjer.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Hvilken kontroll utløser meldingen "Oppdater priser og rabatter som er angitt manuelt eller eksternt dokument"?

Når du endrer leveringsdatoen, kan du få en melding om å oppdatere priser og rabatter som er angitt manuelt, eller eksternt dokument. Du får denne meldingen fordi hvis leveringsdatoen endres, kan en annen handels- eller salgsavtale utløses og føre til en prisendring. En endring i forsendelsesdatoen kan også ha innvirkning på lagerplanene og annen relatert informasjon.

Meldingen utløses når en av datoene eller en annen parameter endres. Formålet med meldingen er å sørge for at du kjenner til prisendringer som kan forekomme på grunn av endringene.

Meldingen er anmodningen om evaluering av forretningsavtale (TAE). Hvis du vil ha en fullstendig beskrivelse, se [Evalueringspolicyer for forretningsavtale](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Hvorfor kan jeg ikke postere mer enn én faktura for en bestillingslinje som har kategoribaserte varer?

Et antall er obligatorisk hvis du vil postere fakturaer. Hvis hele antallet av en linje er fakturert bare for et delvis beløp, kan du fakturere restbeløpet på en annen faktura.
