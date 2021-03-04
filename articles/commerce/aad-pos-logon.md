---
title: Aktivere Azure Active Directory-godkjenning for POS-pålogging
description: Dette emnet forklarer hvordan du konfigurerer påloggingsopplevelsen for Microsoft Dynamics 365 Commerce salgssted (POS) slik at den bruker Azure Active Directory-godkjenning.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 6946cb5f8bc8aa451f72d1eebcd324f408ad5f7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414566"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Aktivere Azure Active Directory-godkjenning for POS-pålogging
[!include [banner](includes/banner.md)]


Mange kunder som bruker Microsoft Dynamics 365 Commerce, bruker også andre Microsoft Cloud-tjenester, og de kan bruke Azure Active Directory (Azure AD) til å administrere brukerlegitimasjon for disse tjenestene. I slike tilfeller vil kundene kanskje bruke samme Azure AD-konto på tvers av programmer. Dette emnet forklarer hvordan du konfigurerer påloggingsopplevelsen for Commerce salgssted (POS) slik at den bruker Azure AD-godkjenning.

## <a name="configure-azure-ad-authentication"></a>Konfigurere Azure AD-godkjenning

Hvis du vil gjøre Azure AD tilgjengelig som godkjenningsmetode for POS-pålogging for en butikk, må du konfigurere innstillingene for butikkens funksjonalitetsprofil og deretter bruke denne innstillingen på POS-klienter.

Hvis du vil konfigurere en funksjonalitetsprofil, gjør du følgende.

1. Gå til **Retail og Commerce** \> **Kanaloppsett** \> **Salgsstedsoppsett** \> **Salgsstedsprofiler** \> **Funksjonalitetsprofiler**.
1. Velg funksjonalitetsprofilen du vil endre.
1. I hurtigfanen **Funksjoner**, i delen **Stabspålogging på salgssted**, endrer du verdien i feltet **Metode for påloggingsgodkjenning** fra **ID og passord for personale** til **Azure Active Directory**.

Alle funksjonalitetsprofiler bruker som standard **ID og passord for personale** som godkjenningsmetode for POS. Derfor må du endre verdien i feltet **Metode for påloggingsgodkjenning** hvis du vil bruke Azure AD. Hver detaljhandelsbutikk som er koblet til den valgte funksjonalitetsprofilen, påvirkes av denne endringen.

Følg denne fremgangsmåten for å bruke innstillingene på salgsstedsklienter.

1. Gå til **Retail og Commerce** \> **IT for Retail og Commerce** \> **Distribusjonsplan**.
1. Kjør distribusjonsplanen **1070** (**Kanalkonfigurasjon**).

> [!NOTE]
> Azure AD-godkjenning krever en Internett-tilkobling. Den vil ikke fungere når salgssted er i frakoblet modus.
> 
> For øyeblikket støtter ikke **Lederoverstyring**-funksjonen Azure AD som godkjenningsmetode. Det kreves en operatør-ID og et passord selv om Azure AD er konfigurert som godkjenningsmetode for salgsstedspålogging.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Knytt en Azure AD-konto til en arbeider

Før en butikkarbeider kan bruke en Azure AD-konto til å logge seg på POS-programmet, må Azure AD-kontoen knyttes til denne arbeideren.

Følg denne fremgangsmåten for å knytte en Azure AD-konto til en arbeider.

1. Gå til **Detaljhandel og handel** \> **Ansatte** \> **Arbeidere**.
1. Åpne detaljersiden for en arbeider.
1. I handlingsruten, i kategorien **Commerce** i gruppen **Ekstern identitet** velger du **Tilknytt eksisterende identitet**.
1. I dialogboksen **Bruk eksisterende eksterne ID** velger du **Søk ved hjelp av e-post**, angir en Azure AD-e-postadresse og velger **Søk**.
1. Velg den returnerte Azure AD-kontoen, og velg deretter **OK**.

Feltene **Alias**, **UPN** og **Ekstern underidentifikator** i kategorien **Commerce** på arbeiderens detaljside fylles ut.

> [!NOTE]
> Når en arbeiderpost er oppdatert, for eksempel hvis en ny Azure AD-konto er tilknyttet, endres et passord eller hvis en adressebok for ansatte blir oppdatert, anbefales det at du kjører **1060** (**Personale**) distribusjonsplan for å synkronisere den nyeste ansattinformasjonen til kanalen. På denne måten kan POS-appen hente de riktige dataene for brukergodkjenning og godkjenningskontroll.

## <a name="additional-resources"></a>Tilleggsressurser

[Definere funksjonalitet for utvidet pålogging MPOS og Cloud POS](extended-logon.md)

[Opprette en funksjonalitetsprofil for Retail](retail-functionality-profile.md)

[ Konfigurere en arbeider](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)


[!INCLUDE[footer-include](../includes/footer-banner.md)]