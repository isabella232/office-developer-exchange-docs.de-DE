---
title: ReferenceAttachmentType ComplexType (EWS)
manager: sethgros
ms.date: 03/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
ms.openlocfilehash: da9ff2b73f86bba3003c31dec009ea11a9b26b32
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831030"
---
# <a name="referenceattachmenttype-complextype-ews"></a><span data-ttu-id="d1e66-102">ReferenceAttachmentType ComplexType (EWS)</span><span class="sxs-lookup"><span data-stu-id="d1e66-102">ReferenceAttachmentType complexType (EWS)</span></span>

## <a name="type-information"></a><span data-ttu-id="d1e66-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d1e66-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1e66-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d1e66-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1e66-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d1e66-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d1e66-106">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1e66-106">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1e66-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d1e66-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d1e66-108">t:AttachmentType</span><span class="sxs-lookup"><span data-stu-id="d1e66-108">t:AttachmentType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d1e66-109">Definition</span><span class="sxs-lookup"><span data-stu-id="d1e66-109">Definition</span></span>

```XML
<xs:complexType name="ReferenceAttachmentType">
    <xs:complexContent>
        <xs:extension base="t:AttachmentType">
            <xs:sequence>
                <xs:element name="AttachLongPathName" type="xs:string" maxOccurs="1" minOccurs="0"></xs:element>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="d1e66-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d1e66-110">Elements and attributes</span></span>

<span data-ttu-id="d1e66-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="d1e66-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d1e66-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1e66-112">Child elements</span></span>

|<span data-ttu-id="d1e66-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1e66-113">**Element**</span></span>|<span data-ttu-id="d1e66-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d1e66-114">**Type**</span></span>|<span data-ttu-id="d1e66-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1e66-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d1e66-116">AttachLongPathName</span><span class="sxs-lookup"><span data-stu-id="d1e66-116">AttachLongPathName</span></span>](http://msdn.microsoft.com/library/98464422-2c13-8d33-0fe3-b1978f2d5b4a%28Office.15%29.aspx) <br/> |<span data-ttu-id="d1e66-117">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1e66-117">xs:string</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d1e66-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1e66-118">Attributes</span></span>

<span data-ttu-id="d1e66-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1e66-119">None.</span></span>
  

