---
title: Definere dekningsregler for varer
description: Denne prosedyren viser hvordan du oppretter dekningsregler og overstyrer dekningsinnstillinger for en bestemt vare. Den viser også hvordan du kan angi standard lagerinnstillinger.
author: ChristianRytt
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15b0ad9faf2bcac25dec01a7ab44f804ad2345cd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567229"
---
# <a name="define-coverage-rules-for-items"></a>Definere dekningsregler for varer

[!include [banner](../../includes/banner.md)]

Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren viser hvordan du oppretter dekningsregler og overstyrer dekningsinnstillinger for en bestemt vare. Den viser også hvordan du kan angi standard lagerinnstillinger.

## <a name="create-a-coverage-group"></a>Opprette en dekningsgruppe

Opprett en dekningsgruppe ved å gjøre følgende:

1. Gå til **Navigasjonsrute > Moduler > Hovedplanlegging > Oppsett > Dekningsgrupper**.
1. Velg **Ny**.
1. Skriv inn en verdi i **Dekningsgruppe**-feltet.
1. Skriv inn en verdi i **Navn**-feltet.
1. Skriv inn en verdi i feltet **Kalender**. Velg kalenderen som hovedplanlegging bruker til å opprette forslag for etterfylling for varer i denne gruppen.  
1. I **Dekningskode**-feltet velger du et alternativ. Velg "Krav" for denne prosedyren.  
1. Angi 90 i feltet **Dekningshorisont (dager)**. For varer i denne gruppen oppretter hovedplanleggingen etterfyllingsforslag for opptil 90 dager i fremtiden.  
1. Angi 1 i **Negative dager**-feltet.
1. Angi 1 i **Positive dager**-feltet.
1. Vis eller skjul delen **Annet**.
1. Under delen **Sikkerhetsmarginer i dager** i feltet **RPåslag dager lagt til i behovsdato** angir du 1. Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 16. mai.
1. Angi 1 i feltet **Sikkerhetsdager trukket fra behovsdato**. Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 14. mai.  
1. Angi 1 i feltet **Respittid, gjenbestilling lagt til vareleveringstiden**.
1. Velg **Lagre**.

## <a name="create-a-new-product"></a>Opprett et nytt produkt

Opprett er nytt produkt ved å gjøre følgende:

1. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.
1. Velg **Ny**.
1. Skriv inn en verdi i feltet **Produktnummer**.
1. Skriv inn en verdi i feltet **Produktnavn**.
1. Klikk på rullegardinknappen i feltet **Varemodellgruppe** for å åpne oppslaget.
1. Finn og velg ønsket post i listen.
1. Velg koblingen i den valgte raden i listen.
1. Klikk på rullegardinknappen i feltet **Varegruppe** for å åpne oppslaget.
1. Finn og velg ønsket post i listen.
1. Velg koblingen i den valgte raden i listen.
1. Klikk på rullegardinknappen i **Lagringsdimensjonsgruppe**-feltet for å åpne oppslaget.
1. Finn og velg ønsket post i listen.
1. Velg koblingen i den valgte raden i listen.
1. Klikk på rullegardinknappen i **Sporingsdimensjonsgruppe**-feltet for å åpne oppslaget.
1. Finn og velg ønsket post i listen.
1. Velg koblingen i den valgte raden i listen.
1. Velg **OK**.

## <a name="set-up-default-order-settings"></a>Konfigurere standard ordreinnstillinger

Definer standard ordreinnstillinger ved å gjøre følgende:

1. Velg **Plan** i **handlingsruten**.
1. Under **Ordreinnstillinger** klikker du **Standard ordreinnstillinger**.
1. Under **Bestilling**, i feltet **Standardområde** skriver du inn området som brukes som standard når bestillinger opprettes.
1. Skriv inn området der varen lagres, i feltet **Standardlager**.
1. Vis eller skjul delen **Beholdning**.
1. I feltet **Multippel** skriver du inn 10.
1. I feltet **Minimumsordre** skriver du inn 10.
1. I feltet **Maks. ordreantall** skriver du inn 100.
1. I feltet **Standard ordreantall** skriver du inn 10.
1. Angi et tall i feltet **Leveringstid for innkjøp**.
1. Merk av eller fjern merket i avmerkingsboksen **Virkedager**.
1. Velg **Lagre**.
1. Velg Bestilling i feltet **Standard ordretype**.
1. Velg **Lagre**.
1. Lukk siden. Lukk siden Standard ordreinnstillinger.  

## <a name="add-an-item-to-a-coverage-group"></a>Legge til en vare i en dekningsgruppe

Legg til en vare i en dekningsgruppe ved å gjøre følgende:

1. Vis eller skjul delen **Plan**.
1. Klikk på rullegardinknappen i **Dekningsgruppe**-feltet for å åpne oppslaget.
1. I listen finner du **dekningsgruppen** du har opprettet.
1. Velg koblingen i den valgte raden i listen.

## <a name="create-item-coverage-rules"></a>Opprette varedekningsregler

Opprett varedekningsregler ved å gjøre følgende:

1. Velg **Plan** i **handlingsruten**.
1. Under **Dekning** klikker du **Varedekning**.
1. Velg **Ny**.
1. Velg fanen **Generelt**.
1. Merk av i boksen i overskriften til **Overstyr dekningsgruppeinnstillinger**.
1. Angi 60 i feltet **Dekningshorisont (dager)**. Selv om varene i dekningsgruppen Krav er planlagt 90 dager frem i tid, blir elementet planlagt 60 dager frem i tid.  
1. Angi 2 i **Negative dager**-feltet.
1. Angi 2 i **Positive dager**-feltet.
1. Klikk på fanen **Leveringstid**.
1. Merk av i boksen i overskriften for **Innkjøp**.
1. Angi 5 i feltet **Innkjøpstid**.
1. Velg **Lagre**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]