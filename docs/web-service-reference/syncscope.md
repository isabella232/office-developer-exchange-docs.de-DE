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
description: Das SyncScope-Element gibt an, ob nur Elemente oder Elemente und Ordner zugeordnete Informationen in einer Synchronisierungsantwort zurückgegeben werden.
ms.openlocfilehash: 5ede26204c823a452189222075c784f24e98d188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463034"
---
# <a name="syncscope"></a><span data-ttu-id="ca9cf-103">SyncScope</span><span class="sxs-lookup"><span data-stu-id="ca9cf-103">SyncScope</span></span>

<span data-ttu-id="ca9cf-104">Das **SyncScope** -Element gibt an, ob nur Elemente oder Elemente und Ordner zugeordnete Informationen in einer Synchronisierungsantwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-104">The **SyncScope** element specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 <span data-ttu-id="ca9cf-105">**SyncFolderItemsScopeType**</span><span class="sxs-lookup"><span data-stu-id="ca9cf-105">**SyncFolderItemsScopeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca9cf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ca9cf-106">Attributes and elements</span></span>

<span data-ttu-id="ca9cf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca9cf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ca9cf-108">Attributes</span></span>

<span data-ttu-id="ca9cf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca9cf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca9cf-110">Child elements</span></span>

<span data-ttu-id="ca9cf-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ca9cf-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca9cf-112">Parent elements</span></span>

|<span data-ttu-id="ca9cf-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ca9cf-113">**Element**</span></span>|<span data-ttu-id="ca9cf-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca9cf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca9cf-115">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="ca9cf-115">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="ca9cf-116">Das-Element, das eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner definiert.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-116">The element that defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="ca9cf-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="ca9cf-117">The following is the XPath expression to this element:</span></span>  <br/> <span data-ttu-id="ca9cf-118">/SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="ca9cf-118">/SyncFolderItems</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ca9cf-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="ca9cf-119">Text value</span></span>

<span data-ttu-id="ca9cf-120">In der folgenden Tabelle sind die möglichen Werte für das **SyncScope** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-120">The following table lists the possible values for the **SyncScope** element.</span></span> 
  
<span data-ttu-id="ca9cf-121">**SyncScope-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="ca9cf-121">**SyncScope element values**</span></span>

|<span data-ttu-id="ca9cf-122">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ca9cf-122">**Value**</span></span>|<span data-ttu-id="ca9cf-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca9cf-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca9cf-124">NormalItems</span><span class="sxs-lookup"><span data-stu-id="ca9cf-124">NormalItems</span></span>  <br/> |<span data-ttu-id="ca9cf-125">Gibt an, dass nur Elemente in dem Ordner in einer Synchronisierungsantwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-125">Specifies that only items in the folder are returned in a synchronization response.</span></span>  <br/> |
|<span data-ttu-id="ca9cf-126">NormalAndAssociatedItems</span><span class="sxs-lookup"><span data-stu-id="ca9cf-126">NormalAndAssociatedItems</span></span>  <br/> |<span data-ttu-id="ca9cf-127">Gibt an, dass beide Elemente in den Ordnern und Ordnern zugeordneten Informationen in einer Synchronisierungsantwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-127">Specifies that both items in the folder and folder associated information are returned in a synchronization response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca9cf-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca9cf-128">Remarks</span></span>

<span data-ttu-id="ca9cf-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ca9cf-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca9cf-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ca9cf-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca9cf-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca9cf-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ca9cf-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ca9cf-132">Schema Name</span></span>  <br/> |<span data-ttu-id="ca9cf-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ca9cf-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ca9cf-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca9cf-134">Validation File</span></span>  <br/> |<span data-ttu-id="ca9cf-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ca9cf-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ca9cf-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ca9cf-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca9cf-137">False</span><span class="sxs-lookup"><span data-stu-id="ca9cf-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca9cf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca9cf-138">See also</span></span>



[<span data-ttu-id="ca9cf-139">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ca9cf-139">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="ca9cf-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca9cf-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

