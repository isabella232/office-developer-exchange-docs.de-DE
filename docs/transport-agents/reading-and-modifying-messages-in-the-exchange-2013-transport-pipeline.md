---
title: Lesen und Ändern von Nachrichten in der Exchange 2013-Transportpipeline
manager: sethgros
ms.date: 09/17/2021
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b53ed47a-3d01-4c4e-ad32-fb0532872aad
description: Erfahren Sie mehr über die .NET Framework Klassen, die Sie in Ihren Exchange 2013-Transport-Agents zum Lesen, Schreiben und Ändern von Nachrichten verwenden können.
ms.openlocfilehash: 5bf4406f7ca82512bb55388e0865e0d343cae66e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537236"
---
# <a name="reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline"></a>Lesen und Ändern von Nachrichten in der Exchange 2013-Transportpipeline

Erfahren Sie mehr über die .NET Framework Klassen, die Sie in Ihren Exchange 2013-Transport-Agents zum Lesen, Schreiben und Ändern von Nachrichten verwenden können.
  
**Gilt für:** Exchange Server 2013
  
- Klassen zum Lesen, Schreiben oder Ändern von Nachrichten
- Encoder-Namespace
- iCalendar-Namespace
- MIME-Namespace
- TextConverters-Namespace
- Tnef-Namespace
- vCard-Namespace
  
Wenn Nachrichten die Transportpipeline durchlaufen, kann Ihr Transport-Agent Nachrichteninhalte zwischen verschiedenen Datenformaten lesen, schreiben und konvertieren. Sie können beispielsweise MIME-Daten lesen und schreiben, eingehende Nachrichten im Format Uuencoded oder Quoted-printable (qp) identifizieren und dann in einen von Ihrer Organisation verwendeten Standard konvertieren oder Kalender- oder Kontaktinformationen im Zusammenhang mit eingehenden Nachrichten lesen und speichern. 
  
Sie können auch Inhalte identifizieren, die eine Sicherheitsgefährdung darstellen, und den Inhalt oder die Nachrichten, die sie enthalten, verschieben oder löschen. Beispielsweise durch Entfernen von Links in einer HTML-Nachricht.
  
Dieser Artikel enthält Informationen zu den .NET Framework Klassen, die Sie zum Lesen, Schreiben und Ändern von Nachrichten verwenden können.
  
> [!CAUTION]
> Viele der Eigenschaften und Parameter in den Inhaltskonvertierungs-APIs ermöglichen Werte, die groß genug sind, um Leistungsprobleme zu verursachen, einschließlich Denial-of-Service. Wenn Sie die Inhaltskonvertierungs-APIs in einem Transport-Agent verwenden, sollten Sie Grenzwerte für die Eigenschaften- und Parameterwertgrößen implementieren, die Sie beim Lesen oder Schreiben unterstützen, um den Ressourcenverbrauch ihres Agents zu begrenzen. 

<a name="Namespaces"> </a>

## <a name="classes-used-to-read-write-or-modify-messages"></a>Klassen zum Lesen, Schreiben oder Ändern von Nachrichten

In der folgenden Tabelle sind die .NET Framework Klassen aufgeführt, die Sie zum Lesen, Schreiben und Ändern von E-Mail-Nachrichten verwenden können.
  
**.NET Framework-Namespaces für die Nachrichtenverarbeitung**

|**.NET Framework Namespace**|**Kurse**|
|:-----|:-----|
|[Microsoft. Exchange. Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Enthält Klassen für die In-Memory-Codierung und -Decodierung, eine Encoderstreamklasse, die eine der Encoder- oder Decoderklassen akzeptiert, die in einer zugeordneten Enumeration enthalten sind, und die [ByteEncoder-Basisklasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) und [die ByteEncoderException-Ausnahmeklasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) für die Encoder und Decoder.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Enthält Typen, mit denen Sie Datenströme lesen und schreiben können, die Kalenderinformationen enthalten. Enthält einen Kalenderleser und -writer, ein Ausnahmeobjekt, ein Serienobjekt sowie Strukturen und Enumerationen, mit denen Sie Eigenschafteninformationen zu Kalenderelementen zurückgeben können.  <br/> |
|[Microsoft. Exchange. Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Enthält Klassen, Strukturen, Enumerationen und Delegaten, die Sie zum Erstellen, Lesen, Schreiben, Durchlaufen, Codieren und Decodieren von MIME-Daten verwenden können. Enthält einen streambasierten Reader und Writer, mit dem Sie nur Lese- und Schreibzugriff auf MIME-Datenströme sowie DOM-basierte Methoden und Klassen erhalten, die Sie in MIME-Dokumenten verwenden können.  <br/> |
|[Microsoft. Exchange. Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Enthält Klassen, Strukturen, Enumerationen und Stellvertretungen, mit denen Sie einen Datenstrom lesen und schreiben und Konvertierungen zwischen bestimmten Datentypen ausführen können. Beispielsweise HTML in RtF (Rich Text Format). Textkonverter ermöglichen es Ihnen, das Format eines Dokumentdatenstroms von einem Formular in ein anderes zu ändern und Elemente eines Dokuments selektiv zu entfernen, die ein Sicherheitsrisiko darstellen könnten.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Enthält einen Vorwärtsstreamleser und Writer, eine Ausnahmeklasse sowie Strukturen und Enumerationen, die das Lesen und Schreiben von TNEF-Daten (Transport Neutral Encapsulation Format) erleichtern.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Enthält einen Vorwärtsdatenstromleser und -writer, eine Ausnahmeklasse sowie Strukturen und Enumerationen, die das Lesen und Schreiben vCard-formatierter Kontaktdaten erleichtern.  <br/> |
   
## <a name="encoders-namespace"></a>Encoder-Namespace
<a name="Encoders"> </a>

Der Encoder-Namespace enthält Klassen für die In-Memory-Codierung und -Decodierung. Diese erben von der [ByteEncoder-Basisklasse.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) Klassen codieren und decodieren für Base64, BinHex, Quoted-printable (qp) und Unix-to-Unix (Uu). Die folgenden Klassen werden für die In-Memory-Codierung und -Decodierung verwendet: 
  
- [Base64Encoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Encoder.aspx)
    
- [Base64Decoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Decoder.aspx)
    
- [BinHexEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexEncoder.aspx)
    
- [BinHexDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexDecoder.aspx)
    
- [QPEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPEncoder.aspx)
    
- [QPDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPDecoder.aspx)
    
- [UUEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUEncoder.aspx)
    
- [UUDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUDecoder.aspx)
    
Die Encoder und Decoder erben von der [ByteEncoder-Basisklasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) und verwenden die [ByteEncoderException-Ausnahmeklasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) für die Fehlerbehandlung. 
  
Darüber hinaus enthält der Namespace die [MacBinaryHeader-Klasse,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.MacBinaryHeader.aspx) die MacBinary-codierte Dateien identifiziert und den zugehörigen Dateiheader liest. 
  
Schließlich führt die [EncoderStream-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStream.aspx) eine Konvertierung für einen Datenstrom anstelle eines Speicherobjekts durch. Diese Klasse akzeptiert eine der Encoder- oder Decoderklassen und liest oder schreibt gemäß der zugeordneten [EncoderStreamAccess-Enumeration.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStreamAccess.aspx) 
  
## <a name="icalendar-namespace"></a>iCalendar-Namespace
<a name="iCalendar"> </a>

Der iCalendar-Namespace bietet einen vorwärtsgerichteten Reader und Writer für iCalendar-Daten sowie unterstützende Strukturen und Klassen zum Erstellen, Zugreifen und Ändern von iCalendar-Datenströmen.
  
Die [Klassen CalendarReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.aspx) und [CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx) werden zum Lesen und Schreiben von iCalendar-Datenstrom verwendet. 
  
CalendarReader verwendet einen lesbaren [Stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx) als Argument für seine Konstruktoren. Anschließend können Sie die Methoden [ReadFirstChildComponent,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadFirstChildComponent.aspx) [ReadNextSiblingComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextSiblingComponent.aspx)und [ReadNextComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextComponent.aspx) verwenden, um sequenziell auf die iCalendar-Komponenten im Datenstrom zuzugreifen. Basierend auf dem Wert, den Sie für die [ComplianceMode-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceMode.aspx) festgelegt haben, führen Fehler im iCalendar-Stream dazu, dass eine Ausnahme ausgelöst wird oder die [ComplianceStatus-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceStatus.aspx) auf einen anderen Wert als ["Kompatibel"](https://msdn.microsoft.com/library/microsoft.exchange.data.contenttypes.icalendar.calendarcompliancestatus.aspx)festgelegt wird. Sie können diese Eigenschaft überprüfen, um Probleme mit eingehenden iCalendar-Daten zu ermitteln. 
  
Die [CalendarWriter-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx) verwendet einen beschreibbaren [Stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx) als Argument für ihre Konstruktoren. 
  
## <a name="mime-namespace"></a>MIME-Namespace
<a name="MIME"> </a>

Der MIME-Namespace stellt Klassen bereit, mit denen Sie MIME-Dokumente erstellen, darauf zugreifen und diese ändern können. Sie können mit MIME-Dokumenten arbeiten, indem Sie entweder eine stream- oder DOM-basierte Methode verwenden.
  
### <a name="mimedocument-class-and-the-mime-dom"></a>MimeDocument-Klasse und MIME-DOM

Die [MimeDocument-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) ermöglicht den DOM-Zugriff auf ein MIME-Dokument. Verwenden Sie Objekte dieses Typs, wenn Sie über den verfügbaren Arbeitsspeicher verfügen, um ein gesamtes DOM zu laden, und Sie zufälligen Zugriff auf die Kopfzeilen und den Inhalt der Nachricht haben müssen. 
  
Sie laden Daten mithilfe der [GetLoadStream-](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.GetLoadStream.aspx) oder [Load-Methoden](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.Load.aspx) in ein [MimeDocument-Objekt.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) Anschließend können Sie die DOM-Hierarchie durchlaufen und MIME-Daten erstellen, ändern oder entfernen. Nachdem Sie die MIME-Daten geändert haben, können Sie sie mithilfe einer der [WriteTo-Methoden](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeNode.WriteTo.aspx) in einen Datenstrom schreiben. 
  
Die folgende Abbildung zeigt die Struktur von Daten innerhalb eines [MimeDocument-Objekts.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) 
  
**Abbildung 1. Struktur von MimeDocument-Objekten**

![MIME DOM-Architektur](media/MimeDomArchitecture.gif)
  
### <a name="mimereader-and-mimewriter-classes-and-stream-based-mime-parsing"></a>MimeReader- und MimeWriter-Klassen und streambasierte MIME-Analyse

Die [MimeReader-](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) und [MimeWriter-Klassen](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) ermöglichen den vorwärtsgerichteten Zugriff auf MIME-Datenströme. Verwenden Sie diese Klassen, wenn Sie die MIME-Daten, die bereits gelesene oder geschriebene Daten erfordern, nicht ändern müssen. Wenn Sie beispielsweise Nachrichten drucken möchten, die in ein vordefiniertes Format passen, ist die [MimeWriter-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) möglicherweise ideal. 
  
Die [MimeDocument-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) kapselt ein DOM. Die [Klassen MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) und [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) stellen Zustandscomputer dar. Ihre Zustände ändern sich basierend auf der empfangenen Eingabe und den aufgerufenen Methoden. Die Abbildungen 2 bis 5 sind vereinfachte Zustandsübergangsdiagramme, die für das [MimeReader-Objekt](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) zeigen, welche Methoden gültig sind, um von jedem Zustand aus aufzurufen, sowie den zustand, der sich daraus ergeben wird. 
  
Um diese Diagramme zu verwenden, folgen Sie den Pfeilen von einem Zustand zum nächsten, wobei Sie die Methodenaufrufe notieren oder Werte zurückgeben, die zu einer Änderung des Zustands führen. Gehen Sie beispielsweise im ersten Diagramm davon aus, dass Sie sich am Anfang des Datenstroms befinden, der zu dem von Ihnen erstellten MimeReader gehört. Rufen Sie zum Abrufen des Zustands "Part Headers" einen von [ReadNextPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadNextPart.aspx) oder ReadFirstChildPart in dieser Reihenfolge auf. [](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadFirstChildPart.aspx) Wenn Kopfzeilen vorhanden sind (d. h., wenn mime wohlgeformt ist), geben Sie den Status "Part Headers" ein. Andernfalls wird eine Ausnahme ausgelöst. 
  
**Abbildung 2. Vereinfachtes Zustandsübergangsdiagramm für MimeReader-Objekte**

![MimeReader-Statusdiagramm](media/MimeReader_StateDiagram_01.gif)
  
> [!NOTE]
> Die Abbildungen 3, 4 und 5 erweitern die Zustände, die in den vorherigen Diagrammen dargestellt sind. 
  
**Abbildung 3. Erweiterung des Status "Part Headers" ab Abbildung 2**

![Erweiterung des Status "Part-Kopfzeilen"](media/MimeReader_StateDiagram_02.gif)
  
**Abbildung 4. Erweiterung des Headerstatus von Abbildung 3, wenn ein Parameter in einer Kopfzeile gefunden wurde**

![Erweiterung des Status "Part Headers", wenn ein Parameter in einer Kopfzeile gefunden wurde](media/MimeReader_StateDiagram_03.gif)
  
> [!NOTE]
> Der von Abbildung 5 dargestellte Zustand ist rekursiv. Wenn eine Adressgruppe gefunden wird, können Sie die [GroupRecipientReader-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeAddressReader.GroupRecipientReader.aspx) verwenden, um die Adressen in der Gruppe zu lesen. 
  
**Abbildung 5. Erweiterung des Headerstatus ab Abbildung 3, wenn eine Adresse oder Adressgruppe gefunden wird**

![Erweiterung des Status "Kopfzeilen" für eine Adresse oder Gruppe](media/MimeReader_StateDiagram_04.gif)
  
Die Abbildungen 6 und 7 zeigen diagramme für den vereinfachten Zustandsübergang für das [MimeWriter-Objekt.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) 
  
> [!NOTE]
> Abbildung 7 wird auf den Status der Teilkopfzeilen in Abbildung 6 erweitert. 
  
**Abbildung 6. Vereinfachtes Zustandsübergangsdiagramm für MimeWriter-Objekte**

![Statusübergang-Diagramm für MimeWriter](media/MimeWriter_TopLevel.gif)
  
**Abbildung 7. Erweiterung des Zustands "Part Headers" in Abbildung 6**

![Statusübergang-Diagrammerweiterung für MimeWriter](media/MimeWriter_Diagram_Expansion.gif)
  
## <a name="textconverters-namespace"></a>TextConverters-Namespace
<a name="TextConverters"> </a>

Der TextConverters-Namespace enthält Typen, die die Konvertierung des Inhalts von E-Mail-Nachrichten unterstützen. Diese Typen können eine Codeseitenkonvertierung ausführen, nicht sichere HTML entfernen und andere Transformationen für E-Mail-Nachrichtentext ausführen. Die [Microsoft.Exchange. Der Data.TextConverters-Namespace](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) enthält die folgenden Klassen, die von der abstrakten [Klasse "TextConverter"](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) abgeleitet sind: 
  
- [EnrichedToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.EnrichedToHtml.aspx)
    
- [EnrichedToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.EnrichedToText.aspx)
    
- [HtmlToEnriched](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToEnriched.aspx)
    
- [HtmlToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToHtml.aspx)
    
- [Htmltortf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToRtf.aspx)
    
- [HtmlToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToText.aspx)
    
- [RtfCompressedToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfCompressedToRtf.aspx)
    
- [RtfToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToHtml.aspx)
    
- [RtfToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToRtf.aspx)
    
- [RtfToRtfCompressed](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToRtfCompressed.aspx)
    
- [RtfToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToText.aspx)
    
- [TextToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToHtml.aspx)
    
- [TextToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToRtf.aspx)
    
- [TextToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToText.aspx)
    
Mit diesen Textkonvertern können Sie das Format eines Dokumentdatenstroms ändern oder Elemente entfernen, die nicht sicher in einem HTML-Dokument sind. Diese Klassen können selbst verwendet werden, um eine Konvertierung mithilfe eines einzelnen Aufrufs einer der Convert-Methoden in der [TextConverter-Basisklasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) durchzuführen, oder sie können an einen Konstruktor des Konverters übergeben werden, der sie zum Ausführen konvertierter Lese- oder Schreibvorgänge verwendet. 
  
Die von der Basisklasse geerbte Funktionalität ist nützlich, um Konvertierungen durchzuführen, wenn Sie über genügend Speicherplatz zum Speichern des Originaldokuments und der konvertierten Ausgabe verfügen oder wenn Sie die Ergebnisse der Konvertierung speichern möchten. Die **Convert-Methode** verwendet Eingabe- und Ausgabedatenströme, Textleser oder Textautoren und konvertiert den Inhalt der Eingabe in die zugeordnete Ausgabe. 
  
Ebenfalls im Namespace enthalten sind die folgenden Textlese-, Writer- und Streamklassen:
  
- [ConverterReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterReader.aspx) - Abgeleitet von **System.IO.TextReader**. 
    
- [ConverterWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterWriter.aspx) - Abgeleitet von **System.IO.TextWriter**. 
    
- [ConverterStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterStream.aspx) - Abgeleitet von **System.IO.Stream**. 
    
Diese werden verwendet, um Konvertierungen durchzuführen, wenn Sie keinen Platz zum Speichern der ursprünglichen oder der konvertierten Ausgabe haben, wenn Sie die Eingabe von einem Datenstrom empfangen oder an einen Stream senden oder wenn Sie die Ausgabe nur für Indizierungs- oder Suchzwecke verwenden möchten und daher das Ergebnis einer Konvertierung nicht speichern möchten.
  
## <a name="tnef-namespace"></a>Tnef-Namespace
<a name="TNEF"> </a>

Der Tnef-Namespace enthält Klassen und Typen, die das vorwärtsgerichtete streambasierte Lesen und Schreiben von TNEF-Daten ermöglichen. TNEF ist ein Datenformat, das verwendet wird, um MAPI-Eigenschaften für Clients zu kapseln, die MAPI nicht interpretieren können.
  
Die [Klassen TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) und [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) stellen die Kernfunktionen in der [Microsoft.Exchange bereit. Data.ContentTypes.Tnef-Namespace.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) 
  
Die [TnefReader-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) verwendet einen lesbaren Datenstrom als Argument für ihre Konstruktoren. Anschließend verwenden Sie die [ReadNextAttribute-Methode,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadNextAttribute.aspx) um die Attribute im TNEF-Stream sequenziell zu lesen. Nachdem Sie ein Attribut gelesen haben, können Sie auf Informationen über das Attribut zugreifen, indem Sie eine der schreibgeschützten Eigenschaften für das [TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) -Objekt verwenden, zusätzlich zum Abrufen eines [TnefPropertyReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefPropertyReader.aspx) zum Lesen der aktuellen Eigenschaft. Mithilfe der [ReadAttributeRawValue-Methode](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadAttributeRawValue.aspx) können Sie auch direkt auf das aktuelle Attribut zugreifen. 
  
Die [TnefWriter-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) verwendet einen schreibbaren [Stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx) als Argument für die Konstruktoren. Die [TnefWriter-Klasse](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) bietet mehrere Möglichkeiten zum Schreiben von Daten in diesen Datenstrom. 
  
## <a name="vcard-namespace"></a>vCard-Namespace
<a name="vCard"> </a>

Der vCard-Namespace enthält Klassen, Strukturen und Enumerationen, die zum Lesen und Schreiben von Kontaktinformationen verwendet werden, die in einer E-Mail-Nachricht im vCard-Datenformat enthalten sind. Der Namespace enthält einen Kontaktleser und Writer, eine Ausnahmeklasse, einen Eigenschaftenleser, einen Parameterleser und unterstützende Enumerationen, mit denen Sie vCard-Daten lesen können, die einer E-Mail-Nachricht zugeordnet sind.
  
## <a name="see-also"></a>Siehe auch

- [Transport-Agents in Exchange](transport-agents-in-exchange-2013.md)  
- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [MIME-Medientypen](http://www.iana.org/assignments/media-types)
    

