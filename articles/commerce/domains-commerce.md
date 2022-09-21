---
title: Domener i Dynamics 365 Commerce
description: Denne artikkelen beskriver hvordan domener behandles i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 09/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 132aec92d2b3d2765dd6bd261fb4182f8aae679a
ms.sourcegitcommit: dbb997f252377b8884674edd95e66caf8d817816
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/10/2022
ms.locfileid: "9465200"
---
# <a name="domains-in-dynamics-365-commerce"></a>Domener i Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan domener behandles i Microsoft Dynamics 365 Commerce.

Domener er webadresser som brukes til å navigere til Dynamics 365 Commerce-områder i en nettleser. Du styrer administrasjonen av domenet med en valgt DNS-leverandør (Domain Name Server). Det refereres til domener i hele områdebyggeren i Dynamics 365 Commerce for å koordinere hvordan et område skal åpnes når det er publisert. Denne artikkelen omtaler hvordan domener behandles og refereres til i løpet av livssyklusen til utvikling og lansering på handelsområdet.

> [!NOTE]
> Fra og med 6. mai 2022 blir alle miljøer som opprettes i Dynamics 365 Commerce, klargjort med domenet `.dynamics365commerce.ms`, og erstatter det tidligere mønsteret `.commerce.dynamics.com`. Eksisterende miljøer som er klargjort med domenet `.commerce.dynamics.com`, fortsetter å fungere.

## <a name="provisioning-and-supported-host-names"></a>Klargjøring av og støttede vertsnavn

Når du klargjør et e-handelsmiljø i [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), brukes boksen **Støttede vertsnavn** i vinduet Klargjøring av e-handel til å angi domener som skal knyttes til det distribuerte handelsmiljøet. Disse domenene vil være DNS-navn (Domain Name Server) for kunden, der nettsteder for e-handel vil være driftet. Hvis du går til et domene på dette stadiet, blir ikke trafikken omdirigert for domenet til Dynamics 365 Commerce. Trafikk for et domene blir bare rutet til handelsendepunktet når DNS CNAME-posten oppdateres til å bruke handelsendepunktet med domenet.

> [!NOTE]
> Du kan skrive inn flere domener i boksen **Støttede vertsnavn** ved å skille dem med semikolon.

Illustrasjonen nedenfor viser LCS for e-handelsklargjøring med boksen **Støttede vertsnavn** uthevet. 

![LCS for e-handelsklargjøring med boksen **Støttede vertsnavn** uthevet.](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Du kan opprette en serviceforespørsel for å legge til flere domener i et miljø hvis klargjøring allerede har skjedd. Hvis du vil opprette en serviceforespørsel i LCS, kan du i miljøet gå til **Kundestøtte \> Kundestøtteproblemer** og velge **Send en hendelse**.

## <a name="commerce-generated-urls"></a>Commerce-genererte URL-adresser

Når du klargjør et Dynamics 365 Commerce-e-handelsmiljø, vil Commerce generere en URL-adresse som skal virke i miljøet. Det refereres til denne URL-adressen i områdekoblingen for e-handel som vises i LCS etter at miljøet er klargjort. En Commerce-generert URL-adresse er i formatet `https://<e-commerce tenant name>.dynamics365commerce.ms`, der navnet på e-handelsleieren er navnet som er angitt i LCS for Commerce-miljøet.

Du kan også bruke vertsnavn for produksjonsområde i et sandkassemiljø. Dette alternativet er ideelt når du skal kopiere et område fra et sandkassemiljø til produksjon.

## <a name="site-setup"></a>Weboppsett

Når e-handelsmiljøet er klargjort, må du sette opp området i områdebygger for Commerce for å knytte området til den fungerende URL-adressen.

Når du konfigurerer et område i områdebyggeren for første gang, vises dialogboksen **Konfigurer området**.

Følgende illustrasjon viser dialogboksen **Konfigurer området** for et område kalt "standard" når du åpner området for første gang i områdebyggeren.

![**Dialogboksen Konfigurer område**.](./media/Domains_SetupyoursiteScreen.png)

Ved hjelp av boksen **Velg et domene** kan du knytte et av de støttede vertsnavnene som er oppgitt for området i LCS, til området i områdebyggeren.

Boksen **Bane** kan stå tom, eller du kan legge til en ekstra banestreng som vil bli gjenspeilet i den fungerende URL-adressen. Hvis du lar boksen **Bane** være tom, knyttes den grunnleggende Commerce-genererte URL-adressen til området som er definert i områdebyggeren. Baner må være unike for hvert område-/domenepar. Innenfor området og domenet som er valgt, kan bare ett område i miljøet bruke den tomme banen eller være knyttet til en unik banestreng. Alle strenger som legges til i feltet **Bane** under områdekonfigurasjonen, blir en delbane av den grunnleggende Commerce-genererte URL-adressen som brukes til å få tilgang til området i en nettleser.

> [!NOTE]
> Banen er også kjent som **samsvarsbanen** når du legger til en kanal i konfigurasjonsdelen **Områdeinnstillinger \> Kanaler** for områdebyggeren.

Hvis du for eksempel har et område i områdebyggeren som heter Fabrikam i en e-handelsleier med navnet XYZ, og hvis du konfigurerer området med en tom bane, vil du få tilgang til det publiserte områdeinnholdet i en nettleser ved å gå til den grunnleggende Commerce-genererte URL-adressen:

`https://xyz.dynamics365commerce.ms`

Hvis du har lagt til banen Fabrikam under installasjonen av det samme området, får du tilgang til det publiserte områdeinnholdet i en nettleser ved hjelp av følgende URL-adresse:

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>Sider og URL-adresser

Når området er satt opp med en bane, vil alle URL-adresser som er tilknyttet sidene i områdebyggeren, bygge videre på den fungerende URL-adressen (den Commerce-genererte URL-adressen eller den Commerce-genererte URL-adressen pluss banen) for området. Oppretter en ny URL-adresse i områdebyggeren (**URL-adresser /> + Ny**) ved å velge en side fra listen i dialogboksen **Ny URL-adresse**, og angivelse av URL-adressebanen for den siden knytter denne URL-adressen til den valgte siden. Verdien i URL-adressebanen føyes deretter til områdets fungerende URL-adresse for å få tilgang til siden, og den er merket som `./<URL path>` i URL-adresselisten på siden **URL-adresser** i områdebyggeren.

Den følgende illustrasjonen viser dialogboksen **Ny URL-adresse** i områdebyggeren med eksempel på uthevet URL-adressebane. 

![Dialogboksen **Ny URL-adresse** i områdebyggeren.](./media/Domains_PageSetup2a.png)

Den følgende illustrasjonen viser siden **URL-adresser** i områdebyggeren med eksempel på uthevet URL-adresse i listen.

![Kjør brukerflyt-alternativet policyflyt.](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Domener i områdebyggeren

Verdiene for de støttede vertsnavnene er tilgjengelige for å knyttes til et domene ved konfigurasjon av et område. Når du velger en vertsnavnverdi som domene, vil du se det valgte domenet som det refereres til i hele områdebyggeren. Dette domenet er bare en referanse i Commerce-miljøet. Direktetrafikk for det domenet vil ikke videresendes til Dynamics 365 Commerce ennå.

Hvis du har to områder som er konfigurert med to forskjellige domener, kan du legge til attributtet **?domain=** i den fungerende URL-adressen for å få tilgang til det publiserte områdeinnholdet i en nettleser.

Miljøet xyz er for eksempel klargjort, og to områder er opprettet og tilknyttet i områdebyggeren: ett med domenet `www.fabrikam.com` og det andre med domenet `www.constoso.com`. Hvert område ble konfigurert med en tom bane. Du kan deretter få tilgang til disse to områdene i en nettleser på følgende måte ved hjelp av attributtet **?domain=**:
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

Når en domenespørrestreng ikke er angitt i et miljø med flere domener som er oppgitt, bruker Commerce det første domenet du oppgav. Hvis banen Fabrikam for eksempel først ble oppgitt under konfigurasjon av området, kan URL-adressen `https://xyz.dynamics365commerce.ms` brukes til å få tilgang til det publiserte områdets innholdsområde for `www.fabrikam.com`.

## <a name="traffic-forwarding-in-production"></a>Viderekobling av trafikk i produksjon

Du kan simulere flere domener ved hjelp av parametere for domenespørringsstreng på endepunktet commerce.dynamics.com. Men når du må gå i gang med produksjon, må du videresende trafikken for det egendefinerte domenet til endepunktet `<e-commerce tenant name>.dynamics365commerce.ms`.

Endepunktet `<e-commerce tenant name>.dynamics365commerce.ms` støtter ikke egendefinerte SSL-er (Secure Sockets Layers), så du må konfigurere tilpassede domener ved hjelp av Front Door Service eller et innholdsleveringsnettverk (CDN). 

Hvis du vil konfigurere tilpassede domener ved hjelp av Front Door Service eller CDN, har du to alternativer:

- Konfigurer Front Door Service, for eksempel i Azure, til å håndtere fronttrafikk og koble til Commerce-miljøet. Dette gir bedre kontroll over behandling av domene- og sertifikatadministrasjon og mer detaljerte sikkerhetspolicyer.

- Bruk den Commerce-støttede forekomsten av Front Door Service i Azure. Dette krever koordineringshandling med Dynamics 365 Commerce-teamet for domenekontroll og henting av SSL-sertifikater for produksjonsdomenet.

> [!NOTE]
> Hvis du bruker en ekstern CDN-tjeneste eller Front Door Service, må du sørge for at forespørselen er tilknyttet Commerce-plattformen med det Commerce-leverte vertsnavnet, men med hodet X-Forwarded-Host (XFH) \<custom-domain\>. Hvis for eksempel Commerce-endepunktet er `xyz.dynamics365commerce.ms` og det egendefinerte domenet er `www.fabrikam.com`, bør vertshodet for den videresendte forespørselen være `xyz.dynamics365commerce.ms`, og XFH-hodet bør være `www.fabrikam.com`.

Hvis du vil ha informasjon om hvordan du setter opp en CDN-tjeneste direkte, kan du se [Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md).

Hvis du vil bruke den Commerce-støttede forekomsten av Front Door Service i Azure, må du opprette en serviceforespørsel for installasjon av CDN fra jobbintroduksjonsteamet til Commerce. 

- Du må angi firmanavn, produksjonsdomene, miljø-ID og navn på e-handelsleieren for produksjonen. 
- Du må bekrefte om dette er et eksisterende domene (brukes for et aktivt område) eller et nytt domene. 
- For et nytt domene kan domenekontrolleren og SSL-sertifikatet oppnås i ett trinn. 
- For et domene som betjener et eksisterende nettsted, finnes det en trinnvis prosess som kreves for å etablere domeneverifisering og SSL-sertifikatet. Denne prosessen har en servicenivåavtale på 7 virkedager før et domene blir aktivt, fordi den inneholder flere sekvensielle trinn.

Hvis du vil opprette en serviceforespørsel i LCS, kan du i miljøet gå til **Kundestøtte \> Kundestøtteproblemer** og velge **Send en hendelse**.

> [!NOTE]
> Egendefinerte domener med SSL støttes bare i produksjonsmiljøer. For ikke-produktive miljøer, for eksempel sandkasse og brukergodkjenningstesting (UAT), bruker du den Commerce-genererte URL-adressen til å få tilgang til publisert innhold i en nettleser.

## <a name="ssl-certificate-process"></a>SSL-sertifikatprosess

Når en serviceforespørsel arkiveres, vil Commerce-teamet koordinere følgende trinn med deg.

For nye domener:
- Commerce-teamet konfigurerer forekomsten av Azure Front Door (Commerce-driftet).
- Commerce-teamet vil deretter gi CNAME-posten tilgang til å henvise til ditt egendefinerte domene.
- Etter at CNAME-posten er oppdatert, vil den Commerce-driftede forekomsten av Azure Front Door kontrollere domeneeierskapet og få SSL-sertifikatet.

For eksisterende/aktive domener:
- Commerce-teamet instruerer deg om å legge til en CNAME-post for `afdverify.<custom-domain>` som du oppgir til DNS-leverandøren for domenet.
- Når den er fullført, legger Commerce-teamet til domenet i forekomsten av Azure Front Door og formidler ekstra DNS TXT-poster som skal legges til i DNS for domenet.
- Når TXT-postene er fullført, fullfører Commerce-teamet oppdateringene for Azure Front Door for domenet som skal konfigurere SSL-sertifikatet.

## <a name="apex-domains"></a>Apex-domener

Den Commerce-støttede forekomsten av Azure Front Door støtter ikke Apex-domener (rotdomener som ikke inneholder underdomener). Apex-domener krever at en IP-adresse løses, og den Commerce-støttede forekomsten av Azure Front Door finnes bare med virtuelle endepunkter. Hvis du vil bruke et Apex-domene, har du følgende alternativer:

- **Alternativ 1** – Bruk DNS-leverandøren til å omadressere Apex-domenet til et www-domene. Fabrikam.com omadresserer for eksempel til `www.fabrikam.com`, der `www.fabrikam.com` er CNAME-posten som peker til den Commerce-driftede forekomsten av Azure Front Door.

- **Alternativ 2** – Hvis DNS-leverandøren støtter ALIAS-poster, kan du peke apex-domenet til Azure Front Door endpoint-endepunktet, som sikrer at IP-endringen ved sluttpunktet gjenspeiles. Du må være vert for Azure Front Door-forekomsten selv.
  
- **Alternativ 3** – Hvis DNS-leverandøren ikke støtter ALIAS-poster, må du endre DNS-leverandøren til Azure DNS og være vert både for Azure DNS og Azure Front Door-forekomsten selv.

> [!NOTE]
> Hvis du bruker Azure Front Door, må du også konfigurere Azure DNS i det samme abonnementet. Apex-domenet som er driftet på Azure DNS, kan peke til din forekomst av Azure Front Door som en aliaspost. Dette er den eneste løsningen, ettersom Apex-domener alltid må peke til en IP-adresse.
  
Hvis du har spørsmål angående Apex-domener, kan du kontakte [Microsofts kundestøtte](https://support.microsoft.com/).

  ## <a name="additional-resources"></a>Tilleggsressurser

  [Distribuere en ny e-handelsleier](deploy-ecommerce-site.md)

  [Definere en kanal for nettbutikk](./channel-setup-online.md)

  [Opprette et e-handelsområde](create-ecommerce-site.md)

  [Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](associate-site-online-store.md)

  [Administrere robots.txt-filer](manage-robots-txt-files.md)

  [Laste opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)

  [Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

  [Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

  [Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

  [Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

  [Aktivere stedsbasert butikkregistrering](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
