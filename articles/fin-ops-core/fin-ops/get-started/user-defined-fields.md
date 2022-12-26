---
title: Opprett og arbeid med egendefinerte felt
description: Denne artikkelen forklarer hvordan du oppretter egendefinerte felt via brukergrensesnittet for å tilpasse programmet slik at det passer for bedriften.
author: jasongre
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18e7e8525352e8fdc397621c381ed4297837e30c
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887294"
---
# <a name="create-and-work-with-custom-fields"></a>Opprett og arbeid med egendefinerte felt

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Selv om det er et omfattende sett med felt som standard for å administrere mange forretningsprosesser, har et firma noen ganger behov for å spore ytterligere informasjon i systemet. Selv om programmerere kan brukes til å legge til disse feltene som utvidelser i utviklerverktøy, gjør funksjonen egendefinerte felt det mulig å legge til felt direkte fra brukergrensesnittet, slik at du kan skreddersy programmet slik at det passer til bedriften din ved hjelp av nettleseren.

*Bare brukere med spesialtilgang har tilgang til denne funksjonen.*

Denne videoen viser hvor enkelt det er å legge til et egendefinert felt på en side: [Legge til egendefinerte felt](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Opprette egendefinerte felt

Når du har identifisert tilleggsinformasjon du vil spore i programmet, kan du opprette det egendefinerte feltet i den aktuelle tabellen og vise det nye feltet på en side.

Trinnene nedenfor beskriver prosessen for å opprette et egendefinert felt og plassere dette feltet i en side.

1. Naviger til siden der det er behov for det nye feltet.
2. Fordi sluttmålet er å vise det egendefinerte feltet i et skjema, finnes inngangspunktet for å opprette egendefinerte felt i tilpassingsopplevelsen. Åpne tilpassingsverktøylinjen ved å velge **Alternativer** og deretter **Tilpass dette skjemaet**.
3. Klikk på **Sett inn** og deretter **Felt**.
4. Velg området i skjemaet der du vil vise det nye feltet. Når du har valgt det, viser **Sett inn felt**-dialogboksen en liste over eksisterende felt som kan settes inn i det merkede området i siden.
5. Bekreft at feltet du er interessert i, ikke allerede finnes i listen. Hvis det finnes, kan du ganske enkelt velge feltet i listen og klikke **Sett inn**.
6. Klikk på **Opprett nytt felt**-knappen over listen for å starte prosessen med å lage et egendefinert felt. Dette åpner **Opprett nytt felt**-dialogboksen.

    Hvis du ikke ser **Opprett nytt felt**-knappen, har du ikke de nødvendige tillatelsene til å bruke denne funksjonen.

7. Angi følgende informasjon i dialogboksen **Opprett nytt felt**.
   
    1. Velg databasetabellen der dette feltet skal legges til. Legg merke til at bare tabeller som støtter egendefinerte felt, vises i fra rullegardinlisten. Se delen nedenfor for tekniske detaljer om støttede tabeller.

    2. Velg datatypen for det nye feltet. Tilgjengelige datatyper er avmerkingsboks, dato, dato/klokkeslett, desimal, tall, plukkliste og tekst.

        - Hvis du velger datatypen tekst, kan du også angi den maksimale lengden på teksten som kan angis i dette feltet.
        - Hvis du velger datatypen plukkliste, kan du også velge settet med gyldige verdier for feltet.

    3. Angi navn, etikett, og hjelpetekst for feltet. Navnet tilsvarer det fysiske feltnavnet i databasen, mens etikett- og hjelpeteksten er teksten som brukes til å representere dette feltet i brukergrensesnittet.

8. Hvis dette er det eneste feltet du vil opprette for denne siden, klikker du **Lagre**. Hvis du vil opprette flere felt, klikker du **Lagre og ny** og går tilbake til trinn 7. 

>[!Note] 
> For øyeblikket er det en grense på **20 egendefinerte felter per tabell**.

9. Når du avslutter **Opprett nytt felt**-dialogboksen, kommer du tilbake til **Sett inn felt**-dialogboksen. Egendefinerte felt som nettopp ble lagt til, merkes automatisk i feltlisten til å bli satt inn i siden.
10. Klikk på **Sett inn** for å sette inn de merkede feltene i det valgte området i siden.
11. **Valgfritt:** Aktiver **Flytt**-modus fra tilpassingsverktøylinjen for å flytte de nye feltene til ønsket plassering i det valgte området. Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om hvordan du bruker de ulike tilpassingsfunksjonene for å optimalisere et skjema for din personlige bruk.

> [!WARNING]
> Muligheten til å angi verdier i et egendefinert felt som legges til en side, er avhengig av om tabellen som er knyttet til det egendefinerte feltet, kan redigeres eller være skrivebeskyttet. Når den tilknyttede tabellen er skrivebeskyttet, blir også alle felt som er koblet til denne tabellen, inkludert eventuelle egendefinerte felt, skrivebeskyttet.


## <a name="sharing-custom-fields-with-other-users"></a>Dele egendefinerte felt med andre brukere

Når du har opprettet et egendefinert felt og vist det på en side, kan det hende at du vil gi denne oppdaterte sidevisningen som inneholder det nye feltet, til andre brukere i systemet. Dette kan gjøres på to forskjellige måter ved hjelp av tilpassingsfunksjonene i produktet:

- Den anbefalte ruten er å **publisere en [lagret visning](saved-views.md)** med det egendefinerte feltet lagt til på siden for riktig sett med brukere. Hvis funksjonen for lagret visning ikke er aktivert, kan systemadministrator bruke tilpasningen for de ønskede brukerne fra siden **Tilpasning**. Hvis du vil ha mer informasjon, kan du se [Tilpasse brukeropplevelsen](personalize-user-experience.md).
- Du kan også eksportere endringene (kalt *tilpasninger*), sende dem til én eller flere brukere, og få hver av disse brukerne til å importere endringene. Med **Behandle**-alternativet på tilpassingsverktøylinjen kan du eksportere og importere tilpasninger.

## <a name="managing-custom-fields"></a>Behandle egendefinerte felt

Administrasjon av alle de egendefinerte feltene kan gjøres ved hjelp av **Egendefinerte felter**-siden i systemadministrasjonsmodulen. Denne siden gir brukere tilgang til mange funksjoner, som:

- Vise en liste over alle de egendefinerte feltene i systemet.
- Begrenset redigering av eksisterende egendefinerte felt.
- Slette egendefinerte felt.
- Vise egendefinerte felt på dataenheter.
- Gi oversettelser av etiketter og hjelpetekst for egendefinerte felt.

### <a name="viewing-all-custom-fields"></a>Vise alle egendefinerte felt

**Egendefinerte felt**-siden gir en oversikt over alle de egendefinerte feltene som er definert i systemet. Velg tabellen som du er interessert i, og siden oppdateres og vil vise en liste over de egendefinerte feltene som er knyttet til denne tabellen. Hvis du velger et egendefinert felt fra listen, kan du vise alle detaljene om feltet.

### <a name="editing-custom-fields"></a>Redigere egendefinerte felt

Når du har opprettet et egendefinert felt, er det bare bestemte deler av informasjonen om det egendefinerte feltet som kan endres på **Egendefinerte felt**-siden.

Du *kan* endre disse attributtene:

- Etikett
- Hjelpetekst
- Lengde, for tekstfelt

Du *kan ikke* redigere følgende attributter:

- Feltnavn
- Datatype

I tillegg, for plukklistefelt, kan du endre rekkefølgen på settet med gyldige verdier for det egendefinerte feltet og legge til nye verdier. Eksisterende verdier for plukklistefeltet kan imidlertid ikke fjernes. Klikk på **Bruk endringer** når du er ferdig med å redigere feltene for en bestemt tabell slik at endringene lagres.

### <a name="exposing-custom-fields-on-data-entities"></a>Vise egendefinerte felt på dataenheter

Det kan også være viktig å tillate at egendefinerte felt kan vises på dataenheter. Dataenheter brukes i [Oversikt over Office-integrering](../../dev-itpro/office-integration/office-integration.md)-funksjonen, samt for dataimport- og dataeksportscenarioer.

Følg denne fremgangsmåten for å vise et egendefinert felt på en dataenhet:

1. Velg det egendefinerte feltet på **Egendefinerte felt**-siden.
2. Utvid **Enheter**-delen til å vise settet med relevante enheter.
3. Klikk på **Rediger**-knappen.
4. Endre **Aktivert**-feltet slik at det velges for hver enhet som skal vise dette feltet.
5. Klikk på **Bruk endringer** for å lagre valgene.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Tillate at egendefinerte felt vises på andre språk

Ettersom det kan være behov for tilgang til egendefinerte felt på forskjellige språk, har **Egendefinerte felt**-siden en mekanisme for å tillate at etikett- og hjelpeteksten for et egendefinert felt kan oversettes til andre språk.

Trinnene nedenfor beskriver prosessen for å oversette egendefinerte felt til andre språk:

1. Velg det egendefinerte feltet på **Egendefinerte felt**-siden.
2. Velg **Oversettelser**-knappen i handlingsruten. Dette åpner en rullegardinmeny med eksisterende oversettelser for dette feltet.
3. **Språk**-rullegardinmenyen viser settet med språk som det er allerede er gitt oversettelser for.

    Hvis du vil redigere en eksisterende oversettelse, velger du språk fra menyen og endrer verdiene for etiketten og hjelpeteksten.

    Ellers klikker du **Legg til språk**-knappen, velger ønsket språk fra menyen og angir deretter oversatte verdier for etikett- og hjelpeteksten.

4. Klikk på **OK** når du er ferdig.

### <a name="deleting-custom-fields"></a>Slette egendefinerte felt

Når du bestemmer at et egendefinert felt ikke lenger trengs, kan systemansvarlig velge å slette feltet fra **Egendefinerte felter**-siden. Hvis du vil slette et egendefinert felt, velger du feltet du vil slette, klikker på **Slett**, klikker på **Ja** for å bekrefte slettingen, og klikker til slutt **Bruk endringer**.

> [!NOTE]
> Denne handlingen kan ikke angres, og fører til at dataene som er knyttet til feltet, slettes permanent fra databasen.

## <a name="appendix"></a>Tillegg

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a>Hvorfor kan jeg ikke angi en verdi i det egendefinerte feltet? 

Hvis du ikke kan skrive inn en verdi i det egendefinerte feltet når siden er i **redigeringsmodus**, kan dette skyldes at tabellen som feltet ble lagt til i, for øyeblikket er skrivebeskyttet. Alle feltene i en tabell blir skrivebeskyttet hvis backing-tabellen for øyeblikket er konfigurert som skrivebeskyttet på siden.   

### <a name="who-can-create-custom-fields"></a>Hvem kan opprette egendefinerte felt?

Bare systemadministratorer kan opprette egendefinerte felt som standard. De privilegerte brukerne som organisasjonen anser som nødvendige, kan imidlertid gis rettigheter til å opprette egendefinerte felt av en systemansvarlig ved hjelp av sikkerhetsrollen **Privilegert bruker for kjøretidstilpasning**. Brukere uten denne sikkerhetsrollen kan ikke opprette egendefinerte felt, men vil fremdeles kunne se og samhandle med egendefinerte felt som er lagt til av andre brukere i systemet.

### <a name="what-tables-support-custom-fields"></a>Hvilke tabeller støtter egendefinerte felt?

Av ytelsesårsaker og tekniske årsaker er det bare tabeller som oppfyller følgende vilkår som for tiden tillater at egendefinerte felt legges til.

- Tabellen må merkes som en av disse gruppene:

    - Gruppere
    - WorksheetHeader
    - Hoved
    - Diverse
    - Parameter
    - Referanse
    - TransactionHeader

- Tabellen kan ikke utvide en annen tabell.
- Tabellen kan ikke merkes som en systemtabell.
- Tabellen kan ikke være en midlertidig tabell.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Kan jeg referere til egendefinerte felt fra utviklerverktøy?  

Egendefinerte felt kan bare administreres gjennom brukergrensesnittet og kan ikke refereres til av koden. 

### <a name="how-can-i-move-custom-fields-between-environments"></a>Hvordan flytter jeg egendefinerte felter mellom miljøer? 

Den gjeldende anbefalingen for flytting av egendefinerte felter mellom miljøer er å opprette de egendefinerte feltene på nytt i målmiljøet manuelt. Slik viser du den fullstendige listen over egendefinerte felter i en bestemt tabell:
1. Gå til siden **Egendefinerte felter**, og velg tabellen fra rullegardinlisten. 
2. I målmiljøet følger du prosessen som beskrives tidligere i denne artikkelen, for å opprette hvert felt på nytt. 
3. Når alle feltene er opprettet, klikker du **Ta i bruk endringer**.  
4. Flytt alle tilpasningene som inneholder egendefinerte felter, ved å eksportere disse tilpasningene fra originalmiljøet og importere dem til målmiljøet.  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
