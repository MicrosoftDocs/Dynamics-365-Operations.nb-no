---
title: Opprette serviceavtaler
description: "Dette emnet beskriver hvordan du bruker funksjoner i modulene Servicestyring og Prosjektstyring og regnskap for å opprette serviceavtaler."
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
ms.sourcegitcommit: 2a46173a3566a56a21add9d42c111d456b1ae7c1
ms.openlocfilehash: 517bc1b9de9b2512f42e4f32b4a19e517e349e8e
ms.contentlocale: nb-no
ms.lasthandoff: 02/19/2018

---

# <a name="create-service-agreements"></a>Opprette serviceavtaler

[!include[banner](../includes/banner.md)]

Dette emnet beskriver hvordan du bruker funksjoner i modulene Servicestyring og Prosjektstyring og regnskap for å opprette serviceavtaler.

## <a name="create-a-service-agreement-from-service-management"></a>Opprette en serviceavtale fra Servicestyring

1. Gå til **Servicestyring**.
2. Klikk **Serviceavtaler** for å opprette en ny serviceavtalelinje i sidehodet. 
3. Klikk **Ny**. Angi en beskrivelse, velg en referanse til et prosjekt i **Prosjekt-ID**-feltet og fyll ut resten av feltene og linjene for serviceavtalen. Klikk **Lagre**.
4. Klikk **Relasjoner**-kategorien og velg **Serviceobjekter** eller **Serviceoppgaver** for å opprette serviceobjektrelasjoner eller serviceoppgaverelasjoner for serviceavtalen. Serviceobjektene og oppgavene du har opprettet relasjoner til kan knyttes til linjene på serviceavtalen.
5. I den nedre halvdelen av siden oppretter du serviceavtalelinjer ved å kopiere linjer fra en servicemal eller en annen serviceavtale eller ved å opprette serviceavtalelinjer manuelt.

> [!NOTE]
> Hvis du kopierer linjer til serviceavtalen fra en annen serviceavtale, kan du angi om du også ønsker å kopiere serviceobjekter og serviceoppgaverelasjoner. Hvis du kopierer disse relasjonene, legges de til eksisterende relasjoner på serviceavtalen. Hvis du kopierer serviceavtalelinjer fra en servicemal, kopieres serviceobjektet og serviceoppgaverelasjoner automatisk som serviceobjektrelasjoner og serviceoppgaverelasjoner på de nye serviceavtalelinjene.

## <a name="create-service-agreement-lines-manually"></a>Opprette serviceavtalelinjer manuelt

1. Fra **Serviceavtaler**-siden, legg til en serviceavtalelinje i linjerutenettet. 
2. Angi den relevante informasjonen for serviceavtalelinjen. 
3. Trykk **CTRL+S** for å lagre linjen, og lukk deretter siden.

## <a name="create-a-service-agreement-from-project"></a>Opprette en serviceavtale fra Prosjekt

1. Klikk **Prosjektstyring og regnskap**.
2. Klikk **Alle prosjekter**.
3. Velg prosjektet fra listen.
4. Klikk **Administrer** i **handlingsruten**. I **Ny**-handlingsgruppen klikker du **Service** og velger **Serviceavtale**.
5. Følg trinnene i delen **Opprett en serviceavtale** som beskrevet tidligere i dette emnet for å angi prosjektreferansen.


## <a name="related-topics"></a>Relaterte emner

[Serviceavtaler](service-agreements.md)



