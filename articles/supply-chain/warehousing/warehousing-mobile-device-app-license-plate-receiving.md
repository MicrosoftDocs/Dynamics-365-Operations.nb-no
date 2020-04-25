---
title: Nummerskiltmottak via mobilappen for lagerstyring
description: Dette emnet forklarer hvordan du konfigurerer mobilappen for lagerstyring for å støtte bruk av en prosess for nummerskiltmottak for å motta fysisk beholdning.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261362"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a>Nummerskiltmottak via mobilappen for lagerstyring

Dette emnet forklarer hvordan du konfigurerer mobilappen for lagerstyring slik at den støtter bruk av en prosess for nummerskiltmottak for å motta fysisk beholdning.

Du kan bruke denne funksjonaliteten til raskt å registrere mottak av innkommende beholdning som er relatert til et forhåndsvarsel for forsendelse. Systemet oppretter automatisk et forhåndsvarsel for forsendelse når lagerstyringsprosesser brukes til å sende en overføringsordre. For bestillingsprosessen kan et forhåndsvarsel for forsendelse registreres manuelt, eller det kan importeres automatisk ved hjelp av en innkommende dataenhetsprosess for forhåndsvarsel for forsendelse.

Dataene fra forhåndsvarselet for forsendelse knyttet til laster og forsendelser via *emballasjestrukturer*, der paller (overordnede nummerskilt) kan inneholde saker (nestede nummerskilt).

> [!NOTE]
> Hvis du vil redusere antallet lagertransaksjoner når det brukes emballasjestrukturer som har nestede nummerskilt, registrerer systemet den fysiske lagerbeholdningen på det overordnede nummerskiltet. For å utløse flytting av den fysiske lagerbeholdningen fra det overordnede nummerskiltet til de nestede nummerskiltene, basert på pakkestrukturdataene, må mobilenheten inneholde et menyelement som er basert på arbeidsopprettingsproessen *Pakk til nestede nummerskilt*.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Vise eller hoppe over mottakssammendragssiden

Du kan bruke funksjonen *Kontroller om det skal vises en mottakssammendragsside på mobilenheter* for å dra nytte av en mer detaljert flyt i appen for lagerstyring som en del av prosessen for mottak av nummerskilt.

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Kontroller om det skal vises en mottakssammendragsside på mobilenheter*

Når denne funksjonen er aktivert, vil menyelementer på mobilenheter for mottak av nummerskilt eller mottak og plassering av nummerskilt gi en innstilling for **visning av mottakssammendragsside**. Denne innstillingen har følgende alternativer:

- **Vis et detaljert sammendrag** – Ved nummerskiltmottak får arbeiderne se en ekstra side som viser hele forhåndsvarselet om forsendelse.
- **Hopp over sammendrag** – Arbeiderne ser ikke hele forhåndsvarselet om forsendelse. Lagerarbeiderne kan heller ikke angi en disposisjonskode eller legge til unntak under mottaksprosessen.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret

En mottaksprosess for nummerskilt kan ikke brukes hvis et forhåndsvarsel for forsendelse inneholder en nummerskilt-ID som allerede finnes og har fysiske lagerbeholdningsdata på en annen lagerlokasjon enn lagerlokasjonen der registreringen av nummerskiltet skjer.

For scenarier for overføringsordrer der transittlageret ikke sporer nummerskilt (og derfor ikke ikke sporer fysisk lagerbeholdning per nummerskilt), kan du bruke de funksjonen *Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret* å hindre fysiske lagerbeholdningsoppdateringer av nummerskilt som er under transitt.

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret*

Følg denne fremgangsmåten for å administrere funksjonaliteten når denne funksjonen er tilgjengelig.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. I kategorien **Generelt**, på hurtigfanen **Nummerskilt**, angir du feltet **Policy for lagernummerskilt i transitt** til en av følgende verdier:

    - **Tillat gjenbruk av ikke-sporede nummerskilt** – Systemet fungerer på samme måte som når unksjonen den *Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret* ikke er tilgjengelig. Denne verdien er standardinnstillingen når du aktiverer funksjonen for første gang.
    - **Hindre gjenbruk av ikke-sporede nummerskilt** – Bare lagerbeholdninger som er relatert til et sendt nummerskilt, vil bli tillatt på destinasjonslageret før overføringsordren er mottatt.

## <a name="more-information"></a>Mer informasjon

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Hvis du vil ha mer informasjon om menyelementer for mobilenheter, kan du se [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md).
