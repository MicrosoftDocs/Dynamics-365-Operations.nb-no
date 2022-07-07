---
title: Statuser for arbeidsordre
description: Denne artikkelen forklarer livssyklustilstander for arbeidsordrer i Aktivastyring.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c6a7c204370542353e9b629b78091972f8ce9a1
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017094"
---
# <a name="work-order-lifecycle-states"></a>Livssyklustilstand for arbeidsordre


[!include [banner](../../includes/banner.md)]

 

Livssyklustilstander for arbeidsordre definerer tilstandene som en arbeidsordre kan gå gjennom. Eksempler er **opprettet**, **planlagt**, **pågår** og **avsluttet**. Livssyklustilstander for arbeidsordre kan oppdateres manuelt i en arbeidsordre, eller de kan oppdateres automatisk (for eksempel under planlegging av arbeidsordren).

Livssyklustilstandene for arbeidsordre som kreves for arbeidsordrene, må være knyttet til tilsvarende prosjektstadier på siden **Parametere for prosjektstyring og regnskap** (**Prosjektstyring og regnskap** \> **Parametere for prosjektstyring og regnskap**). Først definerer du prosjektstadier i Prosjektstyring og regnskap. Deretter definerer du livssyklustilstander for arbeidsordrer og livssyklusmodeller for arbeidsordrer i Aktivastyring.

I tabellen nedenfor beskrives alternativene i delene **Arbeidsordre** og **Tidsplan** i hurtigfanen **Generelt** på siden **Livssyklustilstand for arbeidsordre** (**Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Livssyklustilstander**).

![Siden Livssyklustilstand for arbeidsordre.](media/09-setup-for-work-orders.png)

| Navn på alternativ                   | beskrivelse |
|-------------------------------|-------------|
| Aktivt                        | Sett dette alternativet til **Ja** hvis arbeidsordren skal være aktiv når den er i denne livssyklustilstanden. |
| Legg til linje                      | Sett dette alternativet til **Ja** hvis arbeidsordrejobber kan legges til i en arbeidsordre som er i denne livssyklustilstanden. |
| Slett                        | Sett dette alternativet til **Ja** hvis en arbeidsordre kan slettes når den er i denne livssyklustilstanden. |
| Slett linje                   | Sett dette alternativet til **Ja** hvis arbeidsordrejobber kan slettes fra en arbeidsordre som er i denne livssyklustilstanden. |
| Tillat planlegging              | Sett dette alternativet til **Ja** hvis en arbeidsordre kan planlegges når den er i denne livssyklustilstanden. |
| Sett faktisk start              | Sett dette alternativet til **Ja** hvis brukeren skal bli bedt om å velge faktisk startdato og -klokkeslett for en arbeidsordre når den oppdateres til denne livssyklustilstanden. |
| Sett faktisk slutt                | Sett dette alternativet til **Ja** hvis brukeren skal bli bedt om å velge faktisk sluttdato og -klokkeslett for en arbeidsordre når den oppdateres til denne livssyklustilstanden. |
| Poster journaler                 | Sett dette alternativet til **Ja** hvis arbeidsordrejournaler skal posteres automatisk når en arbeidsordre oppdateres til denne livssyklustilstanden. Hvis det oppstår feil under journalposteringen, vises en melding, og oppdateringen av livssyklustilstanden for arbeidsordren avbrytes. Hvis du vil vise journallinjene for en arbeidsordre , velger du **Aktivastyring** \> **Arbeidsordrer** \> **Alle arbeidsordrer**, **Aktive arbeidsordrer** eller **Mine aktive arbeidsordrer**, velger arbeidsordren i listen og deretter **Journaler**. Dette oppsettet for automatisk postering av arbeidsordrejournaler ved en bestemt livssyklustilstand er det samme som når du velger **Poster journaler** på siden **Arbeidsordrejournaler**.<p>**Obs!** Hvis du setter dette alternativet til **Ja**, posteres journaler automatisk hvis det ikke er satt opp en arbeidsflyt for godkjenning. Hvis firmaet ditt bruker journalgodkjenningsoppsettet som er konfigurert på siden **Journalgodkjenning** (**Prosjektstyring og regnskap** \> **Oppsett** \> **Journaler** \> **Journalgodkjenning**), må en leder eller assistent validere og postere forbruksregistreringer.</p> |
| Behandle sjekkliste for vedlikehold | Sett dette alternativet til **Ja** hvis alle tilknyttede vedlikeholdssjekklister skal behandles når en arbeidsordre oppdateres til denne livssyklustilstanden. Som en del av denne behandlingen posteres eventuelle tellerregistreringer som ble gjort for en vedlikeholdssjekkliste, og resultatet av hele vedlikeholdssjekklisten evalueres. Vedlikeholdssjekklistelinjer som har resultatene **Bestått** og **Mislykket**, evalueres. Hvis minst én linje mislykkes, merkes hele vedlikeholdssjekklisten som **Mislykket** i Aktivastyring. |
| Klar                         | Sett dette alternativet til **Ja** hvis planstatusen for arbeidsordrejobben for alle arbeidsordrejobber som opprettes i en arbeidsordre, skal oppdateres automatisk til **Klar** når arbeidsordren oppdateres til denne livssyklustilstanden. |
| Start                         | Sett dette alternativet til **Ja** hvis planstatusen for arbeidsordrejobben for alle arbeidsordrejobber som opprettes i en arbeidsordre, skal oppdateres automatisk til **Startet** når arbeidsordren oppdateres til denne livssyklustilstanden. |
| Slutt                           | Sett dette alternativet til **Ja** hvis planstatusen for arbeidsordrejobben for alle arbeidsordrejobber som opprettes i en arbeidsordre, skal oppdateres automatisk til **Avsluttet** når arbeidsordren oppdateres til denne livssyklustilstanden. |
| Slett tidsplanlinjer         | Sett dette alternativet til **Ja** hvis planlegging for alle arbeidsordrejobber som opprettes i en arbeidsordre som allerede er planlagt, skal slettes når arbeidsordren oppdateres til denne livssyklustilstanden. Med andre ord blir kapasitetsreservasjoner for anleggsmiddelet, tilknyttet vedlikeholdsperson og tilknyttede verktøy slettet. Du setter for eksempel dette alternativet til **Ja** for en arbeidsordrelivssyklustilstand som kalles **Estimert**. Når en arbeidsordre så tilbakestilles til denne livssyklustilstanden fordi det kreves ny planlegging, kan planleggingen slettes i denne arbeidsordren. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Definere prosjektstadier og livssyklustilstander for arbeidsordre

1. Velg **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**.
2. I fanen **Prosjektstadium**, for hvert stadium du vil bruke, merker du av for hver prosjekttype som kreves for arbeidsordrene. Prosjekttypene definerer regler om de finansielle oppgavene som er tillatt. Eksempler på finansielle oppgaver er oppretting av prognoser, estimater og saldoer.

    > [!IMPORTANT]
    > Hvis det ikke er valgt et prosjektstadium for en prosjekttype, men prosjektstadiet brukes for en arbeidsordrelivssyklustilstand, oppdateres ikke arbeidsordreprosjektene på riktig måte.

3. Lukk siden **Parametere for prosjektstyring og regnskap**.
4. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Livssyklustilstander**.
5. Velg **Ny** for å opprette en ny livssyklustilstand for arbeidsordre.
6. I feltet **Livssyklustilstand** angir du en ID for livssyklustilstanden.
7. Angi et navn i **Navn**-feltet.

    På hurtigfanen **Detaljer** viser feltet **Livssyklusmodeller** viser antall livssyklusmodeller for arbeidsordrer som bruker denne livssyklustilstanden.

8. I **Generelt**-hurtigfanen i delen **Arbeidsordre** velger du funksjonene som skal være tilgjengelige for denne livssyklustilstanden, ved å sette de relevante alternativene til **Ja**. Se tabellen tidligere i denne artikkelen for beskrivelser av alternativene.
9. I **Prosjekt**-delen i **Fase**-feltet velger du prosjektstadiet som skal knyttes til denne livssyklustilstanden.
10. I **Prosjekt**-delen setter du alternativet **Lukk aktiviteter** til **Ja** hvis prosjektaktiviteter som er knyttet til hver arbeidsordrejobb, skal lukkes automatisk når arbeidsordren er i denne livssyklustilstanden.

    > [!NOTE]
    > Hvis du vil finne nummeret på prosjektaktiviteten som er knyttet til en arbeidsordrejobb, velger du **Aktivastyring** \> **Arbeidsordrer** \> **Alle arbeidsordrer**, **Aktive arbeidsordrer** eller **Mine aktive arbeidsordrer**. Åpne arbeidsordren, og velg deretter arbeidsordrejobben. Aktivitetsnummeret vises i **Aktivitetsnummer**-feltet i **Prosjekt**-delen i fanen **Generelt** på hurtigfanen **Linjedetaljer**.

11. I **Prognose**-delen setter du alternativet **Kopier timeprognose**, **Kopier vareprognose** og/eller **Kopier utgiftsprognose** til **Ja** hvis prosjektprognoser for arbeidsordre skal kopieres automatisk til arbeidsordrejournaler når arbeidsordren er i denne livssyklustilstanden.
12. I delen **Planlegg** setter du ett av alternativene til **Ja** hvis planleggingsstatusen for arbeidsordrejobber skal oppdateres når arbeidsordren er i denne livssyklustilstanden. Hvis du vil ha en beskrivelse av alternativene **Klar**, **Start**, **Slutt** og **Slett planlinjer**, kan du se tabellen tidligere i denne artikkelen.

    > [!NOTE]
    > Hvis du vil vise planlinjer som er knyttet til arbeidsordrejobber, velger du **Aktivastyring** \> **Arbeidsordrer** \> **Alle arbeidsordrer**, **Aktive arbeidsordrer** eller **Mine aktive arbeidsordrer**. Åpne arbeidsordren, velg arbeidsordrejobben i hurtigfanen **Arbeidsordrejobber** og vis relatert informasjon i hurtigfanen **Linjedetaljer**. **Status**-feltet i fanen **Planlegg** viser statusen for arbeidsordrejobben. **Status**-feltet kan settes til følgende verdier: **Planlagt**, **Klar**, **Startet**, **Stoppet** og **Avsluttet**.

13. I feltet **Livssyklustilstand** i delen **Meldinger** velger du livssyklustilstanden for meldinger som tilknyttede meldinger skal oppdateres til. Denne oppdateringen skjer automatisk. Det kan bare gjøres hvis livssyklustilstanden for meldinger er valgt i livssyklusmodellen for meldinger som brukes for meldingen.
14. I delen **Aktiva** setter du alternativet **Oppdater stykkliste for aktiva** til **Ja** hvis alle varer som brukes i en arbeidsordre, skal oppdateres automatisk på siden **Stykkliste for aktiva** når arbeidsordren oppdateres til denne livssyklustilstanden. Denne innstillingen kan være relevant hvis for eksempel livssyklustilstanden for arbeidsordren definerer arbeidsordren som fullført eller avsluttet.
15. I delen **Arbeidsordresamling** setter du alternativet **Slett samlingsreferanse** til **Ja** hvis arbeidsordrer som er i denne livssyklustilstanden, skal slettes automatisk fra arbeidsordresamlinger.
16. I hurtigfanen **Valider** velger du valideringstypene som skal aktiveres i denne livssyklustilstanden, ved å sette de relevante alternativene til **Ja**. Velg deretter typen melding som skal vises hvis obligatoriske felt som er relatert til valideringstypen, ikke er validert, i **Type**-feltet for hver valideringstype du velger. Hvis du velger **Feil**, avbrytes oppdateringen av livssyklustilstanden for arbeidsordren til de tilknyttede obligatoriske feltene er oppdatert i arbeidsordren.

    - Alternativene **Nedetid ved vedlikehold**, **Vedlikeholdssjekkliste**, **Feilsymptom**, **Feilårsak** og **Feilløsning** er knyttet til alternativene i **Obligatorisk**-delen på siden **Arbeidsordretyper** (**Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Arbeidsordretyper**). Hvis du vil aktivere disse valideringene, må de tilknyttede alternativene også settes til **Ja** på arbeidsordretypen som brukes for arbeidsordren.
    - Hvis alternativet **Vedlikeholdssjekkliste** settes til **Ja** for livssyklustilstanden som en arbeidsordre oppdateres til, gjøres en validering for å verifisere at vedlikeholdssjekklistelinjer som er merket som **Obligatorisk**, har blitt registrert som enten **Kontrollert** eller **Gjelder ikke**. Hvis ingen av disse registreringene er gjort på de obligatoriske linjene, vises feilinformasjon eller en advarselsmelding når arbeidsordren oppdateres til denne livssyklustilstanden.
    - Hvis alternativet **Igangsatt kostnad** settes til **Ja** for livssyklustilstanden som en arbeidsordre oppdateres til, beregnes totalt beløp for igangsatt kost (det vil si det totale utgiftsbeløpet som den juridiske enheten har forpliktet seg til å betale), for hver arbeidsordrejobb. Det vises en melding hvis beløpet for igangsatt kost er over 0 (null). Du velger typene av igangsatte kostnader som er inkludert i hurtigfanen **Igangsetting av kostnader** i fanen **Kostkontroll** på siden **Parametere for prosjektstyring og regnskap** (**Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**).
    - Hvis alternativet **Nedetid for vedlikehold** settes til **Ja** for livssyklustilstanden som en arbeidsordre oppdateres til, utføres validering av vedlikeholdsnedetid på anleggsmidlet som er knyttet til arbeidsordren. Hvis det er gjort en registrering av vedlikeholdsnedetid, men det finnes ingen **Avsluttet**-registrering, vises en melding når arbeidsordren oppdateres til denne livssyklustilstanden.
    - Hvis standard prosjektoppsett ikke omfatter alle stadiene du trenger for aktivastyringsoppsettet, kan du sette opp brukerdefinerte prosjektstadier i fanen **Prosjektstadium** på siden **Parametere for prosjektstyring og regnskap**. Følgende illustrasjon viser fanen **Prosjektstadium** på siden **Parametere for prosjektstyring og regnskap**.

    ![Siden Definer prosjektstadier for diverse prosjekttyper.](media/10-setup-for-work-orders.png)

> [!NOTE]
> Hvis livssyklustilstanden som du oppdaterer en arbeidsordre til, er inaktiv, blir journaler som er knyttet til arbeidsordren, men som ennå ikke er postert, slettet automatisk. Denne virkemåten bidrar til å garantere automatisk opprydding av ubrukte data. (En livssyklustilstand er inaktiv hvis alternativet **Aktiv** er satt til **Nei** på hurtigfanen **Generelt** på siden **Livssyklustilstand for arbeidsordre**.)
>
> Hvis du imidlertid angir en arbeidsordre manuelt slik at den er inaktiv, blir journaler som er knyttet til arbeidsordren, men som ennå ikke er postert, **ikke** slettet automatisk. (Hvis du vil gjøre en arbeidsordre inaktiv manuelt, velger du **Aktivastyring** \> **Arbeidsordrer** \> **Alle arbeidsordrer** eller **Aktive arbeidsordrer**. Åpne arbeidsordren, og bytt til **Hode**-visning. Velg **Rediger** på hurtigfanen **Generelt**, og sett deretter alternativet **Aktiv** til **Nei**.)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Relasjoner mellom livssyklusmodeller for arbeidsordrer, arbeidsordretyper og livssyklustilstander for arbeidsordrer.

Livssyklusmodeller refererer til arbeidsflyter, og livssyklustilstander velges i en livssyklusmodell i sekvensiell rekkefølge. Livssyklusmodeller defineres på arbeidsordretyper. Arbeidsordretyper bestemmer størrelsen på eller omfanget av arbeidsflytene og arbeidsprosessene. **Vedlikehold**, som er en standard arbeidsordretype, kan for eksempel være relatert til en arbeidsordrelivssyklusmodell som har mange livssyklustilstander. Du kan derimot ha en **korrigerende** arbeidsordretype som brukes for arbeidsordrer som ikke er planlagt, eller for arbeidsordrer der jobben er fullført før arbeidsordren er gjort på grunn av en hastesituasjon. Denne arbeidsordretypen kan være knyttet til en livssyklusmodell for arbeidsordrer som bare har noen få livssyklustilstander.

Årsaken til bruk av typer er at når en type er definert for for eksempel en arbeidsordre eller et anleggsmiddel, defineres de tilknyttede arbeidsprosessene (livssyklustilstandene) automatisk. Hvis du vil ha mer informasjon om hvordan du definerer arbeidsordretyper, se [Arbeidsordretyper](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> Livssyklustilstander, livssyklusmodeller og typer gjelder for funksjonslokasjoner, anleggsmidler og meldinger, i tillegg til arbeidsordrer.

Følgende illustrasjon viser forholdet mellom arbeidsordretyper, livssyklusmodeller og livssyklustilstander.

![Siden Arbeidsordretype sammenlignet med siden Livssyklusmodeller for arbeidsordre.](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Statusgrupper for arbeidsordrer

Når du har opprettet livssyklustilstandene for arbeidsordrer som kreves for arbeidsordrene dine, kan de deles inn i livssyklusmodeller for arbeidsordrer. Du bør opprette minst én standard livssyklusmodell.

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Livssyklusmodeller**.
2. Velg **Ny** for å opprette en ny livssyklusmodell for arbeidsordre.
3. I feltet **Livssyklusmodell** angir du en ID for livssyklusmodellen.
4. Angi et navn i **Navn**-feltet.

    På hurtigfanen **Detaljer** viser feltet **Livssyklustilstander** antall livssyklustilstander som er valgt i denne livssyklusmodellen. Feltet **Arbeidsordretyper** viser antall arbeidsordretyper som bruker denne livssyklusmodellen.

5. I hurtigfanen **Livssyklustilstander** velger du livssyklustilstandene som skal inkluderes i livssyklusmodellen:

    - Hvis du vil inkludere en livssyklustilstand i livssyklusmodellen, velger du den i delen **Gjenværende livssyklustilstander**, og deretter velger du pil høyre ![Pil høyre.](media/12-setup-for-work-orders.png) for å flytte den til delen **Valgte livssyklustilstander**.
    - Hvis du vil inkludere alle tilgjengelige livssyklustilstander i livssyklusmodellen, velger du **Velg alle tilgjengelige stadier**-knappen ![Velg alle tilgjengelige stadier.](media/13-setup-for-work-orders.png). Alle livssyklustilstander flyttes til delen **Valgte livssyklustilstander**.
    - Hvis du vil fjerne en livssyklustilstand fra livssyklusmodellen, velger du den i delen **Valgte livssyklustilstander**, og deretter velger du pil venstre ![Pil venstre.](media/14-setup-for-work-orders.png) for å flytte den til delen **Gjenværende livssyklustilstander**.

6. Velg **Oppdateringer av livssyklustilstander** for å definere livssyklustilstander som kan følge en valgt livssyklustilstand.
7. I feltet **Planlagt tilstand** i hurtigfanen **Oppdateringer** velger du livssyklustilstanden som alltid skal velges for en arbeidsordre som du har fullført arbeidsordreplanlegging for, uavhengig av den forrige livssyklustilstanden til arbeidsordren.
8. I feltet **Ikke-planlagt livssyklustilstand** velger du livssyklustilstanden som alltid skal velges for en arbeidsordre hvis arbeidsordreplanlegging slettes.
9. Lagre livssyklusmodellen for arbeidsordrer.

![Siden Livssyklusmodeller for arbeidsordre.](media/15-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]