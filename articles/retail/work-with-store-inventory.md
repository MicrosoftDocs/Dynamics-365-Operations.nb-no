---
title: Butikklagerstyring
description: Dette emnet beskriver hvilke typer dokumenter du kan bruke til å styre lager.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c5da94e02b2381bbd058221567172cd428931c45
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024689"
---
# <a name="store-inventory-management"></a>Butikklagerstyring

[!include [banner](includes/banner.md)]

Når du arbeider med lager i Dynamics 365 Retail og bruker salgsstedsprogrammet, er det viktig å merke seg at salgsstedet gir begrenset støtte for lagerdimensjoner og bestemt lagervaretyper.

Salgsstedsløsningen støtter ikke følgende varekonfigurasjoner:

- Stykklistevarer (unntatt pakkeprodukter, som bruker noen av komponentene i stykklisterammeverket)
- Faktisk vekt-varer
- Partikontrollerte varer

Salgsstedsprogrammet støtter for øyeblikket ikke følgende sporingsdimensjoner på salgsstedet:

- Partisporingsdimensjon
- Eierdimensjon

Salgsstedsløsningen gir begrenset støtte for følgende dimensjoner. Begrenset støtte angir at salgsstedet kan plassere noen av disse dimensjonene i lagertransaksjoner automatisk som standard basert på lager-/butikkoppsettkonfigurasjonen. Salgsstedet støtter ikke dimensjonene fullstendig på samme måte som hvis en salgstransaksjon angis manuelt i ERP. 

- **Lagerlokasjon** – Brukere vil ikke kunne administrere mottakslagerlokasjonen for varer som mottas i et butikklager, når butikken ikke har blitt konfigurert til å bruke lagerstyringsprosessen. En standard mottakslokasjon som er definert i butikklageret, vil bli brukt for disse varene. Hvis lagerstyringsprosessen er aktivert for butikken, utløses begrenset støtte som ber brukeren om å velge en mottakslokasjon for hele mottaket. Varer som selges fra butikken, blir alltid solgt fra standardlokasjonen for detaljhandel, slik det er definert i butikklageroppsettet. Lokasjonen for behandling av lager for retur kan styres via definisjonen av standard returlokasjon i butikklageret, eller basert på returårsakskoder som definert i returlokasjonspolicyen.
- **Nummerskilt** – Nummerskilt gjelder bare når **Bruk lagerstyringsprosesser** er aktivert på varen og i butikklageret. Hvis beholdningen mottas i et butikklager der lagerstyringsprosessen er aktivert i POS, og lokasjonen som er valgt for å motta varen, er knyttet til en lokasjonsprofil som krever nummerskiltkontroll, vil POS-programmet bruke et nummerskilt på mottakslinjen systematisk. Brukere i POS vil ikke kunne endre eller behandle disse nummerskiltdataene. Hvis full administrasjon av nummerskilt er nødvendig, anbefales det at butikken bruker WMS-mobilprogrammet eller Back Office ERP-klienten til å administrere mottak av disse varene.
- **Serienummer** – POS-programmet har begrenset støtte for et enkelt serienummer, som skal registreres på en transaksjonssalgslinje for ordrer som er opprettet i POS, med serialiserte varer. Dette serienummeret valideres ikke mot registrerte serienumre som allerede finnes på lageret. Hvis en salgsordre opprettes i telefonsenterkanalen eller oppfylles gjennom ERP, og flere serienumre registreres på en enkelt salgslinje under oppfyllingsprosessen i ERP, vil ikke disse serienumrene kunne brukes eller valideres hvis en retur behandles i POS for disse ordrene.
- **Lagerstatus** – For varer som bruker lagerstyringsprosessen og krever en lagerstatus, kan ikke dette statusfeltet angis eller endres gjennom POS-programmet. Standard lagerstatus som definert i butikklagerkonfigurasjonen, vil bli brukt når varer mottas på lageret.

> [!NOTE]
> Alle organisasjoner må teste varekonfigurasjoner gjennom POS i utviklings- eller testmiljøer før de distribueres til produksjon. Test varene ved å utføre vanlige hentesalgstransaksjoner og opprette kundeordrer (om nødvendig) via salgsstedet med varene dine. Testing må inneholde kjøring av fullstendige utdragsposteringsprosesser i testmiljøet og kontroll av at det ikke er noen problemer.
>
> Konfigurering av varer på en måte som ikke støttes av salgsstedsprogrammet, uten riktig testing, kan føre til at utdragsposteringsprosessen mislykkes i produksjonen uten en enkel måte å rette opp problemene. Partner- eller kundetilpassing til programmet kan eventuelt vurderes slik at disse posteringsprosessene kan fullføres. Hvis det ikke trengs tilpasninger, må organisasjonen sørge for at produktkonfigurasjonen av produktene er utført på en måte som støttes av standard salgsstedsprogram/ordreoppretting/utdragsposteringsprosess.

## <a name="purchase-orders"></a>Bestillinger

Bestillinger opprettes ved hovedkontoret. Hvis et lager for detaljhandel er inkludert i bestillingshodet, kan ordren mottas i butikken ved hjelp av Modern POS (MPOS) eller Cloud POS via operasjonen **Plukk-/mottak**. Når antallene som mottas i butikken, angis i **Motta nå**-feltet i POS for bestillingsdokumentet, kan de lagres lokalt eller disponeres. Hvis du lagrer disse dataene lokalt, har det ingen innvirkning på beholdningen på lager. Lagring bør bare utføres hvis brukeren ikke er klar til å postere mottaket i HK, og bare trenger en måte å midlertidig lagre de tidligere angitte **Motta nå**-dataene på. Dette lagrer motta nå-dataene lokalt i brukerens kanaldatabase. Når dokumentet er behandlet med alternativet **Igangsett**, sendes **Motta nå**-dataene til HK, og bestillingsmottaket posteres. 

## <a name="transfer-orders"></a>Overføringsordrer

En overføringsordre kan angi at en bestemt butikk er lokasjonen som varer kan sendes fra, eller lokasjonen som beholdningen mottas på. Hvis POS-brukeren er leveringslageret for en overføringsordre, kan de angi **Send nå**-antall fra salgsstedet. Dataene som angis av forsendelsesbutikken, kan lagres lokalt eller disponeres. Når det lagres lokalt, gjøres det ingen oppdateringer i overføringsordredokumentet i HK. Lagring bør bare utføres hvis brukeren ikke er klar til å postere forsendelsen i HK, og trenger en måte å midlertidig lagre de tidligere angitte **Send nå**-dataene på. Når butikken er klar til å bekrefte forsendelsen, bør **Igangsett**-alternativet velges. Dermed posteres forsendelsen for overføringsordren i HK, slik at det mottakende lageret nå kan motta mot det. 

Hvis POS-brukeren er det mottakende lageret for en overføringsordre, kan de angi **Motta nå**-antall fra salgsstedet. Dataene som angis av mottaksbutikken, kan lagres lokalt eller disponeres. Lagring bør bare utføres hvis brukeren ikke er klar til å postere mottaket i HK, og trenger en måte å midlertidig lagre de tidligere angitte **Motta nå**-dataene på. Dette lagrer motta nå-dataene lokalt i brukerens kanaldatabase. Når dokumentet er behandlet med alternativet **Igangsett**, sendes **Motta nå**-dataene til HK, og overføringsordremottaket posteres. Det er viktig å huske at mottakslageret blir begrenset, slik at det bare er mulig å motta antall som er lik eller mindre enn sendte antall. Et forsøk på å motta antall i en overføringsordre som ikke er sendt tidligere, fører til feil, og mottaket vil ikke bli bekreftet i HK.

## <a name="stock-counts"></a>Lagerantall

Lagertellinger kan være planlagt eller ikke planlagt. Planlagte lagertellinger startes ved hovedkontoret, som angir hvilke varer som skal telles. Hovedkontoret oppretter et opptellingsdokument som kan mottas i butikken, der faktisk beholdningsantall registreres i Moderne salgssted eller Skysalgssted. Ikke planlagte lagertellinger startes i en butikk, og faktisk beholdningsantall oppdateres i Moderne salgssted eller Skysalgssted. I motsetning til planlagte lagertellinger har ikke ikke-planlagte lagertellinger en forhåndsdefinert liste over varer. Når en lagertelling av en av disse typene er fullført, lagres og sendes den til hovedkontoret. Ved hovedkontoret valideres og posteres antallet som et separat trinn.

## <a name="inventory-lookup"></a>Beholdningsoppslag

Det gjeldende produktantallet på lager for flere butikker og lagre kan vises på **Beholdningsoppslag**-siden. I tillegg til gjeldende antall på lager kan fremtidige antall tilgjengelig for ordre (ATP) vises for hver enkelt butikk. Dette gjør du ved å velge butikken du vil vise ATP-Antallet for, og deretter klikker du **Vis butikktilgjengelighet**.
