---
title: Regulatory Configuration Services (RCS) – globaliseringsfunksjoner
description: Dette emnet forklarer hvordan du bruker Microsoft RCS (Regulatory Configuration Services) og det globale repositoriet for å opprette og bruke globaliseringstjenester.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446304"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Services (RCS) – globaliseringsfunksjoner

[!include [banner](../includes/banner.md)]

Du kan bruke RCS (Microsoft Regulatory Configuration Services) til å opprette en globaliseringsfunksjon som kan brukes i globaliseringstjenester som for eksempel en e-faktureringstjeneste. Med RCS kan du utføre disse oppgavene:

- Definere relaterte komponenter for en funksjon.
- Administrere funksjonens livssyklus via statusen til en funksjon.
- Gjøre en funksjon tilgjengelig for definerte miljøer.
- Dele en funksjon med andre organisasjoner.

Fremgangsmåtene nedenfor forklarer hvordan en bruker i RCS kan legge til en globaliseringsfunksjon og relaterte komponenter, oppdatere funksjonens status og gjøre funksjonen tilgjengelig slik at den kan brukes i globaliseringstjenester.

Før du fullfører prosedyrene, må du fullføre trinnene som gjelder for følgende oppgaver:

- Åpne en RCS-forekomst.
- Opprette og aktivere en konfigurasjonsleverandør. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

I Finance and Operations-appforekomster følger du denne fremgangsmåten.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. Hvis et RCS-miljø ikke er klargjort for firmaet ditt, velger du **Regulatory Services – Konfigurasjon**, og deretter følger du instruksjonene for å klargjøre et miljø.

> [!NOTE]
> Hvis et RCS-miljø allerede er klargjort for ditt firma, bruker du URL-adressen for siden til å få tilgang til miljøet ved å velge alternativet for pålogging.

## <a name="turn-on-the-globalization-features"></a>Aktivere globaliseringsfunksjonene

1. I RCS-forekomsten velger du **Funksjonsbehandling**-flisen.
2. I **Funksjonsbehandling**-arbeidsområdet velger du **Globaliseringsfunksjoner** i listen, og deretter velger du **Aktiver nå**.

    ![Globaliseringsfunksjoner i funksjonsbehandling](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globaliseringsfunksjoner

Hvis du vil bruke en globaliseringsfunksjon, må du først importere den fra det globale repositoriet og opprette din egen versjon av den. Det finnes to måter å legge til globaliseringsfunksjoner på:

- Legg til en avledet funksjon som er basert på en eksisterende funksjon som er publisert eller delt.
- Legg til en ny funksjon som du har opprettet fra grunnen av.

## <a name="access-globalization-features"></a>Få tilgang til globaliseringsfunksjoner

1. Kontroller at **Globaliseringsfunksjoner** er aktivert i Funksjonsbehandling, som beskrevet tidligere i dette emnet.
2. Åpne det nye arbeidsområdet for **Globaliseringsfunksjoner**, gå til **Funksjoner** og velg flisen **E-fakturering**.

    ![Arbeidsområde for globale funksjoner](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    Siden **E-faktureringsfunksjoner** er åpen.

    ![E-faktureringsfunksjoner-siden](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Legg til en avledet globaliseringsfunksjon

Du kan legge til en ny globaliseringsfunksjon ved å avlede den fra en eksisterende funksjon som er publisert eller delt.

1. Velg **Importer** for å åpne **Importer en funksjon fra et global repositorium**-siden.

    ![Importer en funksjon fra en global repositoriumsside](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Velg **Synkroniser** for å få de nyeste funksjonene.

    Den synkroniserte listen inneholder funksjoner som er tilgjengelige for deg, enten fordi de er publisert av Microsoft eller fordi de ble delt med deg av en annen konfigurasjonsleverandør.

    ![Synkronisert liste over funksjoner](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. I listen velger du funksjonene som skal importeres, og deretter velger du **Importer**. Du får en melding når de valgte funksjonene er importert.

    ![Melding om vellykket importering](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Velg **Legg til**, og merk deretter av for **Basert på eksisterende versjon** i rullegardinmenyen i dialogboksen.
5. Angi et navn og en beskrivelse for funksjonen.
6. Velg den grunnleggende versjonen av funksjonen i listen over tilgjengelige funksjoner, og velg deretter **Opprett funksjon**.

    ![Legge til en avledet funksjon](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Funksjonen du la til, er opprettet og har statusen **Utkast**.

    ![En avledet funksjon som har Utkast-status](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Gå gjennom funksjonskomponentene for å finne ut om oppdateringer kreves:

    - Gå gjennom konfigurasjonene i tilfelle du må tilpasse formatene for elektronisk rapportering (ER) og binde dem sammen med formattilordninger for funksjonsversjonen.
    - Gå gjennom oppsettet i tilfelle du trenger å tilpasse **Handlinger**-kategorien, **Gyldighetsregler**-kategorien eller **Variabler**-kategorien for funksjonsversjonen.

8. I **Versjoner**-kategorien velger du en **Gyldig fra**-dato, og angir en beskrivelse hvis **Beskrivelse**-feltet er tomt.
9. Velg **Endre status** for å fullføre funksjonen. Fullførte funksjoner kan gjøres tilgjengelige for et bestemt miljø, slik at de kan brukes i globaliseringstjenester, eller de kan publiseres til det globale repositoriet.

> [!NOTE]
> Funksjoner som har **Funksjonsversjonstatus**-verdien **Publisert**, kan deles med eksterne organisasjoner.

## <a name="add-a-new-globalization-feature"></a>Legge til en ny globaliseringsfunksjon

Du kan legge til en ny globaliseringsfunksjon ved å opprette den fra grunnen av.

1. På **Importer funksjon fra globalt repositorium**-siden velger du **Legg til**, og velger deretter **Ny funksjon**-alternativet i rullegardinmenyen for dialogboksen.
2. Angi et navn og en beskrivelse for funksjonen.
3. Velg **Opprett funksjon**.

    ![Legge til en ny funksjon](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. I **Versjoner**-kategorien velger du en **Gyldig fra**-dato, og deretter velger du **Endre status** for å fullføre funksjonen. Fullførte funksjoner kan gjøres tilgjengelige for et bestemt miljø, slik at de kan brukes i globaliseringstjenester, eller de kan publiseres til det globale repositoriet.

> [!NOTE]
> Funksjoner som har **Funksjonsversjonstatus**-verdien **Publisert**, kan deles med eksterne organisasjoner.

## <a name="feature-component-overview"></a>Oversikt over funksjonskomponent

Globaliseringsfunksjoner består av flere komponenter:

- **Versjon** – denne komponenten støtter administrasjon av funksjonens livssyklus og lar brukere administrere statusen for ulike versjoner av funksjonen.
- **Konfigurasjoner** – Ved hjelp av denne komponenten kan brukere behandle, vise og redigere relaterte ER-formater og formattilordninger.
- **Oppsett** – denne komponenten gjør det mulig for brukere av globaliseringstjenester, for eksempel en e-faktureringstjeneste, å styre oppsettet av den relaterte funksjonsversjonen. Derfor støtter den den fleksible konstruksjonen av kommunikasjons- og svarregler.
- **Miljø** – med denne komponenten kan brukere av globaliseringstjenester som for eksempel en e-faktureringstjeneste, administrere miljøet der funksjonsversjonsoppsettet brukes, og gi godkjenning til brukerne som skal ha tilgang til det.
- **Organisasjoner** – denne komponenten gjør det mulig for brukere å dele funksjonen med eksterne organisasjoner.

## <a name="configuring-feature-components"></a>Konfigurere funksjonskomponenter

### <a name="version-and-status"></a>Versjon og status

Versjonen brukes til å administrere globaliseringsfunksjonens livssyklus.

Statusen kan endres i **Status**-feltet i **Versjon**-kategorien. Følgende statuser er tilgjengelige:

- **Utkast** – funksjonen kan bare redigeres når den er i denne statusen.
- **Fullført** – funksjonen og alle relaterte komponenter er sluttført (fullført), og kan ikke redigeres.
- **Publisert** – funksjonen og alle relaterte komponenter har blitt publisert til det globale repositoriet.
- **Delt** – funksjonen og alle relaterte komponenter er delt med eksterne organisasjoner.
- **Aktivert** – funksjonen og alle relaterte komponenter har blitt aktivert for bruk i en globaliseringstjeneste som for eksempel en e-faktureringstjeneste.

> [!NOTE]
> Funksjoner må gå sekvensielt gjennom noen av disse statusene. Derfor er kanskje ikke hver enkelt status tilgjengelig for hvert eneste stadium i livssyklusen.

### <a name="configurations"></a>Konfigurasjoner

Følgende handlinger er tilgjengelige for konfigurasjoner:

- **Vis** – Vis de underliggende funksjonskonfigurasjonene som ikke krever noen oppdatering.
- **Rediger** – Opprett en utkastversjon av en valgt konfigurasjon slik at du kan redigere formatet eller formattilordningen i Formatutforming-programmet.
- **Slett** – Slett en valgt konfigurasjon fra funksjonen.
- **Rebaser** – baser funksjonen på nytt. Hvis du vil ha mer informasjon, kan du se [Rebasere avledede globaliseringsfunksjoner](#rebase)-delen senere i dette emnet.

### <a name="setups"></a>Oppsett

Følgende handlinger er tilgjengelige for konfigurasjon av funksjoner:

- **Legg til** – Opprett en ny funksjonskonfigurasjon. Dette funksjonsoppsettet kan avledes fra et eksisterende funksjonsoppsett eller opprettes fra bunnen av.
- **Slett** – Slett en valgt funksjonskonfigurasjon.
- **Vis** – Vis et underliggende funksjonsoppsett som ikke krever noen endringer.
- **Rediger** – Opprett, slett eller endre attributtene for de tre hovedkomponentene i et funksjonsoppsett:

    - Handlinger og parametrene deres
    - Relevansregler
    - Variabler

![Konfigurasjonsside for funksjonsversjon](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Miljøer

Følgende handlinger er tilgjengelige for miljøer:

- **Aktiver** – for en valgt funksjonsversjon velger du et publisert miljø, og velger en **Gyldig fra**-dato når den skal være tilgjengelig. Hvis du vil ha mer informasjon, kan du se [Konfigurere miljøer for aktivering](#configureenvironment)-delen senere i dette emnet.
- **Avbryt** – Fjern et miljø for et funksjonsoppsett.

### <a name="organizations"></a>Organisasjoner

Følg disse trinnene for å dele en globaliseringsfunksjon med en ekstern organisasjon.

1. På **E-faktureringsfunksjoner**-siden velger du funksjonen og funksjonsversjonen som skal deles.
2. I **Organisasjoner**-kategorien velger du **Del med**, og angir deretter organisasjonens domenenavn i rullegardinmenyen for dialogboksen.
3. Velg **Del**.

    ![Dele en funksjon med en organisasjon](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Funksjonen deles med den valgte organisasjonen, og er tilgjengelig for den organisasjonen i det globale repositoriet. Derfra kan funksjonen importeres til organisasjonens forekomst av RCS eller Dynamics 365 Finance, slik at den kan brukes.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Rebaser avledede globaliseringsfunksjoner

Du kan rebasere en avledet globaliseringsfunksjon til den nye eller oppdaterte basefunksjonsversjonen. På denne måten kan endringer som er utført i baseversjonen, oppdateres automatisk. Den oppdaterte basefunksjonsversjonen opprettes av den opprinnelige konfigurasjonsleverandøren, og den blir deretter publisert eller delt.

![Oppdatert grunnleggende funksjonsversjon](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Hvis du for eksempel vil rebasere den avledede versjonen av en funksjon du har opprettet, får du først den siste versjonen av funksjonen ved å importere den fra det globale repositoriet.

1. På siden **E-faktureringsfunksjoner** velger du **Importer**.
2. Velg **Synkroniser** for å få de nyeste funksjonene.
3. I listen over funksjoner velger du funksjonene som skal importeres, og deretter velger du **Importer**.

    ![Importere den nyeste versjonen av en funksjon](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. I listen over funksjoner velger du funksjonen som skal rebaseres.
5. I **Versjon**-kategorien velger du **Ny** for å opprette en utkastversjon.

    ![Ny utkastversjon opprettet](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Velg **Rebaser**.
7. I **Rebaser**-dialogboksen velger du den siste versjonen av funksjonen du vil rebasere til.

    ![Dialogboksen Rebaser](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Velg **OK**.
9. Se gjennom funksjonskomponentene, og foreta eventuelle endringer etter behov.
10. Velg **Endre status** for å fullføre den rebaserte funksjonen. Når rebaseringen er fullført, kan du utføre flere handlinger. Du kan for eksempel publisere funksjonen og gjøre den tilgjengelig for bruk i globaliseringstjenester.

    ![Funksjonsstatusen oppdateres til Fullført](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Konfigurere miljøer for globaliseringsfunksjoner

Brukere av globaliseringstjenester kan styre miljøet for å definere en globaliseringsfunksjon og gi autorisasjon til andre brukere som får tilgang til den.

1. I **Globaliseringsfunksjoner**-arbeidsområdet, under **Miljøer**, velger du flisen **E-fakturering**.

    ![Arbeidsområde for globaliseringsfunksjoner](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Velg **Nøkkelhvelv-parametere** og deretter **Ny** for å opprette en hemmelighet for Azure Nøkkelhvelv.
3. Angi et navn og en beskrivelse for Nøkkelhvelv, gå til **URI for nøkkelhvelv**-feltet og angi URL-adressen som identifiserer Nøkkelhvelv-ressursen i Azure.
4. I **Sertifikater**-hurtigkategorien velger du **Legg til** for å legge til sertifikatet, og skriv deretter inn et navn og en beskrivelse for hvert sertifikat.

    ![Sertifikat lagt til](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Velg **Ny** for å opprette et nytt miljø.
6. Angi et navn, en beskrivelse og tokenet for signaturkode for delt tilgang som kreves for å lagre.
7. I **Brukere**-hurtigkategorien velger du **Ny** for å legge til en bruker som skal ha tilgangstillatelse til dette miljøet.
8. Angi brukerens bruker-ID og e-postadresse.
9. Gjenta trinn 7 og 8 for å legge til flere brukere.
10. Velg **Publiser** for å publisere miljøet.

    ![Publisert miljø](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]