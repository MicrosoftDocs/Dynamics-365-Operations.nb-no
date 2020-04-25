---
title: Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management
description: Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere avtalefakturaer i Dynamics 365 Field Service til friktekstfakturaer i Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 943bf04378a8202d676cbabb282a0a6208a92ef3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210010"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management

[!include[banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere avtalefakturaer i Dynamics 365 Field Service til friktekstfakturaer i Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>Maler og oppgaver

Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av avtalefakturaer fra Field Service til fritekstfakturaer i Supply Chain Management.

**Navnet på malen i Dataintegrasjon**

- Avtalefakturaer (Field Service til Supply Chain Management)

**Navnet på oppgaven i Dataintegrasjonprosjektet**

- Fakturahoder
- Fakturalinjer

Følgende synkronisering er påkrevd før synkronisering av avtalefakturaer kan inntreffe:

- Kontoer (Sales til Supply Chain Management) – direkte

## <a name="entity-set"></a>Enhetssett

| Field Service  | Forsyningskjedeadministrasjon                 |
|----------------|----------------------------------------|
| fakturaer       | Fakturahoder i fritekst for CDS-kunde |
| invoicedetails | Fakturalinjer i fritekst for CDS-kunde   |

## <a name="entity-flow"></a>Enhetsflyt

Fakturaer som opprettes fra en avtale i Field Service, kan synkroniseres til Supply Chain Management via et Common Data Service-dataintegreringsprosjekt. Oppdateringer av disse fakturaene synkroniseres til fritekstfakturaene i Supply Chain Management hvis regnskapsstatusen for fritekstfakturaene er **Pågår**. Når fritekstfakturaene blir postert i Supply Chain Management, og regnskapsstatusen oppdateres til **Fullført**, kan du ikke lenger synkronisere oppdateringer fra Field Service.

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service

**Har linjer med avtaleopprinnelse**-feltet er lagt til i **Faktura**-enheten. Dette feltet kan garantere at bare fakturaer som opprettes fra en avtale, synkroniseres. Verdien er **sann** hvis fakturaen inneholder minst én fakturalinje som stammer fra en avtale.

**Har avtaleopprinnelse**-feltet er lagt til i **Fakturalinje**-enheten. Dette feltet kan garantere at bare fakturalinjer som opprettes fra en avtale, synkroniseres. Verdien er **sann** hvis fakturalinjen stammer fra en avtale.

**Fakturadato** er et obligatorisk felt i Supply Chain Management. Feltet må derfor ha en verdi i Field Service før synkroniseringen utføres. For å imøtekomme dette kravet legges følgende logikk til:

- Hvis **Fakturadato**-feltet er tomt på **Faktura**-enheten (det vil si hvis det ikke har en verdi), blir den satt til gjeldende dato når en fakturalinje som stammer fra en avtale, er lagt til.
- Brukeren kan endre **Fakturadato**-feltet. Men når brukeren prøver å lagre en faktura som stammer fra en avtale, får han eller hun en forretningsprosessfeil hvis **Fakturadato**-feltet er tomt på fakturaen.

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="in-supply-chain-management"></a>I Supply Chain Management

En fakturaopprinnelse må være definert for integreringen for å skille fritekstfakturaene i Supply Chain Management som er opprettet fra avtalefakturaer i Field Service. Når en faktura har en fakturaopprinnelse av typen **Integrering av avtalefaktura**, vises **Eksternt fakturanummer**-feltet i **Salgsfaktura**-hodet.

I tillegg til å vises i fakturahodet, kan **Eksternt fakturanummer**-informasjonen brukes til å sikre at fakturaer som opprettes fra Field Service-avtalefakturaer blir filtrert ut under fakturasynkronisering fra Supply Chain Management til Field Service.

1. Gå til **Kunder** \> **Oppsett** \> **Opprinnelseskoder for faktura**.
2. Velg **Ny** for å opprette en ny fakturaopprinnelse.
3. I **Fakturaopprinnelige**-feltet angir du et navn for fakturaopprinnelsen, for eksempel **FS**.
4. I **Beskrivelse**-feltet skriver du inn en beskrivelse, for eksempel **Avtalefakturaer i Field Service**.
5. Merk av for **Tilordning av opprinnelsestype**.
6. Sett **Opprinnelsestype for faktura**-feltet til **Integrering av avtalefaktura**.
7. Velg **Lagre**.

### <a name="in-the-data-integration-project"></a>I dataintegrasjonsprosjektet

Oppgave: **Fakturalinjer**  

Kontroller at standardverdien for Supply Chain Management-feltet **Visningsverdi for hovedkonto** oppdateres for å samsvare med den ønskede verdien.

Standardmalverdien er **401100**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Avtalefakturaer (Field Service til Supply Chain Management): Fakturahoder

[![Maltilordning i Dataintegrering](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Avtalefakturaer (Field Service til Supply Chain Management): Fakturalinjer

[![Maltilordning i Dataintegrering](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
