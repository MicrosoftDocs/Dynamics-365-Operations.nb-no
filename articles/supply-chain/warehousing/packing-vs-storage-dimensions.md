---
title: Angi ulike dimensjoner for pakking og lagring
description: Dette emnet viser hvordan du angir hvilken prosess (pakking, lagring eller nestet pakking) hver angitte dimensjon skal brukes til.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 004d9b4522335b481b640ef0fe35f4db66e3c9f5
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078294"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Angi ulike dimensjoner for pakking og lagring

[!include [banner](../includes/banner.md)]

Noen varer pakkes eller lagres på en slik måte at du kanskje må spore fysiske dimensjoner ulikt for hver av flere forskjellige prosesser. Med funksjonen *Dimensjoner for pakking av produkt* kan du definere én eller flere dimensjonstyper for hvert produkt. Hver dimensjonstype gir et sett med fysiske mål (vekt, bredde, dybde og høyde) og fastsetter prosessen der de fysiske målingsverdiene gjelder. Når denne funksjonen er aktivert, støtter systemet følgende dimensjonstyper:

- *Lagring* - Lagringsdimensjoner brukes sammen med lokasjonsvolummål til å fastsette hvor mange eksemplarer av hver vare som kan lagres på forskjellige lagerlokasjoner.
- *Pakking* – Pakkingsdimensjoner brukes under containerbruk og den manuelle pakkeprosessen til å fastsette hvor mange eksemplarer av hver vare som får plass i forskjellige containertyper.
- *Nestet pakking* – Dimensjoner for nestet pakking brukes når pakkeprosessen inneholder flere nivåer.

*Lagring* sdimensjoner støttes selv om funksjonen *Dimensjoner for pakking av produkt* ikke er aktivert. Du konfigurerer disse ved å bruke siden **Fysiske dimensjoner** i Supply Chain Management. Disse dimensjonene brukes av alle prosesser der dimensjoner for pakking og nestet pakking ikke er angitt.

Du konfigurerer dimensjoner for *pakking* og *nestet pakking* ved å bruke siden **Fysiske produktdimensjoner**, som legges til når du aktiverer funksjonen *Dimensjoner for pakking av produkt*.
Dette emnet inneholder et scenario som illustrerer hvordan du bruker denne funksjonen.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Aktivere funksjonen for dimensjoner for pakking av produkt

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Dimensjoner for pakking av produkt*

## <a name="example-scenario"></a>Eksempelscenario

### <a name="set-up-the-scenario"></a>Definer scenariet

Før du kan kjøre eksempelscenarioet, må du klargjøre systemet som beskrevet i denne delen.

#### <a name="enable-demo-data"></a>Aktivere demonstrasjonsdata

For å kunne arbeide deg gjennom dette scenariet ved å bruke de angitte demonstrasjonspostene og -verdiene som er angitt her, må du være på et system der standard [demonstrasjonsdata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten *USMF* før du begynner.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Legge en ny fysisk dimensjon til et produkt

Legg til en ny fysisk dimensjon for et produkt ved å gjøre følgende:

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg produktet med **Varenummer** *A0001*.
1. I handlingsruten i åpner du fanen **Administrer lager**, og i gruppen **Lager** velger du **Fysiske produktdimensjoner**.
1. Siden **Fysiske produktdimensjoner** åpnes. Velg **Ny** i handlingsruten for å legge til en ny dimensjon i rutenettet med følgende innstillinger:
    - **Fysisk dimensjonstype** – *Pakking*
    - **Fysisk enhet** – *stk.*
    - **Vekt** – *4*
    - **Vektenhet** – *kg*
    - **Dybde** – *3*
    - **Høyde** – *4*
    - **Bredde** – *3*
    - **Lengde** – *cm*
    - **Volumenhet** – *cm3*

**Volum**-feltet beregnes automatisk basert på innstillingene for **Dybde**, **Høyde** og **Bredde**.

#### <a name="create-a-new-container-type"></a>Opprett en ny containertype

Gå til **Lagerstyring \> Oppsett \> Containere \> Containertyper**, og opprett en ny post med følgende innstillinger:

- **Containertypekode** – *Kort eske*
- **Beskrivelse** – *Kort eske*
- **Maksimal nettovekt** – *50*
- **Volum** – *144*
- **Lengde** – *6*
- **Bredde** – *6*
- **Høyde** – *4*

#### <a name="create-a-container-group"></a>Opprette en containergruppe

Gå til **Lagerstyring \> Oppsett \> Containere \> Containergrupper**, og opprett en ny post med følgende innstillinger:

- **Containergruppe-ID** – *Kort eske*
- **Beskrivelse** – *Kort eske*

Legg til en ny linje i **Detaljer**-delen. Sett **Containertype** til *Kort eske*.

#### <a name="set-up-a-container-build-template"></a>Definere en mal for containerversjon

Gå til **Lagerstyring \> Oppsett \> Containere \> Maler for containerversjoner** og velg **Esker**. Endre **Containergruppe-ID** til *Kort eske*.

### <a name="run-the-scenario"></a>Kjøre scenarioet

Når du har klargjort systemet som beskrevet i den forrige delen, er du klar til å kjøre scenarioet som beskrevet i neste del.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Opprette en salgsordre og en forsendelse

I denne prosessen skal du opprette en forsendelse basert på dimensjoner for vare *pakking* der høyden er mindre enn 3.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-001*
    - **Lager:** *63*

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Den bør inneholde en ny, tom linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *5*

1. På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.
1. På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.
1. Lukk siden.
1. I handlingsruten åpner du **Lager**-fanen og velger **Frigi til lager** for å opprette arbeidet for lageret.
1. I hurtigfanen **Salgsordrelinje** velger du **Lager \> Forsendelsesdetaljer**.
1. I handlingsruten åpner du **Transport**-fanen og velger **Vis containere**. Bekreft at varen ble containerbrukt i de to *Kort eske*-containerne.

#### <a name="place-an-item-into-storage"></a>Plassere en vare på lager

1. Åpne mobilenheten, logg deg på lager 63, og gå til **Lager \> Juster inn**.
1. Angi **Lok.** = *SHORT-01*. Lag et nytt nummerskilt med **Vare** = *A0001* og **Antall** = *1 stk.*
1. Velg **OK**. Du får en feilmelding om at lokasjonen SHORT-01 mislyktes fordi vare A0001 ikke passer i lokasjonens angitte dimensjoner. Dette skjer fordi dimensjoner av typen *Lagring* for produktet er større enn dimensjonene som er angitt i lokasjonsprofilen.
