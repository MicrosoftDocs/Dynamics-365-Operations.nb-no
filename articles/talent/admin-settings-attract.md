---
title: Administratorinnstillinger i Attract
description: Dette emnet forklarer hvordan du aktiverer funksjonalitet for organisasjoner og brukere i Attract.
author: 
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 52b48d5daab985c43d59f29ad7b80dda99a7fcef
ms.contentlocale: nb-no
ms.lasthandoff: 10/22/2018

---

# <a name="admin-settings-in-attract"></a>Administratorinnstillinger i Attract
[!include[banner](../includes/banner.md)]

Administrasjonssenteret i Microsoft Dynamics 365 for Talent: Attract inneholder konfigurasjonsinnstillinger, integrasjonsalternativer og oppsettalternativer for Attract-programmet.

## <a name="company-information"></a>Firmainformasjon

Angi et visningsnavn for firmaet, og legg til en firmalogo. Visningsnavnet og logoen kan deretter brukes på jobbutlysinger og under jobbintroduksjonen.

## <a name="linkedin-integration"></a>LinkedIn-integrering

Konfigurer integrasjonen med tilkobling til rekrutteringssystemet for LinkedIn (RSC). Når du kobler til LinkedIn med påloggingsinformasjonen for LinkedIn, kan du synkronisere en kandidats LinkedIn-profil, søknader, intervjutilbakemelding og merknader fra ansettelsesteam. Det kreves en full LinkedIn-rekrutterer-lisens. Hvis du vil ha mer informasjon om RSC, se [Tilkobling til rekrutterersystem (RSC) – vanlige spørsmål](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Brukerrettigheter

Tilordne roller til brukere i organisasjonen. Følgende roller er tilgjengelige: **Administrator**, **Rekrutterer**, **Ansettelsesansvarlig** og **Skrivebeskyttet**. Hvis du vil ha mer informasjon om brukertillatelser, kan du se [Administrasjon av sikkerhet og rolle i Attract](./security-attract.md).

## <a name="feature-management"></a>Funksjonsbehandling

Når du legger til nye funksjoner, kan de utgis i en offentlig forhåndsvisning. Funksjoner for offentlig forhåndsvisning oppfyller ikke alle kravene for tjenesten. Ved å motta dem godtar du å dele data med eksterne systemer. Det kan være at organisasjonen ikke krever alle de nye funksjonene som gis ut. Du kan slå offentlige forhåndsvisningsfunksjoner av og på, avhengig av behovene i organisasjonen.

## <a name="template-management"></a>Malbehandling

En prosessmal inneholder alle aktivitetene som skal tas med som en del av ansettelsesprosessen for en jobb. Organisasjonen kan enten tillate alle teammedlemmer eller bare administratorer å opprette maler for ansettelsesprosessen. Hvis du vil tillate at teammedlemmer oppretter sine egne maler for ansettelsesprosessen, må du aktivere malbehandlingsfunksjonen. Hvis du vil ha mer informasjon om prosessmaler, se [Prosessmaler i Attract](./process-templates-attract.md).

## <a name="email-template-settings"></a>Innstillinger for e-postmal

Organisasjoner kan opprette e-postmaler for ulike scenarier. Du kan velge topptekstbildet som skal tas med i e-postmaler. Den valgte overskriften vises deretter i alle e-postmaler. I bunnteksten i malen kan du legge til en kobling til organisasjonens personvernerklæring og vilkårene for bruk for kommunikasjon. Hvis du vil ha mer informasjon, kan du se [E-postmaler i Attract](./email-templates.md).

## <a name="offer-process"></a>Tilbudsprosess

Du kan konfigurere godkjenningsprosessen for jobbtilbud. Du kan for eksempel angi om et tilbud må være godkjent før det sendes til en kandidat. Du kan også kreve at godkjennere må legge til en kommentar sammen med tilbudsbeslutningen.

Det finnes to godkjenningsarbeidsflyter: **Parallell** og **Sekvensiell**.

- **Parallell** – godkjenninger sendes til alle godkjennerne samtidig.
- **Sekvensiell** – godkjenninger sendes til godkjennere i en bestemt rekkefølge.

Du kan også konfigurere alternativer som er knyttet til kandidatopplevelsen. Med ett alternativ du f.eks. angi om kandidater kan avvise et tilbud uten ekstra diskusjon. Hvis du setter alternativet **Tillat at kandidater kan avslå et tilbud uten ekstra diskusjon** til **Nei**, er **Avslå tilbud**-knappen tilgjengelig for kandidater. Hvis du setter dette alternativet til **Ja**, kan kandidater avvise tilbudet ved å velge en årsak og deretter velge **Avslå tilbud**.

Du kan også definere og håndheve en utløpsdato for tilbudene. Hvis du setter alternativet **Krev en utløpsdato for alle tilbud** til **Ja**, utløper tilbud etter hvor mange timer eller dager du angir.

Hvis du vil ha mer informasjon om tilbudsbehandling, kan du se [Konfigurere tilbudsbehandling](./offer-setup.md).
