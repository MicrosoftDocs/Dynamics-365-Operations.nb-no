---
title: Definere en enhet for å kjøre grensesnittet for produksjonsutførelse
description: Grensesnittet for produksjonsutførelse defineres for hver enhet på produksjonsgulvet. Firmaer konfigurerer vanligvis hver enhet på forskjellig måte, avhengig av hvilket formål enheten tjener. Et firma kan for eksempel ha én enhet i mottaksområdet, der arbeidere stempler inn og ut, og en annen i Shop Floor, der arbeiderne administrerer jobbene sine.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9a5911e81547134d3034d1a47ef94c553ccbb331
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353970"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Definere en enhet for å kjøre grensesnittet for produksjonsutførelse

[!include [banner](../includes/banner.md)]

Grensesnittet for produksjonsutførelse defineres for hver enhet på produksjonsgulvet. Firmaer konfigurerer vanligvis hver enhet på forskjellig måte, avhengig av hvilket formål enheten tjener. Et firma kan for eksempel ha én enhet i mottaksområdet, der arbeidere stempler inn og ut, og en annen i Shop Floor, der arbeiderne administrerer jobbene sine.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Angi konfigurasjon og filtre for en bestemt enhet

Hvis du vil angi konfigurasjons- og jobbfiltre for en enhet, kan du logge deg på siden for **produksjonsutførelse** ved å bruke en konto som har en sikkerhetsrolle som omfatter plikten *Oppretthold tidsovervåking*. (Blant de medfølgende sikkerhetsrollene har bare *Arbeidsleder* denne plikten.) Deretter følger du disse trinnene.

1. Gå til enheten du vil konfigurere, og logg på Microsoft Dynamics 365 Supply Chain Management som en arbeidsleder. (Bruk en konto som inneholder plikten *Oppretthold tidsovervåking*.)
1. Kontroller at det finnes en konfigurasjon for enheten du konfigurerer. Hvis det ikke finnes noen konfigurasjon, angis det en standard konfigurasjon. Hvis du vil ha mer informasjon om hvordan du definerer en konfigurasjon, kan du se [Konfigurere grensesnittet for produksjonsutførelse](production-floor-execution-configure.md).
1. Gå til **Produksjonskontroll \> Produksjonsutførelse \> Produksjonsutførelse**.

    Hvis grensesnittet for produksjonsutførelse allerede er konfigurert minst én gang på den gjeldende enheten, vises en påloggingsside. Ellers vises en velkomstside.

1. Velg **Konfigurer** på påloggingssiden eller velkomstsiden.
1. Velg en konfigurasjon fra listen.
1. Velg **Neste**.
1. Velg ett eller flere filtre som skal brukes på den gjeldende enheten. Disse filtrene vil bidra til å sikre at bare relevante jobber vises på enheten. Hvis du vil definere et filter, velger du filtertypen for å åpne en liste med verdier, og deretter velger du verdien du vil filtrere på. Følgende filtre er tilgjengelige:

    - **Produksjonsenhet** – Dette filteret er filter på det høyeste nivået. Den refererer vanligvis til et stort arbeidsområde som har flere ressursgrupper og individuelle ressurser.
    - **Ressursgruppe** – dette filteret er et filter på mellomnivå. Den refererer vanligvis til en samling relaterte ressurser i et begrenset område i arbeidsområdet. Hvis du velger et **Produksjonsenhet**-filter først, viser listen over ressursgrupper bare grupper fra den enheten. Ellers vises alle tilgjengelige ressursgrupper.
    - **Ressurs** – dette filteret er det mest spesifikke filteret. Den refererer vanligvis til en bestemt maskin eller annen enkeltressurs. Hvis du velger **Ressursgruppe** og/eller **Produksjonsenhet**-filteret først, viser ressurslisten bare ressurser fra denne gruppen og/eller enheten. Ellers vises alle tilgjengelige ressurser.

1. Velg **OK**.
1. Påloggingssiden vises, og enheten er klar til bruk.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Tillate at en arbeider overstyrer standardfiltrene

Du kan gi bestemte arbeidere tillatelse til å endre filterinnstillingene på alle enheter de bruker. For arbeidere som har denne tillatelsen, har grensesnittet for produksjonsutførelse en **Filter**-knapp på sidene **Alle jobber** og **Aktiv jobb**.

> [!NOTE]
> Hvis en arbeider endrer et filter, brukes det nye filteret fra dette tidspunktet og fremover, for alle brukere som logger på enheten.

Følg denne fremgangsmåten for å tillate at en arbeider kan overstyre standard jobbfiltrene som er definert for en enhet.

1. Gå til **Timeregistrering \> Oppsett \> Tidsregistreringsarbeidere**.
1. Velg en arbeider i listen for å åpne arbeiderens side for **Tidsregistreringsarbeidere**.
1. I fanen **Tidsregistrering** setter du alternativet **Angi filtre** til *Ja*.

## <a name="run-the-interface-in-full-screen-mode"></a>Kjør grensesnittet i full skjermmodus

Du vil ofte kjøre grensesnittet for produksjonsutførelse på en enhet som bare brukes til dette formålet. Det kan derfor være fornuftig å kjøre grensesnittet i full skjermmodus, uten å vise noen navigasjon og/eller Chrome-leser.

- Hvis du vil skjule navigasjonsruten som vises i Supply Chain Management, legger du til følgende tekst på slutten av URL-adressen i webleserens adresselinje: `\&limitednav=true`.
- Hvis du også vil skjule adresselinjen i leseren, bruker du den innebygde fullskjermmodusen i leseren. (Hvis du vil ha instruksjoner, se dokumentasjonen for leseren.)

Den øvre delen av illustrasjonen nedenfor viser hvordan grensesnittet ser ut som standard. Den nedre delen viser hvordan den ser ut i full skjermmodus når navigasjonsruten er skjult.

![Standard i forhold til fullskjerm-grensesnitt.](media/pfei-full-screen.png "Standard i forhold til fullskjerm-grensesnitt")

## <a name="extend-the-session-past-12-hours"></a>Utvide økten utover 12 timer

Som standard blir grensesnittet for produksjonsutførelse automatisk avlogget hvis ingen bruker det i 12 timer. En bruker av Supply Chain Management må deretter logge på på nytt. Du kan imidlertid forlenge tidsavbruddsgrensen til opptil 90 dager.

Hvis du vil forlenge grensen for tidsavbrudd, logger du på Supply Chain Management og går til **Systemadministrasjon \> Brukere \> Øktutvidelser**. Angi brukerkontoen Supply Chain Management som brukes til å logge på enheten, og hvor mange timer økten skal være aktiv.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]