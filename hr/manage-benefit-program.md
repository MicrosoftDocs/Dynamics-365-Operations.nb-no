---
title: Definere og administrere et fordelsprogram
description: "Personale inneholder et sett med verktøy som kan brukes til å definere og vedlikeholde fordeler, fradrag og arbeideres kompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere. Denne artikkelen inneholder informasjon om hvordan du definerer og behandler fordeler."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 09ad9ad22c676c3b117cc39e692c64ef92637dc1
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Definere og administrere et fordelsprogram
<a id="define-and-manage-a-benefits-program" class="xliff"></a>

[!include[banner](includes/banner.md)]


Personale inneholder et sett med verktøy som kan brukes til å definere og vedlikeholde fordeler, fradrag og arbeideres kompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere. Dette emnert inneholder informasjon om hvordan du definerer og behandler fordeler.

Fordelsoppsett
<a id="benefit-setup" class="xliff"></a>
-------------

Før arbeidere kan registreres i fordeler, må du opprette elementene i hver enkelt fordel. Disse elementene kombinerer lignende fordelsplaner og definer standardinnstillinger, for eksempel fradragssatser og regnskapsdetaljer. Mange av disse innstillingene kan justeres når arbeidere senere registreres i fordelsprogrammet. En organisasjon kan tilby flere registreringsalternativer for hver fordelsplanen, eller en arbeider kan avstå fra registrering i planen. 

[![Prosessflyt for fordel](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## Fordelselementer
<a id="benefit-elements" class="xliff"></a>
Før du begynner å opprette fordeler og registrer arbeidere i dem, må du definere elementene som utgjør en fordel: type, plan og alternativer.

-   **Type** – En samling av planer for en bestemt fordel, for eksempel en medisinsk fordel eller en parkeringsfordel.
-   **Plan** – En bestemt fordel som leveres på kontrakt av en leverandør.
-   **Alternativ** – Dekningsgraden, for eksempel bare den ansatte eller den ansatte og ektefelle/partner.

For hver type fordeler, for eksempel syn eller tannlege, kan en organisasjon tilby én eller flere planer til arbeidere. Organisasjonen kan tilby forskjellige alternativer for hver plan. Arbeidere kan for eksempel kjøpe tilleggsdekning for livsforsikring på én, to eller tre ganger sin årlige lønnen. Hver kombinasjon av en plan og alternativene blir en fordel som arbeidere kan registrere seg for. 

[![bilde av fordel](./media/benefit-pic.png)](./media/benefit-pic.png)

## Rettighet
<a id="eligibility" class="xliff"></a>
Mange faktorer avgjør arbeideres kvalifikasjon for ulike typer fordeler som en arbeidsgiver tilbyr. Når du oppretter en fordel i Microsoft Talent, kan du angi type rettighet som gjelder for denne fordelen. 

Du kan gjøre en fordel tilgjengelig for alle arbeidere. Enkelte selskaper tilbyr for eksempel parkeringskort til alle ansatte som en fordelsskatt. Når du oppretter denne fordelen, setter du kvalifikasjonen til **Alle arbeidere er kvalifiserte**. 

For andre fordeler, for eksempel utlegg og avgiftslettelser, gjelder ikke berettiget. Når du oppretter disse typer av fordeler, setter du berettigelsen til **Omgå berettigelsesprosess**. 

Fordelsrettigheter kan til slutt være regelbasert. Et selskap kan for eksempel tilby to typer livsforsikringsfordel til ansatte. Ansatte i ledelsen er kvalifisert for én livsforsikringsplan, mens alle andre heltidsansatte er kvalifisert for den andre livsforsikringsplanen. I Talent kan du opprette en fordelsrettighetsregel for å søke etter alle ansatte i ledelsen, og en annen regel til å finne alle andre heltidsansatte og deretter bruke disse reglene til den aktuelle fordelen.

## Registrering
<a id="enrollment" class="xliff"></a>
Når du har opprettet fordelene som organisasjonen tilbyr, og fastslått rettigheten, kan du registrere arbeiderne i fordeler. Du kan registrere én enkelt arbeider i fordeler eller du kan registrere mange arbeidere i én eller flere fordeler i én enkelt prosess. 

Noen ganger stopper en organisasjon å tilby bestemte fordeler. I dette tilfellet må du oppdatere fordelen og arbeidere som er registrert. Utløpsdato for massefordeler lar deg samtidig endre utløpsdatoen både for en fordel og registreringene av arbeidere for denne fordelen. Du kan også velge flere arbeidere som er registrert i en fordel, og endre sluttdatoen for dekningen deres. 

På samme måte kan du med masseutvidelse av fordel utvide utløpsdatoen for både en fordel og arbeiderregistreringene for denne fordelen hvis du vil tilby en fordel lenger enn opprinnelig planlagt.

Se også
<a id="see-also" class="xliff"></a>
--------

[Policyer for fordelsrettigheter](benefit-eligibility-policies.md)




