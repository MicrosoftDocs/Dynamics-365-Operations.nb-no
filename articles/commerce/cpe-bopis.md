---
title: Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø
description: Dette emnet forklarer hvordan du konfigurerer "kjøp på nett, hent i butikk" (BOPIS) i et Microsoft Dynamics 365 Commerce-evalueringsmiljø etter at det er klargjort.
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 62dabaa2610341cc8ad8e85812a317ac3123fcb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414541"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer "kjøp på nett, hent i butikk" (BOPIS) i et Microsoft Dynamics 365 Commerce-evalueringsmiljø etter at miljøet er klargjort.

## <a name="prerequisite"></a>Forutsetning

Fullfør prosedyrene i dette emnet bare etter at evalueringsmiljøet i Commerce er klargjort og konfigurert. Hvis du vil ha informasjon om hvordan du klargjør og konfigurerer miljøet, kan du se [Klargjøre et Dynamics 365 Commerce-evalueringsmiljø](provisioning-guide.md) og [Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).

Når Commerce-miljøet er klargjort og konfigurert ende til ende, kan du bruke dette emnet til å aktivere BOPIS-scenarioer.

## <a name="configure-the-pos"></a>Konfigurere salgsstedet

### <a name="configure-modern-pos"></a>Konfigurere Modern POS

BOPIS -scenarier som involverer en kredittkortbetaling, krever en maskinvarestasjon. Maskinvarestasjonen er bygget inn i Modern POS for Windows- og Android-klienter. Hvis du bruker Cloud POS eller Modern POS for iOS, må salgsstedsklienten være forbundet med en delt maskinvarestasjon. Dette emnet beskriver hvordan du konfigurerer BOPIS for Windows- og Android-klienter. Hvis du vil ha informasjon om hvordan du installerer en delt maskinvarestasjonen, kan du se [Konfigurere og installere Retail Hardware Station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Kasser**.
2. Velg register **SANFRAN-5**, og velg deretter **Rediger**.
3. Endre verdien for feltet **Maskinvareprofil** fra **HW002** til **HW001**, og velg deretter **Lagre**.
4. Gå til **Detaljhandel og handel \> IT for Detaljhandel og handel \> Distribusjonsplan** for å synkronisere endringene.
5. Velg distribusjonsplanen **1090**, og velg deretter **Kjør nå** i handlingsruten.
6. Velg **Ja** og deretter **OK** for å starte datasynkronisering. 

### <a name="install-modern-pos"></a>Installere Modern POS

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Enheter**.
2. Velg enhet **SANFRANCIS-5**.
3. I Handlingsvinduet, velg **Last ned**, og velg deretter **Konfigrasjonsfil**.
4. Velg **Last ned**, og velg deretter **Retail Modern POS**. 
5. Når nedlastingen av **ModernPOSSetup.exe**-filen er fullført, velger du **Åpne fil**.

    ![Åpne fil](./dev-itpro/media/PAYMENTS/openfile.png)

6. Velg **Neste** for å gå gjennom installasjonsprosessen. Når installasjonen er fullført, velger du **Lukk**.

### <a name="activate-modern-pos"></a>Aktivere Modern POS

1. Velg **start**-knappen på Windows-skrivebordet, og skriv deretter inn **Retail Modern POS**.
2. Velg **Retail Modern POS**-programmet som skal initiere aktiveringen.
3. Velg **Neste**. Feltene **Server-URL**, **Enhets-ID** og **Kassenummer** skal være forhåndsutfylt ved hjelp av informasjon fra konfigurasjonsfilen du lastet ned i forrige prosedyre.
4. Velg **Aktiver**.
5. En godkjenningsdialogboks vises. Velg kontoen som bruker e-postadressen som tidligere var tilknyttet arbeider **000713 - Andrew Collette**.

    > [!NOTE]
    > Hvis du ennå ikke har knyttet til en arbeider med din identitet, vil ikke aktiveringen lykkes. I dette tilfellet følger du trinnene under "Knytt en arbeider til din identitet" i emnet [Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
6. Når du blir bedt om å gjøre det mulig for organisasjonen å administrere enheten, velger du **Bare denne appen**.
7. Når aktiveringen er fullført, velger du **Komme i gang**.

### <a name="enable-bopis-in-modern-pos"></a>Aktivere BOPIS i Modern POS

1. Logg inn på Modern POS ved å bruke **000713** som operatør-ID og **123** som passord.
2. Mens den innledende gjennomgangsvideoen spilles av, merker du av for de to avmerkingsboksene nederst i venstre hjørne i dialogboksen, og deretter lukker du dialogboksen.
3. Hvis du ikke blir bedt om å lukke skiftet, blar du til høyre på **velkomstsiden**, velger **Lukk skift** og logger deretter på POS.
4. Når du er logget på, velger du **Utfør en ikke-skuff-operasjon** når du blir bedt om det.
5. Rull til høyre på **velkomstsiden**, og velg operasjonen **Velg maskinvarestasjon**.
6. Velg **Behandle**, angi alternativet **Bruk maskinvarestasjon** til **På**, og velg deretter **OK**.
7. Logg av salgsstedet, og logg deretter på.
8. Når du er logget på, velger du **Åpne et nytt skift**, og deretter velger du **Skuff**.

## <a name="complete-a-bopis-scenario"></a>Fullføre et BOPIS-scenario

### <a name="create-a-storefront-order-for-in-store-pickup"></a>Opprette en butikkfasadeordre for henting i butikk

1. Gå til URL-adressen du angav i trinnet [Initialisere e-handel](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) under miljøkonfigurasjon.
2. Velg en vare, og velg **Legg til i handlevogn**.
3. På handlepose-siden velger du **Plukk opp dette** for ordrelinjen du nettopp la til.
4. I dialogboksen **Velg en butikk** angir du **San Francisco**, og deretter velger du **Søk**-knappen.
5. Finn San Francisco-butikken i resultatlisten, og velg **Plukk her**.
6. Velg **Utsjekking som gjest** på handlepose-siden. 

    > [!NOTE]
    > Du må godta informasjonskapselmeldingen for å fortsette med utsjekkingen. Denne merknaden vises som et banner øverst på betalingssiden.

7. Angi følgende detaljer for kredittkortbetalingsmåten:

    - **Navn på kortinnehaver:** Skriv inn et hvilket som helst navn.
    - **Kortnummer:** Angi **4111-1111-1111-1111**.
    - **Utløpsdato:** Angi **10/20**.
    - **Verdi for kortbekreftelse (CVV-kode):** Angi **737**.

    > [!IMPORTANT]
    > Du bør ikke prøve å bruke faktisk kredittkortinformasjon på testområdet under noen omstendigheter!

8. Fortsett med kassen ved å angi detaljer for faktureringsadressen, og velg deretter **Lagre og fortsett**.
9. Når ordren er klar til å plasseres, velger du **Utsjekking**.

### <a name="synchronize-online-orders-to-the-back-office"></a>Synkronisere elektroniske ordrer til Back Office

Hvis du vil ha informasjon om hvordan du synkroniserer elektroniske ordrer, kan du se [Postering av elektroniske salg og betalinger](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).

### <a name="pick-up-an-order-in-the-store"></a>Hente en ordre i butikken

1. Logg på salgsstedet.
2. På **velkomstskjermen** velger du **Ordreoppfyllelse**
3. I listen over varer for plukking velger du linjen fra bestillingen som ble lagt inn elektronisk.
4. Når ordrelinjen er valgt, velger du **Hent**.

    Linjeelementet legges til i transaksjonsskjermbildet, og **$0,00** vises som forfalt saldo.

5. Velg den forfalt saldoen **$0,00**, eller velg en hvilken som helst betalingsmåte for å fullføre transaksjonen.

## <a name="troubleshooting"></a>Feilsøking

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>Elektroniske ordrer som er hentet på salgsstedet, har en saldo som ikke er null

Når en ordre hentes for plukking i butikk og forfalt saldo ikke er 0 (null), må du kontrollere at det er brukt Modern POS og at maskinvarestasjonen er aktiv. Hvis Cloud POS eller Modern POS for iOS brukes, må du kontrollere at en delt maskinvarestasjon er aktiv. En form for aktiv maskinvarestasjon er nødvendig for å hente betalinger som ble gjort tilkoblet.

### <a name="general-issues-with-payment-capture"></a>Generelle problemer med betalingsregistrering

For alle generelle problemer bør du alltid se hendelsesloggene for maskinvarestasjoner i Modern POS eller Internet Information Services (IIS) som første trinn. Du finner disse loggene under følgende noder i Windows-hendelsesloggen:

- Program- og tjenestelogger \> Microsoft \> Dynamics \> Commerce-ModernPOS
- Program- og tjenestelogger \> Microsoft \> Dynamics \> Commerce-Hardware Station

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Klargjøre et evalueringsmiljø for Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce](cpe-optional-features.md)

[Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-webområde](https://aka.ms/Dynamics365CommerceWebsite)

[Betalingskobling for Ayden](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[Lagre betalingsmåter på nett med Adyen-koblingen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[Oversikt over betalinger for omnikanal](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
