---
title: Konfigurere et evaluerings miljø for e-handel
description: Denne veiledningen inneholder trinnvise instruksjoner for klargjøring og konfigurasjon av forhåndsvisningsmiljøet for Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771686"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>Konfigurere et evaluerings miljø for e-handel

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Denne veiledningen inneholder trinnvise instruksjoner for klargjøring og konfigurasjon av forhåndsvisningsmiljøet for Microsoft Dynamics 365 Commerce. Før du begynner anbefaler vi at du minst skumleser dokumentasjonen for å få en pekepinn på hva prosessen medfører og hva veiledningen inneholder.

*Obs! Hvis du ikke har fått tilgang til Microsoft Dynamics 365 Commerce-forhåndsvisningen ennå, kan du be om forhåndsvisningstilgang fra [nettstedet for e-handel](https://aka.ms/Dynamics365CommerceWebsite).*

## <a name="summary"></a>Sammendrag
Hvis du vil klargjøre miljøet uten problemer, må du opprette prosjektet med et bestemt produktnavn og en bestemt produkttype. Miljøet og Retail Cloud Scale Unit har også bestemte parametere du må bruke for å starte klargjøringen av e-handel senere. Instruksjonene i denne veiledningen inneholder alle de nødvendige trinnene du trenger å utføre, og parametere du må bruke.

Når klargjøringen er fullført, er det noen få trinn du må ta i etterkant for å klargjøre forhåndsvisningsmiljøet. Noen trinn er valgfrie, avhengig av hvilke aspekter av systemet du vil evaluere. Hvis du senere ombestemmer deg, kan du alltid kjøre de valgfrie trinnene senere.

Hvis du har spørsmål om klargjøringstrinnene eller du får problemer, kan du fortelle oss i [Yammer-gruppen for Microsoft Dynamics 365 Commerce-forhåndsvisningen](https://aka.ms/Dynamics365CommercePreviewYammer). 

## <a name="prerequisites"></a>Forutsetninger
Følgende er forutsetninger for klargjøring av ditt Dynamics 365-forhåndsvisningsmiljø:
* Du har tilgang til **Lifecycle Services-portalen (LCS)**
* Du er **godtatt i Dynamics 365 Commerce-forhåndsvisnings programmet**
* Du har de nødvendige tillatelsene til å opprette et prosjekt for **Potensielt førsalg** eller **Overfør, opprett løsninger og finn ut mer om**
* Du er medlem av **Miljøadministrator**- eller **Prosjekteier**-rollen i prosjektet der du skal klargjøre miljøet
* Du har administratortilgang til Azure-abonnementet eller kontakt med en abonnementsadministrator som kan utføre de to trinnene som krever administratortillatelser på dine vegne
* Du har **AAD-leier-ID** tilgjengelig
* Du har opprettet en **AAD-sikkerhetsgruppe** som skal brukes som **systemadministratorgruppe for e-handel** , og du har ID-en tilgjengelig
* Du har opprettet en **AAD-sikkerhetsgruppe** som skal brukes som **moderatorgruppe for vurderinger og omtaler**, og du har ID-en tilgjengelig (kan være den samme SG som systemadministrasjonsgruppen over).
## <a name="provisioning-preview-environment"></a>Klargjøring av forhåndsvisningsmiljø
Disse instruksjonene dekker klargjøringen av Microsoft Dynamics 365 Commerce-forhåndsvisningsmiljøet. Når du har fullført disse trinnene, vil du få et forhåndsvisningsmiljø som er klart til å konfigureres. Alle aktivitetene som beskrives her, skjer i LCS-portalen.

*Vær oppmerksom på at forhåndsvisningstilgangen er knyttet til LCS-kontoen og -organisasjonen du har angitt i forhåndsvisningsprogrammet. Du må bruke den samme kontoen for klargjøring. Hvis du må bruke en annen LCS-konto eller -leier for forhåndsvisningsmiljøet, må du gi oss disse detaljene. Hvis du vil ha kontaktinformasjon, kan du se "Tilleggsressurser".*
### <a name="before-starting"></a>Før du starter
##### <a name="grant-access-to-e-commerce-applications"></a>Gi tilgang til e-handelsprogrammer

*Obs: **Personen som logger seg på, må være AAD-administrator**. Uten å fullføre dette trinnet vil resten av klargjøringstrinnene mislykkes.*

1. Du må ha **AAD-leier-ID** til dette trinnet. Du må autorisere e-handelsprogrammer for å få tilgang til Azure-abonnementet. Den enkleste måten å oppnå dette på, er å sette sammen en URL-adresse som dette:

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Ikke klikk URL-adressen direkte**, i stedet kopierer og limer du den inn i leser- eller tekstredigeringsprogrammet og erstatter **\{AAD_TENANT_ID\}** med **AAD-leier-ID** før du navigerer til URL-adressen.
3. Du vil bli presentert med Microsoft AAD-påloggingsdialogboksen, der du bekrefter at du vil gi Dynamics 365 Commerce (forhåndsvisning) tilgang til abonnementet.
4. Du vil bli sendt til en side som bekrefter om operasjonen var vellykket.

##### <a name="log-in-to-the-lcs"></a>Logg på LCS
1. Logg på LCS-portalen: https://lcs.dynamics.com
1. Kontroller at du er logget på med den samme LCS-kontoen som du brukte til å be om tilgang til forhåndsvisningen.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Kontroller at forhåndsvisningsfunksjonene er tilgjengelige og aktivert
1. På LCS-forsiden ruller du helt til høyre og klikker på flisen **Administrasjon av forhåndsvisningsfunksjoner**.
1. Bla ned til "PRIVATE FORHÅNDSVISNINGSFUNKSJONER", og kontroller at følgende funksjoner er tilgjengelige og aktivert:
    1. **E-handelsevaluering**
    1. **Programmiljøer for Commerce-forhåndsvisning**
1. Hvis du ikke kan se disse funksjonene i listen, kan du kontakte oss med jobb-e-post, LCS-konto og leierdetaljer. Se **Flere ressurser** nedenfor hvis du vil ha informasjon om hvordan du kontakter oss.

![Fanen Forhåndsversjonsstyring](./media/preview1.png)

![Forhåndsvisningsfunksjoner](./media/preview2.png)
### <a name="create-project"></a>Opprett prosjekt
##### <a name="creating-new-project"></a>Opprette nytt prosjekt
1. Klikk på **+** for å opprette et nytt prosjekt.
1. Hvis du er en partner, velger du **Overfør, opprett løsninger og finn ut mer om**.
1. Hvis du er kunde, velger du **Potensielt førsalg**.
1. Angi et navn, en beskrivelse og en bransje etter behov.
1. Velg **Dynamics 365 Retail**, og velg **Produktnavn**.
1. Velg **Dynamics 365 Retail**, og velg **Produktversjon**.
1. For **Metodologi** velger du **Implementeringsmetodologi for Dynamics Retail**.
1. Du kan importere roller og brukere fra et eksisterende prosjekt hvis du ønsker det.
1. Klikk **Opprett**.
1. Du sendes til prosjektvisningen.
##### <a name="add-azure-connector"></a>Legge til Azure-kobling
1. Hvis du er en partner, klikker du **Prosjektinnstillinger** fra verktøyfilsene helt til høyre.
1. Hvis du er en kunde, velger du **Prosjektinnstillinger** fra den øverste menyen.
1. Velg **Azure-koblinger**.
1. Klikk **Legg til** for å legge til Azure-kobling.
1. Skriv inn et navn.
1. Angi **ID for Azure-abonnement**.
1. Aktiver **Konfigurer til å bruke ARM (Azure Resource Manager)**.
1. Kontroller at **AAD-leierdomene (eller ID) for Azure-abonnement** er riktig. Kontakt om nødvendig Azure-abonnementsadministratoren.
1. Klikk **Neste**.
1. Følg instruksjonene på skjermen for å gi de nødvendige programmene tilgang til abonnementet. Kontakt om nødvendig Azure-abonnementsadministratoren:
    1. Logg på Azure-portalen: https://portal.azure.com/
    1. Kontroller at du har valgt riktig katalog.
    1. Klikk **Abonnementer** på menyen til venstre.
    1. Finn det riktige abonnementet fra listen, og velg det. Bruk søk hvis det er nødvendig.
    1. Velg **Tilgangskontroll (IAM)** på menyen.
    1. Klikk **Legg til** under **Legg til rolletilordning** på høyre side. **Legg til rolletilordning**-ruten åpnes.
    1. Velg **Bidragsyter** for **Rolle**.
    1. For **Tilordne tilgang til** lar du valget for **Azure AD-bruker, -gruppe eller -tjenestekontohaver** stå.
    1. Under **Velg** angir du **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Velg **Dynamics-distribusjonstjenester [wsfed-aktivert]** fra listen.
    1. Klikk **Lagre**.
1. Klikk **Neste**.
1. Følg instruksjonene på skjermen for å gi de nødvendige programmene tilgang til abonnementet. Kontakt om nødvendig Azure-abonnementsadministratoren.
1. Klikk **Neste**.
1. For **Azure-område** velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.
1. Klikk **Koble til**.
1. Din Azure-kobling skal vises i listen.
### <a name="import-extension"></a>Importere utvidelse
1. Gå tilbake til prosjektets forside ved å klikke prosjektnavnet øverst.
1. Hvis du er en partner, klikker du **Aktivabibliotek** fra verktøyfilsene helt til høyre.
1. Hvis du er en kunde, velger du **Aktivabibliotek** fra den øverste menyen.
1. Velg **Distribuerbar programvarepakke** fra listen til venstre.
1. Klikk **IMPORTER** i handlingsruten.
1. Velg **Miljøer for e-handelsforhåndsvisning** fra listen over aktiva under **DELT AKTIVABIBLIOTEK**.
1. Klikk **Plukk**.
1. Du kommer tilbake til aktivabiblioteket, og du skal se utvidelsen i listen.

![Prosjektopprettelse – versjoner](./media/import.png)
### <a name="deploy-environment"></a>Distribusjonsmiljø

*Merk: Det er mulig at trinn 6, 7 og/eller 8 ikke vil vises, siden skjermer med ett alternativ hoppes over. Når du er i **Miljøparametere**-visningen, må du bekrefte at du har teksten "Dynamics 365 Commerce (forhåndsvisning) – Demo (10.0.6 med Platform update 30)" rett over **Miljønavn**-feltet. Se skjermbildet nedenfor.*

1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Klikk **+ Legg til** for å legge til et miljø.
1. For **Programversjon** velger du **10.0.6**.
1. Velg **Platform update 30** for **Plattformversjon**.
1. Klikk **Neste**.
1. Velg **DEMO**for miljøtopologi.
1. For miljøtopologi velger du **Dynamics 365 Commerce (forhåndsvisning) – demo**.
1. Hvis du konfigurerte en enkelt Azure-kobling tidligere, vil den bli brukt for dette miljøet. Hvis du konfigurerte flere Azure-koblinger, har du muligheten til å velge hvilken kobling du vil bruke: **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2** (anbefales for best slutt-til-slutt-ytelse)
1. Skriv inn et **Miljønavn**.
1. Juster VM-størrelsen slik det passer. (Vi anbefaler VM-SKUen **D13 v2**.)
1. La **Avanserte innstillinger** stå som de er.
1. Når du har gått gjennom vilkårene for prissetting og lisensiering på skjermen, merker du av for å angi avtale.
1. Klikk **Neste**.
1. Klikk **Distribuer**på bekreftelsesskjermen for distribusjon når du har bekreftet at detaljene er riktige.
1. Du kommer tilbake til visningen **Skybaserte miljøer**, og miljøet skal vises i listen.
1. Det forespurte miljøet vil vises som en kø og deretter distribueres. Det vil ta litt tid å fullføre alle miljøarbeidsflytene, så kom tilbake etter et par timer (ca. 6–9 timer).
1. Før du fortsetter må du kontrollere at miljøstatusen er **Distribuert**.

![Prosjektopprettelse – versjoner](./media/project1.png)

![Prosjektopprettelse – topologi 1](./media/project2.png)

![Prosjektopprettelse – topologi 2](./media/project3.png)

![Prosjektopprettelse – miljøparametere](./media/project4.png)
### <a name="initialize-rcsu"></a>Initialiser RCSU
1. Velg miljøet ditt fra listen i visningen **Skybaserte miljøer**.
1. I miljøvisningen på høyre side av skjermen klikker du **Detaljerte opplysninger**. Detaljerte opplysninger for miljø vises.
1. Klikk **Behandle** under **MILJØFUNKSJONER**.
1. Klikk **Initialiser** i kategorien **Detaljhandel**. Visningen av parametere for RCSU-initialisering vil vises.
1. For **OMRÅDE** velger du **USA øst**, **USA øst 2**, **USA vest** eller **USA vest 2**.
1. For **VERSJON** må du først velge **Angi en versjon** fra rullegardinlisten, og deretter angir du **9.16.19262.5** i tekstfeltet som vises nedenfor. *Obs! Kontroller at du **angir nøyaktig versjon** som skal vises her, for å unngå å måtte oppdatere RCSU senere til riktig versjon.*
1. Aktiver **Bruk utvidelse**.
1. Velg **Miljøer for e-handelsforhåndsvisning** fra listen over utvidelser.
1. Klikk **Initialiser**.
1. Klikk **Ja** på bekreftelsesskjermen for distribusjon når du har bekreftet at detaljene er riktige.
1. Du returneres til visningen **Detaljhandelsstyring** med kategorien **Detaljhandel** aktivert. RCSU-en din er lagt i kø for klargjøring.
1. Vent til RCSU-statusen er **VELLYKKET** før du fortsetter (tar ca. 2–5 timer).
### <a name="initialize-e-commerce"></a>Initialisere e-handel
1. Bytt til kategorien **e-handel (forhåndsvisning)**.
1. Klikk **Oppsett**når du har gått gjennom tillatelse for forhåndsvisning.
1. Angi et navn for **Navn på e-handelsleier**. Vær imidlertid oppmerksom på at dette vil være synlig i noen av URL-adressene som peker til e-handelsforekomsten.
1. For **Retail cloud scale unit-navn** velger du RCSU fra listen (listen kan bare ha ett alternativ).
1. **Geografi for e-handel** fylles ut automatisk og kan ikke endres.
1. Klikk **Neste** for å fortsette.
1. For **Støttede vertsnavn** angir du et gyldig domene (f.eks. www.fabrikam.com).
1. For **AAD-sikkerhetsgruppe for systemadministrasjon** angir du AAD SG-IDen du vil bruke som systemadministrasjonsgruppe for e-handel.
1. For **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler** angir du AAD-ID-en du vil bruke som moderatorgruppe for vurderinger og omtaler.
1. La **B2C**-verdiene stå tomme (7 felt som begynner med B2C).
1. La **Aktiver tjeneste for vurderinger og omtaler** være aktivert.
1. Klikk **Initialiser**.
1. Du returneres til visningen **Detaljhandelsstyring** med kategorien **e-Commerce (forhåndsvisning)** aktivert. Initialiseringen av e-handel har startet.
1. Før du fortsetter må du vente til initialiseringsstatusen for e-handel er **INITIALISERING VELLYKKET**.
1. Under **KOBLINGER** nederst til høyre.
    * Noter deg koblingen **E-handel-området**. Dette er koblingen til roten på C2-området.
    * Noter deg koblingen **Administrasjonsverktøy for e-handelsområde**. Dette er koblingen til områdebehandlingsverktøyet (C1-redigeringsverktøy).
## <a name="post-provisioning-steps"></a>Trinn etter klargjøring
På dette stadiet er miljøet klargjort ende-til-ende, men det finnes fortsatt konfigurasjonstrinn som må tas hånd om før du kan begynne å evaluere miljøet.
### <a name="before-starting"></a>Før du starter
1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Velg miljøet fra listen.
1. Klikk **Detaljerte opplysninger** fra miljøinformasjonen til høyre.
1. Klikk **Pålogging** for å åpne en meny, og velg **Logg på miljøet**.

Kontroller at den juridiske enheten **USRT** er valgt (øvre høyre hjørne).

### <a name="configure-pos"></a>Konfigurer POS
##### <a name="associate-worker-with-your-identity"></a>Knytt arbeideren til din identitet
1. Bruk menyen til venstre, og gå til **Moduler > Detaljhandel > Ansatte > Arbeidere**.
1. Finn og velg ønsket post i listen **000713 - Andrew Collette**.
1. I handlingsruten klikker du på **Detaljhandel**.
1. Klikk **Tilknytt eksisterende ID**.
1. I feltet **E-post** (til høyre for **Søk ved hjelp av e-post**) skriver du inn e-postadressen din.
1. Klikk **Søk**.
1. Velg posten med navnet ditt.
1. Klikk **OK**.
1. Klikk **Lagre**.
##### <a name="activate-cloud-pos"></a>Aktivere Skysalgssted
1. Logg på LCS-portalen.
1. Naviger til prosjektet.
1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Velg miljøet fra listen.
1. Klikk **Detaljerte opplysninger** fra miljøinformasjonen til høyre.
1. Klikk **Pålogging** for å åpne en meny, velg **Logg på Cloud Point of Sale**, salgsstedet skal lastes inn.
1. Klikk **Neste**.
1. Logg på med AAD-kontoen din.
1. Under **Butikknavn** velger **San Francisco**.
1. Klikk **Neste**.
1. Under **Register og enhet** velger du **SANFRAN-1**.
1. Klikk **Aktiver**.
1. Du bør være logget av og ende opp i påloggingsskjermbildet for salgsstedet.
1. Du kan nå logge på Cloud POS-opplevelsen ved hjelp av operatør-ID-en **000713** og passordet **123**.
### <a name="site-setup"></a>Weboppsett
1. Logg deg på **områdebehandlingsverktøyet** ved hjelp av URL-adressen du noterte tidligere.
1. Klikk på **Fabrikam**-området for å åpne dialogboksen for områdeoppsett.
1. For domene velger du domenet du angav tidligere under initialisering av e-handel.
1. Velg **Fabrikam-utvidet nettbutikk** for standardkanal. *Merk: Pass på at du velger den **utvidede** nettbutikken*
1. Velg **nb-no** for standardspråk.
1. La **Bane** stå som den er.
1. Klikk **OK**.
1. Du vil bli sendt til listen over sider på området.
### <a name="enable-jobs"></a>Aktivere jobber
1. Logg på miljøet (hovedkontor).
1. Gå til **Detaljhandel > Forespørsler og rapporter > Satsvise jobber** ved hjelp av menyen til venstre.
1. Utfør følgende trinn for hver jobb i listen nedenfor:
    * **Behandle e-postvarsling for detaljistordre**.
    * **Produkttilgjengelighet**.
    * **P-0001**.
    * **Synkroniser ordrejobb**.
1. Bruk hurtigfilteret til å søke etter jobben ved hjelp av navnet (oppført ovenfor).
1. Hvis statusen for jobben er **Trekk tilbake**, utfører du følgende trinn:
    1. Velg posten.
    1. Åpne **Satsvis jobb**-båndet i handlingsruten, og klikk på **Endre status**.
    1. Velg **Venter**, og klikk på **OK**.
### <a name="run-full-data-sync"></a>Kjør fullstendig datasynkronisering
1. Bruk menyen til venstre og gå til **Moduler > Detaljhandel > Hovedkvarteroppsett > Detaljhandel Planlegger**> Kanaldatabase.
1. **Standard**-kanalen velges fra listen til venstre. *Velg den andre tilgjengelige kanalen (navngitt **scXXXXXXXXX**)*.
1. Klikk **Fullstendig datasynkronisering** fra handlingsruten.
1. Angi **9999** som distribusjonsplan.
1. Klikk **OK**.
1. Klikk **OK**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Etter disse trinnene er du klar til å starte evaluering av forhåndsvisningsmiljøet!
Bruk URL-adressen for **Verktøy for administrasjon av e-handel-området** til å navigere til C1-redigeringsopplevelsen og URL-en til **E-handel-området** for å navigere til C2-områdeopplevelsen.

## <a name="additional-resources"></a>Tilleggsressurser
### <a name="how-to-find-your-aad-tenant-id"></a>Slik finner du din AAD-leier-ID
AAD-leier-ID er en GUID og ser slik ut: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>Fra Azure-portal
1. Logg på Azure-portalen: https://portal.azure.com/
1. Kontroller at du har valgt riktig katalog.
1. Klikk **Azure Active Directory** fra menyen til venstre.
1. Velg **Egenskaper** under **Behandle**.
1. AAD-leier-ID vises under **Katalog-ID**.
##### <a name="from-openid-connect-metadata"></a>Fra OpenID-tilkoblingsmetadata
Opprett **OpenID-URL** ved å erstatte **\{YOUR_DOMAIN\}** med ditt domene, for eksempel microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration vil bli https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Gå til **OpenID-URL** med ditt domenet i det.
1. AAD-leier-ID kan vises i flere egenskapsverdier.
1. Finn **authorization_endpoint**, og trekk ut GUIDen rett etter **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>Finne IDen til AAD-sikkerhetsgruppen
AAD-sikkerhetsgruppe-ID-en er en GUID og ser slik ut: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

Dette trinnet forutsetter at brukeren er medlem av gruppen de prøver å finne ID for.
1. Naviger til Graph Explorer: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Klikk **Logg på med Microsoft**, og logg på med legitimasjonen din.
1. Når du har logget på, klikker du på **vis flere eksempler** fra venstre.
1. Aktiver **Grupper** fra høyre rute.
1. Lukk høyre rute.
1. Klikk **alle grupper jeg tilhører**.
1. Finn gruppen fra tekstboksen **Forhåndsvis svar**.
1. ID for sikkerhetsgruppe er registrert under egenskapen **ID**.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Teste kredittkortinformasjon for å utføre testinnkjøp
Hvis du skal utføre testtransaksjoner på området, kan du bruke denne testkredittkortinformasjonen:

Kortnummer: 4111-1111-1111-1111, utløpsdato: 10/20, CVV: 737

*Merk: du bør ikke prøve å bruke faktisk kredittkortinformasjon på testområdet under noen omstendigheter!*
### <a name="useful-links"></a>Nyttige koblinger
* [LCS (Lifecycle Services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure-portal](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce-webområde](https://aka.ms/Dynamics365CommerceWebsite)
* [Hjelperessurser for Dynamics 365 Retail](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Kundestøtte for Microsoft Dynamics 365 Commerce forhåndsvisning
Hvis det oppstår problemer under utføring av klargjøringstrinnene, kan du gå til [Yammer-gruppen for Microsoft Dynamics 365 Commerce forhåndsvisning](https://aka.ms/Dynamics365CommercePreviewYammer) for å få hjelp. 

Hvis du har problemer med å få tilgang til Yammer-gruppen, kan du også nå oss via e-post på **Dynamics365Commerce@microsoft.com**. Denne e-postadressen overvåkes ikke aktivt, så du bør forvente et forsinket svar.
***
## <a name="prerequisites-for-optional-features"></a>Forutsetninger for valgfrie funksjoner
Hvis du vil evaluere de transaksjonelle e-postfunksjonene, må følgende forutsetninger oppfylles:
* Du har en e-postserver tilgjengelig (SMTP-server), som kan brukes fra Azure-abonnementet der du klargjør forhåndsvisningsmiljøet.
* Du har serverens FQDN/IP, SMTP-portnummer og godkjenningsinformasjon tilgjengelig.

Hvis du vil evaluere funksjoner for digital aktivastyring, spesielt ta inn nye omnikanalbilder, må følgende forutsetninger være oppfylt:
* Du må ha **CMD-leiernavn** tilgjengelig. Du finner mer informasjon om dette navnet nedenfor.
### <a name="configure-image-backend-optional"></a>Konfigurere bildeserver (valgfritt)
##### <a name="finding-your-media-base-url"></a>Finne primær URL-adresse for media
*Obs! Før du kan fullføre dette trinnet, må du fullføre **Områdeoppsett**.*
1. Logg deg på områdebehandlingsverktøyet ved hjelp av URL-adressen du noterte tidligere.
1. Åpne **Fabrikam**-området.
1. Velg **Aktiva** på menyen til venstre.
1. Velg et hvilket som helst enkeltbilde.
1. Finn **Offentlig URL** fra egenskapsinspektøren til høyre. Den har en URL-adresse.
    * Eksempel-URL: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Erstatt den siste identifikatoren i URL-adressen (MA1nQC i eksempel-URL-adressen ovenfor) med følgende streng: **search?fileName=**
    * Eksempel på URL-adresse etter erstatning: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Dette er **URL-adresse for media** – noter den.
##### <a name="updating-the-media-base-url"></a>Oppdatere primær URL-adresse for media
1. Logg på miljøet (hovedkontor).
1. Bruk menyen til venstre og gå til **Moduler > Detaljhandel > Kanaloppsett > Kanalprofiler**.
1. Klikk **Rediger**.
1. Fra **Profilegenskaper** erstatter du egenskapsverdien for **Primær URL-adresse for medieserver** med **Primær URL-adresse for media** du opprettet tidligere.
1. Velg den andre kanalen fra listen til venstre, under **Standard**-kanal.
1. Klikk **+ Legg til** under **Profilegenskaper**.
1. For egenskapen som ble lagt til, velger **Primær URL-adresse for medieserver** som egenskapsnøkkel, og for egenskapsverdi angir du **Primær URL-adresse for media** som du opprettet tidligere.
1. Klikk **Lagre**.

### <a name="configure-email-server-optional"></a>Konfigurere e-postserver (valgfritt)
Vær oppmerksom på at SMTP-serveren eller e-posttjenesten du angir her, må være tilgjengelig fra Azure-abonnementet du bruker for miljøet.
1. Logg på miljøet (hovedkontor).
1. Bruk menyen til venstre og gå til **Moduler > Detaljhandel > Hovedkvarteroppsett > Parametere > E-postparametere**.
1. Klikk kategorien **SMTP-innstillinger**.
1. I feltet **Server for utgående e-post** skriver du inn FQDN eller IP-adresse til SMTP-serveren eller e-posttjenesten.
1. I feltet **SMTP-portnummer** angir du portnummeret (standard er 25 når du ikke bruker SSL).
1. Skriv inn en verdi (hvis godkjenning er nødvendig) i feltet **Brukernavn**.
1. Skriv inn en verdi (hvis godkjenning er nødvendig) i feltet **Passord**.
1. Klikk **Lagre**.
1. Klikk **Oppdater**.
1. Klikk kategorien **Test e-post**.
1. Velg **SMTP** i feltet e-postleverandør.
1. I feltet **Send til** angir du e-postadressen der du vil at test-e-posten skal leveres.
1. Klikk **Send e-posttest**.
### <a name="configure-email-templates-optional"></a>Konfigurere e-postmaler (valgfritt)
E-postmalen for hver transaksjonshendelse du vil sende e-postmeldinger for, må oppdateres med en gyldig e-postadresse for avsender.
1. Bruk menyen til venstre, og gå til **Moduler > Organisasjonsstyring > Oppsett > Maler for e-post til organisasjon**.
1. Klikk **Vis liste**.
1. For hver av malene i listen:
    1. I feltet **Avsenders e-postadresse** skriver du inn senderens e-postadresse for denne e-postmalen.
    1. (Valgfritt) I feltet **Sendernavn** skriver du et navn som skal brukes som avsender for denne e-postmalen.
1. Klikk **Lagre**.
### <a name="customizing-email-templates-optional"></a>Tilpasse e-postmaler (valgfritt)
Du vil kanskje tilpasse e-postmalen til å bruke ulike bilder eller oppdatere koblingene i malen for å koble tilbake til forhåndsvisningsmiljøet. Trinnene nedenfor forklarer hvordan du laster ned standardmaler, tilpasser dem og oppdaterer malene i systemet.
1. Bruk en webleser og last ned [Microsoft Dynamics 365 Commerce forhåndsvisning av standard e-postmaler .zip-fil](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), som inneholder følgende HTML-dokumenter, til den lokale datamaskinen.
    1. Ordrebekreftelsesmal
    1. Utsted gavekort-mal
    1. Ny ordre-mal
    1. Pakke bestilt-mal
    1. Hent ordre-mal
1. Tilpass malene ved hjelp av et tekst- eller HTML-redigeringsprogram. Se en liste over støttede tokener nedenfor.
1. Logg på miljøet (hovedkontor).
1. Bruk menyen til venstre og gå til **Moduler > Detaljhandel > Hovedkvarteroppsett > Parametere > Maler for e-post til organisasjon**.
1. Utvid listen til venstre for å se alle malene.
1. For hver av malene du vil tilpasse, kan du utføre følgende trinn:
    1. Velg malen fra listen.
    1. Under **Innhold i e-postmelding** velger du riktig språkversjonen fra listen (standard **nb-no**).
    1. Under **Innhold i e-postmelding** klikker du **Rediger**, og da skal ruten **Last opp e-postmal** åpnes.
    1. Klikk **Bla gjennom**, og finn HTML-filen med det tilpassede innholdet.
    1. Klikk **Last opp**, og malen lastes opp til systemet, og en forhåndsvisning vises.
    1. Klikk **OK**.
    1. (Valgfritt) Tilpass egenskapen **Emne** for malen.
    1. Klikk **Lagre**.

#### <a name="supported-tokens-in-the-email-template"></a>Støttede tokener i e-postmalen
Disse tokenene blir erstattet på e-postgjengivelsestidspunktet med de faktiske verdiene som gjelder for kunden og deres ordre.

**Salgsordre** – Følgende tokener gjelder for den overordnede salgsordren.

|Navnet på tokenet|Token |
|---|---|
|Ordrenummer|%salesid%|
|Kundens navn|%customername%|
|Leveringsadresse|%deliveryaddress%|
|Faktureringsadresse|%customeraddress%|
|Bestillingsdato|%shipdate%|
|Leveringsmåte|%modeofdelivery%|
|Rabatt|%discount%|
|Merverdiavgift|%tax%|
|Ordretotal|%total%|

**Salgslinje** – Følgende tokener fylles ut for hvert produkt i ordren.

*Merk: Plasser tokenene for **Produktliste – start** og **Produktliste – slutt** på begynnelsen og slutten av HTML-blokken som gjentas for hvert produkt.*

|Navnet på tokenet|Token |
|---|---|
|Produktliste – start|\<!--%tablebegin.salesline% -->|
|Produktliste – slutt|\<!--%tableend.salesline%-->|
|Produktnavn|%lineproductname%|
|Beskrivelse|%lineproductdescription%|
|Antall|%linequantity%|
|Linjeenhetspris|%lineprice% (kontroller)|
|linjevaresum|%linenetamount%|
|linjerabatt|%linediscount%|
|Forsendelsesdato|%lineshipdate%|
|Innkjøpsmetode|%linedeliverymode%|
|leveringsadresse|%linedeliveryaddress%|
|Salgsenhet for linjen|%lineunit%|

