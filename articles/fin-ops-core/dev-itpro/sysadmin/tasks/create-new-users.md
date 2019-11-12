---
title: Oprette nye brugere
description: Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570515"
---
# <a name="create-new-users"></a>Oprette nye brugere

[!include [task guide banner](../../includes/task-guide-banner.md)]

Brugerne er interne medarbejdere i din organisation eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Tilknyt en bruger til en licens (kun nye licenstyper)
For kunder, der er medlem af en af de nye licenstyper, som er tilføjet i oktober 2019, skal brugere være tilknyttet en licens. Brugere, der er tilknyttet en licens, tilføjes automatisk som systembrugere, der ikke har nogen roller, første gang de logger på. Brugere, der ikke er knyttet til et licens, får vist en advarselsmeddelelse.

Systemadministratorer kan [tildele licenser til brugere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [Microsoft 365 Administration](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Tilføje en ny bruger
1. Gå til **Systemadministration \> Brugere \> Brugere**.
2. Gå til handlingsruden, og vælg **Ny**.
3. Angiv et entydigt id for brugeren i feltet **Bruger-id**. Du skal angive et bruger-id.  
4. Angiv brugerens navn i feltet **Brugernavn**.  
5. I feltet **Domæne** skal du angive brugerens domæne.  
6. Angiv brugerens alias i feltet **Alias**.  
7. I feltet **Firma** skal du vælge det ønskede firma. 
8. I oversigtspanelet **Brugerens roller** skal du vælge **Tildel roller** for at [tildele brugere til sikkerhedsroller](assign-users-security-roles.md)
9. Vælg **OK**.
10. Vælg **Gem**.

## <a name="import-users"></a>Importér brugere
1. Vælg **Importer brugere** i handlingsruden.
2. Markér den valgte række på listen.
3. Vælg **Importer brugere**.
4. Vælg **Luk**.

