---
title: Startside for organisasjonsstyring
description: Dette emnet peker til ressurser som gjør det enklere å bruke i organisasjonen din.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b1b519d116a55c255cf90d9478ee1714de90264
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811338"
---
# <a name="organization-administration-home-page"></a>Startside for organisasjonsstyring

[!include [banner](../includes/banner.md)]

Dette emnet peker på innholdet som vil hjelpe privilegerte brukere og administratorer med å konfigurere systemet slik at det fungerer godt og effektivt for organisasjonen og bedriften din.

Mye av innholdet som er oppført her gjelder for funksjoner i modulen **Organisasjonsstyring**. Det er imidlertid et par oppgaver, for eksempel å opprette og bruke en postmal, som kan utføres i en hvilken som helst modul for å hjelpe organisasjonen din å være mer effektiv.

## <a name="number-sequences"></a>Nummerserier

Nummerserier brukes for å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er. En hoveddatapost eller transaksjonspost som krever en ID kalles en *referanse*. Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse.

- [Oversikt over nummerserier](number-sequence-overview.md)
- [Konfigurere nummerserier ved å bruke en veiviser](tasks/set-up-number-sequences-wizard.md) (Oppgaveveiledning)
- [Konfigurere nummerserier enkeltvis](tasks/set-up-number-sequences-individual-basis.md) (Oppgaveveiledning)

## <a name="organizations"></a>Organisasjoner

En organisasjon er en gruppe personer som jobber sammen for å utføre en forretningsprosess eller oppnå et mål. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.

Før du definerer organisasjoner og organisasjonshierarkier, må du passe på å planlegge hvordan virksomheten skal modelleres. Organisasjonsmodellen har en betydelig innvirkning på implementering og forretningsprosesser.

- [Oversikt over organisasjoner og organisasjonshierarkier](organizations-organizational-hierarchies.md)
- [Planlegge organisasjonshierarkiet](plan-organizational-hierarchy.md)
- [Opprette et organisasjonshierarki](tasks/create-organization-hierarchy.md) (Oppgaveveiledning)
- [Opprette en juridisk enhet](tasks/create-legal-entity.md) (Oppgaveveiledning)
- [Opprette en driftsenhet](tasks/create-operating-unit.md) (Oppgaveveiledning)

## <a name="address-books"></a>Adressebøker

Den globale adresseboken er et sentralisert lager for stamdata som må lagres for alle interne og eksterne personer og organisasjoner som selskapet samhandler med. Dataene som er knyttet til partsoppføringer inkluderer partens navn, adresse og kontaktinformasjon.

Når du oppretter den globale adresseboken, kan du opprette flere adressebøker i henhold til behovet ditt, for eksempel en egen adressebok for hvert firma i organisasjonen din eller for hver bransje.

- [Oversikt over global adressebok](overview-global-address-book.md)
- [Planlegge den globale adresseboken og andre adressebøker](plan-configuration-global-address-book-additional-address-books.md)
- [Konfigurere den globale adresseboken](tasks/configure-global-address-book.md)
- [Vanlige spørsmål om adressebøker](qa-address-books.md)

## <a name="workflow"></a>Arbeidsflyt

Arbeidsflyt er et system du kan bruke til å opprette enkle arbeidsflyter eller forretningsprosesser. Når du oppretter en arbeidsflyt spesifiserer du hvordan et dokument flyter eller flyttes gjennom systemet ved å vise hvem som må fullføre en oppgave, ta en avgjørelse, eller godkjenne et dokument.

- [Oversikt over arbeidsflytsystem](overview-workflow-system.md)
- [Arbeidsflytelementer](workflow-elements.md)
- [Handlinger i godkjenningsprosesser i en arbeidsflyt](workflow-actions.md)
- [Oversikt over å opprette arbeidsflyter](create-workflow.md)

## <a name="electronic-signatures"></a>Elektroniske signaturer

En elektronisk signatur bekrefter identiteten til en person som er i ferd med å starte eller godkjenne en dataprosess. I noen bransjer er en elektronisk signatur like bindende som er håndskrevet signatur. Elektroniske signaturer er et krav til samsvar med lovgivning for flere regulerte industrier, for eksempel legemiddelindustrien, matvareindustrien og romfarts- og forsvarsindustrien.

Du kan du bruke elektroniske signaturer for viktige forretningsprosesser. Noen prosesser har innebygde funksjoner for elektronisk signatur. Du kan også opprette egendefinerte signaturkrav for en hvilken som helst databasetabell og et hvilket som helst felt.

- [Oversikt over elektroniske signaturer](electronic-signature-overview.md)
- [Definere elektroniske signaturer](tasks/set-up-electronic-signatures.md) (Oppgaveveiledning)

## <a name="case-management"></a>Saksbehandling

Når du planlegger, sporer og analyserer tilfeller, kan du utvikle effektive løsninger som kan brukes ved lignende problemer. For eksempel, når kundeservicerepresentanter eller HR-generalister oppretter saker, kan de finne informasjon i kunnskapsartikler for å hjelpe dem med å arbeide med eller løse en sak mer effektivt.

- [Oversikt over saksbehandling](cases.md)
- [Planlegge kategorisikkerhet, saksprosesser og sakskategorier](plan-case-management.md)

## <a name="record-templates"></a>Postmaler

Postmaler kan hjelpe deg å opprette poster mer effektivt. Du kan opprette en postmal så feltverdiene som brukes ofte ikke behøver fylles inn eksplisitt for en ny post.

- [Oversikt over postmaler](record-templates.md)
- [Opprett en postmal for å fasilitere dataoppføring](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Oppgaveveiledning)
- [Bruke postmaler til å opprette en ny post](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Oppgaveveiledning)

## <a name="general-organization-administration"></a>Generell organisasjonsadministrasjon

- [Endre banner eller logo](../get-started/tasks/change-banner-or-logo.md) (Oppgaveveiledning)
- [Konfigurere dokumentstyring](configure-document-management.md)
- [Konfigurere og sende e-post](configure-email.md)
- [Dato-/klokkeslettdata og tidssoner](date-time-zones.md)
