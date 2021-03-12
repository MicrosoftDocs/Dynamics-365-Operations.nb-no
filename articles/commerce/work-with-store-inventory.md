---
title: Butikklagerstyring
description: Dette emnet beskriver hvilke typer dokumenter du kan bruke til å styre lager.
author: rubencdelgado
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 616fb8975543344657c00c419ce7279658694675
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989482"
---
# <a name="commerce-inventory-management"></a>Commerce-lagerstyring

[!include [banner](includes/banner.md)]

Når du jobber med lager i Microsoft Dynamics 365 Commerce og bruker alle Commerce-programmene som er koblet til en Commerce Scale Unit (CSU), er det viktig å vite at ordrebehandlingslogikken i CSU gir begrenset støtte for enkelte lagerdimensjoner og enkelte lagervaretyper. Commerce-programmer støtter ikke alle mulighetene for varekonfigurasjon som er tilgjengelige via alternativene for varekonfigurasjon under Dynamics 365 Supply Chain Management.

Commerce-programmer som kjører på CSU, støtter ikke følgende produktdimensjoner og varekonfigurasjoner:

- Produktdimensjon for konfigurasjon og stykklistevarer (bortsett fra produkter for detaljhandelssett, som bruker noen komponenter i stykklisterammeverket)
- Faktisk vekt-varer
- Dimensjonskontrollerte varer for versjonprodukt

Commerce-programmer som kjører på CSU, støtter ikke følgende sporingsdimensjoner:
- Eierdimensjon

- Salgsstedsprogrammet kan tilby begrenset støtte for følgende dimensjoner. Salgsstedet kan automatisk angi noen av dimensjonene i lagertransaksjoner basert på konfigurasjonen av lager- eller butikkoppsettet. Salgsstedet støtter imidlertid ikke dimensjonene fullstendig på samme måte som hvis en salgstransaksjon angis manuelt i Commerce Headquarters. 

- **Lagerlokasjon** – Når de bruker de nye POS-operasjonene [Innkommende operasjon](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) og [Utgående operasjon](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), kan brukerne velge en lagerlokasjon for å motta varer til eller levere utgående overføringsordrevarer fra. Hvis de bruker den foreldede operasjonen **Plukk og mottak**, er støtte for begrenset lokasjonsadministrasjon tilgjengelig for mottak og forsendelse av utgående overføringer. Denne støtten er bare tilgjengelig hvis alternativet **Bruk lagerstyringsprosess** er aktivert for varen og butikklageret. En lagerlokasjon kan for øyeblikket ikke brukes med lager operasjonen **Lagerantall** eller **Beholdningsoppslag**.

- **Nummerskilt** – Nummerskilt gjelder bare når alternativet **Bruk lagerstyringsprosess** er aktivert for varen og butikklageret. Hvis lageret mottas i et butikklager ved hjelp av operasjonen **Innkommende operasjon** eller **Plukk og mottak** der lagerstyringsprosessen er aktivert, og lokasjonen som er valgt til å motta varen, er koblet til en lokasjonsprofil som krever nummerskiltkontroll, bruker POS-appen systematisk et nummerskilt på mottakslinjen. POS-brukere kan ikke endre eller behandle disse nummerskiltdataene. Hvis full administrasjon av nummerskilt er nødvendig, anbefales det at butikken bruker [lagerappen](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) eller Back Office-klienten til å administrere mottak av disse varene.

- **Serienummer** – POS-appen gir begrenset støtte for registrering av ett serienummer på en transaksjonssalgslinje for ordrer som er opprettet i POS og har serialiserte varer. Dette serienummeret valideres ikke mot registrerte serienumre som allerede finnes på lageret. Hvis en salgsordre opprettes i telefonsenterkanalen eller oppfylles gjennom Enterprise Resource Planning (ERP), og flere serienumre registreres på en enkelt salgslinje under oppfyllelsesprosessen i ERP, vil ikke de serienumrene kunne brukes eller valideres hvis en retur behandles for ordren i POS. Når lager mottas ved hjelp av operasjonen **Innkommende operasjon**, kan brukere [registrere eller bekrefte de mottatte serienumrene](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).

- **Parti-ID** – Salgsstedsprogrammet gir begrenset støtte under utdragsposteringsprosessen hvis en partikontrollert vare blir solgt, men salgsstedsbrukere ikke kan definere parti-IDen som ble solgt eller plukket ved bruk av salgsstedsprogrammet.

- **Lagerstatus** – For varer som bruker lagerstyringsprosessen og krever en lagerstatus, kan ikke dette statusfeltet angis eller endres gjennom POS-appen. Standard lagerstatus som definert i butikklagerkonfigurasjonen, vil bli brukt når varer mottas på lageret.

> [!NOTE]
> Alle organisasjoner må teste varekonfigurasjoner gjennom Commerce-apper i utviklings- eller testmiljøer før de distribuerer disse varekonfigurasjonene til produksjonsmiljøer. Test varene ved å bruke dem til å utføre vanlige hentesalgstransaksjoner på salgsstedet, og opprett kundeordrer (om nødvendig) via salgsstedet, telefonsenteret eller e-handel for å validere at de støttes fullt ut. Du bør også teste oppfyllelses- og lagerprosesser for POS (for eksempel lagermottak og ordreoppfyllelsesoperasjoner) før du distribuerer nye varekonfigurasjoner for å sikre at POS-appen kan støtte dem. Testingen må inkludere kjøring av en fullstendig utdrags-/ordreposteringsprosess i testmiljøet og bekrefte at ingen posteringsproblemer oppstår når ordrer for disse varene opprettes og posteres i Commerce Headquarters.
>
> Hvis varer konfigureres på en måte som ikke støttes av Commerce-programmene, og det ikke er mulig å teste disse på riktig måte, kan det oppstå datafeil som ikke er lette å korrigere, eller som ikke kan korrigeres i det hele tatt.

## <a name="purchase-orders"></a>Bestillinger

Bestillinger opprettes i Commerce Headquarters. Hvis et butikklager er inkludert i bestillingshodet eller på bestillingslinjer, kan linjene mottas i butikken ved hjelp av operasjonen [Innkommende operasjon](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) i POS. 

## <a name="transfer-orders"></a>Overføringsordrer

Overføringsordrer kan opprettes i Commerce Headquarters eller via operasjonen [Innkommende operasjon](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) eller [Utgående operasjon](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) i POS. Bruk POS-operasjonen **Innkommende operasjons** til å opprette en forespørsel om overføringsordre der det er sendt lager til butikken fra et annet lager eller butikklokasjon. Bruk POS-operasjonen **Utgående operasjons** til å opprette en forespørsel om overføringsordre der det blir sendt lager fra butikken til et annet lager eller butikklokasjon. Etter at det er opprettet en overføringsordre for en butikk, kan den butikken administrere mottak av lager for overføringsordren via operasjonen **Innkommende operasjon** i POS. Hvis butikken sender lager til en annen lokasjon, brukes operasjonen **Utgående operasjon** i POS til å administrere denne butikkens utgående forsendelsesprosess.

## <a name="stock-counts"></a>Lagerantall

Lagertellinger kan være planlagt eller ikke planlagt. Planlagte lageropptellinger opprettes via Commerce Headquarters ved å opprette et dokument av typen opptellingsjournal som er knyttet til butikkens lager. Denne journalen angir varene som må telles. Butikken kan da få tilgang til disse forhåndsdefinerte opptellingsjournalene og utføre dem ved hjelp av operasjonen **Lagerantall** i POS. Butikkbrukere starter en lageropptelling som ikke er planlagt, ettersom det kreves når de bruker operasjonen **Lagerantall** i POS. I motsetning til planlagte lagertellinger har ikke ikke-planlagte lagertellinger en forhåndsdefinert liste over varer. Når en lagertelling av en av disse typene fullføres i POS, lagres og sendes den til hovedkontoret. Ved hovedkontoret må opptellingen valideres og posteres i Commerce Headquarters som et eget trinn.

## <a name="inventory-lookup"></a>Beholdningsoppslag

Produktantallet som for øyeblikket finnes på lager for flere butikker og lagere, kan vises på siden **Beholdningsoppslag**. I tillegg til det gjeldende antallet på lager, kan fremtidige antall tilgjengelig for ordre (ATP) vises for hver butikk. Velg butikken du vil vise ATP-antall for, og velg deretter **Vis butikktilgjengelighet**. Hvis du vil ha informasjon om hvilke konfigurasjonsalternativer som er tilgjengelige, kan du se [Beregne lagertilgjengelighet for detaljhandelskanaler](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).
