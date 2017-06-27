---
title: Opprette en avdeling, og knytte den til avdelingshierarkiet
description: "En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon. En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale. Du kan bruke avdelinger til å rapportere om funksjonsområder. Avdelinger kan ha ansvar for fortjeneste og tap."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 576418ce1c8b2019a55905558273106badadaa40
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a>Opprette en avdeling, og knytte den til avdelingshierarkiet

[!include[banner](includes/banner.md)]


En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon. En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale. Du kan bruke avdelinger til å rapportere om funksjonsområder. Avdelinger kan ha ansvar for fortjeneste og tap.

En avdeling kan inneholde en gruppe med kostsentre. Stillinger kan tilordnes til avdelinger. Hvis du vil opprette en avdeling, klikker du **Personale** &gt; **Avdelinger** &gt; **Avdeling**. Følgende tabell beskriver feltene som er tilgjengelige.

| Felt               | Beskrivelse                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Navn                | Skriv inn et navn for avdelingen.                                                                                                                                                                                  |
| Avdelingsnummer   | Det kan hende at en standardverdi genereres automatisk hvis en nummerseriekode er tilordnet til **Organisasjonsnummer**-referansen på siden **Nummerserier**.                                                 |
| Søkenavn         | Angi et navn eller akronym som kan brukes til å søke etter avdelingen.                                                                                                                                            |
| Notat                | Angi eventuell tilleggsinformasjon her.                                                                                                                                                                            |
| I hierarki        | En merket boks indikerer at avdelingen er inkludert i avdelingshierarkiet. Hvis du vil ha informasjon om hvordan du legger til en avdeling i avdeling-hierarkiet, kan du se informasjonen senere i denne artikkelen. |
| DUNS-nummer         | DUNS står for Data Universal Number System. Dette er et nisifret nummer som utstedes av Dun & Bradstreet.                                                                                                     |
| Leder             | Angi personen som administrerer avdelingen.                                                                                                                                                                    |
| Adresser           | Legg til adresseinformasjonen for avdelingen. Legg for eksempel til postadressen til bygningen som avdelingen er i.                                                                          |
| Kontaktinformasjon | Legg til kontaktinformasjonen for avdelingen. Legg for eksempel til et telefonnummer for brukerstøtten i avdelingen.                                                                                           |

Bruk følgende fremgangsmåte for å legge til en avdeling i avdelingshierarkiet.

1.  Klikk **Personale** &gt; **Avdelinger** &gt; **Avdelingshierarki**.
2.  Klikk **Rediger**, og velg deretter organisasjonen som avdelingen skal være under.
3.  Klikk **Sett inn**, og velg **Avdeling** i listen.
4.  Velg avdelingen som skal legges til hierarkiet, i listen over avdelinger som vises.
5.  Lagre endringene. Du får en melding om at det har blitt opprettet en kladdeversjon av hierarkiet.
6.  Når du er klar, klikker du **Publiser** i hierarkidesigneren. Du kan angi en gyldig dato som angir når hierarkiet skal publiseres. Hvis du vil legge til en ny avdeling i begynnelsen av neste kalenderår, kan du for eksempel angi gyldighetsdatoen til 1. januar i det nye kalenderåret. Hierarkiendringene vil tre i kraft på denne datoen.





