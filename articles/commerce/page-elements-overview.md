---
title: Ordliste til sidemodel
description: I dette emne beskrives de forskellige elementer, der bruges på siderne på et Microsoft Dynamics 365 Commerce-websted.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c5ec6dfd9147fd5e054303b4fd612caef78b7467d7f6f4850e46fcc9fb1346f2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758306"
---
# <a name="page-model-glossary"></a>Ordliste til sidemodel


[!include [banner](includes/banner.md)]

I dette emne beskrives de forskellige elementer, der bruges på siderne på et Microsoft Dynamics 365 Commerce-websted.

## <a name="page-element-definitions"></a>Definitioner af sideelementer

Følgende tabel indeholder en oversigt over ord, som du skal være bekendt med, når du ændrer udseendet og indholdet på dit websted. Du kan finde mere indgående forklaringer og procedurer ved at følge linkene.

| Periode | Beskrivelse og noter |
|------|-----------------------|
| [Modul](work-with-modules.md) | <p>**Definition:** Moduler er komponenter, der kan redigeres, og som udgør en websides skelet. Eksemplerne omfatter sidehoved-, hero- og karruselmoduler.</p><p>**Hvor vælges det?:** Installerede moduler kan vælges og konfigureres i forskellige stadier af arbejdsgangen for oprettelse af websted, f.eks. skabelon-, layout-, side- og fragmentoprettelsesstadier.</p><p>**Hvor redigeres det?:** Der oprettes brugerdefinerede moduler i programkode ved hjælp af SDK'et (Software Development Kit). De overføres derefter til dit websted, hvor de vil kunne vælges.</p> |
| Modulegenskab | <p>**Definition:** Modulegenskaber er bestemte indstillinger, der defineres af modulet. De kan redigeres i e-handelsredigeringsværktøjerne. Modulegenskaber bruges f.eks. til at angive overskrift og baggrundsbillede for et bannermodul.</p><p>**Hvor konfigureres de?:** Modulegenskaber vælges og konfigureres i egenskabsruden, som vises i redigeringsmiljøer (editorer) til skabeloner, layout, sider, fragmenter og appindstillinger.</p> |
| [Skabelon](templates-layouts-overview.md) | <p>**Definition:** Skabeloner definerer de modulkombinationer og indstillinger, der skal bruges til en kategori af sider (f.eks. marketingsider, kategorisider og produktsider).</p><p>**Hvor vælges det?:** Du kan vælge skabeloner under arbejdsgange til oprettelse af sider eller layout.</p><p>**Hvor redigeres det?:** Skabeloner oprettes i skabeloneditoren. Der kræves ingen kode for at oprette eller redigere dem.</p> |
| [Layout](templates-layouts-overview.md) | <p>**Definition:** Layout angiver det endelige valg og organisering af moduler fra den overordnede skabelons indstillinger. Der kan konfigureres et layout for en enkelt side (*brugerdefineret layout*), eller det kan deles af flere sider (*forudindstillet layout*).</p><p>**Hvor vælges det?:** Layout kan vælges under oprettelse af ny side, eller når der kræves et andet layout til en eksisterende side.</p><p>**Hvor redigeres det?:** Layout oprettes i layouteditoren. Der kræves ingen kode for at oprette eller redigere dem.</p> |
| [Sideforekomst](modify-existing-page.md) | <p>**Definition:** Sideforekomster definerer det endelige, sidespecifikke oversatte indhold for en enkelt side. Dette indhold er afledt af værdierne i modulegenskaberne.</p><p>**Hvor vælges det?:** Sider vælges, når URL-adresser er tildelt.</p><p>**Hvor redigeres det?:** Sider redigeres i sideeditoren. Der kræves ingen kode for at oprette eller redigere dem.</p> |
| [Tema](select-site-theme.md) | <p>**Definition:** Temaer definerer det overlappende typografiark (Cascading Style Sheet – CSS) og bestemmer udseendet af de moduler, der gengives på en side.</p><p>**Hvor vælges det?:** Når et tema er overført til dit websted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS), kan det vælges som en egenskab i sidecontainermodulet.</p><p>**Hvor redigeres det?:** Temaer oprettes og redigeres i øjeblikket ved hjælp af SDK. De overføres derefter til dit websted ved hjælp af LCS.</p> |
| [Fragment](work-with-fragments.md) | <p>**Definition:** Fragmenter er fuldt konfigurerede moduler, der har lokaliseret indhold, der kan genbruges og opdateres centralt på tværs af flere sider. Et fragment, der oprettes ud fra et sidehovedmodul, kan f.eks. bruges i alle skabeloner og på alle sider på tværs af webstedet og opdateres centralt på ét sted.</p><p>**Hvor vælges det?:** Fragmenter kan vælges, hvor der kan vælges moduler. De kan erstattes med et modul for at øge effektiviteten gennem genbrug og centraliseret oprettelse.</p><p>**Hvor redigeres det?:** Fragmenter redigeres i fragmenteditoren. Der kræves ingen kode for at oprette eller redigere dem.</p> |
| [URL-adresse](create-page-URL.md) | <p>**Definition:** Uniform Resource Locators (URL-adresser) er adresser, der peger på websider eller andre URL-adresser.</p><p>**Hvor vælges den?:** URL-adresser vælges, hvor der kræves links mellem sider.</p><p>**Hvor redigeres de?:** URL-adresser redigeres i URL-editoren. Der kræves ingen kode for at oprette eller redigere dem.</p> |
| Aktiv | <p>**Definition:** Aktiver er binære filer, der har et filtypenavn, f.eks. .jpg, .docx, .pdf eller .mpg.</p><p>**Hvor vælges de?:** Aktiver vælges som modulegenskaber til moduler, der kræver dem.</p><p>**Hvor redigeres de?:** Aktiver overføres, og tilknyttede metadata redigeres i aktivstyringen.</p> |

## <a name="additional-resources"></a>Yderligere ressourcer

[Metoder til at tilføje indhold](add-manage-content.md)

[Dokumenttilstande og -livscyklus](document-states-overview.md)

[Arbejde med publiceringsgrupper](publish-groups.md)

[Aktivere og bruge deling på tværs af kanaler](cross-channel-sharing.md)

[Arbejde med moduler](work-with-modules.md)

[Arbejde med fragmenter](work-with-fragments.md)

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Tilpasse navigation på webstedet](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]