---
title: Serviceavtaler
description: "Serviceavtaler lar deg definere ressursene som brukes ved et vanlig servicebesøk, og hvordan disse ressursene skal faktureres til kunden."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: aaff0c1d71fcf2656d5d6e76a2bf4b7b3a699281
ms.contentlocale: nb-no
ms.lasthandoff: 02/19/2018

---

# <a name="service-agreements"></a>Serviceavtaler

[!include[banner](../includes/banner.md)]


Serviceavtaler lar deg definere ressursene som brukes ved et vanlig servicebesøk, og hvordan disse ressursene skal faktureres til kunden.

Hver serviceavtale knyttes til et prosjekt, som transaksjoner posteres og faktureres gjennom. Du kan imidlertid også fakturere serviceordretransaksjoner direkte gjennom prosjektet uten først å måtte knytte serviceordren til en serviceavtale. Dette kan være en praktisk løsning hvis serviceordren gjelder et enkelt besøk og behovet for en rask behandling av transaksjonen veier tyngre enn behovet for å opprettholde detaljerte serviceavtaleopplysninger for kunden over en lengre periode.

## <a name="service-agreement"></a>Serviceavtale

I hver serviceavtale må du angi et prosjekt, en serviceavtale-ID og en serviceavtalegruppe. Serviceavtalegruppen kan brukes til å sortere og organisere serviceavtaler.

Et serviceavtalehode inneholder innstillinger som gjelder alle tilknyttede avtalelinjer:

-  Om serviceavtalen er deaktivert. Hvis en serviceavtale deaktiveres, vil du ikke kunne generere serviceordrer fra serviceavtalen.
-  Varigheten på serviceavtalen.
-  Hvordan serviceordrelinjer kombineres med serviceordrer.
-  Om serviceavtalen er en mal.

I serviceavtalehodet definerer du også alle serviceobjektene og serviceoppgavene som kan brukes med serviceavtalen ved å angi de bestemte serviceoppgavene eller serviceobjektene som skal knyttes til de ulike linjene i avtalen.

Fra serviceavtalehodet kan du kopiere serviceavtalelinjer og servicemallinjer til den gjeldende serviceavtalen.

Du kan suspendere serviceavtaler og stoppe enkle serviceavtalelinjer.

Hvis du merker av for **Avbrutt** på en serviceavtale, kan du ikke gjøre følgende:

-    Opprett serviceordrer automatisk eller manuelt fra serviceavtalen.

Hvis du merker av for **Stoppet** på en serviceavtalelinje, kan du ikke gjøre følgende:

-    Opprett serviceordrer automatisk eller manuelt fra serviceavtalelinjen.
-    Kopier serviceavtalelinjen til en annen serviceavtale eller serviceordre.


> [!NOTE]
> Hvis en serviceavtale suspenderes, stoppes alle de tilknyttede linjene uansett enkeltstatus.

## <a name="service-agreement-lines"></a>Serviceavtalelinjer

Hver serviceavtalelinje beskriver innholdet i det foreslåtte vedlikeholdsarbeidet i detalj. Linjene inneholder følgende informasjon:

-  Transaksjonstypen og en beskrivelse av transaksjonstypen.
-  Den ansatte som utfører vedlikeholdsarbeidet.
-  Objektene vedlikeholdet skal utføres på i henhold til serviceavtalen.
-  Hvor ofte det forskjellige arbeidet skal utføres og tilknyttede vare-, utgifts- og gebyrtransaksjoner skal registreres.
-  Tidsvinduet når serviceordrelinjene kan grupperes til en serviceordre.
-  Serviceoppgavene som brukes til å gruppere sett med avtalelinjer til arbeidsoppgaver og til å summere hvilke serviceoppgaver som vil bli utført, for teknikere og kunder.
-  Om en linje er stoppet. Hvis en linje stoppes, kan du ikke opprette serviceordrer for den bestemte linjen.
-  Prosjektinnstillinger som kategori og linjeegenskap.

## <a name="related-topics"></a>Relaterte emner

[Opprette serviceavtaler](create-service-agreements.md)

