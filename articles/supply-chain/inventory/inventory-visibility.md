---
title: Oversikt over tillegget for lagersynlighet
description: Dette emnet beskriver hva lagersynlighet er, og beskriver funksjonene i det.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dfc1bc0d457d0b0b2632aa2e2e5ba6a3c2f3fae7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575177"
---
# <a name="inventory-visibility-add-in-overview"></a>Oversikt over tillegget for lagersynlighet

[!include [banner](../includes/banner.md)]

Tillegget for lagersynlighet (også referert til som *Lagersynlighet*), er en uavhengig og høyt skalerbar mikrotjeneste som aktiverer beholdningssporing i sanntid. Det har derfor en global visning av lageret.

Eksterne systemer får tilgang til tjenesten via RESTful API-er. På den måten kan de enten utføre spørringer på lagerbeholdningsinformasjon på gitte sett med dimensjoner, eller foreta endringer i lageret i forskjellige tilpassede datakilder.

Som en mikrotjeneste som er bygd på Microsoft Dataverse, er det mulig å utvide Lagersynlighet. Du kan bruke Power Apps til å bygge apper. Du kan også bruke Power BI til å tilby tilpasset funksjonalitet som oppfyller dine forretningskrav.

Du kan integrere lagersynligheten med flere tredjepartssystemer ved å angi konfigurasjonsalternativer for standardiserte lagerdimensjoner og definere transaksjonstyper. Lagersynlighet støtter også tilpasset utvidelse gjennom konfigurerbare beregnede antall.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Integrering av lagersynlighet med Dynamics 365 Supply Chain Management

Den integrerte løsningen henter lagerdata fra Dynamics 365 Supply Chain Management og sporer lagerendringer kontinuerlig. Hvis du vil ha mer informasjon, kan du se [Installere og definere lagersynlighet](inventory-visibility-setup.md) og [Konfigurere lagersynlighet](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Få en global visning av lager

Med den integrerte løsningen kan du definere dine egne datakilder og sentralisere lagerdata. Hvis du vil ha mer informasjon, kan du se [Konfigurere Lagersynlighet](inventory-visibility-configuration.md).

Det er to måter å vise lageret på:

- Send inn en spørring via API-en med høy ytelse. Denne API-en kan returnere lagerdata i sanntid direkte fra en hurtigbufret forekomst. Du finner kontrakter og eksempler i [offentlige API-er for lagersynlighet](inventory-visibility-api.md).
- Vis råvarelisten. Denne listen synkroniseres periodisk fra en hurtigbufret forekomst, og vises i Dataverse. Hvis du vil ha mer informasjon, kan du se [App for lagersynlighet](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Ikke-forpliktende reservasjoner

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Ikke-forpliktende reservasjon gjelder når en virksomhet må reservere et bestemt antall produkter som skal støttes, for eksempel innfrielse av salgsordrer, som unngår oversalg. Når en salgsordre opprettes og bekreftes i Supply Chain Management eller andre ordrestyringssystemer, sendes det en forespørsel om å reservere antallet til Lagersynlighet. Med Lagersynlighet kan du reservere produkter som har dimensjonsdetaljer og bestemte lagertransaksjonstyper. (Hvis du vil ha mer informasjon, kan du se [Appen Lagersynlighet](inventory-visibility-power-platform.md).) Når antallet er reservert, returneres en reservasjons-ID. Du kan bruke denne reservasjons-ID-en til å koble tilbake til den opprinnelige ordren i Supply Chain Management eller andre ordrestyringssystemer.

Funksjonaliteten er utformet slik at en reservasjon i Lagersynlighet ikke endrer det totale antallet. I stedet flagger den bare det reserverte antallet. (Av denne grunnen kalles dette for en *ikke-forpliktende reservasjon*.) Det ikke-forpliktende reserverte antallet kan motposteres når produktene forbrukes i Supply Chain Management eller et tredjepartssystem, ved å kalle API-en på nytt for å gjøre et antallsfratrekk og oppdatere det totale antallet i Lagersynlighet. Hvis du vil ha mer informasjon, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
