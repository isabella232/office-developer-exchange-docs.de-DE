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
description: Das ViewPrivateItems-Element gibt an, ob ein Stellvertreter Benutzer oder eine Clientanwendung über die Berechtigung zum Anzeigen privater Elemente im Postfach des Prinzipals verfügt.
ms.openlocfilehash: 4e1375f7c4a3c660cc5de885deff8d094250ca7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44525969"
---
# <a name="viewprivateitems"></a><span data-ttu-id="6708e-103">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="6708e-103">ViewPrivateItems</span></span>

<span data-ttu-id="6708e-104">Das **ViewPrivateItems** -Element gibt an, ob ein Stellvertreter Benutzer oder eine Clientanwendung über die Berechtigung zum Anzeigen privater Elemente im Postfach des Prinzipals verfügt.</span><span class="sxs-lookup"><span data-stu-id="6708e-104">The **ViewPrivateItems** element indicates whether a delegate user or client application has permission to view private items in the principal's mailbox.</span></span> 
  
```XML
<ViewPrivateItems>true | false</ViewPrivateItems>
```

 <span data-ttu-id="6708e-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="6708e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6708e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6708e-106">Attributes and elements</span></span>

<span data-ttu-id="6708e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6708e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6708e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6708e-108">Attributes</span></span>

<span data-ttu-id="6708e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6708e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6708e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6708e-110">Child elements</span></span>

<span data-ttu-id="6708e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6708e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6708e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6708e-112">Parent elements</span></span>

|<span data-ttu-id="6708e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6708e-113">**Element**</span></span>|<span data-ttu-id="6708e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6708e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6708e-115">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="6708e-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="6708e-116">Bezeichnet einen einzelnen Delegaten, der in einem Postfach hinzugefügt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6708e-116">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6708e-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="6708e-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="6708e-118">Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner.</span><span class="sxs-lookup"><span data-stu-id="6708e-118">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="6708e-119">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6708e-119">This element is read-only.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6708e-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="6708e-120">Text value</span></span>

<span data-ttu-id="6708e-121">Der Wert **true** gibt an, dass der Stellvertreter oder Client private Elemente im Postfach des Prinzipals anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="6708e-121">A value of **true** indicates that the delegate or client can view private items in the principal's mailbox.</span></span> <span data-ttu-id="6708e-122">Der Wert **false** gibt an, dass private Elemente für einen Stellvertreter oder Client nicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="6708e-122">A value of **false** indicates that private items are not visible to a delegate or client.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6708e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6708e-123">Remarks</span></span>

<span data-ttu-id="6708e-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6708e-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6708e-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6708e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6708e-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="6708e-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6708e-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6708e-127">Schema Name</span></span>  <br/> |<span data-ttu-id="6708e-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6708e-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="6708e-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6708e-129">Validation File</span></span>  <br/> |<span data-ttu-id="6708e-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6708e-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6708e-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6708e-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="6708e-132">False</span><span class="sxs-lookup"><span data-stu-id="6708e-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6708e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6708e-133">See also</span></span>



[<span data-ttu-id="6708e-134">AddDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6708e-134">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="6708e-135">UpdateDelegate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6708e-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="6708e-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6708e-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6708e-137">Hinzufügen von Stellvertretungen</span><span class="sxs-lookup"><span data-stu-id="6708e-137">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

