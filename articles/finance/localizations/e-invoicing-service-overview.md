---
title: Oversikt over elektronisk fakturering
description: Dette emnet gir informasjon om Elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 815e3f15f97c7f7083c4044b9f61bd05a33624cc
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778190"
---
# <a name="electronic-invoicing-overview"></a>Oversikt over elektronisk fakturering

[!include [banner](../includes/banner.md)]

Elektronisk fakturering for Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management er en hyperskalerbar flerklientstjeneste som muliggjør konfigurerbar behandling av elektroniske fakturadokumenter og konfigurerbare dokumentutvekslinger. Reglene for behandling og integrering er fullstendig konfigurerbar, og logikken kjøres utenfor Finance og Supply Chain Management. Tjenesten er hovedsakelig rettet mot e-fakturabehandling i scenarier knyttet til offentlige myndigheter, men den kan være egenkonfigurert for andre formål.

Elektronisk fakturering kan hjelpe deg med å oppnå følgende mål:

- Rask og enkel tilpasning av land/område-spesifikke krav
- Standardisert implementering av en løsning for Elektronisk fakturering
- Forbedret sporing for dokumentlogg
- Kortere implementeringssyklus
- Reduserte totale eierkostnader (TCO)
- Enkelt justerbare konfigurasjoner som ikke krever kodeendringer
- Forenklet konfigurasjonsemballasje
- Innebygd eksport, import og integrering, og enkel utvidelse ved behandling av e-fakturadokumenter
- Enkel gjenbruk av samme eksport-, import- og integreringskonfigurasjoner på tvers av firmaer

Hvis du vil bruke Elektronisk fakturering, må du installere det fra prosjektet ditt i Microsoft Dynamics Lifecycle Services (LCS). Deretter følger du installasjonsprosedyren for å aktivere integreringen med Finance eller Supply Chain Management. Hvis du vil ha mer informasjon, kan du se [Komme i gang med Elektronisk fakturering](e-invoicing-get-started.md).

## <a name="service-availability"></a><a name="availability"></a>-servicetilgjengelighet

For øyeblikket er Elektronisk fakturering tilgjengelig for kunder via forhåndsversjonsprogrammet, og i neste fase blir tjenesten generelt tilgjengelig. Fordi funksjonalitet som håndterer lands-/regionsspesifikke krav, kan være begrenset til ulike faser i utgivelsen, bør du alltid se i den mest oppdaterte dokumentasjonen som fremhever dekningen og omfanget av støttede land/område-spesifikke løsninger.

Elektronisk fakturering distribueres i følgende Azure-områder:

- USA
- Europa
- Storbritannia
- Asia

> [!NOTE]
> Elektronisk fakturering støtter ikke lokale distribusjoner.

## <a name="extended-configurability"></a>Utvidet konfigurerbarhet

Elektronisk fakturering kan brukes i situasjoner der du må opprette og sende et elektronisk dokument til utpekte parter. Den er spesielt utformet for å kjøre en konfigurerbar flyt av behandlingshandlinger basert på mottatte data. De konfigurerbare alternativene som er tilgjengelige i Finance og Supply Chain Management, er begrenset til dokumenttransformasjonen. Tjenesten utvider disse alternativene ved å legge til konfigurerbare integreringer som er tilgjengelige i den. I tillegg vil alle de elektroniske fakturafunksjonene som tidligere var tilgjengelige, for eksempel Brazilian Nota fiscal eletrônica (NF-e), meksikanske Comprobante Fiscal Digital por Internet (CFDI) eller andre vesteuropeiske Universal Business Language (UBL)/Pan-European Public Procurement OnLine (PEPPOL), bruke konfigurasjoner for eksport og import, og for å aktivere integreringer med eksterne webtjenester.

## <a name="feature-highlights"></a>Funksjonsfremhevinger

- Enkel integrasjon med Finance og Supply Chain Management
- Konsekvent brukeropplevelse for konfigurasjon og overvåking av e-fakturaprosessen for alle land eller områder
- Raskere, enklere og rimeligere bruk av Elektronisk fakturering i nye land eller områder
- Konfigurasjon av tjenesten ved hjelp av Regulatory Configuration Service (RCS) og funksjonsoppsett for globalisering
- Transformasjon av forretningsdata til flere e-fakturaformater (XML, JavaScript Object Notation \[JSON\], TXT og kommadelte verdier \[CSV\]) ved hjelp av konfigurasjoner som er definert i RCS:

    - Elektroniske rapporteringsformater som er tilgjengelige for land eller områder der konfigurerbarheten for e-fakturatransformasjon ikke er tilgjengelig

- Konfigurerbar innsending av e-fakturaer til eksterne webtjenester, inkludert sertifiseringshåndtering via digitale signaturer:

    - Innebygd, lett utvidbar og konfigurerbar integrering med tilleggsinnhold for flere land

    > [!NOTE]
    > For øyeblikket støttes et begrenset antall direktesendinger. Hvis du vil ha mer informasjon, kan du se delen [Tjenestetilgjengelighet](#availability) tidligere i dette emnet. Støtte vil bli utvidet i fremtiden.

- Behandling av svar fra webtjenester, inkludert behandling av konfigurerbare unntaksmeldinger
- Støtte for elektroniske signaturer (for eksempel ved å bruke XMLDSig-signeringsalgoritme)
- Satsvis behandling av e-fakturameldinger

## <a name="architecture-and-data-flow"></a>Arkitektur og dataflyt

Når Elektronisk fakturering er installert fra LCS, og det nødvendige oppsettet er fullført i alle nødvendige programmer, opprettes det en sikker tilkobling. Tjenesten finnes for øyeblikket i datasentre i USA og Europa. Derfor kan det hende at servicelokasjonen avviker fra plasseringen til den relaterte forekomsten Finance eller Supply Chain Management. Når du har fullført oppsettet av Elektronisk fakturering og slår på integreringen, sendes hoveddata og transaksjonsdata som er relatert til et bestemt dokument, til Elektronisk fakturering når en elektronisk faktura sendes.

> [!NOTE]
> Hvis den elektroniske fakturaen eller et annet dokument inneholder personlige data, må du kontrollere at bruken av denne funksjonen oppfyller EUs personvernforordning (GDPR) og andre regler som er knyttet til overføringen av personlige data.

### <a name="high-level-description-of-the-data-flow"></a>Beskrivelse på høyt nivå av dataflyten

1. Klienten sender et kanonisk forretningsdokument til tjenesten.
2. Basert på kontekstinformasjonen som er mottatt fra klienten, velger tjenesten den aktuelle behandlingsflyten.
3. Tjenesten kjører behandlingshandlingene. Disse handlingene kan inkludere å transformere forretningsdokumentet til en elektronisk faktura, bruke en elektronisk signatur og sende dokumentet til en ekstern webtjeneste.
4. Alle mottatte og behandlede dokumenter lagres i kundens Azure Blob storage.
5. Alle leierhemmeligheter og -sertifikater som ble brukt til behandling, lagres i kundens Azure Key Vault.
6. Tjenesten inneholder behovsbetinget informasjon til klienten om behandlingsstatusen til forretningsdokumentet som ble sendt.
7. Klienten mottar informasjon om fullført behandlingskjøring og gjør all logginformasjon tilgjengelig. Det gjør også dokumentet som ble opprettet eller mottatt under flytbehandling, tilgjengelig.

Illustrasjonen nedenfor viser hvordan dataflyter til og fra Elektronisk fakturering.

![Dataflyt for Elektronisk fakturering.](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Personvernerklæring
Aktivering og bruk av Elektronisk fakturering kan kreve sending av begrensede data, som inkluderer registrerings-IDen for organisasjonen. Dette overføres til tredjepartsleverandører autorisert av skattemyndighetene for å sende elektroniske fakturaer i de forhåndsdefinerte formatene som kreves for integrering med disse myndighetenes webtjenester. Data som er importert fra disse eksterne systemene til denne Dynamics 365-elektroniske tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene om personvernerklæring i dokumentasjon for landspesifikke funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser
- [Tjenesteadministrasjon](e-invoicing-service-administration.md)
- [Konfigurere elektroniske fakturaer i RCS](e-invoicing-configuration-rcs.md)
- [Utstede elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
