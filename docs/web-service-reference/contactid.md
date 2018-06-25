---
title: ContactId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86f66275-1e39-48ed-bd89-ac3bffc465a7
description: Das Element ContactId identifiziert eindeutig einen Kontakt.
ms.openlocfilehash: 4fd3693ed89194c85e5f1770f1db3903d835f43e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757624"
---
# <a name="contactid"></a><span data-ttu-id="2c137-103">ContactId</span><span class="sxs-lookup"><span data-stu-id="2c137-103">ContactId</span></span>

<span data-ttu-id="2c137-104">Das Element **ContactId** identifiziert eindeutig einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="2c137-104">The **ContactId** element uniquely identifies a contact.</span></span> 
  
```XML
<ContactId Id="" ChangeKey=""/>
```

 <span data-ttu-id="2c137-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="2c137-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c137-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c137-106">Attributes and elements</span></span>

<span data-ttu-id="2c137-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c137-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c137-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c137-108">Attributes</span></span>

|<span data-ttu-id="2c137-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2c137-109">**Attribute**</span></span>|<span data-ttu-id="2c137-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c137-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c137-111">Id</span><span class="sxs-lookup"><span data-stu-id="2c137-111">Id</span></span>  <br/> |<span data-ttu-id="2c137-112">Der Textwert des **Id** -Attributs ist der Bezeichner des Kontaktelements.</span><span class="sxs-lookup"><span data-stu-id="2c137-112">The text value of the **Id** attribute is the identifier of the contact item.</span></span>  <br/> |
|<span data-ttu-id="2c137-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="2c137-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="2c137-114">Der Textwert des **ChangeKey** -Attributs ist der Key ändern des Kontaktelements.</span><span class="sxs-lookup"><span data-stu-id="2c137-114">The text value of the **ChangeKey** attribute is the change key of the contact item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2c137-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c137-115">Child elements</span></span>

<span data-ttu-id="2c137-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c137-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c137-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c137-117">Parent elements</span></span>

<span data-ttu-id="2c137-118">[AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span><span class="sxs-lookup"><span data-stu-id="2c137-118">[AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c137-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c137-119">Remarks</span></span>

<span data-ttu-id="2c137-120">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2c137-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2c137-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2c137-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c137-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2c137-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c137-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c137-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c137-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c137-124">Schema name</span></span>  <br/> |<span data-ttu-id="2c137-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="2c137-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c137-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c137-126">Validation file</span></span>  <br/> |<span data-ttu-id="2c137-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c137-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c137-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="2c137-128">Can be empty</span></span>  <br/> |<span data-ttu-id="2c137-129">false</span><span class="sxs-lookup"><span data-stu-id="2c137-129">false</span></span>  <br/> |
   

