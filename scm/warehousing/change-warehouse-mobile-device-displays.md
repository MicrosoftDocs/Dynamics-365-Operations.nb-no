---
title: Visningsinnstillinger for lagermobilenheten
description: "Denne artikkelen beskriver hvordan du definerer utseendet på en mobilenhetsvisning og tilordning av hurtigtaster til kontroller, for eksempel knapper."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 721b293d1f8c76458ca510732f9bb94f003ac6e3
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-mobile-device-display-settings"></a>Visningsinnstillinger for lagermobilenheten

Denne artikkelen beskriver hvordan du definerer utseendet på en mobilenhetsvisning og tilordning av hurtigtaster til kontroller, for eksempel knapper. 

Denne artikkelen gjelder funksjoner for avanserte lageraktiviteter i Lagerstyring. Mobilenheter kan brukes for mange av oppgavene som lagerarbeidere utfører.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Angi stiler og tilordne hurtigtaster
Som en del av konfigurasjonen for mobil enhet, kan du definere ulike oppsett for mobile enheter. Hvis du vil gjøre dette, må du vite navnet på CSS-filen (Cascading Style Sheets) og ASPX-filen (Active Server Page Extension). Standardfiler installeres som en del av installasjonen for portalen for lagermobilenheter. Hvis du ikke vet filnavnene, spør du systemansvarlig. Du kan definere en ny stil på siden **Innstillinger for visning av mobilenhet**:

-    I feltet **CSS-fil** angir du navnet på CSS-filen. Ta med filtypen CSS i filnavnet.
-   I feltet **Visning av innstillinger for visning av mobilenheten** angir du ASPX-filen. Du skal **ikke** inkludere filtypen ASPX.

CSS- og ASPX-filene må være plassert i en bestemt katalog slik at programmet Internet Information Services (IIS) kan laste dem inn. Det kan være nyttig å definere forskjellige CSS-filer hvis du kjører funksjonen for mobilenhet i ulike lesere eller på ulike typer maskinvare som krever annen oppsettskontroll. Enkle innstillinger, for eksempel bakgrunnsfargen, skriften og skriftstørrelsen for tekst, og bredden og virkemåten for knapper, kan lett kontrolleres av annen bruk av CSS-filer. ASPX-filen brukes til å vise mobilområdet på ASP.NET-programmet på serversiden. Filen styrer hvordan den overordnede strukturen for HTML legges ut. Det er lurt å tilpasse denne funksjonaliteten bare hvis du har alvorlige strukturelle problemer med HTML og JavaScript, og du må endre denne koden for de bestemte enhetene. For å tilordne HTML-kontroller på siden for mobil enhet for å bruke hurtigtaster velger du siden **Innstillinger for visning av mobilenhet** feltet **Hurtigtast**, og tilordner de numeriske kodene for tastene. Du kan bruke menyen **Vis koder for hurtigtaster** på den mobile enheten til å finne den numeriske tegnkodene. Legg merke til at tilordningene kan variere, avhengig av maskinvaren som brukes. Du må bruke følgende syntaks for å opprette tilknytningen:

&lt;Kontrollnavnet&gt;(&lt;navn&gt;) =&lt;nøkkel koden&gt;;

Her er en forklaring på delene av syntaksen:

-   **&lt;Kontrollnavnet&gt;** – navnet på en kontroll (for eksempel en knapp) som vises i HTML.
-   **(&lt;navn&gt;) ** – Navnet på tastaturtasten du oppretter hurtigtasten for.
-   **&lt;Nøkkel koden&gt;** – numerisk tegnkoden for nøkkelen som skal brukes som hurtigtast.

Her er et eksempel:

Avbryt(Esc)=27; Full(F2)=113

På alle sider som inneholder en **Avbryt**-knapp, får du denne teksten:

**(Esc) Avbryt**

Trykker du Esc-tasten på tastaturet vil du aktivere **Avbryt** knappen. Hvis du vil bruke innstillingene for stil og tastatur snarvei på en bestemt enhet, må du opprette en tilordning i **Vilkår** feltet. Du må bruke et vanlig .NET-uttrykk til å opprette tilordningen og uttrykket må bestå av tre deler som er atskilt med en loddrett strek (|), som vist her:

Request.UserHostAddress=&lt;bruker adressen for verten&gt;| HostName =&lt;bruker vertsnavnet&gt;| Request.UserAgent=&lt;brukeragent&gt;

Her er en forklaring på delene av uttrykket:

-   **&lt;brukeren vertsadresse&gt;** – A .NET vanlig uttrykk som samsvarer med IP-adressen som anmoder.
-   **&lt;vertsnavn for brukeren&gt;** – A .NET vanlig uttrykk som samsvarer med navnet på til anmoderen.
-   **&lt;brukeragent&gt;** – A .NET vanlig uttrykk som samsvarer med den leseren av vedkommende bruker-IDen.

Følgende eksempel aktiverer bruk av Internet Explorer 8:

Request.UserHostAddress=. \*| HostName =. \*| Request.UserAgent=MSIE\\I8\\.0

Du kan bruke **Vis serverkonfigurasjon for visningsinnstillinger**-menyen på den mobile enheten for å finne informasjon om oppsettet.

## <a name="define-text-colors-for-messages"></a>Definere tekstfarger for meldinger
Du kan bruke siden **Tekstfarger på mobilenheten** til å styre de ulike fargene som brukes i systemgenererte meldinger, for eksempel feilmeldinger. Tekstfargen kan for eksempel angi formålet eller viktigheten for meldingen. Følgende typer meldinger vises.

| Meldingstype | Beskrivelse                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standard      | Standardmeldinger bruker standard fargeinnstillinger for alle meldinger, som er definert av CSS-filen for Portaltjenester for lagermobilenheter.                                                   |
| Feil        | Feilmeldinger angir et problem som brukeren må løse før han eller hun kan fortsette.                                                                                             |
| Vellykket      | Fullført-meldinger bekrefter at en handling er fullført.                                                                                                                                |
| Advarsel      | Advarsler informerer arbeideren om at det er et problem, eller at det kan være et problem hvis arbeideren fortsetter. Arbeideren må imidlertid ikke løse problemet å fortsette. |

For å velge farge velger du siden **Velg farge** og klikker på paletten eller skriver inn en heksadesimal fargekode.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Angi datoformatet som skal brukes på mobilenheter
Du kan utvide listen over godkjente datoformater for hver installasjon. Denne funksjonen kan for eksempel være nyttig hvis du vil angi et format som gjør det enklere for en arbeider å angi datoer på en mobilenhet. Standardformatet bestemmes av brukerens standardspråk, som er angitt i feltet **Språk** på siden **Brukeralternativer**. (Samme side brukes også til å knytte en ansatt til et bestemt lager arbeid brukeren.) **Notat:** for lageret Mobile enheter Portal ikke bruke innstillingen for den **dato klokkeslett- og tallformatet** på den **innstillinger for språk og region** siden. Hvis du vil endre et datoformat, må du kjenne til vanlige uttrykk i Microsoft .NET Framework. Hvis du vil ha mer informasjon, kan du se [Vanlige uttrykk i .Net Framework](http://go.microsoft.com/fwlink/?LinkId=391260). Rediger filen Dates.ini, som er plassert i innhold for å definere datoformater,\\innstillinger\\Dates.ini på lageret Mobile enheter Portal-serveren. Denne filen bruker vanlige .NET-uttrykk til å angi datoformatet. Det vanlige uttrykket må inneholde underordnede uttrykk som oppretter navngitte grupper for dag, måned og år (DDMMÅÅ), som vist i eksemplet nedenfor:

^(? &lt;day&gt;\\d{2})(?&lt; month&gt;\\d{2})(?&lt; året&gt;\\d {2}) $

Hvert underordnede uttrykk krever ett til to sifre for dagen og måneden, og ett til fire sifre for året. Det følgende underordnede uttrykket definerer for eksempel en navngitt gruppe for et år, og krever fra to til fire sifre:

(? &lt;year&gt;\\d{2,4})

Du kan angi mer enn ett uttrykk i den samme filen. Hvert uttrykk må være på en egen linje. Det første uttrykket som samsvarer, brukes til å analysere datoen.

<a name="see-also"></a>Se også
--------

[Configuration of mobile devices for warehouse work](configure-mobile-devices-warehouse.md)


