---
title: InboxFolderPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InboxFolderPermissionLevel
api_type:
- schema
ms.assetid: f250d31b-9193-4c1c-8350-900dead3a023
description: Das InboxFolderPermissionLevel-Element enthält die Berechtigungen für den standardmäßigen Posteingangsordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 8a497a38a58e6455f2bd754aa8da97b421a2bca3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465709"
---
# <a name="inboxfolderpermissionlevel"></a><span data-ttu-id="d883f-104">InboxFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="d883f-104">InboxFolderPermissionLevel</span></span>

<span data-ttu-id="d883f-105">Das **InboxFolderPermissionLevel** -Element enthält die Berechtigungen für den standardmäßigen Posteingangsordner.</span><span class="sxs-lookup"><span data-stu-id="d883f-105">The **InboxFolderPermissionLevel** element contains the permissions for the default Inbox folder.</span></span> <span data-ttu-id="d883f-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d883f-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<InboxFolderPermissionLevel>
   None or Editor or Reviewer or Author or Custom
</InboxFolderPermissionLevel>
```

 <span data-ttu-id="d883f-107">**DelegateFolderPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="d883f-107">**DelegateFolderPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d883f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d883f-108">Attributes and elements</span></span>

<span data-ttu-id="d883f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d883f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d883f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d883f-110">Attributes</span></span>

<span data-ttu-id="d883f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d883f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d883f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d883f-112">Child elements</span></span>

<span data-ttu-id="d883f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d883f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d883f-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d883f-114">Parent elements</span></span>

|<span data-ttu-id="d883f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d883f-115">**Element**</span></span>|<span data-ttu-id="d883f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d883f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d883f-117">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="d883f-117">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="d883f-118">Enthält die Einstellungen für die Stell Vertretungs Berechtigungsstufe für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d883f-118">Contains the delegate permission level settings for a user.</span></span> <span data-ttu-id="d883f-119">Dieses Element wurde in Exchange 2007 SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d883f-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d883f-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="d883f-120">Text value</span></span>

<span data-ttu-id="d883f-121">In der folgenden Tabelle sind die Textwerte aufgeführt, die die Berechtigungsstufen darstellen.</span><span class="sxs-lookup"><span data-stu-id="d883f-121">The following table lists the text values that represent the permission levels.</span></span>
  
<span data-ttu-id="d883f-122">**Text Werte für Berechtigungsstufen**</span><span class="sxs-lookup"><span data-stu-id="d883f-122">**Permission level text values**</span></span>

|<span data-ttu-id="d883f-123">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="d883f-123">**Permission level**</span></span>|<span data-ttu-id="d883f-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d883f-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d883f-125">Keine</span><span class="sxs-lookup"><span data-stu-id="d883f-125">None</span></span>  <br/> |<span data-ttu-id="d883f-126">Der Stellvertreter Benutzer verfügt über keine Zugriffsberechtigungen für den Ordner Posteingangsordner.</span><span class="sxs-lookup"><span data-stu-id="d883f-126">The delegate user has no access permissions to the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="d883f-127">Reviewer</span><span class="sxs-lookup"><span data-stu-id="d883f-127">Reviewer</span></span>  <br/> |<span data-ttu-id="d883f-128">Der Stellvertreter kann Elemente im Posteingangsordner lesen.</span><span class="sxs-lookup"><span data-stu-id="d883f-128">The delegate user can read items in the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="d883f-129">Ursprung</span><span class="sxs-lookup"><span data-stu-id="d883f-129">Author</span></span>  <br/> |<span data-ttu-id="d883f-130">Der Stellvertreter kann Elemente im Posteingangsordner lesen und erstellen.</span><span class="sxs-lookup"><span data-stu-id="d883f-130">The delegate user can read and create items in the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="d883f-131">Editor</span><span class="sxs-lookup"><span data-stu-id="d883f-131">Editor</span></span>  <br/> |<span data-ttu-id="d883f-132">Der Stellvertreter kann Elemente im Posteingangsordner lesen, erstellen und ändern.</span><span class="sxs-lookup"><span data-stu-id="d883f-132">The delegate user can read, create, and modify items in the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="d883f-133">Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="d883f-133">Custom</span></span>  <br/> |<span data-ttu-id="d883f-134">Der Stellvertreter Benutzer verfügt über benutzerdefinierte Zugriffsberechtigungen für den Ordner Posteingang.</span><span class="sxs-lookup"><span data-stu-id="d883f-134">The delegate user has custom access permissions to the Inbox folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d883f-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d883f-135">Remarks</span></span>

<span data-ttu-id="d883f-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d883f-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d883f-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d883f-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d883f-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d883f-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d883f-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d883f-139">Schema Name</span></span>  <br/> |<span data-ttu-id="d883f-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d883f-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="d883f-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d883f-141">Validation File</span></span>  <br/> |<span data-ttu-id="d883f-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d883f-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d883f-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d883f-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="d883f-144">False</span><span class="sxs-lookup"><span data-stu-id="d883f-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d883f-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d883f-145">See also</span></span>



[<span data-ttu-id="d883f-146">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d883f-146">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="d883f-147">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d883f-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="d883f-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d883f-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d883f-149">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="d883f-149">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

