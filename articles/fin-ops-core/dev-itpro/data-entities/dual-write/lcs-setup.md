---
title: Oppsett av dobbel skriving fra Lifecycle Services
description: Dette emnet forklarer hvordan du konfigurerer en tilkobling med dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 53e82fbf8cff834c9eb0d14a0597561158b85fa1
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783208"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Oppsett av dobbel skriving fra Lifecycle Services

[!include [banner](../../includes/banner.md)]



Dette emnet forklarer hvordan du aktiverer dobbel skriving fra Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Forutsetninger

Kunder må fullføre Power Platform-integreringen som beskrevet i følgende emner:

- Hvis du ikke bruker Microsoft Power Platform ennå, og vil utvide Økonomi og drift-miljøet ved å legge til plattformfunksjoner, kan du se [Power Platform-integrering - Aktiver under miljødistribusjon](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Hvis du allerede har Dataverse- og Power Platform-miljøer og vil koble dem til Økonomi og drift-miljøer, kan du se [Power Platform-integrering - Aktiver etter miljødistribusjon](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Konfigurere dobbel skriving for nye og eksisterende Dataverse-miljøer

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

8. Når koblingen er fullført, vises en hyperkobling. Bruk koblingen til å logge deg på administrasjonsområdet for dobbel skriving i økonomi- og driftsmiljøet. Derfra kan du definere enhetstilordninger.

## <a name="linking-mismatch"></a>Koblingskonflikt

Det er mulig at du har koblet skrivetilgangsmiljøet til en Dataverse-forekomst, mens LCS ikke er satt opp for Power Platform-integrering. Denne koblingskonflikten kan forårsake uventet virkemåte. Det anbefales at LCS-miljødetaljer samsvarer med det du er koblet til i skriveprosessen, slik at den samme forbindelsen kan brukes av forretningshendelser, virtuelle tabeller og tillegg.

Hvis miljøet ditt har en koblingskonflikt, viser LCS en advarsel som ligner på følgende eksempel på miljødetaljsiden: "Microsoft har oppdaget at miljøet ditt er koblet via dobbeltskriving til annet mål enn angitt i Power Platform-integrering, noe som ikke anbefales":

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform-integreringskoblingskonflikt.":::

Hvis du får denne advarselen, kan du prøve en av følgende løsninger:

- Hvis LCS-miljøet aldri er satt opp for Power Platform-integrering, kan du koble til Dataverse-forekomsten som er konfigurert med skriveprosessen, ved å følge instruksjonene i denne artikkelen.
- Hvis LCS-miljøet allerede er satt opp for Power Platform-integrering, bør du fjerne koblingen til dobbeltskriving og koble det til det som angis av LCS ved hjelp av [Scenario: Tilbakestill eller endre kobling](relink-environments.md#scenario-reset-or-change-linking).

Tidligere var det tilgjengelig en manuell støtteforespørsel, men det var før alternativ 1 over fantes.  Microsoft støtter ikke lenger manuelle koblinger av forespørsler via støtteforespørsler.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
