---
title: Behandle kundeordrehentinger på salgssted
description: Denne artikkelen beskriver funksjonaliteten som er tilgjengelig i salgsstedsprogrammet (POS) for behandling av henting av kundeordrer.
author: Hhainesms
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0a886f156fff96f3b7e6026c405d3c8700d57f62
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910475"
---
# <a name="process-customer-order-pickups-in-pos"></a>Behandle kundeordrehentinger på salgssted

[!include [banner](includes/banner.md)]

Når det opprettes en [kundeordre](customer-orders-overview.md) for henting i butikk, kan en butikkbruker bruke salgsstedsprogrammet til å starte henting på lageret. Salgsstedet kjører den endelige betalingsregistreringen etter behov. Det vil også fullføre lageret og den økonomiske posteringen for antallene som er hentet.

Hvis du er butikkbruker, kan du utføre hentingen ved å bruke **Tilbakekall ordre**-operasjonen eller **Ordreoppfyllelse**-operasjonen på salgsstedet. Hvis du vil **Hent**-operasjonen tilgjengelig, må du først følge ett av disse trinnene:

- Hvis du vil bruke **Tilbakekall ordre**-operasjonen, søker du etter og velger ordren som skal hentes.
- Hvis du vil bruke **Ordreoppfyllelse**-operasjonen, søker du etter og velger én eller flere ordrelinjer.

Hvis valgt ordre eller valgte ordrelinjer ikke er konfigurert for henting ved den bestemte butikken, eller hvis ordren allerede er fullstendig hentet, vil ikke **Hent**-operasjonen være tilgjengelig.

![Henteoperasjon.](media/pickupoperation.png)

I Microsoft Dynamics 365 Commerce versjon 10.0.17 og senere kan funksjonen for **Forbedret brukeropplevelse for hentebehandling på salgssted** aktiveres gjennom Funksjonsbehandling i Commerce Headquarters. Hvis denne funksjonen er slått av, kan brukere ikke velge henteantall. Som standard er det fullstendige antallet som ble bestilt for linjen, antallet som blir hentet. Denne erfaringen kan være problematisk, fordi brukere kan glemme å velge noen varer for henting når de utfører hentingen gjennom ordreoppfyllelse.

Funksjonen for **Forbedret brukeropplevelse for hentebehandling på salgssted** gir brukerne mer kontroll over valget av produkter som skal hentes, og antallet av disse produktene som skal hentes. Brukere trenger ikke å velge hver linje i salgsordren på ordre fullføringssiden før de velger **Hent**. Alle varene som kan hentes, vises. Brukere kan angi flere linjer for henting selv om bare én produktlinje er valgt.

Når funksjonen for **Forbedret brukeropplevelse for hentebehandling på salgssted** er aktivert, og du velger **Hent**-operasjonen, vises dialogboksen **Hent**. Der kan du velge varene og antallene som skal hentes. Som standard regnes alle bestilte antall som har lager i en hentet eller pakket tilstand, som kvalifisert for henting. Som standard blir dette antallet angitt som henteantall. Du kan endre antallet som er angitt, forutsatt at mengden ikke er 0 (null) og ikke overskrider det totale åpne (det vil si ikke-fakturert) antallet for den valgte linjen.

![Dialogboksen Hent.](media/pickupselect.png)

Når du har valgt antallene som skal hentes og deretter velger **Hent**, vises transaksjonssiden. Hvis funksjonen for [omni-kanalbetalinger](omni-channel-payments.md) er aktivert, og det finnes registrerte, forhåndsautoriserte kredittkortbetalinger, må du bruke betalingen.

På transaksjonssiden beregner systemet beløpene som forfaller, ved å beregne totalen som forfaller for de valgte hentevarene, og deretter trekke fra eventuelle tidligere brukte innbetalinger eller autoriserte kredittkortbetalinger. Du må behandle betaling for å fullføre hentetransaksjonen. Hvis [skjermoppsettet](pos-screen-layouts.md) på transaksjonssiden er konfigurert slik at det inkluderer **Fullfør transaksjon**-operasjonen, og ingen beløp forfaller, kan du fullføre transaksjonen uten å velge en betalingsmetode. Hvis **Fullfør transaksjon**-operasjonen ikke er tilgjengelig, kan du velge koblingen for **USD 0,00 forfalt beløp** i ruten **Totaler** for å fullføre transaksjonen uten å velge en betalingsmetode.

![Transaksjonsside for en hentetransaksjon for kundeordre.](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Endre hentelinjer eller -antall

Hvis du må endre henteantallet etter at du har valgt varene som skal hentes, kan du velge **Angi antall**. Du kan ikke sette henteantallet til **0** (null) eller øke det til en verdi som overskrider det ikke-fakturerte antallet som gjenstår for den bestilte linjen. Hvis du vil fjerne en hentelinje fra transaksjonskurven, velger du **Annuller transaksjon**. Gjeldende transaksjon stoppes, og flyten for **Hent**-operasjonen starter på nytt.

Hvis funksjonen for **Forbedret brukeropplevelse for hentebehandling på salgssted** er aktivert, kan organisasjoner legge til en knapp for operasjonen **Endre hentelinjer** på skjermoppsettet på transaksjonssiden. Når du har opprettet hentetransaksjonskurven på salgsstedet og valgt varer, kan du velge **Endre hentelinjer** hvis du må endre hentevarene, men ikke vil annullere hele transaksjonen. I dialogboksen **Endre hentelinjer** som vises, kan du endre hentevarene og antallene. Transaksjonskurven oppdateres deretter for å gjenspeile endringene.

![Dialogboksen Endre hentevarer.](media/pickupchange.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]