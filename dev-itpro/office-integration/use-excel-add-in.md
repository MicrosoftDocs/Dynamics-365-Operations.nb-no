---
title: Bruke Excel-tillegg
description: "Dette emnet forklarer hvordan du kan åpne enhetsdata i Microsoft Excel, og deretter vise, oppdatere og redigere dataene ved hjelp av Microsoft Dynamics-kontor-tillegget for Excel. Hvis du vil åpne enhetsdata, kan du starte fra Microsoft Excel eller Microsoft Dynamics 365 for operasjoner."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Bruke Excel-tillegg

Dette emnet forklarer hvordan du kan åpne enhetsdata i Microsoft Excel, og deretter vise, oppdatere og redigere dataene ved hjelp av Microsoft Dynamics-kontor-tillegget for Excel. Hvis du vil åpne enhetsdata, kan du starte fra Microsoft Excel eller Microsoft Dynamics 365 for operasjoner.

Ved å åpne enhetsdata i Microsoft Excel, kan du raskt og enkelt vise og redigere dataene ved hjelp av tillegget Microsoft Dynamics-kontor for Excel. Dette tillegget krever Microsoft Excel 2016. **Merk:** Hvis Microsoft Azure Active Directory (AD Azure)-leier er konfigurert til å bruke Active Directory Federation Services (AD FS), må du kontrollere at mai 2016-oppdateringen er installert, slik at Excel-tillegg kan riktig logge deg på.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Åpne enhetsdata i Excel når du starter fra Dynamics 365 for operasjoner
1.  Klikk på en side i Microsoft Dynamics 365 for operasjoner, **åpnet i Microsoft Office**. Hvis datakilden for rot (tabell) for siden er den samme som primære datakilden for alle enheter, standard **åpne i Excel** alternativer er generert for siden. **Åpne i Excel** alternativer finnes på ofte brukte sider, som **alle leverandører** og **alle kunder**.
2.  Klikk en **åpne i Excel** alternativ, og åpne arbeidsboken som er generert. Denne arbeidsboken har bindingsinformasjonen for enheten, en peker til ditt miljø og en peker til Excel-tillegget.
3.  I Excel velger du **aktivere redigering** å aktivere tillegget Excel til å kjøre. Excel-tillegg som kjøres i en rute på høyre side i Excel-vinduet.
4.  Hvis du kjører Excel-tillegget for første gang, klikker du **stoler på dette tillegget**.
5.  Hvis du blir bedt om å logge på, klikker du **logge på**, og deretter logge på ved å bruke samme legitimasjon som du brukte til å logge deg inn i Dynamics 365 for operasjoner. Tilleggsprogrammet Excel bruker en tidligere pålogging kontekst fra Internet Explorer, og automatisk logge deg på, hvis det er mulig. Derfor må du kontrollere brukernavnet i øvre høyre hjørne av Excel-tillegget.

Excel-tillegg automatisk du leser data for entiteten du valgte. Legg merke til at det vises ingen data i arbeidsboken helt til står det i Excel-tillegget.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Åpne enhetsdata i Excel når du starter fra Excel
1.  I Excel, på den **Sett inn** kategorien i den **tillegg** gruppen, klikker du **Store** til å åpne Office-butikken.
2.  I Office-butikk, kan du søke etter nøkkelordet "Dynamics", og klikk **Legg til** siden den **Add-in for Microsoft Dynamics-kontor** (i tillegg).
3.  Hvis du kjører Excel-tillegget for første gang, klikker du **stoler på dette tillegget** å aktivere tillegget Excel til å kjøre. Excel-tillegg som kjøres i en rute på høyre side i Excel-vinduet.
4.  Klikk **legge til informasjon om server** til å åpne den **alternativer** ruten.
5.  Kopier URL-adressen for Web-leseren fra mål-Dynamics 365 for forekomsten av operasjoner, lime den inn i den **URL-adressen** -feltet, og deretter slette alt etter vertsnavnet (for eksempel slette **/? cmp = usmf & mi = CustTableListPage**). Den resulterende URL-adressen må bare vertsnavnet (for eksempel **https://xxx.dynamics.com**).
6.  Klikk **OK**, og klikk deretter **Ja** å bekrefte endringen. Excel-omstarter og laster inn metadata. Den **Design** er nå tilgjengelig. Hvis tilleggsprogrammet Excel har en **laste appleter** -knappen, du sannsynligvis ikke er logget på som bruker riktig. Hvis du vil ha mer informasjon, se "knappen Last inn appleter vises" i delen "Feilsøking" i dette emnet.
7.  Klikk **Design**. Excel-tillegget henter metadata for enhet.
8.  Klikk **Legg til tabell**. Det vises en liste over enheter. Enhetene som er oppført i "navn –" Etikettformat.
9.  Velg en enhet i listen, for eksempel **kunde - kunder**, og klikk deretter **neste**.
10. Å legge til et felt fra den **tilgjengelige felt** viser til den **valgte felt**, klikker du i feltet, og deretter klikker **Legg til**. Eventuelt kan du dobbeltklikke feltet.
11. Etter at du har lagt til de aktuelle feltene i den **valgte felt**, pass på at markøren er på riktig sted i regnearket (for eksempel celle A1), og klikker deretter **gjort**. Deretter **gjort** å avslutte utformingsverktøyet.
12. Klikk **Oppdater** å trekke inn et sett med data.

## <a name="view-and-update-entity-data-in-excel"></a>Vis og Oppdater entity data i Excel
Når du leser entity data i arbeidsboken for Excel-tillegg, kan du oppdatere dataene når som helst ved å klikke **Oppdater** i Excel-tillegget.

## <a name="edit-entity-data-in-excel"></a>Rediger entity data i Excel
Du kan endre enhetsdata som du trenger, og deretter publisere den tilbake ved å klikke **Publiser** i Excel-tillegget. Hvis du vil redigere en post, Merk en celle i regnearket, og endre deretter celleverdien. Hvis du vil legge til en ny post, gjør du ett av følgende:

-   Klikk hvor som helst i regnearket, og klikk deretter **ny** i Excel-tillegget.
-   Klikk i den siste raden i regnearket, og trykk deretter Tab-tasten til markøren flyttes ut av den siste kolonnen i denne raden, og det opprettes en ny rad.
-   Klikk i raden like under regnearket, og begynner å skrive inn data i en celle. Når du flytter fokus fra cellen, utvides regnearket for å ta med den nye raden.

Hvis du vil slette en post, gjør du ett av følgende:

-   Høyreklikk radnummeret ved siden av raden regneark hvis du vil slette, og klikk deretter **sletter**.
-   Høyreklikk raden regneark til å slette, og klikk deretter **sletter**&gt;**tabellrader**.

## <a name="add-or-remove-columns"></a>Legg til eller fjern kolonner
Du kan bruke designer til å justere kolonnene som automatisk legges til i regnearket.

1.  Start data source utformeren av Excel-tillegget ved å klikke på **alternativer** knappen (Tannhjul symbol), og deretter velge den **aktivere design** merket.
2.  Klikk **Design** i Excel-tillegget. Alle datakilder er oppført.
3.  Ved siden av datakilden, klikker du **Rediger** knappen (blyantsymbolet).
4.  Justere listen i den **valgt feltene** liste du trenger:
    -   Å legge til et felt fra den **tilgjengelige felt** viser til den **valgte felt**, klikker du i feltet, og deretter klikker **Legg til**. Eventuelt kan du dobbeltklikke feltet.
    -   Fjerne et felt fra den **valgt feltene**, klikker du i feltet, og klikker deretter **fjerne**. Eventuelt kan du dobbeltklikke feltet.
    -   Hvis du vil endre rekkefølgen på feltene, klikker du feltet i den **valgt feltene**, og klikk deretter **opp** eller **ned**.

5.  Ta i bruk endringene til datakilden ved å klikke **oppdatering**. Deretter **gjort** å avslutte utformingsverktøyet. Hvis du har lagt til et felt (kolonne), klikker du **Oppdater** å trekke inn en oppdatert sett med data.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Det er noen problemer som kan løses gjennom noen enkle trinn.

-   **Knappen Last inn appleter vises.** Hvis tilleggsprogrammet Excel har en **laste appleter** knappen etter innlogging, du sannsynligvis ikke er logget på som bruker riktig. Hvis du vil løse dette problemet, kontrollerer du at riktig brukernavn vises i øvre høyre hjørne av Excel-tillegget. Hvis en feil brukernavn vises, klikker du den, logge av og logge deg inn igjen.
-   **Du får feilmeldingen "Forbudt".** Hvis du får feilmeldingen "Forbudt" mens Excel-tillegg lastes metadata, har kontoen som er logget Excel-tillegget ikke tillatelse til å bruke målrettede service, forekomsten eller databasen. Hvis du vil løse dette problemet, kontrollerer du at riktig brukernavn vises i øvre høyre hjørne av Excel-tillegget. Hvis en feil brukernavn vises, klikker du den, logge av og logge deg inn igjen.
-   **En tom webside vises over Excel.** Hvis det åpnes en tom webside i løpet av prosessen, AD FS krever at kontoen, men versjonen av Excel som kjører tillegget er ikke nylig å laste inn logg på dialogboksen. Hvis du vil løse dette problemet, kan du oppdatere versjonen av Excel du bruker. Hvis du vil oppdatere versjonen av Excel når du er i en virksomhet som er på den utsatte kanalen, kan du bruke den [verktøy for distribusjon av Office](https://technet.microsoft.com/library/jj219422.aspx) til [flytte fra utsatte kanalen til den gjeldende kanalen](https://technet.microsoft.com/library/mt455210.aspx).



