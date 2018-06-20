---
title: ContactsFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsFolderPermissionLevel
api_type:
- schema
ms.assetid: 805f05e7-b320-436a-9965-ba1ee235ac41
description: Das ContactsFolderPermissionLevel-Element enthält die Berechtigungen für den Standardordner Kontakte. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 4b6a109c3a38a20dc5d6f611607b16ada0e4e46b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757626"
---
# <a name="contactsfolderpermissionlevel"></a><span data-ttu-id="28fe8-104">ContactsFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="28fe8-104">ContactsFolderPermissionLevel</span></span>

<span data-ttu-id="28fe8-105">Das **ContactsFolderPermissionLevel** -Element enthält die Berechtigungen für den Standardordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="28fe8-105">The **ContactsFolderPermissionLevel** element contains the permissions for the default Contacts folder.</span></span> <span data-ttu-id="28fe8-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="28fe8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ContactsFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</ContactsFolderPermissionLevel>
```

 <span data-ttu-id="28fe8-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="28fe8-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28fe8-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28fe8-108">Attributes and elements</span></span>

<span data-ttu-id="28fe8-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28fe8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28fe8-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="28fe8-110">Attributes</span></span>

<span data-ttu-id="28fe8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="28fe8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28fe8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28fe8-112">Child elements</span></span>

<span data-ttu-id="28fe8-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="28fe8-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28fe8-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28fe8-114">Parent elements</span></span>

|<span data-ttu-id="28fe8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="28fe8-115">**Element**</span></span>|<span data-ttu-id="28fe8-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28fe8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28fe8-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="28fe8-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="28fe8-118">Die Stellvertretung die berechtigungseinstellungen auf Poolebene für einen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="28fe8-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="28fe8-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="28fe8-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28fe8-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="28fe8-120">Text value</span></span>

<span data-ttu-id="28fe8-121">Die folgende Tabelle enthält die Textwerte, die die Berechtigungsstufen darstellen.</span><span class="sxs-lookup"><span data-stu-id="28fe8-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="28fe8-122">**Ebene Text Berechtigungswerte**</span><span class="sxs-lookup"><span data-stu-id="28fe8-122">**Permission level text values**</span></span>

|<span data-ttu-id="28fe8-123">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="28fe8-123">**Permission level**</span></span>|<span data-ttu-id="28fe8-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28fe8-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28fe8-125">Keine</span><span class="sxs-lookup"><span data-stu-id="28fe8-125">None</span></span>  <br/> |<span data-ttu-id="28fe8-126">Stellvertretungsbenutzers verfügt über keine Access-Berechtigungen in den Ordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="28fe8-126">The delegate user has no access permissions to the Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="28fe8-127">Prüfer</span><span class="sxs-lookup"><span data-stu-id="28fe8-127">Reviewer</span></span>  <br/> |<span data-ttu-id="28fe8-128">Stellvertretungsbenutzers kann Lesen von Elementen in den Ordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="28fe8-128">The delegate user can read items in the Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="28fe8-129">Autor</span><span class="sxs-lookup"><span data-stu-id="28fe8-129">Author</span></span>  <br/> |<span data-ttu-id="28fe8-130">Stellvertretungsbenutzers lesen und Erstellen von Elementen im Ordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="28fe8-130">The delegate user can read and create items in the Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="28fe8-131">Herausgeber</span><span class="sxs-lookup"><span data-stu-id="28fe8-131">Editor</span></span>  <br/> |<span data-ttu-id="28fe8-132">Stellvertretungsbenutzers kann lesen, erstellen und Ändern von Elementen in den Ordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="28fe8-132">The delegate user can read, create, and modify items in the Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="28fe8-133">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="28fe8-133">Custom</span></span>  <br/> |<span data-ttu-id="28fe8-134">Stellvertretungsbenutzers hat benutzerdefinierte Zugriffsberechtigungen in den Ordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="28fe8-134">The delegate user has custom access permissions to the Contacts folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28fe8-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28fe8-135">Remarks</span></span>

<span data-ttu-id="28fe8-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="28fe8-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28fe8-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="28fe8-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28fe8-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="28fe8-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28fe8-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28fe8-139">Schema Name</span></span>  <br/> |<span data-ttu-id="28fe8-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="28fe8-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="28fe8-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28fe8-141">Validation File</span></span>  <br/> |<span data-ttu-id="28fe8-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28fe8-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28fe8-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="28fe8-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="28fe8-144">False</span><span class="sxs-lookup"><span data-stu-id="28fe8-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28fe8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28fe8-145">See also</span></span>



[<span data-ttu-id="28fe8-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28fe8-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="28fe8-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28fe8-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="28fe8-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="28fe8-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="28fe8-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="28fe8-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

