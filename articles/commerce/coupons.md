---
title: Kuponger
description: Denne artikkelen inneholder en oversikt over kupongrelaterte funksjoner i Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 20427a04a552ddec013daa6576ec64ab7046e95f
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709766"
---
# <a name="coupons"></a>Kuponger

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder en oversikt over kupongrelaterte funksjoner i Microsoft Dynamics 365 Commerce.

Kuponger er koder og strekkoder som brukes til å legge til rabatter i transaksjoner. Forhandlere distribuerer kuponger til potensielle eller eksisterende kunder for å bidra til å forbedre merkegjenkjenningen deres, stimulere til konvertering, beholde kundebasen, øke salget og i siste instans øke inntektene. Kuponger har blitt et av de mest populære markedsføringsverktøyene og er en ny norm i e-handelssalg.

I Dynamics 365 Commerce er kuponger knyttet til rabatter og betraktes som tilleggsvalidering av rabatter. Hver kupong er knyttet til én rabatt, og den tilknyttede rabatten definerer settet med produkter som kupongen er gyldig for.

Prisgrupper som er knyttet til en rabatt, definerer de kvalifiserte betingelsene som en kupong kan brukes til. Disse betingelsene omfatter kundegrupper og salgskanaler. Kuponger har også egenskapene **Bruksgrense** og **Kunde obligatorisk**, som kan brukes til å konfigurere valgfrie bruksbegrensninger.

Hver kupong kan ha flere kupongkoder og kupongstrekkoder, og hver kode kan ha sitt eget aktive datointervall og sin egen status. Hvis statusen til en kode er satt til **Inaktiv**, kan ikke koden brukes i noen kanal.

## <a name="set-up-a-coupon"></a>Definer en kupong

Før du kan definere en kupong, må du definere kupongens strekkode og to nummerserier for kupongen.

Følg denne fremgangsmåten for å definere en kupong i Commerce Headquarters.

1. Gå til **Detaljhandel og handel \> Lagerstyring \> Strekkoder og etiketter \> Masketegn**.
1. Velg **Legg til** for å opprette et masketegn av typen **Kupongkode**. I **Tegn**-feltet kan du velge ethvert ubrukte tegn.
1. Gå til **Detaljhandel og handel \> Lagerstyring \> Strekkoder og etiketter \> Oppsett for strekkodemaske**.
1. Velg **Ny** for å opprette en strekkodemaske av typen **Kupong**.
1. Gå til **Detaljhandel og handel \> Lagerstyring \> Strekkoder og etiketter \> Strekkodeoppsett**.
1. Velg **Ny** for å opprette en ny strekkode som bruker strekkodemasken du opprettet.
1. Gå til **Organisasjonsadministrasjon \> Nummerserier**.
1. Opprett to nummerserier:

    1. Én serie for referansen **Kupongnummer**. Denne serien definerer den unike identifikatoren for kupongen.
    1. Én serie for referansen **ID for kupongkode**. Denne serien definerer den unike identifikatoren for hver kode for en kupong.

    For begge nummerserier må du angi **Område**-feltet til **Firma**. I de fleste tilfeller skal begge serienumre genereres automatisk.

1. Gå til **Commerce-parametere \> Priser og rabatter \> Kuponger**.
1. Sett feltet **Strekkodemaske for kupong** til strekkoden du opprettet tidligere.
1. Gå til **Commerce-parametere \> Nummerserier**.
1. Velg nummerseriene du opprettet tidligere for referansene **Kupongnummer** og **ID for kupongkode**.

For å kunne definere en kupong må du opprette rabatten og kupongen separat og deretter knytte dem sammen ved å velge rabatten i **Rabatt**-feltet i kupongkonfigurasjonen. Etter at en kupong er knyttet til en rabatt, blir feltene **Status**, **Gyldighetsdato** og **Utløpsdato** for den tilknyttede rabatten skrivebeskyttet, fordi verdiene fastsettes av kupongens status og gyldighetsperiode. Når statusen for en kupong er satt til **Aktiv**, oppdateres statusen for den tilknyttede rabatten automatisk til **Aktivert**. Når statusen for en kupong er satt til **Inaktiv**, oppdateres statusen for den tilknyttede rabatten likeledes automatisk til **Deaktivert**.

## <a name="use-a-coupon"></a>Bruk en kupong

Hvis du vil legge til en kupong på en salgstransaksjon på salgssteder i Commerce, kan du bruke en kupongkode eller en kupongstrekkode. Hvis du vil bruke en kupongkode, velger du operasjonen **Legg til kupongkode** og angir deretter koden. For å bruke kupongstrekkode kan du enten skanne strekkoden ved å bruke en skanneenhet, eller angi den ved hjelp av det numeriske tastaturet på **Transaksjon**-skjermen.

Forhandlere vil av og til at kasserere skal kunne gi kunder rabatter med faste beløp for å holde kundene fornøyde eller på grunn av produktfeil, men de ønsker ikke å skrive ut kupongkoder og distribuere dem til kassererne. I dette tilfellet kan du sette alternativet **Bruk uten kupongkode** til **Ja**. Kasserere på salgsstedet kan deretter bruke funksjonen **Bruk kupong** i operasjonen **Vis tilgjengelige rabatter** til å legge til en kupong i en transaksjon uten å angi koden manuelt. Hvis det finnes flere kupongkoder for et kupong, vil systemet automatisk velge den første aktive koden og bruke den på transaksjonen.

For å kunne legge til en kupong i en salgsordre for telefonsenter må telefonsenterbrukeren velge **Kuponger** i **Administrer**-fanen i handlingsruten på salgsordresiden.

For å legge til en kupong i en e-handelsordre kan kunden angi kupongkoden i **kampanjekode**-feltet i handlekurven.

Når en kupong er lagt til i en salgsordre, utløser prissettingsmotoren umiddelbart omberegning for hele ordren, uavhengig av om forsinket beregning er aktivert.

> [!NOTE]
> I Commerce versjon 10.0.30 og tidligere må telefonsenterbrukere velge **Omberegn** i **Beregn**-gruppen i **Selg**-fanen i handlingsruten etter at de har lagt til en kupong i en salgsordre for telefonsenter, for å kunne bruke rabatten som er knyttet til denne kupongen.

## <a name="coupon-usage-limit"></a>Bruksgrense for kupong

Du kan konfigurere kuponger for begrenset bruk. Bruksgrensen kan defineres per kunde, per kanal eller globalt. Bruksgrensen brukes per kode på en kupong. En engangskupong som har to kupongkoder, kan for eksempel brukes to ganger: én gang for hver kupongkode.

Kuponger kan brukes på tvers av salgskanaler. Når det gjelder telefonsenter, kan imidlertid kuponger med begrenset bruk bare brukes når innstillingen **Aktiver ordrefullføring** for telefonsenterkanalen er aktivert. Hvis innstillingen **Aktiver ordrefullføring** er deaktivert, kan bare kuponger uten begrenset bruk brukes.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
