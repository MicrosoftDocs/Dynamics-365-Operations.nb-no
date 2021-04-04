---
title: Avgifter på elektroniske ordrer beregnes feil
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe når avgifter på nettordrer beregnes feil, eller når mva-gruppen på salgslinje ikke er riktig angitt.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585461"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Avgifter på elektroniske ordrer beregnes feil

[!include [banner](../../includes/banner.md)]

Dette emnet gir feilsøkingsveiledning som kan hjelpe når avgifter på nettordrer beregnes feil, eller når mva-gruppen på salgslinje ikke er riktig angitt.

## <a name="description"></a>beskrivelse

Når en e-handelsordre blir lagt inn, blir avgiftene feil beregnet, eller mva-gruppen på salgslinjen er feil angitt.

## <a name="resolution"></a>Oppløsning

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Konfigurere merverdiavgift for en detaljhandelsbutikk i Commerce Headquarters

Hvis du vil konfigurere merverdiavgift for en detaljhandelsbutikk i Commerce Headquarters, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Kanaler \> Alle butikker**.
1. Velg butikken du skal konfigurere merverdiavgift for.
1. I hurtigfanen **Generelt** konfigurerer du mva-inforamsjonen for butikken i delen **Merverdiavgift**.

> [!NOTE]
> For produkthenting fra en butikk kommer mva-gruppen fra butikken som er valgt for henting. Du finner mer informasjon under [Angi andre mva-alternativer for butikker](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Konfigurere merverdiavgift for en kundes adresse i Commerce Headquarters

Hvis du vil konfigurere merverdiavgift for en kundes adresse i Commerce Headquarters, gjør du følgende.

1. Gå til **Kunder \> Kunder \> Alle kunder**.
1. Velg kunden du skal konfigurere merverdiavgift for.
1. I hurtigfanen **Adresser** velger du adressen du vil konfigurere merverdiavgift for, velger **Flere alternativer**, og velger deretter **Avansert**.
1. I hurtigfanen **Generelt** velger du **Mva-gruppe**.
1. I feltet **Merverdiavgift** velger du den riktige verdien.

> [!NOTE]
> For forsendelse som omfatter merverdiavgift på kundens adresse, bestemmer leveringsadressen for linjen mva-gruppen for linjen. Hvis kunden sender til en eksisterende adresse som har en mva-gruppe som allerede er konfigurert, vil den eksisterende avgiftsgruppen bli brukt. Som standard har ikke adresser noen mva-gruppe når de opprettes.

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Konfigurere generelle mva-grupper i Commerce Headquarters

Hvis du vil konfigurere generelle mva-grupper i Commerce Headquarters, gjør du følgende.

1. Gå til **Avgift \> Indirekte avgifter \> Merverdiavgift \> Mva-gruppe**.
1. Velg mva-gruppen du vil konfigurere, til venstre.
1. Konfigurer avgiftene for mva-gruppen i hurtigfanen **Destinasjonsbasert avgift for detaljhandel**.

> [!NOTE]
> For forsendelse som ikke innbærer merverdiavgift på kundens adresse, bestemmer leveringsadressen for linjen og de destinasjonsbaserte avgiftene som er konfigurert for mva-gruppen, mva-gruppen. Hvis du vil ha mer informasjon, kan du se [Definere avgifter for nettbutikker basert på destinasjon](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere merverdiavgift for elektroniske ordrer](../sales-tax-config.md)