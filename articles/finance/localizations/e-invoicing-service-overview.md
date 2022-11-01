---
title: Oversikt over elektronisk fakturering
description: Denne artikkelen gir en oversikt over elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: d219863d793c837e2346d66d6b95d38191933bcc
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709188"
---
# <a name="electronic-invoicing-overview"></a>Oversikt over elektronisk fakturering

[!include [banner](../includes/banner.md)]

Elektronisk fakturering for Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management er en hyperskalerbar flerleiertjeneste som muliggjør konfigurerbar behandling av elektroniske fakturaer og konfigurerbar utveksling av elektroniske dokumenter. Reglene for behandling og integrering er fullstendig konfigurerbar, og logikken kjøres utenfor Finance og Supply Chain Management. Tjenesten er hovedsakelig rettet mot behandling av elektroniske fakturadokumenter i scenarioer fra bedrift til offentlig sektor. Den kan imidlertid konfigureres for andre formål, for eksempel bedrift-til-bedrift-scenarioer for ulike typer dokumenter.

Elektronisk fakturering kan hjelpe deg med å oppnå følgende mål:

- Rask og enkel tilpasning av land/område-spesifikke krav
- Standardisert implementering av en løsning for Elektronisk fakturering
- Forbedret sporing for dokumentlogg
- Kortere implementeringssyklus
- Reduserte totale eierkostnader (TCO)
- Enkelt justerbare konfigurasjoner som ikke krever kodeendringer
- Forenklet konfigurasjonsemballasje
- Innebygd eksport, import og integrering, og enkel utvidelse ved behandling av elektroniske fakturadokumenter
- Enkel gjenbruk av samme eksport-, import- og integreringskonfigurasjoner på tvers av firmaer

## <a name="service-availability"></a>-servicetilgjengelighet

Funksjonaliteten for elektronisk fakturering er for øyeblikket tilgjengelig for Finance- og Supply Chain Management-kunder. Hvis du vil ha mer informasjon, kan du se gjennom lisensvilkårene og -betingelsene for programmet.

Fordi funksjonalitet som håndterer lands-/områdespesifikke krav, kan være begrenset til ulike faser i utgivelsen, bør du alltid se gjennom den mest oppdaterte dokumentasjonen som fremhever dekningen og omfanget av støttede lands-/områdespesifikke løsninger.

Elektronisk fakturering distribueres i følgende Azure-områder:

- USA
- Europa
- Storbritannia
- Asia
- Japan
- Sveits
- Brasil
- De forente arabiske emirater
- Australia
- Canada
- Frankrike
- India
- Norge
- Sør-Afrika

> [!NOTE]
> Elektronisk fakturering støtter ikke lokale distribusjoner.

## <a name="feature-highlights"></a>Funksjonsfremhevinger

- Bruksklar integrering med Finance og Supply Chain Management
- En konsekvent brukeropplevelse for konfigurasjon og overvåking av prosessen for elektroniske fakturaer for alle land og områder
- Raskere, enklere og rimeligere bruk av Elektronisk fakturering i nye land eller områder
- Konfigurasjon av tjenesten via oppsettet for Regulatory Configuration Service (RCS) og globaliseringsfunksjoner
- Transformasjon av forretningsdata til flere elektroniske fakturaformater (XML, JavaScript Object Notation \[JSON\], TXT og kommadelte verdier \[CSV\]) ved hjelp av konfigurasjoner som er definert i RCS:

    - ER-formater (elektronisk rapportering) som er tilgjengelige for land og områder der konfigurerbarheten for elektronisk fakturatransformasjon ikke er tilgjengelig

- Konfigurerbar innsending av elektroniske fakturaer til eksterne nettjenester, inkludert sertifiseringshåndtering via digitale signaturer:

    - Innebygd, lett utvidbar og konfigurerbar integrering med tilleggsinnhold for flere land og områder

- Behandling av svar fra nettjenester, inkludert behandling av konfigurerbar håndtering av unntaksmeldinger
- Støtte for elektroniske signaturer (for eksempel elektroniske signaturer som bruker XMLDSig-signeringsalgoritme)
- Muligheten til å sende dokumenter til e-postmeldinger og lagre dem i SharePoint
- Satsvis behandling av elektroniske fakturameldinger
- Konfigurerbar transformasjon av innkommende dokumenter, og behandling av disse dokumentene i Finance og Supply Chain Management
- Muligheten til å motta innkommende dokumenter fra kanaler, for eksempel e-post og SharePoint

## <a name="privacy-notice"></a>Personvernerklæring

Hvis du aktiverer og bruker elektronisk fakturering, kan det hende at det må sendes begrensede data. Disse dataene inkluderer organisasjonens avgiftsregistrerings-ID. Disse dataene overføres til tredjepartsleverandører som er autorisert av skattemyndighetene til å sende elektroniske fakturaer i de forhåndsdefinerte formatene som kreves for integrering med disse myndighetenes nettjenester. Data som importeres fra disse eksterne systemene til denne nettbaserte Dynamics 365-tjenesten, er underlagt vår [personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=512132). Hvis du vil ha mer informasjon, kan du se delene Personvernmerknad i dokumentasjon for landspesifikke funksjoner.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
