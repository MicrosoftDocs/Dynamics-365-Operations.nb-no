---
title: Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management
description: Denne artikkelen beskriver hvordan du oppretter og viser egendefinerte instruksjoner for hvert trinn i hver oppgaveflyt som du definerte for mobilappen Warehouse Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: faa9bfa320823664603153601c56654170e7e23a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334484"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management

> [!IMPORTANT]
> Funksjonene som er beskrevet i denne artikkelen, gjelder bare for den nye mobilappen Warehouse Management. De påvirker ikke den gamle lagerappen, som nå er avskrevet.

Denne artikkelen beskriver hvordan du oppretter og viser egendefinerte instruksjoner for hvert trinn i hver oppgaveflyt som du definerte for mobilappen Warehouse Management. Når lagerarbeiderne mottar velskrevne instruksjoner, kan de umiddelbart begynne å bruke nye flyter uten å kreve tidligere opplæring. Denne funksjonalitet inneholder følgende fordeler:

- **Få arbeidere i gang raskere ved å la dem følge enkle instruksjoner for hvert oppgavetrinn.** Hvert trinn i en flyt gir instruksjoner som gjør det mulig for frontlinjearbeidere å forstå oppgaven.
- **Gi instruksjoner som samsvarer med dine egne prosesser.** Skriv dine egne instruksjoner som samsvarer med forretnings- og lagerprosessene. Du kan for eksempel angi at terminologien passer for fysiske plass og lokale forkortelser.

## <a name="turn-the-warehouse-app-step-instructions-feature-on-or-off"></a>Aktiver eller deaktiver instruksjonsfunksjonen i lagerappen

Før du kan bruke denne funksjonen, må den være aktivert for systemet. Denne funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.29 og kan ikke deaktiveres. Hvis du kjører en versjon som er eldre enn 10.0.29, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Trinninstruksjoner for lagerapp* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="step-titles-and-step-instructions-in-the-app"></a>Trinntitler og trinninstruksjoner i appen

Hvert trinn i en oppgaveflyt i mobilappen Warehouse Management identifiseres av en trinn-ID. I tillegg har hvert trinn en tittel, et ikon og en instruksjon. For mer informasjon, se [Tilordne trinnikoner og -titler for mobilappen Warehouse Management](step-icons-titles.md).

### <a name="step-titles"></a>Trinntitler

En *trinntittel* er en kort beskrivelse av hva en arbeider skal gjøre i løpet av et trinn. Den vises som stor tekst øverst på skjermen, som vist i illustrasjonen nedenfor.

![Eksempel på en trinntittel i Warehouse Management-mobilappen](media/wma-step-title.png "Eksempel på en trinntittel i Warehouse Management-mobilappen")

> [!TIP]
> På grunn av den store tekststørrelsen bør du prøve å holde trinntitlene så korte som mulig. Hvis ikke, kan det hende at teksten blir avkortet. For lange titler kan arbeidere imidlertid fremdeles trykke og holde inne tittelen for å åpne en dialogboks som viser hele teksten.

### <a name="step-instructions"></a>Trinnvise instruksjoner

En *trinninstruksjon* er en lengre beskrivelse som gir mer informasjon om hva en arbeider skal gjøre i løpet av et trinn. Den vises i en popup-dialogboks som vist i illustrasjonen nedenfor.

![Eksempel på en trinninstruksjon i Warehouse Management-mobilappen](media/wma-step-instructions.png "Eksempel på en trinninstruksjon i Warehouse Management-mobilappen")

Trinninstruksjonen vises automatisk når et trinn åpnes. Arbeidere kan avvise den ved å trykke utenfor popup-dialogboksen. I tillegg inneholder dialogboksen en **Ikke vis igjen**-avmerkingsboks som arbeidere kan velge for å hindre at instruksjonen vises neste gang de utfører den samme oppgaven.

## <a name="load-the-default-setup"></a>Last inn standardoppsettet

Når du slår på funksjonen *Trinninstruksjoner for lagerapp* for første gang, vil ikke systemet inneholde noen egendefinerte trinntitler eller instruksjoner. Det første du bør gjøre, er derfor å laste inn standardoppsettet. Standardoppsettet inneholder tekster for alle de tilgjengelige trinn-ID-ene på alle språk som støttes. Følg denne fremgangsmåten for å laste inn standardoppsettet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Trinn formobilenhet**.
1. Velg **Opprett standardoppsett** i handlingsruten. Siden fylles ut med standardtrinnene.

## <a name="customize-step-titles-and-instructions"></a>Tilpass trinntitler og instruksjoner

Følg denne fremgangsmåten for å tilpasse tittelen og/eller instruksjonen for et trinn på en rekke språk.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Trinn formobilenhet**.

    Siden **Trinn for mobilenhet** inneholder alle trinn som er tilgjengelige for systemet ditt. Hver trinn-ID kan deles mellom en rekke menyelementer for mobilenheter. Hvis en trinn-ID deles mellom flere menyelementer, vises samme tittel og instruksjon for alle menyelementene. Du kan imidlertid opprette overstyringer for å tilpasse tittelen og instruksjonen for bestemte menyelementer. (Hvis du vil ha mer informasjon, kan du se neste del.)

    Rutenettet inneholder følgende kolonner:

    - **Menyelementnavn** – Rader der denne kolonnen er tom, bruker standard trinntittel og -instruksjon som gjelder for alle menyelementer for mobilenheter som det ikke er definert noen overstyring for. Rader der denne kolonnen angis til navnet på et menyelement, har overstyringer som bare gjelder for det angitte menyelementet.
    - **Trinn-ID** – Den unike ID-en for trinnet.
    - **Tittel for inndata** – Tittelen som vises når appen ber om ny informasjon. Vanligvis er feltene på siden tomme (det vil si at de ikke har noen forhåndsinnstilte verdier).
    - **Tittel på bekreftelse** – Tittelen som vises når appen ber om bekreftelse av en verdi som allerede er lagret i systemet. Vanligvis har feltene på siden forhåndsinnstilte verdier.

1. Finn kombinasjonen av verdier for **Trinn-ID** og **Menyelementnavn** som du ønsker å redigere, og velg verdien i kolonnen **Trinn-ID**. Siden som åpnes, viser alle de tilgjengelige oversettelsene for tittelen og instruksjonen til det valgte trinnet.
1. Følg ett av disse trinnene for å tilpasse teksten for hvilket som helst språk. For begge alternativene kan du redigere tekster for eksisterende språk. Det første alternativet lar deg imidlertid legge til tekster for nye språk, mens bare det andre alternativet lar deg vise og redigere tekster for alle eksisterende menyspesifikke overstyringer for det valgte språket.

    - På verktøylinjen velger du **Legg til** for å åpne en dialogboks , der du kan legge til eller redigere tekster for språk som støttes. Sett **Referansespråk**-feltet til språket du vil vise verdier for. Verdiene vises i venstre kolonne. Sett feltet **Språk for oversettelseneL** til språket du vil legge til eller tilpasse. I høyre kolonne redigerer du verdiene i feltene **Tittel for inndata**, **Instruksjon for inndata**, **Tittel på bekreftelse** og **Instruksjon for bekreftelse** etter behov. Velg deretter **OK**.
    - I rutenettet finner og velger du raden der **Språk**-feltet er satt til språket du vil redigere. På verktøylinjen velger du **Vis oversettelser av dette trinnet på &lt;språk&gt;** for å åpne en dialogboks der du kan redigere tekster for alle tilgjengelige overstyringer for det valgte språket. Dialogboksen inneholder et rutenett som har rader for både standardtekster (der feltet **Menyelementnavn** er tomt) og for hver tilgjengelige overstyringstekst (der feltet **Menyelementnavn** er angitt til navnet på menyelementet som overstyringen gjelder for). Rediger verdiene i feltene **Tittel for inndata**, **Instruksjon for inndata**, **Tittel på bekreftelse** og **Instruksjon for bekreftelse** etter behov. Velg deretter **OK**.

1. Fortsett å arbeide til du har definert alle nødvendige titler og instruksjoner for hvert obligatoriske språk.

## <a name="add-menu-specific-overrides"></a>Legg til menyspesifikke overstyringer

Som nevnt i forrige del kan du opprette en rekke menyspesifikke overstyringer for hver trinn-ID. Du kan bruke denne funksjonen til å redigere og endre instruksjonen slik at den passer bedre til din lokale forretningsprosess for et bestemt menyelement. For salgsplukking kan du for eksempel gi et hint om at arbeiderne bør begynne med å skanne en arbeids-ID hvis firmaet vanligvis tilbyr arbeids-IDer til arbeidere på et utskrevet dokument.

Hver overstyring gjelder et bestemt menyelement for mobilenhet, og kan inneholde et hvilket som helst antall oversettelser. Hvis det ikke finnes noen overstyring for et menyelement, bruker menyelementet standardtekstene. Hvis det ikke er definert noen overstyring for et språk, brukes standardtekstene, også for menyelementer der det defineres en overstyring for andre språk.

Hvis du vil opprette og konfigurere en overstyring, gjør du følgende.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Trinn formobilenhet**.
1. I rutenettet finner og velger du raden du vil opprette en overstyring for.
1. Velg **Legg til trinnkonfigurasjon** i handlingsruten.
1. I rullegardinlisten i dialogboksen **Legg til trinnkonfigurasjon** setter du feltet **Menyelement** til navnet på menyelementet på mobilenheten som overstyringen gjelder for. Velg deretter **OK**.
1. Siden som vises, viser alle tekstene som er tilgjengelige for den nye overstyringen. I utgangspunktet opprettes bare ett språk. Alle andre språk vil fortsette å bruke standardteksten med mindre du legger til disse språkene her. Rediger tekstene og legg til nye språk slik du ønsker, som beskrevet i den forrige delen.
