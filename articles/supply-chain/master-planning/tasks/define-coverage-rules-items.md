---
title: Definere dekningsregler for varer
description: Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c156ae4a8a19a428378581a0d5c7dc01d86b5ec7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999887"
---
# <a name="define-coverage-rules-for-items"></a>Definere dekningsregler for varer

[!include [banner](../../includes/banner.md)]

Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren viser hvordan du oppretter dekningsregler og overstyrer dekningsinnstillinger for en bestemt vare. Den viser også hvordan du kan angi standard lagerinnstillinger.


## <a name="create-a-coverage-group"></a>Opprette en dekningsgruppe
1. Gå til **Navigasjonsrute > Moduler > Hovedplanlegging > Oppsett > Dekningsgrupper**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Dekningsgruppe**-feltet.
4. Skriv inn en verdi i **Navn**-feltet.
5. Skriv inn en verdi i feltet **Kalender**. Velg kalenderen som hovedplanlegging bruker til å opprette forslag for etterfylling for varer i denne gruppen.  
6. I **Dekningskode**-feltet velger du et alternativ. Velg "Krav" for denne prosedyren.  
7. Angi 90 i feltet **Dekningshorisont (dager)**. For varer i denne gruppen oppretter hovedplanleggingen etterfyllingsforslag for opptil 90 dager i fremtiden.  
8. Angi 1 i **Negative dager**-feltet.
9. Angi 1 i **Positive dager**-feltet.
10. Vis eller skjul delen **Annet**.
11. Under delen **Sikkerhetsmarginer i dager** i feltet **RPåslag dager lagt til i behovsdato** angir du 1. Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 16. mai.  
12. Angi 1 i feltet **Sikkerhetsdager trukket fra behovsdato**. Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 14. mai.  
13. Angi 1 i feltet **Respittid, gjenbestilling lagt til vareleveringstiden**.
14. Klikk på **Lagre**.

## <a name="create-a-new-product"></a>Opprette et nytt produkt
1. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Produktnummer**.
4. Skriv inn en verdi i feltet **Produktnavn**.
5. Klikk på rullegardinknappen i feltet **Varemodellgruppe** for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk på koblingen i den valgte raden i listen.
8. Klikk på rullegardinknappen i feltet **Varegruppe** for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Klikk på koblingen i den valgte raden i listen.
11. Klikk på rullegardinknappen i **Lagringsdimensjonsgruppe**-feltet for å åpne oppslaget.
12. Finn og velg ønsket post i listen.
13. Klikk på koblingen i den valgte raden i listen.
14. Klikk på rullegardinknappen i **Sporingsdimensjonsgruppe**-feltet for å åpne oppslaget.
15. Finn og velg ønsket post i listen.
16. Klikk på koblingen i den valgte raden i listen.
17. Klikk på **OK**.

## <a name="setup-default-order-settings"></a>Konfigurere standard ordreinnstillinger
1. Klikk på **Plan** i **handlingsruten**.
2. Under **Ordreinnstillinger** klikker du **Standard ordreinnstillinger**.
3. Under **Bestilling**, i feltet **Standardområde** skriver du inn området som brukes som standard når bestillinger opprettes.
4. Skriv inn området der varen lagres, i feltet **Standardlager**.
5. Vis eller skjul delen **Beholdning**.
6. I feltet **Multippel** skriver du inn 10.
7. I feltet **Minimumsordre** skriver du inn 10.
8. I feltet **Maks. ordreantall** skriver du inn 100.
9. I feltet **Standard ordreantall** skriver du inn 10.
10. Angi et tall i feltet **Leveringstid for innkjøp**.
11. Merk av eller fjern merket i avmerkingsboksen **Virkedager**.
12. Klikk på **Lagre**.
13. Velg Bestilling i feltet **Standard ordretype**.
14. Klikk på **Lagre**.
15. Lukk siden. Lukk siden Standard ordreinnstillinger.  

## <a name="add-an-item-to-a-coverage-group"></a>Legge til en vare i en dekningsgruppe
1. Vis eller skjul delen **Plan**.
2. Klikk på rullegardinknappen i **Dekningsgruppe**-feltet for å åpne oppslaget.
3. I listen finner du **dekningsgruppen** du har opprettet.
4. Klikk på koblingen i den valgte raden i listen.

## <a name="create-item-coverage-rules"></a>Opprette varedekningsregler
1. Klikk på **Plan** i **handlingsruten**.
2. Under **Dekning** klikker du **Varedekning**.
3. Klikk på **Ny**.
4. Klikk på fanen **Generelt**.
5. Merk av i boksen i overskriften til **Overstyr dekningsgruppeinnstillinger**.
6. Angi 60 i feltet **Dekningshorisont (dager)**. Selv om varene i dekningsgruppen Krav er planlagt 90 dager frem i tid, blir elementet planlagt 60 dager frem i tid.  
7. Angi 2 i **Negative dager**-feltet.
8. Angi 2 i **Positive dager**-feltet.
9. Klikk på fanen **Leveringstid**.
10. Merk av i boksen i overskriften for **Innkjøp**.
11. Angi 5 i feltet **Innkjøpstid**.
12. Klikk på **Lagre**.

