---
title: Tilpasse brukeropplevelsen
description: Dette emnet forklarer hvordan du kan tilpasse appen.
author: jasongre
manager: AnnBe
ms.date: 06/11/2019
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
ms.openlocfilehash: edf698b12f2d0bcb6035bc644537cf9ca2bb87c9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190908"
---
# <a name="personalize-the-user-experience"></a>Tilpasse brukeropplevelsen

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du kan tilpasse appen.

Det finnes tre grunnleggende klasser med tilpasninger.

- Tilpasninger gjort på en konfigurasjonsside. Eksempler er fargetema og tidssone.
- Personlige tilpasninger som er knyttet til bruk av siden, kalt *implisitte* tilpasninger. For eksempel holder systemet oversikt over bredden på rutenettkolonnene hvis du endrer dem, og tilstanden for vist eller skjult for hurtigfanene.
- Tilpasninger en bruker gjør for å endre utseendet på en side ved å endre hvordan et element fungerer eller vises på den siden, ofte gjennom en interaktiv tilpasningsmodus. Disse tilpasningene kalles *eksplisitte* tilpasninger. Brukeren kan for eksempel legge til, skjule eller endre rekkefølgen på elementene på siden.

Alle tilpasninger som en bruker gjør, er bare for denne brukeren, uavhengig av tilpasningstypen eller firmaet som brukeren samhandler med. Endringene som én bruker gjør på en side, påvirker ikke andre brukere i systemet.

## <a name="system-wide-options-for-the-current-user"></a>Systemomfattende alternativer for gjeldende bruker

Siden **Brukeralternativer** inneholder flere systeminnstillinger for gjeldende bruker. For å åpne siden **Brukeralternativer** velger du **Innstillinger**-menyen (tannhjulsymbolet) på navigeringslinjen, og deretter velger du **Brukeralternativer**. Siden **Brukeralternativer** har fire faneblader med ulike brukerinnstillinger:

- **Visuelt** – Velg et fargetema og standardstørrelsen på elementer på sidene.
- **Innstillinger** – Velg standardverdier som brukes hver gang du åpner systemet. Disse verdiene inkluderer firmaet, startsiden og standard visnings-/ redigeringsmodus. (Vis-/redigeringsmodus avgjør om en side er låst for visning eller åpnet for redigering hver gang du åpner den.) Denne kategorien omfatter også alternativer for språk, tidssone, og dato, klokkeslett og tallformat. Denne kategorien inneholder dessuten flere diverse innstillinger som varierer fra versjon til versjon.
- **Konto:** – Juster brukernavnet ditt og andre kunderelaterte alternativer.
- **Arbeidsflyt** – Velg arbeidsflytrelaterte alternativer.

I tillegg til å endre brukerinnstillinger kan du vise og slette bruksdata og tilpasninger ved å klikke på **Bruksdata**-knappen. Når du bruker programmet, huskes mange av valgene, slik at det blir lettere for deg å bruke systemet neste gang. Spesielt **Tilpassing**-kategorien lar deg vise og administrere de personlige endringene du har gjort på sider i systemet. Funksjonsbildeforklaringer, popup-vinduene som viser deg nye funksjoner i systemet (tilgjengelig i Platform update 26), kan også tilbakestilles fra denne kategorien, slik at du igjen varsles om tidligere funksjoner.  

## <a name="implicit-personalizations"></a>Implisitte tilpasninger

Implisitte tilpasninger er tilpasninger som utføres ved å samhandle med kontroller som "husker" gjeldende synlige status.

- **Rutenettkolonner:** – Du kan justere bredden på en kolonne i et rutenett ved å velge størrelseslinjen til venstre eller høyre for kolonneoverskriften og deretter dra den til venstre eller høyre helt til kolonnen har ønsket bredde. Appen lagrer bredden som du angir for en kolonne. Deretter endres kolonnen til bredden hver gang du åpner siden som inneholder dette rutenettet.
- **Hurtigfaner** – Noen sider har utvidbare deler kalt *Hurtigfaner*. Appen lagrer informasjon om hurtigfanene som du har vist og skjult. Deretter, hver gang du går tilbake til siden, vil de samme hurtigfanene enten vises eller skjules, basert på siste samhandling med siden. I noen tilfeller kan du bidra til å forbedre systemytelsen ved å skjule en hurtigfane, fordi appen ikke trenger å hente informasjonen om denne hurtigfanen før hurtigfanen utvides. Som forklart senere i dette emnet kan du også endre rekkefølgen for hurtigfanene på en side.
- **Faktabokser** – Noen sider har en del som er kjent som en *Faktaboksrute*. Denne ruten inneholder skrivebeskyttet informasjon knyttet til gjeldende emne på siden. Hver del i faktaboksruten kalles en *Faktaboks*. Du kan skjule eller vise hele faktaboksruten, og du kan også vise eller skjule individuelle faktabokser. Appene lagrer innstillingene dine. Deretter, hver gang du går tilbake til siden lagres status for faktaboksruten og de individuelle faktaboksene gjenopprettes basert på siste samhandling med siden. I noen tilfeller kan du bidra til å forbedre systemytelsen ved å skjule en faktaboks, fordi appen ikke trenger å hente informasjonen om denne faktaboksen før faktaboksen utvides.
- **Handlingsruter** – En *Handlingsrute* vises øverst på de fleste sidene. Handlingsruten inneholder knapper for mange av handlingene som du kan utføre på gjeldende side. Disse knappene er ofte organisert i kategorier. Du kan feste handlingsruten som åpen, eller du kan skjule den som standard. Deretter, neste gang du åpner siden, vil appen gjenopprette den låste tilstanden i handlingsruten. Hvis handlingsruten er festet åpen, vil appen også vise kategorien med handlinger som du brukte sist.
- **Hurtigfilter** – Et *hurtigfilter* vises over mange rutenett. Med hurtigfilter kan du filtrere rutenettet basert på en kolonne som du velger. Appen lagrer kolonnen du filtrerte på. Deretter, neste gang du åpner siden som inneholder dette rutenettet, vil rutenettet filtreres i samme kolonne. Du kan imidlertid deretter filtrere rutenettet på en annen kolonne.
- **Kolonnehodefiltre** – Når du filtrerer et rutenett ved hjelp av *Kolonnehodefiltre*, kan du endre filteroperatoren etter behov for å finne dataene du vil bruke. Du kan for eksempel endre operatoren fra **begynner med** til **er nøyaktig**. Hver gang du bruker et kolonnehodefilter og endrer filteroperatoren, lagrer appen endringen. Den vil deretter gjenopprette filteroperatoren neste gang du filtrerer på denne kolonnen.
- **Navigasjonsrute** – Du kan åpne *Navigasjonsruten* ved å velge **Meny**-knappen i venstre rute på en hvilken som helst side. (**Meny**-knappen kalles noen ganger *hamburger*, *hamburgermeny* eller *hamburgerknapp*.) Du kan feste navigeringsruten åpen eller beholde den skjult som standard. Når du fester navigasjonsruten åpen, vil appen beholde den åpen helt til du skjuler den.

## <a name="explicit-personalizations"></a>Eksplisitte tilpasninger

Forskjellige personer og firmaer har et annet perspektiv på dataene som er viktigst for dem, eller dataene de ikke trenger for måten de driver forretninger på. Du kan tilpasse måten informasjonen bestilles på og samhandles med. Du kan også angi at noe informasjon skal skjules. Disse funksjonene er nøkkelen til en personlig og produktiv erfaring og eksempler på eksplisitte tilpasninger. Eksplisitte tilpasninger er tilpasningene som du utfører eksplisitt med formålet om å endre utseendet eller virkemåten for et element eller en side.

### <a name="shortcut-menu-options"></a>Hurtigmenyvalg

Hurtigmenyer gir flere måter å endre en side eksplisitt på, slik at de passer behovene eller kravene i firmaet ditt bedre. (En hurtigmeny er også kjent som en *høyreklikkmeny* eller *hurtigmeny*.)

Noen av mest vanlige og viktigste endringene som gjøres på en side, er tilgjengelige direkte som valg på en hurtigmeny. For eksempel, fra og med plattformoppdatering 17, hvis du vil legge til eller skjule kolonner i et rutenett, bare høyreklikker du en kolonneoverskrift i rutenettet, og velg deretter **Legg til kolonner** eller **Skjul denne kolonnen**.

De vanligste typene eksplisitte tilpasninger er i tillegg tilgjengelige ved å høyreklikke et element og deretter velge **Tilpass**. (Vær oppmerksom på at ikke alle elementene på siden kan tilpasses.) Når du bruker denne metoden tilpasning, vises vinduet for elementets egenskaper.

![Tilpasse egenskapene for et element](./media/personalization-element-properties.png)

Du kan bruke egenskapsvinduet til å tilpasse et element på følgende måter:

- Endre elementetiketten.
- Skjul elementet slik at det ikke vises på siden. Dataene i feltet slettes eller endres ikke. Informasjonen vises bare ikke på siden lenger.
- Ta med informasjonen i sammendragsdelen for hurtigfanen (hvis elementet er på en hurtigfane).
- Hopper over feltet når du trykker Tab for å flytte mellom feltene på siden.
- Hindre at dataene i feltet (for en post) blir redigert.

Egenskapsvinduet kan inneholde andre tilpasningsfunksjoner avhengig av elementet. Egenskapsvinduet for en flis kan for eksempel la deg å fremme flisen på et instrumentbord, og egenskapsvinduet for et instrumentbord kan la deg opprette et nytt arbeidsområde på dette instrumentbordet.

### <a name="the-personalization-toolbar"></a>Verktøylinjen for tilpassing

Hvis du vil gjøre flere endringer på en side eller gjøre endringer som ikke er tilgjengelige gjennom andre mekanismer (for eksempel endre rekkefølgen på elementene), kan du bruke **Tilpassing**-verktøylinjen. For å åpne **Tilpasning**-verktøylinjen velg **Tilpass dette skjemaet** i egenskapsvinduet for et element. Du kan også velge **Tilpass dette skjemaet** i **Tilpass**-gruppen i **Alternativer**-kategorien på handlingsruten på hver side.

[![Verktøylinje for tilpassing](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigere på siden

Muligheten til å navigere på siden mens **Tilpassing-verktøylinjeen** er åpen, avhenger av plattformversjonen du kjører.

- Før plattformoppdatering 19, mens **Tilpassing**-verktøylinjen er åpen, er siden skrivebeskyttet (du kan ikke angi noe), og ikke-interaktiv (du kan bare gjøre endringer i elementene som vises på siden). Hvis du vil gjøre endringer i elementer i en skjult inndeling eller en annen kategori, må du lukke **Tilpassing**- verktøylinjen, utvide en inndeling eller bytte til den ønskede kategorien, og åpne deretter **Tilpassing**-verktøylinjen.

- Fra og med plattformoppdateringen 19, hvis **Tilpassing**-verktøylinjen er åpen, siden er fortsatt skrivebeskyttet, men er mye mer interaktiv. Spesifikt kan du utvide eller skjule faktaboksruten, bytte kategorier og utvide eller skjule deler mens **Tilpassing**-verktøylinjen er åpen, på samme måte som du vanligvis gjør på siden. Hvis du vil bruke en personlig endring på en inndeling eller kategori som kan skjules (for eksempel skjule en hurtigfane), vil du utløse knappen som vises ved siden av inndelingen eller kategorien som kan skjules, når den får tastaturfokus, eller når du holder musepekeren over den.

#### <a name="personalization-tools"></a>Verktøy for tilpassing

Følgende verktøy er tilgjengelige på **Tilpassing**-verktøylinjen:

- Bruk **Velg**-verktøyet til å velge og endre egenskapene for et element. Velg **Velg**-verktøyet og deretter elementet du vil endre egenskapene for. Når du velger et element, vises vinduet for elementets egenskaper, og du kan endre egenskapene for det elementet. Du kan gjenta prosessen for andre elementer som kan tilpasses på denne siden. På grunn av måten enkelte elementer brukes på, vil ikke appen la deg endre noen av egenskapene. Derfor, når du velger et element, kan du se at noen av egenskapene ikke kan endres. Du kan for eksempel ikke skjule et felt som er nødvendig.
- Bruk **Flytt**-verktøyet når du vil flytte et element til et annet sted i den gjeldende gruppen med elementer. (Du kan ikke flytte et element utenfor den overordnede gruppen). Velg **Flytt**-verktøyet, og velg deretter elementet du vil flytte. Når du velger et element, søker appen på siden for å finne ut hvor elementet kan flyttes. Deretter opprettes det en rekke "slippsoner." Når du drar elementet rundt i gjeldende gruppe, vises hver "slippsone" som en farget, fet linje ved siden av området der elementet kan slippes.
- Bruk **Skjul**-verktøyet for å skjule et element på siden. Velg **Skjul**-verktøyet, og velg deretter elementet du vil skjule. Når du velger **Skjul**-verktøyet, vil alle elementer som ligger skjult, gjøres synlige og vises i en skyggelagt beholder. Du kan deretter vise dem igjen. Ved å velge **Velg**-verktøyet kan du se hvordan siden vil se ut når de valgte elementene er skjult.

    - Fra og med plattformoppdatering 18 kan du skjule obligatoriske felt og inndelinger som inneholder obligatoriske felt. Dermed kan du opprette en forenklet opplevelse der obligatoriske felt som er standard innen forretningslogikk, ikke vises. Skjulte obligatoriske felt blir også midlertidig gjort synlig hvis de er tomme når lagring forsøkes.

- Bruk **Sammendrag**-verktøyet når du vil at et element skal vises i hurtigfanesammendragsdelen. Verktøyet Sammendrag gjelder bare for feltene som finnes i en inndeling i hurtigfanen. Når du velger **Sammendrag**-verktøyet, vil alle felt som er merket som sammendragsfelt, vises med en skyggelagt beholder. Interaktivt kan du legge til felt i hurtigfanen sammendrag og fjerne felt fra hurtigfanesammendraget ved å velge feltene.
- Bruk **Hopp over**-verktøyet for å fjerne et element fra sidens tastaturtabulatorsekvens. Når du velger **Hopp over**-verktøyet, vil alle elementer som hoppes over, vises i en skyggelagt beholder. Du kan deretter gjøre dem til en del av tabulatorsekvensen igjen.
- Bruk **Rediger**-verktøyet når du vil merke et element som enten er redigerbart eller ikke redigerbart. Når du velger **Rediger**-verktøyet, vil alle elementer som hoppes over som ikke kan redigeres, vises i en skyggelagt beholder. Du kan deretter gjøre dem redigerbare på nytt. Legg merke til at noen felt er nødvendige og ikke kan gjøres ikke-redigerbare. Et hengelåssymbol ved siden av disse feltene.
- Bruk **Sett inn**-knappen for å se en liste over elementer som kan settes inn på en side.

    - Velg **Felt**-verktøyet under **Sett inn** for å legge til et felt på siden. Når du bruker **Felt**-verktøyet, kan du bare legge til felt som er en del av sidedefinisjonen, men som ikke vises på siden for øyeblikket. Hvis du vil ha informasjon om hvordan du oppretter nye felt som ikke er en del av den gjeldende sidedefinisjonen, kan du se [Egendefinerte felt](user-defined-fields.md). Når du har valgt **Felt**-verktøy, må du først velge gruppen eller området der du vil legge til et felt. En dialogboks viser listen over felt som er knyttet til den valgte gruppen eller området. I dialogboksen velger du ett eller flere felt og deretter **Sett inn**. Hvis du vil fjerne et felt som du la til tidligere, gjentar du prosessen, men fjerner merkingen av feltet i dialogboksen.
    - Velg **PowerApp**-verktøyet under **Sett inn** for å bygge inn en app som ble opprettet ved hjelp av Microsoft PowerApps på siden. Hvis du vil ha mer informasjon om hvordan du bygger inn en PowerApps-app på den side, kan du se [Bygge inn PowerApps](embed-power-apps.md).

- Velg **Behandle**-knappen for å vise en liste over administrasjonsalternativer som er relatert til alle tilpasninger for den gjeldende siden.

    - Velg **Fjern** for å tilbakestille siden til standard installert tilstand. Alle tilpasninger på gjeldende side vil bli fjernet. Det finnes ingen angrehandling. Bruk derfor dette alternativet bare hvis du er sikker på at du vil tilbakestille siden.
    - Velg **Import** å laste en tilpasning fra en fil som du eller noen andre har opprettet for siden. Alle gjeldende tilpasninger for siden er erstattet med de tilpasningene fra den valgte filen.
    - Velg **Eksporter** for å lagre dine tilpasningene for siden i en fil. Du kan dele dine tilpasninger med andre brukere. Disse brukerne trenger bare å importere filen som inneholder dine tilpasninger for siden.

- Velg **Lukk**-knappen for å lukke **Tilpasning**-verktøylinjen og returnere siden til den forrige interaktive tilstanden.

Når **Tilpass**-verktøylinjen brukes, er lagringsoperasjoner implisitte. Din tilpasninger trer i kraft så snart du oppretter dem, og du trenger ikke å velge en **Lagre**-knapp. I noen tilfeller når du velger et verktøy, vises et hengelåssymbol ved siden av et element. Dette symbolet indikerer at du ikke kan endre egenskapene for elementet som er knyttet til det valgte verktøyet, fordi endringer i disse egenskapene vil hindre at siden fungerer som den skal.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Legge til en flis, liste eller kobling til et arbeidsområde

For noen sider som inkluderer lister, er en ekstra tilpasningsfunksjon tilgjengelig. Med **Legg til arbeidsområde**-knappen i **Tilpass** gruppen i **Alternativer**-kategorien i handlingsruten kan du vise informasjonen fra den gjeldende listen i en bestemt arbeidsområde. Du kan vise en filtrert og sortert visning av informasjonen i arbeidsområdet, eller du kan vise standardvisningen. Du kan også angi om informasjonen skal vises i arbeidsområdet som en liste, som en sammendragsflis som kan vise antall elementer i listen, eller som en kobling.

[![Legg til i arbeidsområde](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Hvis du vil legge til et arbeidsområde, sorterer eller filtrerer du først på siden, slik at den viser informasjonen slik du vil at den skal vises i arbeidsområdet. Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Liste**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan velge hvilke kolonner som skal vises i listen i arbeidsområdet. Du kan også angi etiketten som skal brukes for listen i arbeidsområdet.
- Hvis du vil legge til en flis i et arbeidsområde, må du først filtrere listen på siden slik at den viser dataene du vil skal oppsummeres, eller som du vil ha rask tilgang til. Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Flis**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan angi etiketten som skal brukes for flis i arbeidsområdet. Du kan også angi om ruten skal vise et tall. Når flisen er lagt til i arbeidsområdet, kan du velge det for å åpne den gjeldende siden i arbeidsområdet og vise den filtrerte listen som er tilknyttet flisen.
- Hvis du vil legge til en kobling i et arbeidsområde, filtrerer du først filteret på siden slik at den viser dataene du er interessert i. Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Kobling**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan angi etiketten som skal brukes for koblingen. Du kan også angi en etikett for en ny inndeling som skal inneholde denne koblingen.

Når listen, flisen eller koblingen er lagt til i et arbeidsområde, kan du åpne arbeidsområdet og endre rekkefølgen på elementene i den etter ønske.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Legge til et sammendrag fra et arbeidsområde til et instrumentbord

Noen arbeidsområder inneholder fliser med antall (det vil si fliser som inneholder tall), og du vil kanskje at disse flisene skal vises på instrumentbordet også. Høyreklikk en antallflis i arbeidsområde, og velg deretter **Tilpass**. I egenskapsområdet for flisen velger du deretter **Fest til instrumentbord**. Neste gang du åpner (og oppdaterer) det valgte instrumentbordet, vil antallet vises under arbeidsområdets navigasjonsflis. Du kan velge det antallet for å gå direkte til dataene det representerer.

### <a name="personalizing-your-dashboard"></a>Tilpasse instrumentbordet

Instrumentbordet er ofte den første siden som vises når du åpner appen. Du kan tilpasse instrumentbordet slik at det viser bare arbeidsområdeflisene som du vil se. Du kan også omorganisere flisene slik at de er i rekkefølgen du vil se dem i, gi nytt navn til arbeidsområdenavigasjonsflisene, eller legg til en helt ny arbeidsområdeflis.

For å tilpasse instrumentbordet høyreklikker du på en flis og velger **Tilpass** til å åpne flisens egenskapsvindu.

- Hvis du vil skjule eller gi nytt navn til den valgte flisen, kan du gjøre denne endringen direkte i egenskapsvinduet.
- For å omorganisere arbeidsområdeflisene velger du **Tilpass dette skjemaet** i egenskapsvinduet for å åpne **Tilpasning**-verktøylinjen. Du kan deretter bruke verktøyet **Flytt** for å ordne flisene slik du vil.
- For å opprette en arbeidsområdeflis velger du **Legg til et arbeidsområde** i egenskapsvinduet. En ny arbeidsområdeflis opprettes nederst på instrumentbordet. Du kan endre navn på denne nye arbeidsområdeflisen slik du vil. Du kan også legge til lister, fliser og koblinger til arbeidsområdet, som beskrevet i [Legge til lister, fliser eller koblinger til arbeidsområder](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace)-delen i dette emnet.

## <a name="administration-of-personalization"></a>Administrasjon av tilpasning

Når du tilpasser en side, kan du dele dine personlige tilpasninger med andre brukere ved å eksportere den tilpassede siden. Deretter kan du be andre brukere om å åpne den tilpassede siden og importere den tilpassede filen du opprettet. Du kan også gi din tilpasning til en bruker som har administratorrettigheter. Brukeren kan deretter bruke tilpasningsfilen til mange brukere samtidig.

Brukere som har administratorrettigheter, kan også administrere tilpasninger for andre brukere på siden for **tilpassing**. Denne siden har fire kategorier:

- **Bruk** – Du kan importere eller velge en tilpasning for én eller flere brukere. Hvis du vil bruke en tilpasning på én eller flere brukere, må du først velge en rolle og brukere som har denne rollen. Velg deretter en eksisterende tilpasning som skal brukes på de valgte brukerne, eller importer en tilpasningsfil. Tilpasningen blir godkjent og brukes for alle de valgte brukerne neste gang de åpner den valgte siden.
- **Fjern** – Du kan fjerne alle tilpasninger for en side eller et arbeidsområde for én eller flere brukere. Velg først en side eller et arbeidsområde for å se en liste over brukerne som har tilpasset den. Velg deretter brukerne som skal ha fjernet tilpasninger for denne siden eller arbeidsområdet, og velg deretter **Fjern**. Alle tilpasninger som de valgte brukerne har brukt på den valgte siden eller arbeidsområdet, slettes. Du kan ikke angre denne handlingen. Hvis en tilpasning ble lagret for siden eller arbeidsområdet, kan tilpasningen importeres på nytt.
- **Administrer per bruker** – Velg en bruker for å vise listen over sider som brukeren har tilpasset. Du kan deretter aktivere eller deaktivere den valgte brukerens mulighet til å bruke tilpassinger for bestemte sider eller for hele systemet. Du kan også importere, eksportere eller fjerne en tilpassing for den valgte brukeren. I tillegg kan du tilbakestille funksjonsbildeforklaringer for den valgte brukeren, som vil gjøre at alle tidligere forkastede popup-vinduer som introduserte nye funksjoner, vises igjen neste gang brukeren støter på disse funksjonene.   
- **System:** – Du kan midlertidig deaktivere alle tilpasninger for alle brukere i systemet. I så fall slettes tilpasningene. Alle sidene er akkurat tilbakestilt til standard tilstand for alle brukere. Hvis du reaktiverer tilpasning senere, vil alle tilpasninger bli brukt på nytt. Du kan også permanent slette alle tilpasninger for alle brukere i systemet. Det er umulig å gjenopprette tilpasninger som er slettet. Før du utfører denne oppgaven må du eksportere tilpasninger du kanskje vil bruke senere.

## <a name="personalization-of-inventory-dimensions"></a>Tilpassing av lagerdimensjoner

Når du tilpasser oppsettet av lagerdimensjoner på en side, tar du hensyn til innstillingene som er opprettet ved hjelp av alternativet **Visningsdimensjoner**. Du bruker eksempelvis tilpasning for å skjule en kolonne for lagerdimensjonen for partinummer, men kolonnen vises neste gang siden åpnes. Dette skjer fordi **Dimensjonsvisning**-innstillingene kontrollerer lagerdimensjonskolonnene som vises.

Innstillingene for **Dimensjonsvisning** gjelder på tvers av alle sider og overstyrer tilpassede oppsett av lagerdimensjonsfelt på hver enkelt side.

I eksemplet ovenfor må du derfor fjerne lagerdimensjonen for partinummer som en del av alternativet **Visningsdimensjoner** for en side hvis du ikke vil at kolonnen for denne dimensjonen skal vises på denne siden.
