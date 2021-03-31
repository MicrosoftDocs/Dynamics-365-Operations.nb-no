---
title: Arbeide med CSS-overstyringsfiler
description: Dette emnet beskriver hvorfor, når og hvordan du bruker gjennomgripende stilark (CSS-overstyringsfiler) i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 41fb0be51f7af25faba1b860319aea84ae7a8b56
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207805"
---
# <a name="work-with-css-override-files"></a>Arbeide med CSS-overstyringsfiler


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvorfor, når og hvordan du bruker gjennomgripende stilark (CSS-overstyringsfiler) i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Permanente områdestiler bør vanligvis håndteres gjennom et områdetema. Temaer gir grunnleggende CSS og stilinnstillinger for modulene på en hvilken som helst side på nettstedet. Temaene opprettes ved hjelp av Dynamics 365 Commerce Online Software Development Kit (SDK), og de distribueres til nettstedene gjennom Microsoft Dynamics Lifecycle Services (LCS). Feilsøkingsfunksjoner for temaer og modulgrensesnittkonfigurasjoner i SDK hjelper nettstedsutviklere med å opprette tilpasningsmulige og sammenhengende områdeutformingspakker. Når disse utformingspakkene distribueres til et område, kan områdeforfattere fokusere på å opprette, redigere og publisere innhold i stedet for områdeutvikling.

Gitt den vanlige livssyklusen til et tema kan avhengighetsforholdet til utviklere for å gjøre stilendringer gjennom SDK- og LCS-distribusjonsforløpet, skape hindringer i enkelte scenarier. Områdeprototyper eller hurtigreparasjoner kan virke tungvint hvis SDK ikke er konfigurert, eller hvis du ikke har tid til å vente på en LCS-distribusjon.

I disse scenariene kan CSS-overstyringsfiler hjelpe. I redigeringsverktøyene for handel kan godkjente brukere laste opp en CSS-fil, forhåndsvise den og deretter aktivere den for å overstyre temaet for et område. Det er ikke nødvendig å distribuere administrasjonskostnader for SDK eller LCS. Overstyringer som er angitt i en CSS-overstyringsfil, kan være så liten som en endring i en enkelt tekststil eller så omfattende som en fullstendig merkevareoverhaling.

Før du bruker CSS-overstyringsfiler, må du være oppmerksom på følgende begrensninger:

- Bare én CSS-overstyringsfil kan være aktiv på et område om gangen. Derfor må alle aktive overstyringer være til stede i én enkelt overstyringsfil.
- Selv om du kan forhåndsvise overstyringer i redigeringsverktøyene for handel, er det ingen dedikerte feilsøkingsfunksjoner som hjelper deg med å identifisere eventuelle feil som overstyres. Med andre ord, når du bruker CSS-overstyringsfiler, har du ikke det samme verktøysettet som SDK gir for modul- og redigeringsvalidering.

CSS-overstyringsfiler gir likevel en rask måte å prototype en design eller implementere en hurtigreparasjon på før en full temaoppdatering er utviklet og distribuert.

## <a name="create-a-css-override-file"></a>Opprette en CSS-overstyringsfil

Hvis du vil opprette en CSS-overstyringsfil, kan du bruke et hvilket som helst integrert utviklingsmiljø (IDE), tekstredigeringsprogram eller redigeringsprogram for kildekode. En typisk fremgangsmåte er å bruke standard Web-feilsøkere i webleseren til å identifisere stilvelgere, egenskaper og verdier på det eksisterende området. I de fleste weblesere kan du endre verdier og forhåndsvise dem i feilsøkingsverktøyet. Når du har identifisert endringene du vil gjøre, kan du lagre dem i din egen CSS-fil.

## <a name="upload-a-css-override-file"></a>Last opp en CSS-overstyringsfil

Hvis du vil laste opp en CSS-fil til webområdet ditt i Commerce, gjør du følgende:

1. Gå til området ditt i redigeringsverktøyet.
1. Velg **Utforming** i navigasjonsruten til venstre.

    > [!NOTE]
    > Avhengig av hvilken versjon av redigeringsverktøyene for handel du bruker, må du kanskje utvide **Innstillinger** i navigasjonsruten før du kan velge **Utforming**.

1. Øverst i hovedutformingsruten velger du **CSS-overstyring**-kategorien, hvis den ikke allerede er valgt.
1. Under **Tilgjengelige CSS-ovestyringer** velger du **Last opp CSS-fil**. Et Filutforsker-vindu vises.
1. Bla til og velg en CSS-fil i Filutforsker, og velg deretter **Åpne** Den opplastede CSS-filen vises nå under **Tilgjengelige CSS-overstyringer**.

## <a name="preview-a-css-override-file"></a>Forhåndsvise en CSS-overstyringsfil

Hvis du vil forhåndsvise en CSS-overstyringsfil før du gjør den aktiv på det aktive området, følger du fremgangsmåten nedenfor.

1. I navigasjonsruten til venstre velger du **Utforming**, og deretter, i kategorien **CSS-overstyring** under **Tilgjengelige CSS-overstyringer**, finner du CSS-filen du vil forhåndsvise.
1. Ved siden av CSS-filnavnet velger du **Forhåndsvis område**.
1. I dialogboksen **Velg en URL-adresse** velger du URL-adressen for området du vil bruke overstyring for, og deretter velger du **OK**.
1. Hvis det finnes flere varianter for den valgte URL-adressen, velger du den ønskede varianten i dialogboksen **Forhåndsvisningsvarianter** som vises.

En ny nettleserfane eller et nytt vindu åpnes, der du kan validere stiloverstyringer mot området. Du kan deretter dele URL-adressen med andre godkjente Commerce-brukere for gjennomgang og tilbakemelding.

## <a name="activate-a-css-override-file-on-your-live-site"></a>Aktivere en CSS-overstyringsfil på det aktive webområdet

Når du har forhåndsvist og godkjent CSS-overstyringsfilen, kan du aktivere den på det aktive webområdet.

> [!NOTE]
> Bare én CSS-overstyringsfil kan være aktiv på området om gangen. Hvis du aktiverer en ny overstyringsfil, deaktiveres den forrige overstyringsfilen. Derfor må du kontrollere at alle nødvendige overstyringer er til stede i én enkelt CSS-overstyringsfil.

Hvis du vil aktivere en CSS-overstyringsfil, gjør du følgende.

1. I navigasjonsruten til venstre velger du **Utforming**, og deretter, i kategorien **CSS-overstyring** under **Tilgjengelige CSS-overstyringer**, finner du CSS-filen du vil aktivere.
1. Under CSS-filnavn velger du **Aktiver**. Overstyringsfilen blir umiddelbart aktiv på det aktive nettstedet ditt.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>Deaktivere en CSS-overstyringsfil på det aktive webområdet

Følg denne fremgangsmåten for å deaktivere en CSS-overstyringsfil på nettstedet ditt.

1. I navigasjonsruten til venstre velger du **Utforming**, og deretter, i kategorien **CSS-overstyring** under **Tilgjengelige CSS-overstyringer**, finner du CSS-filen du vil deaktivere.
1. Under CSS-filnavn velger du **Deaktiver**. Overstyringsfilen blir umiddelbart inaktiv på det aktive nettstedet ditt.

> [!TIP]
> Hvis du vil ha tilgang til flere alternativer for CSS-overstyringsfiler, velger du ellipsen (**...**) ved siden av CSS-filnavnet. Alternativene **Last ned**, **Gi nytt navn** og **Erstatt** er nyttige for hurtigendringer i en eksisterende CSS-overstyringsfil.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Arbeide med forhåndsinnstillinger for stil](style-presets.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]