---
title: Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Finance and Operations
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere avtalefakturaer i Microsoft Dynamics 365 for Field Service til friktekstfakturaer i Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: nb-no
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere avtalefakturaer i Microsoft Dynamics 365 for Field Service til friktekstfakturaer i Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Maler og oppgaver

Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av avtalefakturaer fra Field Service til fritekstfakturaer i Finance and Operations.

**Navnet på malen i Dataintegrasjon:**

- Avtalefakturaer (Field Service til Fin and Ops)

**Navnet på oppgaven i Dataintegrasjonprosjektet**:

- Fakturahoder
- Fakturalinjer

Følgende synkronisering er påkrevd før synkronisering av avtalefakturaer kan inntreffe:

- Kontoer (Sales til Fin and Ops) – direkte

## <a name="entity-set"></a>Enhetssett

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| fakturaer       | Fakturahoder i fritekst for CDS-kunde |
| invoicedetails | Fakturalinjer i fritekst for CDS-kunde   |

## <a name="entity-flow"></a>Enhetsflyt

Fakturaer som opprettes fra en avtale i Field Service, kan synkroniseres til Finance and Operations via et Common Data Service (CDS)-dataintegreringsprosjekt. Oppdateringer av disse fakturaene synkroniseres til fritekstfakturaene i Finance and Operations hvis regnskapsstatusen for fritekstfakturaene er **Pågår**. Når fritekstfakturaene blir postert i Finance and Operations, og regnskapsstatusen oppdateres til **Fullført**, kan du ikke lenger synkronisere oppdateringer fra Field Service.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service

**Har linjer med avtaleopprinnelse**-feltet er lagt til i **Faktura**-enheten. Dette feltet kan garantere at bare fakturaer som opprettes fra en avtale, synkroniseres. Verdien er **sann** hvis fakturaen inneholder minst én fakturalinje som stammer fra en avtale.

**Har avtaleopprinnelse**-feltet er lagt til i **Fakturalinje**-enheten. Dette feltet kan garantere at bare fakturalinjer som opprettes fra en avtale, synkroniseres. Verdien er **sann** hvis fakturalinjen stammer fra en avtale.

**Fakturadato** er et obligatorisk felt i Finance and Operations. Feltet må derfor ha en verdi i Field Service før synkroniseringen utføres. For å imøtekomme dette kravet legges følgende logikk til:

- Hvis **Fakturadato**-feltet er tomt på **Faktura**-enheten (det vil si hvis det ikke har en verdi), blir den satt til gjeldende dato når en fakturalinje som stammer fra en avtale, er lagt til.
- Brukeren kan endre **Fakturadato**-feltet. Men når brukeren prøver å lagre en faktura som stammer fra en avtale, får han eller hun en forretningsprosessfeil hvis **Fakturadato**-feltet er tomt på fakturaen.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="in-finance-and-operations"></a>I Finance og Operations

En fakturaopprinnelse må være definert for integreringen for å skille fritekstfakturaene i Finance and Operations som er opprettet fra avtalefakturaer i Field Service. Når en faktura har en fakturaopprinnelse av typen **Integrering av avtalefaktura**, vises **Eksternt fakturanummer**-feltet i **Salgsfaktura**-hodet.

I tillegg til å vises i fakturahodet, kan **Eksternt fakturanummer**-informasjonen brukes til å sikre at fakturaer som opprettes fra Field Service-avtalefakturaer blir filtrert ut under fakturasynkronisering fra Finance and Operations til Field Service.

1. Gå til **Kunder** \> **Oppsett** \> **Opprinnelseskoder for faktura**.
2. Velg **Ny** for å opprette en ny fakturaopprinnelse.
3. I **Fakturaopprinnelige**-feltet angir du et navn for fakturaopprinnelsen, for eksempel **FS**.
4. I **Beskrivelse**-feltet skriver du inn en beskrivelse, for eksempel **Avtalefakturaer i Field Service**.
5. Merk av for **Tilordning av opprinnelsestype**.
6. Sett **Opprinnelsestype for faktura**-feltet til **Integrering av avtalefaktura**.
7. Velg **Lagre**.

### <a name="in-the-data-integration-project"></a>I dataintegrasjonsprosjektet

Oppgave: **Fakturalinjer**  

Kontroller at standardverdien for Finance and Operations-feltet **Visningsverdi for hovedkonto** oppdateres for å samsvare med den ønskede verdien.

Standardmalverdien er **401100**.

