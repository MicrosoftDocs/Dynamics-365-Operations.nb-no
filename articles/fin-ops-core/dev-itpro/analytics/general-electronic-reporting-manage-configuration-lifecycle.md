---
title: Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)
description: Dette emnet beskriver hvordan du administrerer livssyklusen til ER-konfigurasjoner (elektronisk rapportering) for Dynamics 365 Finance.
author: NickSelin
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b8b61082cf17707c952b6e07613769a671c349bb8fa92c21e3fe8524ef62dcb2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767785"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du administrerer livssyklusen til ER-konfigurasjoner (elektronisk rapportering) for Dynamics 365 Finance.

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

    - Endre en dokumentmal som ble opprettet til en ER-konfigurasjon, og eksporter konfigurasjonen fra den gjeldende programforekomsten som en XML-pakke som kan lagres lokalt eller i Lifecycle Services (LCS).
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

ER-konfigurasjoner som er utformet i utviklingsmiljøet, kan [lastes opp](#data-persistence-consideration) til testmiljøet for konfigurasjonsevalueringen (riktig prosessintegrering, riktige resultater, ytelse) og kvalitetssikring (riktige tilgangsrettigheter drevet av rolle, arbeidsdeling osv.). Funksjoner som gjør at utveksling av ER-konfigurasjoner kan brukes til dette formålet. Kontrollerte ER-konfigurasjoner kan lastes opp til LCS for å dele dem med tjenesteabonnenter, eller de kan [importeres](#data-persistence-consideration) til produksjonsmiljøet for intern bruk.

![Livssyklus for ER-konfigurasjon.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Hensyn angående dataholdbarhet

Du kan individuelt [importere](tasks/er-import-configuration-lifecycle-services.md) forskjellige [versjoner](general-electronic-reporting.md#component-versioning) av en [ER-konfigurasjon](general-electronic-reporting.md#Configuration) til Finance-forekomsten din. Når en ny versjon av en ER-konfigurasjon importeres, kontrollerer systemet innholdet i utkastversjonen til denne konfigurasjonen:

- Når den importerte versjonen er lavere enn den høyeste versjonen av denne konfigurasjonen i gjeldende Finance-forekomst, forblir innholdet i utkastversjonen til denne konfigurasjonen uendret.
- Når den importerte versjonen er høyere enn noen annen versjon av denne konfigurasjonen i gjeldende Finance-forekomst, kopieres innholdet i den importerte versjonen til utkastversjonen av denne konfigurasjonen, slik at du kan fortsette å redigere den siste fullførte versjonen.

Hvis denne konfigurasjonen eies av [konfigurasjonsleverandøren](general-electronic-reporting.md#Provider) som for øyeblikke er aktivert, vises utkastversjonen av denne konfigurasjonen for deg på **Versjoner**-hurtigfanen på **Konfigurasjoner**-siden (**Organisasjonsadministrasjon** > **Elektronisk rapportering** > **Konfigurasjoner**). Du kan velge utkastversjonen av konfigurasjonen og [endre](er-quick-start2-customize-report.md#ConfigureDerivedFormat) innholdet ved å bruke den relevante ER-utformingen. Når du har redigert utkastversjonen til en ER-konfigurasjon, er innholdet ikke lenger i samsvar med innholdet i den høyeste versjonen av denne konfigurasjonen i gjeldende Finance-forekomst. For å unngå at endringene dine går tapt, viser systemet en feil om at importen ikke kan fortsette, fordi versjonen av denne konfigurasjonen er høyere enn den høyeste versjonen av denne konfigurasjonen i gjeldende Finance-forekomst. Når dette skjer, for eksempel med formatkonfigurasjon **X**, vises feilen **Formatering av "X"-versjonen er ikke fullført**.

Hvis du vil angre endringene du innførte i utkastversjonen, velger du den høyeste fullførte eller delte versjonen av ER-konfigurasjonen i Finance på **Versjoner**-hurtigfanen og velger deretter **Hent denne versjonen**. Innholdet i den valgte versjonen kopieres til utkastversjonen.

## <a name="applicability-consideration"></a>Relevanshensyn

Når du utformer en ny versjon av en ER-konfigurasjon, kan du definere [avhengigheten](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) til andre programvarekomponenter. Dermed regnes som en forutsetning for å kontrollere nedlastingen av denne konfigurasjonen versjon fra et ER-repositorium eller en ekstern XML-fil og ytterligere bruk av denne versjonen. Når du prøver å importere en ny versjon av en ER-konfigurasjon, bruker systemet de konfigurerte forutsetningene til å styre om versjonen kan importeres.

Noen ganger kan du kreve at systemet ignorerer de konfigurerte forutsetningene når du importerer nye versjoner av ER-konfigurasjoner. Følg denne fremgangsmåten hvis du vil at systemet skal ignorere forutsetningene under import.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i handlingsruten i fanen **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.
3. Sett alternativet **Hopp over produktoppdateringer og versjonsforskuddskontroll under import** til **Ja**.

    > [!NOTE]
    > Denne parameteren er brukerspesifikk og selskapsspesifikk.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Definere avhengigheten av ER-konfigurasjonene i andre komponenter](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
