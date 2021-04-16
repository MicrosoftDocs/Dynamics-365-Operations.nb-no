---
title: Konvertering av måleenhet per produktvariant
description: Dette emnet forklarer hvordan du definerer måleenhetskonverteringer for produktvarianter. Det inneholder et eksempel på oppsettet.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: eaa20f9a8f145fa8d44bfe77cc85f4dc565c2d27
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841509"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Konvertering av måleenhet per produktvariant

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer måleenhetskonverteringer for ulike produktvarianter.

I stedet for å opprette flere individuelle produkter som må vedlikeholdes, kan du bruke produktvarianter til å opprette variasjoner av ett produkt. En produktvariant kan for eksempel være en T-skjorte av en gitt størrelse og farge.

Tidligere kunne enhetskonverteringer bare defineres for produktstandarden. Derfor har alle produktvarianter samme enhetskonverteringsregler. Når funksjonen *Måleenhetskonverteringer for produktvarianter* er aktivert, kan du nå definere enhetskonverteringer mellom de forskjellige skjortenes størrelser og boksene som brukes for pakking, hvis T-skjorter blir solgt i bokser, og antall t-skjorter som kan pakkes i en boks, avhenger av størrelsen på t-skjorter.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funksjonen i systemet

Hvis du ikke allerede ser denne funksjonen i systemet, kan du gå til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Måleenhetskonverteringer for produktvarianter*.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Definere et produkt for enhetsomregning per variant

Produktvarianter kan opprettes bare for produkter som er produktstandarder. Hvis du vil ha mer informasjon, kan du se [Opprette en produktstandard](tasks/create-product-master.md). Funksjonen *Måleenhetskonverteringer for produktvarianter* er ikke tilgjengelig for produkter som er definert for faktisk vekt-prosesser.

Hvis du vil konfigurere en produktstandard til å støtte enhetskonvertering per variant, gjør du følgende.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktstandarder**.
1. Opprett eller åpne en produktstandard for å gå til siden **Produktdetaljer**.
1. Sett alternativet **Aktiver måleenhetskonverteringer** til *Ja*.
1. I gruppen **Oppsett** i fanen **Produkt** i handlingsruten velger du **Enhetskonverteringer**.
1. Siden **Enhetskonverteringer** åpnes. Velg én av følgende kategorier:

    - **Klasseinterne konverteringer** – Velg denne fanen for å konvertere mellom enheter som tilhører den samme enhetsklassen.
    - **Mellomklassekonverteringer** – Velg denne fanen for å konvertere mellom enheter som tilhører ulike klasser.

1. Velg **Ny** for å legge til en ny enhetskonvertering.
1. Sett feltet **Opprett konvertering for** til én av følgende verdier:

    - **Produkt** – Hvis du velger denne verdien, kan du definere en enhetskonvertering for produktstandarden. Denne enhetskonverteringen vil bli brukt som et tilbakefallsområde for alle produktvarianter som ingen enhetskonvertering er definert for.
    - **Produktvariant** – Hvis du velger denne verdien, kan du definere en enhetskonvertering for en bestemt produktvariant. Bruk feltet **Produktvariant** til å velge varianten.

    ![Legge til en ny enhetskonvertering](media/uom-new-conversion.png "Legge til en ny enhetskonvertering")

1. Bruk de andre feltene som finnes, til å definere enhetskonverteringen.
1. Velg **OK** for å lagre den nye enhetskonverteringen.

> [!TIP]
> Du kan åpne siden **Enhetskonverteringer** for et produkt eller en produktvariant fra følgende sider:
> 
> - Produktdetaljer
> - Detaljer om frigitt produkt
> - Frigitte produktvarianter

## <a name="example-scenario"></a>Eksempelscenario

I dette  selger et firma T-skjerer i størrelsene Liten, Middels, Stor og Ekstra stor. T-skjorten er definert som et produkt, og de ulike størrelsene er definert som varianter av det produktet. T-skjortene er pakket i bokser. Når det gjelder størrelsene Liten, Middels og Stor, kan det være fem T-skjorter i hver boks. Hvis størrelsen er Ekstra stor, er det imidlertid bare plass til fire t-skjorter i hver boks.

Firmaet ønsker å spore de ulike variantene av t-skjorter i enheten *Stykker*, men selger dem i *Boks*-enheter. For størrelsene Liten, Middels og Stor, er konverteringen mellom lagerenheten og salgsenheten 1 boks = 5 stykker. Når størrelsen er Ekstra stor, er konverteringen 1 boks = 4 stykker.

1. Fra siden **Detaljer om frigitt produkt** for produktet **T-skjorte** åpner du siden **Enhetskonverteringer**.
1. På siden **Enhetskonverteringer** definerer du følgende enhetskonvertering for den frigitte produktvarianten **Ekstra stor**.

    | Felt                 | Innstilling                 |
    |-----------------------|-------------------------|
    | Opprett konvertering for | Produktvariant         |
    | Produktvariant       | T-skjorte : : Ekstra stor : : |
    | Fra enhet             | Bokser                   |
    | Faktor                | 4                       |
    | Til enhet               | Stykker                  |

1. Ettersom produktvariantene **Liten**, **Middels** og **Stor** har samme enhetskonvertering mellom *Boks*- og *Stykker*-enhetene, kan du definere følgende enhetskonvertering for dem i produktstandarden.

    | Felt                 | Innstilling |
    |-----------------------|---------|
    | Opprett konvertering for | Produkt |
    | Produkt               | T-skjorte |
    | Fra enhet             | Bokser   |
    | Omregningsfaktor                | 5       |
    | Til enhet               | Stykker  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Bruke Excel til å oppdatere enhetsomregningene

Hvis et produkt har mange produktvarianter som har ulike enhetskonverteringer, kan det være lurt å eksportere enhetskonverteringene til en arbeidsbok i Microsoft Excel, oppdatere dem og deretter publisere dem tilbake til Dynamics 365 Supply Chain Management.

Hvis du vil eksportere enhetskonverteringer til Excel, velger du **Åpne i Microsoft Office** på siden **Enhetskonverteringer**.

## <a name="additional-resources"></a>Tilleggsressurser

[Administrere måleenhet](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]