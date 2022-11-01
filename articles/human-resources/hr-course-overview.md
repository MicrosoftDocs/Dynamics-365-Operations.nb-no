---
title: Kursoversikt
description: Denne artikkelen forklarer hvordan HR-administratorer og -ledere kan bruke kursfunksjonene til å vedlikeholde opplysningene om kurs som er tilgjengelige for ansatte.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716340"
---
# <a name="courses-overview"></a>Kursoversikt

Microsoft Dynamics 365 Human Resources tilbyr en løsning for organisasjonens opplæringsbehov. Denne løsningen tilbyr to opplæringskursbaner: *virtuelt* og *instruktørgenerert*.

*Virtuell opplæring* er en opplæringsopplevelse som utvides gjennom elektroniske ressurser. I *kurs med veileder* tilrettelegger en instruktør en opplæringsøkt for en gruppe ansatte eller medarbeidere.

I opplæringsmodulen kan HR-profesjonelle, administratorer, opplæringsledere og ledere opprette og tilordne begge opplæringskursbaner til ansatte.

> [!NOTE]
> For å bruke virtuelle kurs må du aktivere funksjonen **Kursforbedringer** i Funksjonsbehandling.

## <a name="set-up-virtual-courses"></a>Definere virtuelle kurs

For å konfigurere virtuelle kurs må du aktivere funksjonen **Kursforbedringer** i Funksjonsbehandling. Gå til **Nye kurs \> Nytt**, og sett alternativet **Virtuelt** til **Ja**. Når funksjonen er aktivert, kreves det en kurskobling. Feltet **Kursstatus** settes til **Åpen**. Alternativet **Tillat at den ansatte selv registrerer seg** settes til **Ja**, men kan settes til **Nei**.

Når funksjonen for **Kursforbedringer** er aktivert i Funksjonsstyring, skjer følgende endringer:

- Det må defineres en forfallsdato for kurstilordning.
- En kurskobling er nødvendig.
- **Ansattselvbetjening** viser en ansattoversikt i **Kurs**. Brukeren kan vise kurs som snart har forfalt, som forfaller snart, og som er tilordnet.
- Arbeidere kan fullføre virtuelle kurs og attestere seg selv.

## <a name="set-up-instructor-led-courses"></a>Definer instruktørledede kurs

Instruktørledede kurs trenger ikke konfigureres før de brukes.

Følgende informasjon er valgfri og kan angis for kurs. Hvis denne informasjonen legges inn for kurs, må den defineres før kurspostene opprettes:

- Kurstype
- Kurslokalegrupper
- Kursgrupper
- Kurslokasjoner
- Kurslokaler
- Instruktører
- Kurstyper

Du kan bruke *kurstyper* til å kategorisere kurs i henhold til strukturen eller innholdet. Du kan opprette kurstyper på siden **Kurstyper** .

Det største og minste antallet deltakere som kan meldes på et kurs, er definert på hurtigfanen **Generelt** på siden **Kurs** .

### <a name="course-setup-type"></a>Oppsettype for kurs 

*Oppsettyper* bestemmer strukturen for kurset. Det finnes tre oppsettyper for kurs.

| Type oppsett | Beskrivelse |
|------|--------|
| Standard | Kurs av denne oppsetttypen har ikke en daglig agenda. Det er standard oppsettypen når du oppretter et nytt kurs. |
| Agenda | Velg denne oppsettypen for å planlegge detaljene for hver dag i et kurs som foregår over flere dager. |
| Agenda + økt | <p>Velg denne oppsettypen for mer komplekse kurs. Du kan for eksempel dele agendaen for kurset i *spor* og *økter*:</p><ul><li>*Spor* er bestemte emneområder for et kurs.</li><li>*Økter* deler opp spor og hjelper med å identifisere bestemte prosesser eller teknikker som er relevante for et spor.</li></ul> |

### <a name="course-tasks"></a>Kursoppgaver

For hvert kurs kan du for eksempel utføre følgende oppgaver:

- Registrere deltakere.
- Spesifisere en registreringsfrist.
- Definere minste og største antall deltakere.
- Tilordne en kurslokasjon og et klasserom.
- Anbefale hoteller for kursdeltakere.
- Opprette en kursbeskrivelse som kan posteres i **Ansattselvbetjening**.

> [!NOTE]
> Du kan slette et kurs bare hvis ingen er registrert for kurset.

### <a name="course-statuses"></a>Kursstatuser

Tabellen nedenfor viser en liste over kursstatuser og handlingene som er fullført for hver av dem.

| Status | Handlinger |
|------|--------|
| Opprettet | <ul><li>Skriv inn og endre kursinformasjon.</li><li>Endre kursstatusen til  **Åpen** slik at arbeidere kan melde seg på kurset.</li></ul> | 
| Åpne | <ul><li>Registrer deltakere på kurset.</li><li>Fjern deltakere fra kurset.</li><li>Bekreft deltakere for kurset.</li><li>Endre kursstatus til **Lukket** eller **Avbrutt** for deltakere med statusen **Bekreftet**.</li></ul>|
| Lukket | Du kan åpne kurset på nytt. |
| Kansellert | Du kan åpne kurset på nytt. |

### <a name="course-participants"></a>Kursdeltakere

*Kursdeltakere* er arbeidere som deltar på et opplæringskurs eller et arrangement. Du kan bare registrere deltakere for åpne kurs.

### <a name="workflow"></a>Arbeidsflyt

Ansatte som registrerer seg for et kurs via siden **Ansattselvbetjening** , kan rute registreringen gjennom arbeidsflyt for godkjenning. Du kan tilordne en arbeidsflyt til et kurs i hurtigfanen **Generelt** på **Kurs** -siden.
