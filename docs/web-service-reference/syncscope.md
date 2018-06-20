---
title: SyncScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncScope
api_type:
- schema
ms.assetid: e0ca231f-0374-4844-8d4c-ada8da167920
description: Das SyncScope-Element gibt an, ob nur Elemente oder Elemente und verknüpften Ordnerinformationen in eine Synchronisierung Antwort zurückgegeben werden.
ms.openlocfilehash: 847c0244a8847364e29ea584b0c0b721f00d3064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839154"
---
# <a name="syncscope"></a><span data-ttu-id="3e9fd-103">SyncScope</span><span class="sxs-lookup"><span data-stu-id="3e9fd-103">SyncScope</span></span>

<span data-ttu-id="3e9fd-104">Das **SyncScope** -Element gibt an, ob nur Elemente oder Elemente und verknüpften Ordnerinformationen in eine Synchronisierung Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-104">The **SyncScope** element specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 <span data-ttu-id="3e9fd-105">**SyncFolderItemsScopeType**</span><span class="sxs-lookup"><span data-stu-id="3e9fd-105">**SyncFolderItemsScopeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e9fd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e9fd-106">Attributes and elements</span></span>

<span data-ttu-id="3e9fd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e9fd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e9fd-108">Attributes</span></span>

<span data-ttu-id="3e9fd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e9fd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e9fd-110">Child elements</span></span>

<span data-ttu-id="3e9fd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3e9fd-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e9fd-112">Parent elements</span></span>

|<span data-ttu-id="3e9fd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e9fd-113">**Element**</span></span>|<span data-ttu-id="3e9fd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e9fd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e9fd-115">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="3e9fd-115">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="3e9fd-116">Das Element, das eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher definiert.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-116">The element that defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="3e9fd-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3e9fd-117">The following is the XPath expression to this element:</span></span>  <br/> <span data-ttu-id="3e9fd-118">/ SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="3e9fd-118">/SyncFolderItems</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3e9fd-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="3e9fd-119">Text value</span></span>

<span data-ttu-id="3e9fd-120">Die folgende Tabelle enthält die möglichen Werte für das **SyncScope** -Element.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-120">The following table lists the possible values for the **SyncScope** element.</span></span> 
  
<span data-ttu-id="3e9fd-121">**SyncScope-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="3e9fd-121">**SyncScope element values**</span></span>

|<span data-ttu-id="3e9fd-122">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3e9fd-122">**Value**</span></span>|<span data-ttu-id="3e9fd-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e9fd-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e9fd-124">NormalItems</span><span class="sxs-lookup"><span data-stu-id="3e9fd-124">NormalItems</span></span>  <br/> |<span data-ttu-id="3e9fd-125">Gibt an, dass nur die Elemente im Ordner in einer Synchronisierung Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-125">Specifies that only items in the folder are returned in a synchronization response.</span></span>  <br/> |
|<span data-ttu-id="3e9fd-126">NormalAndAssociatedItems</span><span class="sxs-lookup"><span data-stu-id="3e9fd-126">NormalAndAssociatedItems</span></span>  <br/> |<span data-ttu-id="3e9fd-127">Gibt an, dass beide Elemente in den Ordner und die Informationen des Ordners, in eine Synchronisierung Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-127">Specifies that both items in the folder and folder associated information are returned in a synchronization response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e9fd-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e9fd-128">Remarks</span></span>

<span data-ttu-id="3e9fd-129">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3e9fd-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e9fd-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3e9fd-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e9fd-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e9fd-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3e9fd-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e9fd-132">Schema Name</span></span>  <br/> |<span data-ttu-id="3e9fd-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3e9fd-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3e9fd-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e9fd-134">Validation File</span></span>  <br/> |<span data-ttu-id="3e9fd-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3e9fd-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3e9fd-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3e9fd-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e9fd-137">False</span><span class="sxs-lookup"><span data-stu-id="3e9fd-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e9fd-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e9fd-138">See also</span></span>



[<span data-ttu-id="3e9fd-139">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3e9fd-139">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="3e9fd-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3e9fd-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

