---
title: Administrasjonskomponenter for Elektronisk fakturering-tillegget
description: Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av tillegget Elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592580"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Administrasjonskomponenter for Elektronisk fakturering-tillegget

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av tillegget Elektronisk fakturering. Det inneholder også informasjon om hvordan du konfigurerer tillegget for Elektronisk fakturering.

## <a name="azure"></a>Azure

Bruk Microsoft Azure for å opprette key vault-hemmelighetene og lagringskontoen. Deretter bruker du konfigurasjonen av tillegget for Elektronisk fakturering.

## <a name="lifecycle-services"></a>Lifecycle Services

Bruk Microsoft Dynamics Lifecycle Services (LCS) til å aktivere tillegget for mikrotjenestene på LCS-distribusjonsprosjektet.

> [!NOTE]
> Installasjonen av mikrotjenestetillegget i LCS krever minst en virtuell maskin på nivå 2. Hvis du vil ha mer informasjon om miljøplanlegging, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) er grensesnittet som brukes til å konfigurere tillegget for Elektronisk fakturering. Ressurser som miljøer og funksjoner for elektroniske fakturering opprettes, vedlikeholdes og driftes i RCS. Når ressursene er klare, publiseres de i tilleggstjenesten for Elektronisk fakturering.

For RCS-registrering kan du se [Regulatory Services](https://marketing.configure.global.dynamics.com/).

Hvis du vil ha mer informasjon om RCS, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md)

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Integrering med Elektronisk fakturering-tillegget

Før du kan bruke RCS til å konfigurere elektroniske fakturaer, må du konfigurere RCS til å tillate kommunikasjon med tillegget for Elektronisk fakturering. Du fyller ut denne konfigurasjonen i kategorien **Tillegg for elektronisk fakturering** på siden **Parametere for elektronisk rapportering**.

#### <a name="service-endpoint"></a>Tjenestesluttpunkt

Tillegget for elektronisk fakturering er tilgjengelig i flere geografiske områder for Azure-datasenteret. I tabellen nedenfor finner du en oversikt over tilgjengelighet per område.

| Azure-datasentergeografi |
|----------------------------|
| USA øst                    |
| USA vest                    |
| Europa, nord                   |
| Europa, vest                    |

### <a name="service-environments"></a>Tjenestemiljøer

Tjenestemiljøer er logiske partisjoner som opprettes for å støtte utføring av funksjonene for Elektronisk fakturering i tillegget for Elektronisk fakturering. Sikkserhetshemmelighetene og de digitale sertifikatene, og styringen (det vil si tilgangstillatelser), må konfigureres på tjenestemiljønivå.

Kunder kan opprette så mange tjenestemiljøer de vil. Alle tjenestemiljøene som en kunde oppretter, er uavhengige av hverandre.

Tjenestemiljøer må opprettes og vedlikeholdes i RCS. Når tjenestemiljøene er klare, må de publiseres til Elektronisk fakturering-tillegget.

#### <a name="service-environment-status"></a>Tjenesemiljøstatus

Tjenestemiljøer kan administreres via status. Mulige alternativer er:

- **Ikke publisert** – Miljøet er opprettet, men det er ennå ikke publisert.
- **Publisert** – Miljøet er publisert i tillegget for Elektronisk fakturering.
- **Endret** – Attributtene for et publisert miljø er endret, men endringene er ikke publisert ennå.

#### <a name="customer-secrets"></a>Kundehemmeligheter

Tillegget Elektronisk fakturering er ansvarlig for lagring av alle forretningsdata i Azure-ressursene som firmaet ditt eier. For å sikre at tjenesten fungerer som den skal, og at alle forretningsdataene som trengs for og genereres av tillegget Elektronisk fakturering, bare åpnes av tillegget, må du opprette to hoved-Azure-ressurser:

- En Azure Storage-konto (blob-lagring) som lagrer elektroniske fakturaer
- Et Azure Key Vault som lagrer sertifikater og URIen (Uniform Resource Identifier) for lagringskontoen

> [!NOTE]
> En dedikert Key Vault- og kundelagringskonto må tilordnes spesifikt for bruk med tillegget Elektroniske fakturering.

Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

#### <a name="users"></a>Brukere

Hvert tjenestemiljø må vise en liste over brukerne som kan koble seg til fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering-tillegget.

#### <a name="publication"></a>Publisering

Tjenestemiljøene må de publiseres til Elektronisk fakturering-tillegget før de kan brukes. Det er bare tilgang til publiserte miljøer fra Finance og Supply Chain Management. I tillegg må et tjenestemiljø publiseres før eventuelle oppdateringer av attributtene trer i kraft på den elektroniske faktureringstjenesten.

### <a name="connected-applications"></a>Tilkoblede programmer

Tilkoblede programmer er forekomstene av Finance og Supply Chain Management som du kanskje vil nå gjennom RCS. I tillegg til program-URLen og leietakeren inneholder et tilkoblet program legitimasjon som gjør at RCS kan koble seg til miljøet.

Gjennom de tilkoblede programmene kan du konfigurere deler av Elektronisk fakturering-funksjonen i Finance og Supply Chain Management for å få hele Elektronisk fakturering-funksjonen til å fungere.

## <a name="finance-and-supply-chain-management"></a>Finance og Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Integrering med Elektronisk fakturering-tillegg

Før du kan bruke Finance og Supply Chain Management til å utstede elektroniske fakturaer via tillegget for Elektronisk fakturering, må tillegget konfigureres slik at det er tillatt å kommunisere med tjenesten.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Integreringsfunksjon for tillegget Elektronisk fakturering

Hvis du vil aktivere kommunikasjon mellom Finance og Supply Chain Management og tillegget for Elektronisk fakturering, må du aktivere funksjonen for **Integrering av tillegget Elektronisk fakturering** i arbeidsområdet for **Funksjonsbehandling**.

#### <a name="service-endpoint"></a>Tjenestesluttpunkt

Endepunktet for tjeneste er URL-adressen der tillegget for Elektronisk fakturering er plassert. Før du elektroniske fakturaer kan utstedet må endepunktet for tjenesten konfigurere i Finance og Supply Chain Management, slik at det er tillatt å kommunisere med tjenesten.

For å konfigurere tjenestesluttpunktet, kan du gå til **Organisasjonsadministrasjon \> Oppsett \> parametere for elektronisk dokument**, og deretter, i fanen **Innsendingstjenester** i feltet **URL for tillegg for Elektronisk faktura**, angir du URL-en som beskrevet i tabellen som er beskrevet i delen **Tjenestesluttpunkt**.

#### <a name="environments"></a>Miljøer

Miljønavnet som angis i Finance og Supply Chain Management, refererer til navnet på miljøet som opprettes i RCS og publiseres i tillegget til Elektronisk fakturering.

Miljøet må konfigureres i kategorien **Innsendingstjenester** på siden **Parameter for elektronisk dokument**, slik at hver forespørsel om å utstede elektroniske fakturaer, inneholder miljøet der tillegget for Elektronisk fakturering kan fastslå hvilken elektronisk faktureringsfunksjon som må behandle forespørselen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Konfigurere elektroniske fakturaer i RCS](e-invoicing-configuration-rcs.md)
- [Utstede elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
