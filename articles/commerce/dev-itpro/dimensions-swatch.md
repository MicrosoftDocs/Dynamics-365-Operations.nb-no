---
title: Konfigurere produktdimensjonsverdier som skal vises som prøver
description: Dette emnet beskriver hvordan du konfigurerer produktdimensjonsverdier som prøver på Microsoft Dynamics 365 Commerce-hovedkontoret.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 4ffbb6a162e87fd19cdb44224adc8c223ba8e903
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638300"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Konfigurere produktdimensjonsverdier som skal vises som prøver

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer produktdimensjonsverdier som prøver på Microsoft Dynamics 365 Commerce-hovedkontoret. Hvis du vil ha mer informasjon om produktdimensjoner, kan du se [Produktdimensjoner](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce støtter bruken av størrelse, stil og fargedimensjoner som skal representere produktvarianter. Produktdimensjoner har brukervennlige navn som vises på produktdetaljersider (PDPer), slik at produktvarianter kan velges. Eksempler på disse brukervennlige navnene er Liten, Medium og Stor for størrelser, og Svart og Brun for farger. Hvis et produkt støtter mange variasjoner, kreves det imidlertid flere valg for å vise bildet for hver produktvariant. Derfor kan det være tregt og langtekkelig for kunder å bla gjennom og velge produktvarianter.

Når dimensjoner vises som prøver i PDPer, får kundene en visuell forhåndsvisning av produktvariasjonene. De kan enkelt bla gjennom et stort utvalg av farger, mønstre og variasjoner, og de kan raskt vise forskjellige kombinasjoner av produktvariasjoner.

Funksjonen for visning av dimensjoner som prøver gjør det mulig for Commerce å bruke heksadesimalkoder og -bilder til å vise dimensjoner som prøver. I tillegg kan lignende dimensjoner, for eksempel farger, grupperes på produktlistesider. En kunde søker for eksempel etter produkter som er blå. Hvis de ulike blå dimensjonsverdiene er gruppert sammen, viser søkeresultatlistesiden produkter som har ulike blåtoner. Dimensjonsgruppering forbedrer produktfinanseringserfaringen betraktelig, og hjelper kunder med å finne flere produkter via en enkelt produktsøkespørring.

> [!NOTE]
> Funksjonen for vis dimensjoner som prøver er tilgjengelig fra Dynamics 365 Commerce-versjon 10.0.20-utgivelsen.

Illustrasjonen nedenfor viser et eksempel der farger vises som prøver på en Commerce PDP.

![Eksempel på farger som vises som prøver på en produktdetaljside.](../dev-itpro/media/swatch_pdp.png)

Illustrasjonen nedenfor viser et eksempel der farger vises som prøver på en Commerce-søkeresultatlisteside.

![Eksempel på farger som vises som prøver på en søkeresultatlisteside.](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Aktivere visningsdimensjonene som prøvefunksjon i Commerce Headquarters

Hvis du vil aktivere visningsdimensjonene som prøvefunksjonen i Commerce headquarters, kan du gå til **Arbeidsområder \> Funksjonsbehandling**, og slå på funksjonen **Aktiver bildestøtte for produktdimensjonsverdier** . Når dette funksjonsflagget er aktivert, legges det til tre nye felt for hver dimensjon i de aktuelle tabellene i Commerce Headquarters: **Heksakode**, **URL** (for bilder) og **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Konfigurere dimensjonsverdier i Commerce Headquarters

Visningsdimensjonene som prøvefunksjonen støttes for størrelses-, stil- og fargedimensjoner. Verdiene for heksakode og bilde-URL for de aktuelle dimensjonene kan angis i Commerce Headquarters. Hvis heksakode og bilde-URL-verdier ikke er angitt for en dimensjon, vil systemet som standard vise teksten til dimensjonens brukervennlige navn.

Konfigurasjonen kan utføres på et hvilket som helst av følgende nivåer:

- **Dimensjon** – I Commerce Headquarters åpner du siden for en dimensjon ved å søke etter **Farge**, **Størrelse** eller **Stil**. På hver side viser et rutenett dimensjonsverdiene. Du kan styre verdiene for visningsrekkefølge, heksakode og bilde-URL. Illustrasjonen nedenfor viser en eksempelkonfigurasjon på siden **Farger**.

    ![Eksempel på dimensjonskonfigurasjon på Farger-siden.](../dev-itpro/media/swatch_Color.PNG)

- **Dimensjonsgruppe**– I Dynamics 365 Commerce kan du bruke **RefinerGroup**-egenskapen til å opprette dimensjonsgrupper. Hvis dimensjonsgrupper er definert, åpner du den gjeldende siden ved å søke etter **Fargegruppe**, **Størrelsesgruppe** eller **Stilgruppe**. På hver side kan du styre verdier for heksakode, bilde-URL og presiseringsgruppe. Illustrasjonen nedenfor viser en eksempelkonfigurasjon på siden **Fargegrupper**.

    ![Eksempel på dimensjonskonfigurasjon på Fargegrupper-siden.](../dev-itpro/media/swatch_colorGroup.PNG)

- **Produktdimensjon (under produktoppretting)** – Når du oppretter et nytt produkt, kan du bruke siden **Produktdimensjoner** for å angi dimensjonsverdiene. For eksisterende produkter kan feltene for **Heksakode**, **URL** (for bilder) og **RefinerGroup** allerede være angitt. Du kan imidlertid endre verdier etter behov. Illustrasjonen nedenfor viser en eksempelkonfigurasjon på siden **Produktdimensjoner**.

    ![Eksempel på dimensjonskonfigurasjon på Produktdimensjoner-siden.](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Prosessen med å administrere konfigurasjoner av heksakode og bilde-URL følger det samme mønsteret som brukes til å styre visningsrekkefølgen til dimensjoner.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Konfigurere dimensjonsverdier ved hjelp av heksakoder

For de fleste fargedimensjoner bør du angi en heksakodefargeverdi på dimensjonssider i Commerce Headquarters. Den sorte fargen bør for eksempel ha en heksakodeverdi på **#00000**. Når Commerce gjengir en områdeside, representeres heksakoden av en farget prøve.

Illustrasjonen nedenfor viser et eksempel der fargedimensjoner konfigureres ved hjelp av heksakodeverdier.

![Eksempel på dimensjonskonfigurasjon som bruker heksakoder.](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Konfigurere dimensjonsverdier ved hjelp av bilde-URLer

Noen fargedimensjoner representerer mønstre, ikke fargefarger. En fargedimensjon kan for eksempel beskrives som "leopard". I slike tilfeller kan du mer effektivt representere fargedimensjonene ved å bruke publiserte bilder i stedet for heksakoder for prøver.

Du må laste opp hvert bilde til Commerce-områdebyggeren og publisere det. Deretter angir du bilde-URL-adressen for det publiserte bildet på de aktuelle dimensjonssidene i Commerce Headquarters. Hvis en dimensjon er valgt for visning som en prøve, men en heksakode ikke er definert, vil Commerce gjøre et bildeoppslag når den gjengir siden. Hvis bildeoppslaget mislykkes, vil Commerce vise teksten for dimensjonens brukervennlige navn.

Illustrasjonen nedenfor viser et eksempel der bilde-URLene brukes for konfigurasjonen på siden **Farger**.

![Eksempel på dimensjonskonfigurasjon som bruker bilde-URLer.](../dev-itpro/media/swatch_color_urls.PNG)

Du kan bruke en mediemal til å definere bilde-URLer, på samme som for produkt- og kategoribilder. Når du laster opp bilder til områdebygger, må filnavnkonvensjoner og filbaner være konsekvente.

Illustrasjonen nedenfor viser et eksempel der bilde-URLene brukes for konfigurasjonen av en mediemal.

![Eksempel på konfigurasjon av mediemal.](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Konfigurere dimensjonsverdier ved hjelp av både heksakoder og bilde-URLer

For de fleste fargedimensjoner kan du konfigurere både heksakoder og bilde-URLer. Tilbakefallslogikk for Commerce-gjengivelse vil automatisk se etter enten en heksakode eller en bilde-URL for å vise en fargeprøve. Ved å bruke både heksakoder og bilde-URL-adresser til å konfigurere fargedimensjoner kan du forenkle bildebehandling når antall farger er stort.

Illustrasjonen nedenfor viser et eksempel der både heksakoder og bilde-URLene brukes for konfigurasjonen på siden **Farger**.

![Eksempel på dimensjonskonfigurasjon som bruker både heksakoder og bilde-URLer.](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Konfigurere presiseringsgrupper

Når du definerer en heksakode eller bilde-URL for en dimensjonsverdi, kan du også angi en verdi for **RefinerGroup**-feltet. Dette feltet definerer dimensjonen som skal brukes til å gruppere lignende dimensjonsverdier i presiseringserfaringen.

Hvis for eksempel fargedimensjonsverdiene er "blå", "blårutete", "blåvask" og "mørkeblå", tilordnes hver verdi til ulike heksakoder eller bilde-URLer. Derfor vises hver verdi som forskjellige farger på PDPene og produktkortene for de aktuelle produktene. Hvis du tilordner alle fargedimensjonsverdiene til en **RefinerGroup**-verdi for **Blå**, genererer imidlertid et søk etter "blå" produkter søkeresultater for produkter som har dimensjonsfargeverdiene "blått", "blårutete", "blåvask" og "mørkeblå".

Eksemplet i illustrasjonen nedenfor viser forholdet mellom egenskapene **Farge** og **RefinerGroup** i Commerce Headquarters.

![Eksempel på behandling av presiseringsgruppe.](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Behandle bilder i Commerce-områdebygger

Hvis det brukes bilde-URL-adresser for dimensjonsverdier, må de tilsvarende bildene lastes opp til Commerce-områdebyggeren. Plasseringen til hvert bilde må samsvare med filnavnet og mappebanen som er definert for bildet i Commerce Headquarters. Bildefiler må lastes opp til de riktige kategoriplasseringene i områdekonfiguratoren. Fargebilder må for eksempel lastes opp til **Farge**-kategorimappen. Hvis du vil ha mer informasjon om hvordan du laster opp bilder til områdebyggeren, kan du se [Laste opp bilder](../dam-upload-images.md).

Illustrasjonen nedenfor viser et eksempel der dialogboksen **Opplastingsfiler** brukes til å laste opp bilder til mediabiblioteket for områdekonfiguratoren. Den uthever kategoriene **Størrelse**, **Farge** og **Stil** som er tilgjengelige for valg.

![Eksempel på bildefilkategorier under opplasting til mediebibliotek for områdekonfigurator.](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Aktivere prøvevisning e-handelsområdesider

Før prøver kan vises på e-handelsområdesider som krever dimensjonsvalg, for eksempel PDPer og listesider, må du konfigurere innstillingene for dimensjonsområde i Commerce Headquarters. Hvis du vil ha mer informasjon, kan du se [Bruke områdeinnstillinger for dimensjoner](../dimension-settings.md).

I tillegg bør du aktivere egenskapen **Inkluder produktattributter i søkeresultater** for søkeresultatmoduler. Hvis området bruker tilpassede kategorisider, bør du oppdatere søkeresultatmodulene som brukes på disse sidene, slik at egenskapen **Inkluder produktattributter i søkeresultater** er aktivert. Hvis du vil ha mer informasjon, se [Modul for søkeresultater](../search-result-module.md).

## <a name="display-swatches-in-pos-and-other-channels"></a>Vise prøver i POS og andre kanaler

Commerce har for øyeblikket ikke en standardimplementering som støtter visningen av prøver på salgsstedet og andre kanaler. Du kan imidlertid implementere prøvevisningsfunksjonaliteten som en utvidelse som gjør at kanal-APIer returnerer heksakoder og bilde-URLer som kreves for å gjengi prøver.

## <a name="additional-resources"></a>Tilleggsressurser

[Modul for søkeresultater](../search-result-module.md)

[Bruke områdeinnstillinger for dimensjoner](../dimension-settings.md)

[Produktdimensjoner](../../supply-chain/pim/product-dimensions.md)

[Last opp bilde](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
