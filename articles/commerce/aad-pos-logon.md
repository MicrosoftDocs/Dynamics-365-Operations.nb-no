---
title: Konfigurere Azure Active Directory-godkjenning for salgsstedspålogging
description: Denne artikkelen beskriver hvordan du konfigurerer Azure Active Directory som godkjenningsmetoden på Microsoft Dynamics 365 Commerce-salgsstedet.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 47da2c78cef2bbee324fbc2202898fbabd927c4d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853934"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>Konfigurere Azure Active Directory-godkjenning for salgsstedspålogging

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer Azure Active Directory (Azure AD) som godkjenningsmetoden på Microsoft Dynamics 365 Commerce-salgsstedet.

Forhandlere som bruker Dynamics 365 Commerce sammen med andre Microsoft-skytjenester, for eksempel Microsoft Azure, Microsoft 365 og Microsoft Teams, vil vanligvis bruke Azure AD til sentralisert behandling av brukerlegitimasjonen for å få en sikker og sømløs påloggingsopplevelse på tvers av apper. For å bruke Azure AD-godkjenning for Commerce POS, må du først konfigurere Azure AD som godkjenningsmetode i Commerce Headquarters.

## <a name="configure-pos-authentication-method"></a>Konfigurere godkjenningsmetode for salgssted

Følg denne fremgangsmåten for å konfigurere godkjenningsmetode på salgssted i Commerce Headquarters.
    
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonsprofiler**, og velg funksjonalitetsprofil for å endre.
1. Velg et alternativ for ønsket godkjenningsmetode fra rullegardinlisten **Metode for påloggingsgodkjenning** i hurtigkategorien **Funksjoner** i delen **Stabspålogging på salgssted**.

    **Metode for påloggingsgodkjenning** har tre alternativer:
    
    - **Personal-ID og passord** - Dette standardalternativet krever at POS-brukere angir en personal-ID og passord for å logge seg på salgsstedet, og at lederen skal overstyre funksjonene.
    - **Azure AD uten enkel pålogging** – Dette alternativet krever at POS-brukere bruker Azure AD-legitimasjon for å logge seg på salgsstedet og få tilgang til funksjonaliteten for lederoverstyring. Når salgsstedsklienten oppdateres eller åpnes på nytt, må salgsstedsbrukeren angi Azure AD-legitimasjonen for å kunne logge seg på igjen.
    - **Azure AD med enkel pålogging** – Når dette alternativet er valgt, kan POS-brukere logge seg på Cloud POS (CPOS) med aktiv Azure AD-legitimasjon som brukes av andre webprogrammer i den samme webleseren, eller logge seg på Modern POS (MPOS) med Azure AD-legitimasjon som er logget på Windows. Begge metodene tillater pålogging uten at du trenger å angi Azure AD-legitimasjon på påloggingsskjermen for salgssted. Tilgangen til overstyringsfunksjonaliteten i POS-behandling vil imidlertid fortsatt kreve at du logger deg på med Azure AD-legitimasjon.

1. Gå til **Retail og Commerce > IT for Retail og Commerce > Distribusjonsplan**, og kjør jobben **1070 (Kanalkonfigurasjon)** for å synkronisere de nyeste innstillingene for funksjonalitetsprofilen til POS-klienter.

> [!NOTE]
> - Alternativet for godkjenningsmetode **Azure AD uten enkel pålogging** erstatter alternativet **Azure Active Directory** i Commerce-versjon 10.0.18 og tidligere.
> - Azure AD-godkjenning krever en aktiv Internett-tilkobling og vil ikke fungere når salgsstedet er frakoblet.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Knytte Azure AD-kontoer til salgsstedsbrukere

For å bruke Azure AD som godkjenningsmetode for salgssted, må du knytte Azure AD-kontoer til salgsstedsbrukere i Commerce Headquarters. 

Følg denne fremgangsmåten for å knytte kontoer for Azure AD til salgsstedsbrukere i Commerce Headquarters.
    
1. Gå til **Retail og Commerce > Ansatte > Arbeidere**, og åpne en arbeiderpost.
1. I handlingsruten velger du kategorien **Commerce** og deretter under **Ekstern identitet** velger du **Tilknytt eksisterende ID**. 
1. I dialogboksen **Bruk eksisterende eksterne ID** velger du **Søk ved hjelp av e-post**, angir en Azure AD-e-postadresse og velger **Søk**.
1. Velg den returnerte Azure AD-kontoen, og velg deretter **OK**.

Etter konfigurasjonstrinnene over vil feltene **Alias**, **UPN** og **Ekstern underidentifikator** i kategorien **Commerce** på arbeiderens detaljside fylles ut.

Du må kjøre **1060 (Stab)** i **Retail og Commerce > Retail og Commerce IT > Distribusjonsplan** for å synkronisere den siste salgsstedsbrukeren og Azure AD-kontodataene til kanalen.

> [!NOTE]
> Det er en anbefalt fremgangsmåte, etter at arbeiderinformasjon som passord, POS-tillatelse, tilknyttet Azure AD-konto eller adressebok for ansatt er oppdatert i Commerce Headquarters, at du kjører **1060 (stab)** for å synkronisere den nyeste arbeiderinformasjonen til kanalen. Salgsstedsklienten kan deretter hente de riktige dataene for brukergodkjenning og godkjenningskontroller.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>Låsregistrering og -utlogging for salgssted med Azure AD-godkjenning

Følgende skjer når salgsstedet er konfigurert til å bruke Azure AD-godkjenningsmetoden:

- Funksjonen for **Lås kasse** er ikke tilgjengelig i salgsstedsprogrammet. 
- **Automatisk lås**-funksjonen vil fungere som **Automatisk avlogging**-funksjonen.
- Hvis salgsstedsbrukeren velger **Logg av**, blir brukeren bedt om å logge seg på med Azure AD-legitimasjon neste gang salgsstedet starter, uansett om en enkel pålogging er aktivert.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Funksjonalitet for Lederoverstyring med Azure AD-godkjenning

Når salgsstedet er konfigurert til å bruke Azure AD-godkjenning, vil funksjonalitete for lederoverstyring åpne en dialogboks som ber lederbrukeren om Azure AD-legitimasjon. Når lederpålogging er godkjent, blir lederens Azure AD-legitimasjon slettet, og den forrige brukerens Azure AD-legitimasjon blir brukt for påfølgende salgsstedsoperasjoner.

> [!NOTE]
> - I Commerce-versjoner 10.0.18 og tidligere støtter ikke funksjonen for lederoverstyring Azure AD. En personell-ID og -passord kreves selv om salgsstedet er konfigurert til å bruke Azure AD-godkjenningsmetoden.
> - Når du bruker CPOS med Safari-webeseren på en Apple iOS-enhet, må du først slå av **Blokker popup-vinduer** i Safari-innstillinger for at funksjonen for lederoverstyring skal fungerer med Azure AD-godkjenning. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Anbefalte fremgangsmåter for sikkerhet for Azure AD-basert salgsstedsgodkjenning på delte enheter

Mange forhandlere konfigurerer butikkmiljøet på en måte som gjør det nødvendig for flere brukere å få tilgang til salgsstedsprogrammet fra en delt fysisk enhet. I den sammenhengen kan det, selv om enkel pålogging gir en nyttig og sømløs godkjenningsopplevelse, også føre til at det opprettes sikkerhetshull der den gjeldende salgsstedsbrukeren ikke innser at en annen brukers legitimasjon brukes til å utføre transaksjoner eller operasjoner på salgsstedet. Før du konfigurerer salgsstedssystemet for å bruke Azure AD-godkjenningsmetoden anbefales det på det sterkeste at du går gjennom sikkerhetspolicyen og den delte enhetens påloggingsinnstillinger for å avgjøre hvilket alternativ som passer best.

- Hvis detaljhandelsmiljøet bruker en delt konto (for eksempel en lokal konto) for fysisk enhetspålogging, anbefales det å bruke alternativet **Azure AD uten enkel pålogging**. Dette sikrer at hver salgsstedsbruker eksplisitt angir legitimasjon for Azure AD for å logge seg på salgsstedsprogrammet.
- Hvis detaljhandelsmiljøet krever at ansatte bruker sine egne Azure AD-kontoer for å logge seg på salgsstedssystemet og er vert for den fysiske enheten, anbefales det å bruke alternativet **Azure AD med enkel pålogging**.

## <a name="additional-resources"></a>Tilleggsressurser

[ Konfigurere en arbeider](tasks/worker.md)

[Opprette en funksjonalitetsprofil for Retail](retail-functionality-profile.md)


[Definere funksjonalitet for utvidet pålogging MPOS og Cloud POS](extended-logon.md)

[Anbefalte fremgangsmåter for Cloud POS i delte miljøer](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
