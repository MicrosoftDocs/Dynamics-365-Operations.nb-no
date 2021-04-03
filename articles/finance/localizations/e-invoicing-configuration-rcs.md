---
title: Konfigurere tillegget for elektronisk fakturering i RCS (Regulatory Configuration Services)
description: Dette emnet beskriver hvordan du konfigurerer tillegget for elektronisk fakturering i Dynamics 365 Regulatory Configuration Services (RCS).
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 99fac9a42dc2b180c220612c66fe753d43e5bd7f
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592628"
---
# <a name="configure-the-electronic-invoicing-add-on-in-regulatory-configuration-services-rcs"></a>Konfigurere tillegget for elektronisk fakturering i RCS (Regulatory Configuration Services)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om konfigurasjonsfunksjonene i tillegget for elektronisk fakturering i Dynamics 365 Regulatory Configuration Services (RCS).

Via konfigurasjonsfunksjonene hjelper tillegget for elektronisk fakturering deg med å oppfylle forretningsmessige og forskriftsmessige krav til elektroniske fakturaer uten at du trenger å bruke koding. I scenarioer der elektroniske fakturaer må godkjennes elektronisk av en webtjeneste, hjelper konfigurasjonsfunksjonene deg også med å oppfylle kravene til utveksling av meldinger med en webtjenester, uten å gjøre noen kode.

## <a name="electronic-reporting"></a>Elektronisk rapportering

Elektronisk rapportering (ER) støtter tillegget for elektronisk fakturering.

Datamodelltilordningen og formatene er konfigurerbare komponenter som opprettes og vedlikeholdes gjennom ER og brukes i tillegget for elektronisk fakturering. ER-formatdesigneren er verktøyet for oppretting og vedlikehold av filformater. Den brukes til å konfigurere funksjonene for elektronisk fakturering.

Hvis du vil ha mer informasjon, se [Oversikt over elektronisk rapportering (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Elektronisk fakturering-funksjoner

Funksjonene for elektronisk fakturering genererer elektroniske fakturaer via tillegget for elektronisk fakturering. De omfatter konfigurasjonsregler og bruker dem til å behandle data som Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management sender til tillegget for elektronisk fakturering og til elektroniske fakturaer.

Funksjonene støtter også scenarioer der samsvar med filformatspesifikasjoner er nødvendig, og utdataene er en frittstående elektronisk fil. I de fleste tilfeller publiseres filformatspesifikasjonene av skattemyndighetene.

Funksjonene støtter dessuten utveksling av meldinger med eksterne webtjenester som er vert for enten skattemyndighetene eller en akkreditert part, og forespørsler om autorisasjon eller et godkjenningsstempel i den elektroniske fakturaen.

### <a name="availability-of-electronic-invoicing-features"></a>Tilgjengelighet for funksjoner for elektronisk fakturering

Tilgjengeligheten for funksjonene for elektronisk fakturering er avhengig av landet eller området. Noen funksjoner er generelt tilgjengelige, mens andre er i forhåndsversjon.

#### <a name="preview-features"></a>Forhåndsvisningsfunksjoner

Følgende tabell viser funksjonene for elektronisk fakturering som for øyeblikket er i forhåndsversjon.

| Land/område | Funksjonsnavn                         | Forretningsdokument |
|----------------|--------------------------------------|-------------------|
| Østerrike        | Østerrikske elektroniske fakturaer (AT)    | Salgs- og prosjektfakturaer |
| Belgia        | Belgisk elektronisk faktura (BE)      | Salgs- og prosjektfakturaer |
| Brasil         | Brasiliansk NF-e (BR)                  | Regnskapsdokumentmodell 55, korreksjonsbrev, annulleringer og forkastelser |
| Brasil         | Brasiliansk NFS-e ABRASF Curitiba (BR) | Skattedokumenter for tjenester |
| Danmark        | Dansk elektronisk faktura (DK)       | Salgs- og prosjektfakturaer |
| Egypt          | Egyptisk elektronisk faktura (EG) | Salgs- og prosjektfakturaer |
| Estland        | Estisk elektronisk faktura (EE)     | Salgs- og prosjektfakturaer |
| Finland        | Finsk elektronisk faktura (FI)      | Salgs- og prosjektfakturaer |
| Frankrike         | Fransk elektronisk faktura (FR)       | Salgs- og prosjektfakturaer |
| Tyskland        | Tysk elektronisk faktura (DE)       | Salgs- og prosjektfakturaer |
| Italia          | FatturaPA (IT)                       | Salgs- og prosjektfakturaer |
| Mexico         | Meksikansk CFDI (MX)                    | Salgsfakturaer, følgesedler, lageroverføringer, betalingstillegg og annulleringer |
| Nederland    | Nederlandsk elektronisk faktura (NL)        | Salgs- og prosjektfakturaer |
| Norge         | Norsk elektronisk faktura (NO)    | Salgs- og prosjektfakturaer |
| Spania          | Spansk elektronisk faktura (ES)      | Salgs- og prosjektfakturaer |
| Europa         | Elektronisk faktura i PEPPOL-format            | PEPPOL salgsfakturaer og projektfakturaer |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Konfigurerbare komponenter i elektronisk fakturering-funksjoner

Funksjonene for elektronisk fakturering består av følgende grupper av konfigurerbare komponenter:

- **Formater** – Ved bruk av formater kan du konfigurere hva det elektroniske fakturerings tillegget må generere når et elektronisk dokument blir til en elektronisk faktura. Formater inkluderer formatkonfigurasjonen for den elektroniske fakturaen og for filer og meldinger som brukes til å sende forespørsler og motta svar når kommunikasjon med en ekstern webtjeneste er nødvendig.
- **Handlinger** – Handlinger lar deg konfigurere hvordan tillegget for elektronisk fakturering genererer transformasjonen av et elektronisk dokument som Finance og Supply Chain Management sendte til en elektronisk faktura.
- **Gjeldende regler** – Med gjeldende regler kan du konfigurere konteksten som tillegget for elektronisk fakturering må vurdere å behandle en elektronisk fakturering-funksjon.
- **Variabler** – Variabler lar deg konfigurere støtten for oppbygging av konfigurasjonslogikken. Variabler kan fungere som inndata for verdier for å utføre en bestemt handling. Alternativt kan de fungere som en utveksling av verdier mellom Finance og Supply Chain Management og tillegget for elektronisk fakturering.
- **Elektronisk dokumentmodelltilordning** – Med den elektroniske dokumentmodelltilordningen kan du konfigurere ER-modelltilordningen. Modelltilordningen definerer datatilordningen til den abstrakte fakturaen som er integrert i tillegget for elektronisk fakturering når elektroniske dokumenter sendes.
- **Fakturakontekstmodell** – Med fakturakontekstmodellen kan du konfigurere ER-fakturakontekstmodellen og definere konteksten til en elektronisk faktureringsfunksjon.
- **Svartyper** – Svartyper lar deg konfigurere hva tillegget for elektronisk fakturering må oppdatere i Finance og Supply Chain Management som et resultat av den elektroniske fakturabehandlingen.

### <a name="formats"></a>Formater

Listene nedenfor viser ER-formatkonfigurasjonene som er tilgjengelige for funksjonene for elektronisk fakturering.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Østerrikske (AT) elektronisk fakturaer: Salgs- og prosjektfakturaer for Østerrike

- OIOUBL Salgsfaktura
- OIOUBL Prosjektfaktura
- OIOUBL Salgskreditnota
- OIOUBL Prosjektkreditnota

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgisk (BE) elektronisk faktura: Salgs- og prosjektfakturaer for Belgia

- UBL-salgsfaktura BE
- UBL-prosjektfaktura BE
- UBL-prosjektkreditnota BE
- UBL-salgskreditnota BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brasiliansk (BR) NF-e: NF-e Federal (Brasil)

- Eksportformat for NF-e-innsending (BR)
- Eksportformat for NF-e-korreksjonsbrev (BR)
- Eksportformat for NF-e-annullering (BR)
- Eksportformat for NF-e-forkasting (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brasiliansk NFS-e (BR): NFS-e ABRASF Curitiba city

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF Inquire Curitiba (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Dansk (DK) elektronisk faktura: Salgs- og prosjektfakturaer for Danmark

- OIOUBL Salgsfaktura
- OIOUBL Prosjektfaktura
- OIOUBL Salgskreditnota
- OIOUBL Prosjektkreditnota

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Nederlandsk (NL) elektronisk faktura: Salgs- og prosjektfakturaer for Nederland

- UBL salgsfaktura NL
- UBL prosjektfaktura NL
- UBL prosjektkreditnota NL
- UBL salgskreditnota NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Egyptisk (EG) elektronisk faktura: Salgs- og prosjektfakturaer for Egypt

- Salgsfaktura (EG)(Fakturering)
- Prosjektfaktura (EG)(Fakturering)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Estisk (EE) elektronisk faktura: Salgs- og prosjektfakturaer for Estland

- Salgsfaktura (EE)
- Prosjektfaktura (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Finsk (FI) elektronisk faktura: Salgs- og prosjektfakturaer for Finland

- Salgsfaktura (FI)
- Prosjektfaktura (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Fransk (EG) elektronisk faktura: Salgs- og prosjektfakturaer for Frankrike

- UBL salgsfaktura FR
- UBL prosjektfaktura FR
- UBL prosjektkreditnota FR
- UBL salgskreditnota FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Tysk (DE) elektronisk faktura: Salgs- og prosjektfakturaer for Tyskland

- Salgsfaktura (DE)
- Prosjektfaktura (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Italiensk (IT) elektronisk faktura: Salgs- og prosjektfakturaer for Italia

- Salgsfaktura (IT)
- Prosjektfaktura (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Meksikansk (MX) CFDI: CFDI for Mexico

- CFDI-fakturaformat (MX)
- CFDI følgeseddel (MX)
- CFDI lageroverføring (MX)
- CFDI betalingsformat (MX)
- CFDI fakturaformat for annullering (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norsk (NO) elektronisk faktura: Salgs- og prosjektfakturaer for Norge

- OIOUBL Salgsfaktura
- OIOUBL Prosjektfaktura
- OIOUBL Salgskreditnota
- OIOUBL Prosjektkreditnota

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL elektronisk faktura: PEPPOL salgs- og prosjektfakturaer

- PEPPOL-salgsfaktura
- PEPPOL-prosjektfaktura
- PEPPOL-salgskreditnota
- PEPPOL-prosjektkreditnota

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Spansk (ES) elektronisk faktura: Salgs- og prosjektfakturaer for Spania

- Salgsfaktura (ES)
- Prosjektfaktura (ES)

### <a name="actions"></a>Handlinger

Tabellen nedenfor viser de tilgjengelige handlingene, og om de for øyeblikket er tilgjengelige eller fremdeles i forhåndsversjon.

| Handling                                        | beskrivelse                                                                  | Tilgjengelighet         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Transformere dokument                            | Kjør elektronisk rapportering-format for å transformere dokumentet.                   | Generelt tilgjengelig  |
| Signer xml-dokument                             | Signer XML-dokumenter med digital signatur.                                   | I forhåndsvisning           |
| Signere json-dokument for egyptisk skattemyndighet | Signer json-dokumenter med digital signatur for egyptisk skattemyndighet.       | Generelt tilgjengelig  |
| Integrere med egyptisk ETA-tjeneste           | Kommuniser med egyptisk skattemyndigheten.                                     | Generelt tilgjengelig  |
| Kalle opp brasiliansk SEFAZ-tjeneste                  | Integrer med brasiliansk SEFAZ-tjeneste for innsending av regnskapsdokumenter.       | I forhåndsvisning           |
| Kalle opp meksikansk PAC-tjeneste                      | Integrer med meksikansk PAC-tjeneste for CFDI-innsending.                      | I forhåndsvisning           |
| Behandle svar                              | Analyser svaret du mottok fra webtjenestesamtalen.                     | Generelt tilgjengelig  |
| Bruke MS Power Automate                         | Integrer med flyten som er innebygd i Microsoft Power Automate.                       | I forhåndsvisning           |

## <a name="configuration-providers"></a>Konfigurasjonsleverandører

Konfigurasjonsleverandører leverer funksjonene for elektronisk fakturering og ER-komponentene, for eksempel modelltilordning, formatkonfigurasjon og kontekstmodell. De publiserer funksjonene for elektronisk fakturering og ER-komponenter i det tilknyttede globale repositoriet. Derfra kan andre organisasjoner laste dem ned.

Før du konfigurerer funksjonene for elektronisk fakturering gjennom RCS må du konfigurere din egen organisasjon som en konfigurasjonsleverandør i **Elektronisk rapportering**-modulen. Hvis du ha mer informasjon om hvordan du setter en konfigurasjonsleverandør til **Aktiv**, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Vise elektroniske faktureringsfunksjoner i det globale repositoriet

Hvis du vil bla gjennom funksjonene for elektronisk fakturering som er tilgjengelige i det globale repositoriet for en bestemt konfigurasjonsleverandør, synkroniserer du organisasjonens RCS-forekomst. Når synkroniseringen er fullført, oppdateres listen over tilgjengelige funksjoner for elektronisk fakturering.

## <a name="importing-electronic-invoicing-features"></a>Importere funksjoner for elektronisk fakturering

Før du kan bruke eller konfigurere funksjonene for elektronisk fakturering, må du importere dem til organisasjonens RCS-forekomst. Importoperasjonen oppretter en lokal kopi av funksjonene og kopierer alle ER-artefaktene som funksjonene bruker (for eksempel formatkonfigurasjoner og modellkonfigurasjoner) til organisasjonens RCS-forekomst.

Du kan importere funksjonene for elektronisk fakturering fra en hvilken som helst konfigurasjonsleverandør.

## <a name="creating-electronic-invoicing-features"></a>Opprette funksjoner for elektronisk fakturering

Du kan opprette en elektronisk fakturering-funksjon fra grunnen av, eller du kan avlede den fra en annen elektronisk fakturering-funksjon.

Når du oppretter en funksjon for elektronisk fakturering fra begynnelsen av, må du manuelt legge til ER-komponentene (for eksempel funksjonsversjonskonfigurasjoner og andre konfigurasjoner, for eksempel funksjonsversjonsoppsett og programoppsett). Når du oppretter en funksjon ved å avlede den fra en annen funksjon, arver den nye funksjonen alle konfigurasjoner fra originalen. 

## <a name="electronic-invoicing-feature-version"></a>Elektronisk fakturering-funksjonsversjon

Elektronisk fakturering-funksjonene er versjonsstyrt. Når det opprettes en ny versjon, økes versjonsnummeret automatisk. En "gyldig fra"-dato kan defineres for den nye versjonen.

Funksjonsversjoner av elektronisk fakturering følger en livssyklus med opptil tre statuser:

- **Utkast** – Hvis en funksjonsversjon har denne statusen, kan du redigere konfigurasjonsattributtene og alle artefaktene (for eksempel filformatkonfigurasjoner).
- **Fullfør** – Hvis en funksjonsversjon har denne statusen, er den publisert til det globale repositoriet som er tilknyttet organisasjonen. Du kan ikke lenger redigere funksjonsversjonen eller noen av ER-komponentene.
- **Publisert** – Hvis en funksjonsversjon har denne statusen, er den publisert i tillegget for elektronisk fakturering. Du kan ikke lenger redigere funksjonsversjonen eller noen av ER-komponentene.

### <a name="feature-configurations"></a>Funksjonskonfigurasjoner

Funksjonskonfigurasjoner inneholder alle ER-formatkonfigurasjonene som funksjonene for elektronisk fakturering bruker. Alle de elektroniske filene som en elektronisk faktureringsfunksjon bruker under behandling, kommer fra formatkonfigurasjonene som er lagt til i funksjonskonfigurasjonene til denne funksjonen.

Fra funksjonskonfigurasjonene kan du gå til ER-formatdesigneren, som er ER-verktøyet som brukes til å opprette formatkonfigurasjoner.

### <a name="feature-setup"></a>Funksjonsoppsett

Funksjonsoppsett brukes i kombinasjon med funksjonskonfigurasjoner. Hvert funksjonsoppsett omfatter et sett med handlinger, funksjonsregler og variabler som gir forventet virkemåte, slik at en elektronisk faktureringsfunksjon kan oppfylle et bestemt krav fra den elektroniske fakturaen.

### <a name="application-setup"></a>Programoppsett

Programoppsettet må være tilknyttet et program som er opprettet tidligere.

Gjennom programoppsettet kan du konfigurere delen av en elektronisk faktureringsfunksjon som må utføres i Finance og Supply Chain Management. Minst tre konfigurerbare komponenter er obligatoriske, uansett funksjonen for elektronisk fakturering:

- **Tabellnavn** – Enheten i Finance og Supply Chain Management som har de posterte fakturaene, og som funksjonen for elektronisk fakturering er basert på.
- **Kontekst** – Navnet på fakturakontekstmodellen som ble konfigurert via ER.
- **Forretningsdokumenttilordning** – Navnet på fakturatilordningsmodellen som ble konfigurert via ER.

> [!IMPORTANT]
> Konfigurasjonen som angis i programoppsettet, kan vises i Finance og Supply Chain Management. Gå til **Organisasjonsstyring \> Oppsett \> parameter for elektronisk dokument**. I fanen **Elektronisk dokument** velger du **Distribuer**, og deretter velger du alternativet **Tilkoblede programmer**.

### <a name="deploying-feature-versions"></a>Distribuere funksjonsversjoner

I RCS bruker du kommandoen **Distribuer** til å målutgi en versjon av en elektronisk faktureringsfunksjon. Velg **Distribuer**, og velg deretter ett av følgende alternativer for å definere målet for distribusjonen: 

- **Servicemiljø** – Når målet for distribusjonen er servicemiljøet, blir versjonen av den elektroniske faktureringsfunksjonen publisert i servicemiljøet. Tillegget for elektronisk fakturering er da klart til å motta og behandle elektroniske dokumenter som Finance og Supply Chain Management sender.
- **Tilkoblet program** – Når målet for distribusjonen er det tilkoblede programmet, skrives konfigurasjonen som følger med programoppsettet, i forekomsten Finance og Supply Chain Management som tidligere er tilknyttet.

Bare versjoner av elektronisk fakturering-funksjon med statusen **Fullført** kan distribueres til et servicemiljø eller et tilkoblet program.

### <a name="removing-feature-versions"></a>Fjerne funksjonsversjoner

I RCS bruker du kommandoen **Fjern distribusjon** til å fjerne en bestemt versjon av den elektroniske faktureringsfunksjonen fra et servicemiljø i tillegget for elektronisk fakturering.

> [!IMPORTANT]
> Kommandoen **Fjern distribusjon** fungerer bare i servicemiljøer. Den fjerner ikke versjoner av elektronisk fakturering-funksjoner fra tilkoblede programmer.

### <a name="rebasing-electronic-invoicing-features"></a>Rebasere funksjoner for elektronisk fakturering

Når en elektronisk fakturering-funksjon er avledet fra en annen, oppdaterer kommandoen **Rebaser** den avledede funksjonen med endringene som er lansert i den opprinnelige funksjonen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Utstede elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
