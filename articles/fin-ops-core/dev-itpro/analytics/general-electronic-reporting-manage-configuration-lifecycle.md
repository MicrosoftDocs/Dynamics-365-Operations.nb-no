---
title: Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)
description: Denne artikkelen beskriver hvordan du administrerer livssyklusen til ER-konfigurasjoner (elektronisk rapportering) for Dynamics 365 Finance.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337199"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du administrerer livssyklusen til [ER-[konfigurasjoner](general-electronic-reporting.md#Configuration) (elektronisk rapportering)](general-electronic-reporting.md) for Dynamics 365 Finance.

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

Du kan individuelt [importere](tasks/er-import-configuration-lifecycle-services.md) forskjellige versjoner av en ER-[konfigurasjon](general-electronic-reporting.md#Configuration) til Finance-forekomsten din. Når en ny versjon av en ER-konfigurasjon importeres, kontrollerer systemet innholdet i utkastversjonen til denne konfigurasjonen:

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

## <a name="dependencies-on-other-components"></a>Avhengigheter for andre komponenter

ER-konfigurasjoner kan konfigureres som [avhengige](er-download-configurations-global-repo.md#import-filtered-configurations) av andre konfigurasjoner. Du kan for eksempel [importere](er-download-configurations-global-repo.md) en ER-[datamodellkonfigurasjon](er-overview-components.md#data-model-component) fra det globale repositoriet til [Microsoft Regulatory Configuration Services (RCS)](../../../finance/localizations/rcs-overview.md) eller Dynamics 365 Finance-forekomsten, og deretter opprette en ny ER-[formatkonfigurasjon](er-overview-components.md#format-component) som er [avledet](er-quick-start2-customize-report.md#DeriveProvidedFormat) fra den importerte ER-datamodellkonfigurasjonen. Konfigurasjonen til det avledede ER-formatet vil være avhengig av basis-ER-datamodellkonfigurasjonen.

![Avledet ER-formatkonfigurasjon på konfigurasjonssiden.](./media/ger-configuration-lifecycle-img1.png)

Når du er ferdig med å utforme formatet, kan du endre statusen for den opprinnelige versjonen av ER-formatkonfigurasjonen fra **Utkast** til **Fullført**. Deretter kan du dele den fullførte versjonen av ER-formatkonfigurasjonen ved å [publisere](../../../finance/localizations/rcs-global-repo-upload.md) den i det globale repositoriet. Deretter får du tilgang til det globale repositoriet fra en hvilken som helst RCS- eller Finance-skyforekomst. Du kan deretter importere alle ER-konfigurasjonsversjoner som gjelder programmet, fra det globale repositoriet til programmet.

![Publiserte ER-formatkonfigurasjon på Konfigurasjonsrepositorium-siden.](./media/ger-configuration-lifecycle-img2.png)

Basert på konfigurasjonsavhengigheten når du velger ER-formatkonfigurasjonen i det globale repositoriet for å importere den til en nydistribuert RCS- eller Finans-forekomst, blir base-ER-datamodellkonfigurasjonen automatisk funnet i det globale repositoriet og importeres sammen med den valgte ER-formatkonfigurasjonen som basiskonfigurasjon.

Du kan også eksportere ER-formatkonfigurasjonsversjonen ut av nåværende RCS- eller Finance-forekomst, og lagre den lokalt som en XML-fil.

![Eksport av en ER-formatkonfigurasjonversjon som XML på Konfigurasjoner-siden.](./media/ger-configuration-lifecycle-img3.png)

I versjoner av Finance **før versjon 10.0.29**, når du prøver å importere ER-formatkonfigurasjonsversjonen fra denne XML-filen eller fra et hvilket som helst annet repositorium enn det globale repositoriet til et nydistribuert RCS- eller Finance-forekomst som ennå ikke inneholder noen ER-konfigurasjoner, vil det følgende unntaket gjøres oppmerksom på å informere deg om at det ikke kan anskaffes en basiskonfigurasjon:

> Uløste referanser igjen<br>
Referanse for objektet \<imported configuration name\> til objektet Base (\<globally unique identifier of the missed base configuration\>, \<version of the missed base configuration\>) kan ikke opprettes

![Importere ER-formatkonfigurasjonsversjonen på Konfigurasjonsrepositorium-siden.](./media/ger-configuration-lifecycle-img4.gif)

I **versjon 10.0.29 og senere**, når du prøver å bruke den samme konfigurasjonsimporten, vil ER-rammeverket automatisk prøve å finne navnet på den manglende basiskonfigurasjonen i den globale repositoriet i hurtigbufferen for global repositorium. Deretter vil det vises navnet og den globalt unike identifikatoren (GUID) for den manglende basiskonfigurasjonen i teksten for unntaket som mangler.

> Uløste referanser igjen<br>
Referanse for objektet \<imported configuration name\> til objektet Base (\<name of the missed base configuration\> \<globally unique identifier of the missed base configuration\>, \<version of the missed base configuration\>) kan ikke opprettes

![Unntak på Konfigurasjonsrepositorium-siden når basiskonfigurasjonen ikke blir funnet.](./media/ger-configuration-lifecycle-img5.png)

Du kan bruke det angitte navnet til å finne basiskonfigurasjonen og deretter importere den manuelt.

> [!NOTE]
> Dette nye alternativet fungerer bare når minst én bruker allerede har logget seg på det globale repositoriet ved å bruke siden [Konfigurasjonsrepositorier](er-download-configurations-global-repo.md#open-configurations-repository) eller et av de globale [repositoriumsoppslagsfeltene](er-extended-format-lookup.md) i den gjeldende Finance-forekomsten, og når det globale repositoriumsinnholdet er hurtigbufret.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Definere avhengigheten av ER-konfigurasjonene i andre komponenter](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

