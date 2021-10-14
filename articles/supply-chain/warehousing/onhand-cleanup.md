---
title: Oppryddingsjobb for lagerstyringsposter
description: Dette emnet beskriver oppryddingsjobben for lageroppføringer, som bidrar til å forbedre systemytelsen ved å identifisere og slette relaterte, men overflødige poster.
author: perlynne
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d839ed861a24f6ef7267c85e942c275586b4a8c4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565102"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Oppryddingsjobb for lagerstyringsposter

[!include [banner](../includes/banner.md)]

Ytelsen til spørringer som brukes til å beregne lagerbeholdning, påvirkes av antall poster i tabellene som er involvert. Én måte å forbedre ytelsen på, er ved å redusere antall poster databasen må vurdere.

Dette emnet beskriver oppryddingsjobben for lageroppføringer, som sletter unødvendige poster i InventSum- og WHSInventReserve-tabellene. Disse tabellene lagrer beholdningsinformasjon for varer som er aktivert for prosessering av lagerstyring. (Disse varene omtales som WHS-varer.) Sletting av disse postene kan forbedre ytelsen for beholdningsberegninger betraktelig.

## <a name="what-the-cleanup-job-does"></a>Hva oppryddingsjobben gjør

Oppryddingsjobben for lageroppføringer sletter alle poster i WHSInventReserve- og InventSum-tabellene der alle feltverdiene er *0* (null). Disse oppføringene kan slettes fordi de ikke bidrar til beholdningsinformasjonen. Jobben sletter bare oppføringer som er lavere enn **Lokasjon**-nivået.

Hvis negativ fysisk beholdning er tillatt, kan det hende at oppryddingsjobben ikke kan slette alle de aktuelle postene. Årsaken til denne begrensningen er at jobben må tillate et bestemt scenario der et nummerskilt har flere serienumre, hvorav ett av disse serienumrene har blitt negativt. Systemet vil for eksempel ikke ha en beholdning på null når et nummerskilt har mer enn 1 stk med serienummer 1 og mindre enn 1 stk av serienummer 2. I dette spesielle scenariet brukes jobben en "breddesletting" der den prøver å slette fra lavere nivåer først.

## <a name="schedule-and-configure-the-cleanup-job"></a>Planlegge og konfigurere oppryddingsjobben

Oppryddingsjobben for lagerposter er tilgjengelig i **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Oppryddingsjobb for lagerstyringsposter**. Bruk standardinnstillingene for jobben til å styre omfanget av og tidsplanen for kjøring av jobben. I tillegg finnes følgende innstillinger:

- **Slett hvis ikke oppdatert på dette antallet dager** – Angi det minste antallet dager som jobben skal settes på vent i før den sletter en beholdningsoppføring som har falt til null i antall. Bruk denne innstillingen for å redusere risikoen for å slette lagerbeholdninger som fortsatt brukes. Hvis du vil at oppryddingen skal skje så snart som mulig, kan du enten angi *0* (null) eller la feltet stå tomt.
- **Maksimal utførelsestid (i timer)** – Angi den maksimale utførelsestiden for oppryddingsjobben, oppført i timer. Hvis jobben ikke blir fullført før denne tiden går ut, vil den lagre arbeidet som er fullført så langt, og deretter lukke seg. Denne funksjonen er spesielt relevant for implementeringer som er svært viktige for beholdningen. I disse tilfellene bør du planlegge at jobben skal kjøres når systembelastningen er så lav som mulig. Hvis du vil at den partivise jobben fortsatt skal kjøres til den er fullført, angir du *0* (null) eller lar feltet stå tomt. Denne innstillingen er bare tilgjengelig hvis den tilknyttede funksjonen er [aktivert i systemet](#max-execution-time).

Selv om du kan kjøre jobben innenfor vanlig arbeidstid, anbefaler vi at du kjører den utenfor arbeidstiden. På denne måten bidrar du til å forhindre konflikter som kan oppstå hvis en bruker jobber med en post som samtidig ryddes opp.

Hvis jobben prøver å slette en post for en vare mens denne posten brukes av en annen bruker, oppstår det en vranglås-feil enten for oppryddingsjobben eller brukeren.

Når jobben kjører, har den en tildelt størrelse på 100. Den vil med andre ord prøve å utføres én gang for hver 100. sletting. Fordi enkelte slettinger er settbasert, kan det oppstå scenarier der mer enn 100 poster kan bli slettet i den samme transaksjonen. Derfor kan det hende at låseeskalering fremdeles forekommer.

## <a name="possible-user-impact"></a>Mulig påvirkning på brukerne

Brukere kan bli påvirket hvis oppryddingsjobben for lagerbeholdning sletter alle postene for et gitt nivå (f.eks. nummerskiltnivået). I dette tilfellet er det ikke sikkert at funksjonaliteten for å vise den tidligere tilgjengelige beholdningen ved et nummerskilt fungerer som forventet, fordi de relevante beholdningspostene ikke lenger er tilgjengelige. Dette kan for eksempel skje i følgende situasjoner:

- I **Beholdningsliste** når brukeren opphever valget av betingelsen **Antall \<\> 0** eller velger betingelsen **Lukkede transaksjoner** i innstillingene for **Dimensjonsvisning**.
- I rapporten **Aktuell beholdning etter lagerdimensjon** for tidligere perioder når brukeren angir parameteren **Per dato**.

Ytelsesforbedringen som oppryddingsjobben gir, skal imidlertid veie opp for disse små tapene i funksjonalitet.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Gjør innstillingen for maksimal utførelsestid tilgjengelig.

Som standard er innstillingen **Maksimal utførelsestid** ikke tilgjengelig. Hvis du vil bruke den, må du bruke [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) for å aktivere den tilknyttede funksjonen i systemet. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Maksimal utførelsestid for oppryddingsjobb for lagerbeholdning*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]