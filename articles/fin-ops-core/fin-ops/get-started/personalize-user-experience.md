---
title: Tilpasse brukeropplevelsen
description: Dette emnet forklarer hvordan du kan tilpasse appen.
author: jasongre
manager: AnnBe
ms.date: 10/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3cf2b82470887ee617704b72e47a53d299911e3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811537"
---
# <a name="personalize-the-user-experience"></a>Tilpasse brukeropplevelsen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet forklarer hvordan du kan tilpasse appen.

Det finnes tre grunnleggende klasser med tilpasninger.

- Tilpasninger gjort på en konfigurasjonsside. Eksempler er fargetema og tidssone.
- Tilpasninger som er knyttet til sidebruk. Disse tilpasningene kalles *implisitte* tilpasninger. For eksempel holder systemet oversikt over bredden på rutenettkolonnene hvis du endrer dem, og tilstanden for vist eller skjult for hurtigfanene.
- Tilpasninger en bruker gjør for utseendet på en side ved å endre hvordan et element fungerer eller vises på den siden, ofte gjennom en interaktiv tilpasningsmodus. Disse tilpasningene kalles *eksplisitte* tilpasninger. Brukeren kan for eksempel legge til, skjule eller omorganisere elementene på siden.

Alle tilpasninger som en bruker gjør, er bare for denne brukeren, uavhengig av tilpasningstypen eller firmaet som brukeren samhandler med. Endringene som én bruker gjør på en side, påvirker ikke andre brukere i systemet.

## <a name="system-wide-options-for-the-current-user"></a>Systemomfattende alternativer for gjeldende bruker

Siden **Brukeralternativer** inneholder flere systeminnstillinger for gjeldende bruker. For å åpne siden **Brukeralternativer** velger du **Innstillinger**-knappen (tannhjulsymbolet) på navigeringslinjen, og deretter velger du **Brukeralternativer**. Siden **Brukeralternativer** har fire faneblader med ulike brukerinnstillinger:

- **Visuelt** – Velg et fargetema og standardstørrelsen på elementer på sidene.
- **Innstillinger** – Velg standardverdier som brukes hver gang du åpner systemet. Disse verdiene inkluderer firmaet, startsiden og standard visnings-/ redigeringsmodus. (Vis-/redigeringsmodus avgjør om en side er låst for visning eller åpnet for redigering hver gang du åpner den.) Denne kategorien omfatter også alternativer for språk, tidssone, og dato, klokkeslett og tallformater. Denne kategorien inneholder dessuten flere diverse innstillinger som varierer fra versjon til versjon.
- **Konto:** – Juster brukernavnet ditt og andre kunderelaterte alternativer.
- **Arbeidsflyt** – Velg arbeidsflytrelaterte alternativer.

I tillegg til å endre brukerinnstillinger kan du bruke siden **Brukeralternativer** til å vise og slette bruksdata og tilpasninger. Bare velg **Bruksdata** i handlingsruten.

Når du bruker appen, lagres mange av valgene, slik at det blir lettere for deg å bruke systemet neste gang. I kategorien **Tilpassing** kan du vise og administrere de personlige endringene du har gjort på sider i systemet. I denne kategorien kan du også tilbakestille bildeforklaringer for funksjonen (det vil si popup-vinduene som introduserer nye systemfunksjoner). Du vil deretter bli varslet igjen om tidligere oppdagede funksjoner.

> [!NOTE]
> Hvis funksjonen [Lagrede visninger](saved-views.md) er aktivert, kan du vise og behandle tilpasningene ved å velge **Tilpassing** i handlingsruten på siden **Brukeralternativer** .

## <a name="implicit-personalizations"></a>Implisitte tilpasninger

Implisitte tilpasninger er tilpasninger som utføres ved å samhandle med kontroller som lagrer gjeldende synlige tilstand.

- **Rutenettkolonner:** – Du kan justere bredden på en kolonne i et rutenett ved å velge størrelseslinjen til venstre eller høyre for kolonneoverskriften og deretter dra den til venstre eller høyre helt til kolonnen har ønsket bredde. Appen lagrer bredden som du angir for en kolonne. Neste gang du åpner siden som inneholder rutenettet, endres størrelsen til denne bredden.
- **Hurtigfaner** – Noen sider har utvidbare deler kalt *Hurtigfaner*. Appen lagrer informasjon om hurtigfanene som du har vist og skjult. Neste gang du åpner siden, vil de samme hurtigfanene enten vises eller skjules, basert på siste samhandling med siden. I noen tilfeller kan du bidra til å forbedre systemytelsen ved å skjule en hurtigfane, fordi appen ikke trenger å hente informasjonen om hurtigfaner før hurtigfanen utvides. Som forklart senere i dette emnet kan du også endre rekkefølgen for hurtigfanene på en side.
- **Faktabokser** – Noen sider har en **Relatert informasjon**-rute som viser skrivebeskyttet informasjon som er knyttet til gjeldende emne på siden. Hver del i ruten **Relatert informasjon** kalles en *Faktaboks*. Du kan vise eller skjule ruten **Relatert informasjon**, og du kan også vise eller skjule individuelle faktabokser. Appene lagrer disse innstillingene. Deretter, neste gang du åpner siden, vil ruten **Relatert informasjon** og de individuelle faktaboksene enten utvides eller skjules basert på den siste samhandlingen med siden. I noen tilfeller kan du bidra til å forbedre systemytelsen ved å skjule en faktaboks fordi appen ikke trenger å hente informasjonen for faktabokser før de utvides.
- **Handlingsruter** – En *Handlingsrute* vises øverst på de fleste sidene. Handlingsruten inneholder knapper for mange av handlingene som du kan utføre på gjeldende side. Disse knappene er ofte organisert i kategorier. Du kan "feste" hele handlingsruten som åpen, eller du kan skjule den som standard. Neste gang du åpner siden, vil handlingsruten enten være åpen eller skjult basert på siste samhandling med siden. Hvis du låste handlingsruten åpen, vises den siste kategorien du brukte.
- **Hurtigfilter** – Et *hurtigfilter* vises over mange rutenett. Med hurtigfilter kan du filtrere rutenettet basert på en kolonne som du velger. Appen lagrer kolonnen du filtrerte på. Deretter, neste gang du åpner siden som inneholder dette rutenettet, vil rutenettet filtreres i samme kolonne. Du kan imidlertid deretter velge en annen kolonne å filtrere rutenettet på.
- **Kolonnehodefiltre** – Når du filtrerer et rutenett ved hjelp av *kolonnehodefiltre*, kan du endre filteroperatoren etter behov for å finne dataene du vil bruke. Du kan for eksempel endre operatoren fra **begynner med** til **er nøyaktig**. Hver gang du bruker et kolonnehodefilter og endrer filteroperatoren, lagrer appen endringen. Den vil deretter gjenopprette filteroperatoren neste gang du filtrerer på denne kolonnen.
- **Navigasjonsrute** – Du kan åpne *navigasjonsruten* ved å velge **Vis navigasjonsrute**-knappen øverst til venstre rute på en hvilken som helst side. (Denne knappen kalles noen ganger _**Meny**-knappen_, *hamburger*, *hamburgermeny* eller *hamburgerknapp*.) Du kan feste navigeringsruten åpen eller beholde den skjult som standard. Når du fester navigasjonsruten åpen, vil appen beholde den åpen helt til du skjuler den.

## <a name="explicit-personalizations"></a>Eksplisitte tilpasninger

Forskjellige personer og firmaer har et annet perspektiv på dataene som er viktigst for dem, og dataene de ikke trenger for måten de driver forretninger på. Du kan tilpasse måten informasjonen bestilles på og samhandles med. Du kan også angi at noe informasjon skal skjules. Disse funksjonene er nøkkelen til en personlig og produktiv erfaring og eksempler på eksplisitte tilpasninger. Eksplisitte tilpasninger er tilpasningene som du utfører eksplisitt fordi du vil endre utseendet eller virkemåten for et element eller en side.

### <a name="shortcut-menu-options"></a>Hurtigmenyvalg

Hurtigmenyer gir flere måter å endre en side eksplisitt på, slik at de passer bedre til behovene eller kravene i firmaet ditt. (En hurtigmeny er også kjent som en *høyreklikkmeny* eller *hurtigmeny*.)

Noen av mest vanlige og viktigste endringene som gjøres på en side, er tilgjengelige direkte som valg på en hurtigmeny. For eksempel, fra og med plattformoppdatering 17, hvis du vil legge til eller skjule kolonner i et rutenett, bare høyreklikker du en kolonneoverskrift og velger deretter **Legg til kolonner** eller **Skjul denne kolonnen**.

De vanligste typene eksplisitte tilpasninger er i tillegg tilgjengelige ved å høyreklikke et element og deretter velge **Tilpass**. (Vær oppmerksom på at ikke alle elementene på siden kan tilpasses.) Når du bruker denne tilpasningsmetoden, vises vinduet for elementets egenskaper.

![Tilpasse egenskapene for et element](./media/personalization-element-properties.png)

Du kan bruke egenskapsvinduet til å tilpasse et element på følgende måter:

- Endre elementetiketten.
- Skjul elementet slik at det ikke vises på siden. Dataene i feltet slettes eller endres ikke. Informasjonen vises bare ikke på siden lenger.
- Ta med informasjonen i sammendragsdelen for hurtigfanen (hvis elementet er på en hurtigfane).
- Hopp over feltet, slik at det aldri får fokus når du bruker tabulatoren gjennom siden.
- Hindre at dataene i feltet blir redigert (for en post).

Egenskapsvinduet kan inneholde andre tilpasningsfunksjoner avhengig av elementet. Egenskapsvinduet for en flis kan for eksempel la deg å fremme flisen på et instrumentbord, og egenskapsvinduet for et instrumentbord kan la deg opprette et nytt arbeidsområde på dette instrumentbordet.

### <a name="the-personalization-toolbar"></a>Verktøylinjen for tilpassing

Hvis du vil gjøre flere endringer på en side eller gjøre endringer som ikke er tilgjengelige gjennom andre mekanismer (for eksempel hvis du vil endre rekkefølgen på elementene), kan du bruke **Tilpassing**-verktøylinjen. Hvis du vil åpne **Tilpassing**-verktøylinjen, følger du et av disse trinnene:

- Velg **Tilpass dette skjemaet** i egenskapsvinduet for et element.
- Velg **Tilpass denne siden** i gruppen **Tilpass** i kategorien **Alternativer** på handlingssiden til en hvilken som helst side.
- Velg knappen **Innstillinger** (tannhjulsymbolet) i navigasjonsfeltet, og velg deretter **Tilpass**.

[![Verktøylinje for tilpassing](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigere på siden

Når verktøylinjen **Tilpassing** er åpen, er den underliggende siden skrivebeskyttet (med andre ord kan du ikke redigere data), men den er fortsatt interaktiv. Spesifikt kan du vise eller skjule ruten **Beslektet informasjon**, bytte kategorier og vise eller skjule inndelinger, på samme måte som du vanligvis utfører disse handlingene på siden. Hvis du vil bruke en tilpasning på en inndeling eller kategori som kan skjules (for eksempel skjule en hurtigfane), kan du ganske enkelt velge knappen som vises ved siden av inndelingen eller kategorien som kan skjules, når den får tastaturfokus eller når du holder musepekeren over den.

#### <a name="personalization-tools"></a>Verktøy for tilpassing

Følgende verktøy er tilgjengelige på **Tilpassing**-verktøylinjen:

- Bruk **Velg**-verktøyet til å velge og endre egenskapene for et element. Hvis du vil bruke dette verktøyet, velger du knappen **Velg** på verktøylinjen og velger deretter ønsket element. Egenskapsvinduet for elementet vises, og du kan endre egenskapene for elementet. Du kan gjenta prosessen for andre elementer som kan tilpasses på siden. Vær oppmerksom på at noen personlige egenskaper kanskje ikke er tilgjengelige i noen scenarioer. Du kan for eksempel ikke låse et felt som er nødvendig.
- Bruk **Skjul**-verktøyet for å skjule et element på siden. Hvis du vil bruke dette verktøyet, velger du knappen **Skjul** på verktøylinjen, og deretter velger du elementet som skal skjules. Når du bruker **Skjul**-verktøyet, vil alle elementer som ligger skjult, gjøres synlige, men de vises i en skyggelagt container. Deretter kan du få et element synlig ved å merke det. Hvis du vil se hvordan siden vil se ut når elementer er skjult, bytter du til et annet tilpasningsverktøy.
- Bruk verktøyet **Legg til et felt** for å legge til et felt på siden. Når du bruker dette verktøyet, kan du bare legge til felt som er del av sidedefinisjonen. Hvis du vil ha informasjon om hvordan du oppretter nye felt som ikke er en del av den gjeldende sidedefinisjonen, kan du se [Opprette og arbeide med egendefinerte felt](user-defined-fields.md). Når du har valgt knappen **Legg til et felt** på verktøylinjen, må du først velge gruppen eller området der du vil legge til et felt. En dialogboks viser listen over felt som er knyttet til den valgte gruppen eller området. I dialogboksen velger du ett eller flere felt og deretter **Sett inn**. Hvis du vil fjerne et felt som du la til tidligere, gjentar du prosessen, men fjerner merkingen av feltet i dialogboksen.
- Bruk **Flytt**-verktøyet når du vil flytte et element til et annet sted i den gjeldende gruppen med elementer. Legg merke til at du ikke kan flytte et element utenfor den overordnede gruppen. Hvis du vil bruke dette verktøyet, velger du knappen **Flytt** på verktøylinjen, og deretter velger du elementet som skal flyttes. Når du velger et element, bestemmer appen stedene der elementet kan flyttes. Disse stedene kalles *slippsoner*. Når du drar elementet rundt i gjeldende gruppe, vises hver "slippsone" som en farget, fet linje ved siden av området der elementet kan slippes.
- Bruk **Hopp over**-verktøyet for å fjerne et element fra sidens tastaturtabulatorsekvens. Når du velger **Hopp over**-knappen på verktøylinjen, vil alle elementer som hoppes over, vises i en skyggelagt container. Du kan interaktivt fjerne eller legge til felt i kategorisekvensen.
- Bruk **Vis i hode**-verktøyet når du vil at et felt skal vises i sammendragsdelen i hurtigfanen. Når du velger knappen **Vis i hode** på verktøylinjen, vil alle felt som er merket som sammendragsfelt, vises med en skyggelagt beholder. Interaktivt kan du legge til felt i hurtigfanen sammendrag og fjerne felt fra den ved å velge feltene.
- Bruk **Lås**-verktøyet når du vil merke et element som enten er redigerbart eller ikke redigerbart. Når du velger **Lås**-knappen på verktøylinjen, vil alle elementer som ikke kan redigeres, vises i en skyggelagt container. Du kan deretter gjøre dem redigerbare på nytt. Legg merke til at noen felt er nødvendige og ikke kan gjøres ikke-redigerbare. Et hengelåssymbol ved siden av disse feltene.
- Bruk knappen **Legg til en PowerApp** for å bygge inn en app som ble opprettet ved hjelp av Microsoft PowerApps på siden. Hvis du vil ha mer informasjon om hvordan du bygger inn en PowerApps-app på en side, se [Bygge inn PowerApps-apper](embed-power-apps.md).
- Bruk verktøyet **Fjern** for å tilbakestille siden til standard installert tilstand. Alle tilpasninger på gjeldende side vil bli fjernet. Det finnes ingen angrehandling. Bruk derfor dette verktøyet bare hvis du er sikker på at du vil tilbakestille siden.
- Bruk verktøyet **Importer** for å laste en tilpasning fra en fil som du eller noen andre har opprettet. Når du importerer personlige tilpasninger for en side, kan du velge om de skal legges til eller erstatte alle eksisterende personlige tilpasninger for siden. Det finnes ingen angrehandling. Etter at du har importert personlige tilpasninger, må du derfor fjerne eller angre endringene du ikke vil ha, manuelt.
- Bruk verktøyet **Eksporter** til å lagre dine tilpasninger for siden i en fil. Du kan deretter dele dine tilpasninger med andre brukere. Disse brukerne trenger bare å importere filen som inneholder dine tilpasninger for siden.
- Velg **Lukk**-knappen for å lukke **Tilpasning**-verktøylinjen og returnere siden til den forrige interaktive tilstanden.

Når verktøylinjen for **Tilpasning** er brukt, vil tilpasningene vanligvis gjelde så snart du lager dem. Hvis imidlertid funksjonen [Lagrede visninger](saved-views.md) er aktivert, må du eksplisitt lagre personlige tilpasninger til en visning du velger.

I noen tilfeller når du velger et verktøy, vises et hengelåssymbol ved siden av et element. Dette symbolet indikerer at du ikke kan endre egenskapene for elementet som er knyttet til det valgte verktøyet, fordi endringer i disse egenskapene vil hindre at siden fungerer som den skal.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Legge til en flis, liste eller kobling til et arbeidsområde

For enkelte sider som inneholder lister, er tilpasningsfunksjonen **Legg til i arbeidsområde** tilgjengelig i gruppen **Tilpass** i kategorien **Alternativer** i handlingsruten. Med denne funksjonen kan du skyve relevant informasjon fra gjeldende liste til et bestemt arbeidsområde. Informasjonen som vises i arbeidsområdet, kan baseres på hele listen eller en filtrert og sortert versjon av listen. Du kan også angi om informasjonen skal vises i arbeidsområdet som en liste, som en sammendragsflis som kan vise antall elementer i listen, eller som en kobling.

> [!NOTE]
> Hvis funksjonen [Lagrede visninger](saved-views.md) er aktivert, er innholdet du dytter til et arbeidsområde, direkte koblet til en visning. Visningsspørringen brukes til å hente data i arbeidsområdet, og tilsvarende flis eller kobling i arbeidsområdet åpner siden til denne visningen, slik at visningensspørring og personlige tilpasninger brukes på den.

[![Legg til i arbeidsområde](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Hvis du vil legge til et arbeidsområde, sorterer eller filtrerer du først på siden, slik at den viser informasjonen slik du vil at den skal vises i arbeidsområdet. (Hvis funksjonen for lagrede visninger er aktivert, kan du ikke fortsette før du har lagret en visning som har disse betingelsene.) Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Liste**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan velge hvilke kolonner som skal vises i listen i arbeidsområdet. Du kan også angi etiketten som brukes for listen i arbeidsområdet.
- Hvis du vil legge til en flis i et arbeidsområde, må du først filtrere listen på siden slik at den viser dataene som skal oppsummeres, eller som du vil ha rask tilgang til. (Hvis funksjonen for lagrede visninger er aktivert, kan du ikke fortsette før du har lagret en visning som har disse betingelsene.) Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Flis**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan angi etiketten som skal brukes for flisen i arbeidsområdet. Du kan også angi om ruten skal vise et tall. Når flisen er lagt til i arbeidsområdet, kan du velge den for å åpne den gjeldende siden fra arbeidsområdet. Deretter kan du vise den filtrerte listen som er knyttet til brikken.
- Hvis du vil legge til en kobling i et arbeidsområde, filtrerer du først filteret på siden slik at den viser dataene du er interessert i. (Hvis funksjonen for lagrede visninger er aktivert, kan du ikke fortsette før du har lagret en visning som har disse betingelsene.) Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Kobling**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan angi etiketten som skal brukes for koblingen. Du kan også angi en etikett for en ny inndeling som inneholder denne koblingen.

Når du har lagt til listen, flisen eller koblingen i et arbeidsområde, kan du åpne arbeidsområdet og endre rekkefølgen på elementene i den etter ønske.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Legge til et sammendrag fra et arbeidsområde til et instrumentbord

Noen arbeidsområder inneholder fliser med antall (det vil si fliser som inneholder tall), og du vil kanskje at disse flisene skal vises på instrumentbordet også. I et arbeidsområde høyreklikker du en flis for antall, velger **Tilpass**, og deretter velger du **Fest til instrumentbord** i egenskapsvinduet til flisen. Deretter, neste gang du åpner og oppdaterer det valgte instrumentbordet, vil antallet vises under arbeidsområdets navigasjonsflis. Du kan velge det antallet for å gå direkte til dataene det representerer.

### <a name="personalizing-your-dashboard"></a>Tilpasse instrumentbordet

Instrumentbordet er ofte den første siden som vises når du åpner appen. Du kan tilpasse instrumentbordet slik at det viser bare arbeidsområdeflisene som du vil se. Du kan også omorganisere flisene slik at de vises i rekkefølgen du vil se dem i, gi nytt navn til arbeidsområdenavigasjonsflisene eller legge til en ny arbeidsområdeflis.

For å tilpasse instrumentbordet høyreklikker du på en flis og velger **Tilpass** til å åpne flisens egenskapsvindu.

- Hvis du vil skjule eller gi nytt navn til den valgte flisen, kan du gjøre denne endringen direkte i egenskapsvinduet.
- For å omorganisere arbeidsområdeflisene velger du **Tilpass dette skjemaet** i egenskapsvinduet for å åpne **Tilpasning**-verktøylinjen. Du kan deretter bruke verktøyet **Flytt** for å omorganisere flisene slik du vil.
- For å legge til en arbeidsområdeflis velger du **Legg til et arbeidsområde** i egenskapsvinduet. En ny arbeidsområdeflis opprettes nederst på instrumentbordet. Du kan endre navn på denne nye arbeidsområdeflisen slik du vil. Du kan også legge til lister, fliser og koblinger til arbeidsområdet, som beskrevet i [Legge til lister, fliser eller koblinger til arbeidsområder](#adding-a-tile-list-or-link-to-a-workspace)-delen i dette emnet.

## <a name="administration-of-personalizations"></a>Administrasjon av tilpasninger

Når du tilpasser en side, kan du dele dine personlige tilpasninger med andre brukere ved å eksportere den tilpassede siden. Deretter kan du be andre brukere om å åpne den tilpassede siden og importere den tilpassede filen du opprettet. Du kan også gi dine tilpasninger til en bruker som har administratorrettigheter. Brukeren kan deretter bruke tilpasningsfilen til mange brukere samtidig.

Brukere som har administratorrettigheter, kan også administrere tilpasninger for andre brukere på siden for **Tilpasning**.

For kunder som ikke har aktivert funksjonen [Lagrede visninger](saved-views.md), har denne siden fire kategorier:

- **Bruk** – Du kan importere eller velge en tilpasning for én eller flere brukere. Hvis du vil bruke en tilpasning på én eller flere brukere, må du først velge en rolle og brukere som har denne rollen. Velg deretter en eksisterende tilpasning som skal brukes på de valgte brukerne, eller importer en tilpasningsfil. Tilpasningen blir godkjent og brukes for alle de valgte brukerne neste gang de åpner den valgte siden.
- **Fjern** – Du kan fjerne alle tilpasninger for en side eller et arbeidsområde for én eller flere brukere. Velg først en side eller et arbeidsområde for å se en liste over brukerne som har tilpasset den. Velg deretter brukerne som skal ha fjernet tilpasninger for denne siden eller arbeidsområdet, og velg deretter **Fjern**. Alle tilpasninger som de valgte brukerne har brukt på den valgte siden eller arbeidsområdet, slettes. Du kan ikke angre denne handlingen. Hvis en tilpasning ble lagret for siden eller arbeidsområdet, kan tilpasningen importeres på nytt.
- **Brukere** – Velg en bruker for å vise en liste over sider som brukeren har tilpasset. Du kan deretter aktivere eller deaktivere den valgte brukerens mulighet til å bruke tilpassinger for bestemte sider eller for hele systemet. Du kan også importere, eksportere eller fjerne en tilpassing for brukeren. I tillegg kan du tilbakestille bildeforklaringer for funksjonen for brukeren. Hvis brukeren tidligere har ignorert alle popup-vinduer som introduserer nye funksjoner, vil de da vises igjen neste gang brukeren støter på disse funksjonene.
- **System** – Du kan midlertidig deaktivere tilpasninger for alle brukere i systemet. I dette tilfellet slettes alle personlige tilpasninger for alle brukere, og alle sidene tilbakestilles til standardtilstanden. Hvis du reaktiverer tilpasning senere, vil alle tilpasninger bli brukt på nytt. Du kan også permanent slette alle tilpasninger for alle brukere i systemet. Tilpasninger som er slettet, kan ikke gjenopprettes. Før du utfører denne oppgaven må du eksportere tilpasninger du kanskje vil bruke senere.

For kunder som har aktivert funksjonen [Lagrede visninger](saved-views.md), har siden **Tilpasning** fire kategorier:

- **Publiserte visninger** – Disse visningene er publisert i organisasjonen. Hvis du vil endre brukerne som er målrettet mot disse visningene, kan du endre sikkerhetsrollene eller de juridiske enhetene som er knyttet til hver visning. Du kan også eksportere eller slette én eller flere publiserte visninger.
- **Upubliserte visninger** – Disse visningene er malvisninger som er importert til systemet, men som ennå ikke er publisert. Du kan publisere, eksportere eller slette disse visningene.
- **Personlige visninger** – Disse visningene er opprettet av brukere i systemet. Du kan publisere en personlig visning til organisasjonen eller kopiere én eller flere av disse visningene til andre brukere. Du kan også eksportere eller slette disse visningene etter behov.
- **Brukere** – Velg en bruker for å vise en liste over sider som brukeren har tilpasset. Du kan deretter aktivere eller deaktivere den valgte brukerens mulighet til å bruke tilpassinger for bestemte sider eller for hele systemet. Du kan også importere, eksportere eller fjerne en tilpassing for brukeren. I tillegg kan du tilbakestille bildeforklaringer for funksjonen for brukeren. Hvis brukeren tidligere har ignorert alle popup-vinduer som introduserer nye funksjoner, vil de da vises igjen neste gang brukeren støter på disse funksjonene.
- **System** – Du kan midlertidig deaktivere tilpasninger for alle brukere i systemet. I dette tilfellet slettes alle personlige tilpasninger for alle brukere, og alle sidene tilbakestilles til standardtilstanden. Hvis du reaktiverer tilpasning senere, vil alle tilpasninger bli brukt på nytt. Du kan også permanent slette alle tilpasninger for alle brukere i systemet. Tilpasninger som er slettet, kan ikke gjenopprettes. Før du utfører denne oppgaven må du eksportere tilpasninger du kanskje vil bruke senere.

Brukere som har tilgang til siden **Tilpasning**, kan også importere personlige visninger eller malvisninger ved hjelp av **Importer visninger**-knappen i handlingsruten.

## <a name="personalizing-inventory-dimensions"></a>Tilpasse lagerdimensjoner

Når du tilpasser oppsettet av lagerdimensjoner på en side, tar du hensyn til innstillingene som er opprettet ved hjelp av alternativet **Visningsdimensjoner**. Du bruker eksempelvis tilpasning for å skjule en kolonne for lagerdimensjonen for partinummer, men kolonnen vises neste gang siden åpnes. Dette skjer fordi **Dimensjonsvisning**-innstillingene kontrollerer lagerdimensjonskolonnene som vises. Innstillingene for **Dimensjonsvisning** gjelder på tvers av alle sider og overstyrer tilpassede oppsett av lagerdimensjonsfelt på enkeltsider.

I eksemplet ovenfor må du derfor fjerne lagerdimensjonen for partinummer som en del av alternativet **Visningsdimensjoner** for en side hvis du ikke vil at kolonnen for denne dimensjonen skal vises på denne siden.
