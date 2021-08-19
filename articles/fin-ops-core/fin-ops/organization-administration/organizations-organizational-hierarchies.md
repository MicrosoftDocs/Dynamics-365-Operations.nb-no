---
title: Oversikt over organisasjoner og organisasjonshierarkier
description: Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.
author: sericks007
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.custom:
- "17291"
- intro-internal
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74aa2736b4cfb11039ea1cee3f62e74cf4928a1b27cea16e7e0e86f66bdddd59
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715995"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Oversikt over organisasjoner og organisasjonshierarkier

[!include [banner](../includes/banner.md)]

En organisasjon er en gruppe personer som jobber sammen for å utføre en forretningsprosess eller oppnå et mål. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.

## <a name="organizations"></a>Organisasjoner

Du kan definere følgende typer interne organisasjoner: juridiske enheter, driftsenheter og team.

Alle interne organisasjoner er typer av **Part**-enheten. Disse organisasjonene bruker derfor adresseboken til å lagre adresse- og kontaktinformasjon. En part, som kan være enten en person eller organisasjon, kan tilhøre én eller flere adressebøker.

### <a name="legal-entities"></a>Juridiske enheter

En juridisk enhet er en organisasjon som har en registrert eller lovfestet juridisk struktur. Juridiske enheter kan inngå juridiske kontrakter og er påkrevd for å klargjøre oppgjør som rapporterer om prestasjonen.

Et firma er en type juridisk enhet. Firmaer er for øyeblikket den eneste typen juridisk enhet som du kan opprette, og hver juridisk enhet er tilknyttet en firma-IDen. Denne tilknytningen finnes fordi noen funksjonsområder i programmet bruker en firma-ID eller dataområde-ID, i sine datamodeller. I disse funksjonsområdene brukes firmaer som en grense for datasikkerhet. Brukere har bare tilgang til data for firmaet de er logget på.

### <a name="operating-units"></a>Driftsenheter

En driftsenhet er en organisasjon som brukes til å fordele kontrollen over økonomiske ressurser og driftsprosesser i en virksomhet. Personer i en driftsenhet har plikt til å gjøre mest mulig ut av knappe ressurser, forbedre prosesser og gjøre rede for egen ytelse.

Driftsenhetstypene omfatter kostsentre, forretningsenheter, verdistrømmer, avdelinger og handelskanaler. Følgende tabell inneholder mer informasjon om hver type driftsenhet.

| Driftsenhetstype | Beskrivelse | Formål |
|---------------------|-------------|---------|
| Kostsenter         | En driftsenhet der ledere er ansvarlige for budsjetterte og faktiske utgifter. | Brukes for behandling og driftskontroll for forretningsprosesser som strekker seg over juridiske enheter. |
| Forretningsenhet       | En delvis uavhengig driftsenhet som er opprettet for å nå strategiske forretningsmål. | Brukes for finansrapportering som er basert på bransjer eller produktlinjer som organisasjonen leverer, uavhengig av juridiske enheter. |
| Verdistrøm        | En driftsenhet som styrer én eller flere produksjonsflyter. | Brukes vanligvis i lean manufacturing til å styre aktivitetene og flytene som kreves for å forsyne forbrukere med et produkt eller en tjeneste. |
| Avdeling          | En driftsenhet som representerer en kategori eller en funksjonell del i en organisasjon som utfører en bestemt oppgave, for eksempel salg eller regnskap. | Brukes for å rapportere om funksjonsområder. En avdeling kan ha resultatansvar, og kan bestå av en gruppe kostsentre. |
| Handelskanal      | En driftsenhet som representerer en fysisk butikk, nettbutikk eller markedsplass på Internett. | Brukes for behandling og driftskontroll av én eller flere butikker i eller på tvers av juridiske enheter. |

### <a name="teams"></a>Team

Et team er en organisasjon der medlemmene deler et felles ansvar, en felles interesse eller et felles mål. Team kan ikke brukes i organisasjonshierarkier.

## <a name="organizational-hierarchies"></a>Organisasjonshierarkier

Definer organisasjonshierarkier for å vise og rapportere for bedriften fra ulike perspektiver. Du kan for eksempel definere et hierarki av juridiske enheter for avgiftsrapportering, juridisk eller lovpålagt rapportering. Definer et hierarki som er basert på driftsenheter, for å rapportere finansinformasjon som ikke er lovpålagt, men som brukes til internkontroll. Du kan for eksempel opprette et innkjøpshierarki for å styre innkjøpspolicyer, -regler og -forretningsprosesser.

Hvert hierarki er tilordnet et formål. Formålet med et hierarki bestemmer hvilke organisasjonstyper som kan inkluderes i hierarkiet. Formålet bestemmer også bruksscenariene for hierarkiet.

Organisasjoner i et hierarki kan dele parametere, policyer og transaksjoner. En organisasjon kan arve eller overstyre parameterne for den overordnede organisasjonen. Delte hoveddata, for eksempel produkter og adressebøker, gjelder imidlertid for hele organisasjonen og kan ikke overstyres for individuelle organisasjoner. Oppretting av organisasjoner og hierarkier krever nøye planlegging. Hvis du vil ha mer informasjon, kan du se [Planlegge organisasjonshierarkiet](plan-organizational-hierarchy.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]