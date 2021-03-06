---
title: Konfigurere personaleparametre
description: Dette emne forklarer, hvordan du konfigurerer virksomhedsspecifikke parametre i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c4c93e3d2644a380e3d5d2247961a8b6fb34568
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052403"
---
# <a name="configure-human-resources-parameters"></a>Konfigurere personaleparametre

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Indstillingerne for nogle personaleparametre deles på tværs af firmaer, mens indstillingerne af andre parametre er firmaspecifikke. Dette emne forklarer, hvordan du konfigurerer firmaspecifikke personaleparametre.

To sider bruges til at angive personaleparametre. For parametre, der deles på tværs af firmaer, skal du bruge siden **Delte parametre for personale**. For parametre, der er specifikke for virksomheden (med andre ord gælder indstillingerne for en enkelt virksomhed), skal du bruge siden **Human Resourcesparametre**.

![Gå til Personaleparametre](./media/hr-employee-self-service-human-resources-parameters.png)

På siden **Human Resourcesparametre** er indstillingerne fordelt på seks faner:

- **Generel**
- **Rekruttering** (denne fane er ikke inkluderet i Dynamics 365 Human Resources)
- **Kompensation**
- **Nummerserier**
- **FMLA**
- **Medarbejderselvbetjening**
- **Selvbetjening for leder**
- **Frynsegodeadministration**
- **Orlov og fravær**
- **Betalingsmetoder**

Hver fane indeholder oplysninger, der vedrører en enkelt virksomhed.

## <a name="general"></a>Generel

Indstillingerne på fanen **Generelt** definerer visningen af oplysninger om fravær, skader og sygdom og nye ansættelser. Indstillingerne på denne fane kan også definere nogle standardposter, der vises, mens du arbejder. Denne fane giver dig mulighed for at:

- Vælge den farve, der skal anvendes på åbne fraværsposter
- Angive det typografiark, der skal bruges til rapporter
- Aktivere integration mellem kurser og fraværsregistrering
- Vælg den fraværskode, der bruges til at styre denne integration.
- Angiv, hvor længe hændelser med skades- og sygdomstilfælde skal opbevares.
- Angiv det standard-id, der vises, når der ansættes en ny arbejder.

![Fanen Generelt](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Rekruttering

Indstillingerne under fanen **Rekruttering** definerer de dokumenttyper, der bruges til korrespondance, som automatisk sendes til ansøgere. Du kan også angive det rekrutteringsprojekt, der bruges til uopfordrede ansøgninger.

Den periode, der er defineret for det aldersfordelte rekrutteringsprojekt bestemmer rekrutteringsprojekter, der er medtaget i feltet **Aldersfordelte projekter** i arbejdsområdet **Rekrutteringsstyring**. Den periode, der er defineret for advarsel om deadline for ansøgning bruges til at få vist rekrutteringsprojekter, der nærmer sig deres ansøgningsfrist i feltet den **Deadline for ansøgning nærmer sig** i arbejdsområdet **Rekruttering**.

Du kan finde flere oplysninger om rekruttering under [Rekruttere jobkandidater](hr-personnel-recruit.md).

## <a name="compensation"></a>Kompensation

I Dynamics 365 Finance definerer indstillingerne under fanen **Kompensation**, om brugere skal bekræfte, at de vil gemme oplysninger om en fast eller variabel lønstruktur. Hvis du vælger **Aktivér validering ved lagring**, får brugerne vist en meddelelse, når de lukker en kompensationsrelateret side, hvor de bliver spurgt, om de vil gemme posten. Nogle sider i Kompensationsstyring giver ikke brugerne mulighed for at slette information. Når brugeren får besked på at bekræfte, om oplysningerne skal gemmes, kan det hjælpe med at begrænse mængden af oplysninger, der gemmes, men ikke senere kan slettes. Hvis du rydder **Aktivér validering ved lagring**, gemmes poster med det samme, eventuelt før brugeren er klar. Hvis du bruger Performancestyring, giver fanen **Kompensation** dig også mulighed for at vælge en rangeringsmodel, der skal bruges i stedet for den model, der er tildelt til kompensationsstrukturerne, når performance vurderes.

I Human Resources kan du bruge fanen **Kompensation** til at vælge at begrænse adgangen til kompensationsplaner og angive en standardvaluta.

Du kan finde flere oplysninger om kompensation under [Oversigt over lønstrukturer](hr-compensation-overview.md).

![Fanen Kompensation](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Nummerserier

Indstillingerne under fanen **Nummerserie** bestemmer, hvilke nummerserier der bruges til automatisk at tildele elementer id'er i Human Resources, f.eks.:

- Anvendelser
- Fraværsregistreringer
- Resultater af kompensationsproces
- Sagsnumre
- Kurser
- Kursusagendaer

Hvis du vil vedligeholde nummerseriereferencer og -koder skal du bruge listesiden **Nummerserier** (vælg **Organisationsadministration > Nummerserier > Nummerserier**).

Du kan finde flere oplysninger under [Oversigt over nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Antallet af timer, der er arbejdet, må ikke overstige 1.250, og længden af beskæftigelsen må ikke overstige 12 måneder. Disse maksimale værdier er i overensstemmelse med gældende lovgivning i USA.

![Fanen Nummerserier](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

Du kan angive FMLA-berettigelseskrav og FMLA-berettigelsestimer under fanen FMLA. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværsparametre](hr-leave-and-absence-parameters.md).

![Fanen FMLA](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Medarbejderselvbetjening

Indstillingerne under fanen **Medarbejderselvbetjening** har indflydelse på, hvordan medarbejderens selvbetjening vises for medarbejderne. Under denne fane kan du:

- Angive et navn i arbejdsområdet Medarbejderselvbetjening
- Vælge, hvilke oplysninger en leder kan angive for medarbejdere
- Tilføje nyttige links for medarbejdere
- Begrænse medarbejdere i at tilføje eller redigere forretningskontaktoplysninger. Du kan finde flere oplysninger i [Begrænse redigering af personlige oplysninger](hr-employee-self-service-restrict-editing.md).

Du kan finde flere oplysninger om opsætning af medarbejderselvbetjening i [Oversigt over medarbejder- og lederselvbetjening](hr-employee-manager-self-service-overview.md).

![Fanen Medarbejderselvbetjening](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Selvbetjening for leder

Indstillingerne under fanen **Selvbetjening for leder** har indflydelse på, hvad lederne kan se i Selvbetjening for leder. Under denne fane kan du konfigurere følgende indstillinger:

- Intervallet for udløb af poster
- Informationschefer kan se udløb af poster
- Om ledere kan se ledige stillinger til udvidede underordnede
- Visninger af fratrædende arbejdere
- Nyttige links for ledere

Du kan finde flere oplysninger om opsætning af lederselvbetjening i [Oversigt over medarbejder- og lederselvbetjening](hr-employee-manager-self-service-overview.md).

![Fanen Selvbetjening for leder](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Frynsegodeadministration

Under fanen Frynsegodeadministration kan du konfigurere mailindstillinger for Frynsegodeadministration. Du kan finde flere oplysninger om konfiguration og brug af Frynsegodeadministration i [Oversigt over Administration af frynsegoder](hr-benefits-management-overview.md).

![Fanen Frynsegodeadministration](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Orlov og fravær

Du kan finde flere oplysninger om opsætning og brug af orlov og fravær under [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Betalingsmetoder

Under fanen **Betalingsmetoder** kan du vælge de betalingsmetoder, der understøttes af din organisation. Du kan finde flere oplysninger om konfiguration af kompensation under [Oversigt over lønstrukturer](hr-compensation-overview.md).

![Fanen Betalingsmetoder](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]