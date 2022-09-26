---
title: Bruke partidisposisjonskoder til å merke partier som tilgjengelige eller ikke tilgjengelige
description: Denne artikkelen beskriver hvordan du definerer og bruker partidisposisjonskoder til å merke partier som tilgjengelige eller ikke tilgjengelige i hovedplanlegging, reservering, plukking og/eller forsendelse.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542474"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Bruke partidisposisjonskoder til å merke partier som tilgjengelige eller ikke tilgjengelige

Denne artikkelen beskriver hvordan du definerer og bruker *partidisposisjonskoder*. Hver partidisposisjonskode har statusen *Tilgjengelig* eller *Ikke tilgjengelig*. Du tilordner partidisposisjonskoder til lagerpartier for å angi om hvert parti er tilgjengelig for hovedplanlegging, reservering, plukking og/eller forsendelse.

Hvis du vil bruke partidisposisjonskoder, må du definere kodene og tilordne dem til partiene du vil administrere.

## <a name="set-up-batch-disposition-codes"></a>Definer partidisposisjonskoder

Du må definere hver partidisposisjonskode som du vil bruke i systemet. Du kan opprette så mange koder som du vil. (Du kan for eksempel opprette koder for å identifisere de forskjellige årsakene til at et parti kan være tilgjengelig eller ikke tilgjengelig). Du har imidlertid ofte bare to koder: én for *tilgjengelig* og én for *utilgjengelig*. Du kan også opprette egendefinerte koder som gjør det mulig å bruke et parti for enkelte operasjoner, men ikke andre.

Følg disse trinnene for å konfigurere partidisposisjonskoder.

1. Gå til **Lagerstyring \> Oppsett \> Parti \> Partidisposisjonsstandard**.
1. På siden **Partidisposisjonsstandard** vises de gjeldende partidisposisjonskodene, og du kan opprette, slette og redigere dem. Følg ett av disse trinnene:

    - Hvis du vil redigere en eksisterende kode, velger du den i listeruten.
    - For å opprette en ny kode velger du **Ny** i handlingsruten.

1. Angi følgende felter i hodet til den nye eller valgte koden:

    - **Partidisposisjonskode** – Angi visningsnavnet for koden.
    - **Beskrivelse** – Beskriv hvordan koden skal brukes.
    - **Partidisposisjonsstatus** – Velg statusen som gjelder for partier som koden er tilordnet til:

        - *Utilgjengelig* – Partiene kan ikke brukes til hovedplanlegging, reservering, plukking eller forsendelse. Når du velger denne verdien, blir alle **Blokker**-alternativene på hurtigfanen **Oppsett** angitt til *Ja*, og alle **Nettbar**-alternativer blir angitt til *Nei*. Du kan imidlertid endre noen av disse innstillingene for å legge til unntak.
        - *Tilgjengelig* – Partiene kan brukes til hovedplanlegging, reservering, plukking og/eller forsendelse. Når du velger denne verdien, blir alle **Blokker**-alternativene på hurtigfanen **Oppsett** angitt til *Nei*, og alle **Nettbar**-alternativer blir angitt til *Ja*. Disse innstillingene vil være skrivebeskyttet når feltet **Partidisposisjonsstatus** er satt til *Tilgjengelig*.

1. Hvis du setter feltet **Partidisposisjonsstatus** til *Ikke tilgjengelig*, kan du tilpasse blokkeringsstatusen for hver operasjon (reserver, plukk og send) for hver bestillingstype (salg, overføring og produksjon). For produksjonsordrer kan du velge å blokkere eller fjerne blokkeringen for produksjonsplukkingsjournalen. Du kan også velge å blokkere eller fjerne blokkeringen av hovedplanleggingen. Bruk alternativene på hurtigfanen **Oppsett** til å blokkere eller fjerne blokkeringen for hver operasjon etter behov. Sett alternativet **Nettbar** til *Ja* for å aktivere hovedplanlegging, eller sett det til *Nei* for å blokkere hovedplanlegging.

## <a name="assign-batch-disposition-codes-to-batches"></a>Tilordne partidisposisjonskoder til partier

Når du har definert partidisposisjonskodene du trenger, følger du denne fremgangsmåten for å tilordne dem til partier.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Partier**.
1. Velg ett eller flere partier som du vil tilordne en partidisposisjonskode til.
1. I handlingsruten på **Tilbakestill**-fanen velger du **Tilbakestill partidisposisjonskode**.
1. I dialogboksen **Endre begrensningene for lagerpartiet** setter du feltet **Ny partidisposisjonskode** til navnet på koden du vil tilordne.
1. Velg **OK** for ta i bruk den nye innstillingen og lagre endringen.

    På **Partier**-siden oppdateres verdiene i kolonnene **Partidisposisjonskode** og **Partidisposisjonsstatus** slik at de gjenspeiler de nye innstillingene for de valgte partiene.

## <a name="master-planning-example"></a>Eksempel på hovedplanlegging

Dette eksemplet viser hvordan partidisposisjonskoder kan påvirke hovedplanlegging.

For dette eksemplet defineres partidisposisjonskoder på følgende måte:

- *P-Tilgjengelig:*

    - **Partidisposisjonsstatus:** *Tilgjengelig*
    - **Nettbar:** *Ja*

- *P-Ikke tilgjengelig:*

    - **Partidisposisjonsstatus:** *Ikke tilgjengelig*
    - **Nettbar:** *Nei*

Det finnes et produkt (*Produkt-1*) med to partier: *Parti-A* og *Parti-B*. Disse partiene er satt opp på følgende måte:

- *Parti-A:*

    - **Partidisposisjonskode:** *P-Tilgjengelig*
    - **Antall på lager:** 1

- *Parti-B:*

    - **Partidisposisjonskode:** *P-Ikke tilgjengelig*
    - **Antall på lager:** 1

Det finnes en salgsordre (*SO1*) for et antall på 2 av produktet *Produkt-1*. Leveringsdatoen er tre dager fra i dag.

Du kjører hovedplanlegging og angir følgende verdier som er relevante for dette eksemplet:

- **Planlagt ordre:** *Bestilling*
- **Etterfyllingsstrategi:** *Krav*
- **Leveringstid:** *0*

Som et resultat av planleggingskjøringen bruker systemet det tilgjengelige partiet (*Parti-A*) til å dekke et antall på 1 av produktet *Produkt-1* for salgsordren *SO1*. Det kan imidlertid ikke bruke *Parti-B*, fordi dette partiet er merket som ikke tilgjengelig for planlegging. For å dekke restantallet oppretter systemet derfor et bestillingsforslag (*PPO1*) for et nytt parti av produktet *Produkt-1*.

Illustrasjonen nedenfor viser en tidslinje for planleggingsresultatet.

![Eksempel som viser hvordan partidisposisjonskoder kan påvirke hovedplanlegging.](media/batch-codes-planning-example.png "Eksempel som viser hvordan partidisposisjonskoder kan påvirke hovedplanlegging")
