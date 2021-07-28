---
title: Aktivere og bruke deling på tvers av kanal
description: Dette emnet beskriver hvordan du aktiverer og bruker funksjonen for deling på tvers av kanaler i områdebyggeren i Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a5f35dc48dbdf89e963108e9e8ef6faec326f970
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349728"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Aktivere og bruke krysskanaldeling

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du aktiverer og bruker funksjonen for deling på tvers av kanaler i områdebyggeren i Microsoft Dynamics 365 Commerce.

Deling på tvers av kanaler lar forhandleren bruke på nytt og dele innhold mellom flere kanaler på et område. Denne muligheten er nyttig når områdekanalene har et kompatibelt originalspråk, eller når de har flere felles innholdselementer.

Deling på tvers av kanaler fungerer ved å aktivere en standardkanal som søker etter tilgjengelig innhold når en kanalspesifikk versjon av det forespurte innholdet ikke blir funnet. Innhold som er ment for deling mellom kanaler, opprettes i standardkanalen. Dette innholdet kan lokaliseres for en hvilken som helst nasjonal innstilling som brukes på en områdekanal.

## <a name="when-to-use-cross-channel-sharing"></a>Når bruke deling på tvers av kanal

Deling på tvers av kanal er nyttig når flere kanaler på ett enkelt område kan dele innhold. En forhandler som har flere merker og butikkfasader som er gruppert under ett enkelt område, kan for eksempel dele noe av innholdet blant noen av eller alle butikkfasader. Dette delte innholdet kan omfatte sider for vilkår og betingelser, betalingsbetingelser, leveringsmåter og vanlige spørsmål.

Deling på tvers av kanal støtter også fragmenter. Derfor kan en innholdsside som inneholder kanalspesifikke fragmenter opprettes som innhold på tvers av kanaler. I dette tilfellet vil kanalspesifikke fragmenter på en krysskanalside bare bli gjengitt når de blir forespurt fra den tilsvarende butikkfasadekanalen, selv om det meste av innholdet blir delt mellom kanaler.

Områder som bare har én kanal, eller områder med flere kanaler som ikke kan dele innhold, kan ikke dra nytte av deling på tvers av kanaler.

## <a name="enable-cross-channel-sharing"></a>Aktivere deling på tvers av kanal

Deling på tvers av kanaler er aktivert på områdenivå. Dette er en énveisoperasjon. Hvis deling på tvers av kanaler er aktivert, kan det med andre ord ikke deaktiveres.

Følg denne fremgangsmåten for å aktivere deling på tvers av kanaler i Commerce-områdebygger:

1. Gå til **Områdeinnstillinger \> Funksjoner**.
1. Sett alternativet for funksjonen **På tvers av kanal** til **På**.

    ![Alternativ for på tvers av kanal satt til På i Commerce-områdebygger.](./media/enabling-cross-channel-sharing.png)

Når du har aktivert deling på tvers av kanaler, vil informasjon om på tvers av kanal vises i **Kanaler**-delen under **Områdeinnstillinger \> Funksjoner**, som vist i eksemplet nedenfor.

![Kanalinformasjon som er synlig etter at deling på tvers av kanal er aktivert.](./media/channels-cross-channel.png)

Etter at du har aktivert deling på tvers av kanaler, vil **Kanal**-feltet øverst til høyre i Commerce-områdebygger inneholde et alternativ for **nettbutikk på tvers av kanal** som du kan bruke til å administrere innhold på tvers av kanaler, som vist i illustrasjonen nedenfor.

![Alternativet for nettbutikk på tvers av kanaler i Kanaler-feltet etter at deling på tvers av kanal er aktivert.](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Opprette og bruke innhold på tvers av kanal

Du kan opprette og bruke innhold på tvers av kanal på flere måter. Du kan for eksempel opprette fragmenter på tvers av kanal, opprette sider på tvers av kanaler som bruker innhold på tvers av kanal og kanalspesifikt innhold, og overstyre på fragmenter på tvers av kanal med kanalspesifikke versjoner av fragmenter.

### <a name="create-a-cross-channel-fragment"></a>Opprette et fragment på tvers av kanal

Følg denne fremgangsmåten for å opprette fragment på tvers av kanaler i Commerce-områdebygger:

1. Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.
1. I dialogboksen **Nytt fragment** velger du **Banner**-modulen, og under **Navn på fragment** skriver du inn et navn (for eksempel **Banner på tvers av kanal**). Velg deretter **OK**.
1. I ruten egenskapsruten for **Kampanjebanner**-modulen velger du **Legg til melding**, og deretter velger du **Melding**.
1. I dialogboksen **Melding**, under **Tekst**, angir du **På tvers av kanal** og velger **OK**. 
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

Dette fragmentet på tvers av kanal kan brukes på tvers av kanal-sider eller kanalspesifikke sider som opprettes på en områdekanal.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Opprette en på tvers av kanal-side som bruker innhold på tvers av kanaler

På tvers av kanal-sider kan brukes på en hvilken som helst kanal på området. Derfor kan du opprette en delt innholdsside én gang og utføre påfølgende oppdateringer på ett sted. En side for **vilkår og betingelser** tvers av kanal som har URL-adressen `/toc`, kan for eksempel deles mellom alle kanalene på et område. Hvis de primære URL-adressene for områdekanalene er `www.fabrikam.com/brand1` og `www.fabrikam.com/brand2`, vil den samme delte siden for **vilkår og betingelser** på tvers av kanal være tilgjengelig fra URL-adressene for begge områdekanaler, både `www.fabrikam.com/brand1/toc` og `www.fabrikam.com/brand2/toc`. Hvis siden for **vilkår og betingelser** må oppdateres senere, trenger du bare å oppdatere den ene delte siden.

Følg fremgangsmåten nedenfor for å opprette en på tvers av kanal-side i Commerce-områdebygger som bruker innhold på tvers av kanal.

1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Velg en mal** velger du en mal, for eksempel **Markedsføring**.
1. Under **Sidenavn** angir du et navn for siden (for eksempel **På tvers av kanal-side**).
1. Under **URL-adresse for side** angir du en URL-adresse for side (for eksempel **examplepage**), og deretter velger du **OK**.
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til fragment**.
1. I dialogboksen **Legg til fragment** velger du fragmentet på tvers av kanal som du opprettet tidligere, som har et kampanjebanner, og deretter velger du **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Du skal se kampanjebanneret som sier På tvers av kanal.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Opprette en kanalspesifikk side som bruker innhold på tvers av kanaler

Hvis du bruker innhold på tvers av kanaler på kanalspesifikke sider, kan du opprette et delt innholdsfragment én gang og deretter bruke det på kanalspesifikke sider. Denne typen "enkeltkilde" er nyttig for delt innhold, for eksempel vilkår og betingelser, betalingsbetingelser eller kontaktinformasjon.

Følg fremgangsmåten nedenfor for å opprette en kanalspesifikk side i Commerce-områdebygger som bruker innhold på tvers av kanal.

1. Fra en bestemt kanal, for eksempel **Fabrikam-utvidet nettbutikk**, går du til **Sider** og velger deretter **Ny** for å opprette en ny side.
1. I dialogboksen **Velg en mal** velger du en mal, for eksempel **Markedsføring**.
1. Under **Sidenavn** angir du et navn for siden (for eksempel **Kanalspesifikk side**).
1. Under **URL-adresse for side** angir du en URL-adresse for side (for eksempel **channelspecificpage**), og deretter velger du **OK**.
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til fragment**.
1. I dialogboksen **Legg til Fragment**, under **Kanal**, velger du **Nettbutikk på tvers av kanal**. Fragmentet på tvers av kanal som du opprettet tidligere, skal vises i listen. Velg det, og velg deretter **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Du skal se kampanjebanneret som sier På tvers av kanal.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Opprette en kanalspesifikk versjon av en på tvers av kanal-side

Deling på tvers av kanaler støtter overstyringer av innhold på tvers av kanaler. For eksempel vil alle områdekanalene bortsett fra én, dele samme innholdsdel. Denne ene områdekanalen krever forskjellig innhold. Hvis du vil implementere det ulike innholdet for den, overstyrer du innholdet på tvers av kanal med kanalspesifikt innhold ved å opprette en kanalspesifikk versjon av den på tvers av kanal-siden.

Følg fremgangsmåten nedenfor for å opprette en kanalspesifikk versjon av en på tvers av kanal-side i Commerce-områdebygger.

1. I **Kanal**-feltet øverst til høyre , velger du **Nettbutikk på tvers av kanal**.
1. Åpne på tvers av kanal-siden du opprettet tidligere.
1. I **Kanal**-feltet øverst til høyre, velger du kanalen som skal ha bestemt innhold. Sideredigeringsprogrammet viser en melding som ber deg om å opprette en ny sidevariant.
1. Velg **Opprett sidevariant**.
1. I **Hoved**-sporet på sidevarianten velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Kampanjebanner**-modulen, og deretter velger du **OK**.
1. I ruten egenskapsruten for **Kampanjebanner**-modulen velger du **Legg til melding**, og deretter velger du **Melding**.
1. I dialogboksen **Melding**, under **Tekst**, angir du **Kanalspesifikk** og velger **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Du skal se kampanjebanneret som sier Kanalspesifikk.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

Hvis du nå bruker den primære URL-adressen til kanalen og går til URL-adressen til på tvers av kanal-siden på dette området, vil du se det kanalspesifikke innholdet i stedet for innholdet på tvers av kanalen.

## <a name="additional-resources"></a>Tilleggsressurser

[Måter å legge til innhold på](add-manage-content.md)

[Ordliste for sidemodell](page-elements-overview.md)

[Dokumentere statuser og livssyklus](document-states-overview.md)

[Arbeide med publiseringsgrupper](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
