---
title: Formalisere forretningsprosesser
description: Dette emnet beskriver hvordan du kan bruke forretningsprosessfunksjonen til å opprette en mal for forretningsprosessen for prosesser som må fullføres i organisasjonen.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 0f4d2b8e5f78c5815c5ad7e5eae0d13ad7d15c12
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898695"
---
# <a name="formalize-business-processes"></a>Formalisere forretningsprosesser

Forretningsprosessfunksjonen lar deg opprette en mal for forretningsprosessen for forretningsprosesser som må fullføres i organisasjonen. Firmaet firmaet utfører for eksempel en personalevurdering hvert år. I så fall kan du opprette en mal som sporer alle aktivitetene som revisjonsprosessen består av. Denne malen kan deretter bidra til å sikre at alle oppgavene utføres hver gang det utføres en revisjon. Hvis aktivitetene må fullføres i en bestemt rekkefølge, hjelpe malen i tillegg å garantere at de gjøres i riktig rekkefølge.

Maler kan brukes til regelmessige prosesser. De kan også kopieres og brukes som utgangspunkt for å opprette nye maler.

Når du oppretter en mal for forretningsprosess, kan en forretningsprosess startes og spores i arbeidsområdet **Forretningsprosess**. Når du starter en forretningsprosess, blir oppgavene tilordnet til de rette personene og vil inkludere en forfallsdato.

## <a name="business-process-templates"></a>Maler for forretningsprosess
En forretningsprosessmal viser en gruppe oppgaver som utgjør en forretningsprosess. Personalledere og -assistenter kan opprette forretningsprosesser som standard. Du kan imidlertid endre rollene som kan opprette forretningsprosesser ved å endre plikten **Vedlikehold generelle forretningsprosesser** i sikkerhetskonfigurasjonen.

For hver forretningsprosess kan du definere en prosesseier. Prosesseieren har oversikt over alle oppgavene for prosessen, og vedkommende kan tildele oppgaver på nytt eller endre forfallsdatoer for fakturaer. Personallederen oppretter for eksempel en mal for forretningsprosess for gjennomgang av fordeler og kompensasjons- og fordelsansvarlig som prosesseier. Kompensasjons- og fordelsansvarlig har deretter oversikt over oppgavene som må fullføres som en del av gjennomgangen.

Prosesseier kan ikke opprette nye forretningsprosesser eller maler for forretningprosess eller slette aktive forretningsprosesser eller maler for forretningprosess.

## <a name="tasks"></a>Oppgaver
En forretningsprosess består ofte av flere oppgaver. Noen oppgaver, for eksempel gjennomgang av interne kurstilbud, kan fullføres i Microsoft Dynamics 365 Talent. I dette tilfellet er et alternativ valgt i feltet **Oppgavekobling**. Andre oppgaver kan omfatte gjennomgang eller utfylling av sider på et nettsted. I så fall er **URL-adressen** valgt i feltet **Oppgavekobling**, og deretter kan webadressen angis. Du kan angi URL-adresser for både eksterne og interne nettsteder. Du kan også opprette oppgaver for oppgaver som du har fullført manuelt, for eksempel gjennomgang av tilgjengeligheten av alle strukturer. I dette tilfellet kreves det ikke en oppgavekobling. Med denne fleksibiliteten kan du spore flere typer oppgaver i en omfattende prosess.

Oppgaver kan tilordnes til en bestemt arbeider eller til en stilling. Kompensasjons- og fordelsansvarlig vil for eksempel alltid være personen som utfører en evaluering av forsikringspremier. Når du oppretter denne oppgaven, velger du derfor **Stilling** i feltet **Tilordningstype**, og deretter velger du **Kompensasjons- og fordelsansvarlig** i listen **Stilling**. Når forretningsprosessen stawwrtes, tilordnes oppgaven til arbeideren som har stillingen **Kompensasjons- og fordelsansvarlig**. Hvis du vil tilordne en oppgave til en spesifikk arbeider, velger du **Arbeider** i feltet **Tilordningstype**, og deretter velger du den aktuelle personen.

Forfallsdatoer for oppgaver avhenger av måldatoen som er angitt i begynnelsen av forretningsprosessen. Noen oppgaver må fullføres innen måldatoen, og andre oppgaver kan fullføres etter måldatoen. Når du definerer en oppgave, angir du en forfallsdato som står i forhold til måldatoen i feltet **Forfallsdato samsvarer ikke med måldato**. La oss si at Kompensasjons- og fordelsansvarlig for eksempel må utføre en evaluering av forsikringsbonuser 10 dager før personalkontrollen er fullført. I så fall vil aktiviteten som er opprettet for gjennomgangen ha verdien **10** for **Forfallsdato samsvarer ikke med måldato**. Hvis forretningsprosessen starter 13 mai., forfaller oppgaven 3. mai.

> [!NOTE]
> Forfallsdato kan også endres etter at forretningsprosessen er startet.

Kompliserte oppgaver kan kreve flere trinn, eller personen som utfører oppgavene må formidle tilleggsinformasjon. Disse scenariene kan du legge til instruksjoner i en oppgave. Instruksjonene kan gir ytterligere informasjon om hvordan oppgaven fullføres til personen som er tilordnet til å fullføre den. Du kan også inkludere rik tekstformatering i instruksjonene.

## <a name="starting-a-business-process"></a>Starte en forretningsprosess
I en mal for forretningsprosess kan du starte en forretningsprosess ved å velge **Start prosess**. Når en prosess er startet, opprettes det oppgaver for de valgte arbeiderne eller stillingene som er definert i oppgavene som er inkludert i malen. En forfallsdato blir også tilordnet til hver oppgave ved å legge til eller trekke fra antallet forskyvningsdager fra måldatoen, som beskrevet i dele "Oppgaver". Du kan vise aktive forretningsprosesser i arbeidsområdet **Forretningsprosesser**.

## <a name="employee-self-service"></a>Ansattselvbetjening
Når en oppgave er tilordnet til en ansatt, kan den ansatt vise den, og alle hans eller hennes andre tilordnede oppgaver på siden **Ansattselvbetjening**. For hver forretningsprosessoppgave som er tilordnet ham eller henne, kan den ansatt se navnet og beskrivelsen av oppgaven, instruksjoner for å fullføre den og navnet på kontaktpersonen. Fra siden **Ansattselvbetjening** kan den ansatte også åpne den tilhørende siden i Microsoft Dynamics 365 eller den tilknyttede websiden, og kan merke oppgavene som pågår, er avbrutt eller fullført.

## <a name="business-process-workspace"></a>Arbeidsområdet Forretningsprosess
Personaleksperter kan vise de aktive forretningsprosessene fra arbeidsområdet **Forretningsprosess**. Dette arbeidsområdet viser alle aktive prosesser og oppgavene som er knyttet til hver av dem. Den omfattende oppgavelisten kan filtreres etter forfallsdato. Arbeidsområdet viser også forfalte oppgaver og oppgaver som er spesifikt tilordnet til personaleksperter. Personaleksperten kan også oppdatere statusen til alle oppgaver, og om nødvendig kan oppgaver tilordnes på nytt slik at den generelle forretningsprosessen har fremdrift.

## <a name="my-business-processes-workspace"></a>Arbeidsområdet Mine forretningsprosesser
Prosesseiere kan vise de aktive forretningsprosessene som er tilordnet til dem fra arbeidsområdet **Min forretningsprosess**. Dette arbeidsområdet viser alle aktive prosesser som brukeren eier, og tilknyttede oppgaver. Den omfattende oppgavelisten kan filtreres etter forfallsdato. Arbeidsområdet viser også oppgaver som er spesifikt tilordnet til prosesseier. Prosesseieren kan også oppdatere statusen for alle oppgaver og tilordne oppgaver på nytt.

## <a name="navigating-business-processes"></a>Navigere i forretningsprosesser
Hvis du vil opprette eller kopiere en mal for forretningsprosessen eller starte en forretningsprosess, går du til Forretningsprosesser - koblinger – Administrasjon for forretningsprosesser. Du kan deretter utføre følgende handlinger:

- Velge **Ny** for å opprette en ny mal for forretningsprosess.
- Velge **Kopier fra mal** for å kopiere den valgte malen til en ny mal.
- Velge **Start prosess** for å starte den valgte forretningsprosessen, tilordne oppgaver og beregne forfallsdatoer.

Hvis du vil vise aktive prosesser og tilknyttede oppgaver, åpner du arbeidsområdet **Forretningsprosesser**.

