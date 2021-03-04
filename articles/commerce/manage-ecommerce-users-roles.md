---
title: Behandle brukere og roller for e-handel
description: Dette emnet forklarer hvordan du gir brukere tilgang til redigeringsmiljøet for Microsoft Dynamics 365 Commerce-området.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414532"
---
# <a name="manage-e-commerce-users-and-roles"></a>Behandle brukere og roller for e-handel


[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du gir brukere tilgang til redigeringsmiljøet for Microsoft Dynamics 365 Commerce-området.

For å kontrollere brukertilgang og gi brukere tillatelse til å utføre bestemte oppgaver, bruker områderedigeringsmiljøet sikkerhetsgrupper som du oppretter i Microsoft Azure Active Directory (Azure AD). Du tilordner først en ny eller eksisterende sikkerhetsgruppe fra Azure AD til hver rolle i redigeringsmiljøet. Deretter kan du gi eller oppheve tillatelser for enkeltbrukere ved å legge til disse brukerne i en passende sikkerhetsgruppe eller fjerne dem fra en sikkerhetsgruppe.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Oversikt over roller i redigeringsmiljøet

Redigeringsmiljøet for Dynamics 365 for Commerce støtter følgende roller.

| Rolle                 | Beskrivelse |
|----------------------|-------------|
| Systemansvarlig | Brukere som har denne rollen, har alle rettigheter til alle verktøy og til alle vurderinger og omtaler. De kan også opprette områder. |
| Administrator   | Brukere som har denne rollen, har alle rettigheter for alle verktøy samt vurderinger og omtaler i en gitt områdestruktur. |
| Nettprodusent         | Brukere som har denne rollen, kan opprette sider, fragmenter og maler, laste opp og administrere aktiva og supplere produkter og kategorier. |
| Leser               | Brukere som har denne rollen, kan vise sider, maler, gjenstander, fragmenter, oppsett og innstillinger, men kan ikke utføre endringer. |
| Moderator for vurderinger og omtaler        | Brukere som har denne rollen, kan sensurere produktvurderinger. |

## <a name="system-administrator-role"></a>Systemansvarlig-rollen

Når du klargjør Dynamics 365 Commerce i Microsoft Dynamics Lifecycle Services (LCS)-miljøet, blir du bedt om å oppgi en sikkerhetsgruppe for **Systemansvarlig**-rollen. Denne rollen brukes deretter automatisk på alle områder du oppretter i miljøet du konfigurerer. Sikkerhetsgruppen for denne rollen kan bare oppdateres i LCS. På siden **Områdeadministrasjon** for alle områder vises den som skrivebeskyttet og er bare til informasjonsformål.

## <a name="administrator-role"></a>Administrator-rollen

Når du oppretter et nytt område i Commerce, blir du bedt om å angi en sikkerhetsgruppe for **Administrator**-rollen. Se tabellen tidligere i dette emnet hvis du vil ha en oversikt over hvilke tillatelser denne rollen gir.

## <a name="add-or-update-security-groups"></a>Legge til eller oppdatere sikkerhetsgrupper

Når området er opprettet, har bare brukere som er i sikkerhetsgruppene som er tilknyttet **Systemansvarlig**- og **Administrator**-rollene, tilgang til redigeringsmiljøet for området. Hvis du vil tilordne brukere til **Nettprodusent**,- **Moderator for vurderinger og omtaler**- og **Leser** -rollene, må du tilordne sikkerhetsgrupper til disse rollene. Hvis du vil legge til en sikkerhetsgruppe i en rolle eller oppdatere en sikkerhetsgruppe som for øyeblikket er tilordnet en rolle, følger du denne fremgangsmåten.

1. Gå til området du vil oppdatere.
1. Åpne **Sikkerhet**-siden i **Områdebehandling**.
1. Velg rollen du vil endre.
1. Legg til sikkerhetsgrupper i roller, eller fjern sikkerhetsgrupper fra roller.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

[Vurderinger for søkemotoroptimalisering (SEO) for området](search-engine-optimization-considerations.md)

[Behandle policy for innholdssikkerhet (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]