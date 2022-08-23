---
title: Konfigurere oppgavebehandling
description: Denne artikkelen beskriver hvordan du konfigurerer funksjoner for oppgavebehandling i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: ff97abab330174b41af76d22c202e8338d6d37fd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282768"
---
# <a name="configure-task-management"></a>Konfigurere oppgavebehandling

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer funksjoner for oppgavebehandling i Microsoft Dynamics 365 Commerce.

Før Dynamics 365 Commerce-ledere og -ansatte kan bruke funksjonene for oppgavestyring i Commerce, må oppgavebehandling være konfigurert. Konfigurasjonstrinn omfatter å gi tillatelser til ledere og ansatte, distribuere tillatelser til salgsstedsklienter (POS), definere POS-varslinger og konfigurere **Oppgaver**-flisen på startsiden for et POS-program.

## <a name="configure-permissions-for-store-managers"></a>Konfigurere tillatelser for butikkledere

Alle ansatte i en gitt butikk kan vise alle oppgaver som er tilordnet til butikken. De kan også oppdatere statusen for oppgavene som er tilordnet til dem. Personer som butikkledere må imidlertid ha administrasjonsrettigheter for aktiviteter for å administrere oppgaver som er tilordnet til butikken, og til å opprette oppgaver med enkelt formål.

Følg denne fremgangsmåten for å konfigurere tillatelser for oppgavebehandling for butikkledere.

1. Gå til **Retail og Commerce \> Ansatte \> Tillatelsesgrupper**.
1. Velg en bestemt tillatelsesgruppe (for eksempel **Leder**), og velg deretter **Rediger**.
1. I hurtigfanen **Tillatelser** setter du alternativet **Tillat oppgavebehandling** til **Ja**.
1. I hurtigfanen **Varslinger** legger du til operasjonen **Oppgavestyring** og angir en verdi i feltet **Visningsrekkefølge**. Angi for eksempel **2** hvis **Ordreoppfyllelse**-operasjonen allerede har en verdi for **Visningsrekkefølge** på **1**.
    
> [!NOTE]
> Hvis en person som ikke er leder, må ha tillatelser for oppgavebehandling på salgsstedet, kan du gi tilgang til den enkelte. Du kan også opprette en ny tillatelses gruppe for ikke-overordnede og sette alternativet **Tillat oppgavebehandling** til **Ja**.

Følgende illustrasjon viser hvordan du konfigurerer tillatelser for oppgavebehandling for butikkledere.

![Konfigurere tillatelser for oppgavebehandling for butikkledere.](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Konfigurere tillatelser for ansatte

Ansatte må ha tillatelse til å opprette oppgavelister, behandle tildelingskriterier og konfigurere gjentakelsen av en hvilken som helst oppgaveliste. Hvis du vil konfigurere disse tillatelsene, tilordner du de ansatte til rollen **Retail-oppgaveleder**.

Hvis du vil konfigurere tillatelser for en ansatt, gjør du følgende.

1. Gå til **Retail og Commerce \> Ansatte \> Brukere**.
1. Velg en ansatt.
1. På hurtigfanen **Brukerens roller** velger du **Tilordne roller**.
1. I dialogboksen **Tilordne roller til bruker** velger du rollen **Retail-oppgaveleder** og velger deretter **OK**.

## <a name="distribute-permissions-to-pos-clients"></a>Distribuere tillatelser til POS-klienter

Før ansatte kan bruke POS-klienter, må tillatelser distribueres og synkroniseres til disse klientene.

Følg denne fremgangsmåten for å distribuere tillatelser til POS-klienter.

1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. Velg distribusjonsplanen **1060** (**Stab**), og velg deretter **Kjør nå**.
1. Velg distribusjonsplanen **1070** (**Kanalkonfigurasjon**), og velg deretter **Kjør nå**.

## <a name="configure-pos-notifications-for-tasks"></a>Konfigurere POS-varslinger for oppgaver

Oppgavebehandling må konfigureres slik at varslinger blir tilgjengelige i POS-programmet.

Hvis du vil konfigurere POS-varslinger for oppgaver, gjør du følgende.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> POS-operasjoner**.
1. Finn operasjonen **1400** (**Oppgavebehandling**), og merk av for **Aktiver varslinger** for den.

Følgende illustrasjon viser operasjonen **Oppgavebehandling** på siden **POS-operasjoner**.

![Operasjonen Oppgavebehandling på siden POS-operasjoner.](media/HQ-POS-Tasks-Notifications.png)

Hvis du vil ha mer informasjon om hvordan du konfigurerer POS-varslinger, kan du se [Vise ordrevarslinger på salgsstedet (POS)](notifications-pos.md).

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Konfigurere Oppgaver-flisen på startsiden for et POS-program

Før du konfigurerer **Oppgaver**-flisen på startsiden for et POS-program, kan du se [Skjermoppsett for salgssted (POS)](pos-screen-layouts.md) for informasjon om hvordan du konfigurerer og legger til nye knapper i et POS-skjermoppsett.

Gjør følgende for å konfigurere **Oppgaver**-flisen på startsiden for et POS-program.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> Skjermoppsett**.
1. Velg et skjermoppsett, velg en oppsettsstørrelse, og velg deretter en knappegruppe.
1. På hurtigfanen **Knappegrupper** velger du **Designer** for å redigere den valgte knappegruppen.
1. Legg til en **Oppgaver**-flis i den aktuelle delen på startsiden.

Illustrasjonen nedenfor viser et eksempel på en **Oppgaver**-flis på en POS-startside.

![Oppgaver-flis på en POS-startside.](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over oppgavebehandling](task-mgmt-overview.md)

[Opprette oppgavelister og legge til oppgaver](task-mgmt-create-lists.md)

[Tilordne oppgavelister til butikker eller ansatte](task-mgmt-assign-lists.md)

[Oppgavebehandling på salgsstedet](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
