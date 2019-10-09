---
title: Assets Supported Formats
seo-title: Assets Supported Formats
description: List of file formats supported by AEM Assets and features supported for each format.
seo-description: List of file formats supported by AEM Assets and features supported for each format.
uuid: 56debf26-d67f-4bca-933c-5eb4ec9d2865
contentOwner: asgupta
products: SG_EXPERIENCEMANAGER/6.4/ASSETS
discoiquuid: 8519f029-3dd1-4325-9758-e6b5b530a0ee
---

# Assets Supported Formats {#assets-supported-formats}

AEM Assets supports a wide range of file formats and each functionality has varied support for different MIME types.

To integrate AEM Assets with other standards-compliant digital asset management (DAM) solutions and desktop software, use Adobe's Extensible Metadata Platform (XMP).

Use the legend to understand the support level.

| Support Level |          Description           |
| ------------- | ------------------------------ |
| x             | Supported                      |
| *             | Supported with add-on features |
| -             | Not applicable                 |

## Supported Raster Image Formats {#supported-raster-image-formats}

<!-- TBD: Check this table on stage. The EPS link might cause bad table width. Consider moving EPS link outside the table. -->

| Asset Management Features ||||||||Dynamic Media Features |||||
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|   |Storage |Metadata management |Metadata extraction |Thumbnail generation |Interactive editing |Metadata writeback |Insights |Upload (Input format) |Create image preset (Output format) |Preview dynamic rendition |Deliver dynamic rendition |Download dynamic rendition |
| PNG |x |x |x |x |x |x |x |x |x |x |x |x |
| GIF |x |x |x |x |x |  |x |x |x |x |x |x |
| TIFF |x |x |x |x |  |x |x |x |x |x |x |x |
| JPEG |x |x |x |x |x |x |x |x |x |x |x |x |
| BMP |x |x |x |x |x |  |x | |x  |  |  |  |
| PNM |x |x |  |  |  |  |x |  |  |  |  |  |
| PGM |x |x |  |  |  |  |x |  |  |  |  |  |
| PBM |x |x |  |  |  |  |x |  |  |  |  |  |
| PPM |x |x |  |  |  |  |x |  |  |  |  |  |
| PSD* |x |x |x |x |  |  |x |x |  |  |  |  |
| [EPS](managing-image-presets.md#adobe-illustrator-ai-postscript-eps-and-pdf-file-formats) |x |x |x |x |  |  | |x |x |x |x |x |
| PICT |  |  |  |  |  |  |x |x |  |  |  |  |
| PSB |x  |x  |x  |x  |  |  |  |  |  |  |  |  |

&ast; The merged image is extracted from the PSD file. It is an image that is generated by Adobe Photoshop and is included in the PSD file. Depending on the settings, the merged image may or may not be the actual image.

In addition to the information above, consider the following:

* The support for EPS files applies to raster images only. For example, thumbnail generation for EPS vector images is not supported by default. To add support, [configure ImageMagick](best-practices-for-imagemagick.md). To integrate third-party tools to enable additional capabilities, see [Command line based Media Handler](media-handlers.md#command-line-based-media-handler).

* Metadata writeback works for PSB file format when it is added to the `NComm` handler.

* To use Dynamic Media to preview and generate dynamic renditions for EPS files, see [Adobe Illustrator (AI), Postscript (EPS), and PDF file formats.](../assets/managing-image-presets.md#adobe-illustrator-ai-postscript-eps-and-pdf-file-formats)

* For EPS files, metadata writeback is supported in PostScript Document Structuring Convention (PS-Adobe) version 3.0 or later.

## Supported PDF Rasterizer library {#supported-pdf-rasterizer-library}

The Adobe PDF Rasterizer library generates high-quality thumbnails and previews for large and content-intensive Adobe Illustrator and PDF files. Adobe recommends using the PDF Rasterizer library for the following:

* Content-intensive AI/PDF files that are resource-intesive to process.
* AI/PDF files, for which thumbnails are not generated by default.
* AI files with Pantone Matching System (PMS) colors.

See [Using PDF Rasterizer](aem-pdf-rasterizer.md).

## Image Transcoding Library support {#supported-image-transcoding-library}

The Adobe Imaging Transcoding library is an image processing solution that performs core image-handling functions, such as, encoding, transcoding, resampling, and resizing. Imaging Transcoding library supports JPG/JPEG, PNG (8-bit and 16-bit), GIF, BMP, TIFF/Compressed TIFF (apart from 32-bit TIFF files and PTIFF files), ICO, and ICN MIME types.

See [Imaging Transcoding Library](imaging-transcoding-library.md).

## Supported Camera Raw {#supported-camera-raw}

The Adobe Camera Raw library enables AEM Assets to ingest raw images. See [Camera Raw Support](camera-raw.md).

## Supported Document Formats {#supported-document-formats}

AEM supports the following functionality for the various document formats.

<!-- TBD: table below with merged cells. pls check -->

<table> 
 <tbody>
  <tr>
   <th>Asset Management Features</th> 
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th>Dynamic Media Features</th> 
   <th></th>
   <th></th>
   <th></th>
   <th></th>
  </tr>
  <tr>
   <th> </th> 
   <th>Storage</th> 
   <th>Metadata management</th> 
   <th>Fulltext extraction</th> 
   <th>Metadata extraction</th> 
   <th>Thumbnail generation</th> 
   <th>Sub-asset extraction</th> 
   <th>Metadata writeback</th> 
   <th>Upload (Input format)</th> 
   <th>Create image preset (Output format)</th> 
   <th>Preview dynamic rendition</th> 
   <th>Deliver dynamic rendition</th> 
   <th>Download dynamic rendition</th> 
  </tr>
  <tr>
   <th>Format</th> 
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
   <th></th>
  </tr>
  <tr>
   <td><a href="../assets/managing-image-presets.md#adobe-illustrator-ai-postscript-eps-and-pdf-file-formats"><strong>AI</strong></a></td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>DOC</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>DOCX</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>ODT</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td><a href="/help/assets/managing-image-presets.md#adobe-illustrator-ai-postscript-eps-and-pdf-file-formats"><strong>PDF</strong></a></td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
  </tr>
  <tr>
   <td>HTML</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>RTF</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>TXT</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>XLS</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>XLSX</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>ODS</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PPT</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x<br /> </td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PPTX</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>ODP</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td ><strong><a href="/help/assets/managing-image-presets.md#indesign-indd-file-format">INDD</a></strong></td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PS</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>QXP</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>EPUB</td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
 </tbody>
</table>

In addition to the above functionality, consider the following:

* To use Dynamic Media to generate dynamic renditions for PDF files, see [Adobe Illustrator (AI), Postscript (EPS), and PDF file formats](../assets/managing-image-presets.md#adobe-illustrator-ai-postscript-eps-and-pdf-file-formats).
* To use Dynamic Media to preview and generate dynamic renditions for AI files, see [Adobe Illustrator (AI), Postscript (EPS), and PDF file formats](../assets/managing-image-presets.md#adobe-illustrator-ai-postscript-eps-and-pdf-file-formats).
* To use Dynamic Media to generate dynamic renditions for INDD files, see [InDesign (INDD) file format](../assets/managing-image-presets.md#indesign-indd-file-format).


## Supported Multimedia Formats {#supported-multimedia-formats}


| | Storage |Metadata management |Metadata extraction |Thumbnail generation |FFMPEG transcoding |
|---|---|---|---|---|---|
| AAC |x |x |  |- |* |
| MIDI |x |x |  |- |* |
| 3GP |x |x |  |- |* |
| MP3 |x |x |x |- |* |
| MPG |x |x |  |- |* |
| OGA |x |x |  |- |* |
| OGG |x |x |  |- |* |
| RA |x |x |  |- |* |
| WAV |x |x |  |- |* |
| WMA |x |x |  |- |* |
| DVI |x |x |  |* |* |
| FLV |x |x |  |* |* |
| M4V |x |x |  |* |* |
| MPEG |x |x |  |* |* |
| OGV |x |x |  |* |* |
| MOV |x |x |  |* |* |
| WMV |x |x |  |* |* |
| SWF |x |x |  |  |  |

## Supported input video formats for Dynamic Media Transcoding {#supported-input-video-formats-for-dynamic-media-transcoding}

| **Video file extension** |**Container** |**Recommended video codecs** |**Unsupported video codecs** |
|---|---|---|---|
| .mp4 |MPEG-4 |H264/AVC (all profiles) |  |
| .mov .qt |Apple QuickTime  |H264/AVC, Apple ProRes422 & HQ, Sony XDCAM, Sony DVCAM, HDV, Panasonic DVCPro, Apple DV (DV25), Apple PhotoJPEG, Sorenson, Avid DNxHD, Avid AVR |Apple Intermediate, Apple Animation |
| .flv .f4v |Adobe Flash |H264/AVC, Flix VP6, H263, Sorenson |SWF (vector animation files) |
| .wmv |Windows Media 9 |WMV3 (v9), WMV2 (v8), WMV1 (v7), GoToMeeting (G2M2, G2M3, G2M4) |Microsoft Screen (MSS2), Microsoft Photo Story (WVP2) |
| .mpg .vob .m2v .mp2 |MPEG-2  |MPEG-2 |  |
| .m4v |Apple iTunes |H264/AVC |  |
| .avi |A/V Interleave |XVID, DIVX, HDV, MiniDV (DV25), Techsmith Camtasia, Huffyuv, Fraps, Panasonic DVCPro |Indeo3 (IV30), MJPEG, Microsoft Video 1 (MS-CRAM) |
| .webm |WebM |Google VP8 |  |
| .ogv .ogg |Ogg |Theora, VP3, Dirac |  |
| .mxf |MXF |Sony XDCAM, MPEG-2, MPEG-4, Panasonic DVCPro |  |
| .mts |AVCHD |H264/AVC |  |
| .mkv |Matroska |H264/AVC |  |
| .r3d .rm |Red Raw Video |MJPEG 2000 |  |
| .ram .rm |RealVideo | Unsupported |Real G2 (RV20), Real 8 (RV30), Real 10 (RV40) |
| .flac |Native Flac |Free lossless audio codec |  |
| .mj2 |Motion JPEG2000 |Motion JPEG 2000 codec |  |

## Supported archive formats {#supported-archive-formats}

The supported archive formats and the applicability of the common DAM workflows, is covered in the following table.

| Formats | Storage | Versioning | Workflow | Publishing | Access Control | Dynamic Media delivery |
|---|---|---|---|---|---|---|
| TGZ | x | x | x | x | x | |
| JAR | x | x | x | x | x | |
| RAR | x | x | x | x | x | |
| TAR | x | x | x | x | x | |
| ZIP* | x | x | x | x | x | x |

<!--
<table> 
 <tbody>
  <tr>
   <th> </th> 
   <th>Storage</th> 
   <th>Versioning</th> 
   <th>Workflow</th> 
   <th>Publishing</th> 
   <th>Access Control</th> 
   <th>Dynamic Media Delivery</th> 
  </tr>
  <tr>
   <td>Formats</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>TGZ</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x<br /> </td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
  </tr>
  <tr>
   <td>JAR</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x<br /> </td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
  </tr>
  <tr>
   <td>RAR</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x<br /> </td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
  </tr>
  <tr>
   <td>TAR</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x<br /> </td> 
   <td>x</td> 
   <td>x</td> 
   <td> </td> 
  </tr>
  <tr>
   <td>ZIP*</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x<br /> </td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
  </tr>
 </tbody>
</table>

-->

**\*** The ZIP archives created using the `Deflate64` algorithm have limited support in AEM. Archive and unarchive operations are not supported. Operations, such as, uploading, browsing, and downloading are supported.

## Other supported formats {#other-supported-formats}

The applicability of common DAM workflows for a few other file formats is described in the table below.

<table> 
 <tbody>
  <tr>
   <th>Features</th> 
   <th> </th> 
   <th> </th> 
   <th> </th> 
   <th> </th> 
   <th> </th> 
   <th> </th> 
  </tr>
  <tr>
   <th> </th> 
   <th>Storage</th> 
   <th>Versioning</th> 
   <th>Workflow</th> 
   <th>Publishing</th> 
   <th>Access Control</th> 
   <th>Dynamic Media Delivery</th> 
  </tr>
  <tr>
   <th>Formats</th> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>*</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x<br /> </td> 
   <td>x<br /> </td> 
   <td>x<br /> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>SVG</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x<br /> </td> 
   <td>x</td> 
  </tr>
  <tr>
   <td>CSS</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
  </tr>
  <tr>
   <td>VTT</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
  </tr>
  <tr>
   <td>XML</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
   <td>x</td> 
  </tr>
  <tr>
   <td>JavaScript (when configured with own delivery domain)</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>x</td> 
  </tr>
 </tbody>
</table>

 &ast; The other formats are supported in AEM for storage, versioning, ACL, workflow, publishing, and metadata management.

## Supported MIME types {#supported-mime-types}

By default, AEM detects the file format using the file extension. AEM can detect the file format from the contents of the files. For latter, select [!UICONTROL Detect MIME from content] option in [!UICONTROL Day CQ DAM Mime Type Service] in the [!UICONTROL AEM Web Console].

A list of supported MIME types is available in CRXDE Lite at `/conf/global/settings/cloudconfigs/dmscene7/jcr:content/mimeTypes`.

<!-- TBD: Apply correct formatting for table cells uing backticks after converting the table to MD.
-->

<table> 
 <tbody>
  <tr>
   <td><strong>File extension</strong></td> 
   <td><strong>MIME type/Internet media type</strong></td> 
   <td><strong>Default jobParam value</strong></td> 
   <td><strong>Allowed jobParam value</strong></td> 
  </tr>
  <tr>
   <td>Image</td> 
   <td>image/s7asset</td> 
   <td><code>usmAmount=1.75&amp;usmRadius=0.2&amp;usmThreshold=2&amp;usmMonochrome=0&amp;</code></td> 
   <td><p>The default jobParam applies to all image MIME type assets.</p> 
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_knockout_background_options.html">knockoutBackgroundOptions</a></li> 
     <li>manualCropOptions</li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_auto_color_crop_options.html">autoColorCropOptions</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_auto_transparent_crop_options.html">autoTransparentCropOptions</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_color_management_options.html">colorManagementOptions</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_auto_set_creation_options.html">autoSetCreationOptions</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/string_constants/r_email_settings.html">emailSetting</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_xmp_keywords.html">xmpKeywords</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html">unsharpMaskOptions</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>3G2</td> 
   <td>video/3gpp2</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>3GP</td> 
   <td>video/3gpp</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>AAC</td> 
   <td>audio/x-aac</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>AFM</td> 
   <td>application/x-font-type1</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>AI</td> 
   <td>application/postscript</td> 
   <td><code>aiprocess=Rasterize&amp;airesolution=150&amp;aicolorspace=Auto&amp;aialpha=false</code></td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_post_script_options.html">postScriptOptions</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_illustrator_options.html">illustratorOptions</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>AIFF</td> 
   <td>audio/x-aiff</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>AVI</td> 
   <td>video/x-msvideo</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>BMP</td> 
   <td>image/bmp</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>CSS</td> 
   <td>text/css</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>DOC</td> 
   <td>application/msword</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>EPS</td> 
   <td>application/postscript</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>EPS</td> 
   <td>application/eps</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>EPS</td> 
   <td>application/x-eps</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>EPS</td> 
   <td>image/eps</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>EPS</td> 
   <td>image/x-eps</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>F4V</td> 
   <td>video/x-f4v</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>FLA</td> 
   <td>application/x-shockwave-flash</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>FLV</td> 
   <td>video/x-flv</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>FPX</td> 
   <td>image/vnd.fpx</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>GIF</td> 
   <td>image/gif</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>ICC</td> 
   <td>application/vnd.iccprofile</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>ICM</td> 
   <td><p>application/vnd.iccprofile</p> </td> 
   <td><p> </p> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>INDD</td> 
   <td>application/x-indesign</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>JPEG</td> 
   <td>image/jpeg</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>JPG</td> 
   <td>image/jpeg</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>M2V</td> 
   <td>video/mpeg</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>M4V</td> 
   <td><br /> video/x-m4v</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>MOV</td> 
   <td>video/quicktime</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>MP3</td> 
   <td>audio/mpeg</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>MP4</td> 
   <td>video/mp4</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>MPEG</td> 
   <td>video/mpeg</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>MPG</td> 
   <td>video/mpeg</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>MTS</td> 
   <td>model/vnd.mts</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>OGV</td> 
   <td>video/ogg</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>OTF</td> 
   <td>application/x-font-otf</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PDF</td> 
   <td>application/pdf</td> 
   <td><code>pdfprocess=Rasterize&amp;resolution=150&amp;colorspace=Auto&amp;pdfbrochure=true&amp;keywords=true&amp;links=true</code></td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_pdf_options.html">pdfOptions</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>PFB</td> 
   <td>application/x-font-type1</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PFM</td> 
   <td>application/x-font-type1</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PICT</td> 
   <td>image/x-pict</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PNG</td> 
   <td>image/png</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PPT</td> 
   <td>application/vnd.ms-powerpoint</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>PS</td> 
   <td>application/postscript</td> 
   <td><code>psprocess=Rasterize&amp;psresolution=150&amp;pscolorspace=Auto&amp;psalpha=false&amp;psextractsearchwords=true</code></td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_post_script_options.html">postScriptOptions</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_illustrator_options.html">illustratorOptions</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>PSD</td> 
   <td>image/vnd.adobe.photoshop</td> 
   <td><code>process=MaintainLayers&amp;layerNaming=Layername&amp;anchor=Center&amp;createTemplate=true&amp;extractText=true&amp;extendLayers=false</code></td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_photoshop_options.html">photoshopOptions</a></li> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_photoshop_layer_options.html">photoshopLayerOptions</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>RTF</td> 
   <td>application/rtf</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>SVG</td> 
   <td>image/svg+xml</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>SWF</td> 
   <td>application/x-shockwave-flash</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>TAR</td> 
   <td>application/x-tar</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>TIF</td> 
   <td>image/tiff</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>TIFF</td> 
   <td>image/tiff</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>TTC</td> 
   <td>application/x-font-ttf</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>TTF</td> 
   <td>application/x-font-ttf</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>VOB</td> 
   <td>video/dvd</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>VTT</td> 
   <td>text/vtt</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>WAV</td> 
   <td>audio/x-wav</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>WEBM</td> 
   <td>video/webm</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>WMA</td> 
   <td>audio/x-ms-wma</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>WMV</td> 
   <td>video/x-ms-wmv</td> 
   <td> </td> 
   <td>
    <ul> 
     <li><a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exclude_master_video_from_avs.html">ExcludeMasterVideoFromAVS</a></li> 
    </ul> </td> 
  </tr>
  <tr>
   <td>XLS</td> 
   <td>application/vnd.ms-excel</td> 
   <td> </td> 
   <td> </td> 
  </tr>
  <tr>
   <td>ZIP</td> 
   <td>application/zip</td> 
   <td> </td> 
   <td> </td> 
  </tr>
 </tbody>
</table>

 
>[!MORELIKETHIS]
>
>[Enable MIME type-based Assets/Scene7 upload job parameter support](../sites-administering/scene7.md#enabling-mime-type-based-assets-scene-upload-job-parameter-support).