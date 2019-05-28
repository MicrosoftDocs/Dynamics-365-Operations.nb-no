---
title: Telefonsenterkataloger
description: Dette emnet beskriver telefonsenterspesifikke funksjoner for kataloger i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 65c1c3070aa48bf7a2016534071693716fabe831
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562747"
---
# <a name="call-center-catalogs"></a>Telefonsenterkataloger

[!include [banner](includes/banner.md)]

Dette emnet beskriver telefonsenterspesifikke funksjoner som er koblet til katalogegenskaper i Microsoft Dynamics 365 for Retail.

Katalogfunksjonene i Dynamics 365 for Retail kan brukes til flere formål. Opprinnelig ble funksjonene for katalog opprettet for å støtte integreringer med tredjeparts e-handel. Katalogoppsett tillatte selskaper å opprette en gruppering av produkter og attributter som kan publiseres eksternt for forbruk av en tredjeparts e-handelsløsning.

Når telefonsenterkanalstøtte ble lagt til Dynamics 365 for Retail, ble katalogkonseptet utvidet for å legge til flere muligheter for å støtte og behandle funksjoner relatert til tradisjonelle markedsføringskataloger direkte til kunde. Et selskap som er direkte til kunde vil ofte få utskrevne kataloger, som sendes til én eller flere segmenter av kunder. Disse katalogene får vanligvis bestemt kampanjer eller vil bare tre i kraft hvis kunden oppgir en identifikasjonskode for katalog ved oppretting av tilbudene.

Direkte til kunde-markedsføringsfirmaer er svært fokuserte på å spore responsen på disse katalogene for å sikre at kostnadene for å produsere og e-poste dem svarer seg. Hvis du vil spore responsen, skrives vanligvis en kode på baksiden av katalogen, og denne koden blir deretter forespurt og brukes når katalogmottakeren ringer for å bestille via telefon (eller nå er det mer vanlig at koden angis når kunden har sendt en ordre online). Selv om det finnes ulike bransjevilkår som brukes til å identifisere denne katalogsporingskoden (inkludert nøkkelkode, promokode, katalogkode, kildekode), refererer vi til koden i Dynamics 365 for Retail som **kilde kode-ID**.

## <a name="basic-catalog-setup"></a>Grunnleggende katalogoppsett

Gå til **Retail** \> **Kataloger og sortimenter** \> **Alle kataloger** for å konfigurere katalogen.

Når du oppretter en ny katalog, må du først koble katalogen til én eller flere kanaler for detaljhandel. Dette gjøres i hurtigkategorien **Detaljhandelskanaler** i skjemaet **Katalogoppsett**. Klikk **Legg til**, og velg én eller flere detaljhandelskanaler. Bare varer som er knyttet til den valgte kanalen [sortimenter](https://docs.microsoft.com/dynamics365/unified-operations/retail/assortments), kan brukes ved opprettelse av katalogen.

Hvis du vil legge til produkter i en katalog, må du velge et navigasjonshierarki. Navigasjonshierarkiet støtter kategoristrukturen for katalogen. Du må velge blant navigasjonshierarkier som er koblet til detaljhandelskanalene valgt i hurtigkategorien **Detaljhandelskanaler** på **Katalog**-siden. Hvis en navigasjonskanal ikke ble koblet til en kanal tidligere, kan du gå til **Retail** \> **Kanaloppsett** \> **Kanalkategorier og produktattributter** for å koble en navigasjonshierarkistandard til hver av detaljhandelskanalene.

På **Kataloger**-menykategorien på **Katalogoppsett**-siden klikker du på **Legg til produkter** for å konfigurere produktene som skal legges til i katalogen, eller velg en node i navigasjonshierarkiet (hvis du velger en node, endres skjermpresentasjonen slik at du kan legge til produkter direkte i en kategori i katalogen).

Klikk på den øverste noden i kataloghierarkiet for å gå tilbake til hodevisning for hovedkatalogen. Konfigurer ikrafttredelses- og utløpsdatoer etter behov i **Generelt**-hurtigkategorien.

Før katalogen er tilgjengelig for bruk, må den publiseres. Klikk **Valider katalog** på **Kataloger**-menyen for å behandle en validering. Dette er påkrevd handling og vil kontrollere at den nødvendige konfigurasjonen er riktig. Klikk på **Vis resultater** for å se detaljene for valideringen. Hvis det oppdages feil, må du rette dataene og kjøre validering på nytt helt til valideringen er bestått.

Når valideringen er bekreftet, klikker du på **Arbeidsflyt** på menyen for å starte godkjenningsarbeidsflyten. Klikk på **Send** på **Arbeidsflyt**-menyen for å kjøre prosessen. Konfigurer trinnene og godkjente brukere for arbeidsflyten fra **Retail** \> **Hovedkvarteroppsett** \> **Detaljhandelsarbeidsflyter**. Arbeidsflyten definerer trinnene for å få katalogen til en **Godkjent**-status. Når mappen er i en **Godkjent**-status, kan du klikke **Publiser**-alternativet på **Kataloger**-menyen for å fullføre prosessen. Etter at katalogen er i en **Publisert**-status, den kan brukes i ordreregistrering i telefonsenteret og send katalog-prosesser.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Bruk katalogene til å kjøre salgsordrepriser og kampanjer

En hovedårsak for å definere en katalog for bruk med et kundesenter, er for å konfigurere spesifikke priser og kampanjer for katalogen. Kunder som bestiller fra denne katalogen, får disse prisene og kampanjene i ordreregistrering i telefonsenteret hvis katalogens **Kildekode-ID** er brukt på ordrehodet eller -linjer.

Du kan konfigurere katalogspesifikke priser ved å velge **Prisgrupper**-valget fra **Kataloger**-kategorien for å koble én eller flere prisgrupper til katalogen. Alle handelsavtaler, prisjusteringsjournaler og avanserte rabatter for detaljhandel (terskel, antall, samlerabatt) som er koblet til samme prisgruppe, vil bli brukt når kunder bestiller fra denne katalogen.

På **Kildekoder**-hurtigkategorien klikker du **Legg til** for å legge til én eller flere **Kildekode-ID**-identifikatorer i denne katalogen. Dette er koden som skal brukes under ordreregistrering i telefonsenteret til salgsordrehodet (og -linjene). Denne koden brukes til å knytte salgsordren i katalogen og til slutt til prisgruppene og spesialpriser og -kampanjer som er konfigurert.

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Bruk kilde-ID-en til å spore kostnader og svarrater

Når du definerer **Kildekode-ID**, kan du velge å koble denne ID-en til en **Målmarkeds-ID**. **Målmarkeds-ID** kan defineres i **Retail** \> **Kunder** \> **Målmarked**. Målmarkedet er en liste over kunder og/eller kundeemner som hører til et brukerdefinert segment. Kobling av kunde- eller kundeemnedata til kildekoden-ID gir bedre oversikt over mottakerne av katalogen. Hvis en kunde er koblet til et målmarked og målmarkedet er koblet til en aktiv kildekode-ID/-katalog, vil telefonsenterbrukere kunne se hvilke kataloger en kunde har mottatt ved å velge **Kildekoder**-menyalternativet i **Kunder**-menykategorien på **Kundestøtte**-siden. Under ordreregistrering kan telefonsenterbrukere også se de bestemte katalogene en kunde ble sendt, i **Kilde**-rullegardinlisten i salgsordrehodet. Ved å endre filteret fra **Alle** til **Målrettet** kan brukeren se de bestemte aktive katalogene kunden ble sendt. Dette er nyttig i situasjoner hvor kunden kan ha glemt katalogen sin eller ikke kan finne eller lese katalogkoden når de ringer for å opprette en salgsordre.

Det er mulig å koble flere kildekoden-ID-er til en katalog. Dette er ofte nødvendig når et selskap vil spore responsen etter forskjellige segmenter. Firmaet vil gi en unik katalogkode til ulike kundesegmenter, som gjør det mulig å spore responsraten ned til segmentnivå i en bestemt kataloghendelse.

Hvis du velger en bestemt **Kildekode-ID**-post og klikker på **Detaljer**-alternativet på **Kildekoder**-hurtigkategorien, vises flere felt der salgsprognoser, utsendelseskostnader og forsendelsesdatoer kan registreres. Disse dataene er nyttige for å gjøre detaljert analyse over effektiviteten i katalogen. Brukere kan gå tilbake til denne siden over tid og bruke **Kildekodeanalyse**- og **Sammenlign kampanjer**-knappene til å utløse analyserapporter basert på gjeldende salgsdata og sammenligne kostnader og budsjett med faktiske beløp.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Konfigurer katalogspesifikke ordre- og vareskript

Når en telefonsenterbruker oppretter en salgsordre, kan vedkommende bruke skript på skjermen. Disse skriptene er tekstbaserte og kan gi tilleggsinformasjon som brukeren bør si til kunden, eller det kan være interne merknader/påminnelser som telefonsenterbrukeren kan gjennomgå og reagere på når de oppretter salgsordren.

Det er ofte nyttig å ha forskjellige sett med skript for ulike kataloger. På **Skript**-hurtigfanen kan forhåndsdefinert skript kobles til en katalog. Bruk **Tidsberegning**-feltet for å angi om skriptet skal vises i begynnelsen av ordren (så snart kildekode-ID-en registreres i ordrehodet) eller på slutten av ordren (i sammendragsskjemaet for salgsordre).

Når du velger en node i katalogens hierarki og arbeider med dataene på **Produkter**-hurtigfanen, kan brukere også koble skript som er spesifikke for kataloger eller elementer, ved hjelp **Skript**-handling.

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Konfigurere katalogspesifikk mersalg og kryssalgelementer

Kobling av mersalg-/kryssalgforslag til en vare kan gjøres fra produktoppsettet, men i noen tilfeller kan et firma fremme spesialmersalg/kryssalg til kunder som bestiller et bestemt produkt fra en bestemt katalog. På **Produkter**-hurtigkategorien kan du velge en vare og klikke på **Mersalg/kryssalg av varer** for å konfigurere produkter som skal selges via mersalg eller kryssalg til kunder som kjøper den valgte varen fra katalogen. Under ordreregistrering i telefonsenteret, vil katalogspesifikke mersalgsvarer/kryssalgsvarer vises på skjermen i stedet for standard mersalgs-/kryssalgsprodukter som kan ha blitt konfigurert for denne varen via den vanlige produktkonfigurasjonen.

Mersalg/kryssalg av varer kan også dra nytte av skriptfunksjonene for å vise bestemte meldinger som brukeren vil se når elementet for mersalg/kryssalg vises under ordreregistrering. Skript som er knyttet til mersalg/kryssalg-produkter som er konfigurert spesifikt for et katalogprodukt, vises bare når kildekoden for katalogen brukes i ordreregistrering i telefonsenteret.

## <a name="catalog-page-analysis"></a>Katalogsideanalyse

I **Kataloger**-kategorien er alternativer tilgjengelige for å konfigurere **Katalogsider**. Med denne funksjonen kan du definere bestemte sider og sidetyper for den utskrevne katalogen og de tilknyttede kostnadene.

Når du konfigurerer produktene i katalogen, kan du bruke **Produktsideoppsett**-handlingen til å definere spesifikke sider, prosent av siden og plassering av sidedetaljer for varen. Konfigurering av disse dataene gjør det mulig for brukere å dra nytte av **Rapport for katalogområdeanalyse**. Denne rapporten finner du ved å gå til **Retail** \> **Telefonsenterrapporter** \> **Katalogområdeanalyse**-rapporten. Denne rapporten analyserer salg som plasseres i katalogen (salgsordrer der kilde-ID-en for katalogen ble knyttet til ordrehodet eller -linjen) og deres tilknyttede prosent av siden og kostnader for å gi en tradisjonell direktemarkedsførings **Kvadrattommeanalyse**-rapport.

## <a name="catalog-requests"></a>Katalogforespørsler

Ettersom kataloger konfigureres og publiseres i Dynamics 365 for Retail, kan **Send katalog**-funksjonen brukes. Denne funksjonen er tilgjengelig på **Kundesøk**- og **Kundeservice**-sider. Når du har valgt en kundepost gjennom **Kundesøk** eller ved visning av en bestemt kundekonto fra **Kundestøtte**, kan brukere velge **Send katalog**-alternativet, som åpner en dialogboks som tillater brukeren å velge fra en liste over alle publiserte og aktive kataloger. Brukeren kan velge en katalog og et antall og en bestemt kildekode-ID for sending. Når de klikker på **Send**-knappen, lagres en forespørsel som deretter kan administreres ved å skrive ut **Katalogforespørsler**-rapporten. Denne rapporten finner du ved å gå til **Retail** \> **Telefonsenterrapporter** \> **Katalogforespørselsrapport**. Den viser alle katalogforespørsler, inkludert kundenavnet og -adressedetaljene til kunden som ba om katalogen. Denne rapporten kan brukes internt, eller dataene kan overføres til en tredjepart som støtter eksterne prosesser for fysisk sending av katalogen til kunden.

## <a name="additional-features"></a>Tilleggsfunksjoner

I **Kataloger**-kategorien er også alternativer for konfigurasjon av en **Betalingsplan** og **Gratisprodukter** tilgjengelige. Hvis kildekode-ID-en som er koblet til katalogen, brukes under ordreregistrering i telefonsenteret, blir kunden berettiget til gratisprodukter eller bruk av bestemte katalogbetalingsplaner som definert. Hvis det er nødvendig å begrense kunden til å bare kunne velge fra betalingsplaner som er koblet til deres katalog og ikke alle aktive betalingsplaner i systemet, kan **Tillat bare katalogplaner** være merket av for én eller flere av kildekode-ID-ene som er definert for å håndheve denne begrensningen.

## <a name="additional-notes"></a>Tilleggsmerknader

For øyeblikket, når en kildekode-ID brukes for en salgsordre i telefonsenteret, brukes den til å drive priser, kampanjer, skript og mersalg/kryssalg som er katalogspesifikke. Systemet vil ikke forby eller hindre et produkt som ikke er i katalogen, i å bli bestilt på salgsordren. Hvis en vare er bestilt som ikke er en del av katalogen, bruker systemet først **Prisgruppen** som er definert i telefonsenterkanalen (**Retail** \> **Kanaler** \> **Telefonsentre** \> **Alle telefonsentre**), for varepris eller kampanjer. Hvis det ikke finnes noen bestemt kanalpris, brukes basissalgsprisen for varen.
