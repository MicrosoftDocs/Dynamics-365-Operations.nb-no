---
title: Nummerskiltmottak via mobilappen Lagerstyring
description: Dette emnet forklarer hvordan du konfigurerer mobilappen Lagerstyring for å støtte bruk av en prosess for nummerskiltmottak for å motta fysisk beholdning.
author: perlynne
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6663188334c70035906f924c7850a0dc5002f306
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103069"
---
# <a name="license-plate-receiving-via-the-warehouse-management-mobile-app"></a>Nummerskiltmottak via mobilappen Lagerstyring

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer mobilappen Lagerstyring slik at den støtter bruk av en prosess for nummerskiltmottak for å motta fysisk beholdning.

Du kan bruke denne funksjonaliteten til raskt å registrere mottak av innkommende beholdning som er relatert til et forhåndsvarsel for forsendelse. Systemet oppretter automatisk et forhåndsvarsel for forsendelse når lagerstyringsprosesser brukes til å sende en overføringsordre. For bestillingsprosessen kan et forhåndsvarsel for forsendelse registreres manuelt, eller det kan importeres automatisk ved hjelp av en innkommende dataenhetsprosess for forhåndsvarsel for forsendelse.

Dataene fra forhåndsvarselet for forsendelse knyttet til laster og forsendelser via *emballasjestrukturer*, der paller (overordnede nummerskilt) kan inneholde saker (nestede nummerskilt).

> [!NOTE]
> Hvis du vil redusere antallet lagertransaksjoner når det brukes emballasjestrukturer som har nestede nummerskilt, registrerer systemet den fysiske lagerbeholdningen på det overordnede nummerskiltet. For å utløse flytting av den fysiske lagerbeholdningen fra det overordnede nummerskiltet til de nestede nummerskiltene, basert på pakkestrukturdataene, må mobilenheten inneholde et menyelement som er basert på arbeidsopprettingsproessen *Pakk til nestede nummerskilt*.

## <a name="warehousing-mobile-device-app-processing"></a>Behandle lager i en app for mobilenheter

Når en arbeider skanner en innkommende nummerskilt-ID, initialiserer systemet en mottaksprosess for nummerskiltet. Basert på denne informasjonen blir innholdet på nummerskiltet (data som kommer fra ASN) fysisk registrert på mottaksstedet. Arbeidsflytene som følger, avhenger av prosesseringsbehovene til bedriften din.

## <a name="work-policies"></a>Arbeidspolicyer

Som med (for eksempel) menyelementprosessen *Ferdigmeld* for mobilenheter, støtter mottaksprosessen for nummerskilt flere arbeidsflyter basert på det definerte oppsettet.

### <a name="work-policies-with-work-creation"></a>Arbeidspolicyer med arbeidsopprettelse

Når du registrerer innkommende varer ved hjelp av en arbeidspolicy som oppretter arbeid, genererer og plasserer systemet arbeidsposter for hver registrering. Hvis du bruker *Mottak og plassering av nummerskilt*-arbeidsprosess, blir registrering og plassering behandlet som én enkelt operasjon ved hjelp av ett enkelt menyelement på en mobilenhet. Hvis du bruker *Mottak av nummerskilt*-prosessen, blir mottaks- og plasseringsprosessene behandlet som to forskjellige lageroperasjoner med hvert sitt menyelement på en mobilenhet.

### <a name="work-policies-without-work-creation"></a>Arbeidspolicyer uten arbeidsopprettelse

Du kan bruke mottaksprosessen for nummerskilt uten å opprette arbeid. Hvis du definerer arbeidspolicyer som har arbeidsordretype *Overføringsmottak* og/eller *Bestillinger*, og du bruker prosessen for *Mottak (og plassering) av nummerskilt*, vil ikke følgende to prosesser i Warehousing-mobilappen opprette arbeid. I stedet registrerer de bare den innkommende fysiske beholdningen på nummerskiltet på mottaksstedet.

- *Mottak av nummerskilt*
- *Mottak og plassering av nummerskilt*

> [!NOTE]
> - Du må definere minst én lokasjon for en arbeidspolicy i **Beholdningslokasjoner**-delen. Du kan ikke angi samme plassering for flere arbeidspolicyer.
> - Alternativet **Skriv ut etikett** for menyelementer for lagerstyring på mobilenheter skriver ikke ut en nummerskiltetikett uten arbeidsopprettelse.

Hvis du vil gjøre denne funksjonaliteten tilgjengelig i systemet, må du aktivere *Forbedringer for nummerskiltmottak*-funksjonen i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Motta beholdning på en lokasjon som ikke sporer nummerskilt

Det er mulig å bruke en lagerlokasjon som er tilordnet en lokasjonsprofil, selv om **Bruk sporing av nummerskilt** ikke er aktivert. Når du mottar beholdningen, kan du derfor registrere den tilgjengelige beholdningen direkte på en lokasjon uten arbeidsopprettelse.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Legge til menyelementer for mobilenheter for hver mottakslokasjon på et lager

Ved hjelp av *Forbedringer for nummerskiltmottak* kan du motta en hvilken som helst lokasjon i et lager ved å legge til lokasjonsspesifikke menyelementer for mottak (og plassering) av nummerskilt i Warehousing-mobilappen. Tidligere støttet systemet bare mottak på standardlokasjonen som er definert for hvert lager. Når denne funksjonen er aktivert, inneholder imidlertid menyelementer for mottak (og plassering) av skiltnummer på mobilenheter nå alternativet **Bruk standarddata**, som lar deg velge en egen definert "til"-plassering for hvert menyelement. (Dette alternativet var allerede tilgjengelig for enkelte andre typer menyelementer.)

Hvis du vil gjøre denne funksjonaliteten tilgjengelig i systemet, må du aktivere *Forbedringer for nummerskiltmottak*-funksjonen i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="show-or-skip-the-receiving-summary-page"></a>Vise eller hoppe over mottakssammendragssiden

Du kan bruke funksjonen *Kontroller om det skal vises en mottakssammendragsside på mobilenheter* for å dra nytte av en mer detaljert flyt i mobilappen Lagerstyring som en del av prosessen for mottak av nummerskilt.

Når denne funksjonen er aktivert, vil menyelementer på mobilenheter for mottak av nummerskilt eller mottak og plassering av nummerskilt gi en innstilling for **visning av mottakssammendragsside**. Denne innstillingen har følgende alternativer:

- **Vis et detaljert sammendrag** – Ved nummerskiltmottak får arbeiderne se en ekstra side som viser hele forhåndsvarselet om forsendelse.
- **Hopp over sammendrag** – Arbeiderne ser ikke hele forhåndsvarselet om forsendelse. Lagerarbeiderne kan heller ikke angi en disposisjonskode eller legge til unntak under mottaksprosessen.

Hvis du vil bruke denne funksjonaliteten, må funksjonen *Kontroller om det skal vises en mottakssammendragsside på mobilenheter* være aktivert for systemet. Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Kontroller om det skal vises en mottakssammendragsside på mobilenheter* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret

En mottaksprosess for nummerskilt kan ikke brukes hvis et forhåndsvarsel for forsendelse inneholder en nummerskilt-ID som allerede finnes og har fysiske lagerbeholdningsdata på en annen lagerlokasjon enn lagerlokasjonen der registreringen av nummerskiltet skjer.

For scenarier for overføringsordrer der transittlageret ikke sporer nummerskilt (og derfor ikke ikke sporer fysisk lagerbeholdning per nummerskilt), kan du bruke de funksjonen *Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret* å hindre fysiske lagerbeholdningsoppdateringer av nummerskilt som er under transitt. Hvis du vil gjøre denne funksjonaliteten tilgjengelig, må funksjonen *Hindre at nummerskilt som er sendt med overføringsordrer, brukes i andre lagre enn mållageret* aktiveres for systemet. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter den i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Følg denne fremgangsmåten for å administrere funksjonaliteten når denne funksjonen er tilgjengelig.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. I fanen **Generelt**, på hurtigfanen **Nummerskilt**, angir du feltet **Policy for lagernummerskilt i transitt** til en av følgende verdier:

    - **Tillat gjenbruk av ikke-sporede nummerskilt** – Systemet fungerer på samme måte som når unksjonen den *Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret* ikke er tilgjengelig. Denne verdien er standardinnstillingen når du aktiverer funksjonen for første gang.
    - **Hindre gjenbruk av ikke-sporede nummerskilt** – Bare lagerbeholdninger som er relatert til et sendt nummerskilt, vil bli tillatt på destinasjonslageret før overføringsordren er mottatt.

## <a name="more-information"></a>Mer informasjon

Hvis du vil ha mer informasjon om menyelementer for mobilenheter, kan du se [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md).

Hvis du vil ha mer informasjon om *Ferdigmeld*-produksjonsscenariet, kan du se [Oversikt over policyer for lagerarbeid](warehouse-work-policies.md).

For mer informasjon om innkommende lastadministrasjon for lagerstyring, se [Lagerhåndtering av innkommende laster for bestillinger](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]