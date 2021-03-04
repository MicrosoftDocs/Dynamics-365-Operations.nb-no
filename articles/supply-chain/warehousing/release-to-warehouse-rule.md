---
title: Frigi til lager-regel
description: Dette emnet gir informasjon om funksjonen Frigi til lager-regel, som gir fleksibilitet under frigivelse til lageret. Det legger til et konfigurasjonsalternativ som kontrollerer om systemet tillater at det frigis delvise reserverte ordrelinjer.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 27030e8dd58b290d80f6b00cbd250e09c1e50819
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434202"
---
# <a name="release-to-warehouse-rule"></a>Frigi til lager-regel

[!include [banner](../includes/banner.md)]

Funksjonen *Frigi til lager-regel* gir fleksibilitet under frigivelse til lageret. Det legger til et konfigurasjons alternativ for hvert lager. Du kan bruke dette alternativet til å angi om delvis reserverte ordrelinjer kan frigis for dette lageret. Funksjonen fungerer sammen med avanserte funksjoner for direkteoverføring i situasjoner der del av et ordrelinjeantall er merket mot en forsyningskilde, men den gjenværende delen kan behandles i lageret. Derfor kan linjen frigis slik at lagerbehandlingen av det tilgjengelige lagerantallet kan fortsette.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Aktivere og initialisere funksjonen Frigi til lager-regel

### <a name="turn-on-the-feature"></a>Aktivere funksjonen

Før du kan bruke funksjonen *Frigi til lager- regel*, må den aktiveres i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Frigi til lager*

### <a name="initialize-the-feature"></a>Initialisere funksjonen

Når funksjonen er aktivert i systemet, må du initialisere den for å sette regelen til riktig starttilstand for alle lagre.

- For lagre som ikke er aktivert for lagerstyring, settes regelen i utgangspunktet til **Ikke tilgjengelig**.
- For lagre som er aktivert for lagerstyring, settes regelen i utgangspunktet til **Tillat delvis reservasjon**

Følg denne fremgangsmåten for å initialisere funksjonen og sette Frigi til lager-regelen for alle lagre.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. På **Lagerstyringsparametere**-siden, på **Generelt**-fanen, i **Firmainformasjon**-delen, velger du koblingen for **Initialiser frigivelse til lager**-regelen. (Hvis denne koblingen ikke vises, er enten funksjonen ikke aktivert, eller den er allerede initialisert.)
1. Når du blir bedt om å bekrefte handlingen, velger du **Ja** for å initialisere funksjonen.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Angi Frigi til lager-regelen for hvert lager

Når funksjonen er aktivert og initialisert, vil alle lagre ha en startinnstilling som beskrevet i den forrige delen. Du kan endre denne innstillingen for individuelle lagre ved å følge disse trinnene.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lagre**.
1. Velg lageret som skal konfigureres.
1. Velg **Rediger** for å legge siden inn i redigeringsmodus.
1. På **Lager**-hurtigfanen, i **Reservasjoner**-delen, styrer **Krav for beholdningsreservasjon**-feltet om delvis frigivelse av ordre er tillatt. Velg én av følgende verdier:

    - **Gjelder ikke** – når funksjonen først aktiveres og initialiseres, blir denne verdien automatisk tilordnet alle lagre som ikke er aktivert for lagerstyring. Verdien kan endres. Denne verdien er ikke tilgjengelig for lagre som er aktivert for lagerstyring.
    - **Tillat delvis reservasjon** – ordrer kan frigis når et hvilket som helst antall reserveres. Systemet vil evaluere om det ikke-reserverte antallet skal merkes for avansert direkteoverføring, og vil merke dette antallet som nødvendig. Hvis det ikke finnes noen merking, vil systemet opprette arbeid bare for det reserverte antallet. Når funksjonen først aktiveres og initialiseres, blir denne verdien automatisk tilordnet alle lagre som er aktivert for lagerstyring. Denne verdien er ikke tilgjengelig for lagre som ikke er aktivert for lagerstyring.
    - **Krever full reservasjon** – ordrer kan bare frigis hvis hele antallet er reservert. De kan ikke frigis hvis det totale antallet ikke er enten fysisk reservert eller planlagt for direkteoverføring. Denne verdien er ikke tilgjengelig for lagre som ikke er aktivert for lagerstyring.

1. Velg **Lagre**.

## <a name="scenarios"></a>Scenarier

Denne delen inneholder to scenarier som du kan arbeide gjennom for å lære hva funksjonen gjør, og hvordan du bruker den.

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom disse scenariene ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke disse scenariene som en veiledning for å bruke funksjonen når du arbeider i et produksjonssystem. I så fall må du imidlertid erstatte dine egne verdier, og det kan hende du mangler noen typer obligatoriske oppføringer som standard demonstrasjonsdata gir.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>Scenario 1: Krev fullstendig frigivelse (ingen planlagt direkteoverføring)

Dette scenariet viser hvordan funksjonen fungerer for lagre som er satt til **Krev full reservasjon**.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lagre**.
1. For lager _62_ angir du **Krav for beholdningsreservasjon**-feltet til **Krev full reservasjon**, som beskrevet i delen [Angi Frigi til lager-regelen for hvert lager](#set-option-warehouse) tidligere i dette emnet.
1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en salgsordre.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til _US-004_.
    - På hurtigfanen **Generelt** angir du **Lager**-feltet til _62_.

1. Velg **OK** for å opprette den nye salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Det inneholder en tom linje i rutenettet i **Salgsordrelinjer**-delen. På denne linjen angir du følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *2*

1. Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Varenummer:** *A0002*
    - **Antall:** *2*

1. Velg den første ordrelinjen og deretter på **Beholdning**-menyen over rutenett, velger du **Reservasjon**.
1. På **Reservasjon**-siden velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Ikke reserver den andre ordrelinjen.
1. Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.
1. Legg merke til at du får følgende feilmelding: Hele antall må være fysisk reservert." Derfor oppretter ikke systemet noe arbeid, forsendelse eller last for ordren.

    > [!NOTE]
    > Du vil motta samme feilmelding hvis du delvis reserverer den andre linjen.

### <a name="scenario-2-allow-partial-release"></a>Scenario 2: Tillat delvis frigivelse

Dette scenariet viser hvordan funksjonen fungerer for lagre som er satt til **Tillat delvis frigivelse**.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lagre**.
1. For lager _62_ angir du **Krav for beholdningsreservasjon**-feltet til **Tillat delvis reservasjon**, som beskrevet i delen [Angi Frigi til lager-regelen for hvert lager](#set-option-warehouse) tidligere i dette emnet.
1. På samme måte som i det [forrige scenariet](#scenario1), går du til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**, og oppretter du en salgsordre for kundekonto _US-004_ fra lager _62_. Legg til følgende to ordrelinjer:

    - **Linje 1:** Angi **Varenummer**-feltet til _A0001_, **Antall**-feltet til _2_ og **Enhet**-feltet til _Pcs_.
    - **Linje 2:** Angi **Varenummer**-feltet til _A0002_, **Antall**-feltet til _2_ og **Enhet**-feltet til _Pcs_.

1. På samme måte som i [forrige scenario](#scenario1), reserverer du hele antallet for ordrelinje 1, men ikke reserver ordrelinje 2.
1. Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.
1. Legg merke til at du ikke får en feilmelding denne gangen. I stedet oppretter systemet arbeid, forsendelser og laster etter behov, og viser resultatene.
1. Hvis du vil vise informasjon om forsendelse, last og arbeid, bruker du alternativene på **Lager**-menyen over rutenettet:

    - **Linje 1:** Tre alternativer er tilgjengelige: **Forsendelsesdetaljer**, **Lastdetaljer** og **Arbeidsdetaljer**. Velg hvert alternativ for å vise detaljene for forsendelsen, lasten og arbeidet som ble opprettet da ordren ble frigitt til lageret.
    - **Linje 2:** Bare **Arbeidsdetaljer**-alternativet er tilgjengelig. Velg den, og legg merke til at det ikke er opprettet noe arbeid, fordi ingen beholdning er reservert. Derfor ble ingen forsendelse eller last opprettet heller.

> [!NOTE]
> Det samme resultatet forventes når den andre linjen er delvis reservert. I dette tilfellet vil arbeidet bli opprettet for det reserverte linjeantallet, men ikke for det ikke-reserverte antallet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]