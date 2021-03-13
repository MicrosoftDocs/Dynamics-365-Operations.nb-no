---
title: Opplæring i installasjon og konfigurasjon av Regression Suite Automation Tool
description: Dette emnet er en opplæring i hvordan du konfigurerer og installerer RSAT (Regression Suite Automation Tool).
author: robinarh
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 46115dc4a46be951517265197f76637ad3e63b78
ms.sourcegitcommit: b337b647a1be4908fc361fb6d962e96a69f301a9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/21/2021
ms.locfileid: "5036726"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Opplæring i installasjon og konfigurasjon av Regression Suite Automation Tool

Dette emnet hjelper deg å konfigurere og komme i gang med RSAT og verktøyene som er knyttet til bruk av RSAT.

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Bruk nettleserverktøyene til å laste ned og lagre denne siden i PDF-format.

## <a name="key-concepts"></a>Nøkkelbegreper

- Forstå installasjonen og den nødvendige konfigurasjonen som kreves for de ulike programmene som støtter RSAT (Regression Suite Automation Tool).
- Forstå hvordan du kan bruke oppgaveopptakerfunksjonen sammen med Microsoft Dynamics Lifecycle Services (LCS) og Microsoft Azure DevOps, til å opprette, konfigurere, kjøre, undersøke og rapportere testtilfeller.
- Gi funksjonsbrukere muligheten til å registrere forretningsoppgaver ved hjelp av oppgaveopptakeren, og konverter deretter oppgaveopptakene til en serie med automatiserte tester uten å måtte skrive kildekode.

## <a name="before-you-begin"></a>Før du begynner

### <a name="prerequisites"></a>Forutsetninger

- Denne opplæringen krever et miljø som kjører Microsoft Dynamics 365 for Finance and Operations versjon 10.0 (april 2019) eller nyere. For kunder som bruker Microsoft Dynamics 365 for Finance and Operations, støttes også Enterprise Edition 7.3, Platform update 20 (PU20) eller senere.
- Brukeren må ha administratorrettigheter til miljøet.
- Du må ha tilgang til LCS for kundeleier og Azure DevOps (tidligere kalt Microsoft Visual Studio Team Services \[VSTS\]).
- Brukeren som oppretter og administrerer seriene med tester, må ha en lisens for Azure DevOps Test Plans eller Test Manager. Følgende lisenser gir deg også tilgang til Test Plans:
    - Visual Studio Enterprise-lisens
    - Visual Studio Test Professional-lisens
    - Abonnentlisens for MSDN-plattformer
- RSAT må ha tilgang til testmiljøet via en nettleser.
- Hvis du vil generere og redigere testparametere, må du ha Microsoft Excel installert.

## <a name="configure-azure-devops"></a>Konfigurer Azure DevOps

### <a name="user-eligibility"></a>Brukerrettigheter

Kontroller at brukeren er opprettet i Azure DevOps og har et abonnementsnivå som gir tilgang til Azure Test Plans. En lisens for Azure DevOps Test Plans kreves bare hvis brukeren skal opprette og administrere testtilfeller (det vil si at ikke alle RSAT-brukere trenger denne lisensen). Hvis du vil ha informasjon om lisenskrav, kan du se [Lisenskrav](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Opprette et nytt Azure DevOps-prosjekt

RSAT bruker Azure Devops til administrasjon av testtilfeller og testserier, rapportering og undersøkelse testkjøringsresultater.

> [!NOTE]
> Du kan bruke et eksisterende Azure DevOps-prosjekt. Hvis det eksisterende Azure DevOps-prosjektet imidlertid er konfigurert slik at det har en egendefinert mal, får du feilmeldingen «Feil under VSTS-synkronisering» når du synkroniserer testtilfeller fra Forretningsprosessmodelerer (BPM) til Azure DevOps (se delen [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)). Hvis du har fulgt følgende anbefalte fremgangsmåter for den egendefinerte malen, kan du synkronisere testtilfellene til Azure DevOps. (Disse anbefalte fremgangsmåtene vises i feilmeldingen.)

- Ikke slett arbeidselementtyper eller standardfelt.
- Ikke slett statusen til en arbeidselementtype.
- Ikke legg til obligatoriske felt i en arbeidselementtype.

![Feilmelding med en liste over anbefalte fremgangsmåter](./media/setup_rsa_tool_02.png)

For denne opplæringen anbefaler vi for øvrig at du oppretter et nytt Azure DevOps-prosjekt. Hvis du vil ha mer informasjon, kan du se [Problemer ved synkronisering til BPM når du bruker en egendefinert mal for Azure DevOps-prosess (VSTS)](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).

1. Åpne URL-adressen til Azure DevOps (`https://dev.azure.com/<Azure DevOps Name>`).
2. Velg **Opprett prosjekt** i øvre høyre hjørne på Azure DevOps-siden.

    ![Opprett prosjekt-knappen](./media/setup_rsa_tool_03.png)

3. Fyll ut følgende felt, og velg deretter **Opprett**:

    - **Prosjektnavn**
    - **Versjonskontroll** – Velg **Team Foundation Version Control**. Vær oppmerksom på at standardalternativet **Git** ikke støttes.
    - **Arbeidselementbehandling**

    ![Dialogboksen Opprett nytt prosjekt](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Opprette et personlig tilgangstoken

I denne opplæringen skal du bruke Forretningsprosessmodelerer (BPM) i LCS til å opprette et bibliotek for testtilfeller og synkronisere testtilfellene med Azure DevOps. Du må ha et personlig tilgangstoken for å synkronisere BPM med Azure DevOps.

1. Velg profilikonet i øvre høyre hjørne på siden for Azure DevOps-prosjektet, og velg deretter **Sikkerhet**.

    ![Sikkerhet-kommandoen](./media/setup_rsa_tool_05.png)

2. Velg **Personlige tilgangstokener** under **Sikkerhet** i venstre rute. Velg deretter **Nytt token**.

    ![Nytt token-knappen i fanen Personlige tilgangstokener i Brukerinnstillinger](./media/setup_rsa_tool_06.png)

3. Fyll ut følgende felt, og velg deretter **Opprett**:

    - **Navn**
    - **Utløp (UTC)** – Velg **Egendefinert**, og bruk deretter datovelgeren til å velge den siste tilgjengelige datoen.
    - **Omfang** – Velg alternativet **Full tilgang**.

    ![Dialogboksen for å opprette et nytt personlig tilgangstoken](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Noter deg det personlige tilgangstokenet som opprettes. Du får bruk for det senere når du foretar RSAT-konfigurasjonen.

    ![Personlig tilgangstoken](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>Konfigurere LCS-prosjektet

Du trenger et LCS-prosjekt (Lifecycle Services) for hovedtestbiblioteket. Forretningsprosessmodelerer (BPM) i LCS brukes som hovedbibliotek for testtilfellene. BPM brukes til å administrere og distribuere testbiblioteker på tvers av LCS-prosjekter. En Microsoft-partner eller uavhengig programvareleverandør som for eksempel bygger testbiblioteker, gir ut testtilfeller i form av BPM-biblioteker. I BPM organiseres testtilfeller etter forretningsprosess. BPM definerer ikke utføringsrekkefølgen eller -frekvensen for testomgangen. Disse detaljene administreres i Azure DevOps, som beskrevet senere i dette emnet.  

For LCS-prosjektet kan du bruke en eksisterende kundeimplementering eller et eksisterende partnerprosjekt.

### <a name="update-the-lcs-language"></a>Oppdatere LCS-språket

> [!NOTE]
> For at brukergrensesnittet (UI) skal kunne vise forretningsprosesser på riktig måte, må det foretrukne LCS-språket settes til **Engelsk (USA)**.

1. Gå til LCS-implementeringsprosjektet.
2. Velg **Innstillinger**-knappen (tannhjulsymbolet) i øvre høyre hjørne på siden, og velg deretter **Språkinnstilling**.

    ![Oppdatere språkinnstilling](./media/setup_rsa_tool_09.png)

3. I feltet **Foretrukket språk** velger du **Engelsk (USA)** og deretter **Lagre**.

    ![Språkinnstilling-fanen i Brukerinnstillinger](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>Konfigurere LCS for å koble til Azure DevOps-prosjektet

Hvis du opprettet et nytt Azure DevOps-prosjekt tidligere, konfigurerer du LCS-prosjektet for å koble til det. Hvis LCS-prosjektet imidlertid allerede er koblet til Azure DevOps-prosjektet, kan du gå videre til neste del.

1. Gå til LCS-implementeringsprosjektet.
2. Velg **Meny**-knappen, og velg deretter **Prosjektinnstillinger**.

    ![Prosjektinnstillinger-kommandoen](./media/setup_rsa_tool_11.png)

3. I venstre rute velger du **Visual Studio Team Services**, og deretter velger du **Konfigurer Visual Studio Team Services**.

    ![Fanen Visual Studio Team Services i Prosjektinnstillinger](./media/setup_rsa_tool_12.png)

4. I feltet **URL-adresse til Azure DevOps-området** angir du URL-adressen til Azure DevOps-området. I feltet **Personlig tilgangstoken** angir du det personlige tilgangstokenet som ble opprettet tidligere.

    > [!NOTE]
    > Selv om VSTS nå kalles Azure DevOps, bruker du den gamle URL-adressen til å koble LCS til Azure DevOps-prosjektet. URL-adressen til Azure DevOps som brukes i denne opplæringen, er for eksempel `https://dev.azure.com/D365FOFastTrack/`. I illustrasjonen nedenfor er den imidlertid angitt som `https://D365FOFastTrack.visualstudio.com/`.

    ![Trinn 1 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. Velg **Fortsett**.
6. I feltet **Visual Studio Team Services-prosjektet** velger du VSTS-prosjektet på det valgte området som skal kobles til LCS-prosjektet. **Prosessmal**-feltet er satt til **Fleksibel** som standard. Når det gjelder en egendefinert mal, ser du gjennom veiledningen for anbefalte fremgangsmåter i delen [Opprette et nytt Azure DevOps-prosjekt](#create-a-new-azure-devops-project). Velg deretter **Fortsett**.

    ![Trinn 2 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. Se gjennom innstillingene, og velg deretter **Lagre**.

    ![Trinn 3 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. Velg **Autoriser** for å autorisere at LCS kan få tilgang til det konfigurerte Azure DevOps-området på vegne av deg, og for å aktivere funksjoner som kan integreres med VSTS.

    ![Autoriser-knappen](./media/setup_rsa_tool_16.png)

9. Det vises en meldingsboks der det står «Du er i ferd med å bli omdirigert til et eksternt område for å gi Lifecycle Services tilgang til å koble til Visual Studio Team Services på dine vegne. Fortsette?» Velg **Ja**.

    ![Meldingsboks](./media/setup_rsa_tool_17.png)

10. Velg **Godta**.

    ![Autorisere tilgang](./media/setup_rsa_tool_18.png)

11. Hvis du er autorisert som bruker, skal brukergrensesnittet sende deg tilbake til siden for LCS-prosjektinnstillinger.

    ![Autorisert bruker](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Opprett et nytt BPM-bibliotek

1. Gå til LCS-implementeringsprosjektet.
2. Velg **Meny**-knappen, og velg deretter **Forretningsprosessmodelerer**.

    ![Kommandoen Forretningsprosessmodelerer](./media/setup_rsa_tool_20.png)

3. Velg **Nytt bibliotek**.

    ![Nytt bibliotek-knappen](./media/setup_rsa_tool_21.png)

4. Skriv inn et navn i feltet **Navn på bibliotek**, og velg deretter **Opprett**. For denne opplæringen gir du BPM-biblioteket navnet **RSAT**.

    ![Dialogboksen Opprett nytt bibliotek](./media/setup_rsa_tool_22.png)

5. Åpne det nye BPM-biblioteket **RSAT**.
6. Velg prosessen **Eksempel på kjerneforretningsprosess**, og velg deretter **Redigeringsmodus** til høyre.

    ![Redigeringsmodus-knappen](./media/setup_rsa_tool_23.png)

7. Endre verdien i **Navn**-feltet og **Beskrivelse**-feltet til **Opprett et produkt**. Velg deretter **Lagre**.

    ![Feltene Navn og Beskrivelse](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Miljø

### <a name="version-requirement"></a>Versjonskrav

En test eller et sandkassemiljø som kjører versjon 10, er nødvendig. For kunder som bruker versjon 7.3, støttes også Platform update 20 eller senere.

> [!NOTE]
> RSAT må ha tilgang til testmiljøet via en nettleser.

### <a name="user-criteria"></a>Brukerkriterier

Brukeren må ha administratorrettigheter til dette miljøet.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Konfigurere Hjelp-innstillinger for å koble til LCS

Dette trinnet er nødvendig for å kunne koble til LCS, slik at oppgaveopptak kan lagres i riktig BPM-bibliotek i LCS via klienten.

1. Start klienten.
2. Gå til **Systemadministrasjon \> Oppsett \> Systemparametere**.
3. I feltet **Konfigurasjon av hjelp for Lifecycle Services** i **Hjelp**-fanen velger du det relevante LCS-prosjektet (**RSAT** for denne opplæringen).

    ![Feltet Konfigurasjon av hjelp for Lifecycle Services i Hjelp-fanen](./media/setup_rsa_tool_25.png)

    BPM-biblioteker fylles ut i det riktige LCS-prosjektet.

4. Velg **Lagre**.
5. Du må kanskje oppdatere nettleseren for å kunne se det oppdaterte innholdet i Hjelp.

    ![Varsling om oppdatering av nettleseren](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Oppgaveopptak

> [!NOTE]
> Kontroller at alle oppgaveopptakene starter på hovedinstrumentbordet. Hold individuelle opptak korte, og fokuser på én forretningsoppgave, for eksempel opprettelse av en salgsordre.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Opprette et oppgaveopptak og lagre det i BPM-biblioteket

Opprett et tilsvarende oppgaveopptak du kan knytte til den enkle forretningsprosessen som ble opprettet i det nye BPM-biblioteket.

1. Start klienten.
2. Velg **Innstillinger**-knappen (tannhjulsymbolet) på hovedinstrumentbordet, og velg deretter **Oppgaveopptaker**.

    ![Velge Oppgaveopptaker på Innstillinger-menyen](./media/setup_rsa_tool_27.png)

3. Velg **Opprett opptak**.

    ![Opprett opptak-knappen](./media/setup_rsa_tool_28.png)

4. Fyll ut feltene **Navn på opptak** og **Beskrivelse av opptak**, og velg deretter **Start**.

    ![Feltene Navn på opptak og Beskrivelse av opptak](./media/setup_rsa_tool_29.png)

5. Ta opp trinnene for å opprette et produkt. Når du er ferdig, velger du **Stopp** for å stoppe opptaket.

    ![Trinn for å opprette et produkt](./media/setup_rsa_tool_30.png)

6. Velg **Lagre i Lifecycle Services**.

    ![Lagre oppgaveopptak i Lifecycle Services](./media/setup_rsa_tool_31.png)

    Bibliotekinformasjon lastes inn fra LCS.

    ![Laste inn bibliotekinformasjon](./media/setup_rsa_tool_32.png)

7. Velg BPM-biblioteket som oppgaveopptaket skal knyttes til. For denne opplæringen velger du BPM-biblioteket **RSAT** som ble opprettet tidligere, og forretningsprosessen **Opprett et produkt** under det. Velg deretter **OK**.

    ![Knytte oppgaveopptaket til et BPM-bibliotek og en forretningsprosess](./media/setup_rsa_tool_33.png)

    Meldingen «Lagring i Lifecycle Services er utført» vises.

    ![Melding om vellykket lagring i LCS](./media/setup_rsa_tool_34.png)

8. Hvis du vil lagre oppgaveopptaket lokalt og deretter laste det opp til BPM via LCS, følger du denne fremgangsmåten:

    1. Når opptaket er fullført, velger du **Lagre på denne PC-en**.

        ![Lagre på denne PC-en](./media/setup_rsa_tool_35.png)

    2. I nettleserens varslingsfelt velger du **Lagre** eller **Lagre som** for å lagre filen på den lokale datamaskinen.

        ![Varslingsfelt](./media/setup_rsa_tool_36.png)

    3. Gå til BPM-biblioteket **RSAT**, og velg forretningsprosessen du vil lagre oppgaveopptaket mot.
    4. Velg **Last opp** i **Oversikt**-fanen.

        ![Last opp-knappen](./media/setup_rsa_tool_37.png)

    5. Velg **Bla gjennom**, og velg AXTR-filen du lagret tidligere. Velg deretter **Last opp**.

        ![Velge AXTR-filen som skal lastes opp](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>Teste synkroniseringen fra BPM til Azure DevOps

Nå som et oppgaveopptak er knyttet til forretningsprosessen, må du validere at forretningsprosessen og det tilknyttede oppgaveopptaket kan synkroniseres til Azure DevOps som (henholdsvis) en funksjon og et testtilfelle, ved å bruke VSTS-synkroniseringsfunksjonen i LCS.

> [!NOTE]
> Den tilsvarende arbeidselementtypen som opprettes i Azure DevOps, varierer avhengig av prosessmalen du valgte da du konfigurerte LCS-prosjektet med Azure DevOps, som beskrevet i delen [Opprette et nytt Azure DevOps-prosjekt](#create-a-new-azure-devops-project).

1. Gå til BPM-biblioteket, og åpne **RSAT**-biblioteket du opprettet tidligere.
2. Velg ellipseknappen (**...**), og velg **VSTS-synkronisering**.

    ![Kommandoen VSTS-synkronisering på ellipsemenyen](./media/setup_rsa_tool_39.png)

    Etter at VSTS-synkronisering er fullført, vises det en **Behov**-fane på venstre side som omfatter det tilsvarende Azure DevOps-arbeidselementet.

    > [!NOTE]
    > Arbeidselementet som opprettes i Azure DevOps, har navnet på BPM-biblioteket som tittelprefiks.

    ![Behov-fanen](./media/setup_rsa_tool_40.png)

3. Oppdater siden.
4. Velg ellipseknappen (**...**). Det vises et ekstra alternativ, **Synkroniser testtilfeller**. Velg dette alternativet.

    ![Kommandoen Synkroniser testtilfeller på ellipsemenyen](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Hvis alternativet **Synkroniser testtilfeller** ikke er tilgjengelig etter at du har oppdatert siden, går du til hovedsiden for BPM og velger **Synkroniser testtilfeller** for hele biblioteket. På denne måten fremtvinger du en synkronisering for hele biblioteket.
    >
    > ![Velge Synkroniser testtilfeller for hele biblioteket](./media/setup_rsa_tool_42.png)

    Etter at Synkroniser testtilfeller er fullført, blir det opprettet et nytt testtilfelle i **Behov**-fanen.

    ![Nytt testtilfelle i Behov-fanen](./media/setup_rsa_tool_43.png)

5. Gå til Azure DevOps-prosjektet, og velg **Tavler \> Arbeidselementer**.

    ![Kommandoen Arbeidselementer under Tavler](./media/setup_rsa_tool_44.png)

6. Valider at arbeidselementet og testtilfellet du opprettet ved hjelp av BPM-synkronisering, finnes.

    ![Arbeidselement og testtilfelle](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>Installere og konfigurere RSAT

Du kan installere RSAT på alle datamaskiner som kjører Windows 10 og kan koble til miljøet via en nettleser (Internet Explorer eller Google Chrome).

> [!NOTE]
> Før du installerer en ny versjon av verktøyet, anbefaler vi at du avinstallerer den forrige versjonen.

### <a name="install-an-authentication-certificate"></a>Installere et godkjenningssertifikat

Hvis du vil aktivere godkjenning, må du generere og installere et sertifikat på samme datamaskin som RSAT kjører på.

#### <a name="generate-a-certificate"></a>Generere et sertifikat

1. Hvis du vil generere en sertifikatfil, åpner du et Microsoft Windows PowerShell-vindu som administrator og kjører følgende kommando:

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Åpne sertifikatbehandling ved å skrive inn **certlm.msc** i dialogboksen **Kjør**, og bekreft at sertifikatet **D365 Automated testing certificate** er opprettet under **Personlig \> Sertifikater**.

    > [!NOTE]
    > Pass på at du skriver inn **certlm.msc** msc, ikke **certmgr.msc**, fordi sertifikatene er lagret på den lokale datamaskinen.

    ![Sertifikatet D365 Automated testing certificate](./media/setup_rsa_tool_46.png)

3. Høyreklikk på sertifikatet, og velg deretter **Kopier**.
4. Gå til **Klarerte rotsertifiseringsinstanser \> Sertifikater**.

    ![Sertifikater-mappen under mappen Klarerte rotsertifiseringsinstanser](./media/setup_rsa_tool_47.png)

5. Velg **Lim inn** på **Handling**-menyen for å kopiere sertifikatet til plasseringen **Klarerte rotsertifiseringsinstanser**.

    ![Kommandoen Lim inn på Handling-menyen](./media/setup_rsa_tool_48.png)

6. Hvis du vil hente avtrykket for det installerte sertifikatet, men uten mellomrom eller spesialtegn, åpner du et Windows PowerShell-vindu som administrator og kjører følgende kommandoer:

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Lagre avtrykket, fordi du trenger det senere når du skal oppdatere WIF-filene for AOS (Application Object Server) og foreta RSAT-konfigurasjonen.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>Konfigurere AOS-datamaskinen slik at den klarerer tilkoblingen

> [!NOTE]
> Hvis miljøet er et miljø på Lag 2 eller høyere, må sertifikatavtrykket oppdateres i filen wif.config for **alle** AOS-datamaskiner for miljøet.

1. Opprett en RDP-tilkobling (Remote Desktop Protocol) til AOS-datamaskinen. Påloggingsdetaljer er tilgjengelige på siden for miljødetaljer i LCS.
2. Åpne Microsoft Internet Information Services (IIS), og finn **AOSService** i listen over områder.

    ![AOSService i listen over områder](./media/setup_rsa_tool_49.png)

3. Høyreklikk på **Utforsk** for å åpne mappen **\<Drive\>: \\AosService\\WebRoot**. Finn filen **wif.config**.

    ![Filen wif.config i WebRoot-mappen](./media/setup_rsa_tool_50.png)

4. Oppdater filen **wif.config** ved å legge til en ny instansoppføring for navnet på sertifikatet og instansen, som vist i eksemplet nedenfor.

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Hvis flere brukere bruker samme program, må hver bruker generere separate avtrykk, og hvert av disse avtrykkene må legges til i **\<keys\>**-delen.

5. Hvis det er flere enn én AOS-datamaskin, gjentar du trinn 3 til og med 4 for hver ekstra datamaskin.

    > [!NOTE]
    > I motsetning til eldre Lag 2-miljøer distribueres nye Lag 2-miljøer med to AOS-forekomster.

6. Kjør **iisreset** på alle AOS-datamaskinene.

    > [!NOTE]
    > Hvis du ikke har administratorrettigheter til å kjøre **iisreset** på en Lag 1-datamaskin, velger du Vedlikehold > Start tjenester på nytt på siden Miljødetaljer i LCS.

#### <a name="tier-2-environment"></a>Miljø på Lag 2 eller høyere

Hvis et miljø på Lag 2 eller høyere (sandkasse for standard aksepttest eller høyere), bekrefter eller angir du følgende registerinnstilling på datamaskinen der RSAT er installert. Dette trinnet er nødvendig fordi det gjør at du unngår godkjenningsfeil eller RSAT-tilkoblingsfeil.

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>Installere RSAT

1. Gå til <https://www.microsoft.com/download/details.aspx?id=57357>, og velg **Download**.
2. Merk av for alle filene, og velg deretter **Next**.

    ![Merke av for alle filene](./media/setup_rsa_tool_51.png)

3. Dobbeltklikk på MSI-pakken for å kjøre installasjonsprogrammet. Når installasjonen er fullført, velger du **Fullfør**.

    ![Installasjonsprogramfilen for RSAT](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Installere Selenium og nettleserdrivere

I eldre versjoner av RSAT måtte du installere Selenium og nettleserdrivere. Du trenger ikke lenger å installere disse driverne, fordi de nå installeres automatisk.

1. Første gang du åpner RSAT, blir du bedt om å laste ned og installere Selenium automatisk. Hvis du vil ha mer informasjon, kan du se delen [Konfigurere RSAT](#configure-rsat).
2. Før du kan kjøre et testtilfelle, blir du bedt om å laste ned og installere nettleserdriveren som svarer til standardnettleseren som er valgt i RSAT-konfigurasjonen. Hvis du vil ha mer informasjon, kan du se delen [Laste inn og kjøre testtilfeller](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>Komme i gang med RSAT

### <a name="create-a-test-plan-and-test-suites"></a>Opprette en testplan og testserier

1. Gå til Azure DevOps-prosjektet, og velg **Testplaner**.

    ![Kommandoen Testplaner](./media/setup_rsa_tool_53.png)

2. Velg **Ny testplan**.

    ![Knappen Ny testplan](./media/setup_rsa_tool_54.png)

3. Fyll ut **Navn**-feltet, og velg deretter **Opprett**. For denne opplæringen gir du testplanen navnet **RSAT-testplan**.

    ![Dialogboksen Ny testplan](./media/setup_rsa_tool_55.png)

4. Velg plusstegnet (**+**), og velg deretter **Statisk serie** for å opprette en statisk serie under den nye testplanen. Gi den nye testserien navnet **T01 – Produser for lager**.

    > [!NOTE]
    > Du kan også opprette en spørringsbasert serie hvis du vil at de nye testtilfellene fra BPM skal hentes inn i RSAT-testserien automatisk.

    ![Opprette en statisk serie](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Knytte testtilfeller til testserier

1. Velg **Legg til eksisterende** på høyre side for å legge til eksisterende testtilfeller i testserien.

    ![Knappen Legg til eksisterende](./media/setup_rsa_tool_57.png)

2. Velg **Kjør spørring** på siden **Legg til testtilfeller i serie**, og velg deretter testtilfellet som skal legges til i testserien. For denne opplæringen velger du testtilfellet **Opprett et nytt produkt**. Deretter velger du **Legg til testtilfeller** i nedre høyre hjørne på siden (denne knappen vises ikke i illustrasjonen nedenfor).

    ![Kjør spørring-knappen](./media/setup_rsa_tool_58.png)

    Testtilfellet legges til i testserien **T01 – Produser for lager**.

    ![Testtilfelle lagt til testserien](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>Konfigurer RSAT

1. Åpne RSAT.

    ![RSAT-ikon](./media/setup_rsa_tool_60.png)

2. Du får en advarsel om at Regression Suite Automation Tool krever Selenium, og blir spurt om du vil automatisk laste det ned og installere det nå. Velg **Ja**.

    ![Advarselsmelding om at Regression Suite Automation Tool krever Selenium](./media/setup_rsa_tool_61.png)

3. Velg **Innstillinger**-knappen (tannhjulsymbolet) i øvre høyre hjørne, og fyll deretter ut følgende felt i dialogboksen som vises:

    - **URL-adresse til Azure DevOps** – Skriv inn URL-adressen til Azure DevOps-prosjektet, for eksempel `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Tilgangstoken** – Angi tilgangstokenet som gjør at verktøyet kan koble til Azure DevOps. Bruk det personlige tilgangstokenet du opprettet tidligere i denne opplæringen. Hvis du vil ha mer informasjon, kan du se [Godkjenne tilgang med personlige tilgangstokener](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Prosjektnavn** – Velg navnet på Azure DevOps-prosjektet.
    - **Testplan** – Velg Azure DevOps-testplanen som inneholder testtilfellene. Hvis du vil ha mer informasjon, kan du se [Opprette testplaner og testserier](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Etter at du har valgt en testplan, velger du **Test tilkobling** for å teste tilkoblingen til Azure DevOps.
    - **Vertsnavn** – Angi vertsnavnet på testmiljøet, for eksempel **\<myaos\>.cloudax.dynamics.com**. Ikke ta med prefikset **https://** eller **http://**.
    - **SOAP-vertsnavn** – Angi SOAP-vertsnavnet på testmiljøet. SOAP-vertsnavnet er vanligvis det samme som vertsnavnet, men det har suffikset **SOAP**. Her er et eksempel: **\<myaos\>soap.cloudax.dynamics.com**. Ikke ta med prefikset **https://** eller **http://**.

        > [!NOTE]
        > Du kan finne vertsnavnet og SOAP-vertsnavnet ved å åpne IIS-behandling, høyreklikke på **Områder \> AOSService** og deretter velge **Rediger bindinger**. Verdiene i **Vertsnavn**-kolonnen gir deg vertsnavnet og SOAP-vertsnavnet (SOAP-vertsnavnet har suffikset **soap** i URL-adressen).

        ![Vertsnavn og SOAP-vertsnavn i Vertsnavn-kolonnen](./media/setup_rsa_tool_63.png)

    - **Navn på administratorbruker** – Angi e-postadressen for administratorbruker i testmiljøet.
    - **Avtrykk** – Angi avtrykket for godkjenningssertifikatet, som beskrevet tidligere i denne opplæringen.
    - **Arbeidskatalog** – Angi mappeplasseringen for lagring av testautomatiseringsfiler, for eksempel Excel-testdatafiler. Du kan for eksempel skrive inn eller velge **C:\\Temp\\RegressionTool**.

        > [!NOTE]
        > Hvis navnet på mappen har mellomrom, mislykkes kjøringen fordi mappen ikke blir funnet. Dette er et kjent problem og skal være løst i den nyeste versjonen av verktøyet.

    - **Standardnettleser** – Velg **Internet Explorer** eller **Google Chrome**. Kontroller at de riktige nettleserdriverne er installert.
    - **Tidsavbrudd for testkjøring** – Angi tidsavbruddsperioden for testkjøringer i minutter. Når tidsavbruddsperioden har utløpt, lukkes alle aktive vinduer, og ventende testtilfeller mislykkes.
    - **Tidsavbrudd for testhandling** – Dette feltet styrer tidsavbruddsperioden i minutter for serverforespørsler i Finance and Operation-miljøet. Standardverdien (2 minutter) skal vanligvis være nok. Det kan imidlertid være aktuelt å øke verdien for tregere miljøer hvis det oppstår feil i forbindelse med tidsavbrudd.
    - **Firmanavn** – Angi firmanavnet som skal brukes som standard firma når det opprettes Excel-parameterfiler. Du kan endre firmaet senere ved å redigere Excel-parameterfilen.

    ![Dialogboksen Innstillinger](./media/setup_rsa_tool_62.png)

4. Velg **Bruk** for å bruke og lagre innstillingene.

    Hvis du vil lagre de gjeldende innstillingene i en konfigurasjonsfil på datamaskinen, velger du **Lagre som**. Du kan gjenopprette innstillingene fra en konfigurasjonsfil på datamaskinen ved å velge **Åpne**.

5. Velg **Lukk** for å lukke dialogboksen.

### <a name="load-and-run-test-cases"></a>Laste inn og kjøre testtilfeller

1. Velg **Last inn** for å laste inn **RSAT-testplan** fra Azure DevOps-prosjektet.

    ![Last inn-knappen](./media/setup_rsa_tool_64.png)

2. Velg testtilfellet **Opprett et nytt produkt** fra testserien, og velg deretter **Ny \> Generer testkjøring og parameterfiler**.

    ![Kommandoen Generer testkjøring og parameterfiler på Ny-menyen](./media/setup_rsa_tool_65.png)

    Excel-parameterfilen opprettes i den lokale mappen du angav i RSAT-konfigurasjonen (for eksempel **C:\\Temp\\RegressionTool**).

    ![Excel-parameterfil opprettet](./media/setup_rsa_tool_66.png)

3. Hvis du vil lagre parameterfilene, velger du **Last opp**. Testautomatiseringsfiler for alle valgte testtilfeller lastes opp til Azure DevOps for fremtidig bruk. (Disse filene omfatter Excel-testparameterfiler.)

    På denne måten kan du velge **Last inn** for å laste inn parameterfilene (og automatiseringsfilene) fra testtilfellet direkte fra Azure DevOps. Du trenger ikke å generere parameterfilene på nytt. Denne metoden blir viktig senere, når du ønsker å beholde endringene i parameterfilen og ikke vil at de skal bli overskrevet.

4. Du kan kontrollere at automatiseringsfilene og parameterfilene er lagret i Azure DevOps, ved å gå til Azure DevOps-prosjektet, velge **Tavler \> Arbeidselementer** og velge testtilfellet **Opprett et nytt produkt**. Følgende fire filer skal vises i **Vedlegg**-fanen:

    - **CS** – C\#-automatiseringsfil
    - **DLL** – Kompilert automatiseringsfil som en samling
    - **XLSX** – Excel-parameterfil
    - **XML** – Opptaksfil

    ![Filer i Vedlegg-fanen](./media/setup_rsa_tool_67.png)

5. Velg testtilfellet som skal kjøres, og velg deretter **Kjør**.

    > [!NOTE]
    > Hvis du bruker Internet Explorer, må du kontrollere at skrivebordsoppløsningen er satt til **100 %** i **Skjerminnstillinger \> Skala og oppsett** i Windows før du kjører testtilfeller. Hvis du ikke kan endre denne innstillingen på en virtuell maskin (VM), må du endre den på klienten (den bærbare datamaskinen) som du prøver å få tilgang til VM-en fra. Innstillingene for oppløsning arves deretter av skjerminnstillingene for VM-en.

    ![Skrivebordsoppløsningen satt til 100 %](./media/setup_rsa_tool_68.png)

6. Hvis nettleserdriverne ikke er installert på systemet, får du en advarsel om at denne operasjonen krever driveren for \<browser name\>. Deretter blir du spurt om du vil laste den ned og installere den automatisk nå. Velg **Ja**.

    ![Advarsel for Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Advarsel for Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Hvis du bruker Chrome og får en feilmelding om at økten ikke ble opprettet fordi du bruker feil Chrome-versjon, laster du ned den nyeste Chrome-driveren fra <http://chromedriver.chromium.org/downloads> til mappen **C:\\Programfiler (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.

    ![Feilmelding for Chrome](./media/setup_rsa_tool_71.png)

    Testtilfellet kjøres, og **Resultat**-feltet oppdateres.

    ![Oppdatert Resultat-felt](./media/setup_rsa_tool_72.png)

    Hvis du har fulgt denne opplæringen slik den er skrevet, mislykkes testtilfellet **Opprett et nytt produkt** fordi oppgaveopptaket for opprettelsen av et produkt lagret produktnavnet som en hardkodet verdi. Hvis du kjører det samme testtilfellet på nytt, skal du få en feilmelding fordi produktet allerede finnes.

    ![Resultat-felt satt til Mislyktes](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Vise testresultatene

1. Dobbeltklikk på det mislykkede testtilfellet.

    Du får en feilmelding.

    ![Feilmelding](./media/setup_rsa_tool_73.png)

2. Velg **Detaljer** for å vise hele feilmeldingen.

    ![Hele feilmeldingen](./media/setup_rsa_tool_74.png)

3. Hvis du vil vise en detaljert versjon av feilmeldingen i Azure DevOps, velger du **Åpne i Azure DevOps**. I Azure DevOps kan du vise statusen for testtilfellet og den detaljerte feilmeldingen.

    ![Detaljert feilmelding i Azure DevOps](./media/setup_rsa_tool_75.png)

4. Hvis du vil vise testresultatene direkte i Azure DevOps-prosjektet, kan du gå til **Testplaner \> Testplaner \> Kjøringer**. Dobbeltklikk på testkjøringen du vil vise flere detaljer om.

    ![Liste over testkjøringer i Azure DevOps](./media/setup_rsa_tool_76.png)

5. Fanen **Kjøringssammendrag** angir at testtilfellet mislyktes, men den faktiske feilmeldingen vises ikke. Hvis du vil vise den detaljerte feilmeldingen, velger du **Testresultater**-fanen.

    ![Fanen Kjøringssammendrag](./media/setup_rsa_tool_77.png)

    **Testresultater**-fanen inneholder informasjon om testtilfellet sammen med resultatet og feilmeldingen.

    ![Testresultater-fanen](./media/setup_rsa_tool_78.png)

6. Dobbeltklikk på den aktuelle posten for å vise den detaljerte feilmeldingen.

    ![Detaljert feilmelding](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Alle feilmeldinger også tilgjengelige lokalt i **C:\\Brukere\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.

7. Du kan også eksportere resultatene av testkjøringen fra testplannivået ved å velge **Eksporter**.

    ![Eksportere en testplan](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Endre Excel-parameterfilen

1. Åpne RSAT.
2. Velg testtilfellet, og velg deretter **Rediger** for å åpne Excel-parameterfilen.

    I arket **EcoResProductCreate** legger du merke til at verdien i **Produktnummer**-feltet er hardkodet. Du må oppdatere dette feltet til et nytt produktnummer før du kjører testtilfellet på nytt.

3. Hvis du vil generere et unikt produktnummer for hver kjøring uten å måtte åpne Excel-parameterfilen på nytt og oppdatere produktnummeret manuelt hver gang, bruker du følgende Excel-formel.

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > I tillegg til **Generelt**-fanen inneholder Excel-parameterfilen en datafane for hver skjemaside testtilfellet går til.

    ![Produktnummer-feltet](./media/setup_rsa_tool_81.png)

4. Velg **Lagre**, og lukk deretter Excel-arbeidsboken.
5. Velg **Last opp** for å lagre Excel-parameterfilen i Azure DevOps.

    ![Melding om vellykket opplasting](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Hvis du vil kjøre testtilfeller i en bestemt brukerkontekst, angir du brukerens e-post-ID i **Testbruker**-feltet i **Generelt**-fanen i Excel-parameterfilen. I den nyeste versjonen av RSAT er oppsettet av feltene i Excel-parameterfilen oppdatert, men konseptet er uendret.
    >
    > ![Testbruker-feltet](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Validere resultatene

- Velg **Kjør** for å kjøre testtilfellet på nytt, og kontroller at testtilfellet har bestått. Du kan vise testresultatene som beskrevet i delen [Vise testresultatene](#view-the-test-results).

    ![Resultat-feltet satt til Bestått](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Kjeding av testtilfeller

En nøkkelfunksjon i RSAT er kjeding av testtilfeller (det vil si funksjonen som gjør at en test kan sende verdier til andre tester). Testtilfeller kjøres i henhold til den definerte rekkefølgen i Azure DevOps-testplanen. (Denne rekkefølgen kan også oppdateres i selve testverktøyet.) Hvis du vil sende variabler fra ett testtilfelle til et annet, er det derfor svært viktig at testene er i riktig rekkefølge.

I denne delen skal du opprette en lagret variabel i det første testtilfellet, opprette et andre testtilfelle og sende den lagrede variabelen fra det første til det andre testtilfellet. Du skal deretter kjøre testtilfellen som et kjedet testtilfelle i RSAT.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Endre et eksisterende oppgaveopptak for å opprette en lagret variabel

1. Start klienten.
2. Velg **Innstillinger**-knappen (tannhjulsymbolet), og velg deretter **Oppgaveopptaker**.
3. Velg **Rediger opptak**.

    ![Rediger opptak-knappen](./media/setup_rsa_tool_85.png)

4. Velg **Åpne fra Lifecycle Services**.

    ![Knappen Åpne fra Lifecycle Services](./media/setup_rsa_tool_86.png)

5. Velg **Velg Lifecycle Services-biblioteket**.

    ![Knappen Velg Lifecycle Services-biblioteket](./media/setup_rsa_tool_87.png)

    BPM-biblioteker lastes inn fra LCS.

    ![Laste inn BPM-biblioteker](./media/setup_rsa_tool_88.png)

6. Etter at BPM-bibliotekene er lastet inn fra LCS, velger du BPM-biblioteket **RSAT** og forretningsprosessen **Opprett et nytt produkt** som oppgaveopptaket var knyttet til. Velg deretter **OK**.

    ![Velge et BPM-bibliotek og en forretningsprosess](./media/setup_rsa_tool_89.png)

7. Navnet på det aktuelle oppgaveopptaket angis i feltet **Navn på opptak**. Velg **Start**.

    ![Navnet på oppgaveopptaket i feltet Navn på opptak](./media/setup_rsa_tool_90.png)

8. Gå til **Behandling av produktinformasjon \> Produkter**, og velg **Ny** for å åpne siden der det opprinnelige oppgaveopptaket, **Opprett et produkt**, ble tatt opp.
9. Velg **Sett inn trinn**.

    > [!NOTE]
    > Det nye trinnet settes inn **etter** trinnet du valgte i ruten.

    ![Knappen Sett inn trinn](./media/setup_rsa_tool_91.png)

10. Høyreklikk på **Produktnummer**-feltet, og velg deretter **Oppgaveopptaker \> Kopier**.

    ![Kopier-kommandoen](./media/setup_rsa_tool_92.png)

11. Det legges til et nytt trinn i ruten. Noter verdien i **Produktnummer**-feltet siden du får behov for det senere.

    ![Nytt trinn lagt til](./media/setup_rsa_tool_93.png)

12. Velg **Redigeringen er fullført**.
13. Velg **Lagre i Lifecycle Services**, og knytt det nye oppgaveopptaket til det samme BPM-biblioteket og den samme forretningsprosessen som det opprinnelige oppgaveopptaket var knyttet til. Hvis du vil ha mer informasjon, kan du se delen [Opprette et oppgaveopptak og lagre det i BPM-biblioteket](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Gå til BPM-biblioteket, og velg **Synkroniser testtilfeller** for å skrive over oppgaveopptaket som er knyttet til testtilfellet i Azure DevOps, slik det er beskrevet i delen [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).
15. Åpne RSAT, og velg **Last inn** for å laste inn alle testtilfellene i testserien på nytt. Du må generere automatiserings- og parameterfilene for det aktuelle testtilfellet på nytt ved å velge testtilfellet og deretter **Ny \> Generer testkjøring og parameterfiler**, slik det er beskrevet i delen [Laste inn og kjøre testtilfeller](#load-and-run-test-cases).

    > [!NOTE]
    > Hvis du lot Excel-parameterfilen være åpen, mislykkes ny generering. Derfor må du kontrollere at Excel-parameterfilen for testtilfellet lukkes før du genererer den nye Excel-parameterfilen.

16. Velg **Rediger** for å åpne den nye Excel-parameterfilen. En ny **Lagret variabel**-oppføring vises på linje 9. Denne variabelen, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, lagres i XML-filen for oppgaveopptaket og kan brukes i senere tester.

    ![Lagret variabel-oppføringen](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Opprette et nytt testtilfelle

1. Gå til BPM-biblioteket **RSAT**.
2. Velg prosessen **Eksempel på støtteforretningsprosess**, og velg deretter **Redigeringsmodus** til høyre.
3. Endre verdien i **Navn**-feltet og **Beskrivelse**-feltet til **Frigi produkt**. Velg deretter **Lagre**.

    ![Navnet og beskrivelsen er endret til Frigi produkt](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Opprette et nytt oppgaveopptak som har en valideringsfunksjon

- Opprett et oppgaveopptak for å frigi produktet som ble opprettet tidligere, til den juridiske enheten USRT. Hvis du vil ha mer informasjon, kan du se delen [Opprette et oppgaveopptak og lagre det i BPM-biblioteket](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > Når det gjelder kjedede testtilfeller, anbefaler vi alltid at du finner eller filtrerer for posten du trenger, ved å *skrive inn verdien for feltet manuelt*. På den måten kan verktøyet fastsette posten som handlingen må utføres mot, i det etterfølgende testtilfellet.

    ![Nytt oppgaveopptak som har en valideringsfunksjon](./media/setup_rsa_tool_96.png)

    Som den foregående illustrasjonen viser, validerer du verdien i **Produktnummer**-feltet etter at produktet er funnet ved hjelp av hurtigfilteret, men før du velger **Frigi produkter**, for å kontrollere at produkt-ID-en er produkt-ID-en som ble opprettet tidligere. Du kan validere verdien ved å høyreklikke på **Produktnummer**-feltet og deretter velge **Oppgaveopptaker \> Valider \> Gjeldende verdi**.

    ![Validere gjeldende verdi](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Lagre oppgaveopptaket i BPM

1. Etter at oppgaveopptaket er fullført, velger du **Lagre i Lifecycle Services**.

    ![Lagre fullført oppgaveopptak i Lifecycle Services](./media/setup_rsa_tool_98.png)

2. Bibliotekinformasjon lastes inn fra LCS.

    ![Laste inn bibliotekinformasjon fra LCS](./media/setup_rsa_tool_99.png)

3. Velg BPM-biblioteket som oppgaveopptaket skal knyttes til. For denne opplæringen velger du BPM-biblioteket **RSAT** som ble opprettet tidligere, og forretningsprosessen **Frigi produkt** under det. Velg deretter **OK**.

#### <a name="sync-bpm-to-azure-devops"></a>Synkronisere BPM med Azure DevOps

1. Gå til BPM-biblioteket, og åpne **RSAT**-biblioteket.
2. Velg **VSTS-synkronisering** og deretter **Synkroniser testtilfeller**. Hvis du vil ha mer informasjon, kan du se delen [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).

    Etter at synkroniseringen er fullført, vises det nye arbeidselementet og det tilsvarende testtilfellet for forretningsprosessen **Frigi produkt** i Azure DevOps i **Tavler \> Arbeidselementer**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Legge til det nye testtilfellet i den eksisterende testserien

1. Gå til **Testplaner \> Testplaner**, og velg planen **RSAT-testplan**.
2. Velg **Legg til eksisterende**.
3. Velg **Kjør spørring** på siden **Legg til testtilfeller i serie**.
4. Velg det nye testtilfellet som ble opprettet for **Frigi produkt**, og velg deretter **Legg til testtilfeller** i nedre høyre hjørne på siden (denne knappen vises ikke i illustrasjonen nedenfor).

    ![Siden Legg til testtilfeller i serie](./media/setup_rsa_tool_100.png)

    Testserien har nå to testtilfeller.

    ![To testtilfeller i testserien](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Laste inn testtilfeller i RSAT

1. Åpne RSAT, og velg **Last inn**.
2. Testtilfellene lastes inn, og du får en advarsel om at denne handlingen skriver over Excel-testdatafiler, og at lokale endringer går tapt. Du blir også spurt om du vil fortsette. Velg **Ja** for å oppdatere Excel-parameterfiler i det lokale systemet, men ikke Excel-parameterfilene som ble lastet opp til Azure DevOps.

    ![Denne handlingen overskriver Excel-testdatafiler](./media/setup_rsa_tool_102.png)

    Begge testtilfellene lastes inn, sammen med Excel-parameterfilen for det første testtilfellet. Siden du valgte **Last opp** i den siste kjøringen, hentes parameterfilene fra Azure DevOps.

    ![Testtilfeller lastet inn](./media/setup_rsa_tool_103.png)

3. Velg bare det andre testtilfellet, og velg deretter **Ny \> Generer testkjøring og parameterfiler**.

#### <a name="edit-the-excel-parameter-file"></a>Redigere Excel-parameterfilen

1. Velg bare det andre testtilfellet, og velg deretter **Rediger** for å åpne den tilsvarende Excel-parameterfilen.
2. Kopier den lagrede variabelen **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (se delen [Endre et eksisterende oppgaveopptak for å opprette en lagret variabel](#modify-an-existing-task-recording-to-create-a-saved-variable)) fra det første testtilfellet til alle feltene der produktnummeret brukes. I dette tilfellet kopierer du variabelen til feltene **Produktnummer** og **Valider produktnummer** i arket **EcoResProductListPage**.

    ![Feltene Produktnummer og Valider produktnummer](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Variabler kan bare sendes mellom tester i den samme testkjøringen. Navnene på variablene må samsvare nøyaktig.

3. Velg **Lagre**, og lukk deretter Excel-arbeidsboken.
4. Velg **Last opp** for å lagre endringene du har gjort i Excel-parameterfilen.

#### <a name="run-the-chained-test-cases"></a>Kjøre kjedede testtilfeller

1. Velg begge testtilfellene, og velg deretter **Kjør**.
2. Kontroller at begge testtilfellene har bestått.

    ![Resultat-feltet satt til Bestått for begge testtilfeller](./media/setup_rsa_tool_105.png)
