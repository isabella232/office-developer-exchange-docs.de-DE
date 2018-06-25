---
title: GroupId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 656d9b9a-8a65-4a75-8466-5b0d96512dab
description: Das GroupId-Element wird eine Gruppe eindeutig identifiziert.
ms.openlocfilehash: eaba176321c0dd872b71ef50cbaa298d1277bb79
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829750"
---
# <a name="groupid"></a><span data-ttu-id="a1bce-103">GroupId</span><span class="sxs-lookup"><span data-stu-id="a1bce-103">GroupId</span></span>

<span data-ttu-id="a1bce-104">Das **GroupId** -Element wird eine Gruppe eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a1bce-104">The **GroupId** element uniquely identifies a group.</span></span> 
  
```XML
<GroupId Id="" ChangeKey=""/>
```

 <span data-ttu-id="a1bce-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="a1bce-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a1bce-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a1bce-106">Attributes and elements</span></span>

<span data-ttu-id="a1bce-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a1bce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1bce-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a1bce-108">Attributes</span></span>

|<span data-ttu-id="a1bce-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a1bce-109">**Attribute**</span></span>|<span data-ttu-id="a1bce-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1bce-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1bce-111">Id</span><span class="sxs-lookup"><span data-stu-id="a1bce-111">Id</span></span>  <br/> |<span data-ttu-id="a1bce-112">Der Textwert des **Id** -Attributs ist der Bezeichner der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a1bce-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="a1bce-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="a1bce-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="a1bce-114">Der Textwert des **ChangeKey** -Attributs ist der Key Ändern der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a1bce-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a1bce-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1bce-115">Child elements</span></span>

<span data-ttu-id="a1bce-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="a1bce-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a1bce-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1bce-117">Parent elements</span></span>

<span data-ttu-id="a1bce-118">[AddNewImContactToGroup](addnewimcontacttogroup.md) | [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md) | [AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md) | [RemoveImGroup](removeimgroup.md)  |  [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md) | [SetImGroup](setimgroup.md)</span><span class="sxs-lookup"><span data-stu-id="a1bce-118">[AddNewImContactToGroup](addnewimcontacttogroup.md) | [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md) | [AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md) | [RemoveImGroup](removeimgroup.md) | [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md) | [SetImGroup](setimgroup.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a1bce-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a1bce-119">Remarks</span></span>

<span data-ttu-id="a1bce-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a1bce-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a1bce-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a1bce-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1bce-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a1bce-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1bce-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1bce-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a1bce-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a1bce-124">Schema name</span></span>  <br/> |<span data-ttu-id="a1bce-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a1bce-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a1bce-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a1bce-126">Validation file</span></span>  <br/> |<span data-ttu-id="a1bce-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a1bce-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a1bce-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a1bce-128">Can be empty</span></span>  <br/> ||
   

