---
title: Detaljer for arbeidslinje
description: Dette emnet inneholder informasjon om Arbeidslinjedetaljer-siden, som viser en omfattende liste som kan sorteres og filtreres, over de enkelte arbeidslinjene i systemet.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4f0952cc8778ffc509bed80b3a5038dbf4fb76c2
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597198"
---
# <a name="work-line-details"></a>Detaljer for arbeidslinje

[!include [banner](../includes/banner.md)]

**Arbeidslinjedetaljer**-siden viser en omfattende liste som kan sorteres og filtreres, over de enkelte arbeidslinjene i systemet. Den gir en fullstendig oversikt over arbeid som blir planlagt og utført i lageret. Du kan enkelt bytte mellom å vise alle arbeidslinjer og vise bare åpne arbeidslinjer. Detaljer som gis for hver linje, er arbeidsstatus, varenummer, lokasjon, arbeidsantall, last-ID og forsendelses-ID.

## <a name="turn-on-the-work-line-details-feature"></a>Aktivere funksjonen detaljer for arbeidslinje

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Arbeidslinjedetaljer*

## <a name="open-and-use-the-work-line-details-page"></a>Åpne og bruke Arbeidslinjedetaljer-siden

Hvis du vil vise en liste over arbeidslinjedetaljer, kan du gå til **Lagerstyring \> Arbeid \> Arbeidslinjedetaljer**. Herfra kan du utføre følgende handlinger:

- Bruk **Filter**-feltet til å søke etter linjer som har en bestemt verdi for alle tilgjengelige parametere. (Tilgjengelige parametere inkluderer mange parametere som ikke vises som kolonner i rutenettet.)
- Bruk **Vis lukkede**-avmerkingsboksen til å vise eller skjule lukkede linjer.
- Velg **Vis dimensjoner** for å åpne **Dimensjonsvisning**-dialogboksen, der du kan velge å vise eller skjule forskjellige dimensjonskolonner i rutenettet.
- Velg en kolonneoverskrift for å åpne en meny der du kan velge å sortere eller filtrere listen etter verdier i den kolonnen.
- Velg en arbeidslinje, og velg deretter **Endre lokasjon** for å åpne en dialogboks der du kan endre lokasjonen for arbeidslinjen. Lokasjonen du angir, overstyrer oppsettet til lokasjonsdirektivet.
- Velg en arbeidslinje, og velg deretter **Avbryt arbeidslinje** for å åpne en dialogboks der du kan redusere antallet av den arbeidslinjen delvis eller helt.
- Juster antall.
- Vis transaksjonene bak en arbeidslinje.

## <a name="try-out-the-feature"></a>Prøv ut funksjonen

Denne delen inneholder en tredjepartsdemo som viser hvordan du arbeider med arbeidslinjedetaljer.

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom denne demonstrasjonen ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke denne demonstrasjonen som en veiledning når du arbeider i et produksjonssystem. Du må imidlertid erstatte dine egne verdier, og det kan hende du mangler noen typer obligatoriske oppføringer som standard demonstrasjonsdata gir.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Kontroller at scenariooppsettet omfatter nok tilgjengelig beholdning

Hvis du arbeider med **USMF**-demonstrasjonsdata, må du først kontrollere at systemet er konfigurert slik at det finnes nok beholdning på hver relevante plukklokasjon. For denne demonstrasjonen er forventes det at du har følgende tilgjengelige beholdning:

- **Vare M9200:** 45 ea. (eller mer)
- **Vare M9202:** 10 ea. (eller mer)

Følg denne fremgangsmåten for å kontrollere at det er nok beholdning tilgjengelig, og for å gjøre eventuelle nødvendige justeringer.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**, og finn ut hvilke plukklokasjoner som skal brukes ved plukking av salgsordrer på lager 51. (Hvis du vil ha mer informasjon, kan du se [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](control-warehouse-location-directives.md).)
1. Kontroller beholdningsnivåene ved relevante lokasjoner.
1. Juster beholdningen etter behov. Du kan opprette manuelle flyttinger, bruke etterfylling eller bruke en annen flyt til å justere beholdningen.

### <a name="part-1-create-picking-work"></a>Del 1: Opprett plukkarbeid

Før du begynner å opprette arbeid, må du kontrollere at lageret er konfigurert til å svare på arbeidsforespørsler på forventet måte.

Følg denne fremgangsmåten for å opprette plukkearbeid.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å åpne **Opprett salgsordre**-dialogboksen.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til _US-001_.
    - På hurtigfanen **Generelt** angir du **Lager**-feltet til _51_.

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Den inneholder en ny, tom rad i **Salgsordrelinjer**-rutenettet. Angi følgende verdier for denne ordrelinjen:

    - **Varenummer:** _M9200_
    - **Antall:** _20_
    - **Enhet:** _ea_

1. Velg den nye ordrelinjen og deretter på **Beholdning**-menyen velger du **Reservasjon** for å åpne **Reservasjon**-siden.
1. På **Reservasjon**-siden velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i kategorien **Lager** i handlingsruten. Systemet oppretter en forsendelse, legger den til en ny last, og oppretter det nødvendige arbeidet.
1. Opprett en ny salgsordre for samme kundekonto og lager som du brukte for den første ordren. Legg til følgende to ordrelinjer i denne ordren:

    - **Linje 1:** Angi **Varenummer**-feltet til _M9200_, **Antall**-feltet til _25_ og **Enhet**-feltet til _ea_.
    - **Linje 2:** Angi **Varenummer**-feltet til _M9202_, **Antall**-feltet til _10_ og **Enhet**-feltet til _ea_.

1. Gjenta trinn 6 til og med 8 for å reservere beholdningen for hver ordrelinje (én om gangen), og gjenta deretter trinn 9 for å frigi ordren til lageret.

### <a name="part-2-change-the-location-for-a-work-line"></a>Del 2: Endre lokasjonen for en arbeidslinje

1. Gå til **Lagerstyring \> Arbeid \> Arbeidslinjedetaljer**.
1. Finn og velg en av arbeidslinjene du opprettet for denne demonstrasjonen.
1. Velg **Endre lokasjon** for å åpne **Velg ny lokasjon**-dialogboksen.
1. I **Velg ny lokasjon**-dialogboksen i **Lokasjon**-feltet velger du en ny lokasjon for arbeidslinjen.
1. Velg **OK** for ta i bruk endringen og lukke dialogboksen.

> [!IMPORTANT]
> Du kan bare sende lokasjonsendringer hvis den nye lokasjonen har nok tilgjengelig beholdning (for en plukking), eller hvis den består lokasjonstypevalidering (for en plassering).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>Del 3: Endre antallet i en arbeidslinje eller avbryt en arbeidslinje

1. Gå til **Lagerstyring \> Arbeid \> Arbeidslinjedetaljer**.
1. Finn og velg en av arbeidslinjene du opprettet for denne demonstrasjonen. Vær oppmerksom på at du bare kan avbryte eller endre antall for arbeidslinjer der arbeidstypen er _plukk_.
1. Velg **Avbryt arbeidslinje** for å åpne **Antall som skal avbrytes**-dialogboksen.
1. I **Antall som skal avbrytes**-dialogboksen endrer du verdien i **Antall**-feltet for å angi antallet som skal *trekkes fra* antallet som for øyeblikket er angitt for linjen. Som standard viser **Antall**-feltet hele antallet.

    - Hvis du avbryter hele antallet, endres **Arbeidsstatus**-verdien til _Avbrutt_, men **Arbeidsantall**-feltet vil fremdeles vise den opprinnelige verdien.
    - Hvis du bare deler av antallet, oppdateres **Arbeidsantall**-feltet for å vise den nye verdien, men **Arbeidsstatus**-verdien endres ikke.

1. Velg **OK** for ta i bruk endringen og lukke dialogboksen.

> [!IMPORTANT]
> Hvis du avbryter bare en del av antallet for en arbeidslinje, må du også fjerne det foreldede antallet fra lastlinjen. Hvis ikke, med mindre underlevering er konfigurert riktig, kan ikke belastningslinjen leveringsbekreftes.
