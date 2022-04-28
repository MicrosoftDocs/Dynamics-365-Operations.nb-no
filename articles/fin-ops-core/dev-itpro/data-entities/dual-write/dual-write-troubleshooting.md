---
title: Generell feilsøking
description: Dette emnet inneholder generell feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/07/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 8b5951f9f40179ca0bf31f5cccf1f05a0f968213
ms.sourcegitcommit: 1843235766b6f8cf950a13a310e9f4f2f53c59a4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/07/2022
ms.locfileid: "8554606"
---
# <a name="general-troubleshooting"></a>Generell feilsøking

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder generell feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Dataverse.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivere og vise plugin-sporingsloggen i Dataverse for å vise feildetaljer

Sporingslogger kan være nyttige ved feilsøking av direkte synkroniseringsproblemer med dobbel skriving mellom Finance & Operations og Dataverse. Loggene kan gi spesifikke detaljer til teamene som yter teknisk støtte og konstruksjonsstøtte for Dynamics 365. Denne artikkelen beskriver hvordan du aktiverer sporingslogger og hvordan du viser dem. Sporingslogger administreres på Innstillinger-siden i Dynamics 365 og krever rettigheter på administratornivå for å endre og vise dem. 

**Nødvendig rolle for å aktivere sporingsloggen og vise feil**: Systemadministrator

### <a name="turn-on-the-trace-log"></a>Aktiver sporingsloggen
Følg denne fremgangsmåten for å aktivere sporingsloggen.

1.  Logg på Dynamics 365, og velg deretter **Innstillinger** i det øverste navigasjonsfeltet. På Systemer-siden klikker du på **Administrasjon**.
2.  På Administrasjon-siden klikker du på **Systeminnstillinger**.
3.  Velg fanen og programtillegget **Tilpassing**, gå til delen for sporing av egendefinert arbeidsflytaktivitet og endre rullegardinmenyen til **Alle**. Dette vil spore alle aktiviteter og gir et omfattende sett med data for teamene som må gå gjennom potensielle problemer.

> [!NOTE]
> Hvis du setter rullegardinlisten til **Unntak**, leveres det kun sporingsinformasjon når det forekommer unntak (feil).

Når dette er aktivert, vil sporingsloggene for programtillegget fortsette å samles inn til de slås av manuelt ved å gå tilbake til denne plasseringen og velge **Av**.

### <a name="view-the-trace-log"></a>Vis sporingsloggen
Følg denne fremgangsmåten for å se sporingsloggen.

1. På Innstillinger-siden i Dynamics 365 velger du **Innstillinger** i det øverste navigasjonsfeltet. 
2. Velg **Sporingslogg for programtillegg** i delen **Tilpassinger** på siden.
3. Du finner oppføringer i listen over sporingslogger, basert på typenavn og/eller meldingsnavn.
4. Åpne ønsket oppføring for å vise hele loggen. Meldingsblokken i kjøringsdelen vil gi tilgjengelig informasjon for programtillegget. Hvis tilgjengelig, blir det også gitt unntaksdetaljer. 

Du kan kopiere innholdet i sporingsloggene og lime dem inn i et annet program som Notisblokk eller andre verktøy for å vise logger eller tekstfiler slik at du lettere kan se alt innholdet. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktiver feilsøkingsmodus for å feilsøke problemer med direkte synkronisering i økonomi- og driftsapper

**Nødvendig rolle for å vise feilene:** Systemadministrator

Dobbel skriving-feil som kommer fra Dataverse, kan vises i økonomi- og driftsappen. Du kan aktivere detaljert logging for feil ved å følge disse trinnene:

1. For alle prosjektkonfigurasjoner i økonomi- og driftsapper finnes det et **IsDebugMode**-flagg i **DualWriteProjectConfiguration**-tabellen.
2. Åpne **DualWriteProjectConfiguration** ved hjelp av Excel-tillegget. Hvis du vil bruke tillegget, aktiverer du utformingsmodus i Excel-tillegget for økonomi og drift og legger til **DualWriteProjectConfiguration** i arket. Hvis du vil ha mer informasjon, kan du se [Vis og oppdater enhetsdata med Excel](../../office-integration/use-excel-add-in.md).
3. Sett **IsDebugMode** til **Ja** i prosjektet.
4. Kjør scenariet som genererer feil.
5. De detaljerte loggene lagres i tabellen **DualWriteErrorLog**.
6. Hvis du vil slå opp data i tabelleseren, bruker du følgende kobling: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog` og erstatter `999` etter behov.
7. Oppdater på nytt etter [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), som er tilgjengelig for plattformoppdatering 37 og senere. Hvis du har denne reparasjonen installert, vil feilsøkingsmodusen registrere flere logger.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Kontroller synkroniseringsfeil på den virtuelle maskinen for økonomi- og driftsappen

**Nødvendig rolle for å vise feilene:** Systemadministrator

1. Logg på Microsoft Dynamics Lifecycle Services (LCS).
2. Åpne LCS-prosjektet du har valgt til å utføre testing av dobbel skriving for.
3. Velg flisen **Skybaserte miljøer**.
4. Bruk Eksternt skrivebord for å logge på den virtuelle maskinen for økonomi- og driftsappen. Bruk den lokale kontoen som vises i LCS.
5. Åpne hendelseslisten.
6. Velg **Program- og tjenestelogger \> Microsoft \> Dynamics \> AX-DualWriteSync \> Drift**.
7. Se gjennom listen over nylige feil.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Landingsside i grensesnitt for dobbel skriving som viser tomt
Når du åpner siden for dobbel skriving i Microsoft Edge eller i nettleseren Google Chrome, lastes ikke hjemmesiden, og du ser en tom side eller en feil som for eksempel "Noe gikk galt".
I Devtools vises det en feil i konsolloggene:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: Kan ikke lese egenskapen 'sessionStorage' fra 'Window': Tilgang nektes for dette dokumentet. ved t.storeInSessionStorage (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860) ved new t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103) ved ci (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115) ved Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728) ved jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191) ved Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692) ved Or (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076) ved Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750) ved vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130) ved hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151)

Grensesnittet bruker nettleserens øktlagring til å lagre noen egenskapsverdier for lasting av hjemmesiden. For at dette skal fungere, må informasjonskapsler fra tredjeparter være tillatt i nettleseren for området. Feilen angir at grensesnittet ikke får tilgang til øktlagringen. Det kan vøre to scenarioer der dette problemet oppstår:

1.  Du åpner grensesnittet i inkognitomodus i Edge/Chrome, og informasjonskapsler fra tredjeparter i inkognito er blokkert.
2.  Du har blokkert informasjonskapsler fra tredjeparter fullstendig i Edge/Chrome.

### <a name="mitigation"></a>Reduksjon
Informasjonskapsler fra tredjeparter må være tillatt i nettleserinnstillingene.

### <a name="google-chrome-browser"></a>Google Chrome-nettleseren
Første alternativ:
1.  Gå til innstillingene ved å skrive inn chrome://settings/ i adresselinjen, og naviger deretter til Personvern og sikkerhet -> Informasjonskapsler og andre områdedata.
2.  Velg "Tillat alle informasjonskapsler". Hvis du ikke ønsker å gjøre dette, velger du det andre alternativet.

Andre alternativ:
1.  Gå til innstillingene ved å skrive inn chrome://settings/ i adresselinjen, og naviger deretter til Personvern og sikkerhet -> Informasjonskapsler og andre områdedata.
2.  Hvis "Blokker informasjonskapsler fra tredjeparter i Inkognito" eller "Blokker informasjonskapsler fra tredjeparter" er valgt, går du til "Nettsteder som alltid kan bruke informasjonskapsler", og klikker på **Legg til**. 
3.  Legg til navnet på nettstedet for økonomi- og driftsappene dine - https://<your_FinOp_instance>.cloudax.dynamics.com. Merk av for "Alle informasjonskapsler, kun på dette nettstedet". 

### <a name="microsoft-edge-browser"></a>Microsoft Edge-nettleseren
1.  Gå til Innstillinger -> Områdetillatelser -> Informasjonskapsler og områdedata.
2.  Slå av "Blokker informasjonskapsler fra tredjeparter".  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Fjern tilknytningen til og koble til et annet Dataverse-miljø fra en økonomi- og driftsapp

**Nødvendig rolle for å koble fra miljøet:** Systemansvarlig for enten økonomi- og driftsappen eller Dataverse.

1. Logg på økonomi- og driftsappen.
2. Gå til **Arbeidsområder \> Databehandling**, og velg flisen **Dobbel skriving**.
3. Velg alle kjørende tilordninger, og klikk på **Stopp**.
4. Klikk på **Koble fra miljø**.
5. Velg **Ja** for å bekrefte operasjonen.

Du kan nå koble til et nytt miljø.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Kan ikke vise informasjonsskjemaet for salgsordrelinjen 

Når du oppretter en salgsordre i Dynamics 365 Sales, kan du bli omdirigert til ordrelinjeskjemaet for Dynamics 365 Project Operations hvis du klikker på **+ Legg til produkter**. Det finnes ingen måter fra dette skjemaet å vise **Informasjon**-skjemaet for salgsordrelinje. Alternativet for **Informasjon** vises ikke i rullegardinlisten under **Ny ordrelinje**. Dette skjer fordi Project Operations er installert i ditt miljø.

Følg denne fremgangsmåten for å reaktivere alternativet for **Informasjon**-skjema:

1. Gå til **Ordrelinje**-tabellen.
2. Finn **Informasjon**-skjemaet under skjemaer-noden.
3. Velg **Informasjon**-skjemaet, og klikk deretter **Aktiver sikkerhetsroller**.
4. Endre sikkerhetsinnstillingen til **Vis til alle**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Slik aktiverer du og lagrer nettverkssporing, slik at sporinger kan knyttes til støtteforespørsler

Det kan hende at støttegruppen må gjennomgå nettverkssporing for å feilsøke enkelte problemer. Følg denne fremgangsmåten for å opprette en nettverkssporing:

### <a name="google-chrome-browser"></a>Google Chrome-nettleseren

1. Trykk på **F12** i den åpnede fanen, eller velg **Utviklerverktøy** for å åpne utviklerverktøyene.
2. Åpne **Nettverk**-fanen, og skriv inn **integ** i filtertekstboksen.
3. Kjør scenariet og registrer forespørslene som blir logget.
4. Høyreklikk på oppføringene, og velg **Lagre alle som en HAR med innhold**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge-nettleseren

1. Trykk på **F12** i den åpnede fanen, eller velg **Utviklerverktøy** for å åpne utviklerverktøyene.
2. Åpne **Nettverk**-fanen.
3. Kjør scenarioet.
4. Velg **Lagre** for å eksportere resultatene som HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
