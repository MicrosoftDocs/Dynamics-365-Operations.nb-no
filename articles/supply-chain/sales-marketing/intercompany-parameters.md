---
title: Konserninterne parametere
description: Dette emnet forklarer konserninterne parametere
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 705efee84b255105ba39c603d23d2509e77b331a
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548448"
---
# <a name="intercompany-parameters"></a>Konserninterne parametere

[!include [banner](../../includes/banner.md)]

I en konsernintern organisasjon kan du definere parametere som bestemmer hvordan du handler mellom de ulike juridiske enhetene. Disse parameterne bestemmes av feltene du velger. Du kan velge ulike kombinasjoner for å gjenspeile ulike handelsscenarier.

Følgende to eksempler beskriver scenarioer for konserninterne organisasjoner, en med to nivåer og en med tre nivåer.

## <a name="example-1-two-level-intercompany-chain"></a>Eksempel 1: Konsernintern kjede med to nivåer

Den konserninterne organisasjonen inneholder følgende juridiske enheter:

- Juridisk enhet A – Selger til eksterne kunder, men har ingen beholdning. Denne juridiske enheten kjøper fra Juridisk enhet B.
- Juridisk enhet B – Selger bare til juridisk enhet A.

Begge juridiske enheter kan selge til og kjøpe fra hverandre.

I dette eksempelet er prissettingen for den opprinnelige salgsordren, som sendes til den eksterne kunden, alltid basert på salgsprisen. Prissettingen for den konserninterne salgsordren og den konserninterne bestillingen styres av intern salgs-/overføringsprissetting på den konserninterne salgsordren i juridiske enhet B.

Informasjonen i ordrehodet styres fra den opprinnelige salgsordren til den eksterne kunden. Alle endringer i den konserninterne salgsordren er ikke synkronisert med den opprinnelige salgsordren.

Velg **Bestillingspolicyer** på **Konsernintern**-siden for leverandører i Juridisk enhet A. Velg følgende felt i feltgruppen **Opprinnelig salgsordre (direktelevering)**:

- **Skriv ut følgeseddel automatisk**
- **Poster faktura automatisk**
- **Skriv ut faktura automatisk**

Velg følgende felt i feltgruppen In the **Konsernintern bestillinger (direktelevering)**:

- **Poster faktura automatisk**

Velg følgende felt i gruppen **Opprinnelig salgsordre<-> Konsernintern bestilling**:

- **Kundeopplysninger**
- **RMA-nummer**

Velg følgende felt i feltgruppen **Konsernintern bestilling<-> Konsernintern salgsordre**:

- **Kundeopplysninger**
- **RMA-nummer**
- **Partinummer**
- **Serienummer**

Velg **Salgsordrepolicyer** på **Konsernintern**-siden for kunder i Juridisk enhet B. Velg følgende felt i feltgruppen **Opprett konsernintern salgsordre**:

- **Salgsordrenummerering** : **Firma + opprinnelig nummer**
- **Tillat samleoppdatering av dokumenter for opprinnelig kunde**

Velg følgende felt i feltgruppen **Konserninterne salgsordrepriser**:

- **Pris- og rabattsøk**
- **Tillat prisredigering**
- **Tillat rabattredigering**

Velg følgende felt i feltgruppen **Konsernintern bestilling \> Konsernintern bestilling**:

- **Partinummer**
- **Serienummer**

## <a name="example-2-three-level-intercompany-chain"></a>Eksempel 2: Konsernintern kjede med tre nivåer

Den konserninterne organisasjonen inneholder følgende juridiske enheter:

- Juridisk enhet A – En juridisk salgsenhet som selger til eksterne kunder og kjøper fra juridisk enhet B.
- Juridisk enhet B – En juridisk enhet for produksjon eller distribusjon som ikke kan levere produkter, og kjøper fra juridisk enhet C.
- Juridisk enhet C – En juridisk enhet for produksjon eller distribusjon som leverer produkter til juridisk enhet B.

Prissetting av intern overføring mellom juridiske enheter B og C er ved kostnad fra selgende juridisk enhet ved starten av kjeden. Det er også ved kostnad til juridisk enhet A, som selger til eksterne kunder. Prissettingen på den opprinnelige salgsordren til den eksterne kunden er imidlertid alltid basert på salgsprisen.

Prissetting på alle konserninterne salgsordrer og konserninterne bestillinger styres av den konserninterne salgsordren. Den styres ved starten av kjeden. Derfor kontrollerer juridisk enhet C, som selger til juridisk enhet B, prisen. Konsernintern salgsordreprissetting er basert på prissetting av internt salg/overføring som defineres i juridisk enhet C.

Informasjonen i ordrehodet styres fra den opprinnelige salgsordren til den eksterne kunden. Alle endringer i konserninterne ordrer blir ikke synkronisert mot den opprinnelige salgsordren.

Du må velge følgende parametere:

Velg **Bestillingspolicyer** på **Konsernintern**-siden for leverandører i Juridisk enhet A. Velg følgende felt i feltgruppen **Opprinnelig salgsordre (direktelevering)**:

- **Skriv ut følgeseddel automatisk**
- **Poster faktura automatisk**
- **Skriv ut faktura automatisk**

Velg følgende felt i feltgruppen In the **Konsernintern bestillinger (direktelevering)**:

- **Poster faktura automatisk**

Velg følgende felt i feltgruppen **Opprinnelig salgsordre<-> Konsernintern bestilling**:

- **Kundeopplysninger**
- **RMA-nummer**

Velg følgende felt i feltgruppen **Konsernintern bestilling<-> Konsernintern salgsordre**:

- **Kundeopplysninger**
- **RMA-nummer**
- **Partinummer**
- **Serienummer**

Velg **Salgsordrepolicyer** på **Konsernintern**-siden for kunder i Juridisk enhet B. Velg følgende felt i feltgruppen **Opprett konsernintern salgsordre**:

- **Salgsordrenummerering** : **Firma + opprinnelig nummer**
- **Tillat samleoppdatering av dokumenter for opprinnelig kunde**

Velg følgende felt i feltgruppen **Konsernintern bestilling \> Konsernintern bestilling**:

- **Partinummer**
- **Serienummer**

Velg følgende felt i feltgruppen **Konsernintern postering av kundefaktura**:

- **Enhetspris er lik kostpris**
- **Start postering av opprinnelig kundefaktura**

Velg **Bestillingspolicyer** på **Konsernintern**-siden for leverandører i Juridisk enhet B. Velg følgende felt i feltgruppen **Opprinnelig salgsordre (direktelevering)**:

- **Skriv ut følgeseddel automatisk**
- **Poster faktura automatisk**
- **Skriv ut faktura automatisk**

Velg følgende felt i feltgruppen In the **Konsernintern bestillinger (direktelevering)**:

- **Poster faktura automatisk**

Velg følgende felt i feltgruppen **Opprinnelig salgsordre<-> Konsernintern bestilling**:

- **Kundeopplysninger**
- **RMA-nummer**
- **Pris og rabatt**

Velg følgende felt i feltgruppen **Konsernintern bestilling<-> Konsernintern salgsordre**:

- **Kundeopplysninger**
- **RMA-nummer**
- **Partinummer**
- **Serienummer**

Velg **Salgsordrepolicyer** på **Konsernintern**-siden for kunder i Juridisk enhet C. Velg følgende felt i feltgruppen **Opprett konsernintern salgsordre**:

- **Salgsordrenummerering** : **Nummerseriekode**
- **Tillat samleoppdatering av dokumenter for opprinnelig kunde**

Velg følgende felt i feltgruppen **Konserninterne salgsordrepriser**:

- **Pris- og rabattsøk**

Velg følgende felt i feltgruppen **Konsernintern postering av kundefaktura**:

- **Enhetspris er lik kostpris**
- **Start postering av opprinnelig kundefaktura**

Velg følgende felt i feltgruppen **Konsernintern salgsordre<-> Konsernintern bestilling**:

- **Partinummer**
- **Serienummer**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
