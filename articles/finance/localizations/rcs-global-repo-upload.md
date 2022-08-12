---
title: Opprette ER-konfigurasjoner i RCS og laste dem opp til det globale repositoriet
description: Denne artikkelen forklarer hvordan du oppretter en konfigurasjon for elektronisk rapportering (ER) i Microsoft RCS (Regulatory Configuration Services) og laster den opp til det globale repositoriet.
author: JaneA07
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f73f7189ad82d85169a4e0df573dd26dab8bb009
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070608"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Opprette ER-konfigurasjoner i Regulatory Configuration Services (RCS) og laste dem opp til det globale repositoriet

[!include [banner](../includes/banner.md)]

Du kan bruke Microsoft Regulatory Configuration Services (RCS) til å utforme konfigurasjoner for elektronisk rapportering (ER) og publisere dem slik at de kan brukes i organisasjonen.

Fremgangsmåtene nedenfor forklarer hvordan en bruker i rollen systemansvarlig eller elektronisk rapportering kan opprette en avledet versjon av en ER-konfigurasjon som er konfigurert i en RCS-forekomst, og deretter laste opp den avledede konfigurasjonen til det globale repositoriet. 

Før du kan fullføre de prosedyrene, må du gjøre følgende:

- Ha tilgang til et RCS-miljø for din organisasjon.
- Opprett en aktiv konfigurasjonsleverandør og gjør den aktiv. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Du må kontrollere at det er klargjort et RCS-miljø for organisasjonen din. Hvis du ikke har en RCS-forekomst klargjort for organisasjonen, kan du gjøre det ved hjelp av følgende trinn:

1. I en økonomi- og driftsapp går du til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. I **Relaterte koblinger / Eksterne koblinger** velger du **Regulatory Services – Konfigurasjon**, og deretter følger du instruksjonene for **registrering** for å klargjøre.

Hvis et RCS-miljø allerede er klargjort for organisasjonen din, bruker du URL-adressen for siden til å få tilgang til den og velger deretter alternativet for **pålogging**.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Opprette en avledet versjon av en konfigurasjon i RCS

> [!NOTE]
> Hvis dette er første gang du har brukt RCS, vil du ikke ha noen konfigurasjon som er tilgjengelig for deg å avlede fra. Du må importere en konfigurasjon fra det globale repositoriet. For mer informasjon, se [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Logg på** RCS, og velg arbeidsområdet **Elektronisk rapportering**.
2. Kontroller at du har en aktiv konfigurasjonsleverandør for organisasjonen som er satt til aktiv (se forhåndskrav). 
3. Velg **Rapporteringskonfigurasjoner**.
4. Velg konfigurasjonen du vil avlede en ny versjon fra. Du kan bruke filtreringsfeltet over treet til å begrense søket.
5. Velg **Opprett konfigurasjon** \> **Avled fra navn**.
6. Angi et navn og en beskrivelse, og velg deretter **Opprett konfigurasjon** for å opprette en ny avledet versjon med statusen "Utkast".
7. Velg den nylig avledede konfigurasjonen, og gjør om nødvendig flere endringer i konfigurasjonsformatet. 
8. Når endringene er fullført, må du angi **Endre status** for konfigurasjonen til **Fullført** for å kunne publisere den i repositoriet. Velg **OK**.

![Ny konfigurasjonsversjon i RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Når konfigurasjonsstatusen endres, kan du få en valideringsfeilmelding som er knyttet til de tilkoblede appene. Hvis du vil deaktivere valideringen, velger du **Brukerparametere** i kategorien **Konfigurasjoner**, og deretter setter du alternativet **Hopp over validering ved konfigurasjonens statusendring og rebasering** til **Ja** 

## <a name="upload-a-configuration-to-the-global-repository"></a>Laste opp en konfigurasjon til det globale repositoriet

Hvis du vil dele en ny eller avledet konfigurasjon med organisasjonen, kan du laste den opp til det globale repositoriet ved å følge disse trinnene:

1. Velg den fullførte versjonen av konfigurasjonen, og velg deretter **Last opp til repositorium**.
2. Velg alternativet **Globalt (Microsoft)**, og velg deretter **Last opp**.

    ![Laste opp til alternativer for repositorium.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Velg **Ja** i bekreftelsesboksen. 
4. Oppdater beskrivelsen av versjonen etter behov, og velg deretter **OK**. Du kan også velge å laste opp versjonen til en tilkoblet app eller til et GIT-repositorium.  

Statusen for konfigurasjonen oppdateres til **Delt**, og konfigurasjonen lastes opp til det globale repositoriet. Det opprettes også en utkastversjon av konfigurasjonen du lastet opp, og den kan brukes hvis det kreves etterfølgende endringer.

Etter at konfigurasjonen er lastet opp til det globale repositoriet, kan du arbeide med den der på følgende måter:

- Importere den til Dynamics 365-forekomsten. Hvis du vil ha mer informasjon, kan du se [(ER) Importere konfigurasjoner fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Hvis du vil dele den med en tredjepart eller en ekstern organisasjon, kan du se [RCS Dele konfigurasjoner for elektronisk rapportering (ER) med eksterne organisasjoner](rcs-global-repo-share-configuration.md)

    ![Avledet versjon av Intrastat Contoso-konfigurasjon i det globale repositoriet.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Slette en konfigurasjon fra det globale repositoriet
Fullfør fremgangsmåten nedenfor for å slette en konfigurasjon som organisasjonen har opprettet.

1. I arbeidsområdet **Elektronisk rapportering** kontrollerer du at konfigurasjonsleverandøren er **Aktiv**. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Velg **repositorium** på den aktive konfigurasjonsleverandøren.
3. Velg lagertypen **Global**, og velg **Åpne**.
4. I hurtigfanen **Filter** finner du konfigurasjonen du vil slette, ved hjelp av **Filter**-funksjonaliteten.
5. I hurtigfanen **Versjon** velger du versjonen av konfigurasjonen du vil slette, og deretter velger du **Slett**:

    ![Slette en konfigurasjon fra det globale repositoriet.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Velg **Ja** i bekreftelsesboksen.

    ![Slette bekreftelsesmelding for konfigurasjonsversjon.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Konfigurasjonsversjonen blir slettet, og bekreftelsesmeldingen vises. 

> [!NOTE]
> Konfigurasjoner kan bare slettes av konfigurasjonsleverandøren som opprettet dem. Hvis konfigurasjonen er delt med en annen organisasjon, må du oppheve delingen av konfigurasjonen før du sletter den.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

