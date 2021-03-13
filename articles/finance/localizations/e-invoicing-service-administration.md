---
title: Administrasjonskomponenter for Elektronisk fakturering-tillegget
description: Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av tillegget Elektronisk fakturering.
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104420"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Administrasjonskomponenter for Elektronisk fakturering-tillegget

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av tillegget Elektronisk fakturering. Det inneholder også informasjon om hvordan du konfigurerer tillegget for Elektronisk fakturering.

## <a name="azure"></a>Azure

Bruk Microsoft Azure for å opprette key vault-hemmelighetene og lagringskontoen. Deretter bruker du konfigurasjonen av tillegget for Elektronisk fakturering.

## <a name="lifecycle-services"></a>Lifecycle Services

Bruk Microsoft Dynamics Lifecycle Services (LCS) til å aktivere tillegget for mikrotjenestene på LCS-distribusjonsprosjektet.

I LCS velger du flisen **Administrasjon av forhåndsvisningsfunksjoner**, og deretter aktiverer du funksjonen **E-faktureringstjeneste**.

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) er grensesnittet som brukes til å konfigurere tillegget for Elektronisk fakturering. Ressurser som miljøer og funksjoner for elektroniske fakturering opprettes, vedlikeholdes og driftes i RCS. Når ressursene er klare, publiseres de i tilleggstjenesten for Elektronisk fakturering.

Hvis du vil ha mer informasjon om RCS, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md)

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Integrering med Elektronisk fakturering-tillegget

Før du kan bruke RCS til å konfigurere elektroniske fakturaer, må du konfigurere RCS til å tillate kommunikasjon med tillegget for Elektronisk fakturering. Du fyller ut denne konfigurasjonen i kategorien **Tillegg for elektronisk fakturering** på siden **Parametere for elektronisk rapportering**.

#### <a name="service-endpoint"></a>Tjenestesluttpunkt

URL-adressen til tillegget for Elektronisk fakturering kan variere i henhold til den geografiske plasseringen til Azure-datasenteret. I tabellen nedenfor finner du en oversikt over tilgjengelighet per område:

| Azure-datasentergeografi | URL for tjenestesluttpunkt                                                       |
|----------------------------|----------------------------------------------------------------------------|
| USA øst                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| USA vest                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| Europa, nord                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| Europa, vest                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a>App-ID

Program-IDen er IDen for programmet for Elektronisk fakturering. I dette tilfellet er verdien fast: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

#### <a name="lcs-environment-id"></a>LCS-miljø-ID

LCS-miljø-IDen er IDen for organisasjonens LCS-abonnement.

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
