---
title: "\"UserRoles\""
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be003e12-3496-468d-a61c-48af0b819654
description: Das Element "UserRoles" gibt die Benutzerrollen, die den aufrufenden Benutzer oder der Benutzer, dem die aufrufende partneranwendung als, fungiert der aktuelle Anruf zuweisen möchte.
ms.openlocfilehash: 19dc1a7e00decb9141326b53b650d72101013c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839462"
---
# <a name="userroles"></a><span data-ttu-id="35d79-103">"UserRoles"</span><span class="sxs-lookup"><span data-stu-id="35d79-103">UserRoles</span></span>

<span data-ttu-id="35d79-104">Das Element **"UserRoles"** gibt die Benutzerrollen, die den aufrufenden Benutzer oder der Benutzer, dem die aufrufende partneranwendung als, fungiert der aktuelle Anruf zuweisen möchte.</span><span class="sxs-lookup"><span data-stu-id="35d79-104">The **UserRoles** element specifies the user roles that the calling user, or the user that the calling partner application is acting as, wants to apply to the current call.</span></span> 
  
```XML
<UserRoles>
   <Role/>
</UserRoles>
```

 <span data-ttu-id="35d79-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="35d79-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35d79-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="35d79-106">Attributes and elements</span></span>

<span data-ttu-id="35d79-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="35d79-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35d79-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="35d79-108">Attributes</span></span>

<span data-ttu-id="35d79-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="35d79-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35d79-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35d79-110">Child elements</span></span>

[<span data-ttu-id="35d79-111">Role</span><span class="sxs-lookup"><span data-stu-id="35d79-111">Role</span></span>](role.md)
  
### <a name="parent-elements"></a><span data-ttu-id="35d79-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35d79-112">Parent elements</span></span>

[<span data-ttu-id="35d79-113">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="35d79-113">ManagementRole</span></span>](managementrole.md)
  
## <a name="remarks"></a><span data-ttu-id="35d79-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35d79-114">Remarks</span></span>

<span data-ttu-id="35d79-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="35d79-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="35d79-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="35d79-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35d79-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="35d79-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35d79-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="35d79-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35d79-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="35d79-119">Schema name</span></span>  <br/> |<span data-ttu-id="35d79-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="35d79-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="35d79-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="35d79-121">Validation file</span></span>  <br/> |<span data-ttu-id="35d79-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="35d79-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35d79-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="35d79-123">Can be empty</span></span>  <br/> ||
   

