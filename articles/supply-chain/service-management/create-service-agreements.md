---
title: Opprette serviceavtaler
description: Dette emnet beskriver hvordan du bruker funksjoner i modulene Servicestyring og Prosjektstyring og regnskap for å opprette serviceavtaler.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c937f43896d239a5cc8b48ed06854add8c9a618
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202796"
---
# <a name="create-service-agreements"></a>Opprette serviceavtaler

[!include [banner](../includes/banner.md)]

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

[Oversikt over å utvikle og etablere serviceavtaler](service-agreements.md)


