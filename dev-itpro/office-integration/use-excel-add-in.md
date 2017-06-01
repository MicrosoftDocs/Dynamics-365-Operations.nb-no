---
title: Bruke Excel-tillegget
description: "Dette emnet forklarer hvordan du kan åpne enhetsdata i Microsoft Excel, og deretter vise, oppdatere og redigere dataene ved hjelp av Microsoft Dynamics Office-tillegget for Excel. Hvis du vil åpne enhetsdata, kan du starte fra Microsoft Excel eller Microsoft Dynamics 365 for Operations."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c391fb70d837db9c0f167b392291fc1c5cc2bb53
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="use-the-excel-add-in"></a>Bruke Excel-tillegget

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du kan åpne enhetsdata i Microsoft Excel, og deretter vise, oppdatere og redigere dataene ved hjelp av Microsoft Dynamics Office-tillegget for Excel. Hvis du vil åpne enhetsdata, kan du starte fra Microsoft Excel eller Microsoft Dynamics 365 for Operations.

Ved å åpne enhetsdata i Microsoft Excel, kan du raskt og enkelt vise, oppdatere og redigere dataene ved hjelp av Microsoft Dynamics Office-tillegget for Excel. Dette tillegget krever Microsoft Excel 2016. **Obs!** Hvis Microsoft Azure Active Directory-leieren (AD Azure) er konfigurert til å bruke Active Directory Federation Services (AD FS), må du kontrollere at oppdateringen fra mai 2016 er installert, slik at Excel-tillegg kan logge deg på på riktig måte.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Åpne enhetsdata i Excel når du starter fra Dynamics 365 for Operations
1.  Klikk på **Åpne i Microsoft Office** på en side i Microsoft Dynamics 365 for Operations. Hvis rotdatakilden (tabell) for siden er den samme som rotdatakilden for alle enheter, genereres standard **Åpne i Excel**-alternativer for siden. **Åpne i Excel**-alternativer finnes på ofte brukte sider, som **Alle leverandører** og **Alle kunder**.
2.  Klikk på et **Åpne i Excel**-alternativ, og åpne arbeidsboken som genereres. Denne arbeidsboken har bindingsinformasjonen for enheten, en peker til miljøet og en peker til Excel-tillegget.
3.  I Excel klikker du på **Aktivere redigering** for å aktivere kjøring av Excel-tillegget. Excel-tillegg kjøres i en rute til høyre i Excel-vinduet.
4.  Hvis du kjører Excel-tillegget for første gang, klikker du på **Klarer tillegget**.
5.  Hvis du blir bedt om å logge på, klikker du på **Logg på**, og deretter logger du på ved å bruke samme legitimasjon som du brukte til å logge på Dynamics 365 for Operations. Excel-tillegget bruker en tidligere påloggingskontekst fra Internet Explorer, og logger deg automatisk på, hvis det er mulig. Du må derfor kontrollere brukernavnet i øverst til høyre i Excel-tillegget.

Excel-tillegg leser automatisk dataene for enheten du valgte. Legg merke til at det ikke vises data i arbeidsboken før Excel-tillegget leser dem inn.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Åpne enhetsdata i Excel når du starter fra Excel
1.  I Excel, i kategorien **Sett inn**i **Tillegg**-gruppen, klikker du på **Store** for å åpne Office Store.
2.  Søk etter nøkkelordet Dynamics i Office Store, og klikke på **Legg til** ved siden av **Microsoft Dynamics Office-tillegg** (Excel-tillegget).
3.  Hvis du kjører Excel-tillegget for første gang, klikker du på **Klarer tillegget** for å aktivere kjøring av Excel-tillegget. Excel-tillegg kjøres i en rute til høyre i Excel-vinduet.
4.  Klikk på **Legg til serverinformasjon** for å åpne **Alternativer**-ruten.
5.  Kopier nettadressen i nettleseren fra målforekomsten av Dynamics 365 for Operations, lim den inn i **Server-URL**-feltet, og slett deretter alt etter vertsnavnet. Den resulterende URL-adressen må inneholde bare vertsnavnet.
Hvis URL-adressen for eksempel er https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage, sletter du alt unntatt **https://xxx.dynamics.com**.
6.  Klikk på **OK**, og klikk deretter på **Ja** for å bekrefte endringen. Excel-tillegget starter på nytt og laster inn metadata. **Utforming**-knappen er nå tilgjengelig. Hvis Excel-tillegget har en **Laste inn appleter**-knapp, er du sannsynligvis ikke logget på som riktig bruker. Hvis du vil ha mer informasjon, kan du se "Laste inn appleter-knappen vises" i delen "Feilsøking" i dette emnet.
7.  Klikk på **Utforming**. Excel-tillegget henter metadata for enhet.
8.  Klikk på **Legg til tabell**. Det vises en liste over enheter. Enhetene vises i formatet "Navn – Etikett".
9.  Velg en enhet i listen, for eksempel **Kunde – Kunder**, og klikk deretter på **Neste**.
10. Hvis du vil legge til et felt fra listen **Tilgjengelige felt** i listen **Valgte felt**, klikker du på feltet og deretter på **Legg til**. Du kan også dobbeltklikke på feltet.
11. Når at du har lagt til de aktuelle feltene i listen **Valgte felt**, kontrollerer du at markøren er på riktig sted i regnearket (for eksempel celle A1), og klikker deretter på **Fullført**. Klikk deretter på **Fullført** for å avslutte utformingen.
12. Klikk på **Oppdater** for å trekke inn et sett med data.

## <a name="view-and-update-entity-data-in-excel"></a>Vise og oppdatere enhetsdata i Excel
Når Excel-tillegget har lest inn enhetsdata i arbeidsboken, kan du oppdatere dataene når som helst ved å klikke på **Oppdater** i Excel-tillegget.

## <a name="edit-entity-data-in-excel"></a>Redigere enhetsdata i Excel
Du kan endre enhetsdata som du trenger, og deretter publisere dem tilbake ved å klikke på **Publiser** i Excel-tillegget. Hvis du vil redigere en post, merker du en celle i regnearket og endre deretter celleverdien. Hvis du vil legge til en ny post, gjør du ett av følgende:

-   Klikk hvor som helst i datakildetabellen, og klikker deretter på **Ny** i Excel-tillegget.
-   Klikk i den siste raden i datakildetabellen, og trykk deretter på Tab-tasten til markøren flyttes ut av den siste kolonnen i denne raden og det opprettes en ny rad.
-   Klikk i raden like under datakildetabellen, og begynner å skrive inn data i en celle. Når du flytter fokus fra cellen, utvides tabellen, slik at den nye raden tas med.
-   For feltbindinger for hodeposter velger du ett av feltene, og deretter klikker du på **Ny** i Excel-tillegget.

Legg merke til at en ny post bare kan opprettes hvis alle viktige og obligatorisk felt er bundet i regnearket, eller hvis standardverdiene er fylt ut ved hjelp av filterbetingelsen.
Hvis du vil slette en post, gjør du ett av følgende:

-   Høyreklikk på radnummeret ved siden av regnearkraden du vil slette, og klikk deretter på **Slett**.
-   Høyreklikk i regnearkraden du vil slette, og klikk deretter på **Slett** &gt; **Tabellrader**.
Hvis datakilder har blitt lagt til som tilknyttet, publiseres hodet før linjene. Hvis det finnes avhengigheter mellom andre datakilder, må du kanskje endre standard publiseringsrekkefølge. Hvis du vil endre publiseringsrekkefølgen, klikker du på **Alternativer** (tannhjul) i Excel-tillegget. I hurtigfanen **Datatilkobling** klikker du på **Konfigurer publiseringsrekkefølge**.

## <a name="add-or-remove-columns"></a>Legg til eller fjern kolonner
Du kan bruke utformingen til å justere kolonnene som automatisk legges til i regnearket.

1.  Start datakildeutformingen for Excel-tillegget ved å klikke på **Alternativer**-knappen (tannhjulsymbolet), og merk deretter av for **Aktiver utforming**.
2.  Klikk på **Utforming** i Excel-tillegget. Alle datakildene vises.
3.  Klikk på **Rediger**-knappen (blyantsymbolet) ved siden av datakilden.
4.  Juster listen i listen **Valgt felt** etter behov:
    -   Hvis du vil legge til et felt fra listen **Tilgjengelige felt** i listen **Valgte felt**, klikker du på feltet og deretter på **Legg til**. Du kan også dobbeltklikke på feltet.
    -   Hvis du vil fjerne et felt fra listen **Valgte felt**, klikker du på feltet og deretter på **Fjern**. Du kan også dobbeltklikke på feltet.
    -   Hvis du vil endre rekkefølgen på feltene, klikker du på feltet i listen **Valgte felt**, klikker på et felt, og klikker deretter på **Opp** eller **Ned**.

5. Hvis du vil bruke endringene for datakilden, klikker du på **Oppdater**. Klikk deretter på **Fullført** for å avslutte utformingen. 
6. Hvis du har lagt til et felt (kolonne), klikker du på **Oppdater** for å trekke inn et oppdatert sett med data.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Feilsøking
Det finnes enkelte problemer som kan løses ved hjelp av noen enkle trinn.

-   **Laste inn appleter-knappen vises.** Hvis Excel-tillegget har en **Laste inn appleter**-knapp etter pålogging, er du sannsynligvis ikke logget på som riktig bruker. Hvis du vil løse dette problemet, kontrollerer du at riktig brukernavn vises øverst til høyre i Excel-tillegget. Hvis feil brukernavn vises, klikker du på det, logger av og på igjen.
-   **Du får feilmeldingen "Forbudt".** Hvis du får feilmeldingen "Forbudt" når Excel-tillegget laster inn metadata, har kontoen som er logget Excel-tillegget, ikke tillatelse til å bruke tjenesten, forekomsten eller databasen. Hvis du vil løse dette problemet, kontrollerer du at riktig brukernavn vises øverst til høyre i Excel-tillegget. Hvis feil brukernavn vises, klikker du på det, logger av og på igjen.
-   **En tom nettside vises over Excel.** Hvis det åpnes en tom nettside i løpet av påloggingsprosessen, krever kontoen AD FS, men versjonen av Excel som kjører tillegget, er ikke ny nok til å laste inn dialogboksen for pålogging. Hvis du vil løse dette problemet, oppdaterer du Excel-versjonen du bruker. Hvis du vil oppdatere versjonen av Excel når du er i en virksomhet som er på den utsatte kanalen, kan du bruke [distribusjonsverktøyet for Office](https://technet.microsoft.com/library/jj219422.aspx) til [flytte fra den utsatte kanalen til gjeldende kanal](https://technet.microsoft.com/library/mt455210.aspx).





