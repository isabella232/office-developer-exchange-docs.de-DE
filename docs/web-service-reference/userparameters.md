---
title: UserParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: Das UserParameters-Element enthält eine Liste der Clienterweiterungen aktiviert und deaktiviert.
ms.openlocfilehash: e0a72fe13255380ee56b32c863fb3bffb2e1ac5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839458"
---
# <a name="userparameters"></a><span data-ttu-id="e722f-103">UserParameters</span><span class="sxs-lookup"><span data-stu-id="e722f-103">UserParameters</span></span>

<span data-ttu-id="e722f-104">Das **UserParameters** -Element enthält eine Liste der Clienterweiterungen aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e722f-104">The **UserParameters** element contains a list of enabled and disabled client extensions.</span></span> 
  
```XML
<UserParameters UserId="" EnabledOnly="">
   <UserEnabledExtensions/>
   <UserDisabledExtensions/>
</UserParameters>
```

 <span data-ttu-id="e722f-105">**GetClientExtensionUserParametersType**</span><span class="sxs-lookup"><span data-stu-id="e722f-105">**GetClientExtensionUserParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e722f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e722f-106">Attributes and elements</span></span>

<span data-ttu-id="e722f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e722f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e722f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e722f-108">Attributes</span></span>

|<span data-ttu-id="e722f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e722f-109">**Attribute**</span></span>|<span data-ttu-id="e722f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e722f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e722f-111">UserId</span><span class="sxs-lookup"><span data-stu-id="e722f-111">UserId</span></span>  <br/> |<span data-ttu-id="e722f-112">Der Textwert des **Benutzer-ID** -Attributs ist der Bezeichner des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="e722f-112">The text value of the **UserId** attribute is the identifier of the user.</span></span>  <br/> |
|<span data-ttu-id="e722f-113">EnabledOnly</span><span class="sxs-lookup"><span data-stu-id="e722f-113">EnabledOnly</span></span>  <br/> |<span data-ttu-id="e722f-114">Der Textwert der der **EnabledOnly** gibt an, ob die Antwort nur die aktivierten Erweiterungen enthält.</span><span class="sxs-lookup"><span data-stu-id="e722f-114">The text value of the **EnabledOnly** indicates whether the response only contains the enabled extensions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e722f-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e722f-115">Child elements</span></span>

<span data-ttu-id="e722f-116">[UserEnabledExtensions](userenabledextensions.md) | [UserDisabledExtensions](userdisabledextensions.md)</span><span class="sxs-lookup"><span data-stu-id="e722f-116">[UserEnabledExtensions](userenabledextensions.md) | [UserDisabledExtensions](userdisabledextensions.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e722f-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e722f-117">Parent elements</span></span>

[<span data-ttu-id="e722f-118">GetClientExtension</span><span class="sxs-lookup"><span data-stu-id="e722f-118">GetClientExtension</span></span>](getclientextension.md)
  
## <a name="remarks"></a><span data-ttu-id="e722f-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e722f-119">Remarks</span></span>

<span data-ttu-id="e722f-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e722f-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e722f-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e722f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e722f-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e722f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e722f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e722f-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e722f-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e722f-124">Schema name</span></span>  <br/> |<span data-ttu-id="e722f-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e722f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="e722f-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e722f-126">Validation file</span></span>  <br/> |<span data-ttu-id="e722f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e722f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e722f-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e722f-128">Can be empty</span></span>  <br/> ||
   

