---
title: ViewPrivateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ViewPrivateItems
api_type:
- schema
ms.assetid: 80b949ac-440c-4a01-b428-ebafb5b1b802
description: Das ViewPrivateItems-Element gibt an, ob eine Stellvertretung Benutzer oder eine Client-Anwendung die Berechtigung zum Anzeigen von privaten Elemente im Postfach für den Prinzipal hat.
ms.openlocfilehash: c35f24ae79e907424cb5cfb0efeec2307334ca12
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839506"
---
# <a name="viewprivateitems"></a><span data-ttu-id="7582d-103">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="7582d-103">ViewPrivateItems</span></span>

<span data-ttu-id="7582d-104">Das **ViewPrivateItems** -Element gibt an, ob eine Stellvertretung Benutzer oder eine Client-Anwendung die Berechtigung zum Anzeigen von privaten Elemente im Postfach für den Prinzipal hat.</span><span class="sxs-lookup"><span data-stu-id="7582d-104">The **ViewPrivateItems** element indicates whether a delegate user or client application has permission to view private items in the principal's mailbox.</span></span> 
  
```XML
<ViewPrivateItems>true | false</ViewPrivateItems>
```

 <span data-ttu-id="7582d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7582d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7582d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7582d-106">Attributes and elements</span></span>

<span data-ttu-id="7582d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7582d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7582d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7582d-108">Attributes</span></span>

<span data-ttu-id="7582d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7582d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7582d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7582d-110">Child elements</span></span>

<span data-ttu-id="7582d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7582d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7582d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7582d-112">Parent elements</span></span>

|<span data-ttu-id="7582d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7582d-113">**Element**</span></span>|<span data-ttu-id="7582d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7582d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7582d-115">Beauftragte Benutzer</span><span class="sxs-lookup"><span data-stu-id="7582d-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="7582d-116">Identifiziert einen einzelnen Delegaten hinzufügen oder aktualisieren in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="7582d-116">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7582d-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="7582d-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="7582d-118">Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="7582d-118">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="7582d-119">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7582d-119">This element is read-only.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7582d-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="7582d-120">Text value</span></span>

<span data-ttu-id="7582d-121">Der Wert **true** gibt an, dass die Stellvertretung oder Client private Elemente im Postfach des Prinzipals anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="7582d-121">A value of **true** indicates that the delegate or client can view private items in the principal's mailbox.</span></span> <span data-ttu-id="7582d-122">Der Wert **false** gibt an, dass private Elemente nicht zu einer Stellvertretung oder Client sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="7582d-122">A value of **false** indicates that private items are not visible to a delegate or client.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7582d-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7582d-123">Remarks</span></span>

<span data-ttu-id="7582d-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7582d-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7582d-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7582d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7582d-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="7582d-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7582d-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7582d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7582d-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7582d-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="7582d-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7582d-129">Validation File</span></span>  <br/> |<span data-ttu-id="7582d-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7582d-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7582d-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7582d-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="7582d-132">False</span><span class="sxs-lookup"><span data-stu-id="7582d-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7582d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7582d-133">See also</span></span>



[<span data-ttu-id="7582d-134">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7582d-134">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="7582d-135">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7582d-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="7582d-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7582d-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="7582d-137">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="7582d-137">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

