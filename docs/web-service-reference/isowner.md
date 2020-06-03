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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466521"
---
# <a name="isowner"></a><span data-ttu-id="e76e1-103">Isowner</span><span class="sxs-lookup"><span data-stu-id="e76e1-103">IsOwner</span></span>

<span data-ttu-id="e76e1-104">Das **isowner** -Element gibt an, ob der angegebene e-Mail-Benutzer der Besitzer ist.</span><span class="sxs-lookup"><span data-stu-id="e76e1-104">The **IsOwner** element specifies whether the specified email user is the owner.</span></span> 
  
```XML
<IsOwner>true | false</IsOwner>
```

 <span data-ttu-id="e76e1-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="e76e1-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e76e1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e76e1-106">Attributes and elements</span></span>

<span data-ttu-id="e76e1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e76e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e76e1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e76e1-108">Attributes</span></span>

<span data-ttu-id="e76e1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e76e1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e76e1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e76e1-110">Child elements</span></span>

<span data-ttu-id="e76e1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e76e1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e76e1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e76e1-112">Parent elements</span></span>

|<span data-ttu-id="e76e1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e76e1-113">**Element**</span></span>|<span data-ttu-id="e76e1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e76e1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e76e1-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="e76e1-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="e76e1-116">Gibt Informationen zur Rechteverwaltungslizenz an.</span><span class="sxs-lookup"><span data-stu-id="e76e1-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e76e1-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e76e1-117">Text value</span></span>

<span data-ttu-id="e76e1-118">Der Textwert **true** für das **isowner** -Element gibt an, dass der Benutzer der Besitzer von Rechten ist, die für ein Element ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e76e1-118">A text value of **true** for the **IsOwner** element indicates that the user is the owner of rights issued on an item.</span></span> <span data-ttu-id="e76e1-119">Der Wert **false** gibt an, dass der Benutzer nicht der Besitzer von Rechten ist, die für ein Element ausgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e76e1-119">A value of **false** indicates that the user is not the owner of rights issued on an item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e76e1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e76e1-120">Remarks</span></span>

<span data-ttu-id="e76e1-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e76e1-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e76e1-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e76e1-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e76e1-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e76e1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e76e1-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e76e1-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e76e1-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e76e1-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e76e1-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="e76e1-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="e76e1-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e76e1-127">Validation File</span></span>  <br/> |<span data-ttu-id="e76e1-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e76e1-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e76e1-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e76e1-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e76e1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e76e1-130">See also</span></span>



- [<span data-ttu-id="e76e1-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e76e1-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

