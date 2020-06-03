---
title: FolderNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderNames
api_type:
- schema
ms.assetid: 6cbe4083-5705-4695-a54e-8dab3e472662
description: Das FolderNames-Element enthält ein Array benannter verwalteter Ordner, die einem Postfach hinzugefügt werden sollen.
ms.openlocfilehash: 00cb1a81f420469033ccbc745313d2719b155aff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530986"
---
# <a name="foldernames"></a><span data-ttu-id="42419-103">FolderNames</span><span class="sxs-lookup"><span data-stu-id="42419-103">FolderNames</span></span>

<span data-ttu-id="42419-104">Das **FolderNames** -Element enthält ein Array benannter verwalteter Ordner, die einem Postfach hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42419-104">The **FolderNames** element contains an array of named managed folders to add to a mailbox.</span></span> 
  
[<span data-ttu-id="42419-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="42419-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="42419-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="42419-106">FolderNames</span></span>](foldernames.md)
  
```xml
<FolderNames>
   <FolderName/>
</FolderNames>
```

 <span data-ttu-id="42419-107">**NonEmptyArrayOfFolderNamesType**</span><span class="sxs-lookup"><span data-stu-id="42419-107">**NonEmptyArrayOfFolderNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42419-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="42419-108">Attributes and elements</span></span>

<span data-ttu-id="42419-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="42419-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42419-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="42419-110">Attributes</span></span>

<span data-ttu-id="42419-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="42419-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42419-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42419-112">Child elements</span></span>

|<span data-ttu-id="42419-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="42419-113">**Element**</span></span>|<span data-ttu-id="42419-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42419-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42419-115">FolderName</span><span class="sxs-lookup"><span data-stu-id="42419-115">FolderName</span></span>](foldername.md) <br/> |<span data-ttu-id="42419-116">Gibt einen einzelnen verwalteten Ordner an, der dem Postfach hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="42419-116">Identifies a single managed folder to add to mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="42419-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42419-117">Parent elements</span></span>

|<span data-ttu-id="42419-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="42419-118">**Element**</span></span>|<span data-ttu-id="42419-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42419-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42419-120">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="42419-120">CreateManagedFolder</span></span>](createmanagedfolder.md) <br/> |<span data-ttu-id="42419-121">Das Stammelement in einer Anforderung zum Hinzufügen eines verwalteten Ordners zu einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="42419-121">The root element in a request to add a managed folder to a mailbox.</span></span>  <br/> <span data-ttu-id="42419-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="42419-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42419-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42419-123">Remarks</span></span>

<span data-ttu-id="42419-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="42419-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42419-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="42419-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42419-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="42419-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="42419-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="42419-127">Schema Name</span></span>  <br/> |<span data-ttu-id="42419-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="42419-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="42419-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="42419-129">Validation File</span></span>  <br/> |<span data-ttu-id="42419-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="42419-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="42419-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="42419-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="42419-132">False</span><span class="sxs-lookup"><span data-stu-id="42419-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42419-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42419-133">See also</span></span>



[<span data-ttu-id="42419-134">FindFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="42419-134">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="42419-135">Suchen von Ordnern</span><span class="sxs-lookup"><span data-stu-id="42419-135">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="42419-136">Hinzufügen von verwalteten Ordnern</span><span class="sxs-lookup"><span data-stu-id="42419-136">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

