---
title: Opprette avdelinger og inkludere dem i avdelingshierarkiet
description: En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon. En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: cdc0440c02d0e66eaa89bfd875d8c8edf8d99c96
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688608"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Opprette avdelinger og inkludere dem i avdelingshierarkiet


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon. En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale. Du kan bruke avdelinger til å rapportere om funksjonsområder. Avdelinger kan ha ansvar for fortjeneste og tap.

En avdeling kan inneholde en gruppe med kostsentre. Stillinger kan tilordnes til avdelinger. Hvis du vil opprette en avdeling, klikker du **Personale** &gt; **Avdelinger** &gt; **Avdeling**. Følgende tabell beskriver feltene som er tilgjengelige.

| Felt               | Beskrivelse                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Navn**                | Skriv inn et navn for avdelingen.                                                                                                                                                                                  |
| **Avdelingsnummer**   | Det kan hende at en standardverdi genereres automatisk hvis en nummerseriekode er tilordnet til **Organisasjonsnummer**-referansen på siden **Nummerserier**.                                                 |
| **Søkenavn**         | Angi et navn eller akronym som kan brukes til å søke etter avdelingen.                                                                                                                                            |
| **Notat**                | Angi eventuell tilleggsinformasjon her.                                                                                                                                                                            |
| **I hierarki**        | En merket boks indikerer at avdelingen er inkludert i avdelingshierarkiet. Hvis du vil ha informasjon om hvordan du legger til en avdeling i avdeling-hierarkiet, kan du se informasjonen senere i denne artikkelen. |
| **DUNS-nummer**         | DUNS står for Data Universal Number System. Dette er et nisifret nummer som utstedes av Dun & Bradstreet.                                                                                                     |
| **Leder**             | Angi personen som administrerer avdelingen.                                                                                                                                                                    |
| **Adresser**           | Legg til adresseinformasjonen for avdelingen. Legg for eksempel til postadressen til bygningen som avdelingen er i.                                                                          |
| **Kontaktinformasjon** | Legg til kontaktinformasjonen for avdelingen. Legg for eksempel til et telefonnummer for brukerstøtten i avdelingen.                                                                                           |

Bruk følgende fremgangsmåte for å legge til en avdeling i avdelingshierarkiet.

1.  Klikk **Personale** &gt; **Avdelinger** &gt; **Avdelingshierarki**.
2.  Klikk **Rediger**, og velg deretter organisasjonen som avdelingen skal være under.
3.  Klikk **Sett inn**, og velg **Avdeling** i listen.
4.  Velg avdelingen som skal legges til hierarkiet, i listen over avdelinger som vises.
5.  Lagre endringene. Du får en melding om at det har blitt opprettet en kladdeversjon av hierarkiet.
6.  Når du er klar, klikker du **Publiser** i hierarkidesigneren. Du kan angi en gyldig dato som angir når hierarkiet skal publiseres. Hvis du vil legge til en ny avdeling i begynnelsen av neste kalenderår, kan du for eksempel angi gyldighetsdatoen til 1. januar i det nye kalenderåret. Hierarkiendringene vil tre i kraft på denne datoen.

## <a name="steps-for-creating-a-department"></a>Fremgangsmåter for å opprette en avdeling
Se artikkelen [Definere nye avdelinger](./hr-personnel-define-departments.md) for trinnvis fremgangsmåte for å opprette en ny avdeling. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
