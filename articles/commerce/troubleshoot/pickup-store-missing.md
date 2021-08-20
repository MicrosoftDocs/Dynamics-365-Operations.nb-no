---
title: Detaljhandelsbutikk vises ikke i listen over butikker å hente fra
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en detaljhandel ikke vises i listen over butikker der varer kan hentes.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6ccd60082b65fdbd47fef4a67ba269d7d7afc04679647d3eb8d2a5e9c21a19b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762626"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Detaljhandelsbutikk vises ikke i listen over butikker å hente fra

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en detaljhandel ikke vises i listen over butikker der varer kan hentes.

## <a name="description"></a>beskrivelse

En butikk vises ikke i listen over butikker der varer kan hentes.

## <a name="resolution"></a>Oppløsning

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Konfigurere lengde- og breddegrad for butikkadressen i Commerce Headquarters

Hvis du vil konfigurere lengde- og breddegrad for butikkadressen i Commerce Headquarters, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Kanaler \> Butikker \> Alle butikker**.
1. Finn butikken du vil skal vises blant hentealternativene på e-handelsområdet. Noter deg verdien for **Driftsenhetsnummer**.
1. Gå til **Organisasjonsstyring \> Organisasjoner \> Driftsenheter**.
1. Søk etter operasjonsnummeret du noterte deg tidligere, og velg deretter driftsenheten i søkeresultatene.
1. Velg **Flere alternativer** i hurtigfanen **Adresser**, og velg deretter **Avansert**.
1. Kontroller at faltene **Lengdegrad** og **Breddegrad** er riktig angitt i hurtigfanen **Generelt**. Som et ledd i dette trinnet må du kontrollere at verdiene er riktig angitt som positive eller negative tall.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Konfigurere oppfyllelsesgrupper i Commerce Headquarters

Hvis du vil konfigurere oppfyllelsesgrupper i Commerce Headquarters, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Kanaler \> Nettbutikker**.
1. Velg nettbutikken du vil konfigurere.
1. Velg **Konfigurer** i handlingsruten, og velg deretter **Tilordning for oppfyllelsesgruppe**.
1. På siden **Tilordning for oppfyllelsesgruppe** velger du oppfyllelsesgruppen for nettbutikken.
1. Under **Oppsett** kontrollerer du at detaljhandelen er riktig konfigurert for oppfyllelsesgruppen.

## <a name="additional-resources"></a>Tilleggsressurser 

[Opprette en driftsenhet](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Konfigurere en nettkanal](../channel-setup-online.md)