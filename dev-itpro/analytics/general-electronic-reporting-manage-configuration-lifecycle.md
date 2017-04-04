---
title: Administrere livssyklus til konfigurasjoner for elektronisk rapportering
description: "Dette emnet beskriver hvordan du administrerer livssyklusen til elektronisk rapportering (ER)-konfigurasjoner for Microsoft Dynamics-365 for operasjoner løsning."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Administrere livssyklus til konfigurasjoner for elektronisk rapportering

Dette emnet beskriver hvordan du administrerer livssyklusen til elektronisk rapportering (ER)-konfigurasjoner for Microsoft Dynamics-365 for operasjoner løsning.

<a name="overview"></a>Oversikt
--------

Elektronisk rapportering (ER) er en motor som støtter lovbestemte obligatoriske og landsspesifikke elektroniske dokumenter i Microsoft Dynamics 365 for Operations. Vanligvis forutsetter ER en mulighet til å utføre følgende oppgaver for ett enkelt dokument elektronisk. Hvis du vil ha mer informasjon, se [elektronisk rapportering oversikt](general-electronic-reporting.md).

-   Utforme en mal for et elektronisk dokument:
    -   Identifiser de påkrevde datakildene som kan presenteres i dokumentet:
        -   Underliggende Dynamics 365 for operasjoner data, for eksempel datatabeller, data-enheter og -klasser.
        -   Prosess-spesifikke egenskaper, for eksempel kjøring av dato, klokkeslett og tidssone.
        -   Inndataparametere for brukere, angitt av brukeren under kjøring.
    -   Definer de nødvendige dokumentetelementene og deres topologi for å angi et endelig dokumentformat.
    -   Konfigurer den ønskede flyten av data fra valgte datakilder til definerte dokumentelementer (via datakildebindinger til dokumentets formatkomponenter) og angi kontrollogikk for prosessen.
-   Gjør en mal tilgjengelig slik at den kan brukes i andre forekomster av Dynamics 365 for Operations:
    -   Endre en dokumentmal som ble opprettet i Dynamics 365 for Operations til en ER-konfigurasjon, og eksporter konfigurasjonen fra den gjeldende Dynamics 365 for Operations-forekomsten som en XML-pakke som kan lagres lokalt eller i LCS.
    -   Gjør om en ER-konfigurasjon til en dokumentmal for Dynamics 365 for Operations.
    -   Importer en XML-pakke som er lagret lokalt eller i LCS, i den gjeldende forekomsten av Dynamics 365 for Operations.
-   Tilpass malen for et elektronisk dokument:
    -   Inkluder en mal fra LCS i den gjeldende forekomsten av Dynamics 365 for Operations som en ER-konfigurasjon.
    -   Utform en tilpasset versjon av ER-konfigurasjonen og behold en referanse til den grunnleggende versjonen.
-   Integrer en mal med en bestemt forretningsprosess, slik at den er tilgjengelig i Dynamics 365 for Operations:
    -   Konfigurer innstillinger slik at Dynamics 365 for Operations starter å bruke en ER-konfigurasjon, ved å referere til denne konfigurasjonen i en parameter som er relatert til prosessen. For eksempel referere til konfigurasjonen ER i en bestemt kontoer-leverandører betalingsmåte for å generere en melding om elektronisk betaling for behandling av fakturaer.
-   Bruk en mal i en bestemt forretningsprosess:
    -   Kjøre en konfigurasjon ER i en bestemt forretningsprosess. For eksempel er Hvis du vil generere en melding om elektronisk betaling for behandling av fakturaer når en betalingsmåte som refererer til ER konfigurasjonen valgt.

## <a name="concepts"></a>Begreper
Følgende roller og relaterte aktiviteter er tilknyttet ER konfigurasjonen livssyklus.

| Rolle                                       | Aktiviteter                                                      | beskrivelse                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funksjonell konsulent for elektronisk rapportering | Opprett og administrer ER-komponenter (modeller og formater).           | Business person som utvikler ER domene-spesifikke datamodeller, utforminger nødvendige malene for elektroniske dokumenter og binder dem i henhold til dette.                                                                           |
| Utvikler av elektronisk rapportering             | Opprett og behandle datatilordninger for modellen.                          | En Dynamics 365 for operasjoner spesialisten som velger den nødvendige Dynamics 365 for operasjoner datakilder og binder dem til datamodeller ER domene-spesifikke.                                                                 |
| Regnskapsansvarlig                      | Konfigurer prosessrelaterte innstillinger som refererer til ER-artefakter. | For eksempel en **regnskapsansvarlig** rolle som gjør at innstillingene for en Gjenopprettingsdiskett-konfigurasjon som skal brukes i en bestemt kontoer betalingsmåte for leverandører til å generere en melding om elektronisk betaling for behandling av fakturaer. |
| Leverandørbetalingsassistent            | Bruk ER-artefakter i en bestemt forretningsprosess.                | For eksempel en **Leverandørbetalingsassistent** rolle som gjør at meldinger elektronisk betaling som skal genereres for behandling av fakturaer, basert på ER formatet som er konfigurert for en bestemt betalingsmåte.           |

## <a name="er-configuration-development-lifecycle"></a>Utviklinglivssyklus for ER-konfigurasjon
Av følgende ER-relaterte årsaker anbefaler vi at du utformer ER-konfigurasjoner i utviklingsmiljøet, som en separat forekomst av Dynamics 365 for Operations:

-   Brukere som har en av rollene **Utvikler av elektronisk rapportering** eller **Funksjonell konsulent for elektronisk rapportering**, kan redigere konfigurasjoner og kjøre dem for testformål. Dette scenariet kan føre til kall av metoder for klasser og tabeller som kan være farlige for forretningsdata og ytelse for Dynamics 365 for Operations-forekomsten.
-   Kall av metoder for klasser og tabeller som ER-datakilder for ER-konfigurasjoner er ikke begrenset av Dynamics 365 for Operations-startpunkter og logget firmainnhold. Brukere som har rollene **Utvikler av elektronisk rapportering** eller **Funksjonell konsulent for elektronisk rapportering** kan få tilgang til forretningssensitive data.

ER konfigurasjoner som er utformet i utviklingsmiljøet kan lastes opp til testmiljø for evaluering av konfigurasjon (riktig integrering, at resultater og ytelse) og kvalitetssikring, for eksempel at drevet med role tilgangsrettigheter og arbeidsdeling. Funksjoner som muliggjør ER konfigurasjonen utveksling kan brukes til dette formålet. Til slutt kan anerkjente ER konfigurasjoner lastes opp til LCS, der de deles med abonnenter, eller til produksjonsmiljøet for intern bruk, som vist i illustrasjonen nedenfor. ![ER konfigurasjon livssyklus](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Se også
--------

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)


