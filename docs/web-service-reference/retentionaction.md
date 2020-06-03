---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: Das Retention Action-Element gibt die Aktion an, die für Elemente mit dem Aufbewahrungs Tag ausgeführt wird.
ms.openlocfilehash: c16988413e732ddc3cd6ebc355cb73c4d96550c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465233"
---
# <a name="retentionaction"></a><span data-ttu-id="75c49-103">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="75c49-103">RetentionAction</span></span>

<span data-ttu-id="75c49-104">Das **Retention** Action-Element gibt die Aktion an, die für Elemente mit dem Aufbewahrungs Tag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75c49-104">The **RetentionAction** element specifies the action performed on items with the retention tag.</span></span> 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 <span data-ttu-id="75c49-105">**RetentionActionType**</span><span class="sxs-lookup"><span data-stu-id="75c49-105">**RetentionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75c49-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="75c49-106">Attributes and elements</span></span>

<span data-ttu-id="75c49-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="75c49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75c49-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="75c49-108">Attributes</span></span>

<span data-ttu-id="75c49-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="75c49-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75c49-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75c49-110">Child elements</span></span>

<span data-ttu-id="75c49-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="75c49-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="75c49-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75c49-112">Parent elements</span></span>

[<span data-ttu-id="75c49-113">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="75c49-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="75c49-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="75c49-114">Text value</span></span>

<span data-ttu-id="75c49-115">Der Textwert des Elements **Retention** Action ist die für Elemente ausgeführte Aktion.</span><span class="sxs-lookup"><span data-stu-id="75c49-115">The text value of the **RetentionAction** element is the action performed on items.</span></span> <span data-ttu-id="75c49-116">Die folgende Liste enthält die Textwerte für das **Retention** -Element.</span><span class="sxs-lookup"><span data-stu-id="75c49-116">The following list contains the text values for the **RetentionAction** element.</span></span> 
  
> <span data-ttu-id="75c49-117">**None** : für das Element wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75c49-117">**None** - No action is performed on the item.</span></span> 
    
> <span data-ttu-id="75c49-118">**MoveToDeletedItems** – das Element wird in den Standardordner "Gelöschte Elemente" verschoben.</span><span class="sxs-lookup"><span data-stu-id="75c49-118">**MoveToDeletedItems** - The item is moved to the default Deleted Items folder.</span></span> 
    
> <span data-ttu-id="75c49-119">**MoveToFolder** – das Element wird in einen angegebenen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="75c49-119">**MoveToFolder** - The item is moved to a specified folder.</span></span> 
    
> <span data-ttu-id="75c49-120">**DeleteAndAllowRecovery mit** – das Element wird gelöscht und in den Papierkorb verschoben.</span><span class="sxs-lookup"><span data-stu-id="75c49-120">**DeleteAndAllowRecovery** - The item is deleted and put into the Dumpster.</span></span> 
    
> <span data-ttu-id="75c49-121">**PermanentlyDelete** – das Element wird endgültig aus dem Postfach gelöscht.</span><span class="sxs-lookup"><span data-stu-id="75c49-121">**PermanentlyDelete** - The item is permanently deleted from the mailbox.</span></span> 
    
> <span data-ttu-id="75c49-122">**MarkAsPastRetentionLimit** – das Element wird als das Beibehaltungs Zeitlimit überschritten markiert.</span><span class="sxs-lookup"><span data-stu-id="75c49-122">**MarkAsPastRetentionLimit** - The item is marked as having exceeded the retention time limit.</span></span> 
    
> <span data-ttu-id="75c49-123">**MoveToArchive mit** – das Element wird in das Archivpostfach verschoben.</span><span class="sxs-lookup"><span data-stu-id="75c49-123">**MoveToArchive** - The item is moved to the archive mailbox.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="75c49-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75c49-124">Remarks</span></span>

<span data-ttu-id="75c49-125">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="75c49-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="75c49-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="75c49-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75c49-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="75c49-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75c49-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="75c49-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="75c49-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="75c49-129">Schema name</span></span>  <br/> |<span data-ttu-id="75c49-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="75c49-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="75c49-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="75c49-131">Validation file</span></span>  <br/> |<span data-ttu-id="75c49-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="75c49-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="75c49-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="75c49-133">Can be empty</span></span>  <br/> ||
   

