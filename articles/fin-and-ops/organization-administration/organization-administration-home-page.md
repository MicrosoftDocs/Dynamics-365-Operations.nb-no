---
title: Startside for organisasjonsstyring
description: "Dette emnet peker på ressurser som hjelper deg med å bruke Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition i organisasjonen din."
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: eb8674a6401b11e8e33d3cba54add1fb4bca1cd3
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="organization-administration-home-page"></a>Startside for organisasjonsstyring

[!include[banner](../includes/banner.md)]


Dette emnet peker på innhold som vil hjelpe privilegerte brukere og administratorer til å konfigurere Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Dette innholdet vil hjelpe dem å konfigurere systemet så det jobber godt og effektivt for organisasjonen og bedriften din.

Mye av innholdet som er oppført her gjelder for funksjoner i modulen **Organisasjonsstyring**. Det er imidlertid et par oppgaver, for eksempel å opprette og bruke en postmal, som kan utføres i en hvilken som helst modul for å hjelpe organisasjonen din å være mer effektiv. 

<a name="number-sequences"></a>Nummerserier
----------------
Nummerserier brukes for å generere lesbare, unike ID-er for hoveddataposter og transaksjonsposter som krever ID-er. En hoveddatapost eller transaksjonspost som krever en ID kalles en *referanse*. Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse.

-   [Oversikt over nummerserie](number-sequence-overview.md)
-   [Konfigurere alle nødvendige nummerserier ved å bruke en veiviser](tasks/set-up-number-sequences-wizard.md) (Oppgaveveiledning)
-   [Konfigurere nummerserier enkeltvis](tasks/set-up-number-sequences-individual-basis.md) (Oppgaveveiledning)

## <a name="organizations"></a>Organisasjoner
En organisasjon er en gruppe personer som jobber sammen for å utføre en forretningsprosess eller oppnå et mål. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten.

Før du oppretter organisasjoner og organisasjonshierarkier i Finance and Operations, må du sørge for at du planlegger hvordan virksomheten din skal modelleres. Organisasjonsmodellen har en betydelig innvirkning på implementeringen av Finance and Operations og på forretningsprosesser.

-   [Organisasjoner og organisasjonshierarkier](organizations-organizational-hierarchies.md)
-   [Planlegge organisasjonshierarkiet](plan-organizational-hierarchy.md)
-   [Opprette et organisasjonshierarki](tasks/create-organization-hierarchy.md) (Oppgaveveiledning)
-   [Opprette en juridisk enhet](tasks/create-legal-entity.md) (Oppgaveveiledning)
-   [Opprette en driftsenhet](tasks/create-operating-unit.md) (Oppgaveveiledning)

## <a name="address-books"></a>Adressebøker
Den globale adresseboken er et sentralisert lager for stamdata som må lagres for alle interne og eksterne personer og organisasjoner som selskapet samhandler med. Dataene som er knyttet til partsoppføringer inkluderer partens navn, adresse og kontaktinformasjon. 

Når du oppretter den globale adresseboken, kan du opprette flere adressebøker i henhold til behovet ditt, for eksempel en egen adressebok for hvert firma i organisasjonen din eller for hver bransje. 

-   [Global adressebok](overview-global-address-book.md)
-   [Planlegg hvordan du konfigurerer den globale adresseboken og flere adressebøker](plan-configuration-global-address-book-additional-address-books.md)
- [Konfigurere den globale adresseboken](tasks/configure-global-address-book.md)
-   [Vanlige spørsmål om adressebøker](qa-address-books.md)


## <a name="workflow"></a>Arbeidsflyt
Arbeidsflyt er et system som er installert med Finance and Operations, og du kan bruke den for å opprette individuelle arbeidsflyter eller forretningsprosesser. Når du oppretter en arbeidsflyt spesifiserer du hvordan et dokument flyter eller flyttes gjennom systemet ved å vise hvem som må fullføre en oppgave, ta en avgjørelse, eller godkjenne et dokument. 

-   [Arbeidsflytoversikt](overview-workflow-system.md)
-   [Arbeidsflytelementer](workflow-elements.md)
-   [Arbeidsflythandlinger](workflow-actions.md)
-   [Opprette en arbeidsflyt](create-workflow.md)

## <a name="electronic-signatures"></a>Elektroniske signaturer
En elektronisk signatur bekrefter identiteten til en person som er i ferd med å starte eller godkjenne en dataprosess. I noen bransjer er en elektronisk signatur like bindende som er håndskrevet signatur. Elektroniske signaturer er et krav til samsvar med lovgivning for flere regulerte industrier, for eksempel legemiddelindustrien, matvareindustrien og romfarts- og forsvarsindustrien.

I Dynamics 365 for Finance and Operations kan du bruke elektroniske signaturer for viktige forretningsprosesser. Noen prosesser har innebygde funksjoner for elektronisk signatur. Du kan også opprette egendefinerte signaturkrav for en hvilken som helst databasetabell og et hvilket som helst felt.

-   [Oversikt over elektronisk signatur](electronic-signature-overview.md)
-   [Definere elektroniske signaturer](tasks/set-up-electronic-signatures.md) (Oppgaveveiledning)

## <a name="case-management"></a>Saksbehandling
Når du planlegger, sporer og analyserer tilfeller, kan du utvikle effektive løsninger som kan brukes ved lignende problemer. For eksempel, når kundeservicerepresentanter eller HR-generalister oppretter saker, kan de finne informasjon i kunnskapsartikler for å hjelpe dem med å arbeide med eller løse en sak mer effektivt. 

-   [Oversikt over saksbehandling](cases.md)
-   [Konfigurere sakssikkerhet, prosesser og kategorier](plan-case-management.md)

## <a name="record-templates"></a>Postmaler
Postmaler kan hjelpe deg å opprette poster mer effektivt. Du kan opprette en postmal så feltverdiene som brukes ofte ikke behøver fylles inn eksplisitt for en ny post. 

-   [Postmaler](record-templates.md)
- [Opprett en postmal for å fasilitere dataoppføring](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Oppgaveveiledning)
- [Bruk en postmal for å fasilitere opprettelse av en ny oppføring](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Oppgaveveiledning)

## <a name="general-organization-administration"></a>Generell organisasjonsadministrasjon
-   [Endre banner eller logo](../get-started/tasks/change-banner-or-logo.md) (Oppgaveveiledning)
- [Konfigurere dokumentstyring](configure-document-management.md)
- [Konfigurere og sende e-post](configure-email.md)
-   [Dato-/klokkeslettdata og tidssoner](date-time-zones.md)








