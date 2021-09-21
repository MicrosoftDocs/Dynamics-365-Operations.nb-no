---
title: Installer tillegget for lagersynlighet
description: Dette emnet beskriver hvordan du installerer tillegget for lagersynlighet for Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b2b85f533a3318701ed08857b899cf9bdd103863
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474826"
---
# <a name="install-and-set-up-inventory-visibility"></a>Installere og definere lagersynlighet

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Dette emnet beskriver hvordan du installerer tillegget for lagersynlighet for Microsoft Dynamics 365 Supply Chain Management.

Du må bruke Microsoft Dynamics Lifecycle Services (LCS) til å installere tillegget for lagersynlighet. LCS er en samarbeidsportal som gir et miljø og et sett med jevnlig oppdaterte tjenester som hjelper deg med å administrere applivssyklusen til Finance and Operations-appene dine.

Hvis du vil ha mer informasjon, se [Lifecycle Services-ressurser](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Forutsetninger for lagersynlighet

Før du kan installere lagersynlighet, må du gjøre følgende:

- Hent et LCS-implementeringsprosjekt der minst ett miljø er distribuert.
- Sørg for at forutsetningene for å definere tillegg er fullført. Hvis du vil ha mer informasjon om disse forutsetningene, kan du se [Oversikt over tillegg](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Lagersynlighet krever ikke kobling til dobbel skriving.
- Kontakt produktteamet til Lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å få følgende tre obligatoriske filer:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (hvis versjonen av Supply Chain Management du kjører, er eldre enn versjon 10.0.18)

> [!NOTE]
> Landene og regionene som for øyeblikket støttes, omfatter Canada (CCA, ECA), USA (WUS, EUS), EU (NEU, WEU), Storbritannia (SUK, WUK), Australia (EAU, SEAU), Japan (EJP, WJP) og Brasil (SBR, SCUS).

Hvis du har spørsmål om disse forutsetningene, kan du ta kontakt med produktteamet for lagersynlighet.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Konfigurere Dataverse

Hvis du vil konfigurere Dataverse slik at det kan brukes med Lagersynlighet, bruker du Package Deployer-verktøyet til å distribuere lagersynlighetspakken. Følgende underdeler beskriver hvordan du fullfører hver oppgave.

> [!NOTE]
> For øyeblikket støttes kun Dataverse-miljøer som ble opprettet ved hjelp av LCS. Hvis Dataverse-miljøet ble opprettet på en annen måte (for eksempel ved å bruke Power Apps-administrasjonssenteret), og hvis det er koblet til Supply Chain Management-miljøet ditt, må du først kontakte produktgruppen i Lagersynlighet for å løse tilordningsproblemet. Du kan deretter installere Lagersynlighet.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Migrer fra en gammel versjon av Dataverse-løsningen

Hvis du har installert en eldre versjon av Lagersynlighet-løsningen for Dataverse, bruker du disse instruksjonene til å oppdatere versjonen. Det finnes to tilfeller:

- **Tilfelle 1:** Hvis du har konfigurert Dataverse manuelt ved å importere `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip`-løsningen, følger du denne fremgangsmåten:

    1. Last ned følgende tre filer:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Importer `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` og `InventoryServiceBase_managed.cab` manuelt i Dataverse ved å følge disse trinnene:

        1. Åpne URL-adressen for Dataverse-miljøet.
        1. Åpne siden **Løsninger**.
        1. Velg **Import**.

    1. Bruk Package Deployer-verktøyet til å distribuere `InventoryServiceApplication.PackageDeployer.zip`-pakken. Hvis du vil ha instruksjoner, kan du se [Bruke Package Deployer-verktøyet til å distribuere pakken](#deploy-package) senere i dette emnet.

- **Tilfelle 2:** Hvis du konfigurerte Dataverse ved hjelp av Package Deployer-verktøyet før du installerte den eldre `.*PackageDeployer.zip`-pakken, må du laste ned `InventoryServiceApplication.PackageDeployer.zip` og foreta en oppdatering. Hvis du vil ha instruksjoner, kan du se [Bruke Package Deployer-verktøyet til å distribuere pakken](#deploy-package).

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Bruk Package Deployer-verktøyet til å distribuere pakken.

1. Installer utviklerverktøyene som beskrevet i [Nedlastingsverktøy fra NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
1. Fjern blokkeringen for filen `InventoryServiceApplication.PackageDeployer.zip` du lastet ned fra Teams-gruppen, ved å følge disse trinnene:

    1. Velg og hold (eller høyreklikk på) på filen, og velg deretter **Egenskaper**.
    1. I dialogboksen **Egenskaper**, på **Generelt**-fanen, finner du **Sikkerhet**-delen. Velg **Fjern blokkering**, og ta i bruk endringen. Hvis det ikke finnes noen **Sikkerhet**-del på **Generelt**-fanen, er filen ikke blokkert. I dette tilfellet går du videre til neste trinn.

    ![Fjern blokkeringen for den nedlastede filen](media/unblock-file.png "Fjern blokkeringen for den nedlastede filen")

1. Pakk ut `InventoryServiceApplication.PackageDeployer.zip`, der du finner følgende elementer:

    - `InventoryServiceApplication`-mappe
    - `[Content_Types].xml`-fil
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`-fil

1. Kopier hvert av disse elementene til `.\Tools\PackageDeployment`-katalogen. (Denne katalogen ble opprettet da du installerte utviklerverktøyene.)
1. Kjør `.\Tools\PackageDeployment\PackageDeployer.exe`, og følg instruksjonene på skjermen for å importere løsningene.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Installer tillegget for lagersynlighet

Før du installerer tillegget, må du registrere en app og legge til en klienthemmelighet i Azure Active Directory (Azure AD) under Azure-abonnementet ditt. Hvis du vil ha instruksjoner, kan du se [Registrer en app](/azure/active-directory/develop/quickstart-register-app) og [Legg til en klienthemmelighet](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Skriv ned verdiene for **App-ID (klient)**, **Klienthemmelighet** og **Leier-ID**, siden du trenger dem senere.

Når du har registrert en app og lagt til en klienthemmelighet i Azure AD, følger du denne fremgangsmåten for å installere tillegget for lagersynlighet.

1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index).
1. På hjemmesiden velger du prosjektet der miljøet er distribuert.
1. På prosjektsiden velger du miljøet du vil installere tillegget i.
1. På miljøsiden ruller du ned til du ser delen delen **Miljøtillegg** i delen **Power Platform-integrering**. Der kan du finne Dataverse-miljønavnet.
1. I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.

    ![Miljøsiden i LCS](media/inventory-visibility-environment.png "Miljøsiden i LCS")

1. Velg koblingen **Installer et nytt tillegg**. En liste over tilgjengelige tillegg vises.
1. Velg **Lagersynlighet** i listen.
1. Angi følgende felter for miljøet:

    - **ID for AAD-app (klient)** – Angi ID-en for Azure AD-appen du opprettet og noterte ned tidligere.
    - **ID for AAD-leier** – Angi leier-ID-en du noterte tidligere.

    ![Siden Konfigurer tillegg](media/inventory-visibility-setup.png "Siden Konfigurer tillegg")

1. Godta vilkåret og betingelsen ved å merke av for **Vilkår og betingelser**.
1. Velg **Installer**. Statusen for tillegget vises som **Installerer**. Når installasjonen er fullført, oppdaterer du siden. Statusen skal endres til **Installert**.

> [!IMPORTANT]
> Hvis du har mer enn ett LCS-miljø, oppretter du et annet Azure AD program for hvert miljø. Hvis du bruker samme program-ID og leie-ID til å installere tillegget for lagersynlighet for forskjellige miljøer, vil det oppstå et tokenproblem for eldre miljøer. Bare den siste som ble installert, vil være gyldig.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Avinstaller tillegget for lagersynlighet

Hvis du vil avinstallere tillegget for lagersynlighet, velger du **Avinstaller** på LCS-siden. Avinstalleringsprosessen avslutter tillegget for lagersynlighet, fjerner registreringen av tillegget fra LCS og sletter alle midlertidige data som er lagret i hurtigbufferen i tillegget for lagersynlighet. De primære lagerdataene som er lagret i Dataverse-abonnementet, slettes imidlertid ikke.

Hvis du vil avinstallere lagerdata som er lagret i Dataverse-abonnementet, åpner du [Power Apps](https://make.powerapps.com), velger **Miljø** på navigasjonslinjen og velger Dataverse-miljøet som er knyttet til LCS-miljøet. Deretter går du til **Løsninger** og sletter følgende fem løsninger:

- Forankringsløsning for lagersynlighetsapp i Dynamics 365-løsninger
- Løsning for lagersynlighetsapper i Dynamics 365 FNO SCM
- Konfigurasjon av lagertjeneste
- Frittstående versjon av Lagersynlighet
- Basisløsning for lagersynlighet i Dynamics 365 FNO SCM

Når du har slettet disse løsningene, blir dataene som er lagret i tabeller, også slettet.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Definere lagersynlighet i Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Distribuere integreringspakken for lagersynlighet

Hvis du kjører Supply Chain Management versjon 10.0.17 eller tidligere, kan du kontakte kundestøttegruppen for lagersynlighet på [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) for å hente pakkefilen. Deretter distribuerer du pakken i LCS.

> [!NOTE]
> Hvis det oppstår en versjonsfeil under distribusjon, må du importere X++-prosjektet til utviklingsmiljøet manuelt. Opprett deretter den distribuerbare pakken i utviklingsmiljøet, og distribuer den i produksjonsmiljøet.
>
> Koden er inkludert i Supply Chain Management versjon 10.0.18. Hvis du kjører den versjonen eller senere, er det ikke nødvendig å distribuere påkrevd distribusjon.

Sørg for at følgende funksjoner er aktivert i miljøet i Supply Chain Management. (De er som standard aktiverte.)

| Funksjonsbeskrivelse | Kodeversjon | Veksle klasse |
|---|---|---|
| Aktivere eller deaktivere bruk av lagerdimensjoner i InventSum-tabell      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Aktivere eller deaktivere bruk av lagerdimensjoner i InventSumDelta-tabell | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Definer integrering av lagersynlighet

Når du har installert tillegget, forbereder du Supply Chain Management-systemet slik at du kan arbeide med det ved å gjøre følgende:

1. I Supply Chain Management åpner du arbeidsområdet **[Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og aktiverer følgende funksjoner:
    - *Integrering av lagersynlighet* – Obligatorisk.
    - *Integrering av lagersynlighet med motpostering av reservasjon* – Anbefales, men valgfritt. Krever versjon 10.0.22 eller nyere. Hvis du vil ha mer informasjon, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

1. Gå til **Lagerstyring \> Oppsett \> Parametere for integrering av lagersynlighet**.
1. Åpne kategorien **Generelt**, og gjør følgende innstillinger:
    - **Endepunkt for lagersynlighet** – Angi URL-adressen til miljøet der du kjører Lagersynlighet. Hvis du ønsker mer informasjon, se [Finn endepunkt for tjeneste](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maksimalt antall poster i en enkelt forespørsel** – Angi til det maksimale antallet poster som skal inkluderes i en enkelt forespørsel. Du må angi et positivt heltall som er mindre enn eller lik 1 000. Standardverdien er 512. Vi anbefaler på det sterkeste at du ikke beholder standardverdien med mindre du har mottatt råd fra Microsoft Kundestøtte eller på annen måte er sikker på at du må endre den.

1. Hvis du aktiverte den valgfrie funksjonen *Integrering av lagersynlighet med motpostering av reservasjon*, åpner du fanen **Motpostering av reservasjon** og gjør følgende innstillinger:
    - **Aktiver motpostering av reservasjon** – Sett til *Ja* for å aktivere denne funksjonaliteten.
    - **Motposteringsmodifikator for reservasjon** – Velg lagertransaksjonsstatusen som motposterer reserveringer som gjøres i lagersynligheten. Denne innstillingen bestemmer ordrebehandlingsstadiet som utløser motregninger. Fasen spores etter ordrens lagertransaksjonsstatus. Velg ett av følgende:
        - *I ordre/bestilling* – Når det gjelder statusen *I transaksjon*, sender en ordre en motposteringsforespørsel når den opprettes. Motposteringsantallet vil være antallet i den opprettede ordren.
        - *Reserver* – For statusen *Reserver bestilt transaksjon* sender en ordre en motforespørsel når den er reservert, plukket, følgeseddelpostert eller fakturert. Forespørselen utløses bare én gang, for første trinn når den nevnte prosessen inntreffer. Motposteringsantallet vil være antallet der lagertransaksjonsstatusen endres fra *I ordre/bestilling* til *Reservert av bestilt* (eller senere status) på den tilsvarende ordrelinjen.

1. Gå til **Lagerstyring \> Periodisk \> Integrering av lagersynlighet** og aktiver jobben. Alle lagerendringshendelser fra Supply Chain Management posteres nå til Lagersynlighet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
