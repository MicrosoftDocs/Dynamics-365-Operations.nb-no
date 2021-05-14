---
title: Tilpasse brukeropplevelsen
description: Dette emnet forklarer hvordan du kan tilpasse appen.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 764444442aedcbf0934f1c636d7440bc0d277043
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944539"
---
# <a name="personalize-the-user-experience"></a>Tilpasse brukeropplevelsen

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kan tilpasse appen og dekker følgende emner: 

- **Systemomfattende alternativer** – Disse tilpasningsalternativene utføres på en konfigurasjonsside og er tilgjengelige for alle brukere. Eksempler er fargetema og tidssone. 
- **Begrenset tilpassingsstilgang** – På dette tilgangsnivået lagres brukerhandlinger som er knyttet til vanlig sidebruk, automatisk av appen, og de gjenopprettes neste gang du besøker siden. For eksempel lagrer appen bredden på rutenettkolonnene hvis du endrer dem, og tilstanden for vist eller skjult for hurtigfanene. 
- **Full tilpassingstilgang** – På dette tilgangsnivået har brukere tilgang til alle tilpassingsfunksjoner i appen. Spesielt har de tilgang til verktøylinjen **Tilpassing**. 
- **Dele tilpasninger** – Brukere som har full tilpasningstilgang, kan eksportere sine personlige tilpasninger og dele dem med andre brukere.
- **Administrasjon av tilpasninger** – Privilegerte brukere kan få tilgang til administrasjonssiden **Tilpasning** for å administrere alle personlige tilpasninger på et organisasjonsnivå. 

## <a name="system-wide-options-for-the-current-user"></a>Systemomfattende alternativer for gjeldende bruker

Siden **Brukeralternativer** inneholder flere systeminnstillinger for gjeldende bruker. Disse alternativene er tilgjengelige for alle brukere, selv brukere som ikke har fått tilgang til tilpasning. For å åpne siden **Brukeralternativer** velger du **Innstillinger**-knappen på navigeringslinjen, og deretter velger du **Brukeralternativer**. Siden **Brukeralternativer** har fire faneblader med ulike brukerinnstillinger:

- **Visuelt** – Velg et fargetema og standardstørrelsen på elementer på sidene.
- **Innstillinger** – Velg standardverdier som brukes hver gang du åpner systemet. Disse verdiene inkluderer standardfirmaet, startsiden og standard visnings-/redigeringsmodus. (Vis-/redigeringsmodus avgjør om en side er låst for visning eller åpnet for redigering hver gang du åpner den.) Denne fanen omfatter også alternativer for språk, tidssone, og dato, klokkeslett og tallformater. Denne fanen inneholder dessuten flere diverse innstillinger som varierer fra versjon til versjon.
- **Konto:** – Vis eller juster brukernavnet ditt og andre kunderelaterte alternativer.
- **Arbeidsflyt** – Velg arbeidsflytrelaterte alternativer.

I tillegg til å endre brukerinnstillinger kan du også vise og slette bruksdata og tilpasninger fra siden **Brukeralternativer**. Hvis du vil se dine bruksdata, velger du **Bruksdata** i handlingsruten. I fanen **Tilpassing** kan du vise og administrere de personlige endringene du har gjort på sider i systemet. I denne fanen kan du også tilbakestille bildeforklaringer for funksjonen (det vil si popup-vinduene som introduserer nye systemfunksjoner). Du vil deretter bli varslet igjen om tidligere oppdagede funksjoner.

> [!NOTE]
> Hvis funksjonen [Lagrede visninger](saved-views.md) er aktivert, kan du vise og behandle tilpasningene ved å velge **Tilpassing** i handlingsruten på siden **Brukeralternativer** .

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Begrenset tilpasningstilgang (tidligere implisitte tilpasninger)

På nivået **begrenset tilpassingsstilgang** lagres brukerhandlinger som er knyttet til vanlig sidebruk, automatisk av appen, og de gjenopprettes neste gang du besøker siden. Det kreves ingen eksplisitt lagringshandling. 

Her er en liste over handlingene som faller under vanlig bruk av siden, og som dekkes av begrenset tilpassingstilgang: 

- **Rutenettkolonnebredder:** – Du kan justere bredden på en kolonne i et rutenett ved å velge størrelseslinjen til venstre eller høyre for kolonneoverskriften og deretter dra den til venstre eller høyre helt til kolonnen har ønsket bredde. Appen lagrer bredden som du angir for en kolonne. Neste gang du åpner denne siden, endres størrelsen på kolonnen til denne bredden.
- **Rutenettbunntekst og kolonnesummer** – *(Bare tilgjengelig når den nye rutenettkontrollen er aktivert)* Du kan bestemme om en total skal vises nederst i en numerisk kolonne i et rutenett, og om bunnteksten i rutenettet er synlig. Appen lagrer disse innstillingene og bruker dem neste gang du åpner siden. Hvis du vil ha mer informasjon, se [Rutenettfunksjoner](grid-capabilities.md). 
- **Hurtigfaner** – Noen sider har utvidbare deler kalt *Hurtigfaner*. Appen lagrer informasjon om hurtigfanene som du har vist eller skjult. Neste gang du åpner siden, vil de samme hurtigfanene enten vises eller skjules, basert på siste samhandling med siden. I noen tilfeller kan du bidra til å forbedre systemytelsen ved å skjule en hurtigfane, fordi appen ikke trenger å hente informasjonen om hurtigfaner før hurtigfanen utvides. Som forklart senere i dette emnet kan du også endre rekkefølgen for hurtigfanene på en side.
- **Faktabokser** – Noen sider har en **Relatert informasjon**-rute som viser skrivebeskyttet informasjon som er knyttet til gjeldende emne på siden. Hver del i ruten **Relatert informasjon** kalles en *Faktaboks*. Du kan vise eller skjule ruten **Relatert informasjon**, og du kan også vise eller skjule individuelle faktabokser. Appene lagrer disse innstillingene. Neste gang du åpner siden, vil ruten **Relatert informasjon** og de individuelle faktaboksene enten utvides eller skjules basert på den siste samhandlingen med siden. I noen tilfeller kan du bidra til å forbedre systemytelsen ved å skjule ruten **Relatert informasjon** eller en faktaboks fordi appen ikke trenger å hente informasjonen for faktabokser før de utvides.
- **Handlingsruter** – En *Handlingsrute* vises øverst på de fleste sidene. Handlingsruten inneholder knapper for mange av handlingene som du kan utføre på gjeldende side. Disse knappene er ofte organisert i kategorier. Du kan *feste* hele handlingsruten som åpen, eller du kan skjule den som standard. Neste gang du åpner siden, vil handlingsruten enten være åpen eller skjult basert på siste samhandling med siden. Hvis du festet handlingsruten som åpen, vises den siste fanen du brukte.
- **Hurtigfilter** – Et *hurtigfilter* vises over mange rutenett. Med hurtigfilter kan du filtrere rutenettet basert på én enkeltkolonne som du velger. Appen lagrer kolonnen du filtrerte på. Deretter, neste gang du åpner denne siden, vil rutenettet bruke den samme kolonnen til filtrering som standard. Du kan imidlertid fortsatt velge en annen kolonne å filtrere rutenettet på.
- **Kolonnehodefiltre** – Når du filtrerer et rutenett ved hjelp av *kolonnehodefiltre*, kan du endre filteroperatoren etter behov for å finne dataene du vil bruke. Du kan for eksempel endre operatoren fra **begynner med** til **er nøyaktig**. Hver gang du bruker et kolonnehodefilter og endrer filteroperatoren, lagrer appen endringen. Den vil deretter gjenopprette filteroperatoren neste gang du filtrerer på denne kolonnen.
- **Navigasjonsrute** – Du kan åpne *navigasjonsruten* ved å velge **Vis navigasjonsrute**-knappen øverst til venstre rute på en hvilken som helst side. (Denne knappen kalles noen ganger _**Meny**-knappen_, *hamburger*, *hamburgermeny* eller *hamburgerknapp*.) Du kan feste navigeringsruten åpen eller beholde den skjult som standard. Når du fester navigasjonsruten åpen, vil appen beholde den åpen helt til du skjuler den.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Full tilpasningstilgang (tidligere eksplisitte tilpasninger)

På nivået **full tilpassingstilgang** har brukere tilgang til alle tilpassingsfunksjoner i appen. Siden forskjellige personer og firmaer har forskjellige behov når de samhandler med appen, særlig i henhold til bruksfelt, inneholder den medarbeidereverktøy som gjør at brukere og organisasjoner kan skreddersy måten informasjon bestilles og samhandles på i appen. Disse funksjonene er nøkkel for å gi enkle, optimaliserte opplevelser i appen som er skreddersydd for deg og organisasjonen. 

Hvis funksjonen [Lagrede visninger](saved-views.md) er aktivert, er det nødvendig med en eksplisitt lagring for å beholde disse endringene i brukeropplevelsen for en bestemt visning. Når funksjonen **Lagrede visninger** er deaktivert, lagres disse endringene automatisk.

Følgende deler dekker omfanget av tilpasningsmuligheter som er tilgjengelige for brukere på nivået **full tilpassingstilgang**. Her er noen av disse funksjonene:

- Hurtigmenyvalg
- Verktøylinjen **Tilpassing**
- Legge til fliser, lister og koblinger til arbeidsområder
- Legge til et sammendrag fra et arbeidsområde til et instrumentbord
- Tilpasse instrumentbordet

### <a name="shortcut-menu-options"></a>Hurtigmenyvalg

Hurtigmenyer er én måte for å endre grensesnittet på en side, slik at de passer bedre til behovene eller kravene i organisasjonen din. (En hurtigmeny er også kjent som en *høyreklikkmeny* eller en *hurtigmeny*.)

Noen av mest vanlige og viktigste endringene som gjøres på en side, er tilgjengelige direkte som valg på en hurtigmeny. For eksempel, hvis du vil legge til eller skjule kolonner i et rutenett, bare høyreklikker du en kolonneoverskrift og velger deretter **Sett inn kolonner** eller **Skjul denne kolonnen**.

De vanligste typene tilpasninger er i tillegg tilgjengelige ved å høyreklikke et element og deretter velge **Tilpass**. (Vær oppmerksom på at ikke alle elementene på siden kan tilpasses.) Når du bruker denne tilpasningsmetoden, vises elementets *egenskapsvindu*.

![Tilpasse egenskapene for et element](./media/cli-element-property-window.png)

Du kan bruke egenskapsvinduet til å tilpasse et element på følgende måter:

- Endre elementetiketten.
- Skjul elementet slik at det ikke vises på siden. Dataene i feltet slettes eller endres ikke. Informasjonen vises bare ikke på siden lenger.
- Ta med informasjonen i sammendragsdelen for hurtigfanen (hvis elementet er på en hurtigfane).
- Hopp over feltet, slik at det aldri får fokus når du bruker tabulatoren gjennom siden.
- Hindre at dataene i feltet blir redigert (for en post).
- Angi et felt som skal være obligatorisk for dataregistrering. Hvis det ikke er angitt noen verdi i dette feltet, vises det med en rød kantlinje og en stjerne som angir denne statusen. Dette alternativet er tilgjengelig fra og med versjon 10.0.11, når funksjonene [Lagrede visninger](saved-views.md) og **Angi felt som obligatoriske ved hjelp av tilpasning** er aktivert.

Egenskapsvinduet kan inneholde andre tilpasningsfunksjoner avhengig av elementet. Egenskapsvinduet for en flis kan for eksempel la deg å fremme flisen på et instrumentbord, og egenskapsvinduer for elementer på standard instrumentbord kan la deg opprette et nytt tilpasset arbeidsområde.

### <a name="personalization-toolbar"></a>Verktøylinje for tilpassing

Hvis du vil gjøre flere endringer på en side eller gjøre endringer som ikke er tilgjengelige gjennom andre mekanismer (for eksempel hvis du vil endre rekkefølgen på elementene), kan du bruke **Tilpassing**-verktøylinjen. Hvis du vil åpne **Tilpassing**-verktøylinjen, følger du et av disse trinnene:

- Velg **Ctrl+Skift+P** fra ethvert element på siden.
- Velg **Tilpass denne siden** i egenskapsvinduet for et element.
- Velg **Tilpass denne siden** i gruppen **Tilpass** i fanen **Alternativer** på handlingssiden til en hvilken som helst side.
- Velg knappen **Innstillinger** (tannhjulsymbolet) i navigasjonsfeltet, og velg deretter **Tilpass**.

[![Verktøylinje for tilpassing](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigere på siden

Når verktøylinjen **Tilpassing** er åpen, er den underliggende siden skrivebeskyttet (med andre ord kan du ikke redigere data), men den er fortsatt interaktiv. Spesifikt kan du vise eller skjule ruten **Beslektet informasjon**, bytte kategorier og vise eller skjule inndelinger, på samme måte som du vanligvis ville utført disse handlingene på siden. Hvis du vil bruke en tilpasning på en inndeling eller kategori som kan skjules (for eksempel skjule en hurtigfane), kan du ganske enkelt velge knappen som vises ved siden av inndelingen eller fanen som kan skjules, når den får tastaturfokus eller når du holder musepekeren over den.

#### <a name="personalization-tools"></a>Verktøy for tilpassing

Følgende verktøy er tilgjengelige på **Tilpassing**-verktøylinjen:

- Bruk **Velg**-verktøyet til å velge og endre egenskapene for et element. Hvis du vil bruke dette verktøyet, velger du knappen **Velg** på verktøylinjen og velger deretter ønsket element. Egenskapsvinduet for elementet vises, der du kan endre egenskapene for elementet. Du kan gjenta prosessen for andre elementer som kan tilpasses på siden. Vær oppmerksom på at noen personlige egenskaper kanskje ikke er tilgjengelige i noen scenarioer. Du kan for eksempel ikke låse et felt som er nødvendig.
- Bruk **Skjul**-verktøyet for å skjule et element på siden. Hvis du vil bruke dette verktøyet, velger du knappen **Skjul** på verktøylinjen, og deretter velger du elementet som skal skjules. Når du bruker **Skjul**-verktøyet, vil alle elementer som ligger skjult, gjøres synlige, men de vises i en skyggelagt container. Deretter kan du få et element synlig ved å merke det. Hvis du vil se hvordan siden vil se ut når elementer er skjult, bytter du til et annet tilpasningsverktøy eller lukker verktøylinjen for tilpasning.
- Bruk verktøyet **Legg til et felt** for å legge til felt på siden. Når du bruker dette verktøyet, kan du bare legge til felt som er del av sidedefinisjonen. Hvis du vil ha informasjon om hvordan du oppretter nye felt som ikke er en del av den gjeldende sidedefinisjonen, kan du se [Opprette og arbeide med egendefinerte felt](user-defined-fields.md). Når du har valgt knappen **Legg til et felt** på verktøylinjen, må du først velge rutenettet eller delen der du vil legge til et felt. En dialogboks viser listen over felt som er knyttet til det valgte rutenettet eller den valgte delen. I dialogboksen velger du ett eller flere felt og deretter **Oppdater**. Hvis du vil fjerne et felt som du la til tidligere, gjentar du prosessen, men fjerner merkingen av feltet i dialogboksen.
- Bruk **Flytt**-verktøyet når du vil flytte et element til et annet sted i den gjeldende gruppen med elementer. Legg merke til at du ikke kan flytte et element utenfor den overordnede gruppen. Hvis du vil bruke dette verktøyet, velger du knappen **Flytt** på verktøylinjen, og deretter velger du elementet som skal flyttes. Når du velger et element, bestemmer appen stedene der elementet kan flyttes. Disse stedene kalles *slippsoner*. Når du drar elementet rundt i gjeldende gruppe, vises hver "slippsone" som en farget, fet linje ved siden av området der elementet kan slippes.
- Bruk **Hopp over**-verktøyet for å fjerne et element fra sidens tastaturtabulatorsekvens. Når du velger **Hopp over**-knappen på verktøylinjen, vil alle elementer som hoppes over, vises i en skyggelagt container. Du kan interaktivt fjerne eller legge til felt i kategorisekvensen.
- Bruk **Vis i hode**-verktøyet når du vil at et felt skal vises i sammendragsdelen i hurtigfanen. Når du velger knappen **Vis i hode** på verktøylinjen, vil alle felt som er merket som sammendragsfelt, vises med en skyggelagt beholder. Du kan interaktivt legge til felt i hurtigfanen Sammendrag og fjerne felt fra sammendraget ved å velge feltene.
- Bruk **Krev**-verktøyet til å angi et element som obligatorisk for dataregistrering. Når du velger **Krev**-knappen på verktøylinjen, vil alle elementer som er tilpasset for å gjøres obligatoriske, vises i en skyggelagt beholder. Du kan deretter gjøre dem ikke-obligatoriske på nytt. Dette alternativet er tilgjengelig fra og med versjon 10.0.12, når funksjonen **Angi felt som obligatoriske ved hjelp av tilpasning** er aktivert.
- Bruk **Lås**-verktøyet når du vil merke et element som enten er redigerbart eller ikke redigerbart. Når du velger **Lås**-knappen på verktøylinjen, vil alle elementer som ikke kan redigeres, vises i en skyggelagt container. Du kan deretter gjøre dem redigerbare på nytt. Legg merke til at noen felt er nødvendige og ikke kan gjøres ikke-redigerbare. Et hengelåssymbol ved siden av disse feltene.
- Bruk verktøyet **Legg til en app fra Power Apps** for å bygge inn en app som ble opprettet ved hjelp av Microsoft Power Apps, på siden. Hvis du vil ha mer informasjon om hvordan du bygger inn en app fra Power Apps på en side, kan du se [Bytte inn apper fra Power Apps](embed-power-apps.md). Dette alternativet er bare tilgjengelig når funksjonen [Lagrede visninger](saved-views.md) er deaktivert.
- Bruk knappen **Legg til en app** til å bygge inn en app, enten en opprettet fra Microsoft Power Apps eller en tredjeparts, på siden. Dette alternativet er bare tilgjengelig når funksjonen [Lagrede visninger](saved-views.md) er aktivert. 
- Bruk verktøyet **Fjern** for å tilbakestille siden til standard installert tilstand. Alle tilpasninger på gjeldende side vil bli fjernet. Du kan ikke angre denne handlingen. Bruk derfor dette verktøyet bare hvis du er sikker på at du vil tilbakestille siden. Når funksjonen **Lagrede visninger** er aktivert, fjerner dette verktøyet personlige tilpasninger for gjeldende visning.
- Bruk verktøyet **Importer** for å laste en tilpasning fra en fil som du eller noen andre har opprettet. 

    - Når funksjonen **Lagrede visninger** er deaktivert, kan du velge om du vil legge til eller erstatte den eksisterende personlige tilpasningen med personlige tilpasninger som importeres for siden. Du kan ikke angre denne handlingen. Etter at du har importert personlige tilpasninger, må du derfor fjerne eller angre endringene du ikke vil ha, manuelt.
    - Når funksjonen **Lagrede visninger** er aktivert, blir de importerte tilpasningene en visning på siden. Hvis visningen allerede finnes, kan du hoppe over importen, erstatte den gjeldende visningen som har samme navn, eller gi den importerte visningen nytt navn.

- Bruk verktøyet **Eksporter** til å lagre dine tilpasninger for siden i en fil. Du kan deretter dele dine tilpasninger med andre brukere. Disse brukerne trenger bare å importere filen som inneholder dine tilpasninger for siden. Når funksjonen **Lagrede visninger** er aktivert, lagrer dette verktøyet den gjeldende visningen i en fil for deling.
- Velg **Lukk**-knappen for å lukke **Tilpasning**-verktøylinjen og returnere siden til den forrige interaktive tilstanden.

Når verktøylinjen for **Tilpasning** er brukt, vil tilpasningene vanligvis gjelde så snart du lager dem. Hvis imidlertid funksjonen [Lagrede visninger](saved-views.md) er aktivert, må du eksplisitt lagre personlige tilpasninger til en visning du velger.

I noen tilfeller når du velger et verktøy, vises et hengelåssymbol ved siden av et element. Dette symbolet indikerer at du ikke kan endre egenskapene for elementet som er knyttet til det valgte verktøyet, fordi endringer i disse egenskapene vil hindre at siden fungerer som den skal.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Legge til fliser, lister og koblinger til et arbeidsområde

For enkelte sider som inneholder lister, er tilpasningsfunksjonen **Legg til i arbeidsområde** tilgjengelig i gruppen **Tilpass** i fanen **Alternativer** i handlingsruten. Med denne funksjonen kan du skyve relevant informasjon fra gjeldende liste til et bestemt arbeidsområde. Informasjonen som vises i arbeidsområdet, kan baseres på hele listen eller en filtrert og sortert versjon av listen. Du kan også angi om informasjonen skal vises i arbeidsområdet som en liste, som en sammendragsflis som kan vise antall elementer i listen, eller som en kobling.

> [!NOTE]
> Hvis funksjonen [Lagrede visninger](saved-views.md) er aktivert, er innholdet du dytter til et arbeidsområde, direkte koblet til en visning. Visningsspørringen brukes til å hente data i arbeidsområdet, og tilsvarende flis eller kobling i arbeidsområdet åpner siden til denne visningen, slik at visningensspørring og personlige tilpasninger brukes på den. Hvis visningen oppdateres, vil de tilhørende arbeidsområdeelementene bli justert til den nye visningsdefinisjonen.

[![Legg til i arbeidsområde](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Hvis du vil legge til et arbeidsområde, sorterer eller filtrerer du først på siden, slik at den viser informasjonen slik du vil at den skal vises i arbeidsområdet. (Hvis funksjonen **Lagrede visninger** er aktivert, kan du ikke fortsette før du har lagret en visning som har disse betingelsene.) Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Liste**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan velge hvilke kolonner som skal vises i listen i arbeidsområdet. Du kan også angi etiketten som brukes for listen i arbeidsområdet.
- Hvis du vil legge til en flis i et arbeidsområde, må du først filtrere listen på siden slik at den viser dataene som skal oppsummeres, eller som du vil ha rask tilgang til. (Hvis funksjonen **Lagrede visninger** er aktivert, kan du ikke fortsette før du har lagret en visning som har disse betingelsene.) Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Flis**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan angi etiketten som skal brukes for flisen i arbeidsområdet. Du kan også angi om ruten skal vise et tall. Når flisen er lagt til i arbeidsområdet, kan du velge den for å åpne den gjeldende siden fra arbeidsområdet. Deretter kan du vise den filtrerte listen som er knyttet til brikken.
- Hvis du vil legge til en kobling i et arbeidsområde, filtrerer du først filteret på siden slik at den viser dataene du er interessert i. (Hvis funksjonen **Lagrede visninger** er aktivert, kan du ikke fortsette før du har lagret en visning som har disse betingelsene.) Velg deretter **Legg til i arbeidsområde**. Velg et arbeidsområde, og deretter, i **Presentasjon**-feltet, velger du **Kobling**. Når du har valgt **Konfigurer**, vises en dialogboks der du kan angi etiketten som skal brukes for koblingen. Du kan også angi en etikett for en ny inndeling som inneholder denne koblingen.

Når du har lagt til listen, flisen eller koblingen i et arbeidsområde, kan du åpne arbeidsområdet og endre rekkefølgen på elementene i den etter ønske.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Legge til et sammendrag fra et arbeidsområde til et instrumentbord

Noen arbeidsområder inneholder fliser med antall (det vil si fliser som inneholder tall), og du vil kanskje at disse flisene skal vises på instrumentbordet også. I et arbeidsområde høyreklikker du en flis for antall, velger **Tilpass**, og deretter velger du **Fest til instrumentbord** i egenskapsvinduet til flisen. Neste gang du åpner og oppdaterer instrumentbordet, vil antallet vises under arbeidsområdets navigasjonsflis. Du kan velge det antallet for å gå direkte til dataene det representerer.

### <a name="personalizing-your-dashboard"></a>Tilpasse instrumentbordet

Instrumentbordet er ofte den første siden som vises når du åpner appen. Den kan tilpasses som en hvilken som helst annen side i systemet, ved å bruke de samme mekanismene som er beskrevet tidligere i dette emnet. 

> [!WARNING]
> Når du skjuler innhold på instrumentbordet, er det for øyeblikket viktig at du direkte målretter en flis, og ikke rommet rundt den. Hvis du skjuler gruppen rundt en flis, kan det være uventede resultater hvis flere fliser legges til senere, eller hvis systemet byttes til et annet språk.

Én unik tilpasningskapasitet som er tilgjengelig på instrumentbordet, er muligheten til å legge til fliser. 

- Hvis funksjonen **Helside-apper** er slått av, legger du til en ny flis ved å høyreklikke et element på instrumentbordet og deretter velge **Legg til et arbeidsområde**. En ny arbeidsområdeflis opprettes nederst på instrumentbordet. Du kan endre navn på denne nye arbeidsområdeflisen slik du vil. Du kan også legge til lister, fliser og koblinger til arbeidsområdet, som beskrevet i [Legge til fliser, lister eller koblinger i et arbeidsområde](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace)-delen i dette emnet.
- Hvis funksjonen **Helside-apper** er slått på, legger du til en ny flis ved å høyreklikke et element på instrumentbordet og deretter velge **Legg til en app**. I dialogboksen velger du om du vil legge til en flis for et nytt arbeidsområde eller en flis med innhold fra Power Apps eller et nettsted. Deretter følger du trinnene for å konfigurere alternativet du valgte. En ny flis opprettes nederst på instrumentbordet. 

## <a name="sharing-personalizations"></a>Dele tilpasninger

Når du tilpasser en side, kan du dele dine personlige tilpasninger med andre brukere gjennom flere metoder. I listen nedenfor ordnes metodene i rekkefølge fra de mest anbefalte til minst anbefalte.

1. Publiser visninger til brukere.
2. Kopier visninger eller tilpasninger til brukere.
3. Eksporter og importer visninger eller tilpasninger.

### <a name="publish-views-to-users"></a>Publiser visninger til brukere

Hvis funksjonen for [lagrede visninger](saved-views.md) er aktivert, og hvis siden støtter visninger, er det den beste måten å dele tilpasninger med andre brukere på, å publisere visningen til brukere som har én eller flere sikkerhetsroller. Hvis du vil ha mer informasjon, se [Publisere visninger](saved-views.md#publishing-views).

### <a name="copy-views-or-personalizations-to-users"></a>Kopier visninger eller tilpasninger til brukere

Hvis funksjonen for [lagrede visninger](saved-views.md) er slått av, eller hvis siden ikke støtter visninger, er det anbefalt å kopiere dem mellom brukere. Denne metoden er bare tilgjengelig for privilegerte brukere (for eksempel systemadministratorer). Administratorer kan imidlertid slå opp en bestemt brukers tilpasning i systemet (inkludert brukerens personlige visning hvis lagrede visninger er aktivert), og kopiere konfigurasjonen til andre brukere.

Hvis lagrede visninger er aktivert, følger du fremgangsmåten nedenfor for å kopiere tilpasninger.

1. Gå til **Systemadministrasjon \> Oppsett \> Tilpassing**.
2. Følg denne fremgangsmåten for å kopiere personlige visninger:

    1. Velg **Personlige visninger**.
    2. Velg de ønskede visningene i listen.
    3. Velg **Kopier til brukere**.
    4. Velg brukerne du vil distribuere visninger til.

    Følg denne fremgangsmåten for å kopiere tilpasninger på sider som ikke støtter visninger:

    1. Velg **Brukerinnstillinger**.
    2. Velg brukeren som har tilpasningen du vil distribuere.
    3. Velg **Behandle alle tilpasninger**.
    4. Velg de ønskede tilpasningene i listen.
    5. Velg **Kopier til brukere**.
    6. Velg brukerne du vil distribuere tilpasninger til.

Hvis lagrede visninger ikke er aktivert, følger du fremgangsmåten nedenfor for å kopiere en tilpasning.

1. Gå til **Systemadministrasjon \> Oppsett \> Tilpassing**.
2. Velg **Bruk**.
3. Velg brukerne du vil distribuere tilpasningen til.
4. Velg **Velg eksisterende tilpasning**.
5. Finn og velg (enkelt) tilpasningen du er interessert i.
6. Velg **OK**.

### <a name="export-and-import-views-or-personalizations"></a>Eksporter og importer visninger eller tilpasninger

En annen måte å dele tilpasninger på, er ved eksport og import. Enkeltbrukere, eller en administrator som handler på deres vegne, kan bruke denne metoden til å eksportere tilpasningene eller visningene, og deretter gi den eksporterte filen til andre brukere for å importere. Brukere kan eventuelt gi sine eksporterte tilpasninger til en bruker med administratorrettigheter, og denne brukeren kan deretter bruke **Tilpassing**-administrasjonssiden til å bruke tilpasningsfilen for mange brukere samtidig.

#### <a name="export"></a>Eksporter

Du kan generelt eksportere én av dine egne visninger eller tilpasninger ved å åpne den aktuelle siden, åpne verktøylinjen for **tilpasning** og deretter velge **Eksporter**. Hvis du vil ha mer informasjon om verktøylinjen, kan du se delen [Verktøylinje for tilpassing](#personalization-toolbar) tidligere i dette emnet. Hvis [lagrede visninger](saved-views.md) er aktivert, kan du også gå til **Innstillinger \> Brukeralternativer \> Tilpassing** for å vise en liste over alle tilpasningene i systemet. Derfra kan du velge visningene eller tilpasningene som skal eksporteres, og deretter velge **Eksporter**.

I tillegg kan administratorer eksportere tilpasningene til andre brukere ved å følge disse trinnene.

1. Gå til **Systemadministrasjon \> Oppsett \> Tilpassing**.
2. Velg ønsket bruker i kategorien **Brukere**.
3. Finn og velg visningen eller tilpasningen du er interessert i.
4. Velg **Eksporter**.

#### <a name="import"></a>Import

Hvis du vil importere en visning eller tilpasning, kan du bare åpne **tilpasningsverktøylinjen** og velge **Importer**. I tillegg kan administratorer importere en fil og umiddelbart gi den til én eller flere brukere.

Hvis lagrede visninger er aktivert, følger du fremgangsmåten nedenfor.

1. Gå til **Systemadministrasjon \> Oppsett \> Tilpassing**.
2. Velg **Importer visninger \> Brukervisninger** i handlingsruten.
3. Velg importmodus:

    - **Velg bestemte brukere** – Gi visningen eller tilpasningen til valgte brukere.
    - **Importer som den er** – Importer visningen eller tilpasningen til den samme brukeren som eksporterte den.

4. Velg **Bla gjennom** og finn og velg tilpasningen som skal importeres.
5. Velg **Neste**.
6. Hvis du valgte **Velg bestemte brukere** i trinn 3, velger du brukerne du vil importere tilpasningen til.
7. Velg **Import**.
8. Løs konflikter etter behov.

Hvis lagrede visninger ikke er aktivert, følger du fremgangsmåten nedenfor.

1. Gå til **Systemadministrasjon \> Oppsett \> Tilpassing**.
2. Velg **Bruk**.
3. Velg brukerne du vil distribuere tilpasningen til.
4. Velg **Importer tilpasninger fra en fil**.
5. Velg **Bla gjennom** og finn og velg tilpasningen som skal importeres.
6. Velg **OK**.

## <a name="administration-of-personalizations"></a>Administrasjon av tilpasninger

**Tilpassing**-siden er den sentrale huben for administrasjon av personlige tilpasninger på organisasjonsnivå. Innholdet og funksjonene på denne siden avhenger av om **Lagrede visninger**-funksjonen er aktivert.

For kunder som har aktivert **Lagrede visninger**-funksjonen, kan du se "Behandle visninger globalt"-delen i [Lagrede visninger](saved-views.md)-emnet.

For kunder som ennå ikke har aktivert funksjonen [Lagrede visninger](saved-views.md), har denne siden fire kategorier:

- **Bruk** – Du kan importere eller velge en tilpasning for én eller flere brukere. Hvis du vil bruke en tilpasning på én eller flere brukere, må du først velge en rolle og brukere som har denne rollen. Velg deretter en eksisterende tilpasning som skal brukes på de valgte brukerne, eller importer en tilpasningsfil. Tilpasningen blir godkjent og brukes for alle de valgte brukerne neste gang de åpner den valgte siden.

- **Fjern** – Du kan fjerne alle tilpasninger for en side eller et arbeidsområde for én eller flere brukere. Velg først en side eller et arbeidsområde for å se en liste over brukerne som har tilpasset den. Velg deretter brukerne som skal ha fjernet tilpasninger for denne siden eller arbeidsområdet, og velg deretter **Fjern**. Alle tilpasninger som de valgte brukerne har brukt på den valgte siden eller arbeidsområdet, slettes. Du kan ikke angre denne handlingen. Hvis en tilpasning ble lagret for siden eller arbeidsområdet, kan tilpasningen importeres på nytt.

- **Brukere** – Velg en bruker for å vise en liste over sider som brukeren har tilpasset. Du kan deretter aktivere eller deaktivere den valgte brukerens mulighet til å bruke tilpassinger for bestemte sider eller for hele systemet. Du kan også importere, eksportere eller fjerne en tilpassing for brukeren. I tillegg kan du tilbakestille bildeforklaringer for funksjonen for brukeren. Hvis brukeren tidligere har ignorert alle popup-vinduer som introduserer nye funksjoner, vil de da vises igjen neste gang brukeren støter på disse funksjonene.

- **System** – Du kan midlertidig deaktivere tilpasninger for alle brukere i systemet. I dette tilfellet slettes alle personlige tilpasninger for alle brukere, og alle sidene tilbakestilles til standardtilstanden. Hvis du reaktiverer tilpasning senere, vil alle tilpasninger bli brukt på nytt. Du kan også permanent slette alle tilpasninger for alle brukere i systemet. Tilpasninger som er slettet, kan ikke gjenopprettes. Før du utfører denne oppgaven må du eksportere tilpasninger du kanskje vil bruke senere.

## <a name="personalizing-inventory-dimensions"></a>Tilpasse lagerdimensjoner

Når du tilpasser oppsettet av lagerdimensjoner på en side, tar du hensyn til innstillingene som er opprettet ved hjelp av alternativet **Visningsdimensjoner**. Du bruker eksempelvis tilpasning for å skjule en kolonne for lagerdimensjonen for partinummer, men kolonnen vises neste gang siden åpnes. Dette skjer fordi **Dimensjonsvisning**-innstillingene kontrollerer lagerdimensjonskolonnene som vises. Innstillingene for **Dimensjonsvisning** gjelder på tvers av alle sider og overstyrer tilpassede oppsett av lagerdimensjonsfelt på enkeltsider.

I eksemplet ovenfor må du derfor fjerne lagerdimensjonen for partinummer som en del av alternativet **Visningsdimensjoner** for en side hvis du ikke vil at kolonnen for denne dimensjonen skal vises på denne siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
