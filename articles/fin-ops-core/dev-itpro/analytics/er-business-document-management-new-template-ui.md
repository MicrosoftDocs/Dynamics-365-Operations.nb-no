---
title: Brukergrensesnitt i Microsoft Office-stil i Forretningsdokumentbehandling (inneholder video)
description: Denne artikkelen forklarer hvordan du bruker det nye brukergrensesnittet i funksjonen for administrasjon av forretningsdokument i ER-rammeverket (elektronisk rapportering).
author: v-anamir
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 208cfc91f11d4893785538ce4874e85a5725e993
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109268"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Brukergrensesnitt i Microsoft Office-stil i Forretningsdokumentbehandling

[!include [banner](../includes/banner.md)]

Med forretningsdokumentadministrering kan forretningsbrukere redigere forretningsdokumentmaler ved å bruke en Microsoft Office 365-tjeneste eller den aktuelle Microsoft Office-skrivebordsapplikasjonen. Redigeringer kan inneholde utformingsendringer eller nye distribusjoner, eller brukere kan legge til plassholdere for å inkludere ytterligere data uten å måtte endre kildekoden. Hvis du vil ha mer informasjon om hvordan du arbeider med administrering av forretningsdokumenter, kan du se [Oversikt over administrering av forretningsdokumenter](er-business-document-management.md).

Det nye brukergrensesnittet (UI) er tydeligere og mer behagelig å bruke. Området **Forretningsdokument** viser bare malene som eies av den nåværende [aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md) [leverandøren](general-electronic-reporting.md#Provider), og som er plassert i den gjeldende forekomsten av Dynamics 365 Finance. I det forrige grensesnittet oppførte kategorien **Mal** alle malene som var tilgjengelige for alle leverandører. Den viste også alle malene som var opprettet og redigert av alle brukere som hadde samme rolle.

Du kan bruke knappen **Nytt dokument** i arbeidsområdet **Behandling av forretningsdokument** til å opprette og redigere en mal i en [ER (elektronisk rapportering)](general-electronic-reporting.md)-format[konfigurasjon](general-electronic-reporting.md#Configuration) som tilbys av en annen leverandør, og som er plassert i den gjeldende Finance-forekomsten, eller til å laste opp en ny mal fra en Excel-arbeidsbok. I versjon 10.0.25 og senere kan du også bruke knappen **Nytt dokument** til å opprette og redigere en mal i en ER-formatkonfigurasjon som er lagret i det [globale repositoriet](general-electronic-reporting.md#Repository).

I eksemplene i denne artikkelen er den aktive leverandøren Contoso, og du bruker den til å opprette en mal som er basert på en mal som leveres av Microsoft. Du kan også opprette en mal ved å laste opp din egen mal i Excel-format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Videoen om hvordan du [oppretter et nytt forretningsdokument ved å bruke Forretningsdokumentbehandling](https://youtu.be/gAIYl-mM_pw) (vist ovenfor) er inkludert i [spillelisten for økonomi og drift](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), som er tilgjengelig på YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gjøre det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering tilgjengelig

Hvis du vil begynne å bruke det nye dokumentbrukergrensesnittet i forretningsdokumentadministrering, må du aktivere **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i **Funksjonsadministrering**-arbeidsområdet.

Følg disse trinnene for å aktivere denne funksjonen for alle juridiske enheter.

1. I **Funksjonsadministrering**-arbeidsområdet, i **Alle**-fanen velger du **Office-lignende brukergrensesnittopplevelse for forretningsdokumentadministrering**-funksjonen i listen.
2. Velg **Aktiver nå** for å aktivere den valgte funksjonen.
3. Oppdater siden for å få tilgang til den nye funksjonen.

## <a name="add-or-activate-a-provider"></a>Legg til eller aktiver en konfigurasjonsleverandør

Hver mal i et forretningsdokument lagres i en ER-formatkonfigurasjon som er merket som eid av en bestemt konfigurasjonsleverandør. Når du oppretter en ny mal, opprettes det en ny ER-formatkonfigurasjon for å holde den. Derfor må en leverandør identifiseres for konfigurasjonen. Den aktive leverandøren av ER-rammeverket brukes til dette formålet. Hvis det ikke er noen leverandør i ER, kan du opprette en. Hvis det ikke finnes en *aktiv* leverandør, kan du aktivere en av de eksisterende leverandørene. Det åpnes en dialogboks for å legge til eller aktivere en leverandør når det er nødvendig, mens du begynner å legge til en ny mal.

### <a name="add-a-new-provider"></a>Legg til en ny leverandør

Følg denne fremgangsmåten i dialogboksen **Konfigurasjonsleverandør** for å opprette en ny leverandør:

1.  På fanen **Velg konfigurasjonsleverandør**, i **Navn**-feltet, angir du navnet på den nye leverandøren.
2.  Angi Internett-adressen (URL-adresssen) til den nye leverandøren i feltet **Internett-adresse**. 
3.  Velg **OK**.

    ![Opprett en ny leverandør i Behandling av forretningsdokument.](./media/bdm_create_provider.png)

Leverandøren som legges til, aktiveres automatisk.

### <a name="activate-a-provider"></a>Aktiver en leverandør

Følg denne fremgangsmåten i dialogboksen **Konfigurasjonsleverandør** for å aktivere en leverandør:

1.  På fanen **Velg konfigurasjonsleverandør**, i feltet **Konfigurasjonsleverandør**, velger du leverandøren.
2.  Velg **OK**.

    ![Aktiver en leverandør i Behandling av forretningsdokument.](./media/bdm_choose_provider.png)

Den valgte leverandøren aktiveres.

> [!NOTE]
> Hver forretningsdokumentbehandlingsmal er i en ER-formatkonfigurasjon som refererer til leverandøren som konfigurasjonsforfatter. Derfor er en aktiv leverandør nødvendig for hver mal.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Rediger en mal som eies av en annen leverandør

Dette eksemplet viser hvordan du bruker knappen **Nytt dokument** i arbeidsområdet **Behandling av forretningsdokument** til å opprette og redigere en mal i en ER-formatkonfigurasjon som tilbys av en annen leverandør, og som er plassert i den gjeldende Finance-forekomsten. I dette eksemplet er den aktive leverandøren Contoso, som bruker ER-formatkonfigurasjonen som leveres av Microsoft. Når du velger **Nytt dokument**, viser **Velg**-fanen på siden **Opprett en ny mal** alle malene til den gjeldende Finance-forekomsten som eies av den gjeldende leverandøren og andre leverandører. Velg en mal for å åpne den. Du kan deretter opprette en ny redigerbar kopi av malen. Den redigerte malen lagres i en ny ER-formatkonfigurasjon som genereres automatisk.

1. I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.

    ![Arbeidsområdet Administrasjon av forretningsdokument.](./media/BDM_overview_new_template1.png)

2. På siden **Opprett en ny mal**, på **Velg**-fanen velger du dokumentet som skal brukes som mal, og velger deretter **Opprett dokument**.

    ![Forretningsdokumenter-dialogboksen.](./media/BDM_overview_new_template2.png)

3. I den nye dialogboksen, i **Tittel**-feltet endrer du tittelen etter behov. Tittelteksten brukes til å navngi den nye ER-formatkonfigurasjonen som opprettes automatisk. Utkastversjonen av denne konfigurasjonen (**Kopi av FTI-kunderapport (GER)**) vil inneholde den redigerte malen og vil bli brukt til å kjøre dette ER-formatet for den gjeldende brukeren. Den opprinnelige malen fra den grunnleggende ER-formatkonfigurasjonen vil bli brukt til å kjøre dette ER-formatet for alle andre brukere.
4. I **Navn** -feltet endrer du navnet på den første revisjonen av den redigerbare malen som skal opprettes automatisk.
5. I **Kommentar**-feltet oppdater du merknadene for revisjonen av den redigerbare malen som opprettes automatisk.
6. Velg **OK** for å bekrefte starten på redigeringsprosessen.

    ![Dokumentopprettelse-dialogboksen.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Last opp en mal som bruker en eksisterende Excel-arbeidsbok

Dette eksemplet viser hvordan du bruker knappen **Nytt dokument** i arbeidsområdet **Behandling av forretningsdokument** til å opprette og redigere en mal i en ER-formatkonfigurasjon, basert på den tilgjengelige Excel-arbeidsboken. I dette eksemplet er den aktive leverandøren Contoso, og du bruker konfigurasjonene for [ER-datamodell](er-overview-components.md#data-model-component) og [ER-modelltilordning](er-overview-components.md#model-mapping-component) som er levert av Microsoft. Når du har valgt **Nytt dokument**, velger du kategorien **Opplasting** på siden **Opprett en ny mal**. Der kan du angi detaljene i en Excel-arbeidsbokopplasting. Når du har lastet opp Excel-arbeidsboken, blir den transformert til en forretningsdokumentmal som åpnes for redigering. Den redigerte malen blir lagret i en ny ER-formatkonfigurasjon som genereres automatisk.

Følg denne fremgangsmåten for å oppgi nødvendig informasjon før du laster opp en mal.

1. I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.
2. Gå til siden **Opprett en ny mal**, **Last opp**-fanen og deretter **Mal**-fanen, og velg **Bla gjennom** for å søke etter og velge Excel-filen du vil bruke som en mal. I **Mal**-delen er feltene **Tittel** og **Beskrivelse** fylt ut automatisk. De angir navnet på og beskrivelsen av den nye ER-formatkonfigurasjonen som opprettes automatisk. Du kan redigere disse feltene etter behov.
3. I **Dokumenttype**-delen i **Navn**-feltet angir du typen forretningsdokument. Denne verdien brukes til å søke i den riktige datakilden (det vil si ER-modellkonfigurasjonen).

    ![Kategorien Opplasting på siden Opprett en ny mal.](./media/BDM_overview_new_UI_import_21.jpg)

4. På **Datakilde**-fanen, på hurtigfanen **Filter**, velger du **Bruk filter**. I **Datakilde**-delen fylles **Navn**-feltet ut automatisk, men du kan også velge en verdi manuelt. Du kan bruke filteret til å søke etter riktig datakildenavn etter navn, beskrivelse, kode for land/område og forretningsdokumenttype.

    ![Kategorien Datakilde på siden Opprett en ny mal.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > **Filter**-hurtigfanen brukes til å søke i den riktige datakilden (det vil si ER-modellkonfigurasjonen). Du kan redigere alle filterfelt for å finne den mest relevante datakilden for dokumentet du laster opp.
    > 
    > Betingelsene på **Filter**-hurtigkategorien brukes som **ELLER**-betingelser.

5. Velg **Registrer automatisk** i **Tilordning**-fanen. **Rotdefinisjon**-feltet fylles ut automatisk, men du kan også velge en verdi manuelt. Denne fanen viser slutttilordningen for elementene fra malen og modellen.

    ![Kategorien Tilordning på siden Opprett en ny mal.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Tilordningen i **Malstruktur**-delen bruker hele samsvaret mellom etikettene eller beskrivelsene i datakilden på brukerens språk, og i cellenavnet i malen.

6. Velg **Opprett dokument** for å bekrefte at du vil opprette en mal og starte redigeringsprosessen.

Hvis du vil ha mer informasjon, kan du se [Oversikt over forretningsdokumentadministrering](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Last opp en mal fra det globale repositoriet

Dette eksemplet viser hvordan du bruker knappen **Nytt dokument** i arbeidsområdet **Behandling av forretningsdokument** til å opprette og redigere en mal i en ER-formatkonfigurasjon som tilbys av Microsoft , og som er plassert i det globale repositoriet. I dette eksemplet er den aktive leverandøren Contoso, som bruker ER-formatkonfigurasjonen som leveres av Microsoft. Når du har valgt **Nytt dokument**, viser kategorien **Importer fra globalt repositorium** på siden **Opprett en ny mal** alle forretningsdokumentmalene som er lagret i det globale repositoriet, men som mangler i den gjeldende Finance-forekomsten. Når du har valgt en mal, importeres den fra det globale repositoriet til den gjeldende Finance-forekomsten for å opprette en ny redigerbar kopi. Den redigerte malen lagres i en ny ER-formatkonfigurasjon som genereres automatisk.

1. I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.
2. På siden **Opprett en ny mal**, på fanen **Importer fra globalt repositorium** velger du dokumentet som skal brukes som mal, og velger deretter **Opprett dokument**.

    ![Fanen Importer fra globalt repositorium på siden Opprett en ny mal.](./media/BDM_overview_new_template22.png)

3. Velg **Ja** i meldingsboksen for å bekrefte at du vil importere det valgte dokumentet fra det globale repositoriet til gjeldende Finance-forekomst. Hvis du blir spurt om godkjenning, følger du instruksjonene på skjermen.
4. I den nye dialogboksen, i **Tittel**-feltet endrer du tittelen etter behov. Tittelteksten brukes til å navngi den nye ER-formatkonfigurasjonen som opprettes automatisk. Utkastversjonen av denne konfigurasjonen (**Kopi av purrenota (Excel)**) vil inneholde den redigerte malen og vil bli brukt til å kjøre dette ER-formatet for den gjeldende brukeren. Den opprinnelige malen fra den grunnleggende ER-formatkonfigurasjonen vil bli brukt til å kjøre dette ER-formatet for alle andre brukere.
5. I **Navn** -feltet endrer du navnet på den første revisjonen av den redigerbare malen som skal opprettes automatisk.
6. I **Kommentar**-feltet oppdater du merknadene for revisjonen av den redigerbare malen som opprettes automatisk.
7. Velg **OK** for å bekrefte starten på redigeringsprosessen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

