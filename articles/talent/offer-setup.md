---
title: Konfigurere tilbudsbehandling i Attract
description: Dette emnet beskriver hvordan du setter opp tilbud i Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63f45f1493935f543cfd25a7d8ed7b54170800a0
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832728"
---
# <a name="set-up-offer-management-in-attract"></a>Konfigurere tilbudsbehandling i Attract

[!include [banner](includes/banner.md)]

Når en kandidat flyttes til tilbudstrinnet i Dynamics 365 Talent: Attract, må du forsikre deg om at tilbudene kan opprettes raskt for kandidaten, godkjent etter behov, og sendes ut til kandidaten. Siden de fleste tilbud er standard, kan de opprettes fra maler som kan brukes på nytt. I Attract er alle tilbud samlet i en pakke for tilbudet, som er en samling av ett eller flere tilbudsdokumenter. 

Dette emnet viser alle trinnene som Attract-administrator vil bruke for å definere ulike tilbudspakkemaler som en del av funksjonen for tilbudsadministrasjon i Attract. Brukere med roller som ikke er administrator, får ikke tilgang til disse funksjonene.

>[!NOTE]
> Tilbudsadministrasjonsfunksjonene er tilgjengelige som en del av tillegget for omfattende ansettelse.

## <a name="offer-data"></a>Tilbudsdata 

Tilbudsdata er den minste enheten i tilbudspakkemalen. Et vanlig tilbud består av standardtekst og et sett med verdier. Settene med verdier er de eneste delene som kan endres mellom tilbud. Under opprettingen av tilbud er det viktigste aspektet som personen som oppretter tilbudet kan fokusere på, en liste over tilbudsdataplassholdere som finnes i en tilbudspakkemal. Hvis du vil angi data for tilbudet, kan du gjøre følgende:

1.  Gå til **Tilbudsadministrasjon**.

1.  Utvid **Biblioteket**-delen i den venstre navigasjonsruten, og gå deretter til **Tilbudsdata**.

    >[!NOTE]
    > På **Tilbudsdata**-siden finnes delene **Kandidatdetaljer** og **Jobbdetaljer**. Attract innehoder noen datatilbudsplassholdere som standard.
    
    > Det er inndelinger på siden for å organisere ulike tilbudsdataplassholdere sammen i logiske grupper. Disse delene kan hjelpe med vedlikehold av tilbudsdata og populasjon av data under oppretting av tilbud.

1.  For å opprette en ny tilbudsdatadel klikke på **Legg til en seksjon**, og angi et unikt navn for seksjonen.

1.  For å legge til tilbudsdataplassholdere i en seksjon klikk på **Legg til tilbudsdata**, og angi et unikt navn for plassholderen.

1.  Hvis du vil redigere navnet på en seksjon, holder du pekeren over navnet på seksjonen og oppdaterer navnet.

1.  Hvis du vil redigere navnet på eksisterende tilbudsdataplassholdere, må du først kontrollere at plassholderen ikke allerede er en del av en mal. Deretter holder du pekeren over navnet på plassholderen for tilbudsdata og oppdatere navnet etter behov.

1. Hvis du vil slette en eksisterende tilbudsdataplassholder, må du først kontrollere at plassholderen ikke er en del av en annen mal. Deretter holder du pekeren over plassholderen, og når papirkurvikonet vises, klikker du på papirkurven for å slette tilbudsdataplassholderen.
    >[!NOTE]
    > Du kan se hvor mange maler som en plassholder for tilbudsdata er en del av, ved å se på tallindikatoren ved siden av hvert enkelt tilbudsdata. 

1. Hvis du vil slette en seksjon, holder du pekeren over navnet. Hvis ingen av tilbudsdataplassholderne i seksjonen vises i en mal, kan du klikke på papirkurvikonet for å slette den. 
    >[!NOTE]
    > Ved å slette seksjonen slettes også alle tilbudsdataplassholdere i seksjonen.

Når tilbudsdataplassholderne er opprettet, kan du bruke dem på tvers av alle dokumentmaler. Tilbudsdataplassholdere er ikke begrenset til en bestemt mal – samme sett kan brukes på tvers av alle maler.

## <a name="offer-data-rules"></a>Regler for tilbudsdata

De fleste organisasjoner har regler for hvordan tilbud må opprettes. En organisasjon vil kanskje kreve at det maksimale årslønntilbudet for et bestemt sted og ansiennitetsnivå sammen må være innenfor et bestemt område, eller at det er bare noen få bestemte verdier som er mulige for tilbudsnivået for nyansettelsen. Attract støtter alle slike dataregler ved hjelp av en CSV-fil.

Når du skal klargjøre dataregel-CSV-filen, gjør du følgende:

1.  Bestem tilbudsdataplassholderen for regelsettet. For eksempel **Årslønn**.

1.  Identifiser de avhengige tilbudsdataplassholderverdiene. Eksempel **Jobbsted** og **Nivå**.

1.  Angi kolonne 1 og 2 som **Jobbsted** og **Nivå**.

1.  Hvis du vil laste opp en områdeverdi, kan du gjøre kolonnene 3 og 4 til **Årslønn**. Hvis du vil laste opp en bestemt verdi i stedet for et område, gjør du bare kolonne 3 til **Årslønn**.

1.  Fyll ut Microsoft Excel-filen basert på nødvendige rollene.

1.  Kontroller at hver rad er en unik kombinasjon av alle verdier som er satt sammen.

1.  Lagre filen i CSV-format.

Gjør følgende for å laste opp regelfilen for tilbudsdata:

1.  Gå til **Tilbudsadministrasjon**.

1.  Utvid **Bibliotek**-delen i det venstre navigasjonspanelet, og gå deretter til **Regler for tilbudsdata**.

1.  Klikk **Nytt datasett** for å vise **Last opp**-dialogboksen.

1.  Angi et unikt navn for regelsettet, og deretter last opp den lagrede CSV-filen.

1.  Klikk **Legg til**.
    Regelsettet behandles i bakgrunnen, og du blir varslet i programmet og via e-post når det er fullført.

    Du vil varsles hvis det er feil under behandling av opplastingen. Deretter kan du laste ned feilloggen, rette filen og laste opp på nytt.

1.  Bruk ellipseknappen (**...**) hvis du vil laste ned regelsettet og oppdatere settet med verdier. Når du har oppdatert, kan du laste opp filen på nytt.

1.  Du kan slette en eksisterende regelsettopplasting hvis plassholderen som defineres, ikke brukes i en annen dokumentmal.

>[!NOTE]
> - Hver plassholder kan bare ha ett unikt sett med kolonner som den er avhengig av. Hvis for eksempel **Årslønn** er avhengig av **Jobbsted** og **Nivå**, kan du ikke laste opp et annet regelsett der **Årslønn** er avhengig av et annet sett med kolonner.

> - Du kan laste ned eksempelsett med tilbudsdata i kategorien **Eksempler** på siden **Regler for tilbudsdata**.

> - Når en tilbudsoppretter overstyrer verdiene som er anbefalt av tilbudsdatareglene, flagges tilbudet som ikke-standard, og tilbudsgodkjenningsarbeidsflyten blir obligatorisk.

## <a name="document-templates"></a>Dokumentmaler

En tilbudsdokumentmal kan hjelpe administratorer med å opprette tilbudsbrev. Tilbudsdokumentmalen er en kombinasjon av teksten som skal inngå i tilbudet, i tillegg til de definerte tilbudsdataplassholderne. 

Hvis du vil opprette en tilbudsdokumentmal, må du gjøre følgende:

1.  Gå til **Tilbudsadministrasjon**.

1.  Utvid **Biblioteket**-delen i den venstre navigasjonsruten, og gå til **Maler**.

    **Maler**-siden viser en liste over dokumentmaler som allerede er definert.

1.  Klikk **Ny mal** for å opprette en ny dokumentmal.

1.  Angi et unikt navn for malen, og klikk på **Opprett**.

1.  Bruk redigeringsprogrammet for rik tekst til å sette inn eller redigere tilbudsdokumentinnholdet. Du kan sette inn tabeller, bilder og hyperkoblinger ved hjelp av alternativene som er tilgjengelige på toppen av tekstredigeringsprogrammet.

1.  Du kan sette inn tilbudsdataplassholdere i tilbudsmaldokumentet ved å:

    - Dra og slippe fra den høyre ruten.

    - Sett hashtag på tilbudsdataplassholderen direkte på posisjonen. Skriv inn **\#**, og skriv deretter inn navnet på tilbudsdataplassholderen. Alternativer vises i rullegardinlisten. Klikk eller trykk på **Enter** for å sette inn tilbudsdataplassholderen.

    >[!NOTE]
    > - Hvis du vil tilknytte en plassholder til tilbudsdokumentmalen uten å vise verdien til kandidaten, holder du pekeren over tilbudsdataplassholderen og klikker på **Fest**-ikonet. Dette vil flytte plassholderen til **Festede tilbudsdata**-delen i tilbudsdokumentmalen. For å fjerne festingen følg de samme trinnene, men klikk på **Løsne** i listen over tilbudsdataplassholdere.

    > - Hvis du vil vise listen over aktive tilbudsdataplassholdere, må du bytte til **Aktiv**-kategorien i høyre rute.

    > - Hvis du setter inn en plassholder som styres av et tilbudsregeldatasett, kan du se avhengigheten for denne dataplassholderen på andre verdier.

    > - Du kan også velge **Importer** for innholdet fra en DOCX-fil på den lokale maskinen og redigere etter behov. På den måten behøver du ikke å skrive inn alt innholdet i redigeringsprogrammet.

1. Hvis du vil forhåndsvise tilbudsdokumentet, kan du bruke **Forhåndsvisning**-alternativet øverst på siden.

1. For å kontrollere om en tilbudsoppretter kan redigere dokumentinnholdet, bruk alternativet **Administrer tillatelse** øverst på siden. Hvis du vil tilby oppretteren å bare sette inn plassholderverdier og ikke redigere tekst, angir du tillatelsesverdien til **Ingen**.

1. Klikk på **Lagre** for å lagre progresjonen. Malen lagres i en kladdetilstand.

1. For å fullføre og merke dokumentet som publisert, klikker du på **Fullfør**.

1. Du kan se hvilke dokumentmaler som er aktive, i utkastmodus, og som er arkiverte og er ikke lenger i bruk på startsiden for dokumentmalbiblioteket.

>[!NOTE]
> Du kan slette alle tilbudsdokumentmaler som ikke er en del av en eksisterende tilbudspakkemal.


## <a name="offer-package-templates"></a>Tilbudspakkemaler

Tilbudspakker er tilbudsartefaktene som deles med kandidaten og består av en kombinasjon av én eller flere tilbudsdokumentmaler. Hvis du vil opprette en pakke, må du gjøre følgende:

1.  Gå til **Tilbudsadministrasjon**.

1.  Gå til **Pakker** i den venstre navigasjonsruten.

    Det vises en liste over aktive pakkemaler som er tilgjengelige for tilbudsopprettere.

1.  Trykk på **Ny pakke** for å opprette en ny tilbudspakke.

1.  Angi et unikt navn, og klikk på **Opprett**.

1.  Klikk på **Legg til mal**.

    >[!NOTE]
    > - Du kan velge å opprette en ny mal eller velge fra en eksisterende mal.

    > - Hvis du vil legge til en eksisterende mal, må du kontrollere at tilbudsdokumentmalen ble lagret, fullført og merket som aktiv.
    
    > - Du kan velge så mange dokumentmaler som du vil. 
    
1.  Klikk på **Ferdig** å gå tilbake til **Pakkestyring**.

    Du kan konfigurere rekkefølgen på dokumentene og også angi om det bestemte tilbudsdokumentet er nødvendig under oppretting av tilbud. Personen som opprettet tilbudet, får muligheten til å slette dokumentene som er merket som **Ikke nødvendig**.

1. For å lagre tilbudspakkemalen slik at den kan brukes av alle opprettere av tilbud, klikk på **Lagre og publiser**.

   Hvis du vil vise utkast av tilbudspakkemaler, gå til **Kladder**-kategorien. Hvis det gjøres en endring i tilbudspakkemalen, må den lagres og publiseres på nytt.

## <a name="configure-an-offer-process"></a>Konfigurere en tilbudsprosess

Det er flere deler av tilbudsopprettingsprosessen som kan konfigureres av en Attract-administrator.

- **Tilby godkjenninger** – Velg om tilbudsgodkjenninger kreves før tilbudet kan sendes til kandidaten. Som administrator kan du også bestemme om alle tilbudsgodkjenninger skal skje i rekkefølge eller i en parallell godkjenningsarbeidsflyt. Du kan også gjøre det obligatorisk om tilbudsgodskjennere må legge til en kommentar sammen med tilbudsgodkjenningen. Tilbudsgodkjennere er obligatoriske for alle ikke-standard tilbud.

- **Kandidatens tilbudserfaring** – Som administrator kan du velge å angi om alle tilbud skal ha en utløpsdato, og i så fall hva som skal være standard forskyvning for utløpsdatoen. Du kan også konfigurere om kandidater kan avvise et tilbud.

- **e-signaturer** - Som administrator kan du også velge metoden som kandidater kan bruke til å signere tilbud.
    - Adobe Sign - Alle tilbudspakker blir sendt og signert via Adobe Sign. Hver tilbudsoppretter som publiserer tilbudet, må ha sin Adobe Sign-konto knyttet til Attract. For Adobe Sign-lisenser og en kostnadsfri prøveversjon kan du velge denne [koblingen](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).

    - DocuSign - Alle tilbudspakker blir sendt og signert via DocuSign. Hver tilbudsoppretter som publiserer tilbudet, må ha sin DocuSign-konto knyttet til Attract. 
    
    - ESign - Dette er standardvalget, som følger med som standard, der brukeren kan signere et tilbud ved å skrive inn navn og initialer.


Hvis du vil vite mer om tilbudsopprettingsprosessen, kan du se [Opprette, godkjenne og signere tilbud](./creating-offers.md).
