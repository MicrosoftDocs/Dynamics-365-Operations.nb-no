---
title: Funksjoner i Store Commerce-appen
description: Denne artikkelen beskriver funksjonaliteten i Store Commerce-appen for Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788520"
---
# <a name="store-commerce-app-capabilities"></a>Funksjoner i Store Commerce-appen

[!include [banner](includes/banner.md)]

Store Commerce-appen byr på den moderne salgsstedsopplevelsen for Microsoft Dynamics 365 Commerce. Den gjør at selskaper kan behandle transaksjoner i butikken og administrere administrasjonsoperasjoner, for eksempel beholdning og ordrebehandling. Med appen kan bedrifter også administrere kundeforhold med fordeler og kundeaktiviteter. 

Store Commerce-appen byr på en komplett omnikanalløsning som er basert på Commerce Scale Unit (CSU). En kunde kan for eksempel kjøpe et produkt på nettet og hente det i en butikk i nærheten, og dermed fortsette handleforløpet på tvers av kanaler uten å miste data. 

Denne artikkelen gir en oversikt over funksjonene i Store Commerce-appen.

## <a name="platform"></a>Plattform

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Omnikanal | Dynamics 365 Commerce gir en omfattende omnikanalløsning som forener opplevelser i administrasjonen, butikken og telefonsenteret samt digitale opplevelser. | [Oversikt](index.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Hodeløs Commerce | Commerce Scale Unit er vert for den hodeløse handelsmotoren. Den hodeløse handelsmotoren fungerer som det sentrale punktet for all forretningslogikk i handel og er drivkraften bak en komplett omnikanalløsning. | <p>[Oversikt over arkitektur](commerce-architecture.md)</p><p>[Hodeløs arkitektur](dev-itpro/retail-server-architecture.md)</p> | [Teknisk foredrag](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce headquarters | Commerce headquarters byr på administrasjonsfunksjoner som gjør at du kan konfigurere produkter, ansatte, forretningsprosesser, prissetting og annen funksjonalitet bedriften trenger. | [Oversikt over arkitektur](commerce-architecture.md) | |
| Salgssted | Store Commerce-appen byr på salgsstedsopplevelsen for Dynamics 365 Commerce. Den har omfattende salgsstedsfunksjoner som hjelper salgsmedarbeidere, kasserere og ledere å yte førsteklasses kundeservice. Den har i tillegg flere distribusjonsalternativer for forhandlere, bidrar til å forbedre ytelsen og gir forbedret administrasjon av programlivssyklusen (ALM). | [Store Commerce-appen](dev-itpro/store-commerce.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Video](https://youtu.be/7B332XH_zfs)</p><p>[Overgang fra MPOS til Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Skydistribusjon | Flere forekomster av Commerce Scale Units kan distribueres for belastningsfordeling og geografisk avstand. | [Skydistribusjon](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Lokal distribusjon | Commerce-kunder kan i større grad eie og administrere Dynamics 365-miljøer ved hjelp av en distribusjon av lokale forretningsdata. | [Lokal distribusjon](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Enhetsbehandling

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Flere formfaktorer | Store Commerce-appen støttes på flere enhetsformfaktorer, for eksempel PC-er, nettbrett og mobilenheter. Det responsive brukergrensesnittet gjør at du kan endre størrelsen på og justere oppsettet automatisk etter skjermstørrelsen. | [Visuelle konfigurasjoner](pos-screen-layouts.md) |  |
| På tvers av plattformer | Store Commerce-appen støttes på nett, Windows, iOS og Android. | [Plattformer](dev-itpro/hybridapp.md) | |
| Varemerking | I skjermutformingen kan du tilpasse skjermoppsett etter forretningsbehovene. I tillegg kan du lage temaer, oppsett, farger og bilder basert på ansattroller og deretter dele dem med brukerne for å holde varemerket konsekvent og øke brukervennligheten. | [Visuelle konfigurasjoner](pos-screen-layouts.md) | [Video](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topologi | Det er støtte for ulike topologier i butikken, basert på nettverkstilgjengelighet. | <p>[Topologi](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Infografikk](dev-itpro/retail-in-store-topology.md)</p> | |
| Administrasjon av flere enheter | Du kan enkelt administrere flere enheter i flere butikker fra Commerce headquarters. | [Aktivering](set-up-activation-accounts-validate-devices-hq.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Administrasjon av ansatte

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Pålogging | Hver butikkansatt kan ha en egen pålogging. Påloggingstyper omfatter brukernavn, strekkode, kortleser, biometri og Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Utvidet pålogging](extended-logon.md)</p> | |
| Tillatelser | Det er støtte for forskjellige tillatelsesnivåer for ansatte, for eksempel tillatelse til å opprette ordrer og tillatelse til å redigere ordrer. | [Tillatelser](tasks/create-pos-permission-groups.md) | |
| Administrasjon av tid og fremmøte | Fremmøte kan administreres ved hjelp av tidsklokkefunksjonen. Fremmøtedata kan behandles i lønn ved hjelp av appen Dynamics 365 Human Resources. | [Tidsbehandling](retail-time-attendance.md) | |
| Salgsprovisjon | Salg kan spores etter selger for å beregne provisjon eller andre insentiver. | [Provisjon](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Varehandel

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Sortimentstyring | Forhandleransvarlige kan klassifisere produkter slik at de er tilgjengelige for salg i en bestemt kanal og i en bestemt periode. | [Assortement](assortments.md) | |
| Kataloger | Forhandleransvarlige kan administrere kataloger for å identifisere produktene du vil tilby med katalogspesifikke priser. | [Kataloger](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Produkt- og kategoristyring | I Commerce headquarters kan forhandleransvarlige opprette produkter som har varianter, attributter, en måleenhet og så videre. De kan også definere et kategorihierarki for å organisere produkter. | [Produkt](retail-hierarchies.md) | |
| Bunter | Forhandleransvarlige kan gruppere produkter for å selge dem som en bunt eller et sett. | [Sett](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Infokoder | Bruk infokoder til å be kassereren om å angi informasjon i løpet av forskjellige handlinger på salgsstedet, for eksempel varesalg, retur av varer eller valg av kunder. | [Infokoder](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Koblede varer | Bruk koblede varer til mersalg av produkter når en vare legges til i transaksjon. | [Koblede varer](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Garantier | Utvidede garantier kan selges sammen med produkter. | [Garanti](extended-warranty.md) | |
| Etikettutskrift | Det går an å generere etiketter som inneholder produktinformasjon som partinummer, serienummer og utløpsdato. | [Etikettutskrift](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Assistert salg

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Bla gjennom produkter | Bla gjennom produkter etter kategori. | [Produkthierarki](retail-hierarchies.md) | |
| Produktsøk | Søk etter produkter basert på navn, og begrens søk ved hjelp av produktattributter som merke, pris og materiale. Denne funksjonen er basert på Azure Cognitive Search. | [Skybasert søk](cloud-powered-search-overview.md) | |
| Produktdetaljer-siden | Sider med omfattende produktdetaljer kan inneholde bilder, en beskrivelse, produktattributter og anbefalte produkter. Anbefalinger er basert på anbefalingstjenesten. | | |
| Produktsammenligning | Sammenligne flere produkter, og hjelp kundene å velge et og legge det til i en transaksjon. | | |
| Uendelig gang | Slå enkelt opp beholdning i andre butikker, og opprett ordrer. | [Beholdningsoppslag](pos-inventory-lookup-operation.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Anbefalinger | Mersalg og kryssalg av produkter ved hjelp av anbefalingstjenesten. Denne tjenesten bruker patentert teknologi til å komme med anbefalinger basert på kjøpstrender og egenskaper, for eksempel nye produkter, produkter med lignende utseende og bestselgere. Disse anbefalingene er tilgjengelige på sider med produktdetaljer, siden **Kundedetaljer** og siden **Transaksjoner**. | [Anbefalinger](product-recommendations.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Kunderelasjon

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Kundeadministrasjon | Opprett, rediger og administrer kundekontoer. Kundekontoer kan administreres i asynkron modus for å unngå sanntidsbehandling. | [Administrasjon](customer-mgmt-stores.md) | |
| Kundeattributter | Med rammeverket for kundeattributter kan ytterligere kunderelaterte data registreres basert på forretningsbehov. | [Attributter](dev-itpro/customer-attributes.md) | |
| Side med kundedetaljer | En omfattende side med kundedetaljer gir deg en omnikanalvisning av kundens samhandlinger på tvers av alle kanaler. Disse samhandlingene omfatter innkjøp, ønskelister og fordelspoeng. | | |
| Skybasert kundesøk | Søk etter kunder basert på navn, telefonnummer, e-postadresse, fordelskort, adresse og så videre. | [Skybasert søk](pos-search-improvements.md#customer-search) | |
| Fordeler | Kunder kan bli med i fordelsprogrammer og tjene opp og innløse fordelspoeng på tvers av kanaler. | [Fordeler](set-up-customer-loyalty-program.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| Kundeaktiviteter | Administrer viktige kunder ved å bruke en klientbok, og spor aktiviteter og notater i kundeprofilen. Integrering med Dynamics 365 Customer Insights lar butikkansatte få indikatorer om neste beste handling for hver kunde. | [Kundeaktiviteter](clienteling-overview.md#activities-and-notes) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>Priser og rabatter

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Handelsavtaler | Prissettingsansvarlige kan bruke forretningsavtaler til å definere spesialpriser basert på langsiktige avtaler for bestemte kunder. | [Priser](price-management.md)| [Video](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Salgsavtaler | Prissettingsansvarlige kan bruke salgsavtaler til å definere kontraktbaserte priser i handelsscenarioer for bedrift-til-bedrift (B2B). | [Priser](price-management.md) | |
| Prisjusteringer | Prissettingsansvarlige kan bruke funksjonen for prisjusteringer til å opprette, spore og administrere prisavslag for sine produkter over tid. | [Prisjusteringer](price-adjustments-discounts.md) | |
| Rabatter | Prissettingsansvarlige kan definere flere typer rabatter for å kjøre en rekke kampanjer. Disse rabattene omfatter enkle rabatter, kvantumsrabatter, terskelrabatter, samlerabatter, betalingsbaserte rabatter og forsendelsesrabatter. | [Rabatter](retail-discounts-overview.md) | |
| Kuponger | Prissettingsansvarlige kan definere kupongkoder eller strekkoder, koble dem til rabatter og distribuere dem til kunder. Salgsmedarbeidere kan legge til kuponger i salgstransaksjoner eller fjerne dem. | [Kuponger](coupons.md) | |
| Prisgrupper | Prissettingsansvarlige kan bruke prisgruppefunksjonen til å definere kontekstavhengige priser basert på kanaler, kataloger, tilknytninger eller fordelsprogrammer. | [Priser](price-management.md) | |
| Tilgjengelige kampanjer | Salgsmedarbeidere kan enkelt slå opp tilgjengelige kampanjer for produkter i butikken, produkter som er lagt til i en transaksjon, og så videre. | [Prisfunksjoner](pos-pricing-functions.md) | |
| Priskontroller | Salgsmedarbeidere kan raskt kontrollere aktive salgspriser på produkter i butikken. | [Prisfunksjoner](pos-pricing-functions.md) | |
| Prisoverstyringer | Salgsmedarbeidere som har de nødvendige tillatelsene, kan overstyre systemkonfigurerte eller beregnede priser. | [Prisfunksjoner](pos-pricing-functions.md) | |
| Manuelle rabatter | Salgsmedarbeidere som har de nødvendige tillatelsene, kan bruke manuelle rabatter på salgstransaksjons- eller salgslinjer. | [Prisfunksjoner](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektroniske betalinger

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Kredit og debet | Store Commerce-appen støtter betaling med kort fra de store kreditt-/debetkortselskapene via Adyen Payment Gateway og ordrefullføring via PayPal. SDK for betalinger tillater eksterne gateway-tilkoblinger som støttes av integrering med uavhengige programvareleverandører (ISV). | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[Betalinger](payment-methods.md)</p> | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Støtte for digital lommebok | Store Commerce-appen støtter betalinger via betalingsmetoder med digital lommebok som ikke bruker BIN-områder (Bank Identification Number) som tradisjonelle kreditt- og debetkort gjør. Betalingsmetoder kan tilordnes til betalinger med digital lommebok, for eksempel Adyen. | [Lommebok](wallets.md) | |
| Støtte for gavekort | Dynamics 365-gavekort med BIN (Bank Identification Number), SVS (Stored Value Solutions) og Givex-gavekort. Gavekort kan kjøpes og løses inn i en ordre. | [Gavekort](dev-itpro/gift-card.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Svindelbeskyttelse | Dynamics 365 Fraud Protection hjelper deg å forhindre svindelaktivitet og å identifisere steder der svindel kanskje ikke oppdages. | [Svindelbeskyttelse](dev-itpro/dfp.md) | [Video](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Avgifter og tillegg

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Avgifter | Store Commerce-appen støtter mange typer indirekte avgifter, blant annet merverdiavgift (mva), Goods and Services Tax (GST), enhetsbaserte gebyrer og kildeskatt. | [Avgifter](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Tillegg | Tillegg kan konfigureres på linjenivå, på hodenivå, som automatiske tillegg, etter kanal og så videre. | [Tillegg](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Ordrebehandling og -oppfyllelse

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Bestillingsoppretting | En ordre kan opprettes for forsendelse eller henting i en butikk i nærheten. Tidsrom kan gis for henting. | [Oversikt](customer-orders-overview.md) | |
| Ordreendring | En ordre kan endres, returneres, annulleres og så videre. | <p>[Avbryt](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Returer](pos-returns.md)</p> | |
| Søk i ordrer | Søk etter og filtrer ordrer ved hjelp av ordrespesifikk informasjon. | [Søk i ordrer](enhancedorderrecall.md) | |
| Ordreattributter | Med rammeverket for ordreattributt kan ytterligere ordrerelatert informasjon registreres basert på forretningsbehov. | [Attributter](dev-itpro/order-attributes.md) | |
| Direkte levering | Varer kan merkes for direkte levering fra en leverandør til en kundeadresse. Direktelevering er en rask form for levering. | [Direkte levering](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Tilbud | Butikkansatte kan opprette tilbud for kunder, og kan angi en spesialpris, manuelle rabatter og en gyldighetsdato for tilbudet. | [Tilbud](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Oppfyllelse | Butikker kan plukke, pakke og sende ordrer. En følgeseddel kan legges til i pakkene som er klare til forsendelse. | [Oppfyllelse](order-fulfillment-overview.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[Video](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| Behandling av distribuert ordre | Store Commerce-appen støtter optimalisering av intelligent ordreoppfyllelse der forretningsstrategier kan konfigureres basert på karakteren til virksomheten, kundetypen, opprinnelsen til en ordre og leveringsmetoden for en ordre. | [DOM](dom.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>Beholdningsstyring

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Kjøp etter ordre | Effektiviser distribusjonen av tilgjengelig beholdning fra et distribusjonssenter til flere butikker eller lagre. | [Kjøp etter ordre](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Direkteoverføring | Effektiviser distribusjonen av beholdning i innkommende bestillinger til flere butikker eller lagre. | [Direkteoverføring](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Innkommende beholdning | Motta beholdning fra en leverandør via en bestilling eller fra et annet lager via en overføringsordre. Opprett en innkommende bestilling eller overføringsordreforespørsel. | [Innlevering](pos-inbound-inventory-operation.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Utgående beholdning | Send beholdning til et annet lager via en overføringsordre, og opprett en forespørsel om utgående overføringsordre. | [Utlevering](pos-outbound-inventory-operation.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Beholdningsoppslag | Kontroller lagerbeholdningen for produkter på tvers av butikker og lagre, og kontroller beholdning som er tilgjengelig for ordre, på fremtidige datoer. | [Beholdningsoppslag](pos-inventory-lookup-operation.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Lagerjustering | Juster beholdning inn på eller ut av et butikklager for å oppfylle bestemte forretningsbehov uten å bruke et salg, et mottak eller en ny opptelling. | [Lagerjustering](work-with-store-inventory.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Lagerantall | Foreta vareopptelling, og juster systemets bokførte beholdning slik at den stemmer overens. | [Opptelling](work-with-store-inventory.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| Lagerbevegelse | Flytt beholdning mellom lokasjoner i en butikk. | [Bevegelse](work-with-store-inventory.md) | <p>[Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>Finans

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Kassastyring | Store Commerce-appen støtter styring av kontanter og andre angitte betalingsmidler i butikken. Skiftavstemming kan i tillegg aktiveres i butikken for avanserte kassastyringsfunksjoner. | [Kontanter](cash-mgmt.md) | |
| Regnskapsoppgjør og -avstemming | Kontanttransaksjoner for en butikk registreres i Commerce headquarters ved hjelp av utdragsposteringsprosessene. | [Utdrag](retail-statements.md) | |
| Inntekts- og utgiftstransaksjoner | Behandle håndkassetransaksjoner i butikken, og registrer inntekt som ikke kommer inn på en tradisjonell måte, for eksempel hittegodspenger, andelen av inntekt fra en kaffebutikk i lobbyen og tepperengjøringstjenester. | [Utdrag](retail-statements.md) | |
| Fakturabetalinger | Registrer betalinger mot fakturaer. | [Faktura](payinvoice.md) | |

## <a name="employee-productivity"></a>Ansattproduktivitet

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Oppgavebehandling | Opprett oppgavelister og oppgaver, og tilordne dem til butikker og ansatte. Spor statusen til oppgaver på tvers av butikker. Det er støtte for sømløs integrering med Microsoft Teams. | <p>[Oppgavebehandling](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Video](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Maskinvare og periferiutstyr

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Koble til eksterne enheter | Koble eksterne enheter, for eksempel skrivere, skannere og betalingsenheter til en salgsstedsterminal. | [Eksterne enheter](retail-peripherals-overview.md) ||
| Del eksterne enheter | Kvitteringsskrivere, kassaskuffer og betalingsenheter kan deles mellom mange terminaler ved å koble dem til en delt maskinvarestasjon. | <p>[Maskinvarestasjon](retail-peripherals-overview.md) ||
| Salgssted og simulator for eksterne enheter | Simulatoren for eksterne enheter støtter testing av scenarioer som vanligvis krever eksterne enheter for fysisk salgssted. Den omfatter også en simulator for salgssted som kan brukes til å teste kompatibiliteten til fysiske eksterne enheter uten at du trenger å distribuere salgsstedsklienten. | [Simulator](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Mottak

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Skriv ut kvitteringer | Kvitteringer av ulike typer, for eksempel salgskvitteringer, kredittkortkvitteringer, gavekvitteringer og fakturaer, kan skrives ut som standard eller etter kassererbekreftelse ved kassen. De kan også skrives ut på nytt fra journalen. | [Skriver ut](receipt-templates-printing.md) | |
| E-postkvitteringer | Kvitteringer kan sendes via e-post fra salgsstedet etter at kjøpet er fullført. | [E-post](email-receipts.md) | |
| Utform kvitteringer | Butikkvitteringer kan tilpasses slik at de viser data og oppsett som er passende for forhandleren og transaksjonstypen. Kvitteringer kan også utvides, slik at de viser egendefinerte data som kreves av forhandleren. | [Utforming](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Frakoblet støtte

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Problemfri frakoblet modus | Med problemfri frakoblet modus kan du fortsette driften selv om Internett-tilkobling er begrenset eller ikke tilgjengelig. Utelatelse av data hjelper deg å redusere datastørrelsen til frakoblede databaser og maksimere ytelse. | [Frakoblet](pos-operations.md) | |
| Ytelsesbasert bytting | Bytt til frakoblet modus når det blir oppdaget redusert ytelse. | [Frakoblet](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI) |
| Instrumentbord for frakoblet modus | Instrumentbordet **Frakoblet status** viser frakoblet status, feil og detaljer for dataene for hver enhet. Det er derfor enkelt å administrere statusen til mange enheter. | [Frakoblet](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Utvidelsesmuligheter

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Commerce headquarters | Commerce headquarters-løsninger kan tilpasses ved å legge til eller endre forretningsprosesser. Commerce headquarters støtter bruk av metadata og en kodedrevet utvidelsesmodell for å legge til egendefinert funksjonalitet. Den kan enkelt integreres i eksterne løsninger. | [Oversikt](dev-itpro/extend-customer-cdx-package.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Hodeløs handel | API-rammeverket for utvidbar omnikanal kan brukes til å tilpasse og legge til forretningslogikk. API-er som har forespørselsbehandlere og utvidelsesmønstre før og etter utløser. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| SDK for Commerce | SDK for Commerce inneholder koden, kodeeksemplene, malene og verktøyene som kreves for å utvide eller tilpasse funksjonaliteten i Dynamics 365 Commerce. SDK-en publiseres i ulike repositorier i GitHub, avhengig av utvidelseskomponentene. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Salgssted | Store Commerce-appen kan utvides uavhengig ved hjelp av funksjonen for salgsstedsutvidelse i SDK for Commerce. Rammeverket støtter tilpassing av brukeropplevelsen, arbeidsflytene og forretningslogikken. | [Salgssted](dev-itpro/pos-extension/pos-extension-overview.md) | [Teknisk foredrag](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Rapportering

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Salgsrapporter | Salgsrapporter etter stab, kasse, betalingstype, returer, produkt og så videre, er tilgjengelige for butikksjefer. Ledere kan vise disse rapportene og bruke dem til å tildele provisjon og identifisere produkttrender. | | |

## <a name="diagnostics"></a>Diagnostikk

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Driftsinnsikt | Måledata for pålitelighet og ytelse for tjenestetilstand kuratert i butikken er tilgjengelig i kundens abonnement på Application Insights. Avanserte funksjoner for varsling og overvåking er tilgjengelige. | | |
| Tilstandskontroll | Tilgjengelighet av eksterne enheter som er koblet til et salgssted, kan verifiseres ved å kjøre tilstandskontrollen. Individuelle problemer med eksterne enheter kan deretter rettes og verifiseres. | [Tilstandskontroll](pos-healthcheck.md) | [Video](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globalisering

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Støtte for flere markeder | Det er bruksklar støtte for markedsspesifikke funksjoner som regnskapsintegrering, GST, avansert fakturering og forskuddsbetalinger. Denne funksjonen dekker flere markeder i Europa, Amerika, Russland, Asia, Saudi-Arabia og så videre. | [Globalisering](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Samsvar

| Funksjon | Beskrivelse | Dokumentasjon | Tilleggsinnhold |
|---|---|---|---|
| Microsoft-standarder | Store Commerce-appen oppfyller Microsoft-standarder for sikkerhet, personvern, tilgjengelighet, EUs personvernforordning (GDPR), EU Data Boundary og så videre. | | |

