---
title: Definere og administrere et fordelsprogram
description: "Personale inneholder et sett med verktøy som kan brukes til å definere og vedlikeholde fordeler, fradrag og arbeideres kompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere. Denne artikkelen inneholder informasjon om hvordan du definerer og behandler fordeler."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Definere og administrere et fordelsprogram

[!include[banner](includes/banner.md)]


Personale inneholder et sett med verktøy som kan brukes til å definere og vedlikeholde fordeler, fradrag og arbeideres kompensasjonsplaner som en organisasjon tilbyr eller behandler for sine arbeidere. Dette emnert inneholder informasjon om hvordan du definerer og behandler fordeler.

<a name="benefit-setup"></a>Fordelsoppsett
-------------

Før arbeidere kan registreres i fordeler, må du opprette elementene i hver enkelt fordel. Disse elementene kombinerer lignende fordelsplaner og definer standardinnstillinger, for eksempel fradragssatser og regnskapsdetaljer. Mange av disse innstillingene kan justeres når arbeidere senere registreres i fordelsprogrammet. En organisasjon kan tilby flere registreringsalternativer for hver fordelsplanen, eller en arbeider kan avstå fra registrering i planen. 

[![Prosessflyt for fordel](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Fordelselementer
Før du begynner å opprette fordeler og registrer arbeidere i dem, må du definere elementene som utgjør en fordel: type, plan og alternativer.

-   **Type** – En samling av planer for en bestemt fordel, for eksempel en medisinsk fordel eller en parkeringsfordel.
-   **Plan** – En bestemt fordel som leveres på kontrakt av en leverandør.
-   **Alternativ** – Dekningsgraden, for eksempel bare den ansatte eller den ansatte og ektefelle/partner.

For hver type fordeler, for eksempel syn eller tannlege, kan en organisasjon tilby én eller flere planer til arbeidere. Organisasjonen kan tilby forskjellige alternativer for hver plan. Arbeidere kan for eksempel kjøpe tilleggsdekning for livsforsikring på én, to eller tre ganger sin årlige lønnen. Hver kombinasjon av en plan og alternativene blir en fordel som arbeidere kan registrere seg for. 

[![bilde av fordel](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Rettighet
Mange faktorer avgjør arbeideres kvalifikasjon for ulike typer fordeler som en arbeidsgiver tilbyr. Når du oppretter en fordel i Microsoft Dynamics 365 for Operations, kan du angi type rettighet som gjelder for denne fordelen. 

Du kan gjøre en fordel tilgjengelig for alle arbeidere. Enkelte selskaper tilbyr for eksempel parkeringskort til alle ansatte som en fordelsskatt. Når du oppretter denne fordelen, setter du kvalifikasjonen til **Alle arbeidere er kvalifiserte**. 

For andre fordeler, for eksempel utlegg og avgiftslettelser, gjelder ikke berettiget. Når du oppretter disse typer av fordeler, setter du berettigelsen til **Omgå berettigelsesprosess**. 

Fordelsrettigheter kan til slutt være regelbasert. Et selskap kan for eksempel tilby to typer livsforsikringsfordel til ansatte. Ansatte i ledelsen er kvalifisert for én livsforsikringsplan, mens alle andre heltidsansatte er kvalifisert for den andre livsforsikringsplanen. I Dynamics 365 for Operations kan du opprette en fordelsrettighetsregel for å søke etter alle ansatte i ledelsen, og en annen regel til å finne alle andre heltidsansatte og deretter bruke disse reglene til den aktuelle fordelen.

## <a name="enrollment"></a>Registrering
Når du har opprettet fordelene som organisasjonen tilbyr, og fastslått rettigheten, kan du registrere arbeiderne i fordeler. Du kan registrere én enkelt arbeider i fordeler eller du kan registrere mange arbeidere i én eller flere fordeler i én enkelt prosess. 

Noen ganger stopper en organisasjon å tilby bestemte fordeler. I dette tilfellet må du oppdatere fordelen og arbeidere som er registrert. Utløpsdato for massefordeler lar deg samtidig endre utløpsdatoen både for en fordel og registreringene av arbeidere for denne fordelen. Du kan også velge flere arbeidere som er registrert i en fordel, og endre sluttdatoen for dekningen deres. 

På samme måte kan du med masseutvidelse av fordel utvide utløpsdatoen for både en fordel og arbeiderregistreringene for denne fordelen hvis du vil tilby en fordel lenger enn opprinnelig planlagt.

<a name="see-also"></a>Se også
--------

[Policyer for fordelsrettigheter](benefit-eligibility-policies.md)




