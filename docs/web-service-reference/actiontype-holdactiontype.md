---
title: ActionType (HoldActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f50449b9-e73b-43c5-af96-6433bf434dce
description: ActionType-Element gibt den Typ der Aktion für den Haltestatus an.
ms.openlocfilehash: cb1cfa8a1306c4a6cacf5c82824d19cab57e7941
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757210"
---
# <a name="actiontype-holdactiontype"></a><span data-ttu-id="7fc32-103">ActionType (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="7fc32-103">ActionType (HoldActionType)</span></span>

<span data-ttu-id="7fc32-104">**ActionType** -Element gibt den Typ der Aktion für den Haltestatus an.</span><span class="sxs-lookup"><span data-stu-id="7fc32-104">The **ActionType** element indicates the type of action for the hold.</span></span> 
  
```XML
<ActionType> Create | Update | Remove </ActionType>
```

 <span data-ttu-id="7fc32-105">**HoldActionType**</span><span class="sxs-lookup"><span data-stu-id="7fc32-105">**HoldActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fc32-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7fc32-106">Attributes and elements</span></span>

<span data-ttu-id="7fc32-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7fc32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fc32-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fc32-108">Attributes</span></span>

<span data-ttu-id="7fc32-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fc32-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7fc32-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fc32-110">Child elements</span></span>

<span data-ttu-id="7fc32-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fc32-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7fc32-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fc32-112">Parent elements</span></span>

[<span data-ttu-id="7fc32-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="7fc32-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="7fc32-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="7fc32-114">Text value</span></span>

<span data-ttu-id="7fc32-115">Der Textwert der **ActionType** -Element ist der Typ des Haltestatus für ein Postfach festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7fc32-115">The text value of the **ActionType** element is the type of hold set on a mailbox.</span></span> <span data-ttu-id="7fc32-116">**Erstellen** ein Textwerts gibt an, dass es sich bei ein Haltestatus Postfach erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc32-116">A text value of **Create** indicates that a mailbox hold will be created.</span></span> <span data-ttu-id="7fc32-117">Der **Aktualisierung** ein Textwerts gibt an, dass ein Haltestatus Postfach aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fc32-117">A text value of **Update** indicates that a mailbox hold will be updated.</span></span> <span data-ttu-id="7fc32-118">Ein Textwert der **Entfernen** gibt an, dass ein Postfach Haltebereich entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc32-118">A text value of **Remove** indicates that a mailbox hold will be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7fc32-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7fc32-119">Remarks</span></span>

<span data-ttu-id="7fc32-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7fc32-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7fc32-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7fc32-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fc32-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7fc32-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fc32-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fc32-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7fc32-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7fc32-124">Schema name</span></span>  <br/> |<span data-ttu-id="7fc32-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7fc32-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="7fc32-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7fc32-126">Validation file</span></span>  <br/> |<span data-ttu-id="7fc32-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7fc32-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7fc32-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7fc32-128">Can be empty</span></span>  <br/> |<span data-ttu-id="7fc32-129">false</span><span class="sxs-lookup"><span data-stu-id="7fc32-129">false</span></span>  <br/> |
   

