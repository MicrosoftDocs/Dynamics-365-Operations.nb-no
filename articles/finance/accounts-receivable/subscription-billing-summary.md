---
title: Oversikt over abonnementsfakturering
description: Denne artikkelen beskriver abonnementsfakturering i Microsoft Dynamics 365 Finance.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 10302e9ae7dff3d018897b666caaf4d4289b4866
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856748"
---
# <a name="subscription-billing-overview"></a>Oversikt over abonnementsfakturering

[!include [banner](../includes/banner.md)]

Med abonnementsfakturering kan organisasjoner administrere abonnementsinntektsmuligheter og gjentakende fakturering gjennom faktureringsplaner. Komplekse prissettings- og faktureringsmodeller og inntektstildeling kan enkelt administreres, og faktureres og føres på linjenivå. Inntektstildeling med flere elementer gjør at tildeling av inntekt kan samsvare med internasjonale regnskapsstandarder (International Financial Reporting Standard 15 \[IFRS 15\]) og standarder i Generally Accepted Accounting Principles (US GAAP) (Accounting Standards Codification Topic 606 \[ASC 606\]).

Løsningen har tre moduler som kan brukes uavhengig av hverandre. Alle tre modulene kan alternativt brukes sammen.

- **Gjentakende kontraktfakturering** – Denne modulen gjør at gjentakende fakturering og prisstyring gir kontroll over parametere for prissetting og fakturering, kontraktsfornyelse og konsolidert fakturering.
- **Inntekts- og utgiftshenvisninger** – Denne modulen fjerner manuelle prosesser og avhengighet av eksterne systemer ved å administrere inntekt og aktivere sanntidsinnsikt i månedlig gjentakende inntekt.
- **Inntektstildeling med flere elementer** – Denne modulen bidrar til forskriftssamsvar for inntekt ved å håndtere prissetting og inntektstildeling på tvers av flere varer.

Hvis du vil ha mer informasjon om abonnementsfakturering, kan du se [Power BI-innhold for abonnementsfakturering](sub-bill-power-bi.md).

Abonnementsfakturering aktiveres via **Funksjonsbehandling**. Den kan imidlertid ikke brukes med funksjonen **Inntektsføring**. Du må derfor deaktivere denne funksjonen før du aktiverer abonnementsfakturering.

1. Angi **Inntektsføring** i filteret i **Alle**-fanen i arbeidsområdet **Funksjonsbehandling**, og velg deretter funksjonsnavnet som filter.
2. Velg funksjonen **Inntektsføring**, og velg deretter **Deaktiver**.
3. Angi **Abonnementsfakturering** i **Funksjonsnavn**-filteret, og velg deretter modulfilteret.
4. Velg funksjonen **Abonnementsfakturering**, og velg deretter **Aktiver**.
5. Velg en av de tre modulene fra den forrige listen, og velg deretter **Aktiver**. Gjenta dette trinnet for hver av de to andre modulene.

    > [!IMPORTANT]
    > Funksjonen **Abonnementsfakturering** må være aktivert før du kan aktivere noen av de tre modulene.
