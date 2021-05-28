---
title: Administrasjonskomponenter for elektronisk fakturering
description: Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av Elektronisk fakturering.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980930"
---
# <a name="electronic-invoicing-administration-components"></a>Administrasjonskomponenter for elektronisk fakturering

[!include [banner](../includes/banner.md)]


Dette emnet inneholder informasjon om komponentene som er knyttet til administrasjon av Elektronisk fakturering. Det inneholder også informasjon om hvordan du konfigurerer Elektronisk fakturering.

## <a name="azure"></a>Azure

Bruk Microsoft Azure for å opprette key vault-hemmelighetene og lagringskontoen. Deretter bruker du konfigurasjonen av Elektronisk fakturering.

## <a name="lifecycle-services"></a>Lifecycle Services

Bruk Microsoft Dynamics Lifecycle Services (LCS) til å aktivere mikrotjenestene på LCS-distribusjonsprosjektet.

> [!NOTE]
> Installasjonen av mikrotjenesten i LCS krever minst en virtuell maskin på nivå 2. Hvis du vil ha mer informasjon om miljøplanlegging, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) er grensesnittet som brukes til å konfigurere Elektronisk fakturering. Ressurser som miljøer og funksjoner for elektroniske fakturering opprettes, vedlikeholdes og driftes i RCS. Når ressursene er klare, publiseres de i tjenesten for Elektronisk fakturering.

For RCS-registrering kan du se [Regulatory Services](https://marketing.configure.global.dynamics.com/).

Hvis du vil ha mer informasjon om RCS, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Integrering med Elektronisk fakturering 

Før du kan bruke RCS til å konfigurere elektroniske fakturaer, må du konfigurere RCS til å tillate kommunikasjon med Elektronisk fakturering. Du fyller ut denne konfigurasjonen i kategorien **Elektronisk fakturering** på siden **Parametere for elektronisk rapportering**.

#### <a name="service-endpoint"></a>Tjenestesluttpunkt

Elektronisk fakturering er tilgjengelig i flere geografiske områder for Azure-datasenteret. I tabellen nedenfor finner du en oversikt over tilgjengelighet per område.

| Azure-datasentergeografi |
|----------------------------|
| USA              |
| Europa                     |
| Storbritannia             |
| Asia                       |

### <a name="service-environments"></a>Tjenestemiljøer

Tjenestemiljøer er logiske partisjoner som opprettes for å støtte utføring av funksjonene for elektronisk fakturering i Elektronisk fakturering. Sikkserhetshemmelighetene og de digitale sertifikatene, og styringen (det vil si tilgangstillatelser), må konfigureres på tjenestemiljønivå.

Kunder kan opprette så mange tjenestemiljøer de vil. Alle tjenestemiljøene som en kunde oppretter, er uavhengige av hverandre.

Tjenestemiljøer må opprettes og vedlikeholdes i RCS. Når tjenestemiljøene er klare, må de publiseres til Elektronisk fakturering.

#### <a name="service-environment-status"></a>Tjenesemiljøstatus

Tjenestemiljøer kan administreres via status. Mulige alternativer er:

- **Ikke publisert** – Miljøet er opprettet, men det er ennå ikke publisert.
- **Publisert** – Miljøet er publisert i Elektronisk fakturering.
- **Endret** – Attributtene for et publisert miljø er endret, men endringene er ikke publisert ennå.

#### <a name="customer-secrets"></a>Kundehemmeligheter

Tjenesten Elektronisk fakturering er ansvarlig for lagring av alle forretningsdata i Azure-ressursene som firmaet ditt eier. For å sikre at tjenesten fungerer som den skal, og at det blir gitt tilgang til alle forretningsdataene som trengs for og genereres av Elektronisk fakturering, på riktig måte, må du opprette to hoved-Azure-ressurser:

- En Azure Storage-konto (blob-lagring) som lagrer elektroniske fakturaer
- Et Azure Key Vault som lagrer sertifikater og URIen (Uniform Resource Identifier) for lagringskontoen


En dedikert Key Vault- og kundelagringskonto må tilordnes spesifikt for bruk med Elektronisk fakturering. Hvis du vil ha mer informasjon, kan du se [Opprette en Azure Storage-konto og et Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

Hvis du vil overvåke Key Vault-tilstanden og motta varsler, konfigurerer du Azure Monitor for key vault. Ved å aktivere Key Vault-logging kan du overvåke hvordan, når og hvem som har tilgang til dine Key Vaults. Hvis du vil ha mer informasjon, kan du se [Overvåking og varsling for Azure Key Vault](/azure/key-vault/general/alert) og [Hvordan du aktiverer Key Vault-logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Det er en god fremgangsmåte å rotere hemmeligheter med jevne mellomrom. Hvis du vil ha mer informasjon, kan du se i [Hemmelighetsdokumentasjon](/azure/key-vault/secrets/).

#### <a name="users"></a>Brukere

Hvert tjenestemiljø må vise en liste over brukerne som kan koble seg til fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering.

#### <a name="publication"></a>Publisering

Tjenestemiljøene må de publiseres til Elektronisk fakturering før de kan brukes. Det er bare tilgang til publiserte miljøer fra Finance og Supply Chain Management. I tillegg må et tjenestemiljø publiseres før eventuelle oppdateringer av attributtene trer i kraft på den elektroniske faktureringstjenesten.

### <a name="connected-applications"></a>Tilkoblede programmer

Tilkoblede programmer er forekomstene av Finance og Supply Chain Management som du kanskje vil nå gjennom RCS. I tillegg til program-URLen og leietakeren inneholder et tilkoblet program legitimasjon som gjør at RCS kan koble seg til miljøet.

Gjennom de tilkoblede programmene kan du konfigurere deler av Elektronisk fakturering-funksjonen i Finance og Supply Chain Management for å få hele Elektronisk fakturering-funksjonen til å fungere.

## <a name="finance-and-supply-chain-management"></a>Finance og Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Integrering med Elektronisk fakturering

Før du kan bruke Finance og Supply Chain Management til å utstede elektroniske fakturaer via Elektronisk fakturering, må det konfigureres slik at det er tillatt å kommunisere med tjenesten.

#### <a name="electronic-invoicing-integration-feature"></a>Integreringsfunksjon for Elektronisk fakturering

Hvis du vil aktivere kommunikasjon mellom Finance og Supply Chain Management og Elektronisk fakturering, må du aktivere funksjonen for **Integrering av Elektronisk fakturering** i arbeidsområdet for **Funksjonsbehandling**.

#### <a name="service-endpoint"></a>Tjenestesluttpunkt

Endepunktet for tjeneste er URL-adressen der Elektronisk fakturering er plassert. Før du elektroniske fakturaer kan utstedet må endepunktet for tjenesten konfigurere i Finance og Supply Chain Management, slik at det er tillatt å kommunisere med tjenesten.

For å konfigurere tjenestesluttpunktet, kan du gå til **Organisasjonsadministrasjon \> Oppsett \> parametere for elektronisk dokument**, og deretter, i fanen **Innsendingstjenester** i feltet **URL for Elektronisk faktura**, angir du URL-en som beskrevet i tabellen som er beskrevet i delen **Tjenestesluttpunkt**.

#### <a name="environments"></a>Miljøer

Miljønavnet som angis i Finance og Supply Chain Management, refererer til navnet på miljøet som opprettes i RCS og publiseres i Elektronisk fakturering.

Miljøet må konfigureres i kategorien **Innsendingstjenester** på siden **Parameter for elektronisk dokument**, slik at hver forespørsel om å utstede elektroniske fakturaer, inneholder miljøet der Elektronisk fakturering kan fastslå hvilken elektronisk faktureringsfunksjon som må behandle forespørselen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Konfigurere elektroniske fakturaer i RCS](e-invoicing-configuration-rcs.md)
- [Utstede elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
