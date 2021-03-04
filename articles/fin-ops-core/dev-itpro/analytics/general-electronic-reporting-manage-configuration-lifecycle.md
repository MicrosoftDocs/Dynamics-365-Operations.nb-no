---
title: Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)
description: Dette emnet beskriver hvordan du administrerer livssyklusen til ER-konfigurasjoner (elektronisk rapportering) for Microsoft Dynamics 365 Finance-løsningen.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a4741784103817c270c4c7f730753ba59a327d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682629"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du administrerer livssyklusen til ER-konfigurasjoner (elektronisk rapportering) for Microsoft Dynamics 365 Finance.

## <a name="overview"></a>Oversikt

Elektronisk rapportering (ER) er en motor som støtter lovbestemte obligatoriske og landsspesifikke elektroniske dokumenter. Vanligvis forutsetter ER en mulighet til å utføre følgende oppgaver for ett enkelt dokument elektronisk. Hvis du vil ha mer informasjon, se [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md).

- Utforme en mal for et elektronisk dokument:

    - Identifiser de påkrevde datakildene som kan presenteres i dokumentet:

        - Underliggende data, for eksempel datatabeller, dataenheter og klasser.
        - Prosess-spesifikke egenskaper, for eksempel dato og klokkeslett for kjøring og tidssone.
        - Inndataparametre for brukere, angitt av sluttbrukeren under kjøring.

    - Definer de nødvendige dokumentetelementene og deres topologi for å angi et endelig dokumentformat.
    - Konfigurer den ønskede flyten av data fra valgte datakilder til definerte dokumentelementer (via datakildebindinger til dokumentets formatkomponenter) og angi kontrollogikk for prosessen.

- Gjør en mal tilgjengelig slik at den kan brukes i andre forekomster:

    - Endre en dokumentmal som ble opprettet til en ER-konfigurasjon, og eksporter konfigurasjonen fra den gjeldende programforekomsten som en XML-pakke som kan lagres lokalt eller i LCS.
    - Gjør om en ER-konfigurasjon til en dokumentmal for program.
    - Importer en XML-pakke som er lagret lokalt eller i LCS, i den gjeldende forekomsten.

- Tilpass malen for et elektronisk dokument:

    - Inkluder en mal fra LCS i den gjeldende forekomsten som en ER-konfigurasjon.
    - Utform en tilpasset versjon av ER-konfigurasjonen og behold en referanse til den grunnleggende versjonen.

- Integrer en mal med en bestemt forretningsprosess, slik at den er tilgjengelig i programmet:

    - Konfigurer innstillinger slik at programmet starter å bruke en ER-konfigurasjon, ved å referere til denne konfigurasjonen i en parameter som er relatert til prosessen. For eksempel, se ER-konfigurasjonen i en bestemt leverandørbetalingsmetode for å generere en melding om elektronisk betaling for behandling av fakturaer.

- Bruk en mal i en bestemt forretningsprosess:

    - Kjør en ER-konfigurasjon i en spesifikk forretningsprosess. For eksempel for å generere en melding om elektronisk betaling for behandling av fakturaer når en betaløingsmetode som refererer til ER-konfigurasjonen, er valgt.

## <a name="concepts"></a>Begreper
Følgende roller og dedikerte aktiviteter er knyttet til livssyklusen for ER-konfigurasjonen.

| Rolle                                       | Aktiviteter                                                      | beskrivelse |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Funksjonell konsulent for elektronisk rapportering | Opprett og administrer ER-komponenter (modeller og formater).           | En forretningsperson som utformer ER-domenespesifikke datamodeller, utformer de nødvendige malene for elektroniske dokumenter, og binder dem i henhold til dette. |
| Utvikler av elektronisk rapportering             | Opprett og behandle datatilordninger for modellen.                          | En spesialist som velger de nødvendige Finance-datakildene og binder dem til ER-domenespesifikke datamodeller. |
| Regnskapsansvarlig                      | Konfigurer prosessrelaterte innstillinger som refererer til ER-artefakter. | For eksempel en **Regnskapsansvarlig**-rolle som tillater at innstillingene for en ER-konfigurasjon kan brukes i en bestemt leverandørbetalingsmåte for å generere en melding om elektronisk betaling for behandling av fakturaer. |
| Leverandørbetalingsassistent            | Bruk ER-artefakter i en bestemt forretningsprosess.                | For eksempel en **Leverandørbetalingsassistent**-rolle som tillater at meldinger om elektronisk betaling kan genereres for behandling av fakturaer, basert på ER-formatet som er konfigurert for en bestemt betalingsmåte. |

## <a name="er-configuration-development-lifecycle"></a>Utviklinglivssyklus for ER-konfigurasjon
Av følgende ER-relaterte årsaker anbefaler vi at du utformer ER-konfigurasjoner i utviklingsmiljøet, som en separat forekomst av Finance and Operations:

- Brukere som har en av rollene **Utvikler av elektronisk rapportering** eller **Funksjonell konsulent for elektronisk rapportering**, kan redigere konfigurasjoner og kjøre dem for testformål. Dette scenariet kan føre til kall av metoder for klasser og tabeller som kan være farlige for forretningsdata og ytelse for forekomsten.
- Kall av metoder for klasser og tabeller som ER-datakilder for ER-konfigurasjoner er ikke begrenset av startpunkter og logget firmainnhold. Brukere som har rollene **Utvikler av elektronisk rapportering** eller **Funksjonell konsulent for elektronisk rapportering** kan få tilgang til forretningssensitive data.

ER-konfigurasjoner som er utformet i utviklingsmiljøet, kan lastes opp til testmiljøet for konfigurasjonsevalueringen (riktig prosessintegrering, riktige resultater, ytelse) og kvalitetssikring (riktige tilgangsrettigheter drevet av rolle, arbeidsdeling osv.). Funksjoner som gjør at utveksling av ER-konfigurasjoner kan brukes til dette formålet. Til slutt kan kontrollerte ER-konfigurasjoner lastes opp til LCS, der de kan deles med abonnenter eller til produksjonsmiljøet for intern bruk, som vist i illustrasjonen nedenfor.

![Livssyklus for ER-konfigurasjon](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]