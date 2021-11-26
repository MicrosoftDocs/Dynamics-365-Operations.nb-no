---
title: Oppsett av dobbel skriving fra Lifecycle Services
description: Dette emnet forklarer hvordan du konfigurerer en tilkobling med dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1fd15b5d664fead10949750678a2d3eab967af22
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781398"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Oppsett av dobbel skriving fra Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet forklarer hvordan du aktiverer dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forutsetninger

Du må fullføre Power Platform-integreringen som beskrevet i følgende emner:

+ [Power Platform-integrering - Aktiver under miljødistribusjon](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Power Platform-integrering - Aktiver etter miljødistribusjon](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Konfigurere dobbel skriving for nye Dataverse-miljøer

Følg denne fremgangsmåten for å konfigurere en dobbelt skriving fra LCS-siden **Miljødetaljer**:

1. På siden **Miljødetaljer** utvides delen **Power Platform-integrering**.

2. Velg knappen for **App med dobbel skriving**.

    ![Power Platform-integrering.](media/powerplat_integration_step2.png)

3. Gå gjennom vilkårene og betingelsene, og merk deretter av for **Konfigurer**.

4. Velg **OK** for å fortsette.

5. Du kan overvåke fremdriften ved å oppdatere siden med miljødetaljer regelmessig. Oppsettet tar vanligvis 30 minutter eller mindre.  

6. Når installasjonen er fullført, får du en melding om prosessen var vellykket eller om det oppstod en feil. Hvis installasjonen mislyktes, vises det en relatert feilmelding. Du må korrigere eventuelle feil før du går til neste trinn.

7. Velg **Koble til Power Platform-miljø** for å opprette en kobling mellom Dataverse og databasene for det gjeldende miljøet. Dette tar vanligvis 5 minutter eller mindre.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Koble til Power Platform-miljø.":::

8. Når koblingen er fullført, vises en hyperkobling. Bruk koblingen til å logge deg på administrasjonsområdet for dobbel skriving i Finance and Operations-miljøet. Derfra kan du definere enhetstilordninger.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Konfigurere dobbel skriving for et eksisterende Dataverse-miljø

Hvis du vil definere skrivetilgang for et eksisterende Dataverse-miljø, må du opprette en Microsoft [støtteforespørsel](../../lifecycle-services/lcs-support.md). Denne forespørselen må inneholde følgende:

+ Finance and Operations-miljø-ID.
+ Miljønavnet fra Lifecycle Services.
+ Dataverse-organisasjons-IDen eller Power Platform-miljø-IDen fra Power Platform-administrasjonssenteret. Be om at IDen er forekomsten som brukes for Power Platform-integrering, i forespørselen.

> [!NOTE]
> Du kan ikke koble fra miljøer ved hjelp av LCS. Hvis du vil oppheve koblingen til et miljø, åpner du arbeidsområdet **Dataintegrering** i Finance and Operations-miljøet, og deretter velger du **Koble fra**.

## <a name="linking-mismatch"></a>Koblingskonflikt

Det er mulig at LCS-miljøet er koblet til en Dataverse-forekomst, mens skrivemiljøet er koblet til en annen Dataverse-forekomst. Denne koblingskonflikten kan forårsake uventet virkemåte, og det kan ende opp med å sende data til feil miljø. Det anbefalte miljøet som skal brukes til dobbel skriving, er det som opprettes som en del av Power Platform-integreringen, og langsiktig, er dette den eneste måten å etablere en kobling mellom miljøer på.

Hvis miljøet ditt har en koblingskonflikt, viser LCS en advarsel på siden med miljødetaljer som ligner på «Microsoft har oppdaget at miljøet ditt er koblet via dobbel skriving til annet mål enn angitt i Power Platform-integrering, noe som ikke anbefales»:

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform-integreringskoblingskonflikt.":::

Hvis du oppdager denne feilen, finnes det to alternativer basert på dine behov:

+ [Koble fra og koble tilbake miljøer for dobbel skriving (Tilbakestill eller endre kobling)](relink-environments.md#scenario-reset-or-change-linking) slik det er angitt på siden med detaljer om LCS-miljøet. Dette er det ideelle alternativet, fordi du kan kjøre det uten Microsoft-støtte.  
+ Hvis du vil at koblingen skal holdes i dobbel skriving, kan du be om hjelp fra Microsoft Kundestøtte til å endre Power Platform-integreringen slik at den bruker det eksisterende Dataverse-miljøet, slik det er dokumentert i den forrige delen.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
