---
title: Vedlikeholde leverandørsertifisering
description: Denne artikkelen beskriver trinnene som leverandører kan bruke til å vedlikeholde sertifiseringene ved hjelp av arbeidsområdet for leverandørsamarbeid.
author: TaylorVH
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c66952d19cddd9d4a9a102ba59e8d6d97b75ed4d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2022
ms.locfileid: "9583207"
---
# <a name="maintain-vendor-certification"></a>Vedlikeholde leverandørsertifisering

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver trinnene som leverandørene dine kan bruke til å vedlikeholde sertifiseringene ved hjelp av **arbeidsområdet for leverandørsamarbeid**. Eksempler på sertifiseringer kan være et WBE-selskap (Woman Business Enterprise) eller et selskap med sertifiseringen Leadership in Energy and Environment Design (LEED). Leverandører må angi sertifiseringsinformasjon i arbeidsområdet for **Leverandøropplysninger**. Derfra velger leverandører **Flere detaljer** og velger deretter **Sertifiseringer**.

## <a name="turn-on-the-vendor-certification-feature"></a>Aktiver funksjonen for leverandørsertifisering

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul** - *Leverandør*
- **Funksjonsnavn** - *Aktiver sertifiseringsbehandling for leverandørsamsvar*

## <a name="add-a-new-certification"></a>Legge til en ny sertifisering

Hvis du vil legge til en ny sertifisering, velger du **Legg til**-knappen som finnes over **Sertifisering**-rutenettet i arbeidsområdet for **Leverandørinformasjon**. Angi følgende informasjon:

- Sertifiseringsnummer
- Sertifiseringstype
- Sertifiseringsorganisasjon
- Sertifiseringsdato
- Gjeldsbeløp, hvis aktuelt
- Ikrafttredelsesdato
- Utløpsdato
- Kommentarer, valgfritt

Hvis det er dokumenter relatert til den bestemte sertifiseringen, kan du knytte dem til ved å velge **Dokument**-knappen.

Sertifiseringer som angis av leverandørene på denne siden, vil bli tilordnet en kilde for "Leverandør". Du kan angi sertifikatinformasjon på leverandørens vegne under leverandørbankkontoer. Informasjonen vil vises her, og kilden vil vises som **Kunde**.

Leverandører kan redigere eller slette sertifiseringene etter behov.

## <a name="vendor-collaboration-generated-certification-records"></a>Poster for genererte sertifiseringer for leverandørsamarbeid

Når en leverandør har lagt til sertifiseringsinformasjon, vil informasjonen være synlig på siden for **genererte sertifiseringer for leverandørsamarbeid**. Hvis du vil åpne siden, kan du gå til **Leverandører > Forespørsler > Leverandørrapporter > Genererte sertifiseringer for leverandørsamarbeid**. Alle nye eller endrede sertifiseringsposter vises som standard. En regnskapsassistent kan vise endringene og validere informasjonen gjennom bekreftelsesprosessen for å validere. Når informasjonen er bekreftet, kan sertifiseringsposten som vises på siden, velges og merkes som gjennomgått. Hvis du merker posten som gjennomgått, fjernes den fra standardlisten.

Alle sertifiseringsendringer er synlige på siden for **genererte sertifiseringer for leverandørsamarbeid**. Hvis en endring ikke vises på siden, kan du vise den ved å justere filtrene for leverandørkontoen, gjeldende datointervall eller velge om du vil inkludere informasjon for sertifiseringsendringer som er gjennomgått.

