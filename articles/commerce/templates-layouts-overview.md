---
title: Oversigt over skabeloner og layout
description: Dette emne omhandler skabeloner og layout i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 835b283ea93f761791745a41c74b6a12c11eea02
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962954"
---
# <a name="templates-and-layouts-overview"></a>Oversigt over skabeloner og layout


[!include [banner](includes/banner.md)]

Skabeloner er et grundlæggende element i Microsoft Dynamics 365 Commerce-sidemodellen. Hvis dit mål er at maksimere effektiviteten og ensartetheden for arbejdsgange til oprettelse af websteder, er det vigtigt, at du lærer, hvordan du drager fordel af skabeloner til dit websted. De tidlige beslutninger om skabelonstruktur er vigtige, og de kan påvirke omkostningerne og smidigheden for daglige, lejlighedsvise og webstedsdækkende opdateringer af brands. Velstrukturerede skabeloner har også andre fordele. De kan f.eks. forbedre SEO-scoren (optimering af søgemaskine) og minimere antallet af fejl.

En god start på arbejdet med skabeloner er at forstå de funktionelle fordele ved skabeloner og layout, forskellene mellem dem og hierarkiet.

I følgende illustration vises sidemodelhierarkiet bag en gengivet webside.

![Diagram over sidemodel](../commerce/media/page-model-diagram.png)

| Enhed        | Grundlæggende funktion |
|---------------|----------------|
| Skabelon      | Skabeloner definerer modulindstillinger og grundlæggende fundment for et sæt layout og sideforekomster. |
| Layout        | Layout definerer det endelige valg og organiseringen af moduler for en side eller et sæt sider. |
| Sideforekomst | Sideforekomster definerer data og indhold for bestemte sider. |

## <a name="templates"></a>Skabeloner

Skabelonerne findes øverst i Dynamics 365 Commerce-sidemodelhierarkiet og repræsenterer et vigtigt indledende trin til konfiguration af webstedet. Skabeloner er grundlæggende med til at styre konsistensen på tværs af en familie af underordnede layout og sider ved at definere basisstrukturen og oprettelsesindstillingerne for arbejdsgange til downstream-oprettelse af layout og sider. Skabeloner kan være med til at forenkle indholdsoprettelsesprocessen via foruddefinerede, centralt styrede elementer (f.eks. sidehoveder og sidefødder) og guidede oprettelsesforløb, der er med til at sikre, at valg af modulkonfiguration følger brandet.

### <a name="controlling-consistency"></a>Kontrollere konsistens

Når du designer en skabelon, er den største beslutning, du skal tage, hvor meget kontrol skabelonen skal have over sideoprettelsesprocessen. En skabelon, der efterlader alt åbent for en downstream-forfatter, er den letteste type skabelon at oprette, men den kan have langsigtede konsekvenser for vedligeholdelsen af de sider, der oprettes ud fra den. En veldefineret skabelon giver vejledning og en strømlinet oprettelsesoplevelse, men den giver også forfattere tilstrækkelig fleksibilitet, så de kan fuldføre deres opgaver. Alle disse aspekter afhænger af det kontrolniveau, som skabelonen gennemtvinger.

Skabeloner kan hjælpe indholdsforfattere med at blive mere effektive og holde fast i brandet på følgende måder:

- Begrænse de moduler, der kan bruges på en side.
- Foreslå standardmodul- og -konfigurationsvalg.
- Foretage nogle eksplicitte modul- og konfigurationsvalg, der styres på skabelonniveau. Denne proces kaldes også *låsning* af en indstilling.

Følgende eksempel viser, hvordan en basisskabelon (skabelon X) kan konfigureres:

- Alle underordnede layout for skabelon X skal have en sidehovedcontainer, en brødtekstcontainer og en sidefodscontainer.
- I skabelon X er konfigurationen af sidehovedcontaineren låst og kan kun ændres i selve skabelon X. Alle de underordnede layout og sider har altid dette sidehoved.
- Containeren til brødtekst kræver mindst ét modul og op til højst ti moduler. Disse moduler defineres af downstream-layout og -sider.
- For brødtekstcontaineren er hero-, funktion-, karrusel- og bannermodulerne tilgængelige.
- En container til en sidefod konfigureres i skabelon X, men den kan tilsidesættes af downstream-layout og -sider.

Skabelonen i dette eksempel definerer en simpel struktur og et sæt indstillinger for forfattere af downstream-indhold. Bemærk, at visse dele af en side (i dette tilfælde sidehovedet) er fuldt defineret og låst i skabelonen, og de kan ikke ændres af en downstream-forfatter. Andre dele (i dette tilfælde brødteksten) kan defineres af downstream-forfattere inden for specifikke retningslinjer (i dette tilfælde et minimumantal og maksimumantal moduler af bestemte typer). Og andre dele (i dette tilfælde sidefoden) defineres i skabelonen, men kan tilsidesættes af downstream-forfattere.

Et vigtigt første trin for websteds- og brandadministratorer er at bestemme den korrekte balance mellem begrænsning og fleksibilitet af underordnede layout- og sideforfattere. Når der bruges skabeloner, kan denne balance konfigureres fuldt ud. Det påvirker, om sideelementer opdateres centralt (låst i skabelonen) eller overlades til individuelle underordnede niveauer, der er lavere i sidehierarkiet.

Hvis du vil begynde at bruge skabeloner, skal du se [Arbejde med skabeloner](work-with-templates.md).

## <a name="layouts"></a>Layouts

Layout er det næste niveau i sidemodelhierarkiet, under skabeloner. En skabelon definerer alle de moduler, der er tilladt for en side, men et layout er en eksplicit udvælgelse og organisering af moduler. Sider er det næste niveau i sidemodelhierarkiet, under layout. De definerer det lokaliserede indhold for de moduler, der er valgt i layoutet.

Følgende eksempel bygger på skabeloneksemplet fra forrige afsnit og viser, hvordan et grundlæggende layout kan konfigureres:

- Layoutets overordnede skabelon kræver, at brødtekstcontaineren har mellem et og ti moduler. Disse moduler kan kun være hero-, funktions-, karrusel- og bannermoduler. Derfor kan layoutet definere følgende valg og arrangement af moduler:

    - Det første modul i brødtekstcontaineren er et bannermodul, og det efterfølges af et hero-modul og to funktionsmoduler.
    - Det første funktionsmodul er venstrejusteret, og det andet funktionsmodul er højrejusteret.

- Selvom en standardsidefod er nedarvet fra den overordnede skabelon, er det skabelonens forfatter, der har efterladt sidefoden låst op. Derfor kan layoutet tilsidesættes ved at definere et andet sidefodsfragment.

Layoutet i dette eksempel definerer det endelige arrangement af moduler for underordnede sider. Ligesom en skabelon kan et layout definere standard- eller låste modulegenskaber, der altid vil blive nedarvet af underordnede sider (f.eks. justeringen af funktionsmodulerne). Det egentlige indhold eller de faktiske data for hvert modul i layoutet defineres derefter længere nede i hierarkiet i alle forekomster af den underordnede side. En væsentlig forskel her er, at layout ikke direkte indeholder lokaliseret indhold, mens de underordnede sider gør. Layoutets primære funktion er at definere den endelige arrangements- og standardkonfiguration af moduler til de underordnede sider.

Dette hierarki er stærkt af to årsager. For det første behandles layout, der deler den samme overordnede skabelon, som kompatible med scenarier for skift af layout. Derfor kan layoutet for alle sider ændres til et andet layout fra det samme skabelonhierarki, uden at det kræver, at indholdet på sideniveau ændres. Du kan drage fordel af denne funktion, hvis du vil skabe lejlighedsvise designopdateringer, eksperimentere eller oprette et redigeret permanent design for et websted. For det andet giver layout en anden central mulighed for at ændre delte elementer for en gruppe af sider, uden at det er nødvendigt at opdatere enkelte sider. Hvis en produktkategori f.eks. har 1.000 sider, der deler det samme layout, kan modulerne omarrangeres i layoutet, så denne ændring omgående bliver afspejlet på alle 1.000 underordnede sider.

Ved at forstå dette hierarki kan du levere en smidig og effektiv struktur til websteder, der hjælper med at spare omkostninger, kan skaleres og giver bedre resultater, efterhånden som webstedet udvikles over tid.

### <a name="preset-and-custom-layouts"></a>Forudindstillede og brugerdefinerede layout

Layout på dit websted kan enten være *forudindstillede* eller *brugerdefinerede*:

- **Forudindstillede layout** giver mulighed for en arbejdsgang til sideoprettelse, hvor alle moduler allerede er valgt og arrangeret, og der kræves kun dataindtastning. Denne fremgangsmåde kan spare tid, når der skal oprettes mange sider med de samme layoutkrav. Forudindstillede layout har en-til-mange-relation til deres underordnede sider. Det betyder, at et enkelt forudindstillet layout kan bruges til centralt at styre modularrangementet for hundredvis eller tusindvis af underordnede sider.
- **Brugerdefinerede layout** er i det væsentlige layout til engangsbrug, der er integreret på én side. De vises ikke som en indstilling, når der oprettes andre nye sider, eller i scenarier med skift af layout. Fordelen ved denne fremgangsmåde er, at en forfatter kan eksperimentere med at oprette en side, der har et brugerdefineret layout. Hvis forfatteren vil genbruge layoutet til andre sider, kan det nemt konverteres til et forudindstillet layout. Det nye forudindstillede layout vises derefter som en indstilling i arbejdsgange for sideoprettelse og i scenarier til layoutændring for sider i det samme skabelonhierarki. Omvendt kan forudindstillede layout fordeles på brugerdefinerede layout. På denne måde kan en forfatter flytte en side væk fra det forudindstillede layout og oprette et nyt brugerdefineret layout til engangsbrug. (Dette nye brugerdefinerede layout er stadig bundet af eventuelle begrænsninger i den overordnede skabelon).

Forudindstillede layout og brugerdefinerede layout redigeres i forskellige dele af oprettelsesværktøjssættet. Da brugerdefinerede layout ikke har nogen afhængigheder på andre sider, redigeres de direkte i sideeditoren. I dette tilfælde er tilstedeværelsen af et layout hovedsageligt transparent for brugeren og vises kun i egenskaber på sideniveau og via handlinger for layoutindstillinger. Men da ændringer af forudindstillede layout kan påvirke mange underordnede sider, skal de redigeres i layouteditoren, hvor udgivelseshandlinger tager højde for den fulde downstream-virkning på underordnede sider.

I følgende illustrationer vises scenarier for forudindstillede og brugerdefinerede layout.

![Scenarier med forudindstillede og tilpassede layout](../commerce/media/template-figure1.png)

Hvis du vil begynde at bruge forudindstillede layout, skal du se [Arbejde med forudindstillede layout](work-with-layouts.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Arbejde med skabeloner](work-with-templates.md)

[Arbejde med forudindstillede layout](work-with-layouts.md)

[Arbejd med publiceringsgrupper](publish-groups.md)
