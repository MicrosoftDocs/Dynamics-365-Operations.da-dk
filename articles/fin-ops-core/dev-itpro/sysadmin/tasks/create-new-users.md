---
title: Oprette nye brugere
description: Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.
author: peakerbl
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f861b7493d039b332358be7df7d0198cbadcb7a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679834"
---
# <a name="create-new-users"></a>Oprette nye brugere

[!include [banner](../../includes/banner.md)]

Brugerne er interne medarbejdere i din organisation eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Tilknyt en bruger til en licens (kun nye licenstyper)
For kunder, der er medlem af en af de nye licenstyper, som er tilføjet i oktober 2019, skal brugere være tilknyttet en licens. Brugere, der er tilknyttet en licens, tilføjes automatisk som systembrugere, der ikke har nogen roller, første gang de logger på.

Systemadministratorer kan [tildele licenser til brugere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [Microsoft 365 Administration](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Tilknytte en ekstern bruger til en licens (kun nye licenstyper)
Brugere uden for den lejer, som miljøet blev implementeret i, skal repræsenteres i værtslejebiblioteket (Azure Active Directory (Azure AD)), så de kan tildeles licenser. Disse eksterne brugere skal føjes til lejeren i Azure AD som gæstebrugere og derefter tildeles de relevante licenser. Du kan finde flere oplysninger under [Tilføje Azure Active Directory B2B-samarbejdsbrugere i Azure-portalen](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Tilføje en ny bruger
1. Gå til **Systemadministration \> Brugere \> Brugere**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv et entydigt id for brugeren i feltet **Bruger-id**. Du skal angive et bruger-id.  
4. Angiv brugerens navn i feltet **Brugernavn**.  
5. I feltet **Domæne** skal du angive brugerens domæne.  
6. Angiv brugerens alias i feltet **Alias**.  
7. I feltet **Firma** skal du vælge det ønskede firma. 
8. I oversigtspanelet **Brugerens roller** skal du vælge **Tildel roller** for at tildele brugere til sikkerhedsroller. Du kan finde flere oplysninger under [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md).
9. Vælg **OK**.
10. Vælg **Gem**.

## <a name="import-users"></a>Importér brugere
1. Gå til **Systemadministration \> Brugere \> Brugere**.
2. Vælg **Importer brugere** i handlingsruden.
3. Markér den valgte række på listen.
4. Vælg **Importer brugere**.
5. Vælg **Luk**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]