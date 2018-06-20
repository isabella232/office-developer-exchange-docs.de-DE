---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: Das RetentionPolicyType-Element gibt an, welche Richtlinie Aufbewahrung auf Elemente in einer Unterhaltung angewendet wird.
ms.openlocfilehash: dacb3fa75611cbd6e6e29eab7c791dfd8964c9ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831229"
---
# <a name="retentionpolicytype"></a><span data-ttu-id="9005e-103">RetentionPolicyType</span><span class="sxs-lookup"><span data-stu-id="9005e-103">RetentionPolicyType</span></span>

<span data-ttu-id="9005e-104">Das **RetentionPolicyType** -Element gibt an, welche Richtlinie Aufbewahrung auf Elemente in einer Unterhaltung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9005e-104">The **RetentionPolicyType** element specifies the retention policy type applied to items in a conversation.</span></span> 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 <span data-ttu-id="9005e-105">**RetentionType**</span><span class="sxs-lookup"><span data-stu-id="9005e-105">**RetentionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9005e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9005e-106">Attributes and elements</span></span>

<span data-ttu-id="9005e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9005e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9005e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9005e-108">Attributes</span></span>

<span data-ttu-id="9005e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9005e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9005e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9005e-110">Child elements</span></span>

<span data-ttu-id="9005e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9005e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9005e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9005e-112">Parent elements</span></span>

[<span data-ttu-id="9005e-113">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="9005e-113">ConversationAction</span></span>](conversationaction.md)
  
## <a name="text-value"></a><span data-ttu-id="9005e-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="9005e-114">Text value</span></span>

<span data-ttu-id="9005e-115">Der Textwert des **RetentionPolicyType** -Elements ist die Aufbewahrung auf Elemente in einer Unterhaltung angewendet.</span><span class="sxs-lookup"><span data-stu-id="9005e-115">The text value of the **RetentionPolicyType** element is the retention type applied to items in a conversation.</span></span> <span data-ttu-id="9005e-116">Der Textwert der **Löschen** gibt an, dass die Elemente in der Unterhaltung gelöscht werden, wenn das Anhalten der Aufbewahrungszeit läuft ab.</span><span class="sxs-lookup"><span data-stu-id="9005e-116">The text value of **Delete** indicates that the items in the conversation are deleted when the retention hold expires.</span></span> <span data-ttu-id="9005e-117">Der Textwert der **Archive** gibt an, dass die Elemente in der Unterhaltung in das Archivpostfach verschoben werden, wenn das Anhalten der Aufbewahrungszeit läuft ab.</span><span class="sxs-lookup"><span data-stu-id="9005e-117">The text value of **Archive** indicates that the items in the conversation are moved to the archive mailbox when the retention hold expires.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9005e-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9005e-118">Remarks</span></span>

<span data-ttu-id="9005e-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9005e-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9005e-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9005e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9005e-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9005e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9005e-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="9005e-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9005e-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9005e-123">Schema name</span></span>  <br/> |<span data-ttu-id="9005e-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9005e-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="9005e-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9005e-125">Validation file</span></span>  <br/> |<span data-ttu-id="9005e-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9005e-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9005e-127">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9005e-127">Can be empty</span></span>  <br/> ||
   

