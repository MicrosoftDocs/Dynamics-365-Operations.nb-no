---
title: Konfigurere det mobile arbeidsområdet Aktivastyring
description: Denne artikkelen beskriver hvordan du konfigurerer Microsoft Dynamics 365 Supply Chain Management og mobilappen Finance and Operations (Dynamics 365), slik at de kan kjøre et mobilt arbeidsområde for aktivastyring som arbeidere kan bruke til å utføre aktivastyringsoppgaver.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ee92ed2c0e2a59adaebe20ed3d426ac03c056dac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870849"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Konfigurere det mobile arbeidsområdet Aktivastyring

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer Microsoft Dynamics 365 Supply Chain Management og mobilappen Finance and Operations (Dynamics 365), slik at de kan kjøre et mobilt arbeidsområde for **Aktivastyring** som arbeidere kan bruke til å utføre aktivastyringsoppgaver.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Konfigurere vedlikeholdspersoner som brukere i Supply Chain Management

Følg denne fremgangsmåten for hver bruker som skal ha tilgang til det mobile arbeidsområdet for **Aktivastyring**.

1. I Supply Chain Management går du til **Personale \> Arbeidere** og kontrollerer at det finnes en arbeiderpost for brukeren du vil opprette. Opprett en ny arbeiderpost etter behov.
1. Gå til **Aktivastyring \> Oppsett \> Arbeidere \> Arbeidere**, og kontroller at arbeiderposten du identifiserte (eller opprettet) i det forrige trinnet, er tilordnet til en vedlikeholdspersonpost. Opprett en ny vedlikeholdspersonpost etter behov, og angi arbeiderposten fra forrige trinn i **Arbeider**-feltet.
1. Gå til **Aktivastyring \> Oppsett \> Arbeidere \> Vedlikeholdspersongrupper**, og kontroller at vedlikeholdspersonposten du identifiserte (eller opprettet) i det forrige trinnet, er hører til i en vedlikeholdspersongruppe.
1. Gå til **Systemadministrasjon \> Brukere**.
1. Velg den relevante brukeren i rutenettet.
1. Angi arbeiderkontoen du vil knytte til den gjeldende brukerkontoen, i **Person**-feltet i hurtigfanen **Brukerdetaljer**. Denne arbeiderkontoen skal være arbeiderposten du identifiserte (eller opprettet) i trinn 1 og tilordnet til en vedlikeholdspersonpost i trinn 2.

> [!NOTE]
> Brukertillatelser og sikkerhetsroller gjelder for funksjonene i det mobile arbeidsområdet for **Aktivastyring** på samme som for funksjonene i brukergrensesnittet i Supply Chain Management. Derfor må hver bruker du konfigurerer med tilgang til det mobile arbeidsområdet for **Aktivastyring**, ha sikkerhetsrollene som kreves for å utføre lignende operasjoner direkte i Supply Chain Management.

## <a name="publish-the-asset-management-mobile-workspace"></a>Publisere det mobile arbeidsområdet Aktivastyring

Hvis du vil gjøre funksjoner for aktivastyring tilgjengelige i mobilappen Finance and Operations (Dynamics 365), må du publisere det mobile arbeidsområdet for **Aktivastyring**.

1. I Supply Chain Management velger du **Innstillinger**-knappen (tannhjulsymbolet i øvre høyre hjørne), og deretter velger du **Mobilapp** på menyen.
1. Finn flisen **Aktivastyring** i dialogboksen **Administrer mobilapp**. Hvis den inneholder teksten «I metadata – ikke publisert», er arbeidsområdet ennå ikke publisert. Hvis den inneholder teksten «I metadata – publisert», er arbeidsområdet allerede publisert, og du kan hoppe over resten av denne fremgangsmåten.

    ![Dialogboksen Administrer mobilapp.](media/mobile-workspaces.png "Dialogboksen Administrer mobilapp")

1. Velg flisen **Aktivastyring**, og velg deretter **Publiser** på verktøylinjen. Etter noen sekunder skal du få en varsling om at arbeidsområdet er publisert. I tillegg skal teksten på flisen endres til «I metadata – publisert».

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Installere og konfigurere mobilappen Finance and Operations (Dynamics 365)

1. Gå til en av følgende appbutikker for å installere appen **Microsoft Finance and Operations (Dynamics 365)** på mobilenheten:

    - [For Google Android-enheter](https://go.microsoft.com/fwlink/?linkid=850662)
    - [For Apple IOS-enheter](https://go.microsoft.com/fwlink/?linkid=850663)

1. Åpne appen Finance and Operations (Dynamics 365). Påloggingssiden skal vises. Angi URL-adressen din for Supply Chain Management i **Logg på**-feltet, eller velg en nylig URL-adresse i listen **Siste miljøer**, og trykk deretter på **Koble til**.

    ![Påloggingsside.](media/mobile-app-sign-in.png "Påloggingsside")

1. Hvis du blir bedt om å bekrefte tilkoblingen, merker du av for **Jeg forstår** og trykker deretter på **Koble til**.
1. På siden **Velg en konto** bruker du Microsoft-kontoen til å logge deg på mobilprogrammet.

    Siden **Arbeidsområder** vises. Den viser alle de mobile arbeidsområdene som er publisert av Supply Chain Management-forekomsten din.

    ![Liste over arbeidsområder.](media/mobile-app-workspaces.png "Liste over arbeidsområder")

1. Hvis du må endre den juridiske enheten (firmaet), trykker du på Meny-knappen (noen ganger kalt hamburgeren eller hamburgerknappen) i øvre venstre hjørne, og deretter trykker du på **Endre firma**.

    ![Endre den juridiske enheten.](media/mobile-app-change-comp.png "Endre den juridiske enheten")

1. Velg arbeidsområdet du vil arbeide med, på **Arbeidsområder**-siden for å åpne det.

    ![Mobilt arbeidsområde for aktivabehandling.](media/mobile-app-asset-workspace.png "Mobilt arbeidsområde for aktivabehandling")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Arbeide med det mobile arbeidsområdet Aktivastyring

Hvis du vil ha mer informasjon om hvordan du arbeider med det mobile arbeidsområdet for **Aktivastyring**, kan du se [Bruke det mobile arbeidsområdet Aktivastyring](asset-management-mobile-workspace.md).

Hvis du vil ha mer informasjon om mobilappen Finance and Operations (Dynamics 365), kan du gå til [Startside for mobilapp](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]