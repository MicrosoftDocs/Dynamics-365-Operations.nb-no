---
title: Endre arbeidspulje i arbeid
description: Dette emnet beskriver hvordan du kan bruke knappen for Endre arbeidspulje for arbeidselementer til å endre arbeidsutvalget for eksisterende arbeid.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 066655b58d4676bafb6e8ed8d80a95636c047444
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566029"
---
# <a name="change-work-pool-on-work"></a>Endre arbeidspulje i arbeid

[!include [banner](../includes/banner.md)]

Du kan bruke arbeidspuljer for å organisere arbeidet i grupper. Du kan for eksempel opprette en arbeidspulje for å klassifisere arbeid som skjer på en spesifikk lagerlokasjon.

Funksjonen *Endre arbeidspulje i arbeid* legger til en knapp for **Endre arbeidsutvalg** i handlingsruten for arbeidselementer. Derfor kan lagerledere enkelt endre arbeidsutvalget for eksisterende arbeid. Med denne funksjonen kan ledere reagere raskt på endringer på shop floor på lageret, og det bidrar til å forbedre muligheten til å tilpasse seg endrede situasjoner og behovet for å overføre arbeid til andre arbeidsgrupper.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Aktivere funksjonen Endre arbeidspulje i arbeid

Før du begynner å definere eller bruke denne funksjonen må du kontrollere at den er tilgjengelig i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Endre arbeidspulje i arbeid*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Konfigurere funksjonen Endre arbeidspulje i arbeid

Hvis du vil bruke denne funksjonen, må du ha noen arbeidsgrupper konfigurert. Du kan også definere arbeidsmalene, slik at de automatisk tilordner et utvalg. Hvis du vil arbeide med eksempelscenarioet som er oppgitt senere i dette emnet, setter du opp systemet som beskrevet i denne delen.

### <a name="set-up-work-pools"></a>Definere arbeidspuljer

I arbeidsutvalg kan du organisere arbeidselementer etter type. Hvis du vil arbeide med funksjonen *Endre arbeidspulje i arbeid*, må du ha minst to arbeidsgrupper tilgjengelig. Følg denne fremgangsmåten for å vise og legge til arbeidspuljer.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsutvalg**.
1. Hvis du arbeider med demonstrasjonsdata fra **USMF**-firmaet og vil arbeide deg gjennom eksempelscenarioet senere i dette emnet, legger du til to arbeidsgrupper som har følgende innstillinger:

    - Arbeidspulje 1:

        - **ID for arbeidsutvalg:** *WebShop*
        - **Beskrivelse:** *WebShop*

    - Arbeidspulje 2:

        - **ID for arbeidsutvalg:** *CallCenter*
        - **Beskrivelse:** *Telefonsenter*

1. Velg **Lagre** i handlingsruten.

### <a name="set-up-work-templates"></a>Konfigurer arbeidsmaler

For hver av arbeidsmalene kan du angi et standard arbeidsutvalg, i henhold til hva du trenger. For hver relevante mal tilordner du et arbeidsutvalg i kolonnen **ID for arbeidsutvalg**. I dette tilfellet vil alle arbeidselementer som genereres ved hjelp av en gitt mal, automatisk arve det tilordnede arbeidsutvalget. Hvis du arbeider med demonstrasjonsdata fra **USMF**-firmaet og vil arbeide deg gjennom eksempelscenarioet senere i dette emnet, følger du disse trinnene.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. I handlingsruten velger du **Rediger** for å legge siden inn i redigeringsmodus.
1. Rediger malen ved å angi følgende verdier:

    - **Arbeidsmal:** *62 Plukk til pakke*
    - **ID for arbeidsutvalg:** *WebShop*

1. Velg **Lagre**.

## <a name="example-scenario"></a>Eksempelscenario

Dette scenariet viser hvordan du kan endre strømmen av behandling for et eksisterende arbeidselement ved å endre arbeidsgruppen. Den bruker demonstrasjonsdata fra **USMF**-firmaet og innstillingene som ble foreslått tidligere i dette emnet.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Opprette en salgsordre og frigi den til lageret

1. Kontroller at det er nok lagerbeholdning for varene *A0001* og *A0002* på lager *62*. Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**, og rediger filtrene slik de vises her:

    - **Lager**-verdien begynner med *62*.
    - **Varenummer**-verdien er enten *A001* eller *A002*.

    Demonstrasjonsdata bør ha 10 som antall per stykk.

    Deretter må du opprette en salgsordre.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-007*
    - **Lager:** *62*

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Den bør inneholde en ny, tom linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *2*

1. Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.
1. På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.
1. Lukk siden.
1. Velg **Legg til linje** på **Salgsordrelinjer**-hurtigfanen for å legge til en ny linje i salgsordren. På denne linjen angir du følgende verdier:

    - **Varenummer:** *A0002*
    - **Antall:** *2*

1. Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.
1. På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.
1. Lukk siden.
1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.
1. Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID som er opprettet fra frigivelsen. Noter bølge-IDen.

### <a name="review-the-outbound-wave"></a>Se gjennom den utgående bølgen

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. I rutenettet søker du etter bølge-IDen som ble opprettet fra frigivelsen av salgsordren.
1. Velg bølge-ID for å vise detaljene.
1. I hurtigfanen **Bølgelinjer** kontrollerer du at det vises en forsendelses-ID for salgsordren.

    > [!TIP]
    > Hvis alternativet **Behandle bølge ved frigivelse til lager** er satt til *Nei* i oppsettet for forsendelsesbølgemalen, må du behandle bølgen manuelt ved å velge **Prosess** fra **Bølge**-fanen i handlingsruten for å opprette arbeid.

1. Kontroller at bølgen er behandlet. Denne behandlingen oppretter det nødvendige arbeidet.

### <a name="view-work-details-and-change-the-work-pool"></a>Vise arbeidsdetaljer og endre arbeidsutvalget

Du kan bruke **Arbeidsdetaljer**-siden til å vise arbeidet som ble opprettet, og til å administrere arbeidsutvalget.

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. Velg raden for arbeidet som nettopp ble opprettet. **Ordrenummer**-kolonnen vil vise salgsordrenummeret.

    Feltet **ID for arbeidsutvalg** blir satt til IDen for arbeidsutvalget som ble definert i arbeidsmalen.

    > [!TIP]
    > Hvis du ikke ser feltet **ID for arbeidsutvalg**, legger du til kolonnen i rutenettet og oppdaterer deretter siden.

1. Hvis du vil endre arbeidsutvalget som er knyttet til arbeids-IDen, går du til handlingsruten i fanen **Arbeid** og velger **Endre ID for arbeidsutvalg**.
1. I dialogboksen **Endre arbeidsutvalg**, i hurtigfanen **Parametere** i feltet **ID for arbeidsutvalg**, velger du *CallCenter*.
1. Velg **OK** for å bruke endringen.
1. Merk at verdien for feltet **ID for arbeidsutvalg** nå er endret til *CallCenter*.

> [!IMPORTANT]
> Når dialogboksen **Endre arbeidsutvalg** vises, kan det hende at feltet **ID for arbeidsutvalg** er tomt som standard. Hvis feltet er tomt når du velger **OK** for å bruke endringer, fjerner du arbeidsutvalget helt fra arbeidet.
>
> I tillegg til å bytte arbeidsutvalg kan du bruke denne fremgangsmåten til å legge til et arbeidsutvalg i alle arbeidselementer som ikke har et, eller til å fjerne et arbeidsutvalg fra alle arbeidselementer som har et.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]