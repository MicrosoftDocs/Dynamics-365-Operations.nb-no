---
title: Opprette en avdeling, og knytte den til avdelingshierarkiet
description: "En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon. En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale. Du kan bruke avdelinger til å rapportere om funksjonsområder. Avdelinger kan ha ansvar for fortjeneste og tap."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee51abe108b3bc0aabc764b991222db6d185e532
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a>Opprette en avdeling, og knytte den til avdelingshierarkiet

En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon. En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale. Du kan bruke avdelinger til å rapportere om funksjonsområder. Avdelinger kan ha ansvar for fortjeneste og tap.

En avdeling kan inneholde en gruppe med kostsentre. Stillinger kan tilordnes til avdelinger. Klikk for å opprette en avdeling, **Personale**&gt;**avdelinger**&gt;**avdeling**. Tabellen nedenfor beskriver feltene som er tilgjengelige.

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

1.  Klikk **Personale**&gt;**avdelinger**&gt;**avdelingshierarki**.
2.  Klikk **Rediger**, og velg deretter organisasjonen som avdelingen skal være under.
3.  Klikk **Sett inn**, og velg **Avdeling** i listen.
4.  Velg avdelingen som skal legges til hierarkiet, i listen over avdelinger som vises.
5.  Lagre endringene. Du får en melding som at det er opprettet en kladdeversjon av hierarkiet.
6.  Når du er klar, klikker du **Publiser** i hierarkidesigner. Du kan angi en gyldig dato som angir når hierarkiet skal publiseres. Hvis du vil legge til en ny avdeling i begynnelsen av neste kalenderår, kan du for eksempel angi gyldighetsdatoen til 1. januar i det nye kalenderåret. Hierarkiendringene vil tre i kraft på denne datoen.



