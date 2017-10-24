---
title: "Innkjøpspolicyer"
description: "Denne artikkelen inneholder informasjon om innkjøpspolicyer. En innkjøpspolicy er en samling av regler som styrer rekvisisjonsprosessen. Innkjøpspolicyer hjelpe innkjøpsadministratorer med å implementere sin innkjøpsstrategi ved å opprette en policystruktur som er i samsvar med organisasjonens krav til strategiske innkjøp."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 11614
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 494eb9af2b293c6dbf22d80825e50dc80987c3ea
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="purchasing-policies"></a>Innkjøpspolicyer

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om innkjøpspolicyer. En innkjøpspolicy er en samling av regler som styrer rekvisisjonsprosessen. Innkjøpspolicyer hjelpe innkjøpsadministratorer med å implementere sin innkjøpsstrategi ved å opprette en policystruktur som er i samsvar med organisasjonens krav til strategiske innkjøp.

En innkjøpspolicy består av et sett med policyregler. Når du definerer en policyregel, velger du først en regeltype. Du oppretter deretter en regel for regeltypen ved å definere innstillingene, startdato og sluttdato for regelen.  

For eksempel oppretter en administrator en policy, velger regeltypen **Katalogpolicy** og legger deretter til en katalogpolicyregel i policyen. Denne katalogpolicyregel angir at katalogen Adventure må brukes til interne innkjøp. Når innkjøpspolicyen er knyttet til en bestemt organisasjon, ser ansatte i denne organisasjonen Adventure-katalogen ved oppretting av rekvisisjoner.

## <a name="assigning-policies-to-organizations"></a>Tilordne policyer til organisasjoner
Før en policy kan tre i kraft, må den være tilknyttet en organisasjon. Innkjøpspolicyer knyttes til hierarkiformålet **Internkontroll av innkjøp**. Innkjøpspolicyer gjelder derfor bare for organisasjoner i hierarkier som har hierarkiformålet **Internkontroll av innkjøp**. Du kan også velge organisasjoner fra en liste over juridiske enheter i tabellen CompanyInfo. Disse juridiske enheter er angitt i policyrammeverket som "Firmaer."

## <a name="determining-which-rule-to-apply"></a>Bestemmer hvilke regel som skal gjelde
Flere regler kan påvirke brukerne i en organisasjon, avhengig av hvordan du konfigurerer innkjøpspolicyer. Eksemplene nedenfor viser forskjellige måter du kan konfigurere innkjøpspolicyer på og angir hvordan policyer brukes når det oppstår en transaksjon.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Eksempel 1: Enkel konfigurasjon av innkjøpspolicy

Organisasjoner som er små og mindre komplekse kan definere innkjøpspolicyer etter juridisk enhet, og kan bare bruke organisasjonshierarkiet Firmaer.  

For Fabrikam, en liten bedrift, varierer innkjøpskravene lite på tvers av organisasjonen. Innkjøpsreglene varierer bare mellom organisasjonens juridiske enheter. For eksempel kjøper ansatte i Fabrikam Canada og ansatte i Fabrikam USA varer og tjenester fra ulike kataloger og forskjellige leverandører. Dermed angir Fabrikam dets innkjøpspolicyer på nivået for juridisk enhet.  

Fabrikam oppretter to innkjøpspolicyer. A-policyen brukes på den juridiske enheten for USA, 1111. B-policyen brukes på den juridiske enheten for Canada, 2222. Når en ansatt i den juridiske enheten 1111 oppretter en innkjøpsrekvisisjon, avledes policyreglene fra policyen A. Produktkatalogen som den ansatte ser, er for eksempel angitt i katalogpolicyregel for policyen A.  

Når en ansatt i den juridiske enheten 2222 oppretter en innkjøpsrekvisisjon, avledes policyreglene fra policyen B.  

**Merk:** Hvis en ansatt for juridisk enhet 1111 kjøper en vare på vegne av en ansatt for juridisk enhet 2222, brukes policyreglene som er angitt for den juridiske enheten 2222 (det vil si policyreglene fra policyen B).

### <a name="example-2-complex-purchasing-policy-configuration"></a>Eksempel 2: Kompleks konfigurasjon av innkjøpspolicy

Alle innkjøpsregler ble definert i et enkelt organisasjonshierarki, organisasjonshierarkiet Firmaer, i det forrige eksemplet. En kompleks organisasjon kan imidlertid definere policyer for flere organisasjonshierarkier.  


Contoso er et stort firma som krever komplekse innkjøpsregler for å styre rekvisisjonsprosessen. Contoso har definert regler for to ulike organisasjonshierarkier: Avdeling og Global innkjøpskontroll.  

Policyen 123 er definert for organisasjonshierarkiet Avdeling for Salg Storbritannia – salgsavdeling. I policyen 123 angir kontrollregelen for innkjøpsrekvisisjon at det må iverksettes begrensninger for minimum ordreantall. I denne regelen er alternativet **Benytt begrensninger for minimumsbestillingsantall** valgt.  

Policyen 456 er definert for organisasjonshierarkiet Global innkjøpskontroll for salgs- og markedsføringsavdelingen. I policyen 456 angir ikke kontrollregelen for innkjøpsrekvisisjon at det må iverksettes begrensninger for minimum ordreantall. I denne regelen er valget av alternativet **Benytt begrensninger for minimumsbestillingsantall** opphevet.  

Erik arbeider i Salg Storbritannia – salgsavdeling i Contoso Storbritannia kontoret. Policyene for både organisasjonshierarkiene Avdeling og Global innkjøpskontroll gjelder for hans avdeling. Når Erik oppretter en innkjøpsrekvisisjon, må systemet bestemme hvilken policy som skal brukes. Systemansvarlig konfigurerer innkjøpspolicyparametere for å angi at innkjøpspolicyer må brukes i den følgende prioritetsrekkefølgen:

1.  Global innkjøpskontroll
2.  Avdeling
3.  Firmaer

Derfor gjelder policyen 456 for innkjøpsrekvisisjonen som Erik oppretter, og det kreves ingen min. bestillingsantall for innkjøpsrekvisisjonen.

## <a name="policy-rules"></a>Policyregler
### <a name="catalog-policy-rule"></a>Policyregel for katalog

Katalogpolicyregelen bestemmer hvilken innkjøpskatalog brukere ser når de oppretter innkjøpsrekvisisjoner. Hvis en bruker har fått tillatelse til å bestille produkter på vegne av en annen bruker, bruker rekvisisjonen katalogpolicyregelen som er definert for bestillerens juridiske enhet og driftsenhet, til å bestemme hvilken katalog som skal vises. Før du kan definere en katalogpolicyregel, må du opprette og publisere en innkjøpskatalog.

### <a name="category-access-policy-rule"></a>Policyregel for kategoritilgang

Policyregelen for kategoritilgang bestemmer hvilke kategorier brukere har tilgang til når de oppretter innkjøpsrekvisisjoner. Hvis ingen regler er angitt, kan alle innkjøpskategoriene legges til i innkjøpsrekvisisjonen.

1.  Velg alternativet **Inkluder overordnet regel** for å bruke policyregelen for kategoritilgang for den overordnede organisasjonen for kategorien.
2.  Velg kategoriene som regelen gjelder for, i ruten **Tilgjengelige kategorier**. Når du velger en kategori, blir alle kategorier som er høyere i hierarkiet, også lagt til i **Valgte kategorier**-listen.
3.  Velg alternativet **Inkluder underkategorier** for å bruke regelen for alle underkategorier for den valgt innkjøpskategorien.

### <a name="category-policy-rule"></a>Kategoripolicyregel

Kategoripolicyregelen definerer hvordan brukere kan velge leverandører for hver kategori. Den definerer også krav for mottak og fakturering av prosesser.

### <a name="re-approval-rule-for-purchase-orders"></a>Regel for ny godkjenning for bestillinger

Regelen for ny godkjenning er en valgfri regel som definerer kriteriene for å kreve ny godkjenning når en bestilling endres. De valgte feltene evalueres i arbeidsflyten for bestillingen når vilkåret Krever ny godkjenning av bestilling er definert i arbeidsflyten.

> [!NOTE]
> Regnskapsdistribusjonen tilbakestilles alltid når en godkjent bestilling med endringsadministrasjon aktivert, endres. Derfor bør du være oppmerksom på at hvis du vil unngå ny godkjenning av en bestilling når bestemte felt er endret, skal IKKE feltet Accounting distribution.changed tas med som et merket felt for ny godkjenning. 

### <a name="purchase-requisition-rfq-rule"></a>Regel for tilbudsforespørsel for innkjøpsrekvisisjon

Regelen for tilbudsforespørsel for innkjøpsrekvisisjon definerer kriterier for å kreve en tilbudsforespørsel for en innkjøpsrekvisisjonslinje. Hvis en linje oppfyller betingelsene, vises stempelet "uformell Tilbudsforespørsel" eller "formell Tilbudsforespørsel" i rekvisisjonslinjen.

### <a name="purchase-requisition-control-rule"></a>Kontrollregel for innkjøpsrekvisisjon

Kontrollregel for innkjøpsrekvisisjon er en valgfri regel. Når du oppretter reglene av denne typen, kan du angi alternativer i forskjellige kategorier:

-   I **Oppstart av arbeidsflyt** kategorien kan du konfigurere feltene som må registreres i rekvisisjonslinjen for rekvisisjonen som skal sendes til godkjenning når rekvisisjonsformålet er **Forbruk**.
-   I kategorien **Ordreantall** kan du konfigurere feltene som er nødvendige på innkjøpsrekvisisjonen i visse tilfeller. Du kan også bruke ordreantall.
-   I kategorien **Datoer** kan du konfigurere om Regnskapsdatoen er lik ønsket dato
-   I kategorien **Adresse** kan du definere om brukeren har tillatelse til å opprette nye adresser i systemet som skal gjelde for innkjøpsrekvisisjonen.

### <a name="requisition-purpose-rule"></a>Regel for rekvisisjonsformål

Rekvisisjonsformålsregelen er en valgfri regel som bestemmer typen rekvisisjonsformål som er tillatt for en bestemt juridisk enhet. Med mindre et annet formål er angitt i denne regelen har innkjøpsrekvisisjonene automatisk formålet **Forbruk** når de opprettes.

### <a name="replenishment-category-access-policy-rule"></a>Policyregel for tilgang til etterfyllingskategori

Policyregel for tilgang til etterfyllingskategori er en valgfri regel som bestemmer produktene som er tilgjengelige for å dekke rekvisisjonsbehovet for en bestemt juridisk enhet når rekvisisjonsformålet er **etterfylling**.

### <a name="replenishment-control-rule"></a>Kontrollregel for etterfylling

Kontrollregel for etterfylling er en valgfri regel som definerer feltene som må angis på rekvisisjonslinjen for rekvisisjonen som skal sendes til godkjenning når rekvisisjonsformålet er **etterfylling**.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Konsolideringsregel for bestillingsopprettelse og behov

Konsolideringsregel for bestillingsopprettelse og behov definerer policyreglene skal brukes når en bestilling genereres fra en godkjent innkjøpsrekvisisjon. Når du oppretter reglene av denne typen, kan du angi alternativer i forskjellige kategorier:

-   I kategorien **Bestillingsdeling** kan du definere vilkår for å dele innkjøpsrekvisisjonslinjene inn i separate bestillinger.
-   I kategorien **Pris-/rabattoverføring** kan du definere når du skal omberegne prisavtalen når en bestilling opprettes:
    -   **Bare hvis det ikke finnes forretningsavtale** – Priser og rabatter overføres fra innkjøpsrekvisisjonen bare hvis det ikke finnes noen aktuell forretningsavtale eller basispris. Hvis det finnes en forretningsavtale eller basispris for varen eller leverandøren, beregnes prisene og rabattene på nytt basert på forretningsavtalen eller basisprisen og brukes i bestillingen. Dette er standardvirkemåten hvis ikke annet er angitt.
    -   **Alltid** – Priser og rabatter overføres alltid fra innkjøpsrekvisisjonen.

    Du kan også tillate at bestilleren endrer metoden for pris- og rabattoverføring for enkeltlinjer i innkjøpsrekvisisjonen, uavengig av regelen for overføring av priser/tabatter som er definert. Velg alternativet **Tillat manuell overstyring av innkjøpsrekvisisjonslinje** hvis du vil aktivere denne funksjonen.
-   I kategorien **Overføring av varebeskrivelse** kan du overføre varebeskrivelsen fra rekvisisjonen når den kommer fra en Tilbudsforespørsel.
-   I kategorien **Pristoleranse** kan du definere regler for å rute godkjente innkjøpsrekvisisjoner tilbake via gjennomgangsprosessen, når prisen på en vare i en innkjøpskatalog øker. Angi deretter det maksimale beløpet som nettobeløpet for en linjevare i en innkjøpsrekvisisjon kan øke, fra tidspunktet innkjøpsrekvisisjonen godkjennes til tidspunktet bestillingen opprettes. Nettobeløpet beregnes ved å bruke følgende formel: (\[Antall × (enhetspris-rabatt) ÷ prisenhet\] + innkjøpstillegg) × (100-rabattprosent) ÷ 100. Innkjøpsrekvisisjonslinjer som overskrider pristoleransen du har angitt, blir låst for manuell behandling. Reglene du konfigurerer i kategorien **Feilbehandling**, bestemmer hvordan innkjøpsrekvisisjonslinjene behandles.
-   I kategorien **Feilbehandling** kan du konfigurere behandlingsregelen som skal brukes for en innkjøpsrekvisisjon hvis den ikke kan valideres når bestillingen opprettes, på grunn av en leverandørfeil eller en pristoleransefeil. Velg ett av følgende alternativer:
    -   **Ingen handling** – innkjøpsrekvisisjonslinjene forblir på siden **Frigi godkjente innkjøpsrekvisisjoner**. Statusen for innkjøpsrekvisisjonslinjene blir værende **Godkjent**. Feilene må imidlertid løses før en bestilling kan genereres for innkjøpsrekvisisjonslinjene.
    -   **Avbryt innkjøpsrekvisisjonslinjen** – innkjøpsrekvisisjonslinjene avbrytes. Bestilleren kan opprette en ny innkjøpsrekvisisjon for de annullerte linjene hvis han eller hun fortsatt ønsker å rekvirere linjevarene.
    -   **Opprett en ny innkjøpsrekvisisjonslinje** – innkjøpsrekvisisjonslinjene avbrytes. Deretter genereres nye innkjøpsrekvisisjoner som bare inneholder innkjøpsrekvisisjonslinjene som ikke ble validert. De nye innkjøpsrekvisisjonene som er generert, har statusen **Utkast**. Disse innkjøpsrekvisisjonene kan sendes inn på nytt for gjennomgang etter at valideringsfeilene er løst. Klargjøreren for innkjøpsrekvisisjonslinjene blir varslet om at linjene er annullert, og at nye innkjøpsrekvisisjoner ble generert for de mislykkede innkjøpsrekvisisjonslinjene.
-   I kategorien **Manuell bestillingsopprettelse** kan du definere parameterne som bestemmer om en innkjøpsrekvisisjon må behandles manuelt, eller om den kan konverteres automatisk til en bestilling. Parameterne kan gjelde for interne katalogvarer, eksterne katalogvarer eller ikke-katalogvarer. Velg ett av følgende alternativer:
    -   **Opprett bestillinger manuelt** – manuelt opprette bestillinger for alle innkjøpsrekvisisjoner.
    -   **Opprett automatisk bestillinger** – opprette bestillinger automatisk for alle godkjente innkjøpsrekvisisjoner. Ingen innkjøpsrekvisisjoner er låst for manuell oppretting av bestillinger.
    -   **Opprett bestillinger automatisk, bortsett fra under disse betingelsene** – manuelt opprette bestillinger for innkjøpsrekvisisjoner som oppfyller vilkårene du definerer. Alle andre innkjøpsrekvisisjoner som er godkjent, konverteres automatisk til bestillinger. Hvis du velger **Opprett bestillinger automatisk, bortsett fra under disse betingelsene**, kan du legge til innkjøpskategorier og leverandører for å angi hvilke godkjente innkjøpsrekvisisjonslinjer som skal sperres for manuell behandling. Dette alternativet kan gjelde for interne katalogvarer, eksterne katalogvarer og ikke-katalogvarer. Når du velger en innkjøpskategori, blir alle underkategorier for denne innkjøpskategorien også valgt. Velg alternativet **Alle** for en bestemt type innkjøpsrekvisisjonslinje for å låse alle linjer av denne typen for manuell behandling.

    Hvis du vil at bestillinger skal genereres automatisk fra godkjente innkjøpsrekvisisjoner når den satsvise jobben for bestillingsgenerering kjøres, velger du alternativet **Kjør automatisk bestillingsopprettelse som en satsvis jobb**. Dette alternativet gjelder bare for innkjøpsrekvisisjoner som ikke krever manuell behandling. Ved å kjøre den automatiske genereringen av bestillinger som en satsvis jobb kan du planlegge denne aktiviteten på et tidspunkt når det er mindre belastning på ressursene. Hvis alternativet **Forskuddsbetaling kreves** er valgt på innkjøpsrekvisisjonslinjene, kan du merke av for **Når rekvisisjonen er konfigurert for forskuddsbetaling** hvis du vil låse godkjente innkjøpsrekvisisjonslinjer for manuell behandling. Innkjøpsrekvisisjoner som er låst for manuell behandling, kan filtreres slik at du kan vise bare innkjøpsrekvisisjonslinjene som krever forskuddsbetaling.
-   I kategorien **Behovskonsolidering** kan du definere parameterne som bestemmer om innkjøpsrekvisisjoner som behandles manuelt, kan vurderes for konsolidering av innkjøpsrekvisisjoner. Parameterne kan gjelde for interne katalogvarer, eksterne katalogvarer eller ikke-katalogvarer. Velg ett av følgende alternativer:
    -   **Ikke tillat etterspørselskonsolidering** – ingen godkjente innkjøpsrekvisisjonslinjer er kvalifisert for behovskonsolidering. Dette alternativet er valgt som standard og gjelder bare for innkjøpsrekvisisjonslinjer som krever manuell behandling ved oppretting av bestillinger.
    -   **Tillat alltid etterspørselskonsolidering** – alle godkjente innkjøpsrekvisisjonslinjer er kvalifisert for behovskonsolidering. **Obs!** Hvis du velger alternativet **Tillat alltid etterspørselskonsolidering** i kategorien **Behovskonsolidering**, men du velger alternativet **Opprett automatisk bestillinger** i kategorien **Manuell bestillingsopprettelse**, blir alle innkjøpsrekvisisjoner låst for manuell behandling.
    -   **Tillat etterspørselskonsolidering under disse betingelsene** – Definer kriteriene som bestemmer om godkjente innkjøpsrekvisisjonslinjer er kvalifisert for behovskonsolidering. For hver type innkjøpsrekvisisjonslinje kan du angi kriteriene etter innkjøpskategori og leverandør. Hvis du velger **Tillat etterspørselskonsolidering under disse betingelsene**, kan du angi kriteriene etter innkjøpskategori og leverandør for hver type innkjøpsrekvisisjonslinje. Når du velger en innkjøpskategori, blir alle underkategorier for denne innkjøpskategorien også valgt. Hvis du velger **Alle** for en bestemt linjetype, er alle innkjøpsrekvisisjonslinjene for denne linjetypen berettiget til behovskonsolidering.





