---
title: Administrere rekrutteringsprosesser
description: Denne artikkelen beskriver et konsept som rekrutteringspersoner kan bruke til å spore trinnene i en rekrutteringsprosess.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: anbichse
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74ff8b081f5c82a089eef47b5cc18bc498a34c21
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752084"
---
# <a name="manage-recruiting-processes"></a>Administrere rekrutteringsprosesser

[!include [banner](../includes/banner.md)]

Dette emnet beskriver et konsept som rekrutteringspersoner kan bruke til å spore trinnene i en Rekruttering prosess, inkludert aktiviteter for å annonsere ledige stillinger og rekruttere søkere, spore søker- og søknadsinformasjon, intervjue søkere og velge én eller flere kandidater for å besette de ledige stillingene i organisasjonen.

## <a name="overview"></a>Oversikt

Rekrutteringsprosjekter kan hjelpe deg med å organisere trinnene skal du fullføre når du fyller ledige stillinger i en juridisk enhet. En søker er en person som søker på ansettelse for bedriften. En søknad er en søkers uttrykk for interesse for å bli ansatt hos et firma, og kan være knyttet til et rekrutteringsprosjekt til uttrykkt interesse for en bestemt åpning. En enkelt søker kan ha flere søknader i samme juridiske enhet eller på tvers av flere firmaer i organisasjonen.

## <a name="recruitment-projects"></a>Rekrutteringsprosjekter

Med rekrutteringsprosjekter kan bemanningskonsulenter følge opp fremdriften mot å fylle én eller flere åpne stillinger. Rekrutteringsprosjektet identifiserer avdelingen og jobben der én eller flere stillinger er åpne. Rekrutteringsprosjekter sporer også følgende informasjon om ledige stillinger:

- Det spesifikke antallet ledige stillinger
- Ansettelsesansvarlig og en alternativ kontakt for stillingen
- Datoen da rekvisisjonen ble godkjent
- Søknadsfristen
- Den beregnede startdatoen

Rekrutteringsprosjektet inneholder **stillingsannonsen** som brukes i **Ansattselvbetjening** for å annonsere den ledige stillingen. For å vise den ledige stillingen til ansatte må rekrutteringsprosjektet må ha en **stillingsannonse**, feltet **Vis på ansattselvbetjening** må settes til Ja, **Søknadsfristen** må være satt til en fremtidig dato, og rekrutteringsprosjektet må ha **prosjektstatusen** Startet. Tabellen nedenfor viser de mulige rekrutteringsprosjektstatusene og tilhørende beskrivelser.

| Status    | Viser at ...                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Planlagt | Rekrutteringsinnsats klargjøres. Rekruttering er ennå ikke startet for dette prosjektet. |
| Startet   | Søknader godtas nå for ledige stillinger i dette prosjektet.                   |
| Avsluttet  | Alle ledige stillinger for dette prosjektet er besatt.                                         |
| Avbrutt  | Rekruttering er avbrutt for dette prosjektet.                                          |

Rekrutteringspersoner kan også registrere **mediene** som brukes til å annonsere den ledige stillingen via eksterne enheter, samt spore **utviklinger** mot prosjektet eller søknadene.

## <a name="applicants"></a>Søkere

En søker er en person som søker på en jobb i bedriften. Søkere deles mellom alle juridiske enheter i organisasjonen og gir deg et stort utvalg av medarbeidere til å søke fra. Du kan opprettholde kompetanse, referanser, overnattingsforespørsler og personlige opplysninger for søkere. Når du oppretter en søkerpost, opprettes en personpost for den søkeren i den globale adresseboken. Du kan bruke siden **Søker** siden for å oppdatere følgende globale adressebokinformasjon for personer som er søkere:

- Adresseinformasjon
- Kontaktinformasjon
- Identifikasjonsinformasjon
- Navnedetaljer
- Personlig informasjon

## <a name="applications"></a>Søknader

Du kan registrere informasjon fra jobbsøknader du mottar på siden **Søknad**. Søknaden er søkerens uttrykk for interesse for en stilling i organisasjonen. Hvis du vil opprette en søknad, må søkeren allerede finnes som en søker eller en person i systemet.

Jobbsøknader som sendes av søkere på weben, er enten anmodede søknader som ble sendt som svar på en stillingsannonse, eller uanmodede søknader. Anmodede søknader blir automatisk tilknyttet rekrutteringsprosjektet som stillingsannonsen ble opprettet fra. Uanmodede søknader knyttes til rekrutteringsprosjektet som er angitt i **Rekruttering**-området på siden **Personalparametere**.

### <a name="application-status"></a>Søknadsstatus

Søknadsstatus angir hvor en søknad er i rekrutteringsprosessen. Tabellen nedenfor viser de mulige søknadsstatusene og tilhørende beskrivelser.

| Status    | Viser at ...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Mottatt  | Søknaden er mottatt.                                                             |
| Bekreftet | Det kan sendes beskjed til søkeren om at søknaden er mottatt.            |
| Intervju | Det kan sendes en innkalling til intervju til søkeren.                                     |
| Avslag | Det kan sendes et avslagsbrev til søkeren.                                          |
| Avbrutt  | Det kan sendes en bekreftelse på at søknaden er trukket tilbake, til søkeren. Denne statusen tilordnes manuelt. |
| Ansatt  | Det kan sendes et tilbud om ansettelse til søkeren.                                         |

### <a name="correspondence-actions"></a>Korrespondansehandlinger

En **søknads** korrespondansehandling bestemmer dokument- eller e-postmalen du bruker til å kommunisere med søkeren som sendte inn søknaden. Du kan knytte til **søknadsbokmerker** med korrespondansehandlinger, slik at du kan bruke verdier fra søknaden, søkeren, intervjuet og rekrutteringsprosjektet i kommunikasjon med søkere. **E-postmaler for søknad** kan opprettes for korrespondansehandlinger for raskt å sende e-postmeldinger til søkere som har en søknad med en bestemt status og korrespondansehandlingskombinasjon. Du kan for eksempel sende en e-postmelding med bekreftelse for alle programmer med en **Status** mottatt og en **korrespondansehandling** som er mottatt. Etter sending av e-post, har du muligheten til å automatisk oppdatere status for søknadene.

## <a name="application-routing"></a>Søknadsruting

Hvis en søknad må vurderes av flere arbeidere, kan du bruke siden **Søknadsruting** for å opprette en sirkuleringsliste for arbeidere for å administrere prosessen.

## <a name="interviews"></a>Intervjuer

**Søkerintervjuer** kan være planlagt fra **Søknader**-siden. Bruk knappen **Send møteinformasjon** til å sende en kalenderfil med informasjon om intervjutidsplanen til søkeren og intervjueren.

## <a name="skill-mapping"></a>Kompetansesøk

**Kompetansesøk** og **Profiler for kompetansesøk** kan brukes til å identifisere kandidater som kan egne seg for en ledig stilling.

## <a name="hiring-applicants"></a>Ansette søkere

Bruk siden **Søknader** for å ansette en søker. Når du ansetter en søker, vil søknadsposten ha statusen **Ansatt** og søkerens personoppføring for global adressebok knyttes til den nye arbeiderposten. Endringer i den globale adressebokinformasjon for den nye arbeiderposten vises også i søkerposten. Dette kan redusere dataregistrering hvis den nye arbeideren fortsatt søker på en annen jobb innenfor organisasjonen. For å ansette en eksisterende arbeider til en ny stilling velger du **Endre stilling** i rullegardinmenyen **Søknadsstatus** for å starte overføringsprosessen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]