---
title: Vedlikeholde leverandørsertifisering
description: Dette emnet beskriver trinnene som leverandører kan bruke til å vedlikeholde sertifiseringene ved hjelp av arbeidsområdet for leverandørsamarbeid.
author: v-kiarnd
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 932b8bc2982a7c38404ff4203fce7fb65c1182d4490d2aad5a6d78fd809ec768
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736118"
---
# <a name="maintain-vendor-certification"></a>Vedlikeholde leverandørsertifisering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver trinnene som leverandørene dine kan bruke til å vedlikeholde sertifiseringene ved hjelp av **arbeidsområdet for leverandørsamarbeid**. Eksempler på sertifiseringer kan være et WBE-selskap (Woman Business Enterprise) eller et selskap med sertifiseringen Leadership in Energy and Environment Design (LEED). Leverandører må angi sertifiseringsinformasjon i arbeidsområdet for **Leverandøropplysninger**. Derfra velger leverandører **Flere detaljer** og velger deretter **Sertifiseringer**.

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

