---
title: Tilpasse brukeropplevelsen
description: Denne artikkelen forklarer hvordan du kan tilpasse Microsoft Dynamics 365 for Operations.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 689efef6ffa10bbee30cd734f3f09ba20957834d
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="personalize-the-user-experience"></a>Tilpasse brukeropplevelsen

[!include[banner](../includes/banner.md)]


Denne artikkelen forklarer hvordan du kan tilpasse Microsoft Dynamics 365 for Operations.

Det finnes mange typer tilpasninger i Microsoft Dynamics 365 for Operations. Noen tilpasninger er valgene du gjør i en liste over alternativer på en konfigurasjonsside. Noen personlige tilpasninger er implisitte, for eksempel holder Dynamics 365 for Operations oversikt over bredden på rutenettkolonnene hvis du endrer dem, og tilstanden for vist/skjult for hurtigfanene. Andre tilpasninger er eksplisitt. For eksplisitte tilpasninger, angir du en interaktiv tilpassingsmodus og endrer utseendet på en side ved å direkte styre hvordan elementer vises eller fungerer på siden. 

Alle personlige innstillinger, av en hvilken som helst type, som en bruker gjør i Dynamics 365 for Operations, er bare for denne brukeren, uavhengig av firmaet som brukeren samhandler med. Endringer som en bruker gjør på en side, påvirker ikke andre brukere i systemet.

## <a name="systemwide-options-for-the-current-user"></a>Systemomfattende alternativer for gjeldende bruker
I navigasjonsfeltet du vil finne et tannhjul bilde som kalles **Innstillinger**-menyknappen. Når du åpner **Innstillinger** menyen, vises en rekke valg. Hvis du velger **Alternativer**, åpnes brukerens **Alternativer** side. Der finner du fire alternativkategorier: **Visuelt**, **Innstillinger**, **Konto** og **Arbeidsflyt**.

-   **Visuelt:**bruk for å velge et fargetema og standardstørrelse på elementer på sidene.
-   **Innstillinger:** Her kan du velge standarder for hver gang du åpner Dynamics 365 for Operations, inkludert firma, startside og standardmodus for Vis/Rediger (som bestemmer om en side er låst for visning eller åpnet for redigering av hver gang du åpner den). Du finner også alternativer for språk, tidssone og dato, klokkeslett og nummerformat. Til slutt inneholder denne siden en rekke diverse innstillinger som vil være forskjellig fra versjon til versjon.
-   **Konto:**Bruk for å angi bruker-IDen og andre kunderelaterte alternativer.
-   **Arbeidsflyt:**dette er der du kan velge arbeidsflytrelaterte alternativer.

## <a name="implicit-personalizations"></a>Implisitte tilpasninger
Implisitte tilpasninger er de personlige tilpasningene som utføres ved å samarbeide med visse Kontroller som husker gjeldende synlig status. 

**Rutenettkolonner:** Du kan justere bredden på en kolonne i en liste ved å velge størrelseslinjen til venstre eller høyre for kolonneoverskriften og dra den til venstre eller høyre til ønsket bredde. Dynamics 365 for Operations lagrer bredden som du ønsker og viser denne kolonnen med denne bredden hver gang du åpner siden med denne listen. 

**Hurtigfaner:** noen sider har utvidbare deler kalt hurtigfaner. Dynamics 365 for Operations lagrer hvilke hurtigfaner har du utvidet, og hvilke hurtigfaner du har skjult. Hver gang du går tilbake til siden, blir de samme hurtigfanene vist eller skjult basert på siste gang de er brukt. Vi skal forklare hvordan du endrer rekkefølgen på hurtigfane inndelingene dine i denne artikkelen. I noen tilfeller kan kan skjule en hurtigfane forbedre ytelsen fordi Dynamics 365 for Operations ikke trenger å hente informasjon om denne hurtigfanen før hurtigfanen utvides. 

**Faktabokser:** noen sider har en del kalt en faktaboksrute. Denne ruten inneholder skrivebeskyttet informasjon knyttet til gjeldende emne på siden. Hver del i faktaboksruten, kalles en faktaboks. Du kan vise eller skjule en faktaboks og Dynamics 365 for Operations vil lagre dine preferanser. I noen tilfeller kan kan skjule en faktaboks forbedre ytelsen fordi Dynamics 365 for Operations ikke trenger å hente informasjon om denne faktaboksen før faktaboksen utvides.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Eksplisitte tilpasninger ved hjelp av verktøylinjen for tilpasning
Hver person og hvert firma har ulike perspektiver om hvilke data som er viktigst for dem, eller som ikke er nødvendig for hvordan de driver virksomheten. Muligheten til å tilpasse hvordan informasjonen er ordnet, samhandlet med eller skjult er viktig for å gjøre Dynamics 365 for Operations til en personlig og produktiv erfaring. 

Eksplisitt tilpasninger er de tilpasningene som du utfører eksplisitt med formålet å endre utseendet eller virkemåten for et element eller en side, ved å velge en meny for personlig tilpasning. Den vanligste typen eksplisitt personalisering er der du høyreklikker et element og velger **Tilpass**. (Vær oppmerksom på at ikke alle elementene på siden ikke kan tilpasses.) Når du velger denne metoden for tilpasning, vises vinduet for elementets egenskaper. 

[![Tilpasse egenskapene for et element](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Du vil tilpasse et element på siden på denne måten hvis du bare vil endre etiketten for elementet, skjule elementet slik at det ikke vises på siden (dette endrer ikke data, det ganske enkelt viser ikke informasjonen), inkludere informasjonen i delen for hurtigfanesammendrag (hvis elementet er i hurtigfanen), hoppe over feltet når du bruker tabulatortasten, eller gjøre det slik at dataene ikke kan endres ved å merke den som "Ikke rediger." 

Når du vil flytte eller skjule elementer eller foreta flere endringer, kan du bruke verktøylinjen for tilpassing, tilgjengelig fra vinduet for elementegenskaper, ved å velge **Tilpass dette skjemaet**. Verktøylinjen for tilpassing finnes også på skjemaets handlingsrute under Tilpass-gruppen i kategorien **Alternativer**. Velg **Tilpass dette skjemaet** og du vil se verktøylinjen for tilpassing. 

[![Verktøylinje for tilpassing](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Verktøylinjen for tilpassing har flere tilpassingshandlinger. Velg **Velg**-verktøyet når du vil merke og endre egenskapene for mange elementer, ett om gangen. Først klikker du markeringsverktøyet, og klikk deretter elementet du vil endre egenskapene for. Når du velger et element, åpnes vinduet for elementets egenskaper, og du kan endre egenskapene for det elementet. Du kan gjenta prosessen for andre elementer i skjemaet som kan tilpasses. I noen tilfeller vil du merke et element og ser at noen av egenskapene ikke kan endres. Dette betyr at basert på måten det gjeldende elementet blir brukt på kan Dynamics 365 for Operations ikke endre denne egenskapen. Du kan for eksempel ikke skjule et felt som er nødvendig. 

Velg **flytte**-verktøyet når du vil merke og flytte et element til et annet sted i gjeldende gruppe med elementer. (Du kan ikke flytte et element utenfor den overordnede gruppen). Først klikker du flytteverktøyet, og deretter klikker du elementet du vil flytte. Når du klikker elementet du vil flytte, skanner Dynamics 365 for Operations skjemaet for å forstå hvor dette elementet kan flyttes og oppretter en serie med "slippsoner" som vises som en farget, fet linje ved siden av området der elementet kan bli slippes når du drar elementet rundt i gjeldende gruppe. 

Velg **Skjul**-verktøyet for å velge og skjule et element. Hvis du vil skjule et element, velger du bare Skjul-verktøyet og klikker elementet du vil skjule. Når du velger verktøyet Skjul, gjøres alle gjeldende skjulte elementer synlig og vises i en nedtonet container slik at du kan velge elementet for å vise det. Velg markeringsverktøyet for å se hvordan siden vil se ut med de valgte elementene skjult. Velg **sammendrag**-verktøyet når du vil vise et numerisk felt eller et strengfelt i sammendragsområdet for hurtigkategorien. Verktøyet Sammendrag gjelder bare for feltene som finnes i en inndeling i hurtigfanen. Når du velger verktøyet Sammendrag, viser Dynamics 365 for Operations alle feltene som er valgt som sammendragsfelt ved å plassere dem i en nedtonet container. Interaktivt kan du legge til og fjerne felt fra en hurtigfane for sammendrag ved å klikke feltet. 

Velg **Hopp over**-verktøyet for å fjerne et element fra sidens tastaturtabulatorsekvens. Når du velger verktøyet Hopp over, vises alle elementer som er hoppet, i en nedtonet container slik at du kan velge dem på nytt for å gjøre dem til en del av tabulatorsekvensen ved å velge et element som er hoppet over. 

Velg **Rediger**-verktøyet når du vil merke et element som redigerbart eller ikke redigerbart. Når du velger verktøyet Rediger, vises alle gjeldende ikke-redigerbare elementer i en nedtonet container slik at du kan velge å gjøre dem redigerbare. Legg merke til noen av feltene er nødvendige og kan ikke gjøres ikke-redigerbare. Disse feltene vises med et hengelås-ikon ved siden av seg. 

Velg verktøyet **Legg til** for å legge til et felt på siden. Du kan ikke opprette et nytt felt med verktøyet Legg til, men du kan legge til felt som er en del av den gjeldende sidedefinisjonen, men som ikke vises på siden. Når du velger verktøyet Legg til, må du først å velge gruppen eller området der du vil legge til et felt. En dialogboks viser listen over felt som er knyttet til inndelingen som du har valgt. Du kan velge ett eller flere felt for å legge til, og klikke Sett inn fra denne dialogboksen. Hvis du senere vil fjerne et felt som du tidligere har lagt til, gjentar du prosessen, men ganske enkelt fjerner avmerkingen for feltet som du tidligere har lagt til. 

Velg **Behandle**-knappen for å se en liste over alternativer for fargehåndtering relatert til alle tilpasninger for den gjeldende siden. 

Velg **Fjern** til å tilbakestille siden til standard, installert tilstand. Alle tilpasninger på gjeldende side vil bli fjernet. Det finnes ingen handling Angre, så bare bruke dette alternativet når du er sikker på at du vil tilbakestille siden. 

Velg **Import** å bruke en tilpasning fra en tilpasningsfil som du eller noen andre har opprettet for denne siden. Import av en tilpasning fjerner eventuelle tilpasninger du har utført på hele siden, og bruker i stedet alle de personlige tilpasningene fra den valgte filen. Hvis du vil lagre eller dele en personlig tilpasning, og velger du deretter alternativet **Eksporter** for å lagre de personlige tilpasningene i en fil. 

Velg knappen **Lukk** for å lukke verktøylinjen og returnere siden til den tidligere interaktive tilstanden. 

Lagring er implisitt med tilpassingsverktøylinjen. Dine personlige innstillinger trer i kraft umiddelbart når du gjør dem og det er ikke nødvendig å klikke en **Lagre**-knapp. I noen tilfeller vil du se en hengelås-ikonet ved siden av et element når du velger et verktøy. Dette betyr at i rekkefølge for at siden skal fungere som de skal, kan du ikke endre egenskapene knyttet til det valgte verktøyet. Når tilpasningsverktøylinjen åpnes, blir siden ikke-interaktiv. Du kan ikke legge inn data eller vise eller skjule inndelinger.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Eksplisitt tilpassing: legge til flis eller liste i et arbeidsområde
Noen sider med lister har en ekstra personlig tilpasning-funksjon tilgjengelig i sin handlingsrute i Tilpass-gruppen i kategorien Alternativer. Velg **Legg til arbeidsområde** for å åpne rullegardinlisten som gir deg muligheten til å vise informasjonen i gjeldende liste (filtrert og sortert eller standard) på et arbeidsområde som en liste eller en sammendragsflis (som kan brukes til å vise antall elementer i listen). 

[![Legg til i arbeidsområde](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

For å legge til en liste i arbeidsområdet, først sorter eller filtrer listen med informasjonen slik som du vil se den på arbeidsområdet, og velg deretter dialogboksen Legg til i arbeidsområde. Velg deretter det ønskede arbeidsområdet og velg **listen** fra rullegardinlisten Presentasjon. Når du velger **listen**, åpnes en dialogboks der du kan velge kolonnene du vil vise i listen, og etiketten for listen slik den vil vises i arbeidsområdet. 

Hvis du vil legge til en flis i et arbeidsområde, må du først filtrere listen som skal representere dataene du vil ha summert (eller vil ha rask tilgang til). Åpne deretter nedtrekksdialogen Legg til arbeidsområde. Velg deretter det ønskede arbeidsområdet og velg **Flis** fra rullegardinen Presentasjon. Når du velger **Flis**, åpnes en dialogboks der du angir en flisetikett og bestemmer flisen skal vise et antall. Når flisen plasseres på et arbeidsområde, kan du åpne den gjeldende siden fra arbeidsområdet, og den viser listen med informasjon som er knyttet til flisen. 

Når listen eller flisen blir lagt til i et arbeidsområde, kan du deretter åpne dette arbeidsområdet og endre rekkefølgen for listen eller flisen i gruppen der den er plassert.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Eksplisitt tilpassing: legge til et sammendrag fra et arbeidsområde på et instrumentbord
Noen arbeidsområder inneholder antall paneler (side ved side med tall på dem) som du vil også se på dashbordet. Høyreklikk et antall ark i et arbeidsområde, og velg **Tilpass**. Velg **Fest til instrumentbord**. Neste gang du går til (og oppdaterer) det valgte instrumentbordet, ser du det nummeret under dette arbeidsområdets navigasjonsflis på instrumentbordet.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Eksplisitt tilpassing: tilpasse instrumentbordet
Instrumentbordet er ofte den første siden som vises når du åpner Dynamics 365 for Operations. Du kan tilpasse instrumentbordet for å endre navn på arbeidsområdets navigasjonsfliser, for å vise bare flisene som du ønsker å vise, endre navn på flisene, eller til å ordne flisene i rekkefølgen du vil se dem i. For å tilpasse instrumentbordet velger du en hvilken som helst flis og høyreklikker for å åpne en hurtigmeny. På hurtigmenyen velger du **Tilpass**. Hvis den valgte flisen er én som du ønsker å skjule eller gi nytt navn eller hoppe over, kan du gjøre denne endringen direkte i egenskapsvinduet som vises. Hvis du vil ordne fliser, velger du **Tilpass dette skjemaet** i vinduet Egenskap for å åpne verktøylinjen for personlig tilpasning. Du kan deretter bruke verktøyet Flytt for å ordne flisene.

## <a name="administration-of-personalization"></a>Administrasjon av tilpasning
Det er mulig å tilpasse en side og dele den med andre brukere ved å eksportere den tilpassede siden og be andre brukere om å navigere til den tilpassede siden og importere tilpasningsfilen som du har opprettet. Hvis en bruker har administratorrettigheter, kan de også administrere tilpasninger for andre brukere på siden for **oppsett for tilpassing**. Gå til siden b. På siden **Tilpassing** finner du to kategorier, én kalt **System** og én kalt **Brukere**. 

**System:** Dette er der du kan midlertidig deaktivere eller "Slå av" alle tilpasninger i systemet. Dette sletter ikke tilpasninger, i stedet tilbakestilles alle skjemaer til standardtilstanden. Du kan senere reaktivere tilpasning for å bruke alle tilpasninger på nytt for alle skjemaer for brukere. Du kan også slette alle tilpasninger for alle brukere. Legg merke til at når du sletter tilpasninger, er det ikke mulig å automatisk aktivere tilpasninger på nytt fra systemet. Kontroller at du har eksportert tilpasninger du vil importere senere før du utfører dette trinnet. 

**Brukere:** Dette er der du kan bestemme for hver bruker om de kan utføre enten implisitt eller eksplisitt tilpasning. Du kan også bestemme om hver bruker kan utføre implisitt eller eksplisitt tilpasning på et bestemt skjema. Til slutt kan du importere eller eksportere eller slette en tilpasning for hver bruker. 

**Obs!** I den første versjonen tillater tilpassingsadministrasjon bare behandling basert på bruker etter bruker.




