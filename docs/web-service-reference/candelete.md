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
ms.openlocfilehash: 5fe16c276bdb0c5b3b73ca63099559d3e869db3e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461590"
---
# <a name="candelete"></a><span data-ttu-id="2b194-103">CanDelete</span><span class="sxs-lookup"><span data-stu-id="2b194-103">CanDelete</span></span>

<span data-ttu-id="2b194-104">Das **CanDelete** -Element gibt an, ob ein verwalteter Ordner von einem Kunden gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b194-104">The **CanDelete** element indicates whether a managed folder can be deleted by a customer.</span></span> 
  
```xml
<CanDelete/>
```

 <span data-ttu-id="2b194-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="2b194-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b194-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2b194-106">Attributes and elements</span></span>

<span data-ttu-id="2b194-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2b194-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b194-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2b194-108">Attributes</span></span>

<span data-ttu-id="2b194-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b194-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b194-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b194-110">Child elements</span></span>

<span data-ttu-id="2b194-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b194-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2b194-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b194-112">Parent elements</span></span>

|<span data-ttu-id="2b194-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b194-113">**Element**</span></span>|<span data-ttu-id="2b194-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b194-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b194-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="2b194-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="2b194-116">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="2b194-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2b194-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="2b194-117">Text value</span></span>

<span data-ttu-id="2b194-118">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich, wenn dieses Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2b194-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="2b194-119">Der Wert **true** gibt an, dass der Ordner gelöscht werden kann; der Wert **false** bedeutet, dass der Ordner nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b194-119">A value of **true** indicates that the folder can be deleted; a value of **false** means that the folder cannot be deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2b194-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b194-120">Remarks</span></span>

<span data-ttu-id="2b194-121">Verwenden Sie den [DeleteFolder-Vorgang](deletefolder-operation.md), um einen verwalteten Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="2b194-121">To delete a managed folder, use the [DeleteFolder operation](deletefolder-operation.md).</span></span>
  
<span data-ttu-id="2b194-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2b194-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b194-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2b194-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b194-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b194-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b194-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2b194-125">Schema name</span></span>  <br/> |<span data-ttu-id="2b194-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2b194-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="2b194-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2b194-127">Validation file</span></span>  <br/> |<span data-ttu-id="2b194-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2b194-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b194-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2b194-129">Can be empty</span></span>  <br/> |<span data-ttu-id="2b194-130">False</span><span class="sxs-lookup"><span data-stu-id="2b194-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b194-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b194-131">See also</span></span>



[<span data-ttu-id="2b194-132">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b194-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="2b194-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2b194-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2b194-134">Löschen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="2b194-134">Deleting Folders</span></span>](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

