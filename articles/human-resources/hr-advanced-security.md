---
title: Begrens tilgang til arbeidere etter juridisk enhet
description: Denne artikkelen beskriver hvordan du konfigurerer arbeidstilgang etter juridisk enhet.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780395"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Begrens tilgang til arbeidere etter juridisk enhet

Denne artikkelen beskriver hvordan du konfigurerer arbeidstilgang etter juridisk enhet.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ansatte er ansatt i juridiske enheter. Her er noen eksempler:

- Aaron Con er ansatt i den juridiske enheten USSI.
- Ahmed Barnett er ansatt i den juridiske enheten USMF.
- Alicia Thornber er ansatt i de juridiske enhetene GLSI og USMF.

Avhengig av en brukers rolle i firmaet, kan det være at de trenger tilgang for å vise alle ansatte på tvers av alle juridiske enheter. Det kan også hende at en bruker må begrenses, slik at han eller hun bare kan vise ansatte i den juridiske enheten som de har tilgang til. Hvis du vil bestemme hvilke ansatte en bruker kan vise, velger du parameteren **Begrens tilgang til arbeiderinformasjon** på siden **Delte parametere for Human Resources**.

En bruker har for eksempel tilgang til **Arbeider**-siden og har bare tilgang til den juridiske enheten USMF. I dette tilfellet kan brukeren vise følgende informasjon for de ansatte i den forrige listen:

- Hvis funksjonen for å begrense tilgang til arbeiderinformasjon ikke er aktivert, kan brukeren vise informasjon for Aaron, Ahmed og Alicia.
- Hvis funksjonen er aktivert, kan brukeren bare vise informasjon for Alicia og Ahmed, fordi de også er ansatt i den juridiske enheten USMF.

Informasjonen som vises, varierer avhengig av programmet du bruker.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources frittstående

Hvis funksjonen for å begrense tilgang til arbeiderinformasjon er aktivert, vil den begrensede brukeren se en tom verdi i enkelte lister som inneholder arbeiderens navn.

En bruker som for eksempel bare har tilgang til den juridiske enheten USMF, vil oppleve følgende atferd:

- I **Aktive stillinger**-listen er **Arbeider**-kolonnen tom for Aaron sin stilling, fordi brukeren ikke har tilgang til ansatte i den juridiske enheten USSI.
- Hvis brukeren driller ned på arbeiderens navn, vises en tom **Arbeider**-side.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources om Finance-infrastruktur

Hvis funksjonen for å begrense tilgang til arbeiderinformasjon er aktivert, vil den begrensede brukeren se arbeiderens navn i noen lister.

En bruker som for eksempel bare har tilgang til den juridiske enheten USMF, vil oppleve følgende atferd:

- I listen **Aktive stillinger** vil **Arbeider**-kolonnen vise Aaron sitt navn. Hvis brukeren beveger pekeren over arbeiderens navn, vises bare navnet og tittelen.
- Hvis brukeren driller ned på arbeiderens navn, vises en tom **Arbeider**-side.

> [!TIP]
> Hvis du bruker Dynamics 365 Human Resources på Finance-infrastruktur, og vil at begrensede brukere skal se tomme verdier for arbeidernavn, kan du legge til **Begrens tilgang til arbeidere**-sikkerhetsrettigheter til brukerrollene på siden **Sikkerhetskonfigurasjon**.

Når du aktiverer funksjonen, må du utføre noen ekstratrinn for å angi tillatelsene for hver bruker du vil begrense visningen for.

1. Velg en bruker på **Brukere**-siden.
2. Velg en rolle for brukeren. Alternativet **Tilordne organisasjoner** blir tilgjengelig.
3. Velg **Tilordne organisasjoner**.
4. På den nye siden velger du **Gi tilgang til bestemte organisasjoner individuelt**, og deretter velger du organisasjonene brukeren skal ha tilgang til.
5. Gjenta trinn 2 til og med 4 for alle andre roller som brukeren har, inkludert systembrukerrollen.

> [!NOTE]
> De juridiske enheten som en bruker har tilgang til, må samsvare på tvers av alle brukerens roller.
