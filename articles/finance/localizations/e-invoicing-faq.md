---
title: Vanlige spørsmål om Elektronisk fakturering
description: Denne artikkelen gir informasjon om vanlige spørsmål angående elektronisk fakturering.
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fbb43438a9da567460eb744afb64dae5274f04a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904361"
---
# <a name="electronic-invoicing-faq"></a>Vanlige spørsmål om elektronisk fakturering

[!include [banner](../includes/banner.md)]

Denne artikkelen gir svar på vanlige spørsmål om tjenesten for elektronisk fakturering. Elektronisk fakturering utvider de elektroniske faktureringsfunksjonene som finnes i Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Project Operations. 

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

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Støtter tjenesten for elektronisk fakturering lokale installasjoner av Finance, Supply Chain Management og Project Operations? 

Den gjeldende plattformen tillater ikke bruk av den lokale versjonen, og det er ingen planer om å støtte den i fremtiden.

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>Kan tjenesten for elektronisk fakturering brukes sammen med funksjonen for automatisk leverandørimport?

Nei. Det finnes planer for dette grensesnittet, men det er ingen planlagt tidslinje. Når det er planlagt, vil datoene bli belyst i [Frigivelsesplaner](/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Hvordan håndterer tjenesten for elektronisk fakturering filvedlegg i den elektroniske fakturaen? Er det nødvendig å ha en SharePoint-server ved innebygging av PDF-filer i XML-filen?

Filene som er knyttet til den elektroniske fakturaen, håndteres som innebygde binærdata i et XML-element. Det er ikke nødvendig med en SharePoint-server for å bygge inn PDF-filer, men vedlegget må lagres i dokumentbehandlingssystemet Finance, Supply Chain Management og Project Operations.

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>Er tjenesten for elektronisk fakturering tilgjengelig i henhold til bestemmelsene i landet/regionen min?

Tjenesten for elektronisk fakturering er en mikroserviceplattform som vil være globalt tilgjengelig.

Microsoft planlegger å publisere de elektroniske fakturaformatene og integreringene for landene som er funksjonelt lokalisert av Microsoft. Hvis du vil ha mer informasjon, kan du se [Tilgjengelighet av funksjoner for elektronisk fakturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Hvis det elektroniske faktureringsformatet for landet/området ditt ikke er oppført, har plattformen som mål å støtte dette scenariet i fremtiden. Du kan fremdeles dra nytte av konfigurasjonsfunksjonene elektronisk fakturering har, og konfigurere det elektroniske faktureringsformatet selv, eller du kan arbeide med en partner/ISV for å konfigurere dem for organisasjonen.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Er Dynamics 365 for Regulatory Services en ny modul, som Human Resources eller Project Operations, som er knyttet til Finance or Supply Chain Management? Er det ekstra kostnader for dette?

Dynamics 365 for Regulatory Services (RCS) er en skytjeneste for konfigurering av globaliseringsressurser. RCS er gratis for alle som har lisens for Finance, Supply Chain Management og Project Operations.

For RCS-registrering kan du gå til <https://marketing.configure.global.dynamics.com/>.

Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>Må jeg registrere meg for å få tjenesten for elektronisk fakturering, eller kan jeg bare aktivere det i Funksjonsstyring?

Hvis du har lisens for Finance, Supply Chain Management og Project Operations, kan du se [Komme i gang med tjenesteadministrasjon for tillegget for elektronisk fakturering](e-invoicing-get-started-service-administration.md) for å registrere deg for elektronisk fakturering.

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Fungerer tjenesten for elektronisk fakturering med virtuelle maskiner på nivå 1? Hva er det minste nødvendige miljøet?

Integrering med tjenesten for elektronisk fakturering krever at minst en virtuell maskin på nivå 2 er vert for Finance eller Supply Chain Management. Hvis du vil ha mer informasjon om miljøplanlegging, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>Har tjenesten for elektronisk fakturering en testmodus for testing av fakturainnsending?

Dette kan oppnås ved hjelp av konfigurasjon. Hvis du vil teste fakturainnsending, kan du koble til Finance eller Supply Chain Management fra et UAT-miljø (brukergodkjenningstest) og sende testfakturaene. Elektronisk fakturering støtter konfigurering av digitale testsertifikater, og når det gjelder e-fakturaer som krever digital godkjenning, støtter oppsett av en URL-adresse fra testwebtjenester som er publisert av skattemyndighetene.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Finnes det dokumentasjon om medfølgende landspesifikke funksjoner for tjenesten for elektronisk fakturering?

Ja. Hvis du vil ha informasjon om tilgjengeligheten av funksjoner for elektronisk fakturering og formatene de støtter, kan du se [Tilgjengelighet av funksjoner for elektronisk fakturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>Tillater tjenesten for elektronisk fakturering en juridisk enhet i Finance eller Supply Chain Management som er konfigurert for et bestemt land til å forbruke elektroniske faktureringsfunksjoner fra ulike land/områder?

Ja. Funksjonene for elektronisk fakturering kan brukes til å behandle forretningsdokumentinnsendinger uavhengig av landet til den juridiske enheten, hvis følgende er sann:

   - Forretningsdokumentet som genereres, bruker den riktige dokumentmodelltilordningen.
   - Det er samsvar mellom forretningsdokumentet og gjeldende regler konfigurert i funksjonen for elektronisk fakturering.

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>Bruker tjenesten for elektronisk fakturering den samme konfigurasjons- og utformingserfaringen som tilbys av modulen for elektronisk rapportering i Finance og Supply Chain Management? 

Ja. De samme utformingsverktøyene som brukes i ER-modulen (Electronic Reporting) i Finance og Supply Chain Management brukes til å opprette og konfigurere konfigurasjoner for datamodelltilordning og filformat. Disse designerverktøyene brukes også i RCS (Regulatory Configuration Services) til å opprette og konfigurere konfigurasjoner for datamodelltilordning og filformat som brukes i konfigurasjonen av e-faktureringsfunksjonene.

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>Kan gjeldende regler utvides og konfigureres, slik at de ikke er knyttet til noen bestemte parametere, for eksempel en juridisk enhet?

Ja. Gjeldende regler er fullt konfigurerbare. Du kan legge til eller fjerne setninger, bygge logikkoperasjoner og gruppere og fjerne gruppering for setninger. Hvis du vil ha mer informasjon, kan du se [Relevansregler](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules).

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>Støtter tjenesten for elektronisk fakturering å legge til andre ER-formatkonfigurasjoner for å generere andre dokumenttyper? Støtter det sending av dokumentene elektronisk til kunder, for eksempel en følgeseddel?

Du kan bruke andre ER-formatkonfigurasjoner til å lage de ønskede utdatafilene. ER-formatkonfigurasjonen må imidlertid avledes fra samme ER-fakturamodelltilordning som er konfigurert i Finance eller Supply Chain Management for å generere forretningsdokumenter. Ved å sende utdatafilen direkte til kunden som en EDI-transaksjon, støttes ikke innholdet som standard av elektronisk fakturering.

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>Støtter tjenesten for elektronisk fakturering utveksling av elektroniske fakturaer med kunder? Støtter det konfigurasjon av ulike fakturaformater for den samme fakturaen?

Muligheten til å motta og importere elektroniske fakturaer for leverandører er på kartet, men automatisk sending av de elektroniske fakturaene til kunder støttes ikke nå.

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>Omfatter tjenesten for elektronisk fakturering støtte utveksling av EDI-meldinger med andre firmaer?

Fokus for tjenesten for elektronisk fakturering er å utveksle elektroniske fakturameldingstyper som drives av forskriftsmessige samsvarskrav. Mottak og import av elektroniske leverandørfakturaer er på kartet, men sending av elektroniske fakturafiler til kundene støtter ikke som standard, bortsett fra i scenarier der sending av den elektroniske fakturaen til kunden er et forskriftsmessig krav.

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>Støtter tjenesten for elektronisk fakturering import eller fletting av tilpasninger som gjøres i ER-formatkonfigurasjonene fra den eldre funksjonen for elektronisk fakturering?

Du kan bruke ER-formatkonfigurasjoner på nytt i tjenesten for elektronisk fakturering. ER-formatkonfigurasjonen må imidlertid avledes fra samme ER-fakturamodelltilordning som funksjonen for elektronisk fakturering av designet til å bruke, og som er konfigurert i Finance eller Supply Chain Management for å generere forretningsdokumenter.

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>Støtter tjenesten for elektronisk fakturering utstedelse av elektroniske fakturaer fra egendefinerte tabeller? I så fall, hvordan oppretter du ER-datamodellkonfigurasjonene for disse nye tabellene og enhetene?

Ja. Det krever imidlertid at fakturamodelltilordningen tilpasses og legges til de nødvendige referansene i de egendefinerte tabellene, eller avhengig av kompleksiteten, oppretting av en ny tilordning av fakturamodell.

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>Støtter tjenesten for elektronisk fakturering forskjellige webtjenestesluttpunkter?

Tjenesten for elektronisk fakturering støtter forskjellige webtjenestesluttpunkter. Du kan bruke konfigurerbar integrasjon med REST-webtjenester eller en rekke parametriserte landspesifikke webtjenesteintegrering. Ulike sluttpunkt kan konfigureres for de samme webtjenestene og APIene ved hjelp av ulike versjoner av konfigurasjoner. Hvis du vil ha mer informasjon, se [Liste over parametere etter handling](e-invoicing-setup.md#list-of-parameters-by-action).

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>Integreres elektronisk fakturering med de ulike fakturaoperatørenes APIer fra de nordiske landene, eller skal de håndteres for hver enkelt sak?

Microsoft utvider kontinuerlig funksjonsdekning for å gi standardintegrasjoner ved hjelp av funksjonene for elektronisk fakturering. Hvis du vil ha mer informasjon om formatene og integreringene som støttes, kan du se [Tilgjengelighet for funksjoner for elektronisk fakturering](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Hvis du ikke fant svaret du er på jakt etter, kan du sende spørsmålet til produktutviklingsgruppen på <D365EInvoicePreview@microsoft.com>. Vi vil enten kontakte deg eller forbedre dekningen av disse vanlige spørsmålene.
