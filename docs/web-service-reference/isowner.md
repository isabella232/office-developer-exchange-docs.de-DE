---
title: Isowner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea0f0afc-32fe-46cb-8530-62a6ce9490f6
description: Das isowner-Element gibt an, ob der angegebene e-Mail-Benutzer der Besitzer ist.
ms.openlocfilehash: 2dd085aba34052d95efd1e72edca7be4aba71155
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466521"
---
# <a name="isowner"></a><span data-ttu-id="0db46-103">Isowner</span><span class="sxs-lookup"><span data-stu-id="0db46-103">IsOwner</span></span>

<span data-ttu-id="0db46-104">Das **isowner** -Element gibt an, ob der angegebene e-Mail-Benutzer der Besitzer ist.</span><span class="sxs-lookup"><span data-stu-id="0db46-104">The **IsOwner** element specifies whether the specified email user is the owner.</span></span> 
  
```XML
<IsOwner>true | false</IsOwner>
```

 <span data-ttu-id="0db46-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="0db46-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0db46-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0db46-106">Attributes and elements</span></span>

<span data-ttu-id="0db46-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0db46-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0db46-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0db46-108">Attributes</span></span>

<span data-ttu-id="0db46-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0db46-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0db46-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0db46-110">Child elements</span></span>

<span data-ttu-id="0db46-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0db46-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0db46-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0db46-112">Parent elements</span></span>

|<span data-ttu-id="0db46-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0db46-113">**Element**</span></span>|<span data-ttu-id="0db46-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0db46-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0db46-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="0db46-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="0db46-116">Gibt Informationen zur Rechteverwaltungslizenz an.</span><span class="sxs-lookup"><span data-stu-id="0db46-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0db46-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="0db46-117">Text value</span></span>

<span data-ttu-id="0db46-118">Der Textwert **true** für das **isowner** -Element gibt an, dass der Benutzer der Besitzer von Rechten ist, die für ein Element ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0db46-118">A text value of **true** for the **IsOwner** element indicates that the user is the owner of rights issued on an item.</span></span> <span data-ttu-id="0db46-119">Der Wert **false** gibt an, dass der Benutzer nicht der Besitzer von Rechten ist, die für ein Element ausgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0db46-119">A value of **false** indicates that the user is not the owner of rights issued on an item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0db46-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0db46-120">Remarks</span></span>

<span data-ttu-id="0db46-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0db46-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0db46-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0db46-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0db46-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0db46-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0db46-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0db46-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0db46-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0db46-125">Schema Name</span></span>  <br/> |<span data-ttu-id="0db46-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="0db46-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="0db46-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0db46-127">Validation File</span></span>  <br/> |<span data-ttu-id="0db46-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0db46-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0db46-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0db46-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0db46-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0db46-130">See also</span></span>



- [<span data-ttu-id="0db46-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0db46-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

