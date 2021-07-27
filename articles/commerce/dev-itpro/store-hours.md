---
title: Opprette og oppdatere åpningstid
description: Dette emnet beskriver hvordan du oppretter og oppdaterer åpningstid i Commerce Headquarters.
author: josaw1
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 6d8c1d4e7edc4b83e2489ac6a0bad18ab55c042b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348248"
---
# <a name="create-and-update-store-hours"></a>Opprette og oppdatere åpningstid

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Oversikt

Fra ett sted kan forhandlere opprette, vedlikeholde og administrere åpningstiden for forskjellige butikker i ulike geografiske områder. Åpningstiden kan deretter vises på salgsstedsterminalene. På denne måten kan kasserere dele åpningstiden med kunder og hjelpe dem som er interessert i varer i andre butikker. Åpningstiden kan også skrives ut på kvitteringer, i tilfelle kunder ønsker å gå tilbake til butikken senere.

Flere åpningstider kan konfigureres på tvers av ulike kanaler. Disse kanalene omfatter fysiske butikker, telefonsentre, mobile enheter og e-handel-områder.

Hvis en kunde har en plukkordre for en annen butikk, kan kassereren velge datoer som plukkingen skal være tilgjengelig på, i denne butikken. Butikkoppslaget vil inneholde en referanse til datoene og åpningstiden. Kassereren kan velge en dato og et sted, og kan også skrive ut en hentekvittering som inneholder åpningstiden.

Denne funksjonen er tilgjengelig i Microsoft Dynamics 365 Retail versjon 8.1.2 og senere.

## <a name="configure-store-hours"></a>Konfigurere åpningstid

Hvis du vil konfigurere åpningstid, gjør du følgende:

1. Gå til **Retail og Commerce** \> **Kanaloppsett** \> **Åpningstid**.
2. Velg **Ny** for å opprette en ny mal for åpningstid. Hvis du vil bruke en eksisterende mal, velger du malen i den venstre ruten.
3. I dialogboksen **Legg til område** definerer du datoområdet, åpningstiden og eventuelle helligdager.

    - Hvis åpningstiden ikke endres, velger du **Slutter ikke** i feltet **Sluttdato**.
    - Hvis åpningstiden gjelder en bestemt måned, uke eller dag, angir du de aktuelle datoene i feltene **Startdato** og **Sluttdato**.

    > [!NOTE]
    > Du kan opprette flere maler som har overlappende start- og sluttdatoer. Derfor kan du for eksempel definere åpningstid for butikker i forskjellige tidssoner.

    ![Dialogboksen Legg til område.](../dev-itpro/media/Storehours1.png "Dialogboksen Legg til område")

4. Knytt åpningstidsmalen til butikkene der den skal brukes. I dialogboksen **Velg organisasjonsnoder** velger du butikkene, områdene og organisasjonene som malen skal knyttes til.

    - Bare én åpningstidsmal kan knyttes til hver butikk.
    - Bruk pilknappene til å velge butikker, områder eller organisasjoner. Kalenderen vil være tilgjengelig for butikkene eller butikkgruppene, og den vil være synlig på salgsstedet for referanse.

    ![Dialogboksen Velg organisasjonsnoder.](../dev-itpro/media/Storehours2.png "Dialogboksen Velg organisasjonsnoder")

5. På siden **Distribusjonsplan** kjører du jobbene **1070** og **1090** for å gjøre åpningstiden tilgjengelig for salgsstedet.

## <a name="add-store-hours-to-printed-receipts"></a>Legge til åpningstid på utskrevne kvitteringer

Følg disse trinnene for å legge til åpningstid på utskrevne salgsstedskvitteringer.

1. Åpne kvitteringsutformingen.
2. Velg **Bunntekst** i hjørnet nederst til venstre.
3. Dra elementet **Åpningstid** fra venstre rute til bunnteksten nederst i kvitteringsmalen.
4. Du kan redigere standardetiketten på **Åpningstid**-elementet etter behov.
5. Lagre kvitteringen, og lukk kvitteringsutformingen.
6. På siden **Distribusjonsplan** kjører du jobbene **1070** og **1090**.
7. Logg på salgsstedet.
8. Fullfør et salg, og velg å skrive ut en kvittering.

Salgsstedskvitteringer inneholder nå åpningstid. Hvis helligdager er inkludert i malen, vises de på kvitteringen.

![Kvitteringseksempel.](../dev-itpro/media/Storehours3.png "Kvitteringseksempel")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]