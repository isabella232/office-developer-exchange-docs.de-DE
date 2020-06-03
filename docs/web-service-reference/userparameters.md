---
title: User Parameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: Das User Parameters-Element enthält eine Liste der aktivierten und deaktivierten Clienterweiterungen.
ms.openlocfilehash: 76bf858adfb6d2ef76a25c234117131752c60d7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526753"
---
# <a name="userparameters"></a><span data-ttu-id="55f87-103">User Parameters</span><span class="sxs-lookup"><span data-stu-id="55f87-103">UserParameters</span></span>

<span data-ttu-id="55f87-104">Das **User Parameters** -Element enthält eine Liste der aktivierten und deaktivierten Clienterweiterungen.</span><span class="sxs-lookup"><span data-stu-id="55f87-104">The **UserParameters** element contains a list of enabled and disabled client extensions.</span></span> 
  
```XML
<UserParameters UserId="" EnabledOnly="">
   <UserEnabledExtensions/>
   <UserDisabledExtensions/>
</UserParameters>
```

 <span data-ttu-id="55f87-105">**GetClientExtensionUserParametersType**</span><span class="sxs-lookup"><span data-stu-id="55f87-105">**GetClientExtensionUserParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55f87-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="55f87-106">Attributes and elements</span></span>

<span data-ttu-id="55f87-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="55f87-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55f87-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="55f87-108">Attributes</span></span>

|<span data-ttu-id="55f87-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="55f87-109">**Attribute**</span></span>|<span data-ttu-id="55f87-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55f87-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55f87-111">UserId</span><span class="sxs-lookup"><span data-stu-id="55f87-111">UserId</span></span>  <br/> |<span data-ttu-id="55f87-112">Der Textwert des **UserID** -Attributs ist der Bezeichner des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="55f87-112">The text value of the **UserId** attribute is the identifier of the user.</span></span>  <br/> |
|<span data-ttu-id="55f87-113">EnabledOnly</span><span class="sxs-lookup"><span data-stu-id="55f87-113">EnabledOnly</span></span>  <br/> |<span data-ttu-id="55f87-114">Der Textwert des **EnabledOnly** gibt an, ob die Antwort nur die aktivierten Erweiterungen enthält.</span><span class="sxs-lookup"><span data-stu-id="55f87-114">The text value of the **EnabledOnly** indicates whether the response only contains the enabled extensions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="55f87-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55f87-115">Child elements</span></span>

<span data-ttu-id="55f87-116">[UserEnabledExtensions](userenabledextensions.md)  |  [UserDisabledExtensions](userdisabledextensions.md)</span><span class="sxs-lookup"><span data-stu-id="55f87-116">[UserEnabledExtensions](userenabledextensions.md) | [UserDisabledExtensions](userdisabledextensions.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="55f87-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55f87-117">Parent elements</span></span>

[<span data-ttu-id="55f87-118">GetClientExtension</span><span class="sxs-lookup"><span data-stu-id="55f87-118">GetClientExtension</span></span>](getclientextension.md)
  
## <a name="remarks"></a><span data-ttu-id="55f87-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55f87-119">Remarks</span></span>

<span data-ttu-id="55f87-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="55f87-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="55f87-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="55f87-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55f87-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="55f87-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55f87-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="55f87-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="55f87-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="55f87-124">Schema name</span></span>  <br/> |<span data-ttu-id="55f87-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="55f87-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="55f87-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="55f87-126">Validation file</span></span>  <br/> |<span data-ttu-id="55f87-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="55f87-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="55f87-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="55f87-128">Can be empty</span></span>  <br/> ||
   

