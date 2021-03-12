---
title: Arbeide med forhåndsinnstillinger for stil
description: Dette emnet beskriver hvordan du arbeider med forhåndsinnstillinger for områdestiler i Microsoft Dynamics 365 Commerce områdebygger.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1bd8f6e31afa300c5e7687a657ae2807995af8d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006316"
---
# <a name="work-with-style-presets"></a>Arbeide med forhåndsinnstillinger for stil

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du arbeider med forhåndsinnstillinger for områdestiler i Microsoft Dynamics 365 Commerce områdebygger.

## <a name="overview"></a>Oversikt

En forhåndsinnstilling for stil er et lagret sett med alle redigerbare stilverdier i hele temaet for området. Den kan brukes til øyeblikkelig å endre utseendet på et område i områdebygger. Med forhåndsinnstillinger for stil kan Commerce-områdebyggere raskt endre, forhåndsvise og aktivere et sett med stilverdier for hele området uten å måtte bruke CSS eller distribuere temaer. Skriftstiler, knappestiler og områdefarger er vanlige eksempler på stilvariabler som kan behandles gjennom forhåndsinnstillinger for stil.

Settet med stilvariabler som er tilgjengelig på et område, bestemmes av temaet og modulbiblioteket som distribueres til leieren av et område. Dynamics 365 Commerce online-SDK (Software Development Kit) lar utviklere implementere så mange (eller så få) redigerbare stilvariabler som de trenger for et gitt tema. Ved å aktivere flere stilvariabler kan en temautvikler gi forfattere i områdebygger det endelige valget om områdestiler. Derfor kan ikke-utviklere oppdatere og forhåndsvise områdestiler ved hjelp av verktøysettet. Muligheten er også nyttig for alle scenarier der direkte endringer i temaer eller CSS vil føre til unødvendige indirekte kostnader.

Temaer der redigerbare stilvariabler er aktivert, krever en standard forhåndsinnstilling for stil. De kan også inkludere flere forhåndsinnstilte alternativer som en del av en distribuert temapakke. Et tema kan for eksempel distribueres med en standard "moderne lys"-forhåndsinnstilling for stil. Det kan også inneholde flere alternativer for forhåndsinnstillinger i tillegg til standard-forhåndsinnstillingen – for eksempel "moderne mørk," "vintage lys" eller "vintage mørk". Disse innebygde forhåndsinnstillingene for temaer opprettes av utviklere, og kan brukes som utgangspunkt for nye områdeutforminger.

I områdebygger kan forfattere velge mellom de innebygde forhåndsinnstillingene for et tema, eller de kan opprette egne forhåndsinnstillinger for stil og tilpasninger ved hjelp av de aktiverte stilvariablene. En forhåndsinnstilling for stil kan forhåndsvises i områdebygger før den aktiveres på det publiserte området. Når en forfatters stilendringer er gjennomgått, kan den forhåndsinnstilte stilen settes til "aktiv" for det publiserte området.

## <a name="preview-a-style-preset"></a>Forhåndsvise en forhåndsinnstilling for stil

Hvis du vil forhåndsvise en forhåndsinnstilt stil på området i områdebygger, følger du denne fremgangsmåten.

1. I venstre navigasjonsrute for området går du til **Områdeinnstillinger \> Utforming**.
1. I **Forhåndsinnstillinger for stil**-kategorien øverst i redigeringsprogrammet for utforming velger du en forhåndsinnstilling i **Tilgjengelige forhåndsinnstillinger**-listen, og deretter velger du **Vis** for å gå til redigeringsprogrammet for forhåndsinnstillinger.

    Hvis det ikke er noen forhåndsinnstillinger i **Tilgjengelige forhåndsinnstillinger**-listen, kan du se [Opprette en egendefinert forhåndsinnstilling for stil](#create-a-custom-style-preset) for informasjon om hvordan du oppretter en egendefinert stil

    > [!NOTE]
    > Forhåndsinnstillinger som fulgte med temaet, angis med et **Innebygd**-merke. Disse innebygde forhåndsinnstillingene er skrivebeskyttet. Hvis du vil kopiere en innebygd forhåndsinnstilling som en ny forhåndsinnstilling som kan tilpasses, velger du ellipse-knappen (**…**) for forhåndsinnstillingen, og deretter **Lagre som**.

1. På kommandolinjen velger du **Forhåndsvis**.
1. Velg en URL-adresse fra området ditt som skal brukes til å forhåndsvise forhåndsinnstillingen for stil, og velg deretter **OK**.
1. Velg den kanalspesifikke og lokalspesifikke URL-varianten du vil forhåndsvise, ved å velge navnet på varianten. Et nytt forhåndsvisningsvindu åpnes, der den valgte forhåndsinnstillingen for stil tas i bruk på den angitte siden.

> [!NOTE]
> URL-adressen for forhåndsvisning er permanent og godkjent. Derfor kan du kopiere, lime inn og sende den til andre godkjente medarbeidere for gjennomgang før du angir "aktiv" på ditt publiserte område. URL-adressen for forhåndsvisning er også nyttig når du skal kontrollere stiler på forskjellige enheter, i forskjellige nettlesere og på ulike skjermer.

> [!TIP]
> Når du redigerer en forhåndsinnstilling for stil, kan det være nyttig å la forhåndsvisningsvinduet stå åpent i et eget nettleservindu, slik at du raskt kan validere endringene. Når du har lagret endringene i en forhåndsinnstilling, oppdaterer du det åpne nettleservinduet med forhåndsvisningen for å validere brukeropplevelsen.

## <a name="create-a-custom-style-preset"></a>Opprette en egendefinert forhåndsinnstilling for stil

For å opprette en egendefinert forhåndsinnstilt stil følger du denne fremgangsmåten.

1. I venstre navigasjonsrute for området går du til **Områdeinnstillinger \> Utforming**.
1. I **Forhåndsinnstillinger for stil**-kategorien øverst i redigeringsprogrammet for utforming velger du **Ny forhåndsinnstilling** på kommandolinjen.
1. Angi et navn og en beskrivelse av den nye forhåndsinnstillingen, og velg deretter **Lagre**. En ny, egendefinert forhåndsinnstilling opprettes med standardverdiene for temaet som utgangspunkt.

> [!NOTE]
> Du kan også opprette en ny forhåndsinnstilling for egendefinert stil fra en eksisterende forhåndsinnstilling ved å velge ellipseknappen (**…**) for den aktuelle forhåndsinnstillingen, og deretter velge **Lagre som**. Alternativt kan du velge **Lagre som** på kommandolinjen i redigeringsprogrammet for forhåndsinnstillinger.

## <a name="modify-global-and-module-type-style-values"></a>Endre globale stilverdier og stilverdier med modultyper

Noen av stilvariablene i et tema deles mellom flere modultyper. Disse stilvariablene kalles *globale* stilvariabler. Eksempler inkluderer primære områdefarger, standard skriftstiler og knappestiler. Ved å angi globale variabler kan du endre utseendet på tvers av mange ulike modultyper.

Noen stilverdier kan være unike for en modultype, eller det kan hende de rommer en funksjon for valgfri overstyring av en standard globalverdi. Hvis et områdetema har implementert stilvariabler av modultype, kan forfattere i områdebygger tilpasse stilen til en modultype uavhengig av de globale innstillingene. Variabler i modultype kan enten forsterke eller overstyre de globale stilvariablene i et tema.

> [!NOTE]
> Hierarkiet for stilverdier på et område fungerer på følgende måte. Stilverdier som vises lenger til høyre, overstyrer stilverdiene til venstre for seg.
>
> Standardverdier for tema \< Globale stilverdier \< Stilverdier for modultyper \< CSS-overstyring

For å endre verdier for forhåndsinnstillinger av global- eller modultype i områdebygger følger du disse trinnene.

1. I venstre navigasjonsrute for området går du til **Områdeinnstillinger \> Utforming**.
1. I **Forhåndsinnstillinger for stil**-kategorien øverst i redigeringsprogrammet for utforming velger du **Vis** for en forhåndsinnstilt stil for å gå til redigeringsprogrammet for forhåndsinnstillinger.
1. Velg **Forhåndsvisning**, og følg deretter den trinnvise URL-adressen for å åpne en forhåndsvisning av forhåndsinnstillingen i en fullverdig nettleser. La dette forhåndsvisningsvinduet stå åpent.
1. Velg **Rediger** øverst til høyre i redigeringsprogrammet for forhåndsinnstillinger.
1. Bruk kontrollene for stilvariabler i redigeringsprogrammet for å endre enkelte globale stilverdier.
1. Øverst i redigeringsprogrammet, i **Moduler**-kategorien til høyre for **Globalt**-kategorien, velger du en modultype som trenger stiljustering.
1. Bruk stilkontrollene til å endre noen verdier for modultypen.
1. Når du er klar til å forhåndsvise endringene, velger du **Lagre** på kommandolinjen.
1. Gå tilbake til det åpne forhåndsvisningvinduet, og oppdater det. Forhåndsvisning i en fullverdig nettleser er nyttig for å kontrollere stilendringer ved forskjellige stoppunkt for visning, i forskjellige nettlesere og på forskjellige enhetsplattformer.
1. Når alle endringer er fullført og validert, velger du **Fullfør redigering** øverst til høyre i redigeringsprogrammet.

> [!NOTE]
> Hvis du redigerer forhåndsinnstillingen for stil som er aktiv på området, vil du se et blått **Aktivt**-merke i redigeringsprogrammet. Denne indikatoren angir at forhåndsinnstillingen er aktiv på nettstedet ditt. Hvis du endrer den aktive forhåndsinnstillingen, velger du **Publiser** for å pushe disse endringene til det publiserte området ditt.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Aktiver en ny forhåndsinnstilling for stil på det publiserte området ditt

Følg denne fremgangsmåten for å angi en forhåndsinnstilling for stil som den nye aktive forhåndsinnstillingen på området.

- Velg **Angi som aktiv**-knappen på ett av disse stedene:

    - I kommandolinjen i redigeringsprogrammet for forhåndsinnstilte stiler
    - Ellipse-menyen (**...**) for en tilgjengelig forhåndsinnstilling i hovedvisningen i **Forhåndsinnstillinger for stil**-fanen i **Områdeinnstillinger \> Utforming**

Stilverdiene for forhåndsinnstillingen aktiveres på hele den brukerrettede delen av nettstedet ditt.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)
