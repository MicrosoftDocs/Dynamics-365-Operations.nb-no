---
title: Krav til produksjonsoppsett
description: "Denne artikkelen inneholder informasjon om krav til oppsett før du kan arbeide med produksjonskontroll."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 47fe11168ad2ddea2a7033eda8d8bd8220efea32
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="production-setup-requirements"></a>Krav til produksjonsoppsett

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om krav til oppsett før du kan arbeide med produksjonskontroll. 

Produksjonskontroll er integrert med funksjonene i andre moduler. Denne egenskapen gjør det mulig å endre produksjonsordrer samtidig som de oppdateres automatisk i alle andre tilknyttede prosesser og beregninger i systemet. Følgende oppsettprosesser er ført opp i rekkefølgen de bør fullføres i.

## <a name="required-baseline-setup-in-other-modules"></a>Påkrevd basislinjekonfigurasjon i andre moduler
Før du kan arbeide med Produksjonskontroll må du konfigurere informasjon i andre moduler. Dette oppsettet omfatter følgende oppgaver:

-   Konfigurer generell firmainformasjon.
-   Konfigurer økonomi.
-   Definer varegrupper.
-   Konfigurer finanskontoer for varegrupper.
-   Konfigurer lagervaretabellen i Lagerstyring.
-   Opprett stykklister og stykklisteversjoner i Lagerstyring.

## <a name="required-calendar-and-resource-setup"></a>Påkrevd konfigurasjon av kalender og ressurs
Før du tar i bruk Produksjonskontroll må du åpne Organisasjonsstyring og opprette og definere kalender- og operasjonsressurser i følgende rekkefølge:

1.  **Driftstidsmaler** – Konfigurer driftstidsmaler for å definere hvilke tider som er tilgjengelige for produksjonsplanlegging.
2.  **Kalendere** – Konfigurer driftstidskalendere for å definere hvilke dager i året som er tilgjengelige for produksjonsplanlegging.
3.  **Ressursgrupper** – Konfigurer ressursgrupper for å gruppere operasjonsressurser slik at du kan få en oversikt over all ledig kapasitet når du kjører planlegging. Du trenger ikke definere ressursgrupper før du setter opp operasjonsressurser. Vi anbefaler at du forstår hvordan du vil gruppere ressurser når du konfigurerer Produksjonskontroll.
4.  **Ressurser** – Konfigurer operasjonsressurser for å definere ressursene som brukes for å fullføre produksjonsprosessen og planlegge kapasiteten.

## <a name="required-production-parameters-setup"></a>Påkrevd konfigurasjon av produksjonsparametere
**Parametere for produksjonskontroll** – Konfigurer grunnleggende produksjonsparametere for å definere hvordan systemet håndterer og behandler produksjonsordrer. Definer hvordan produksjonsordrer skal opprettes, estimeres, planlegges og forbrukes. Du kan også velge hvilken type tilbakemeldinger du vil ha, og hvordan kostnadsregnskapet skal utføres.

## <a name="required-journal-name-identification"></a>Påkrevd identifikasjon av journalnavn
**Produksjonsjournalnavn** – Angi produksjonsjournalnavn som brukes til å registrere og postere transaksjoner.

## <a name="setup-if-you-use-operations"></a>Hvis du bruker operasjoner
Operasjoner viser til de bestemte aktivitetene som fullføres for å produsere det ferdige produktet. **Merk:** Du må vite hvilke typer aktiviteter som kreves for å produsere varen, og rekkefølgen og prioritetene for aktivitetene. Du må også vite hvilke ressurser som er involvert, og hvor mange.

1.  **Operasjoner** – Konfigurer operasjoner som skal representere oppgavene som må fullføres for å produsere det ferdige produktet.
2.  **Relasjoner** – Konfigurer operasjonsrelasjoner for å fastsette detaljerte egenskaper. For å definere operasjonsrelasjoner klikk **Relasjoner** på siden **Operasjoner**.

## <a name="setup-if-you-use-routes"></a>Hvis du bruker ruter
Hvis du arbeider med ruter, må du definere operasjoner for hver produksjonsrute du definerer. Ruten representerer banen varen tar fra operasjon til operasjon, fra begynnelsen til slutten av produksjonsprosessen.

1.  **Kostnadskategorier** – Konfigurer kostnadskategorier for å definere kostnadene per time for bestemte prosesser og oppstillingstider.
2.  **Kostgrupper** – Konfigurer kostgrupper for å opprette og vedlikeholde forskjellige typer etterkalkulering.
3.  **Rutegrupper** – Konfigurer rutegrupper for å definere parametere som er relatert til grupper av ruter. Du må konfigurere rutegruppene før du oppretter produksjonsruter.
4.  **Ruter** – Konfigurer produksjonsruter, og definer standardinnstillinger for å styre planlegging, etterkalkulering og prissetting av ruteoperasjoner samt rapport om fremdrift.
5.  **Ruter** – Konfigurer ruteversjoner for å aktivere varevariasjoner i produksjonen.

## <a name="optional-advanced-settings"></a>Valgfrie, avanserte innstillinger
1.  **Produksjonsgrupper** – Konfigurer produksjonsgrupper for å fastsette forhold mellom produksjonsordren og finanskontoene. Finanskontoene brukes til å postere eller gruppere ordrene for rapportering.
2.  **Produksjonspuljer** – Opprett produksjonspuljer for å gruppere produksjonsordrer slik at du kan behandle produksjonsordrer det haster med, eller for å slette og postere grupper av ordrer.
3.  **Egenskaper** – Definer egenskaper for å opprette spesielle attributter som du kan tilordne til ressursene for å kontrollere rekkefølgen på produksjoner. Disse attributtene er knyttet til driftstidsmalen.





