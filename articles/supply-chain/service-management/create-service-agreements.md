---
title: Opprette serviceavtaler
description: Denne artikkelen beskriver hvordan du bruker funksjoner i modulene Servicestyring og Prosjektstyring og regnskap for å opprette serviceavtaler.
author: sorenva
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d18d279cd437e98cad6495def953978cb78e723e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901770"
---
# <a name="create-service-agreements"></a>Opprette serviceavtaler

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker funksjoner i modulene Servicestyring og Prosjektstyring og regnskap for å opprette serviceavtaler.

## <a name="create-a-service-agreement-from-service-management"></a>Opprette en serviceavtale fra Servicestyring

1. Gå til **Servicestyring**.
2. Velg **Serviceavtaler** for å opprette en ny serviceavtalelinje i sidehodet. 
3. Velg **Ny**. Angi en beskrivelse, velg en referanse til et prosjekt i **Prosjekt-ID**-feltet og fyll ut resten av feltene og linjene for serviceavtalen. Velg **Lagre**.
4. Klikk på **Relasjoner**-fanen og velg **Serviceobjekter** eller **Serviceoppgaver** for å opprette serviceobjektrelasjoner eller serviceoppgaverelasjoner for serviceavtalen. Serviceobjektene og oppgavene du har opprettet relasjoner til kan knyttes til linjene på serviceavtalen.
5. I den nedre halvdelen av siden oppretter du serviceavtalelinjer ved å kopiere linjer fra en servicemal eller en annen serviceavtale eller ved å opprette serviceavtalelinjer manuelt.

> [!NOTE]
> Hvis du kopierer linjer til serviceavtalen fra en annen serviceavtale, kan du angi om du også ønsker å kopiere serviceobjekter og serviceoppgaverelasjoner. Hvis du kopierer disse relasjonene, legges de til eksisterende relasjoner på serviceavtalen. Hvis du kopierer serviceavtalelinjer fra en servicemal, kopieres serviceobjektet og serviceoppgaverelasjoner automatisk som serviceobjektrelasjoner og serviceoppgaverelasjoner på de nye serviceavtalelinjene.

## <a name="create-service-agreement-lines-manually"></a>Opprette serviceavtalelinjer manuelt

1. Fra **Serviceavtaler**-siden, legg til en serviceavtalelinje i linjerutenettet. 
2. Angi den relevante informasjonen for serviceavtalelinjen. 
3. Velg **Lagre** for å lagre linjen, og lukk deretter siden.

## <a name="create-a-service-agreement-from-project"></a>Opprette en serviceavtale fra Prosjekt

1. Velg **Prosjektstyring og regnskap**.
2. Velg **Alle prosjekter**.
3. Velg prosjektet fra listen.
4. Velg **Administrer** i **handlingsruten**. I gruppen **Ny handling** velger du **Service** og deretter **Serviceavtale**.
5. Følg trinnene i delen **Opprett en serviceavtale** som beskrevet tidligere i denne artikkelen for å angi prosjektreferansen.


## <a name="related-articles"></a>Relaterte artikler

[Oversikt over å utvikle og etablere serviceavtaler](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]