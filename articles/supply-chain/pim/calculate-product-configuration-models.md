---
title: Ofte stillede spørgsmål om beregninger for produktkonfigurationsmodeller
description: I dette emne beskrives beregninger for produktkonfigurationsmodeller, og hvordan du bruger beregninger sammen med begrænsninger.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7fac3ec6df53dcc6e459f62f76d856a11d294b6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424294"
---
# <a name="calculations-for-product-configuration-models-faq"></a>Ofte stillede spørgsmål om beregninger for produktkonfigurationsmodeller

[!include [banner](../includes/banner.md)]

I dette emne beskrives beregninger for produktkonfigurationsmodeller, og hvordan du bruger beregninger sammen med begrænsninger.

Beregninger kan bruges til aritmetiske eller logiske operationer. De supplerer udtryksbegrænsninger i produktkonfigurationsmodeller. Du kan definere beregninger på siden **Detaljer om begrænsningsbaseret model til produktkonfiguration** og derefter oprette udtryk til beregninger i udtrykseditoren. Yderligere oplysninger finder du i Opret beregninger.

## <a name="what-is-a-calculation"></a>Hvad er en beregning?
En beregning er et element, som du kan bruge i en produktkonfigurationsmodel. Beregninger supplerer begrænsninger ved at give dig mulighed for at bruge decimaltal til beregne værdier, når du konfigurerer et produkt. Derudover har beregninger et større udvalg af tilgængelige operatorer end begrænsninger har.  

På samme måde som en begrænsning er en beregning knyttet til en bestemt komponent i en produktkonfigurationsmodel, og den ikke kan genbruges af eller deles med en anden komponent. En vigtig forskel mellem beregninger og begrænsninger er, at beregningerne er imperative (envejs), hvorimod begrænsninger er deklarative (tovejs). Få yderligere oplysninger om begrænsninger under [Udtryksbegrænsninger og tabelbegrænsninger i modeller for produktkonfiguration](expression-constraints-table-constraints-product-configuration-models.md).  

En beregning består af en målattribut og et beregningsudtryk.

## <a name="what-is-a-target-attribute"></a>Hvad er en målattribut?
En målattribut er en attribut, der modtager resultatet af beregningsudtrykket.  

I følgende udtryk er målattributten er en måling af en dug:  

**Udtryk:** Hvis\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** er bordets længde, og **decimalAttribute2** er dugens længde. Udtrykket returnerer værdien **True** til målattributten, hvis **decimalAttribute2** er større end eller lig med **decimalAttribute1**. Ellers returnerer udtrykket værdien **False**. Målingen af dugen er derfor acceptabel, hvis dugens længde er lig med eller overstiger bordets længde.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Hvilke attributtyper kan angives til målattributter?
Alle attributtyper, der understøttes til variantstyring, kan angives til målattributter undtagen tekst uden en fast liste.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Kan en værdi for en målattribut begrænse værdierne for inputattributterne i en beregning?
Nej, værdien for en målattribut kan ikke begrænse værdierne for inputattributterne, fordi beregningerne er envejs. Værdien for målattributten indstilles derfor på grundlag af ændringer i værdien af inputattributterne, men en ændring i værdien af målet påvirker ikke værdien af inputattributterne. Denne funktionsmåde adskiller sig fra funktionsmåden for begrænsninger. Begrænsninger forekommer i begge retninger.

### <a name="example"></a>Eksempel

I følgende udtryk er målet for beregningen længden af en netledning, og inputværdien er en farve:  

**Udtryk:** \[Hvis Farve == "Grøn", 1,5, 1,0\]  

Når du konfigurerer varen, er længden på netledningen **1,5**, hvis du angiver **Grøn** som værdi for farveattributten. Hvis du angiver en anden farve, konfigureres længden til **1,0**. Men da beregninger er envejs, angiver beregningen ikke værdien af farveattributten til **Grøn**, hvis du angiver en længde på **1,5**.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Hvad sker der, hvis en beregning har en målattribut af typen heltal, men en beregning giver et decimaltal?
Hvis en målattribut er af heltalstypen, men en beregning genererer et decimaltal, returneres kun heltalsdelen af det beregnede resultat. Decimaldelen fjernes, og resultatet afrundes ikke. Resultatet 12,70 vises f.eks. som 12.

## <a name="when-do-calculations-occur"></a>Hvornår foretages der beregninger?
Beregninger foretages, når der er angivet en værdi for alle inputattributter.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Kan jeg overskrive den værdi, der er beregnet for målattributten?
Du kan overskrive den værdi, der beregnes for målattributten, medmindre målattributten er angivet som skjult eller skrivebeskyttet.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-read-only"></a>Hvordan angiver jeg en målattribut som skjult eller skrivebeskyttet?
Hvis du vil angive en attribut som skjult eller skrivebeskyttet, skal du følge disse trin.

1.  Klik på **Administration af produktoplysninger** &gt; **Almindelige** &gt; **Produktkonfigurationsmodeller**.
2.  Vælg en produktkonfigurationsmodel, og derefter skal du i handlingsruden klikke på **Rediger**.
3.  Vælg en attribut, der skal bruges som en målattribut på siden **Detaljer om begrænsningsbaseret model til produktkonfiguration**.
4.  På oversigtspanelet **Attributter** skal du vælge **Skjult** eller **Skrivebeskyttet**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Kan en beregning overskrive de værdier, jeg angiver?
Nr. De værdier, du angiver, når du konfigurerer et produkt, er de værdier, der bruges. Den beregning, der foretages, når inputværdierne i en beregning er ændret, kan ikke overskrive de værdier, du angiver for en bestemt attribut.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Hvad sker der, hvis jeg fjerner en inputværdi i en beregning?
Hvis du fjerner en inputværdi i en beregning, fjernes også værdien af målattributten.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Hvorfor får jeg en fejlmeddelelse, der siger, at min model er i konflikt?
Denne meddelelse vises, når en beregning indeholder en fejl, eller når der findes en konflikt i en eller flere begrænsninger. Få yderligere oplysninger om konflikter i begrænsninger under [Udtryksbegrænsninger og tabelbegrænsninger i modeller for produktkonfiguration](expression-constraints-table-constraints-product-configuration-models.md). Her er nogle situationer, hvor der kan opstå fejl i beregningerne:

-   En værdi divideres med 0 (nul).
-   Der findes en konflikt mellem følgende to elementer:
    -   De værdier, der er tilgængelige for en attribut, og som er begrænset af en begrænsning
    -   En værdi, der er genereret af en beregning
-   De værdier, der returneres af beregningen, er uden for attributtens domæne. Et eksempel er et heltal fra \[1..10\], som er beregnet til 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Hvorfor får jeg en fejlmeddelelse, selvom jeg har valideret min produktmodel?
Beregninger er ikke inkluderet i valideringen. Du skal teste produktkonfigurationsmodellen for at finde fejl i beregninger. Følg disse trin for at teste en produktkonfigurationsmodel.

1.  Klik på **Administration af produktoplysninger** &gt; **Almindelige** &gt; **Produktkonfigurationsmodeller**.
2.  Vælg en produktkonfigurationsmodel, og derefter skal du i handlingsruden klikke på **Test** i gruppen **Kør**.




