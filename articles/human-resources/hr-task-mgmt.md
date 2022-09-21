---
title: Oppgavebehandling
description: Denne artikkelen forklarer oppgavebehandlingsfunksjonaliteten som er tilgjengelig i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 29b547ff4f55b572ab774e7e70949ec8cb53ef42
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445901"
---
# <a name="task-management"></a>Oppgavebehandling

[!INCLUDE [PEAP](../includes/peap-1.md)]

Ved hjelp av oppgavebehandling kan du opprette oppgaver som må fullføres for å ansette person (pålasting), avslutte ansettelse (avlasting) og overføre ansatt (overganger). Oppgavebehandling bruker sjekklistekonseptet. En sjekkliste er en liste over pålastings-, avlastings- og overgangsoppgaver. Oppgavebehandling bruker sjekklister til å gruppere oppgaver sammen, og til å tilordne dem til enkeltpersoner eller grupper. Sjekklistefunksjonaliteten for pålasting, avlasting og overganger ligner hverandre.

## <a name="checklist-overview"></a>Sjekklisteoversikt

En sjekkliste er en gruppe oppgaver. Sjekklister gir deg en fleksibel måte å gruppere oppgaver på, og de kan brukes på nytt (for eksempel når du ansetter flere ansatte). Du kan opprette så mange sjekklister du krever, og du kan tilordne de samme oppgavene til flere sjekklister.

### <a name="examples"></a>Eksempler

Eksemplene nedenfor viser hvordan sjekklister kan brukes i arbeidsprosessen. Fordi sjekklistefunksjonaliteten for pålasting, avlasting og overganger er liknende, gjelder imidlertid informasjonen også for pålastings- og avlastingsprosessene.

Som en del av pålastingsprosessen kan Personale opprette oppgaver som sporer pålastingsprosessen for innkommende og nylig innleide ansatte. Siden pålastingsprosessen kan variere avhengig av den ansattes stilling eller geografisk plassering, kan du opprette flere sjekklister for å legge til rette for ulike ansettelsessituasjoner.

**Eksempel 1**

Hver ansatt som er ansatt i USA, må utføre oppgaver som å fylle ut skattetrekksskjemaer. Oppgaver som tilordning av firmabil kan imidlertid bare gjelde ansatte på ledernivå. I dette tilfellet kan det opprettes to sjekklister for **USA-baserte ansatte** og **Bare ledere**. Når en leder på mellomnivå ansettes i USA, velges sjekklisten for **USA-baserte ansatte**. Når en leder ansettes i USA, velges imidlertid begge sjekklistene for å sikre at alle de nødvendige pålastingsoppgavene fullføres.

**Eksempel 2**

Et firma har både sesongansatte og vanlige heltidsansatte. Selv om noen oppgaver (for eksempel bekreftelse av nyansattes ankomsttid) gjelder ansatte av begge typer, gjelder noen tilleggsoppgaver bare for vanlige heltidsansatte. I dette tilfellet kan du opprette to sjekklister. Begge sjekklistene omfatter oppgaver som gjelder både sesongansatte og vanlige heltidsansatte, men bare én sjekkliste omfatter oppgavene som gjelder vanlige heltidsansatte.

## <a name="task-management-workspace"></a>Arbeidsområde for oppgavebehandling

Arbeidsområdet for **Oppgavebehandling** viser alle oppgavene som er tilordnet enkeltpersoner i pålastings-, avlastings- og overgangsprosessen. Hvis du vil vise oppgavene for en prosess, velger du den aktuelle kategorien i øvre venstre hjørne: **Pålasting**, **Avlasting** eller **Overganger**. Som standard har bare HR-personer tilgang til arbeidsområdet for **Oppgavebehandling**.

Kategorien **Pålasting** inneholder en **Starter snart**-liste som viser innkommende ansatte og **Nyansettelser** som viser personer som nylig er ansatt. I begge listene kan du bare velge én ansatt. Når du velger en ansatt, vises alle oppgaver som er relatert til den ansattes pålasting, til høyre på siden. Kategorien **Pålasting** inneholder også en **Alle oppgaver**-liste som viser alle oppgaver for alle innkommende eller nylig ansatte personer. Til slutt inneholder den en liste over forfalte oppgaver og en liste over oppgaver som er tilordnet den gjeldende brukeren.

Kategorien **Avlasting** inneholder en liste over ansatte som går ut av firmaet, og en liste over ansatte som allerede har gått ut av firmaet. I begge listene kan du bare velge én ansatt. Når du velger en ansatt, vises alle oppgaver som er relatert til den ansattes avlasting. Kategorien **Avlasting** inneholder også en **Alle oppgaver**-liste som viser alle avsluttende eller avsluttede ansatte. Til slutt inneholder den en liste over forfalte oppgaver og en liste over oppgaver som er tilordnet den gjeldende brukeren.

Kategorien **Overganger** inneholder en **Alle oppgaver**-liste som viser alle oppgaver for alle ansatte som skal endre stillinger eller som nylig har endret stillinger. Det finnes også en liste over forfalte oppgaver og en liste over oppgaver som er tilordnet den gjeldende brukeren.

I alle de tre kategoriene kan HR-assistenter og -ledere utføre følgende aktiviteter:
- Bruk en sjekkliste for en ansatt
- Oppdater statusen til en oppgave
- Tilordne en oppgave på nytt
- Oppdater forfallsdatoen for en oppgave

> [!NOTE]
> Som standard viser kategorien **Pålasting** anstatte som ble ansatt de siste sju dagene. Hvis du vil endre denne innstillingen, går du til siden **Personalparametere** i kategorien **Generelt** i feltet **Nyansettelser** og angir tidsramme. Informasjonen i listen **Nyansettelser** kan vises i et bestemt antall dager, måneder eller år. Hvis du for eksempel vil vise listen over ansatte som ble ansatt i de siste 14 dagene, setter du **Periode**-feltet til **14** og **Enhet**-feltet til **Dager**.
> På siden **Personalparametere** kan du også oppdatere datoområdet for listene over eksisterende og avsluttede ansatte som vises i **Avlasting**-fanen. Disse innstillingene gjelder også for arbeidsområdet **Personaladministrasjon**.

## <a name="setting-up-tasks"></a>Sette opp oppgaver

Du kan opprette oppgaver enkeltvis og deretter bruke dem på nytt i flere sjekklister. Hvis du vil opprette en oppgave, går du til siden **Oppsett av pålasting**, kategorien **Oppgaver** og velger **Ny**.

Du kan tilordne en opprettet oppgave til flere sjekklister ved å merke oppgaven og deretter velge **Bruk på sjekklister** på menyen.

Du kan også legge til oppgaver direkte i en sjekkliste. Hvis du vil legge til en oppgave i en sjekkliste, kan du gå til siden **Oppsett av pålasting** i kategorien **Sjekkliste** og enten opprette en ny sjekkliste å legge til oppgaven i, eller legge oppgaven til i en eksisterende sjekkliste.

Hvis du vil redigere en oppgave i biblioteket, velger du **Rediger** på menyen for oppgavebibliotek. Hvis oppgaven er knyttet til en sjekkliste, vises disse sjekklistene på siden **Rediger oppgave**. Hvis du vil at oppgavene i kontrollistene skal oppdateres med redigeringene, velger du disse sjekklistene i delen **Bruk på sjekklister**.

Hvis du vil slette oppgaver fra biblioteket, velger du **Slett**. Hvis en oppgave er knyttet til en sjekkliste, vil ikke denne handlingen slette oppgaven fra sjekklisten. Oppgaven må fjernes fra sjekklisten i en separat handling.

> [!NOTE]
> Hvis du legger til en oppgave direkte i en sjekkliste, kan du ikke bruke den på nytt i andre sjekklister.

I tabellen nedenfor beskrives feltene som er tilgjengelige når du oppretter en oppgave etter én av disse metodene.

| Felt           | Beskrivelse |
|-----------------|-------------|
| Oppgave            | Angi navnet på oppgaven. |
| Beskrivelse     | Angi en beskrivelse av oppgaven. |
| Valgfri        | Angi om oppgaven er valgfri og bare er informasjonsrelatert. |
| Oppgavekobling       | Angi URL-adressen til en ekstern webside eller en bestemt side i appen der brukeren skal fullføre oppgaven. Hvis du vil ha mer informasjon, kan du se delen [Oppgavekoblinger](#task-links). |
| Tilordningstype | Oppgaver kan tilordnes en bestemt arbeider, stilling eller gruppe med stillinger, lederen til den berørte ansatte (det vil si den ansatte som er en del av prosessen med pålasting, avlasting eller overgang) eller den berørte ansatte. Velg tilordningstypen. Hvis du vil ha mer informasjon, kan du se delen [Tilordningstyper](#assignment-types). |
| Tilordnet til     | Velg den bestemte arbeideren, stillingen eller gruppen med stillinger som oppgaven skal tilordnes til. |
| Kontaktperson  | Angi personen som skal kontaktes hvis det er spørsmål om oppgaven. |
| Manglende samsvar for forfallsdato | Angi hvor mange dager før eller etter pålastings-, avslutnings- eller overgangsdatoen som oppgaven forfaller. Hvis du vil ha mer informasjon, kan du se delen [Forfallsdatoer for oppgave og Manglende samsvar for forfallsdato-feltet](#task-due-dates-and-the-due-date-offset-field). |
| Instruksjoner    | Angi instruksjoner for fullføring av oppgaven. Hvis du vil ha mer informasjon, kan du se delen [Instruksjoner](#instructions). |

### <a name="task-links"></a>Oppgavekoblinger

En oppgavekobling inneholder en kobling til en ekstern webside eller en side i Dynamics 365-appen. Du kan angi en oppgavekobling hvis personen som er tilordnet en oppgave, skal gå til en bestemt webside eller en bestemt side i Dynamics 365-appen for å fullføre oppgaven. Når du oppretter en oppgavekobling, kan du velge ett av følgende alternativer:

- **Menyelement** – Hvis du velger dette alternativet, vises en liste over alle sidene i Dynamics 365-appen. Velg en side i listen.
- **URL-adresse** – Hvis du velger dette alternativet, legger du inn URL-adressen til websiden som du vil at personen som er tilordnet oppgaven, skal gå til. Den angitte siden kan være en side som ikke er en del av Dynamics 365-appen.
- **Arbeiderdetaljer** – Hvis du velger dette alternativet, velger du ett av følgende alternativer:

    - **Selvbetjeningshandlinger for ansatte** – Dette alternativet viser en liste over sider som er tilgjengelige i **Ansattselvbetjening**. Bruk det hvis oppgaven som ble tilordnet den pålastede ansatte, må fullføres i **Ansattselvbetjening**. Hvis du for eksempel vil at den ansatte skal registrere sin personlige kontaktinformasjon, velger du **Selvbetjeningshandlinger for ansatte**, og deretter velger du **Personalia&gt;Personlige opplysninger**.
    - **Handlinger for arbeiderstyring** – Dette alternativet viser en liste over sider som er knyttet til arbeideroppføringen, men som den ansatte ikke har tilgang til. Hvis du for eksempel vil at oppgaveeieren skal registrere informasjon som er spesifikk for en pålastet ansatt, for eksempel kompensasjonsinformasjon, velger du **Handlinger for arbeidsstyring** og velger deretter **Kompensasjon&gt;Fast kompensasjon**.

### <a name="assignment-types"></a>Tilordningstyper

Når en ansatt ansettes, avsluttes eller overføres, kan du velge én eller flere sjekklisteer. Når en sjekkliste er valgt, og ansettelses-, oppsigelses- eller overføringsprosessen er fullført, opprettes oppgaver og tilordnes brukere for å spore fremdriften.

Når en oppgave opprettes, tilordnes den til en bestemt bruker. Brukeren som en oppgave er tilordnet, avhenger av tilordningstypen som er valgt for denne oppgaven. Følgende verdier er tilgjengelige i **Tilordningstype**-feltet:

- **Arbeider** – Tilordne oppgaven til en bestemt arbeider. Når du har valgt denne verdien, velger du arbeideren i feltet **Tilordnet til**.
- **Stilling** – Tilordne oppgaven til en bestemt stilling. Når du har valgt denne verdien, velger du stillingen i feltet **Tilordnet til**.

    En IT-ingeniør vil for eksempel alltid være ansvarlig for å klargjøre en bærbar datamaskin for en ny ansatt. I dette tilfellet, når du oppretter oppgaven for bærbar datamaskin, velger du **Stilling** som tilordningstype, og deretter velger du **IT-ingeniør** som stilling. Når en person ansettes og sjekklisten tilordnes, tilordnes deretter konfigurasjonsoppgaven for den bærbare datamaskinen til den ansatte som har IT-ingeniørstillingen på tidspunktet da ansettelseshandlingen ble lagt inn.

- **Gruppe** – Tilordne oppgaven til en gruppe med stillinger (tilordningsgruppe). Når du har valgt denne verdien, velger du gruppen i feltet **Tilordnet til**. Hvis du vil ha mer informasjon, kan du se delen [Definere tilordningsgrupper (valgfritt)](#setting-up-assignment-groups-optional).
- **Leder** – Tilordne oppgaven til lederen til den ansatte som ansettes, avsluttes eller overføres.

    > [!IMPORTANT]
    > Når en sjekkliste brukes, og hvis ingen stilling i øyeblikket er tilordnet personen som er ansatt, avsluttet eller overført, kan lederen ikke bestemmes. I dette tilfellet tilordnes oppgaven til sjekklistens eier. Hvis du vil ha mer informasjon, kan du se delen [Konfigurere sjekklister](#setting-up-checklists).

- **Ansatt** – Tilordne personen som blir ansatt, avsluttet eller overført.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Forfallsdatoer for oppgave og Manglende samsvar for forfallsdato-feltet

Forfallsdatoene for oppgaven baseres på startdatoen for ansettelsen, oppsigelsesdatoen eller overgangsdatoen. Noen oppgaver må fullføres før startdatoen til en ansatt, mens andre oppgaver kan fullføres etter det. Når du definerer en oppgave, angir du en feltet **Manglende samsvar for forfallsdato** for å angi en forfallsdato som står i forhold til startdato, forfallsdato eller overgangsdato. En IT-ingeniør må for eksempel klargjøre en bærbar datamaskin for en nyansatt to dager før den ansattes startdato. I dette tilfellet, når du oppretter en konfigurasjonsoppgave for bærbar datamaskin, angir du feltet **Manglende samsvar for forfallsdato** tuk **-2**. Hvis startdatoen for en ansatt er 5. mai, forfaller oppgaven 3. mai.

> [!NOTE]
> Forfallsdato kan justeres etter at oppgaven er opprettet.

Forfallsdatoene beregnes på grunnlag av kalenderen som er knyttet til sjekklisten. Hvis du vil ha mer informasjon, kan du se delen [Konfigurere sjekklister](#setting-up-checklists).

### <a name="instructions"></a>Instruksjoner

Kompliserte oppgaver kan kreve flere trinn, eller personen som utfører oppgaven, må formidle tilleggsinformasjon. I feltet **Instruksjoner** kan du angi instruksjoner eller tilleggsinformasjon for å hjelpe personen som tilordnet oppgaven, med å fullføre den.

## <a name="setting-up-checklists"></a>Definere sjekklister

En sjekkliste er en gruppe oppgaver. Du kan opprette så mange sjekklister du krever, og du kan tilordne de samme oppgavene til flere sjekklister.

Hvis du vil opprette en ny oppgave i en sjekkliste, velger du **Ny** på **Oppgaver**-menylinjen. Når du oppretter en ny oppgave, kan du velge å legge den til i oppgavebiblioteket, slik at den kan deles på tvers av flere sjekklister. Du kan bare legge til oppgaven i biblioteket hvis alternativet **Bruk oppgave i bibliotek** er satt til **Ja**. Hvis du legger til oppgaven i oppgavebiblioteket, kan du også legge den til i andre sjekklister samtidig ved å velge disse sjekklistene i delen **Bruk på sjekklister**. Hvis du ikke legger til oppgaven i biblioteket, vil den bare finnes i sjekklisten som du oppretter den i.

Hvis du vil redigere en oppgave i sjekklisten, velger du **Rediger**. Hvis oppgaven er knyttet til en sjekkliste, vises disse sjekklistene på siden **Rediger oppgave**. Hvis du vil at oppgavene i de andre sjekklistene skal oppdateres med redigeringene, velger du disse sjekklistene i delen **Bruk på sjekklister**.

Hvis du vil fjerne oppgaver fra sjekklisten, velger du **Fjern**. Denne handlingen fjerner bare oppgaver fra sjekklisten. De slettes ikke fra oppgavebiblioteket. Hvis du vil slette en oppgave fra biblioteket, kan du gå til oppgavebiblioteksiden og velge **Slett**.

Når du oppretter en sjekkliste, angir du en eier og en kalender.

Hvis feltet **Tilordningstype** for en oppgave er satt til **Stilling**, **Leder** eller **Gruppe**, men ingen bestemt person kan avledes av tilordningstypen, blir oppgaven tilordnet sjekklistens eier. Her er noen eksempler på situasjoner der oppgaver blir tilordnet til sjekklisteeieren:

- Ingen stilling tilordnes den ansatte som blir ansatt eller avsluttes. Fordi den ansatte ikke har en posisjonstilordning, kan ikke lederen bestemmes.
- **Tildelingstype**-feltet er satt til **Stilling**, men ingen ansatte er tilordnet stillingen på tidspunktet da oppgaven opprettes. Oppgaven **Oppsett av bærbar datamaskin** tilordnes for eksempel til stillingsnummer 000876 (**Teknisk støtteekspert**). På det tidspunktet en person ansettes, er ingen ansatt tilordnet stilling 000876. Derfor blir det opprettet en oppgave for sjekklistens eier.
- **Tildelingstype**-feltet er satt til **Gruppe**, men ingen ansatte er tilordnet stillingene i gruppen på tidspunktet da oppgaven opprettes.

Kalenderen som er angitt for en sjekkliste, brukes til å beregne forfallsdatoen for oppgaver som er en del av sjekklisten. Arbeidsdager og fridager er definert i kalenderoppsettet. Virkedager inkluderes når forfallsdatoen til oppgaver beregnes, og fridager utelates. Fridager inkluderer helger og ferier. 

Når en kalender er definert, knyttes den til en sjekklistemal. På den måten beregnes forfallsdatoen til hver oppgave i sjekklisten på samme måte. Du kan definere flere kalendere, men bare én kalender kan knyttes til hver sjekkliste.

## <a name="setting-up-assignment-groups-optional"></a>Definere tilordningsgrupper (valgfritt)

Noen ganger er det en gruppe enkeltpersoner som er ansvarlig for en oppgave. En gruppe IT-medarbeidere kan for eksempel være ansvarlige for å klargjøre bærbare maskiner for nye ansettelser.

Følg disse trinnene for å konfigurere en tilordningsgruppe.

1. Velg **Ny** på siden **Gruppetilordninger**.
1. Skriv inn et navn (for eksempel **IT Bærbar datamaskin**) og en beskrivelse av gruppen.
1. Velg **Lagre**.
1. Velg **Legg til** på hurtigfanen **Medlemmer**.
1. Velg alle stillinger som er ansvarlige for oppgaven, i **Stillinger**-feltet.

Når en tilordningsgruppe er opprettet, kan den velges når en oppgave opprettes. Hvis du vil velge en bestemt gruppe for en oppgave, må du velge **Gruppe** i **Tildelingstype**. Gruppen du opprettet, er deretter tilgjengelig i feltet **Tilordnet til**.

> [!IMPORTANT]
> Hvis en oppgave tilordnes en gruppe, merkes oppgaven som **Fullført** når én person i gruppen fullfører den. Oppgaver opprettes på tidspunktet for ansettelse, avslutning eller overgang. De opprettes for brukere som er tilordnet stillingene som er inkludert i gruppen.

## <a name="setting-up-task-groups-optional"></a>Definere oppgavegrupper (valgfritt)

Prosessen med pålasting, avlasting og overgang kan inneholde mange oppgaver. For å gjøre det enklere å tilordne alle de nødvendige oppgavene til en sjekkliste, kan du opprette valgfrie oppgavegrupper for å kategorisere relaterte oppgaver. For eksempel må personal-, IT- og lønnsavdelingene fullføre bestemte oppgaver for å ansette en person. Derfor oppretter du følgende oppgavegrupper: **HR**, **IT** og **Lønn**. Når du oppretter en oppgave, kan du deretter knytte en av disse oppgavegruppene til den.

Når du vil legge til en oppgave i en sjekkliste, kan du filtrere listen med oppgaver etter oppgavegruppen som den ønskede oppgaven er tilordnet. Når du for eksempel oppretter en sjekklistemal, kan du filtrere listen slik at bare IT-oppgavene som er tilordnet til **IT**-oppgavegruppen, vises. Derfor kan du sikre at bare de relevante IT-oppgavene er valgt.

## <a name="using-checklists"></a>Bruke sjekklister

Når en arbeider ansettes, avsluttes eller overføres, kan du velge én eller flere sjekklister. Forfallsdatoer og arbeidertilordninger opprettes etter at ansettelses-, oppsigelses- eller overgangsprosessen er fullført. Når du for eksempel velger knappen **Ansett** eller **Ansett og legg til detaljer**, opprettes oppgaver for enkeltpersoner basert på tilordningstypen.

En forfallsdato tilordnes hver oppgave ved å legge til eller trekke fra forfallsdatoen med manglende samsvar fra den ansattes startdato. Hvis du vil ha mer informasjon, kan du se delen [Forfallsdatoer for oppgave og Manglende samsvar for forfallsdato-feltet](#task-due-dates-and-the-due-date-offset-field).

Hvis du bruker personalhandlinger, opprettes oppgavene når **Fullfør**-knappen velges eller handlingen godkjennes.

I arbeidsområdet for **Oppgavebehandling** kan du bruke en sjekkliste for en ansatt ved å velge den ansatte på siden for enkel liste eller detaljsiden, og deretter velge **Bruk sjekkliste**. Verdien i feltet **Måldato** brukes til å beregne forfallsdatoen for oppgavene. Måldatoen bør vanligvis samsvare med den ansattes dato for ansettelse, oppsigelse eller overgang.

Du kan også bruke en sjekkliste for en ansatt ved å åpne siden for **Arbeider** og velge **Sjekklister** på menyen.

## <a name="completing-tasks"></a>Fullføre oppgaver

På siden **Ansattselvbetjening** kan en ansatt vise alle oppgaver som er tilordnet dem. For hver tildelte oppgave vises verdiene **Oppgave**, **Beskrivelse**, **Instruksjoner** og **Kontaktperson**. For hver oppgave kan den ansatte dessuten åpne den tilknyttede eksterne websiden eller den tilknyttede siden i Dynamics 365-appen.

Oppgaver kan også vises på standard instrumentbord. Slik viser du oppgaver på standard instrumentbord:
1. Gå til **Brukeralternativer – Innstillinger – Oppgavebehandling** 
2. Velg **På** for **Vis oppgaver på standard instrumentbord**.  

>[!Note] 
>Funksjonen **Oppgavebehandling** må være aktivert i **Funksjonsbehandling** for at alternativet skal vises i **Brukeralternativer**.

Oppgaver kan være merket som **Pågår**, **Avbrutt** eller **Fullført**. Hvis en oppgave er tilordnet en gruppe, merkes den som **Fullført** når én person i gruppen fullfører den.

Oppgaver kan også tilordnes på nytt.
