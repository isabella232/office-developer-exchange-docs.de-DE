---
title: ManagedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderId
api_type:
- schema
ms.assetid: 3efb7abb-0e91-4d8a-9fa2-3dec8bd17c30
description: Das ManagedFolderId-Element enthält die ID des verwalteten Ordner.
ms.openlocfilehash: acdb69f82678633baff12c46494c39015c36d233
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830340"
---
# <a name="managedfolderid"></a><span data-ttu-id="2b214-103">ManagedFolderId</span><span class="sxs-lookup"><span data-stu-id="2b214-103">ManagedFolderId</span></span>

<span data-ttu-id="2b214-104">Das **ManagedFolderId** -Element enthält die ID des verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="2b214-104">The **ManagedFolderId** element contains the folder ID of the managed folder.</span></span> 
  
```xml
<ManagedFolderId/>
```

 <span data-ttu-id="2b214-105">**string**</span><span class="sxs-lookup"><span data-stu-id="2b214-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b214-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2b214-106">Attributes and elements</span></span>

<span data-ttu-id="2b214-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2b214-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b214-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2b214-108">Attributes</span></span>

<span data-ttu-id="2b214-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b214-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b214-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b214-110">Child elements</span></span>

<span data-ttu-id="2b214-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b214-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2b214-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b214-112">Parent elements</span></span>

|<span data-ttu-id="2b214-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b214-113">**Element**</span></span>|<span data-ttu-id="2b214-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b214-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b214-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="2b214-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="2b214-116">Enthält Informationen zu einem verwalteten Ordner.</span><span class="sxs-lookup"><span data-stu-id="2b214-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2b214-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="2b214-117">Text value</span></span>

<span data-ttu-id="2b214-118">Es wird ein Textwert für dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2b214-118">A text value is required for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b214-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b214-119">Remarks</span></span>

<span data-ttu-id="2b214-120">**ManagedFolderId** -ID-Wert entspricht dem **Guid** -Eigenschaft, die von abgerufen wird die `Get-ManagedFolder` Microsoft Windows Powershell-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2b214-120">The **ManagedFolderId** identifier value is the equivalent of the **Guid** property that is retrieved by the  `Get-ManagedFolder` Microsoft Windows Powershell command.</span></span> <span data-ttu-id="2b214-121">Es ist auch der Wert des Attributs **Objekt-GUID** für den verwalteten Ordner in den Active Directory-Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="2b214-121">It is also the value of the **objectGUID** attribute for the managed folder in the Active Directory directory service.</span></span> 
  
<span data-ttu-id="2b214-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="2b214-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b214-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2b214-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b214-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b214-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b214-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2b214-125">Schema name</span></span>  <br/> |<span data-ttu-id="2b214-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2b214-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="2b214-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2b214-127">Validation file</span></span>  <br/> |<span data-ttu-id="2b214-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2b214-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b214-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2b214-129">Can be empty</span></span>  <br/> |<span data-ttu-id="2b214-130">False</span><span class="sxs-lookup"><span data-stu-id="2b214-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b214-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b214-131">See also</span></span>



[<span data-ttu-id="2b214-132">CreateManagedFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b214-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="2b214-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2b214-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2b214-134">Löschen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="2b214-134">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)
  
[<span data-ttu-id="2b214-135">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="2b214-135">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

