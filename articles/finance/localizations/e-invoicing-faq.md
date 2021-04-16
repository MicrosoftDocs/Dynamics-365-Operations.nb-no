---
title: Vanlige spørsmål om Elektronisk fakturering
description: Dette emnet gir informasjon om vanlige spørsmål angående elektronisk fakturering.
author: gionoder
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 41cddcdad5043ec314a94dda67f4f2e9de406cac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840178"
---
# <a name="electronic-invoicing-faq"></a>Vanlige spørsmål om Elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emnet gir svar på vanlige spørsmål om elektronisk fakturering. Elektronisk fakturering utvider de elektroniske faktureringsfunksjonene som finnes i Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Project Operations. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Hva er viktig med elektronisk fakturering, og hvorfor bør det bety noe for organisasjonen min?

Driftskompleksitet og risiko fortsetter å skjerpe etter hvert som organisasjoner vokser globalt og utvider virksomhetens virksomhet på tvers av regioner. Det er svært viktig å opprettholde samsvar og tilpasse seg ofte hvis bestemmelsene endres, og det er spesielt viktig at fakturering skjer. Fakturering har tradisjonelt vært kostbare og utsatt for feil fordi firmaer bruker papirdokumenter og manuelt intensive prosesser.  

Organisasjoner har begynt å flytte seg bort fra papirfakturaer for å redusere kostnader og gjøre det raskere å gå gjennom hele prosessen. Myndighetene snur i økende grad til elektronisk fakturering som en nøkkelkomponent for digitalisering av skatter og avgifter. Ved å kreve at organisasjoner sender skatteinformasjon i sanntid til skattemyndighetene, kan myndighetene redusere skatteunndragelse og -manipulering og redusere avgiftsforpliktelsen. 

Verden går over til papirløs dokumentbehandling, og uten å implementere elektronisk fakturering kan kunder risikere samsvarsproblemer, unødvendige kostnader og ligge bak konkurrentene. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Inneholder ikke Finance, Supply Chain Management og Project Operations allerede funksjonalitet for elektronisk fakturering? Hvilken verdi gir dette meg som kunde? 

Elektronisk fakturering utvider de elektroniske faktureringsfunksjonene som finnes i Finance, Supply Chain Management og Project Operations. Funksjonaliteten forenkler også overholdelse av de nyeste standardene for elektronisk fakturering, og gir helhetlige erfaringer fra forskjellige geografier i elektronisk fakturabehandling og -utveksling. Funksjoner for elektronisk fakturering muliggjør en rekke fordeler, blant annet: 

   - Raskere og enklere tilpasning av land/område-spesifikke krav.
   - Standardisering av implementeringer av e-faktureringsløsning. 
   - Utvidet sporbarhet for e-fakturabehandling.  
   - Enklere vedlikehold slik at det samsvarer med endrede juridiske krav og lokale forretningspraksis. 
   - Forenklet løsningsemballasje.
   - Skaleringsfunksjoner for et stort antall sendte dokumenter som gir raskere omløpsoperasjon.
   - Mulighet til å dele løsningene dine med andre firmaer.

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Støtter elektronisk fakturering lokale installasjoner av Finance, Supply Chain Management og Project Operations? 

Den gjeldende plattformen tillater ikke bruk av den lokale versjonen, og det er ingen planer om å støtte den i fremtiden.

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>Kan elektronisk fakturering brukes sammen med funksjonen for automatisk leverandørimport?

Nei. Det finnes planer for dette grensesnittet, men det er ingen planlagt tidslinje. Når det er planlagt, vil datoene bli belyst i [Frigivelsesplaner](https://docs.microsoft.com/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Hvordan håndterer elektronisk fakturering filvedlegg i den elektroniske fakturaen? Er det nødvendig å ha en SharePoint-server ved innebygging av PDF-filer i XML-filen?

Filene som er knyttet til den elektroniske fakturaen, håndteres som innebygde binærdata i et XML-element. Det er ikke nødvendig med en SharePoint-server for å bygge inn PDF-filer, men vedlegget må lagres i dokumentbehandlingssystemet Finance, Supply Chain Management og Project Operations.

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>Er elektronisk fakturering tilgjengelig i henhold til bestemmelsene i landet/regionen min?

Elektronisk fakturering er en mikroserviceplattform som vil være globalt tilgjengelig.

Microsoft planlegger å publisere de elektroniske fakturaformatene og integreringene for landene som er funksjonelt lokalisert av Microsoft. Hvis du vil ha mer informasjon, kan du se [Tilgjengelighet av funksjoner for elektronisk fakturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Hvis det elektroniske faktureringsformatet for landet/området ditt ikke er oppført, har plattformen som mål å støtte dette scenariet i fremtiden. Du kan fremdeles dra nytte av konfigurasjonsfunksjonene elektronisk fakturering har, og konfigurere det elektroniske faktureringsformatet selv, eller du kan arbeide med en partner/ISV for å konfigurere dem for organisasjonen.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Er Dynamics 365 for Regulatory Services en ny modul, som Human Resources eller Project Operations, som er knyttet til Finance or Supply Chain Management? Er det ekstra kostnader for dette?

Dynamics 365 for Regulatory Services (RCS) er en skytjeneste for konfigurering av globaliseringsressurser. RCS er gratis for alle som har lisens for Finance, Supply Chain Management og Project Operations.

For RCS-registrering kan du gå til <https://marketing.configure.global.dynamics.com/>.

Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>Må jeg registrere meg for å få elektronisk fakturering, eller kan jeg bare aktivere det i Funksjonsstyring?

Hvis du har lisens for Finance, Supply Chain Management og Project Operations, kan du se [Komme i gang med tjenesteadministrasjon for tillegget for elektronisk fakturering](e-invoicing-get-started-service-administration.md) for å registrere deg for elektronisk fakturering.

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Fungerer elektronisk fakturering med virtuelle maskiner på nivå 1? Hva er det minste nødvendige miljøet?

Integrering med elektronisk fakturering krever at minst en virtuell maskin på nivå 2 er vert for Finance eller Supply Chain Management. Hvis du vil ha mer informasjon om miljøplanlegging, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>Har elektronisk fakturering en testmodus for testing av fakturainnsending?

Dette kan oppnås ved hjelp av konfigurasjon. Hvis du vil teste fakturainnsending, kan du koble til Finance eller Supply Chain Management fra et UAT-miljø (brukergodkjenningstest) og sende testfakturaene. Elektronisk fakturering støtter konfigurering av digitale testsertifikater, og når det gjelder e-fakturaer som krever digital godkjenning, støtter oppsett av en URL-adresse fra testwebtjenester som er publisert av skattemyndighetene.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Finnes det dokumentasjon om medfølgende landspesifikke funksjoner for elektronisk fakturering?

Ja. Hvis du vil ha informasjon om tilgjengeligheten av funksjoner for elektronisk fakturering og formatene de støtter, kan du se [Tilgjengelighet av funksjoner for elektronisk fakturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Hvis du ikke fant svaret du er på jakt etter, kan du sende spørsmålet til produktutviklingsgruppen på <D365EInvoicePreview@microsoft.com>. Vi vil enten kontakte deg eller forbedre dekningen av disse vanlige spørsmålene.
