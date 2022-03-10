---
title: Beholdningsstatuser
description: Denne artikkelen beskriver hvordan du kan bruke lagerstatusene til å kategorisere og holde orden på lager.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db15ad94355823c699e83c9e3f47660f813e1c9a
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103469"
---
# <a name="inventory-statuses"></a>Beholdningsstatuser

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kan bruke lagerstatusene til å kategorisere og holde orden på lager.

## <a name="set-up-and-use-inventory-statuses"></a>Definere og bruke lagerstatuser

Du kan bruke lagerstatuser til å kategorisere beholdning. Du kan deretter utføre aktuelle handlinger, for eksempel etterfylling eller plasseringsarbeid.

Her er noen eksempler på hvordan du kan bruke lagerstatuser:

- Opprett lagerstatuser for lagerbeholdning, innkommende transaksjoner og utgående transaksjoner.
- Angi en standard lagerstatus for lagertransaksjoner.
- Endre en beholdningsstatus for varer før ankomst, under ankomst, eller når varene plasseres under lagerbevegelse.
- Bruk en lagerstatus til å prissette varer som returneres, og til å planlegge varedekning under hovedplanlegging.

En beholdningsstatus er én av dimensjonene i lagringsdimensjonsgruppen. Lagerstatuser kan kategoriseres som tilgjengelige eller utilgjengelige, og du kan bruke parameteren **Lagerblokkering** til å blokkere varer som har en tilgjengelig lagerstatus. Varer som har en blokkert status, regnes som aktuell beholdning og kan ikke brukes i produksjonsordrer, salgsordrer, overføringsordrer eller utgående transaksjoner.

Du kan bruke lagervarer som har enten tilgjengelig eller utilgjengelig lagerstatus for innkommende arbeid. La oss si at du for eksempel oppretter en tilgjengelig status kalt *Klar*, en utilgjengelig status kalt *Skadet*, og en blokkert status kalt *Sperret*. Hvis du oppretter en bestilling for mottatte eller returnerte varer og eventuelle varer er skadet eller ødelagt, kan du endre lagerstatusen for disse varene til *Skadet* på bestillingslinjen. Etter at disse varene er mottatt, settes statusen automatisk til *Sperret*. Hvis du skanner de skadede varene med en mobil enhet, kan Supply Chain Management bruke lokasjonsdirektiver og arbeidsmaler til å vise informasjon om en passende lokasjon eller et lokasjonsområde der du kan plassere disse varene. Når det gjelder returnerte varer, opprettes avgangstypen *Reservering* på **Lagertransaksjoner**-siden.

Du kan angi hvilke beholdningsstatuser som er blokkeringsstatuser ved hjelp av avmerkingsboksen **Lagerblokkering** på **Beholdningsstatuser**-siden. Du kan ikke bruke lagerstatuser som blokkeringsstatuser for salgsordrer, overføringsordrer og prosjektintegreringer.

For utgående arbeid kan du bruke ulike ikke-blokkeringslagerstatuser til å kontrollere hvilket lager det skal reserveres mot. Hvis du har varer med statusen *Blokkering* og hovedplanlegging kjøres på disse varene, regnes de som manglende, og beholdningen etterfylles automatisk. For kvalitetsordrer knyttet til utgående arbeid vil det dessuten ikke være mulig å oppdatere **Beholdningsstatus** som en del av kvalitetsordrevalideringen.

> [!NOTE]
> Du kan ikke endre statusen til lager på lokasjoner der det finnes åpent arbeid. Hvis du for eksempel mottok et innkjøp for en vare, men ikke gjorde det plasserte trinnet, ville det være åpent arbeid for mottakslokasjonen, og du vil få en feilmelding hvis du har forsøkt å endre lagerstatusen på denne lokasjonen. Hvis du fullfører eller avbryter det relaterte arbeidet, kan du endre statusen.
>
> Vanligvis endres statusen til lagerbeholdningen som er relatert til åpent lagerarbeid, bare av arbeidere ved hjelp av den mobile lagerstyringsappen, for eksempel under utføring av en bevegelsesprosess.

Når du har definert beholdningsstatuser, kan du angi standard beholdningsstatus for et område, en vare og et lager. Du kan også angi en standardstatus for salg, overføring og bestillinger. Standardstatus for salgsordrer og utgående overføringsordre kan ikke ha alternativet **Lagerblokkering** satt til *Ja*. Lagerstatusen som arves fra standardinnstillingene for område, lager, vare, bestilling, overføringsordre eller salgsordre, kan endres ved hjelp av den mobile enheten, eller på bestillings-, salgsordre- eller overføringsordrelinjen.

Hvis du planlegger dekning for varer som har en tilgjengelig lagerstatus, velger du alternativet **Dekningsplanlegg etter dimensjon** for en lagringsdimensjon på siden **Lagringsdimensjonsgrupper**. Når du åpner veiviseren **Varedekning**, vises varer som har en tilgjengelig status, på **Status**-siden. Hvis du vil opprette dekningsinnstillinger for disse varene, velger du IDen for lagerstatus for de tilgjengelige lagerstatusene. Basert på dekningsinnstillingene kan du beregne varebehovene og forhåndsberegne forsyning og behov for tilgjengelige varer under hovedplanlegging. Du kan ikke opprette et oppsett av varedekning som har en blokkert lagerstatus. Bruk i stedet **Varedekning**-siden til å opprette eller endre varedekningsparameterne.

## <a name="change-inventory-statuses"></a>Endre lagerstatuser

Du kan endre lagerstatusene enten ved hjelp av siden **Beholdning etter lokasjon**, eller ved å bruke den periodiske oppgaven *Beholdningsstatusendring*.

- Når du bruker den *periodiske oppgaven Beholdningsstatusendring*, kan du velge hvilke poster som skal tas med, og angi oppgaven som skal kjøres i partiet på ønsket intervall.
- Hvis du vil endre lagerstatusen som en ad hoc-prosess, går du til siden **Beholdning etter lokasjon**, velger de relevante postene og velger deretter knappen **Beholdningsstatusendring**.

> [!NOTE]
> Ved hjelp av funksjonen *Endre lagerstatus for varer som kontrolleres av sporingsdimensjoner*, kan du endre lagerstatusen for varer som styres av sporingsdimensjoner, inkludert muligheten til å oppdatere bare valgte poster. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Endre beholdningsstatusen for varer som kontrolleres av sporingsdimensjoner* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Hvis funksjonen er aktivert, kan du gjøre følgende:
>
> - På siden **Beholdning etter lokasjon** kan du gruppere linjer basert på viste dimensjoner, ved hjelp av **Vis dimensjoner**-knappen, og endre statusen for de valgte linjene.
> - På siden **Beholdning etter lokasjon** kan du velge flere poster og deretter bruke **knappen Beholdningsstatusendring** til å endre alle samtidig.
> - I den periodiske oppgaven **Beholdningsstatusendring** kan du filtrere etter sporingsdimensjoner.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
