---
title: Formidle veiledninger for blandet virkelighet for arbeidere i produksjonen
description: Dette emnet beskriver hvordan du integrerer produksjonsstyringsmodulen i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 727a3bc50ea55259c7260a9d060dac59473ee3c1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645150"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Formidle veiledninger for blandet virkelighet for arbeidere i produksjonen

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Arbeidere i produksjonsprosesser vil dra nytte av relevante instruksjoner som gis til riktig tid i sammenheng med arbeidet. *Instruksjoner* gjelder for flere arbeidsområder, inkludert: samling, tjeneste, operasjoner, sertifisering og sikkerhet. På tvers av alle disse kjernefunksjonene kan pågående opplæringsinstruksjoner bidra til å gi ansatte muligheten til å oppnå mer og arbeide bedre.

## <a name="introduction"></a>Innledning

Du kan gi instruksjoner på forskjellige måter. Ett effektivt system som leveres som standard, bruker [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guides kan bidra til å gi de ansatte praktisk læring. Du kan definere standardiserte prosesser med trinnvise instruksjoner som leder de ansatte til verktøyene og delene de trenger, og viser de ansatte hvordan de skal bruke disse verktøyene i virkelige situasjoner.

Du kan knytte veiledninger til ulike deler av produksjonskontrollen, blant annet:

- [Ressurser](#resources)
- [Ressursgrupper](#resource-groups)
- [Frigitte produkter](#released-products)
- [Formler](#formulas)
- [Formelversjoner](#formula-versions)
- [Stykklister](#bom)
- [Stykklisteversjoner](#bom-versions)
- [Ruter](#routes)
- [Ruteversjoner](#route-versions)
- [Ruteoperasjonsrelasjoner](#route-operation-relations)

> [!NOTE]
> Du kan også knytte veiledninger til aktivastyring. Hvis du vil ha mer informasjon om dette alternativet, kan du se [Integrere Dynamics 365 Supply Chain Management (Aktivastyring) med Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).

Når en førstelinjearbeider velger en jobb i produksjonen via Supply Chain Management, kan arbeideren se [de relevante veiledningene](#logic) på jobbkortet. Når arbeideren velger en bestemt veiledning, vises det en QR-kode for denne veiledningen på skjermen. Deretter bruker arbeideren sin HoloLens til å skanne QR-koden, som starter veiledninger og viser de nødvendige instruksjonene.

Underdelene nedenfor beskriver noen få utvalgte scenarier der selskaper på tvers av bransjer, kan se den største verdien ved bruk av veiledninger til å presentere instruksjoner for produksjon.

### <a name="assembly"></a>Samling

![Bruke veiledninger i monteringsoppgaver](media/instruction-guides-hero-assembly.png "Bruke veiledninger i serviceoppgaver")

Instruksjoner i monteringsoperasjoner viser arbeidere verktøyene og delene de trenger, og hvordan de brukes i virkelige arbeidssituasjoner.

Produksjonsledere kan opprette og tilordne veiledninger, for eksempel [produksjonsruter](routes-operations.md), [operasjonsrelasjoner](routes-operations.md#operation-relations) eller [stykklister](bill-of-material-bom.md). Arbeidere finner de relevante instruksjonene om de respektive operasjonsopplevelsen i produksjonen.

### <a name="service"></a>Service

![Bruke veiledninger i serviceoppgaver](media/instruction-guides-hero-service.png "Bruke veiledninger i serviceoppgaver")

Utstyr teknikere med veiledende instruksjoner på jobbområdet, og eliminer behovet for å planlegge ekstra besøk.

Serviceledere kan tilordne veiledninger, for eksempel for bestemte [produkter](../../commerce/product.md), som går gjennom rutiner for kvalitetsvurdering.

### <a name="quality"></a>Kvalitet

![Bruk veiledninger i kvalitetssikringsoppgaver](media/instruction-guides-hero-quality.png "Bruk veiledninger i kvalitetssikringsoppgaver")

Distribusjon av nye prosesser og sikre økt konsekvens ved å gjøre den ansattes kunnskap om til et verktøy som kan gjentas.

Kvalitetssikringsledere kan tilordne veiledninger, for eksempel for [produkter](../../commerce/product.md), som går gjennom rutiner for kvalitetsvurdering.

### <a name="certifications"></a>Sertifiseringer

![Bruk veiledninger for sertifiseringsrelaterte oppgaver](media/instruction-guides-hero-certification.png "Bruk veiledninger for sertifiseringsrelaterte oppgaver")

Sørg for at alle ansatte oppfyller høye standarder ved raskt å identifisere hvem som trenger hjelp og hvor.

### <a name="safety"></a>Sikkerhet

![Bruk veiledninger i instruksjoner for jobbsikkerhet](media/instruction-guides-hero-safety.png "Bruk veiledninger i instruksjoner for jobbsikkerhet")

Angi instruksjoner som veileder virtuelt gjennom farlige prosedyrer før det prøves i det fysiske miljøet. Med en metode for blandet virkelighet kan arbeidere oppleve farlige prosedyrer virtuelt.

Produksjonsledere kan tilby dedikerte håndteringsinstruksjoner for farlige materialhåndtering eller dedikerte håndteringsprosedyrer, ved å tilordne instruksjoner til [produktvarer](../../commerce/product.md), [ruter](routes-operations.md) og [operasjoner](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Komme i gang med instruksjoner og veiledninger

Hvis du vil aktivere instruksjoner i produksjonsprosesser, inneholder Supply Chain Management en standardintegrering med Dynamics 365 Guides. Det kreves en lisensiert og installert programforekomst av Guides for å bygge, vedlikeholde og tilordne instruksjoner for blandet virkelighet til produksjonsressurser og arbeid.

### <a name="prerequisites"></a>Forutsetninger

Hvis du vil bruke denne funksjonen, må systemet inneholde følgende:

- Dynamics 365 Supply Chain Management versjon 10.0.15 eller senere
- [Dobbel skriving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management-apper.
- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versjon 400.0.1.48 eller nyere

### <a name="turn-on-the-feature"></a>Aktivere funksjonen

Hvis du vil gjøre funksjonen tilgjengelig på systemet, må du aktivere konfigurasjonsnøklene for den. Du trenger bare å gjøre dette én gang. Hvis du vil gjøre dette, må en administrator gjøre følgende:

1. Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
1. Vis delen **Blandet virkelighet**, og merk av for **Blandet virkelighet-veiledning**.
1. Vis delen **Produksjonsstyring**, og merk av for **Produksjonsinstruksjoner**.
1. Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Konfigurere hvordan veiledninger vises i produksjonen

Hvis du vil konfigurere hvordan veiledninger skal vises i produksjonen, kan du gå til **Blandet virkelighet \> Dynamics 365 Guides \> Konfigurer integrering av veiledning**.

![Konfigurere integrering av veiledning for produksjon](media/instruction-guides-configure-integration.png "Konfigurere integrering av veiledning for produksjon")

Angi følgende felt:

- **URL-adresse for Microsoft Dataverse** – Angi URL-adressen til Microsoft Dataverse-miljøet der du oppretter Guides. Formatet er contoso.crm4.dynamics.com, der den første delen av URL-adressen vanligvis kalles etter organisasjonen (for eksempel contoso.), den andre delen er spesifikk for dataområdet i miljøet (for eksempel crm4.), og den siste delen er domenet (for eksempel dynamics.com). En måte å finne riktig URL-adresse på, er å gå til [home.dynamics.com](https://home.dynamics.com/) og deretter åpne Guides-appen. Når Guides åpnes, vil du se URL-adressen i adresselinjen i nettleseren (ta bare den primære URL-adressen, som skal ligne på det forrige eksemplet). Denne verdien brukes til å skrive adresser for veiledningene og blir kodet i QR-kodene.
- **QR-kodestørrelse** – Angi størrelsen på den gjengitte QR-koden. Vi anbefaler at du velger en størrelse som fyller meste parten av skjermen, men ikke mer. Vanligvis er *15* en god verdi.
- **Feilkorrigeringsnivå for QR-kode** – Angi detaljnivået for QR-koden. Høyere detaljnivå kan bidra til å øke kodens pålitelighet, men **QR-kodestørrelse** må være stor nok til å støtte detaljnivået som kreves av det valgte korrigeringsnivået.

> [!TIP]
> - QR-kodestørrelser som er for store for skjermen, vil ta litt lengre tid å gjengi og deretter skaleres ned for å få plass til skjermen. Dette har ingen fordeler.
> - QR-kodestørrelser som er for små, kan redusere muligheten for HoloLens til å lese koden på riktig måte i enkelte miljøer.
> - Vi anbefaler at du tester innstillingene for hver enhet som vil vise QR-koder for HoloLens-brukere. Velg innstillinger som gir deg tilstrekkelig lesbarhet i produksjonsmiljøet.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Få en oversikt over alle tilordning av veiledninger

Bruk siden **Alle veiledninger** til å vise listen over alle tilgjengelige veiledninger i organisasjonen og alle tildelinger til produksjonsprosessene og ressurser. Hvis du vil åpne den, kan du gå til **Blandet virkelighet \> Veiledninger \> Alle veiledninger**. Listen øverst viser alle tilgjengelige veiledninger, og du kan bruke feltet her til å filtrere listen. Listen nederst viser alle tilordning av veiledninger og har en verktøylinje for å behandle dem.

![Behandle veiledninger](media/instruction-guides-allguides.png "Behandle veiledninger")

Delene nedenfor beskriver objekttypene du kan tilordne veiledninger til. Hver tilordnet veiledning inneholder instruksjoner som automatisk knyttes til de respektive produksjonsjobbene og vil være tilgjengelig i produksjonen.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Knytte en veiledning til en ressurs

Legg en veiledning til en [ressurs](operations-resources.md) for å tilby veiledningen i konteksten til aktuelle produksjonsjobber.

### <a name="typical-scenario-using-resources"></a>Vanlig scenario ved bruk av ressurser

Du kan for eksempel legge til en veiledning med generell maskinsikkerhet eller håndteringsinstruksjoner i en ressurs av typen maskin. Deretter vil veiledningen være tilgjengelig i alle jobber som utføres på maskinen.

### <a name="add-a-guide-to-a-resource"></a>Legg en veiledning til en ressurs

Slik legger du en veiledning til en ressurs:

1. Gå til **Produksjonskontroll \> Oppsett \> Ressurser \> Ressursfunksjoner**.
1. Velg ressursen du vil tilordne en veiledning til, fra listeruten.
1. Vis hurtigfanen **Tilknyttede veiledninger**.
1. Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger**. Det blir lagt til en ny linje i rutenettet.
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne. Hvis du har et stort antall veiledninger, kan du filtrere listen for å finne den du leter etter.
    ![Behandle veiledninger](media/instruction-guides-allguides.png "Behandle veiledninger")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Knytte en veiledning til en ressursgruppe

Du kan legge en veiledning til [ressursgrupper](tasks/define-discrete-manufacturing-resource-group.md) hvis du bruker dem til å administrere grupper av maskiner, produksjonslinjer eller arbeidsceller.

### <a name="typical-scenarios-using-resource-groups"></a>Vanlige scenarier ved bruk av ressursgrupper

**Eksempel 1:** Du har definert en ressursgruppe for flere maskiner av samme modell. I stedet for å tilordne den veiledningen for håndteringsinstruksjoner for maskinmodellen til hver relevante ressurs, kan du i stedet tilordne veiledningen til ressursgruppen som gjenspeiler denne maskinmodellen.

**Eksempel 2:** Du har definert en ressursgruppe for en arbeidscelle som inneholder forskjellige maskiner, og du har en veiledning som inneholder generelle instruksjoner for hvordan du vedlikeholder arbeidscellen. Veiledningen gjelder alle produksjonsaktiviteter i denne arbeidscellen.

### <a name="add-a-guide-to-a-resource-group"></a>Legge en veiledning til en ressursgruppe:

Slik legger du en veiledning til en ressursgruppe:

1. Gå til **Produksjonskontroll \> Oppsett \> Ressurser \> Ressursgrupper**.
1. Velg ressursgruppen du vil tilordne en veiledning til, fra listeruten.
1. Vis hurtigfanen **Tilknyttede veiledninger**.
1. Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger**. Det blir lagt til en ny linje i rutenettet.
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne. Hvis du har et stort antall veiledninger, kan du filtrere listen for å finne den du leter etter.
    ![Legge en veiledning til en ressursgruppe](media/instruction-guides-resourcegroup.png "Legge en veiledning til en ressursgruppe")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Knytte en veiledning til et frigitt produkt

Du kan legge en veiledning til alle [frigitte produkter](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>Vanlig scenario ved bruk av frigitte produkter

Veiledninger på produktnivå kan hjelpe produksjonsarbeidere med instruksjoner som er relevante for drift av systemet eller håndtering av et bestemt frigitt produkt eller vare.

### <a name="add-a-guide-to-a-released-product"></a>Legg en veiledning til et frigitt produkt

Slik legger du en veiledning til et frigitt produkt:

1. Gå til **Behandling av produksjonsinformasjon \> Produkter \> Frigitte produkter**.
1. Åpne produktet du vil tilordne en veiledning til.
1. Åpne kategorien **Utvikling** i handlingsruten, og velg **Tilknyttede veiledninger** fra **Vis**-gruppen.
1. Siden **Tilknyttede veiledninger** åpnes for det valgte produktet.
1. Velg **Legg til** I handlingsruten for å legge til en ny linje i rutenettet. 
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne.
    ![Legge en veiledning til et frigitt produkt](media/instruction-guides-ReleasedProduct-AddGuides.png "Legge en veiledning til et frigitt produkt")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Knytte en veiledning til en formel

Du kan legge en veiledning til alle [formler](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>Vanlig scenario ved bruk av formler
  
Veiledninger på formelnivå gir produksjonsarbeidere veiledning for håndteringsinstruksjoner i konteksten til en formel eller oppskrift. Veiledninger kan også tilordnes til versjoner av en formel.

> [!NOTE]
> Du kan tilordne veiledning som er relevante for produksjonsprosesser, basert på en formel, til en rute, ruteversjon eller ruteoperasjonsrelasjoner.  

> Veiledninger kan for øyeblikket ikke knyttes til individuelle formellinjer.

### <a name="add-a-guide-to-a-formula"></a>Legg en veiledning til en formel

Slik legger du en veiledning til en formel:

1. Gå til **Behandling av produksjonsinformasjon \> Stykklister og formler \> Formler**.
1. Åpne formelen du vil tilordne en veiledning til.
1. Åpne kategorien **Topptekst** over den øverste hurtigfanen.
1. Vis hurtigfanen **Tilknyttede veiledninger**.
1. Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger**. Det blir lagt til en ny linje i rutenettet.
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne.
    ![Legge en veiledning til en formel](media/instruction-guides-Formula.png "Legge en veiledning til en formel")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Knytte en veiledning til en formelversjon

Du kan legge en veiledning til alle [formelversjoner](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Vanlig scenario ved bruk av formelversjoner

Veiledninger som er knyttet til en individuell versjon av en formel, gir produksjonsarbeidere instruksjoner som går gjennom produksjonen av denne versjonen av formeloppskriften.

> [!TIP]
> Du kan tilordne veiledning som er relevante for produksjonsprosesser, basert på denne formelversjonen, til en rute, ruteversjon eller ruteoperasjonsrelasjoner.  

> [!NOTE]
> Veiledninger kan for øyeblikket ikke knyttes til individuelle formellinjer.

### <a name="add-a-guide-to-a-formula-version"></a>Legg en veiledning til en formelversjon

Slik legger du en veiledning til en formelversjon:

1. Gå til **Behandling av produksjonsinformasjon \> Stykklister og formler \> Formler**.
1. Åpne formelen som inneholder en versjon du vil tilordne en veiledning til.
1. Åpne kategorien **Topptekst** over den øverste hurtigfanen.
1. I hurtigfanen **Formelversjoner** velger du versjonen du vil tilordne en veiledning til.
1. Velg **Tilknyttede veiledninger** på verktøylinjen **Formelversjoner**.
    ![Åpne veiledningene som er knyttet til en valgt formelversjon](media/instruction-guides-FormulaVersion.png "Åpne veiledningene som er knyttet til en valgt formelversjon")
1. Siden **Tilknyttede veiledninger** åpnes for formelversjonen.
1. Velg **Legg til** I handlingsruten for å legge til en ny linje i rutenettet. 
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne.
    ![Legge en veiledning til en formelversjon](media/instruction-guides-FormulaVersionAddGuide.png "Legge en veiledning til en formelversjon")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Knytte en veiledning til en stykkliste

Du kan legge en veiledning til alle [stykklister](bill-of-material-bom.md).

### <a name="typical-scenario-using-bills-of-materials"></a>Vanlig scenario ved bruk av stykklister

Veiledninger som er knyttet til en stykkliste, gir produksjonsarbeidere instruksjoner som forklarer klargjøring og håndtering av materiale fra en stykkliste. Veiledninger kan også tilordnes til versjoner av en stykkliste.

> [!NOTE]
> Veiledninger kan for øyeblikket ikke knyttes til individuelle stykklistelinjer.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Legg en veiledning til en stykkliste

Slik legger du en veiledning til en stykkliste:

1. Gå til **Behandling av produksjonsinformasjon \> Stykklister og formler \> Stykklister**.
1. Åpne stykklisten du vil tilordne en veiledning til.
1. Åpne kategorien **Topptekst** over den øverste hurtigfanen.
1. Vis hurtigfanen **Tilknyttede veiledninger**.
1. Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger**. Det blir lagt til en ny linje i rutenettet.
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne.
    ![Legge en veiledning til en stykkliste](media/instruction-guides-BOM.png "Legge en veiledning til en stykkliste")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Knytte en veiledning til en stykklisteversjon

Du kan legge en veiledning til alle [stykklistversjoner](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Vanlig scenario ved bruk av stykklistversjoner

Veiledninger som er knyttet til en enkelt stykklisteversjon, gir produksjonsarbeidere instruksjoner som forklarer klargjøring og håndtering av materiale for en stykklisteversjon som er forskjellig fra den generelle stykklisten eller andre versjoner av den.

> [!NOTE]
> Veiledninger kan for øyeblikket ikke knyttes til individuelle stykklistelinjer.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Legg en veiledning til en stykklisteversjon

Slik legger du en veiledning til en stykklisteversjon:

1. Gå til **Behandling av produksjonsinformasjon \> Stykklister og formler \> Stykklister**.
1. Åpne stykklisten som inneholder en versjon du vil tilordne en veiledning til.
1. Åpne kategorien **Topptekst** over den øverste hurtigfanen.
1. I hurtigfanen **Stykklisteversjoner** velger du versjonen du vil tilordne en veiledning til.
1. Velg **Tilknyttede veiledninger** på verktøylinjen **Stykklisteversjoner**.
    ![Åpne veiledningene som er knyttet til en valgt stykklisteversjon](media/instruction-guides-BOMVersion.png "Åpne veiledningene som er knyttet til en valgt stykklisteversjon")
1. Siden **Tilknyttede veiledninger** åpnes for stykklisteversjonen.
1. Velg **Legg til** I handlingsruten for å legge til en ny linje i rutenettet.
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne.
    ![Legge en veiledning til en stykklisteversjon](media/instruction-guides-BOMVersionAddGuide.png "Legge en veiledning til en stykklisteversjon")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Knytte en veiledning til en rute

Du kan legge en veiledning til alle [ruter](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>Vanlig scenario ved bruk av ruter

Ruter brukes vanligvis til å angi hvordan et bestemt frigitt produkt skal produseres basert på en stykkliste eller stykklisteversjon, og med et sett med ressurser eller ressursgrupper.

Tilordne en veiledning til en rute for å gi trinnvise instruksjoner for den respektive produksjonsprosessen.

### <a name="add-a-guide-to-a-route"></a>Legg en veiledning til en rute

Slik legger du en veiledning til en rute:

1. Gå til **Produksjonskontroll \> Alle ruter**.
1. Åpne ruten du vil tilordne en veiledning til.
1. Vis hurtigfanen **Tilknyttede veiledninger**.
1. Velg **Legg til** fra verktøylinjen **Tilknyttede veiledninger**. Det blir lagt til en ny linje i rutenettet.
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne.
    ![Legge en veiledning til en rute](media/instruction-guides-Route.png "Legge en veiledning til en rute")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Knytte en veiledning til en ruteversjon

Du kan legge en veiledning til alle [ruteversjoner](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>Vanlig scenario ved bruk av ruteversjoner

Ruteversjoner brukes vanligvis til å angi varianter av produksjonsprosesser basert på en eksisterende rute. Du kan tilordne ulike veiledninger til hver ruteversjon.

### <a name="add-a-guide-to-a-route-version"></a>Legg en veiledning til en ruteversjon

Slik legger du en veiledning til en ruteversjon:

1. Gå til **Produksjonskontroll \> Alle ruter**.
1. Åpne ruten du vil tilordne en veiledning til.
1. I hurtigfanen **Versjoner** velger du versjonen du vil tilordne en veiledning til.
1. Velg **Tilknyttede veiledninger** på verktøylinjen **Versjoner**.
    ![Åpne veiledningene som er knyttet til en valgt ruteversjon](media/instruction-guides-RouteVersion.png "Åpne veiledningene som er knyttet til en valgt ruteversjon")
1. Siden **Tilknyttede veiledninger** åpnes for stykklisteversjonen.
1. Velg **Legg til** I handlingsruten for å legge til en ny linje i rutenettet.
1. For den nye linjen bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne.
    ![Legge en veiledning til en ruteversjon](media/instruction-guides-RouteVersionAddGuide.png "Legge en veiledning til en ruteversjon")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Knytte en veiledning til en ruteoperasjonsrelasjon

Du kan legge en veiledning til alle [ruteoperasjonsrelasjoner](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>Vanlig scenario ved bruk av ruteoperasjonsrelasjoner

Operasjonsrelasjoner er den mest spesifikke måten å legge til veiledning i en produktprosess og relaterte operasjoner. Du kan angi veiledning for hver operasjon i en rute, og angi ulike veiledninger for alle typer relasjonskontekster som er angitt for en rute, for eksempel for spesifikke varer, konfigurasjoner og mye mer. Du kan også angi hvilke faser i operasjonen veiledningen gjelder for (for eksempel oppsett, kø, prosess eller transport).

> [!NOTE]
> Hvis du angir veiledninger for flere operasjonsrelasjoner for en rute, vil det bare være veiledninger fra den mest spesifikke relasjonen som vises i produksjonen for den genererte jobben.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Legg en veiledning til en ruteoperasjonsrelasjon

Slik legger du en veiledning til en ruteoperasjonsrelasjon:

1. Gå til **Produksjonskontroll \> Alle ruter**.
1. Åpne ruten du vil tilordne en veiledning til.
1. Åpne kategorien **Rute** i handlingsruten, og gå til **Vedlikehold**-gruppen og velg **Rutedetaljer**.
1. Siden **Rutedetaljer** åpnes for den valgte ruten.
1. I rutenettet øverst velger du operasjonen du vil gi veiledning for.
1. I rutenettet nederst velger du en spesifikk relasjon (eller den generelle **Alle**-relasjonen).
    ![Velg en operasjon og deretter en relasjon](media/instruction-guides-RouteOperationRelation.png "Velg en operasjon og deretter en relasjon")
1. Over rutenettet nederst åpner du kategorien **Tilknyttede veiledninger**. Kategorien ![Tilknyttede veiledninger](media/instruction-guides-RouteOperationRelation-AddGuide.png "Kategorien Tilknyttede veiledninger")
1. Velg **Legg til** fra verktøylinjen øverst i rutenettet nederst for å legge til en ny linje i rutenettet.
1. For den nye raden bruker du rullegardinlisten i **Navn**-kolonnen til å velge veiledningen du vil tilordne. I resten av raden merker du av for hver kontekst der den valgte veiledningen skal være tilgjengelig.

> [!NOTE]
> Du kan legge til én eller flere veiledninger for hvert trinn i hver operasjon.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Velg veiledninger fra kjøringsgrensesnittet for produksjon

Når en arbeider åpner en jobbliste i kjøringsgrensesnittet for produksjon, finner Supply Chain Management de relevante veiledningene for jobbene som vises. Bruk **Veiledninger**-knappen til å vise de relevante veiledningene.

![Veiledninger-knappen i kjøringsgrensesnittet for produksjon](media/instruction-guides-Shopfloor1.png "Veiledninger-knappen i kjøringsgrensesnittet for produksjon")

Deretter må du ta på en HoloLens og gå til den aktuelle veiledningen ved å se på QR-koden og aktivere den aktuelle veiledningen.

![QR-kode for å gå til veiledninger ved hjelp av en HoloLens](media/instruction-guides-Shopfloor2.png "QR-kode for å gå til veiledninger ved hjelp av en HoloLens")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Løse logikken for valg av veiledninger

Du kan legge til veiledninger for følgende produksjonsdata:

- [Ressurser](#resources)
- [Ressursgrupper](#resource-groups)
- [Frigitte produkter](#released-products)
- [Formler](#formulas)
- [Formelversjoner](#formula-versions)
- [Stykklister](#bom)
- [Stykklisteversjoner](#bom-versions)
- [Ruter](#routes)
- [Ruteversjoner](#route-versions)
- [Ruteoperasjonsrelasjoner](#route-operation-relations)

Når Supply Chain Management genererer jobbene for produksjonen, vil det samle de relevante veiledningene fra disse kildene. Legg merke til de viktigste reglene nedenfor.

- Hvis du knytter en stykklisteversjon eller formelversjon til en rute eller produksjonsordre, vil eventuelle veiledninger som er knyttet til denne versjonen, og også veiledningene som er knyttet til den overordnede stykklisten eller formelen til denne versjonen, vises for jobben.
- Hvis du knytter en ruteversjon eller formelversjon til en rute eller produksjonsordre, vil eventuelle veiledninger som er knyttet til denne versjonen, og også veiledningene som er knyttet til den overordnede ruten eller formelen til denne versjonen, vises for jobben.
- Hvis du definerer flere ruteoperasjonsrelasjoner som omfatter *Alle*-relasjonen og tilordner veiledninger til disse, vil bare veiledningene fra den mest spesifikke relasjonen vises for jobben.  

![Diagram for å løse de relevante veiledningene](media/instruction-guides-Resolve.png "Diagram for å løse de relevante veiledningene")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]