---
title: Dekningsinnstillinger
description: Denne artikkelen inneholder informasjon om dekningsinnstillingene som hovedplanlegging bruker til å beregne varebehov.
author: t-benebo
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1218c447a18f79f9a44bfa413a0414d6926d7499
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871956"
---
# <a name="coverage-settings"></a>Dekningsinnstillinger

[!include [banner](../includes/banner.md)]

Hovedplanlegging bruker dekningsinnstillinger til å beregne varebehov.

Du kan angi dekningsinnstillinger på flere måter:

- Angi dekningsinnstillinger for en dekningsgruppe.

    Du kan opprette en dekningsgruppe som inneholder innstillinger for alle produkter som er koblet til dekningsgruppen. Hvis du vil opprette en dekningsgruppe, går du til **Hovedplanlegging &gt; Oppsett &gt; Dekning &gt; Dekningsgrupper**. Du kan koble en dekningsgruppe til et produkt. Hvis koblingen er spesifikk for et område, lager eller produktdimensjon, kan du bruke **Dekningsgruppe**-feltet på **Varedekning**-siden. Hvis koblingen er generisk, uavhengig av produktdimensjonene, bruker du **Dekningsgruppe**-feltet i **Plan**-hurtigfanen på **Produktdetaljer**-siden. Hvis du ikke kobler en dekningsgruppe til et produkt, bruker hovedplanlegging som standard den generelle dekningsgruppen som er angitt på siden **Hovedplanleggingsparametere**.

- Angi dekningsinnstillinger for et produkt.

    Du kan opprette dekningsinnstillinger for et bestemt produkt. Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. Velg produktet. I handlingsruten, i fanen **Plan** i **Dekning**-gruppen, velger du **Varedekning** for å åpne **Varedekning**-siden. Hvis produktet allerede er koblet til en dekningsgruppe, kan du overstyre innstillingene for dekningsgruppen ved å bruke **Overstyr**-feltet. Dekningsinnstillingene på **Varedekning**-siden har prioritet over innstillingene på **Dekningsgruppe**-siden.

- Angi dekningsinnstillinger for et produkt ved hjelp av en veiviser.

    Veiviseren fører deg gjennom prosessen med å definere de primære varedekningsparameterne. På **Varedekning**-siden i handlingsruten velger du **Veiviser** for å åpne **Varedekningsveiviseren**.

- Angi dekningsinnstillinger for en dimensjonsgruppe.

    Gå til **Behandling av produktinformasjon &gt; Produkter &gt; Frigitte produkter**. På **Detaljer om frigitt produkt**-siden, i hurtigfanen **Generelt** i **Administrasjon**-delen, velger du koblingen i feltet **Lagringsdimensjonsgruppe**. På **Lagringsdimensjonsgrupper**-siden merker du av for **Dekningsplanlegg etter dimensjon** for å opprette dekningsinnstillinger for en dimensjon i lagringsdimensjonsgruppen. Feltet **Dekningsplanlegg etter dimensjon** må være valgt for alle produktdimensjoner, for eksempel konfigurasjon, farge, størrelse og stil.


## <a name="coverage-codes"></a>Dekningskoder

Hovedplanlegging kan konfigureres til å bruke forskjellige metoder for etterfylling. Metodene for etterfylling eller justering av partistørrelse er teknikkene som brukes av systemet for å fastslå den satsvise størrelsen for kjøpte eller produserte varer. 

Hver etterfyllingsmetode tilordnes én av følgende dekningskoder:

- **Manuell** – Metoden for justering av partistørrelse der systemet ikke foreslår kjøps-, overførings- eller produksjonsordrer for varen. Planleggeren for varen vil være ansvarlig for å opprette de nødvendige ordrene for etterfylling av varen.
- **Per behov** – Metoden for justering av partistørrelse der systemet oppretter et bestillingsforslag, en overføring eller en produksjonsordre per behov for varen. Dette brukes vanligvis for kostbare varer med periodisk etterspørsel.  
- **Per periode** – Metoden for justering av partistørrelse som kombinerer alt behov for en periode i én ordre for varen. Ordren vil bli planlagt for den første dagen i perioden, og antallet vil oppfylle nettobehovet i den etablerte perioden. Perioden begynner med det første behovet for varen og dekker den definerte lengden i tid. Neste periode starter med de neste behovene til varen.
- **Min/maks** – Metoden for justering av partistørrelse som inneholder etterfyllingen av lager opptil et bestemt nivå når beholdningsprognosen er under en terskel. Etterfyllingsantallet vil være differansen mellom maksimumsnivået og det forhåndsberegnede nivået.


## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over hovedplaner](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]