---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: Das Element RetentionAction gibt die Aktion für Elemente mit dem Aufbewahrungsrichtlinien-Tag an.
ms.openlocfilehash: 54a1038f2e56aad66f89522423ccfbd69dc44a80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831215"
---
# <a name="retentionaction"></a><span data-ttu-id="e16a3-103">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="e16a3-103">RetentionAction</span></span>

<span data-ttu-id="e16a3-104">Das Element **RetentionAction** gibt die Aktion für Elemente mit dem Aufbewahrungsrichtlinien-Tag an.</span><span class="sxs-lookup"><span data-stu-id="e16a3-104">The **RetentionAction** element specifies the action performed on items with the retention tag.</span></span> 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 <span data-ttu-id="e16a3-105">**RetentionActionType**</span><span class="sxs-lookup"><span data-stu-id="e16a3-105">**RetentionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e16a3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e16a3-106">Attributes and elements</span></span>

<span data-ttu-id="e16a3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e16a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e16a3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e16a3-108">Attributes</span></span>

<span data-ttu-id="e16a3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e16a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e16a3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e16a3-110">Child elements</span></span>

<span data-ttu-id="e16a3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e16a3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e16a3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e16a3-112">Parent elements</span></span>

[<span data-ttu-id="e16a3-113">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="e16a3-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="e16a3-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="e16a3-114">Text value</span></span>

<span data-ttu-id="e16a3-115">Der Textwert des **RetentionAction** -Elements ist die Aktion für Elemente.</span><span class="sxs-lookup"><span data-stu-id="e16a3-115">The text value of the **RetentionAction** element is the action performed on items.</span></span> <span data-ttu-id="e16a3-116">Die folgende Liste enthält die Textwerte für das **RetentionAction** -Element.</span><span class="sxs-lookup"><span data-stu-id="e16a3-116">The following list contains the text values for the **RetentionAction** element.</span></span> 
  
> <span data-ttu-id="e16a3-117">**Keine** - keine Aktion wird für das Element ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e16a3-117">**None** - No action is performed on the item.</span></span> 
    
> <span data-ttu-id="e16a3-118">**MoveToDeletedItems** - das Element wird in den Standardordner für gelöschte Objekte verschoben.</span><span class="sxs-lookup"><span data-stu-id="e16a3-118">**MoveToDeletedItems** - The item is moved to the default Deleted Items folder.</span></span> 
    
> <span data-ttu-id="e16a3-119">**MoveToFolder** - das Element wird in einem angegebenen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="e16a3-119">**MoveToFolder** - The item is moved to a specified folder.</span></span> 
    
> <span data-ttu-id="e16a3-120">**DeleteAndAllowRecovery** - das Element wird gelöscht und in die Dumpster platzieren.</span><span class="sxs-lookup"><span data-stu-id="e16a3-120">**DeleteAndAllowRecovery** - The item is deleted and put into the Dumpster.</span></span> 
    
> <span data-ttu-id="e16a3-121">**PermanentlyDelete** - das Element wird dauerhaft aus dem Postfach gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e16a3-121">**PermanentlyDelete** - The item is permanently deleted from the mailbox.</span></span> 
    
> <span data-ttu-id="e16a3-122">**MarkAsPastRetentionLimit** - Elements wird als wurde das Zeitlimit für die Aufbewahrung überschritten gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e16a3-122">**MarkAsPastRetentionLimit** - The item is marked as having exceeded the retention time limit.</span></span> 
    
> <span data-ttu-id="e16a3-123">**MoveToArchive** - das Element wird in das Archivpostfach verschoben.</span><span class="sxs-lookup"><span data-stu-id="e16a3-123">**MoveToArchive** - The item is moved to the archive mailbox.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e16a3-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e16a3-124">Remarks</span></span>

<span data-ttu-id="e16a3-125">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e16a3-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e16a3-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e16a3-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e16a3-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e16a3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e16a3-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e16a3-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e16a3-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e16a3-129">Schema name</span></span>  <br/> |<span data-ttu-id="e16a3-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e16a3-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="e16a3-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e16a3-131">Validation file</span></span>  <br/> |<span data-ttu-id="e16a3-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e16a3-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e16a3-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e16a3-133">Can be empty</span></span>  <br/> ||
   

