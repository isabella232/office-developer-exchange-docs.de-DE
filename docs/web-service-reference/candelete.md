---
title: CanDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanDelete
api_type:
- schema
ms.assetid: 55e17121-aad0-4f90-889f-2c3512e9579c
description: Das CanDelete-Element gibt an, ob ein verwalteter Ordner von einem Kunden gelöscht werden kann.
ms.openlocfilehash: b70b28bd6b3c9452f5d7f249f453218d555754da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757549"
---
# <a name="candelete"></a><span data-ttu-id="6d221-103">CanDelete</span><span class="sxs-lookup"><span data-stu-id="6d221-103">CanDelete</span></span>

<span data-ttu-id="6d221-104">Das **CanDelete** -Element gibt an, ob ein verwalteter Ordner von einem Kunden gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="6d221-104">The **CanDelete** element indicates whether a managed folder can be deleted by a customer.</span></span> 
  
```xml
<CanDelete/>
```

 <span data-ttu-id="6d221-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d221-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d221-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6d221-106">Attributes and elements</span></span>

<span data-ttu-id="6d221-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6d221-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d221-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6d221-108">Attributes</span></span>

<span data-ttu-id="6d221-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6d221-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d221-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d221-110">Child elements</span></span>

<span data-ttu-id="6d221-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6d221-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d221-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6d221-112">Parent elements</span></span>

|<span data-ttu-id="6d221-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d221-113">**Element**</span></span>|<span data-ttu-id="6d221-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6d221-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d221-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="6d221-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="6d221-116">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="6d221-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6d221-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="6d221-117">Text value</span></span>

<span data-ttu-id="6d221-118">Ein Textwert, der einen booleschen Wert darstellt ist erforderlich, wenn dieses Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d221-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="6d221-119">Der Wert **true** gibt an, dass der Ordner gelöscht werden kann; der Wert **false** bedeutet, dass der Ordner kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="6d221-119">A value of **true** indicates that the folder can be deleted; a value of **false** means that the folder cannot be deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6d221-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6d221-120">Remarks</span></span>

<span data-ttu-id="6d221-121">Um einen verwalteten Ordner zu löschen, verwenden Sie die [DeleteFolder-Vorgang](deletefolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="6d221-121">To delete a managed folder, use the [DeleteFolder operation](deletefolder-operation.md).</span></span>
  
<span data-ttu-id="6d221-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6d221-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d221-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6d221-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d221-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d221-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6d221-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6d221-125">Schema name</span></span>  <br/> |<span data-ttu-id="6d221-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6d221-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="6d221-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6d221-127">Validation file</span></span>  <br/> |<span data-ttu-id="6d221-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6d221-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6d221-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6d221-129">Can be empty</span></span>  <br/> |<span data-ttu-id="6d221-130">False</span><span class="sxs-lookup"><span data-stu-id="6d221-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d221-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d221-131">See also</span></span>



[<span data-ttu-id="6d221-132">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6d221-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="6d221-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6d221-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6d221-134">Löschen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="6d221-134">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

