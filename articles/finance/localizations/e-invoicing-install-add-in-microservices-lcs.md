---
title: Installere tilleggsprogrammet for mikrotjenester i Lifecycle Services
description: Dette emnet forklarer hvordan du installerer tilleggsprogrammet for elektronisk fakturering i Microsoft Dynamics Lifecycle Services (LCS).
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a575f3e26489607dc2143ba05c941240969a0feb
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371723"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Installere tilleggsprogrammet for mikrotjenester i Lifecycle Services

[!include [banner](../includes/banner.md)]

Autentisering i tjenesten for elektronisk fakturering krever at du registrerer Microsoft Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-miljøet i tjenesteplattformen ved å installere tilleggsprogrammet for miljøet i Microsoft Dynamics Lifecycle Services (LCS).

Følg disse trinnene for å registrere et miljø.

1. Logg på LCS-kontoen.
2. Velg et LCS-prosjekt på instrumentbordet for prosjekt.
2. Velg distribusjonsprosjektet på **Miljøer**-instrumentbordet i prosjektet. Miljøet du velger, må kjøre.
3. I fanen **Power Platform-integrering** i **Miljøtillegg**-delen velger du **Installer et nytt tilleggsprogram**.
4. Velg **Elektronisk fakturering**.
5. I feltet **App-ID for AAD** angir du **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Denne verdien er en fast verdi. Pass på at du bare angir en globalt unik identifikator (GUID). Ikke ta med andre symboler, for eksempel mellomrom, komma, punktum eller anførselstegn.
6. I feltet **AAD-leier-ID** angir du leier-IDen for kontoen for Azure-abonnementet. Leieren Azure Active Directory (Azure AD) du angir, skal være den samme leieren som brukes for Regulatory Configuration Service (RCS).
7. Gå gjennom vilkårene og betingelsene, og merk deretter av i avmerkingsboksen.
8. Velg **Installer**. Etter noen minutter skal statusen endres fra **Installerer** til **Installert**. Du må kanskje oppdatere siden for å kunne se denne endringen.

Elektronisk fakturering er nå klar til bruk.

> [!NOTE]
> Firmaer har vanligvis flere Finance- eller Supply Chain Management-miljøer. Disse miljøene omfatter produksjonsmiljøer, UAT-miljøer (testing av brukeraksept) og utviklingsmiljøer (sandkasse). Du må fullføre fremgangsmåten ovenfor for alle miljøer du vil koble til elektronisk fakturering.
