---
title: Egendefinerte felt
description: "Dette emnet forklarer hvordan Microsoft Dynamics 365 for Finance and Operations lar noen brukere opprette egendefinerte felt for å tilpasse programmet slik at det passer for bedriften."
author: jasongre
manager: AnnBe
ms.date: 01/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 5c66f893b0dc26b01e7c4eb024ef543f915bfe9f
ms.openlocfilehash: e272b846fba16445d3a48f9e6c33805d7b4f4d38
ms.contentlocale: nb-no
ms.lasthandoff: 01/19/2018

---

# <a name="custom-fields"></a>Egendefinerte felt

[!include[banner](../includes/banner.md)] 

[!include[banner](../includes/pre-release.md)] 

Selv om Microsoft Dynamics 365 for Finance and Operations, Enterprise edition inneholder et omfattende sett med felt som standard for å administrere mange forretningsprosesser, har et firma noen ganger behov for å spore ytterligere informasjon i systemet. For å legge til rette for dette behovet lar Finance and Operations deg opprette egendefinerte felt for å tilpasse programmet i tråd med bedriftens behov, forutsatt at du har tilgang til funksjonen.

Denne videoen viser hvor enkelt det er å legge til et egendefinert felt på en side.


> [!Video https://www.youtube.com/embed/gWSGZI9Vtnc]

## <a name="creating-custom-fields"></a>Opprette egendefinerte felt
Når du har identifisert tilleggsinformasjon du vil spore i programmet, kan du opprette det egendefinerte feltet i den aktuelle tabellen og vise det nye feltet på en side.   

Trinnene nedenfor beskriver prosessen for å opprette et egendefinert felt og plassere dette feltet i et skjema.  

1.   Naviger til skjemaet der det er behov for det nye feltet. 
2.   Fordi sluttmålet er å vise det egendefinerte feltet i et skjema, finnes inngangspunktet for å opprette egendefinerte felt i tilpassingsopplevelsen. Åpne tilpassingsverktøylinjen ved å velge **Alternativer** og deretter **Tilpass dette skjemaet**. 
3.   Klikk **Sett inn** og deretter **Felt**.  
4.   Velg området i skjemaet der du vil vise det nye feltet. Når du har valgt det, viser **Sett inn felt**-dialogboksen en liste over eksisterende felt som kan settes inn i det merkede området i skjemaet.  
5.   Kontroller at feltet du er interessert i, ikke allerede finnes i listen. Hvis det finnes, kan du ganske enkelt velge feltet i listen og klikke **Sett inn**.   
6.   Klikk **Opprett nytt felt**-knappen over listen for å starte prosessen med å lage et egendefinert felt. Dette åpner **Opprett nytt felt**-dialogboksen. 

     Hvis du ikke ser **Opprett nytt felt**-knappen, har du ikke de nødvendige tillatelsene til å bruke denne funksjonen.  
     
7.   Angi følgende informasjon i dialogboksen **Opprett nytt felt**.
     1.   Velg databasetabellen der dette feltet skal legges til. Legg merke til at bare tabeller som støtter egendefinerte felt, vises i fra rullegardinlisten. Se delen nedenfor for tekniske detaljer om støttede tabeller.  
     2.   Velg datatypen for det nye feltet. Tilgjengelige datatyper er avmerkingsboks, dato, dato/klokkeslett, desimal, tall, plukkliste og tekst.   
          - Hvis du velger datatypen tekst, kan du også angi den maksimale lengden på teksten som kan angis i dette feltet. 
          - Hvis du velger datatypen plukkliste, kan du også velge settet med gyldige verdier for feltet.  
     3.   Angi navn, etikett, og hjelpetekst for feltet. Navnet tilsvarer det fysiske feltnavnet i databasen, mens etikett- og hjelpeteksten er teksten som brukes til å representere dette feltet i brukergrensesnittet.  
8.   Hvis dette er det eneste feltet du vil opprette for dette skjemaet, klikker du **Lagre**. Hvis du vil opprette flere felt, klikker du **Lagre og ny** og går tilbake til trinn 7. Legg merke til at det er en grense på **20 egendefinerte felt per tabell**.
9.   Når du avslutter **Opprett nytt felt**-dialogboksen, kommer du tilbake til **Sett inn felt**-dialogboksen. Egendefinerte felt som nettopp ble lagt til, merkes automatisk i feltlisten til å bli satt inn i skjemaet.  
10.   Klikk **Sett inn** for å sette inn de merkede feltene i det valgte området i skjemaet. 
11.   **Valgfritt:** Aktiver **Flytt**-modus fra tilpassingsverktøylinjen for å flytte de nye feltene til ønsket plassering i det valgte området. Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om hvordan du bruker de ulike tilpassingsfunksjonene for å optimalisere et skjema for din personlige bruk.  

## <a name="sharing-custom-fields-with-other-users"></a>Dele egendefinerte felt med andre brukere
Når du har opprettet et egendefinert felt og vist det i et skjema, kan det hende at du vil gi denne oppdaterte sidevisningen som inneholder det nye feltet, til andre brukere i systemet. Dette kan gjøres på to forskjellige måter ved hjelp av tilpassingsfunksjonene i produktet:

-   Den anbefalte måten er via systemadministratoren, som kan overføre en tilpassing til alle brukere eller en undergruppe av brukere. Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon. 

-   Du kan også eksportere endringene (kalt *tilpasninger*), sende dem til én eller flere brukere, og få hver av disse brukerne til å importere endringene. Med **Behandle**-alternativet på tilpassingsverktøylinjen kan du eksportere og importere tilpasninger.

## <a name="managing-custom-fields"></a>Behandle egendefinerte felt

Administrasjon av alle de egendefinerte feltene i systemet kan gjøres ved hjelp av **Egendefinerte felt**-siden i systemadministrasjonsmodulen.  Denne siden gir brukere tilgang til mange funksjoner, som: 
-   Vise en liste over alle de egendefinerte feltene i systemet.
-   Begrenset redigering av eksisterende egendefinerte felt.
-   Slette egendefinerte felt.
-   Vise egendefinerte felt på dataenheter.
-   Gi oversettelser av etiketter og hjelpetekst for egendefinerte felt.

### <a name="viewing-all-custom-fields"></a>Vise alle egendefinerte felt
**Egendefinerte felt**-siden gir en oversikt over alle de egendefinerte feltene som er definert i systemet. Bare velg tabellen som du er interessert i, og siden oppdateres og vil vise en liste over de egendefinerte feltene som er knyttet til denne tabellen. Hvis du velger et egendefinert felt fra listen, kan du vise alle detaljene om feltet.

### <a name="editing-custom-fields"></a>Redigere egendefinerte felt
Når du har opprettet et egendefinert felt, er det bare bestemte deler av informasjonen om det egendefinerte feltet som kan endres på **Egendefinerte felt**-siden.   

Du *kan* endre disse attributtene: 
-   Etikett 
-   Hjelpetekst
-   Lengde, for tekstfelt

Du *kan ikke* redigere følgende attributter: 
-   Feltnavn
-   Datatype

I tillegg, for plukklistefelt, kan du endre rekkefølgen på settet med gyldige verdier for det egendefinerte feltet og legge til nye verdier. Eksisterende verdier for plukklistefeltet kan imidlertid ikke fjernes. Husk å klikke **Bruk endringer** når du er ferdig med å redigere feltene for en bestemt tabell slik at endringene lagres. 

### <a name="exposing-custom-fields-on-data-entities"></a>Vise egendefinerte felt på dataenheter
Det kan også være viktig å tillate at egendefinerte felt kan vises på dataenheter. Dataenheter brukes i [Åpne på Office](../../dev-itpro/office-integration/office-integration.md)-funksjonen, samt for dataimport- og dataeksportscenarier.  

Følg denne fremgangsmåten for å vise et egendefinert felt på en dataenhet: 
1.   Velg det egendefinerte feltet i **Egendefinerte felt** skjemaet. 
2.   Utvid **Enheter**-delen til å vise settet med relevante enheter.  
3.   Klikk **Rediger**-knappen.
4.   Endre **Aktivert**-feltet slik at det velges for hver enhet som skal vise dette feltet.  
5.   Klikk **Bruk endringer** for å lagre valgene.  

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Tillate at egendefinerte felt vises på andre språk
Ettersom det kan være behov for tilgang til egendefinerte felt på forskjellige språk, har **Egendefinerte felt**-siden en mekanisme for å tillate at etikett- og hjelpeteksten for et egendefinert felt kan oversettes til andre språk.  

Trinnene nedenfor beskriver prosessen for å oversette egendefinerte felt til andre språk: 
1.   Velg det egendefinerte feltet på **Egendefinerte felt**-siden. 
2.   Velg **Oversettelser**-knappen i handlingsruten. Dette åpner en rullegardinmeny med eksisterende oversettelser for dette feltet.
3.   **Språk**-rullegardinmenyen viser settet med språk som det er allerede er gitt oversettelser for. 
     1.   Hvis du vil redigere en eksisterende oversettelse, velger du ønsket språk fra menyen og endrer verdiene for etiketten og hjelpeteksten.  
     2.   Ellers klikker du **Legg til språk**-knappen, velger ønsket språk fra menyen og angir deretter oversatte verdier for etikett- og hjelpeteksten.  
4.   Klikk på **OK** når du er ferdig.  

### <a name="deleting-custom-fields"></a>Slette egendefinerte felt
I enkelte sjeldne tilfeller kan du bestemme at et egendefinert felt ikke lenger er nødvendig. Når dette skjer, kan systemansvarlig velge å slette feltet fra **Egendefinerte felt**-siden. Hvis du vil gjøre dette, kontrollerer du at riktig felt er valgt, klikker **Slett**, klikker **Ja** for å bekrefte slettingen, og klikker til slutt **Bruk endringer**. 

> [!Note]
> Denne handlingen kan ikke angres, og fører til at dataene som er knyttet til feltet, slettes permanent fra databasen. 

## <a name="appendix"></a>Tillegg 
### <a name="who-can-create-custom-fields"></a>Hvem kan opprette egendefinerte felt?
Som en beskyttelse av systemet kan bare systemansvarlige opprette egendefinerte felt som standard. De privilegerte brukerne som organisasjonen anser som nødvendige, kan imidlertid gis rettigheter til å opprette egendefinerte felt av en systemansvarlig ved hjelp av sikkerhetsrollen **Privilegert bruker for kjøretidstilpasning**. Brukere uten denne sikkerhetsrollen kan ikke opprette egendefinerte felt, men vil fremdeles kunne se og samhandle med egendefinerte felt som er lagt til av andre brukere i systemet.    

### <a name="what-tables-support-custom-fields"></a>Hvilke tabeller støtter egendefinerte felt?
Av ytelsesårsaker og tekniske årsaker er det bare tabeller som oppfyller følgende vilkår som for tiden tillater at egendefinerte felt legges til.

- Tabellen må merkes som en av disse gruppene: 
     -   Gruppere
     -   WorksheetHeader
     -   Hoved
     -   Diverse
     -   Parameter
     -   Referanse
     -   TransactionHeader
- Tabellen kan ikke utvide en annen tabell.
- Tabellen kan ikke merkes som en systemtabell.
- Tabellen kan ikke være en midlertidig tabell.
