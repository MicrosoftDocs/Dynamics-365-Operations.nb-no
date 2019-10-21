---
title: E-postmaler
description: Dette emnet gir informasjon om e-postmaler som du kan opprette og bruke i Microsoft Dynamics 365 Talent – Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 7174fd96e5ddc9ba5a91eb423d08afd1daa45f48
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008042"
---
# <a name="email-templates"></a>E-postmaler
[!include[banner](../includes/banner.md)]

Ved hjelp av e-postmalbiblioteket kan administratorer opprette et enhetlig tema og varemerking for alle e-postmeldinger som sendes via Microsoft Dynamics 365 Talent: Attract and Offer. Administratorer kan også kuratere en samling med e-postinnholdsmaler som andre brukere kan bruke. Ansettelsesgruppen kan bruke disse malene i arbeidsflyten til å sende e-postmeldinger mer effektivt. Noen e-postmeldinger er konfigurert til å bli sendt automatisk, og administratoren kan bruke e-postmalbiblioteket til å tilpasse innholdet for disse e-postene.

> [!NOTE]
> Hvis du vil bruke e-postmaler, må organisasjonen ha tillegget for omfattende ansettelse.

## <a name="global-template-configurations"></a>Globale malkonfigurasjoner

Hvis du vil opprette konsekvent merking for alle e-postmeldinger, må administrator først konfigurere den globale toppteksten og bunnteksten for alle e-postmaler. I administrasjonssenteret, i **Innstillinger for e-postmal** i **Topptekst**-delen kan administratoren laste opp et bilde som skal brukes som topptekst eller banner for alle e-postmeldinger. Bildet kan være en firmalogo, et brevhode eller et hvilken som helst annet representativt bilde. Vi anbefaler at bredden er mellom 25 og 800 piksler, og at høyden er mellom 25 og 150 piksler, fordi disse dimensjonene er optimale for de fleste e-postklienter, for eksempel Microsoft Outlook. Bildet må være en JPEG-, JPG-, PNG- eller SVG-fil, og størrelsen på må være mindre enn 1 megabyte (MB). Når et bilde er lastet opp, genereres og vises det en forhåndsvisning av hodet. Hvis hodebildet må fjernes eller erstattes, kan administratoren bruke **Fjern**-alternativet over forhåndsvisningen.

I **Bunntekst**-delen kan administratoren gi koblinger til firmaets personvernerklæring for kommunikasjon og vilkårene. Disse koblingene er inkludert i en bunntekst som blir generert automatisk. Deretter vises en forhåndsvisning av denne bunnteksten. Administratoren kan også velge et bestemt språk som bunntekster i e-postmeldinger skal sendes på, som en del av alle e-postmeldinger. Den samme språkkonfigurasjonen brukes også til å sette sammen tabellen for intervjusammendrag. 

Husk å lagre endringene før du lukker administrasjonssenteret.

> [!NOTE] 
> Toppteksten og bunnteksten er globale innstillinger for alle e-post. Derfor vises de i alle e-postmeldingene som sendes via Attract. Hvis innstillingene ikke er konfigurert, blir toppteksten og bunnteksten utelatt i alle e-postmeldinger.

## <a name="email-template-library"></a>E-postmalbibliotek 

Når de globale malkonfigurasjonene er satt opp, kan administratoren begynne å opprette og kuratere maler for alle e-postmeldinger som sendes fra Attract and Offer. E-postmalbiblioteket er bare tilgjengelig for administratorer. Hvis du vil åpne biblioteket, velger du **E-postmaler**-kategorien på hovednavigasjonsmenyen. Biblioteket er inndelt etter de ulike aktivitetene i Attract som e-postmeldinger må sendes til, for eksempel planlegging, vurdering og jobboppretting og -tilbud. Administratoren kan velge en hvilken som helst kategori for å vise alle e-typene som er knyttet til aktiviteten. Velg for eksempel **Planlegging** for å vise de forskjellige typene e-post som sendes i løpet av planleggingsprosessen, og alle malene som er tilgjengelige for hver type e-post. Hvert avsnitt i en kategori representerer en type e-post.

Noen typer e-post kan ha flere mottakere. I **Planlegging**-kategorien sendes for eksempel e-postmeldingene som sendes når tidsplansammendraget for intervjuet er nødvendig, både til kandidater og intervjuere. Hver del har to primære kolonner: **Maltittel** og **Mottaker**. Hver rad i en del representerer én enkelt mal for en type e-post. Et hengelåssymbol vises først i raden for hver mal. Dette symbolet indikerer at malen er standardmalen som følger med Attract, og at den ikke kan slettes. For en hvilken som helst mal kan administratoren bruke ellipseknappen (**...**) til å kopiere malen, angi den som en standardmal, eller slette den. Når en mal er angitt som en standardmal, kan én av to virkemåter forekomme. Virkemåten er angitt av merket eller merkene som vises i raden for malen:

- **Standard** – Dette kortet betyr at malen er standardmalen for e-post som sendes, og at informasjon registreres i den når en bruker sender e-post av denne bestemte typen.
- **Standard** + **Sendt automatisk** – Denne kombinasjonen av kort betyr at malen er den aktive malen for systemgenererte e-postmeldinger som sendes automatisk.

Hvis du vil redigere en mal, merker du raden og gjøre endringer i malen.

> [!NOTE]
> Hver mottaker av en bestemt type e-post har en standardmal. Alle de standard Attract-malene er angitt som standardmaler til administratoren oppretter en ny mal for en bestemt type e-post og angir denne som standardmalen.

## <a name="create-a-template"></a>Opprett en mal

Opprette en mal ved å velge **+ Ny mal** i det øvre høyre hjørnet av e-postmalbiblioteket. Hvis du vil velge typen e-post som du oppretter malen for, velger du mottakeren, prosessen og hendelsen som e-post må sendes for. Velg deretter **Opprett**.

Malen åpnes i redigeringsvisning, og du kan gi navn til malen. Hvis malen for eksempel er ment for kandidater fra et universititet i USA, men innholdet er skrevet på fransk, kan du angi **Universititet\_USA\_fransk** som tittel. Tittelen, emnelinjen og innholdet i meldingsteksten for alle maler kan støtte språk enn engelsk.

**Til**-feltet for en mal ikke kan redigeres, fordi du allerede har valgt mottakeren da du først laget malen.

Du kan legge til personer som **Rekrutterer** eller **Ansettelsesansvarlig** til Kopi til-linjen. Når e-postmeldingen er sendt, erstattes automatisk disse rollene med de riktige brukerne, basert på konteksten for jobben.

Emnelinjen og innholdet i meldingsteksten støtter plassholdere. Du kan sette inn plassholdere ved å skrive inn **\#** og deretter velge den riktige plassholderen i rullegardinlisten for autofullføring. Listen over tilgjengelige plassholdere vises til høyre på siden. Når e-postmeldingen er sendt, erstattes automatisk plassholderene med de riktige brukerne, basert på konteksten til jobben og mottakeren. En mal for en e-post som sendes til kandidater, inneholder for eksempel plassholderen \#{Kandidat\_Navn}. Når e-postmeldingen sendes til en kandidat som heter Cameron, vil denne plassholderen erstattes med Camerons navn.

Redigeringsprogrammet for innhold for brødteksten er et redigeringsprogram for rik tekst som lar deg stile og formatere tekst. Du kan også sette inn hyperkoblinger og ankere.

Når du har opprettet en mal for en bestemt type e-post, velger du ellipseknappen (**...**) i raden for malen, og angir den som standardmalen.

## <a name="consume-templates"></a>Bruke maler

Når ansettelsesteamet sender en e-post, kan den bruke malene som administratoren opprettet. Hvis det er opprettet flere maler for e-posten som en bruker sender, vises en rullegardinliste i arbeidsflyten for e-postsammensetningen. Standardmalen angis automatisk, men brukeren kan velge en annen mal.

> [!NOTE] 
> Du kan opprette flere maler for e-postmeldinger som sendes automatisk. Imidlertid du kan angi bare én mal som den aktive malen. Siden denne prosessen blir utløst av hendelser, kan bare administratoren avgjøre hvilken mal som skal brukes, på grunnlag av kombinasjonen **Standard**- og **Sendt automatisk**-kort i malbiblioteket.
