---
title: IsFolderContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsFolderContact
api_type:
- schema
ms.assetid: 8b456255-f4ae-4ca0-845a-13c195f1c867
description: Das IsFolderContact-Element gibt an, ob ein Benutzer einen Kontakt für einen Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 51a79b4535667685517ff55ef9f6c2b2aaea564c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830015"
---
# <a name="isfoldercontact"></a><span data-ttu-id="d0020-104">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="d0020-104">IsFolderContact</span></span>

<span data-ttu-id="d0020-105">Das **IsFolderContact** -Element gibt an, ob ein Benutzer einen Kontakt für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d0020-105">The **IsFolderContact** element indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="d0020-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d0020-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<IsFolderContact/>
```

 <span data-ttu-id="d0020-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d0020-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0020-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d0020-108">Attributes and elements</span></span>

<span data-ttu-id="d0020-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0020-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0020-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0020-110">Attributes</span></span>

<span data-ttu-id="d0020-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0020-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0020-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0020-112">Child elements</span></span>

<span data-ttu-id="d0020-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0020-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0020-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0020-114">Parent elements</span></span>

|<span data-ttu-id="d0020-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0020-115">**Element**</span></span>|<span data-ttu-id="d0020-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0020-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0020-117">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="d0020-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="d0020-p103">Definiert den Zugriff, den ein Benutzer verfügt in einen Ordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d0020-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d0020-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="d0020-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="d0020-p104">Definiert den, den ein Benutzer hat Zugriff auf einen Kalenderordner. Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d0020-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0020-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="d0020-123">Text value</span></span>

<span data-ttu-id="d0020-124">Der Textwert **true** gibt an, dass der Benutzer einen Kontakt für den angegebenen Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="d0020-124">A text value of **true** indicates that the user is a contact for the specified folder.</span></span> <span data-ttu-id="d0020-125">Der Wert **false** gibt an, dass der Benutzer einen Kontakt für den angegebenen Ordner nicht ist.</span><span class="sxs-lookup"><span data-stu-id="d0020-125">A value of **false** indicates that the user is not a contact for the specified folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0020-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0020-126">Remarks</span></span>

<span data-ttu-id="d0020-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d0020-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0020-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d0020-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0020-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0020-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0020-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d0020-130">Schema Name</span></span>  <br/> |<span data-ttu-id="d0020-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d0020-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0020-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d0020-132">Validation File</span></span>  <br/> |<span data-ttu-id="d0020-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d0020-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0020-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d0020-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0020-135">False</span><span class="sxs-lookup"><span data-stu-id="d0020-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0020-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0020-136">See also</span></span>



- [<span data-ttu-id="d0020-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0020-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d0020-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="d0020-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

