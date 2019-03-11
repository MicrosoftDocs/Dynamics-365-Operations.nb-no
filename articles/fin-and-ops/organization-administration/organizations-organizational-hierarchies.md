---
title: Organisasjoner og organisasjonshierarkier
description: En organisasjon er en gruppe personer som jobber sammen for å utføre en forretningsprosess eller oppnå et mål. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72834769e393382ac511ad3af21544efddb049d3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "322243"
---
# <a name="organizations-and-organizational-hierarchies"></a>Organisasjoner og organisasjonshierarkier

[!include [banner](../includes/banner.md)]

En organisasjon er en gruppe personer som jobber sammen for å utføre en forretningsprosess eller oppnå et mål. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.

## <a name="organizations"></a>Organisasjoner

I Microsoft Dynamics 365 for Finance and Operations kan du definere følgende typer interne organisasjoner: juridiske enheter, driftsenheter og team.

Alle interne organisasjoner er typer av **Part**-enheten. Disse organisasjonene bruker derfor adresseboken til å lagre adresse- og kontaktinformasjon. En part, som kan være enten en person eller organisasjon, kan tilhøre én eller flere adressebøker.

### <a name="legal-entities"></a>Juridiske enheter

En juridisk enhet er en organisasjon som har en registrert eller lovfestet juridisk struktur. Juridiske enheter kan inngå juridiske kontrakter og er påkrevd for å klargjøre oppgjør som rapporterer om prestasjonen.

Et firma er en type juridisk enhet. I denne versjonen av Microsoft Dynamics 365 for Finance and Operations er firmaer det eneste typen juridisk enhet som du kan opprette, og hver juridisk enhet er tilknyttet en firma-IDen. Denne tilknytningen finnes fordi noen funksjonsområder i programmet bruker en firma-ID eller dataområde-ID, i sine datamodeller. I disse funksjonsområdene brukes firmaer som en grense for datasikkerhet. Brukere har bare tilgang til data for firmaet de er logget på.

### <a name="operating-units"></a>Driftsenheter

En driftsenhet er en organisasjon som brukes til å fordele kontrollen over økonomiske ressurser og driftsprosesser i en virksomhet. Personer i en driftsenhet har plikt til å gjøre mest mulig ut av knappe ressurser, forbedre prosesser og gjøre rede for egen ytelse.

I Microsoft Dynamics 365 for Finance and Operations omfatter driftsenhetstypene kostsentre, forretningsenheter, verdistrømmer, avdelinger og detaljhandelskanaler. Følgende tabell inneholder mer informasjon om hver type driftsenhet.

| Driftsenhetstype | Beskrivelse | Formål |
|---------------------|-------------|---------|
| Kostsenter         | En driftsenhet der ledere er ansvarlige for budsjetterte og faktiske utgifter. | Brukes for behandling og driftskontroll for forretningsprosesser som strekker seg over juridiske enheter. |
| Forretningsenhet       | En delvis uavhengig driftsenhet som er opprettet for å nå strategiske forretningsmål. | Brukes for finansrapportering som er basert på bransjer eller produktlinjer som organisasjonen leverer, uavhengig av juridiske enheter. |
| Verdistrøm        | En driftsenhet som styrer én eller flere produksjonsflyter. | Brukes vanligvis i lean manufacturing til å styre aktivitetene og flytene som kreves for å forsyne forbrukere med et produkt eller en tjeneste. |
| Avdeling          | En driftsenhet som representerer en kategori eller en funksjonell del i en organisasjon som utfører en bestemt oppgave, for eksempel salg eller regnskap. | Brukes for å rapportere om funksjonsområder. En avdeling kan ha resultatansvar, og kan bestå av en gruppe kostsentre. |
| Detaljhandelkanal      | En driftsenhet som representerer en fysisk butikk, nettbutikk eller markedsplass på Internett. | Brukes for behandling og driftskontroll av én eller flere butikker i eller på tvers av juridiske enheter. |

### <a name="teams"></a>Team

Et team er en organisasjon der medlemmene deler et felles ansvar, en felles interesse eller et felles mål. Team kan ikke brukes i organisasjonshierarkier.

## <a name="organizational-hierarchies"></a>Organisasjonshierarkier

Definer organisasjonshierarkier for å vise og rapportere for bedriften fra ulike perspektiver. Du kan for eksempel definere et hierarki av juridiske enheter for avgiftsrapportering, juridisk eller lovpålagt rapportering. Definer et hierarki som er basert på driftsenheter, for å rapportere finansinformasjon som ikke er lovpålagt, men som brukes til internkontroll. Du kan for eksempel opprette et innkjøpshierarki for å styre innkjøpspolicyer, -regler og -forretningsprosesser.

Hvert hierarki er tilordnet et formål i Microsoft Dynamics 365 for Finance and Operations. Formålet med et hierarki bestemmer hvilke organisasjonstyper som kan inkluderes i hierarkiet. Formålet bestemmer også bruksscenariene for hierarkiet.

Organisasjoner i et hierarki kan dele parametere, policyer og transaksjoner. En organisasjon kan arve eller overstyre parameterne for den overordnede organisasjonen. Delte hoveddata, for eksempel produkter og adressebøker, gjelder imidlertid for hele organisasjonen og kan ikke overstyres for individuelle organisasjoner. Oppretting av organisasjoner og hierarkier krever nøye planlegging. Hvis du vil ha mer informasjon, kan du se [Planlegge organisasjonshierarkiet](plan-organizational-hierarchy.md).
