---
title: Opprette en app for gjentakende dataeksport
description: Denne artikkelen viser hvordan du oppretter en logisk Microsoft Azure-app som eksporterer data fra Microsoft Dynamics 365 Human Resources etter en gjentakende tidsplan.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 97972d2179c42e9d2d672cbebb75643ef0a02a62
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113680"
---
# <a name="create-a-recurring-data-export-app"></a>Opprette en app for gjentakende dataeksport

Denne artikkelen viser hvordan du oppretter en logisk Microsoft Azure-app som eksporterer data fra Microsoft Dynamics 365 Human Resources etter en gjentakende tidsplan. Opplæringsprogrammet drar nytte av REST-API for DMF-pakke i Human Resources for å eksportere dataene. Når dataene er eksportert, lagrer den logiske appen den eksporterte datapakken i en Microsoft OneDrive for Business-mappe.

## <a name="business-scenario"></a>Forretningsscenario

I et typisk forretningsscenario for Microsoft Dynamics 365-integreringer må data eksporteres til et nedstrøms system etter en regelmessig tidsplan. Denne opplæringen viser hvordan du eksporterer alle arbeiderposter fra Microsoft Dynamics 365 Human Resources og lagrer listen over arbeidere i en OneDrive for Business-mappe.

> [!TIP]
> De spesifikke dataene som eksporteres i denne opplæringen og målet for de eksporterte dataene, er bare eksempler. Du kan enkelt endre dem slik at de oppfyller dine forretningsbehov.

## <a name="technologies-used"></a>Teknologier som brukes

Denne opplæringen bruker følgende teknologier:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – Hoveddatakilden for arbeidere som skal eksporteres.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Teknologien som sørger for orkestrering og planlegging av den gjentakende eksporten.

    - **[Kontakter](https://docs.microsoft.com/azure/connectors/apis-list)** – Teknologien som brukes til å koble den logiske appen til de nødvendige endepunktene.

        - [HTTP med Azure AD](https://docs.microsoft.com/connectors/webcontents/)-kontakt
        - [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-kontakt

- **[REST-API for DMF-pakke](../dev-itpro/data-entities/data-management-api.md)** – Teknologien som brukes til å utløse eksporten og overvåke fremdriften.
- **[OneDrive for Business](https://onedrive.live.com/about/business/)** – Målet for de eksporterte arbeiderne.

## <a name="prerequisites"></a>Forutsetninger

Før du begynner øvelsen i denne opplæringen, må du ha følgende elementer:

- Et Human Resources-miljø med tillatelser på administratornivå i miljøet
- Et [Azure-abonnement](https://azure.microsoft.com/free/) for å være vert for den logiske appen

## <a name="the-exercise"></a>Øvelsen

På slutten av denne øvelsen vil du ha en logisk app som er koblet til Human Resources-miljøet og OneDrive for Business-kontoen din. Den logiske appen eksporterer en datapakke fra Human Resources, venter på at eksporten skal fullføres, laster ned den eksporterte datapakken og lagrer datapakken i OneDrive for Business-mappen du har angitt.

Den fullførte logiske appen ligner på den følgende illustrasjonen.

![Oversikt over logisk app](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>Trinn 1: Opprette et dataeksportprosjekt i Human Resources

I Human Resources oppretter du et dataeksportprosjekt som eksporterer arbeidere. Gi prosjektet navnet **Eksporter arbeidere**, og kontroller at alternativet **Generer data pakke** er satt til **Ja**. Legg til en enkelt enhet (**arbeider**) i prosjektet, og velg formatet du vil eksportere i. (Microsoft Excel-formatet brukes i denne opplæringen.)

![Dataprosjektet Eksporter arbeidere](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Husk navnet på dataeksportprosjektet. Du kommer til å trenge det når du oppretter den logiske appen i neste trinn.

### <a name="step-2-create-the-logic-app"></a>Trinn 2: Opprette den logiske appen

Mesteparten av øvelsen omfatter oppretting av den logiske appen.

1. Opprett en logisk app i Azure-portalen.

    ![Side for å opprette logisk app](media/integration-logic-app-creation-1.png)

2. Start med en tom logisk app i Logic Apps Designer.
3. Legg til en [utløser for gjentakelsesplan](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) for å kjøre appen hvert døgn (eller etter en plan du velger selv).

    ![Dialogboks for gjentakelse](media/integration-logic-app-recurrence-step.png)

4. Kall DMF REST-API-en [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) for å planlegge eksporten av datapakken.

    1. Bruk handlingen **Aktiver en HTTP-forespørsel** fra HTTP med Azure AD-kontakten.

        - **URL-adresse for basisressurs:** URL-adressen til Human Resources-miljøet (ikke inkluder informasjon om bane/navneområde)
        - **URI for Azure AD-ressurs:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Human Resources-tjenesten har enda ikke en kontakt som viser alle API-ene som utgjør REST-API-en for DMF-pakke, for eksempel **ExportToPackage**. Du må i stedet kalle API-ene ved å bruke rå HTTPS-forespørsler via HTTP med Azure AD-koblingen. Denne koblingen bruker Azure Active Directory (Azure AD) for godkjenning og autorisasjon til Human Resources.

        ![HTTP med Azure AD-kontakt](media/integration-logic-app-http-aad-connector-step.png)

    2. Logg deg på Human Resources-miljøet via HTTP med Azure AD-kontakten.
    3. Konfigurer en HTTP **POST**-forespørsel for å kalle DMF REST-API-en **ExportToPackage**.

        - **Metode:** POST
        - **URL-adresse til forespørselen:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Teksten i forespørselen:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Aktivere en HTTP-forespørselshandling](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Du vil kanskje gi nytt navn til hvert trinn, slik at det blir mer meningsfylt enn standardnavnet, **Aktiver en HTTP-forespørsel**. Du kan for eksempel endre navnet på dette trinnet til **ExportToPackage**.

5. [Initialiser en variabel](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) for å lagre kjørestatusen til **ExportToPackage**-forespørselen.

    ![Handlingen Initialiser variabel](media/integration-logic-app-initialize-variable-step.png)

6. Vent til kjørestatusen for dataeksporten er **Vellykket**.

    1. Legg til en [Til-løkke](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) som gjentas til verdien av **ExecutionStatus**-variabelen er **Vellykket**.
    2. Legg til en **Forsinkelse**-handling som venter fem sekunder før den spør etter gjeldende kjørestatus for eksporten.

        ![Beholder for Til-løkke](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Sett grenseantallet til **15** for å vente i maksimalt 75 sekunder (15 gjentakelser x 5 sekunder) for at eksporten skal fullføres. Hvis eksporten tar mer tid, justerer du grenseantallet etter behov.        

    3. Legg til handlinge **Aktiver HTTP-forespørsel** for å kalle DMF REST-API-en [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus), og sett variabelen **ExecutionStatus** til resultatet av **GetExecutionSummaryStatus**-svaret.

        > Dette eksemplet sjekker ikke for feil. API-en **GetExecutionSummaryStatus** kan returnere ikke-vellykkede sluttilstander (det vil si andre tilstander enn **Vellykket**). Hvis du vil ha mer informasjon, kan du se i [API-dokumentasjonen](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Metode:** POST
        - **URL-adresse til forespørselen:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Teksten i forespørselen:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Du må kanskje angi verdien for **Teksten i forespørselen:** enten i kodevisning eller i funksjonsredigeringsprogrammet i utformingen.

        ![Aktivere en HTTP-forespørselshandling 2](media/integration-logic-app-get-execution-status-step.png)

        ![Angi variabelhandling](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > Verdien for handlingen **Angi variabel** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) er forskjellig fra verdien for teksten **Aktivere en HTTP-forespørsel 2**, selv om verdiene vises på samme måte i utformingen.

7. Få tak i URL-adressen for nedlasting av den eksporterte pakken.

    - Legg til hendelsen **Aktiver HTTP-forespørsel** for å kalle DMF REST-API-en [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl).

        - **Metode:** POST
        - **URL-adresse til forespørselen:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Teksten i forespørselen:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![GetExportedPackageURL-handlingen](media/integration-logic-app-get-exported-package-step.png)

8. Last ned den eksporterte pakken.

    - Legg til en HTTP **GET**-forespørsel (en innebygd [HTTP-koblingshandling](https://docs.microsoft.com/azure/connectors/connectors-native-http)) for å laste ned pakken fra URL-adressen som ble returnert i forrige trinn.

        - **Metode:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Du må kanskje angi verdien for **URI** enten i kodevisning eller i funksjonsredigeringsprogrammet i utformingen.

        ![HTTP GET-handling](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Denne forespørselen krever ingen ekstra godkjenning fordi URL-adressen som API-en **GetExportedPackageUrl** returnerer, inneholder et token for delte tilgangssignaturer som gir tilgang til å laste ned filen.

9. Lagre den nedlastede pakken ved hjelp av [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)-koblingen.

    - Legg til en OneDrive for Business-handling [Opprett fil](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file).
    - Koble til OneDrive for Business-kontoen etter behov.

        - **Mappebane:** En mappe du velger
        - **Filenavn:** worker\_package.zip
        - **Filinnhold:** Teksten fra forrige trinn (dynamisk innhold)

        ![Opprett fil-handling](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>Trinn 3: Teste den logiske appen

Hvis du vil teste den logiske appen, velger du **Kjør**-knappen i utformingsverktøyet. Du ser at trinnene i den logiske appen begynner å kjøre. Etter 30 til 40 sekunder, skal den logiske appen slutte å kjøre, og OneDrive for Business-mappen skal inneholde en ny pakkefil som inneholder de eksporterte arbeiderne.

Hvis det rapporteres en feil i et hvilket som helst trinn, velger du det mislykkede trinnet i utformingen og undersøker feltene **Inndata** og **Utdata** for den. Feilsøk og rett opp trinnet etter behov for å korrigere feilene.

Illustrasjonen nedenfor viser hvordan Logic Apps Designer ser ut når alle trinnene i den logiske appen er kjørt vellykket.

![Vellykket kjøring av logisk app](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Sammendrag

I denne opplæringen lærte du hvordan du bruker en logisk app til å eksportere data fra Human Resources og lagre de eksporterte dataene i en OneDrive for Business-mappe. Du kan endre trinnene i denne opplæringen etter behov for å dekke dine forretningsbehov.


