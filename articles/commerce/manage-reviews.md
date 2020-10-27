---
title: Administrere vurderinger og anmeldelser
description: Dette emnet forklarer hvordan du behandler vurderinger og omtaler i Microsoft Dynamics 365 Commerce-områdebygger.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974012"
---
# <a name="manage-ratings-and-reviews"></a>Administrere vurderinger og anmeldelser

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du behandler vurderinger og omtaler i Microsoft Dynamics 365 Commerce-områdebygger.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce bruker Microsoft Azure Cognitive Service til å automatisk moderere vurderingstekst ved å fjerne upassende ord. I tillegg kan moderatorer bruke Dynamics 365 Commerce-områdebygger til å implementere følgende manuelle oppgaver:

- Sensurere omtaler ved å svare på dem eller fjerne dem.
- Slette omtalene til en kunde på en kundens forespørsel.
- Masseimportere vurderings- og omtaledata for alle produkter i en Microsoft Power BI-mal, slik at tendenser for vurderinger og omtaler kan analyseres.

## <a name="read-a-review"></a>Lese en omtale 

Gjør følgende for å lese en omtale i Commerce-områdebygger:

1. Gå til **Hjem \> Omtaler \> Sensur** .
1. Bruk søkefeltet øverst til høyre på siden for å filtrere omtalene som vises etter produkt-ID, produktnavn eller omtaletekst.

Flere filtre gjør at du kan begrense omtalene etter periode, rangering, kanal eller betydning (fjernet, svart på eller rapportert).

![Startside for sensur](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Svare på en omtale 

Noen ganger kan kunder som kjøpte et produkt, uttrykke tilfredshet eller misnøye, eller de forstår ikke hvordan de kan bruke produktet. Som moderator kan du legge inn et svar på en omtale. Dette svaret vises sammen med omtalen på området. 

Gjør følgende for å svare på en omtale i Commerce-områdebygger:

1. Gå til **Hjem \> Omtaler \> Sensur** .
1. Finn og velg omtalen som krever et svar.
1. Velg **Legg til et svar** i egenskapsruten til høyre.
1. Skriv inn svarteksten og navnet som skal vises for svareren. Standard svarnavn er **Moderator** .
1. Når du er ferdig, velg du **Legg inn svar** .

![Svare på en omtale](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Fjerne en omtale 

Noen ganger er det en forretningsmessig begrunnelse for at moderatorer fjerner omtaler fra kunder. 

Gjør følgende for å fjerne en omtale i Commerce-områdebygger:

1. Gå til **Hjem \> Omtaler \> Sensur** .
1. Finn og velg gjennomgangen som må fjernes.
1. Velg en årsak til fjerningen under **Fjern omtale** , og velg deretter **Fjern** .
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Slette omtalene til en kunde på en kundens forespørsel 

Noen ganger vil kundene ha sine data for vurderinger og omtaler slettet for godt fra et webområde for e-handel. En moderator som mottar en forespørsel om fjerning fra en kunde, kan fjerne kundens data ved hjelp av funksjonen for omtalesletting. Hvis du vil finne og slette en kundes data, krever moderator e-postadressen som kunden brukte til å logge på og gi omtaler. 

Gjør følgende for å finne og slette kundedata i Commerce-områdebygger:

1. Gå til **Hjem \> Omtaler \> Slett** .
1. I boksen **Søk etter brukere etter e-postadresse** angir du kundens e-postadresse, og deretter velger du **Søk** .
1. Hvis kunden har omtaleaktivitet (for eksempel innsending av omtaler, stemmer om nyttigheten til en annen kundes omtale eller merknader om en annen kundes omtale), vises resultatene. For hvert element er det en **Slett** -knapp.
1. Velg **Slett** for hvert element som må slettes. Velg **Ja** når du blir bedt om å bekrefte. 
    
![Slette kundedata](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Det kan ta opptil sju dager før data blir fjernet fra systemet. Moderatorer bør varsle kunder om denne forsinkelsen.
> - Hvis kundene har endret navnet sitt i kontoinnstillingene, kan flere elementer vises i søkeresultatene. I dette tilfellet må moderatoren velge **Slett** for hvert element for å slette kundens data fullstendig. 

## <a name="download-ratings-and-reviews-data"></a>Laste ned data om vurderinger og omtaler

Commerce-områdebygger lar moderatorer å importere vurderinger og omtaler i gruppe, slik at de kan analysere trender. En Power BI-mal som inneholder grunnleggende mål, er tilgjengelig. Moderatorer kan bruke denne malen til å koble sammen masseimporterte data og vise et instrumentbord. De trenger ikke opprette et egendefinert instrumentbord. Moderatorer kan tilpasse Power BI-malen slik at den dekker sine spesielle behov. 

Gjør følgende for å laste ned vurderinger og omtaler i Commerce-områdebygger:

1. Gå til **Hjem \> Omtaler \> Rapportering** .
1. Velg **Last ned omtaledata** for å laste ned data om vurderinger og omtaler i CSV-format (kommadelte verdier).

## <a name="view-ratings-and-reviews-trends"></a>Vise trenger for vurderinger og omtaler

Moderatorer kan laste ned Power BI-malen, slik at de kan vise tendenser på et instrumentbord.

Gjør følgende for å vise trender for vurderinger og omtaler i Commerce-områdebygger:

1. Gå til **Hjem \> Omtaler \> Rapportering** .
1. Velg **PowerBI-mal** for å laste ned malen.

    ![Last ned Power BI-malen](media/rnr-moderation-reports.png) 

1. Åpne den nedlastede malen ved hjelp av Power BI-appen. Lukk dialogboksen **Tilgang til webinnhold** som vises, og lukk deretter "Oppdater"-feilmeldingen som vises.
1. Gå til **Hjem** , velg **Rediger spørringer** , og velg deretter **Innstillinger for datakilde** .
1. Velg **Endre kilde** i dialogboksen **Innstillinger for datakilde** .
1. I feltet **URL** angir du banen til omtaledataene du lastet ned i forrige prosedyre (for eksempel **c:\\reviews\\ReviewsData.csv** ).

    ![URL-felt i dialogboks for kommadelte verdier](media/rnr-powerbi-datasource-settings.png) 

1. Velg **OK** , og velg deretter **Bruk endringer** . Det vil ta ett til to minutter å bruke endringene i datakilden.
1. Velg **Trendark** for å vise trender for vurderinger og omtaler.

    ![Trender for vurderinger og omtaler](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Velge å bruke vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)
