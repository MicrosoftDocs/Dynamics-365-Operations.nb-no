---
title: Legge til en side med personvernpolicy
description: Dette emnet beskriver hvordan du legger til en side med personvernpolicy på området ditt i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce6491d176f90717877f084b11546010084c5f3b
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761279"
---
# <a name="add-a-privacy-policy-page"></a>Legge til en side med personvernpolicy


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en side med personvernpolicy på området ditt i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Overholdelse av personvern inkluderer organisatoriske tiltak som informerer brukerne om hvordan deres data samles inn og håndteres. Brukere kan deretter bestemme hvordan de vil at deres personlige data skal håndteres og kan iverksette nødvendige tiltak.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Se gjennom Microsofts personvernerklæring i Dynamics 365 Commerce

Hvis du vil se gjennom Microsofts personvernerklæring mens du er logget på redigeringsverktøyene i Dynamics 365 Commerce, velger du **Hjelp**-knappen (**?**) i øvre høyre hjørne, og deretter velger du **Personvern og informasjonskapsler**. En ny fane åpnes med en kobling til [Microsofts personvernerklæring](https://privacy.microsoft.com/privacystatement).

## <a name="build-a-privacy-policy-page-for-your-site"></a>Bygge en personvernspolicy-side for nettstedet ditt

I Dynamics 365 Commerce er det flere måter å gi brukerne av nettstedet ditt tilgang til personvernpolicyen. Denne delen viser hvordan du bygger en personvernspolicy-side og deretter refererer til siden ved hjelp av et bunntekstfragment.

Veiledningen nedenfor er et eksempel som viser hvordan du bygger en generell personvernpolicy-side for et handelsområde. Du er ansvarlig for å utforme og implementere en personvernpolicy-sideløsning som best dekker firmaets juridiske krav.

Hvis du vil starte, går du til webområdet du vil bygge en personvernspolicy-side for, i redigeringsverktøyene.

### <a name="create-a-template"></a>Opprett en mal

> [!NOTE]
> Hvis en mal som kan brukes til siden for personvernpolicy, allerede er opprettet, går du videre til delen [Bygge en personvern-side](#build-a-privacy-policy-page).

Hvis du vil opprette en mal, følger du trinnene nedenfor.

1. Gå til **Maler**, og velg deretter **Ny** for å opprette en sidemal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **Kampanjebannermal**, og velger deretter **OK**.
1. I malen legger du til eventuelle nødvendige moduler i de nødvendige sidesporene. Hvis du vil ha veiledning, holder du pekeren over de røde utropstegnene. (**HTML-hode**-sporet kan for eksempel kreve en **Standard eksternt skript**-modul.)
1. Legg til en **Standardside**-modul i **Meldingstekst**-sporet.
1. I **Standardside**-modulen i **Hoved**-sporet legger du til en **innholdsrik blokk**-modul.
1. I **Innholdsrik blokk**-modulen kan du legge til en **innholdsrik blokkelement**-modul.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

### <a name="build-a-privacy-policy-page"></a>Bygge en side med personvernpolicy

Følg denne fremgangsmåten for å bygge en personvernspolicy-side.

1. Gå til **Sider**, og velg deretter **Ny** for å opprette en side.
1. I dialogboksen **Velg en mal** velger du malen for siden for personvernpolicy.
1. Angi et sidenavn og en side-URL, og velg deretter **OK**. 
1. I **Hoved**-sporet på den nye siden legger du til en **innholdsrik blokk**-modul.
1. I **Innholdsrik blokk**-modulen kan du legge til en **innholdsrik blokkelement**-modul.
1. Velg **Legg til datakilde** i egenskapsruten for **Innholdsrik blokk**-modulen, og velg deretter **Rikt tekstinnhold**.
1. I redigeringsprogrammet for rik tekst skriver du inn innholdet for siden for personvernpolicy. Utvid redigeringsprogrammet for rik tekst til fullskjermmodus etter behov.
1. Når du er ferdig med å skrive inn innhold, velger du **Forhåndsvisning** for å forhåndsvise siden i nettleseren.
1. Fyll ut eventuelle gjenværende tillegg til side- og modulegenskapene.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

Følg disse trinnene for å publisere URL-en for personvernpolicy-siden.

1. Gå til **URL-adresser**, og velg URL-adressen for personvernpolicy-siden.
1. Velg **Publiser** for å publisere den valgte URL-adressen.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Opprette en kobling til siden for personvernpolicy i en bunntekst

Du kan legge til en kobling til siden for personvernpolicy i et fragment. På denne måten kan du dele koblingen og oppdatere den på tvers av flere sider på området ved å referere til fragmentet. Dette eksemplet viser hvordan du legger til en kobling til siden for personvernpolicy i et bunntekstfragment.

Hvis du vil legge til en kobling til et bunntekstfragment, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg **Ny** for å opprette et sidefragment.
1. I dialogboksen **Nytt fragment** velger du **Bunntekst**-modulen.
1. Under **Navn på fragment** angir du et navn på fragmentet, og deretter velger du **OK**.
1. Legg til en **Bunntekstelement**-modul i **Bunntekstkategori**-sporet.
1. Velg **Koble til tekst** i egenskapsruten til høyre.
1. I dialogboksen **Koble til tekst** skriver du inn koblingsteksten og koblingsmålet på siden for personvernpolicy, og deretter klikker du **OK**.
1. For å få nettadressen til personvernpolicy-siden går du til **Sider**, personvernpolicy-siden, og kopierer URL-adressen fra egenskaper-ruten.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.
1. Forhåndsvis fragmentet, og test koblingen til siden for personvernpolicy.

Fragmentet kan nå refereres i malen for andre områdesider. Når det refereres til dette fragmentet i **Bunntekst**-modulen for en mal, vises koblingsreferansen på alle sider som er bygget ved hjelp av denne malen.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over samsvar](compliance-overview.md)

[Funksjoner og egenskaper for tilgjengelighet](accessibility.md)

[Informasjonskapselsamsvar](cookie-compliance.md)

[Erstatte bruker-IDer knyttet til sporede innholdsendringer](replace-IDs-tracked-changes.md)
