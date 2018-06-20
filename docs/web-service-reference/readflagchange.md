---
title: ReadFlagChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadFlagChange
api_type:
- schema
ms.assetid: 527bfe90-63d0-4b2f-97f7-7875b3a516b2
description: Das ReadFlagChange-Element wird in SyncFolderItems Vorgangsantworten zurückgegeben, wenn ein Element gelesen wurde. Diese Eigenschaft ist schreibgeschützt.
ms.openlocfilehash: 28ef0267e8308ba58057bec01ab2672a19ee94a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830953"
---
# <a name="readflagchange"></a><span data-ttu-id="05904-104">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="05904-104">ReadFlagChange</span></span>

<span data-ttu-id="05904-105">Das **ReadFlagChange** -Element wird in [SyncFolderItems Vorgang](syncfolderitems-operation.md) Antworten zurückgegeben, wenn ein Element gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="05904-105">The **ReadFlagChange** element is returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read.</span></span> <span data-ttu-id="05904-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="05904-106">This property is read-only.</span></span> 
  
```xml
<ReadFlagChange>
   <ItemId/>
   <IsRead/>
</ReadFlagChange>
```

 <span data-ttu-id="05904-107">**SyncFolderItemsReadFlagType**</span><span class="sxs-lookup"><span data-stu-id="05904-107">**SyncFolderItemsReadFlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05904-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="05904-108">Attributes and elements</span></span>

<span data-ttu-id="05904-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="05904-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05904-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="05904-110">Attributes</span></span>

<span data-ttu-id="05904-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="05904-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05904-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05904-112">Child elements</span></span>

|<span data-ttu-id="05904-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="05904-113">**Element**</span></span>|<span data-ttu-id="05904-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05904-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05904-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="05904-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="05904-116">Identifiziert das Element, für das das Lesen-Flag geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="05904-116">Identifies the item for which the read-flag has been changed.</span></span>  <br/> |
|[<span data-ttu-id="05904-117">IsRead</span><span class="sxs-lookup"><span data-stu-id="05904-117">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="05904-118">Gibt an, ob der Read-Flag auf **true**festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="05904-118">Indicates whether the read-flag has been set to **true**.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05904-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05904-119">Parent elements</span></span>

|<span data-ttu-id="05904-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="05904-120">**Element**</span></span>|<span data-ttu-id="05904-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05904-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05904-122">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="05904-122">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="05904-123">Enthält ein Array Sequenz von Dateitypen ändern, die die Typen der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="05904-123">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05904-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05904-124">Remarks</span></span>

<span data-ttu-id="05904-125">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="05904-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05904-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="05904-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05904-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="05904-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05904-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="05904-128">Schema Name</span></span>  <br/> |<span data-ttu-id="05904-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="05904-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="05904-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="05904-130">Validation File</span></span>  <br/> |<span data-ttu-id="05904-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05904-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05904-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="05904-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="05904-133">False</span><span class="sxs-lookup"><span data-stu-id="05904-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05904-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05904-134">See also</span></span>



- [<span data-ttu-id="05904-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="05904-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

