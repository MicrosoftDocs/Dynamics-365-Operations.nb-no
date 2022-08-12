---
title: Signere MPOS .appx-filen med en kodesigneringssertifikat
description: Denne artikkelen forklarer hvordan du signerer MPOS med et kodesigneringssertifikat.
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 4cbdfcb5229be2f04531031c80f41f672b2a4747
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169106"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>Signere MPOS .appx-filen med en kodesigneringssertifikat

[!include [banner](../includes/banner.md)]

Hvis du vil installere Modern POS (MPOS), må du signere MPOS-appen med et kodesigneringssertifikat fra en klarert leverandør og installere samme sertifikat på alle maskinene der MPOS er installert, under den klarerte rotmappen for den gjeldende brukeren.

Hvis du vil signere MPOS-appen med et sertifikat, bruker du et av disse alternativene i filen **Retail SDK\\Build tool\\Customization.settings**:

- Legg til den sikre filoppgavedelen i Azure DevOps-byggtrinn, og last opp sertifikatet for å sikre filoppgaven. Bruk variabelen for utdatabane for oppgave for sikker fil som en parameter i filen Customization.settings.

    > [!NOTE]
    > Oppgaven for sikker fil støtter ikke et passordbeskyttet sertifikat. Du må fjerne passordet før du laster opp denne oppgaven. Siden sertifikatet lastes opp til den sikre filsystemoppgaven i Azure, kan du bare fjerne passordet for dette trinnet. Du bør imidlertid diskutere fjerningen av passordet med sikkerhetsekspertene for å finne ut om dette er riktig å gjøre for prosjektet. Ikke fjern sertifikatpassordet for andre scenarioer.
- Bruk et sertifikat som er i filsystemet. Du gjør dette ved å laste ned eller generere et sertifikat og legge det i filsystemet der bygget kjører. Den Microsoft-driftede agenten eller byggbrukeren må ha tilgang til denne banen og filen.
- Bruk avtrykket til å slå opp i sertifikatet i butikken, og logg deg på med dette sertifikatet.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Bruke en oppgave for sikker fil ved signering av Universal Windows Platform-app

> [!NOTE]
> Du kan også bruke Azure Key Vault til å lagre sertifikatet og bruke Azure-signeringsverktøyet til å signere APPX-filen for Modern POS og de selvbetjente installasjonsprogrammene. Når det gjelder eksempelskript for datasamlebånd og mer informasjon, kan du se [Konfigurere en kompileringskontroll i Azure DevOps for å generere selvbetjeningspakker for Retail](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Vi anbefaler bruk av en oppgave for sikker fil ved signering av UWP-apper (Universal Windows Platform). Hvis du vil ha mer informasjon om pakkesignering, kan du se [Konfigurere pakkesignering](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Denne prosessen vises på følgende bilde.

![Flyt for signering av MPOS-app.](media/POSSigningFlow.png)

> [!NOTE]
> OOB-pakking støtter for øyeblikket bare signering av APPX-filen, mens de ulike selvbetjente installasjonsprogrammene som MPOIS, RSSU og HWS signeres ikke av denne prosessen. Du må signere den manuelt ved hjelp av SignTool eller andre signeringsverktøy. Sertifikatet som brukes ved signering av APPX-filen, må være installert på maskinen der Modern POS er installert.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Fremgangsmåte for å konfigurere sertifikatet for signering i Azure Pipelines

### <a name="certificate-in-the-file-systemsecure-location"></a>Sertifikat i filsystemet / sikker plassering

Last ned [DownloadFile-oppgaven](/visualstudio/msbuild/downloadfile-task), og legg den til som første trinn i byggprosessen. Fordelen ved å bruke oppgaven for sikker fil er at filen krypteres og legges på disken under bygging uansett om kompileringskontrollen blir vellykket, mislykket eller avbrutt. Filen slettes fra nedlastingsstedet etter at byggprosessen er fullført.

1. Last ned og legg til oppgaven for sikker fil som første trinn i Azure-kompileringskontrollen. Du kan laste ned oppgaven for sikker fil fra [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
1. Last opp sertifikatet til oppgaven for sikker fil, og angi referansenavn under Utdatavariabler, som vist på bildet nedenfor.
    > [!div class="mx-imgBorder"]
    > ![Oppgave for sikker fil.](media/SecureFile.png)
1. Opprett en ny variabel i Azure Pipelines ved å velge **Ny variabel** i **Variabler**-fanen.
1. Gi variabelen et navn i verdifeltet, for eksempel **MySigningCert**.
1. Lagre variabelen.
1. Åpne filen **Customization.settings** fra **RetailSDK\\BuildTools**, og oppdater **ModernPOSPackageCertificateKeyFile** med variabelnavnet du opprettet i datasamlebåndet (trinn 3). For eksempel:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Dette trinnet kreves hvis sertifikatet ikke er passordbeskyttet. Hvis sertifikatet er passordbeskyttet, fortsetter du med følgende trinn.
    
1. Hvis du vil tidsstemple MPOS .appx-filen ved signering av den med et sertifikat, kan du åpne filen **Retail SDK\\Build tool\\Customization.settings** og oppdatere variabelen **ModernPOSPackageCertificateTimestamp** med tidsstempelleverandøren (for eksempel `http://timestamp.digicert.com`).
1. Legg til en ny secure-text-variabel i **Variabler**-fanen for datasamlebåndet. Bruk **MySigningCert.secret** som navn, angi verdien til passordet for sertifikatet. Velg låseikonet for å sikre variabelen.
1. Legg til oppgaven **PowerShell-skript** i datasamlebåndet (etter Last ned sikker fil og før byggtrinnet). Angi **Visning**-navnet og angi **Innebygd** som type. Kopier og lim inn følgende i skriptdelen.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. Åpne filen **Customization.settings** fra **RetailSDK\\BuildTools**, og oppdater **ModernPOSPackageCertificateThumbprint** med verdien til sertifikatavtrykket.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Hvis du vil ha mer informasjon om hvordan du får avtrykket for et sertifikat, kan du se [hente avtrykket for et sertifikat](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Laste ned eller generere et sertifikat for å signere MPOS-appen manuelt ved hjelp av msbuild i SDK

Hvis et nedlastet eller generert sertifikat brukes til å signere MPOS-appen, oppdaterer du noden **ModernPOSPackageCertificateKeyFile** i filen **BuildTools\\Customization.settings** slik at den peker mot plasseringen til PFX-filen (**$(SdkReferencesPath)\\appxsignkey.pfx**). For eksempel:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

I dette tilfellet er navnet på sertifikatfilen **appxsignkey.pfx**, som ligger i mappen **Retail SDK\\Reference**.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Bruke avtrykk til å signere MPOS-appen

Hvis du bruker avtrykk til å signere MPOS-appen, installerer du sertifikatet lokalt. Oppdater avtrykksverdien i noden **ModernPOSPackageCertificateThumbprint** i filen **BuildTools\\Customization.settings**.

Dette alternativet fungerer hvis byggbrukeren er en lokal bruker. Hvis du imidlertid bruker Azure DevOps-agentene til å generere bygget, kan det hende at agenten ikke har tilgangstillatelse til sertifikatlageret for å bruke sertifikatet til signering, eller byggmaskinen har ikke sertifikatet installert. I dette tilfellet er løsningen å endre byggbrukeren til lokal bruker og installere sertifikatet på datamaskinen. Dette alternativet fungerer imidlertid ikke hvis du ikke har administratortilgang til datamaskinen.

> [!NOTE]
> Hvis PFX-filen eller alternativet for oppgaven for sikker fil brukes til å signere appen, lar du noden **ModernPOSPackageCertificateThumbprint** i **Customization.settings** være tom. Hvis avtrykksalternativet brukes, lar du **ModernPOSPackageCertificateKeyFile** være tom. Hvis begge verdiene oppdateres, mislykkes bygget.

### <a name="certification-renewal"></a>Sertifiseringsfornyelse

### <a name="renew-a-certificate-from-trusted-ca"></a>Fornye et sertifikat fra klarert sertifiseringsinstans

Kontakt sertifiseringsinstansen vedrørende fornyelse av sertifikatet. Når det gjelder et klarert sertifikat, er det ingenting som må gjøres på MPOS-siden.

### <a name="renew-a-self-signed-certificate"></a>Fornye et egensignert sertifikat

Ikke bruk eksempelsertifikatet som er tilgjengelig i Retail SDK, til produksjon. Den kan brukes bare til utviklingsformål. Contoso-eksempelsertifikatet kan ikke fornyes, og eksempelsertifikatet som er inkludert i Retail SDK versjon 10.0.16 eller tidligere, utløper 31. desember 2020. Hvis dette sertifikatet eller et egensignert sertifikat har blitt brukt til å signere et tilpasset Modern POS, er det stor sannsynlighet for at Modern POS ikke kommer til å fungere riktig etter denne datoen.
 
### <a name="impact"></a>Konsekvens
 
Hvis det ovenstående stemmer i ditt tilfelle, blir problemet at installasjonsprogrammet ikke kan kjøre etter 31. desember 2020. Det kan hende at Modern POS ikke fungerer, avhengig av IT-policyene som brukes av bedriften. Det er helt avgjørende at du tester dette ved å endre datoen midlertidig til en fremtidig dato, slik at du kan fastslå innvirkningen på organisasjonen din.
 
### <a name="steps-to-determine-the-issue"></a>Fremgangsmåte for å finne om det er problemer
 
1.  Bruk Windows-innstillinger til å endre datamaskinklokken til en dato og et klokkeslett i år 2021.
2.  Kontroller at Modern POS kan åpnes, at du kan logge deg på, og at en transaksjon kan fullføres.
3.  Kontroller at det selvbetjente installasjonsprogrammet for Modern POS kan kjøre, og at installasjonen i så fall fullføres.
4.  Gå tilbake til innstillingene for Windows-klokke for å rette datoen og klokkeslettet.
 
Hvis du kan fullføre alle disse trinnene uten problemer, kan du bruke gjeldende sertifikat etter 31. desember 2020.  
 
### <a name="steps-going-forward"></a>De neste trinnene 

Vi anbefaler på det sterkeste at du fornyer det tidligere brukte sertifikatet. Vi anbefaler på det sterkeste at du skaffer et nytt sertifikat. Du gjør dette ved å utføre ett av følgende:
 
- **Foretrekkes** – Skaff et kodesigneringssertifikat fra en klarert sertifiseringsinstans.

- **Foretrekkes ikke** – Generer et egensignert kodesigneringssertifikat du vil bruke. Dette brukes vanligvis bare til utviklingsformål innenfor et domene og anbefales ikke til produksjon. 

- **Tilgjengelig som en midlertidig løsning** – Bruk det fornyede Contoso-kodesigneringssertifikatet. Dette brukes vanligvis til testing, så det anbefales ikke at du bruker det i produksjon.
 
Generer deretter en ny, tilpasset Modern POS-pakke som er signert ved hjelp av dette sertifikatet som er skaffet via en av handlingene ovenfor. Du må følge et av de følgende trinnene, avhengig av sertifikatet:
 
- Hvis du bruker et nytt, klarert sertifikat (eller et nytt, egensignert sertifikat), må du installere et nytt sertifikat på hver enhet. Etter dette må du ta den nyopprettede Modern POS-pakken (installasjonsprogram), avinstallere det eksisterende programmet og deretter installere den nye Modern POS-pakken på nytt. Du må foreta en enhetsaktivering av Modern POS på hver enhet.

- Hvis du bruker det fornyede Contoso-sertifikatet, må du installere det nye sertifikatet på hver enhet og installere Modern POS-pakken (installeringsprogrammet). Du trenger ikke å avinstallere, men du må installere på nytt på enheten. Merk at enhetsaktivering av Modern POS ikke er nødvendig. Dette alternativet er en midlertidig løsning. Bare bruk dette alternativet for å unngå ny aktivering og løse problemet før du skaffer et nytt, klarert sertifikat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
