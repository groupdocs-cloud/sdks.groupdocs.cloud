---
############################# Static ############################
layout: "product"
date: 2021-04-27T09:31:06+03:00
draft: false

product: "Annotation"
product_tag: "annotation"
platform: "Node.js"
platform_tag: "node"

############################# Head ############################
head_title: "Node.js Document & Image Annotation Cloud SDK for PDF Word Excel HTML"
head_description: "Node.js Cloud SDK for managing images and document annotations. Use REST APIs to easily manipulate PDF, image, HTML, Word, Excel, & email annotation."

############################# Header ############################
title: "Let's Annotate in Node.js with RESTful API"
description: "REST API & Cloud SDK for Node.js to build online document & image annotation tools with support for text & image annotation options. Let's annotate!"
button:
    enable: true

############################# SubMenu ############################
submenu:
    enable: true
    
    left:
        img_alt: "GroupDocs.Annotation Cloud SDK for Node.js"
        image: "/sdk/272x272/groupdocs_annotation-for-node.webp"
        product: "GroupDocs.Annotation"
        platform: "Node.js"

    middle:
        button:
            # button loop
            - link: "#overview"
              text: "Overview"

            # button loop
            - link: "#features"
              text: "Features"


            # button loop
            - link: "https://docs.groupdocs.cloud/annotation/release-notes/"
              text: "Release Notes"

            # button loop
            - link: "https://purchase.groupdocs.cloud/pricing"
              text: "Pricing"

    right:
        link_download: "https://github.com/groupdocs-annotation-cloud/groupdocs-annotation-cloud-node"
        link_learn: "https://docs.groupdocs.cloud/annotation/"
        link_buy: "https://purchase.groupdocs.cloud/buy"

############################# Overview ############################
overview:
    enable: true
    content: |
      GroupDocs.Annotation Cloud REST API for .NET allows you to programmatically work with business document annotation operations and develop tools using C# and other .NET technologies. The tools that you develop using our annotation SDK for .NET APIs, enable your end-users to annotate files of supported file formats, such as PDF, Microsoft Word, Excel, PowerPoint, Images and various other formats. Apply redactions, watermark overlays, sticky notes, pointers and text markups etc. The open-source SDK works as a wrapper for cross-platform .NET REST APIs. Apply annotations as drawings or text markups.
    tabs:
      enable: true
      
      ## TAB ONE ##
      tab_one:
        description: |
          Node.js module is required for communicating with the GroupDocs.Annotation Cloud SDK API for Node.js.‎
      
        left:
          enable: false
          icon: "fas fa-crop"
          title: "Figure Annotations"
          content: |
            
        right:
          enable: true
          icon: "fas fa-cubes"
          title: "Node.js 4.8.7 or higher"
          content: |
            
      
      ## TAB TWO ##
      tab_two:
        description: |
          GroupDocs.Annotation Cloud SDK APIs support following file formats:‎

        left:
          enable: true
          table:
            # table loop
            - title: "Microsoft Office Formats"
              content: |
                * **Word**: DOC, DOCX, DOCM, DOT, DOTX, RTF
                * **Excel**:  XLS, XLSX, XLSM, XLSB, CSV
                * **PowerPoint**: PPT, PPTX, PPS, PPSX
                * **Visio**: VSD, VSDX, VSS, VST

        right:
          enable: true
          table:
            # table loop
            - title: "Other Formats"
              content: |
                * **OpenDocument**: ODT, OTT, ODS, ODP
                * **Image Files**: BMP, PNG, JPG, JPEG, TIFF, TIF, GIF
                * **Fixed Layout**: PDF
                * **Web**: HTM, HTML
                * **Email**: EML
                * **CAD**: DWG, DXF


      ## TAB THREE ##
      tab_three:
        description: |
          GroupDocs.Annotation set of SDK REST APIs is not dependent on your local operating system or ‎database. We offer our SDK APIs in numerous programming languages and with frequent new ‎additions.‎
      
        left:
          enable: true
          table:
            # table loop
            - icon: "fab fa-windows"
              title: "Operating Systems"
              content: |
                * Microsoft Windows Desktop
                * Microsoft Windows Server
                * Linux
                * MacOS

            # table loop
            - icon: "fas fa-code"
              title: "Supported Frameworks"
              content: |
                * Java 7 (1.7) and above

        right:
          enable: true
          table:
            # table loop
            - icon: "fas fa-cogs"
              title: "Development Environments"
              content: |
                * NetBeans
                * IntelliJ IDEA
                * Eclipse
            # table loop
            - icon: "fas fa-tools"
              title: "Build Automation Tool"
              content: |
                * Maven

############################# Features ############################
features:
    enable: true
    title: "Advanced Document Annotation REST API Features"

    feature:
      # feature loop
      - icon: "fas fa-copy"
        content: "Support for Multiple File Formats"

      # feature loop
      - icon: "fas fa-desktop"
        content: "Import Annotation Information from Document & Return the List of Imported Annotations"

      # feature loop
      - icon: "fas fa-comment"
        content: "Export/Add Annotation to a Document & Retrieve the Resultant Document as Stream"
      
      # feature loop
      - icon: "fas fa-puzzle-piece"
        content: "Render Document Pages to Images and Retrieve Images’ Links"

      # feature loop
      - icon: "fas fa-retweet"
        content: "Retrieve Link to Previously Generated Image by Page Number of Annotated Document"

      # feature loop
      - icon: "fas fa-archive"
        content: "Render Document to PDF, Save Resultant Document to Storage & Fetch its Link"

      # feature loop
      - icon: "fas fa-file-pdf"
        content: "Render Document to PDF as an Output Stream"

      # feature loop
      - icon: "fas fa-eye-slash"
        content: "Add Text Redaction Annotation in Slides‎"

      # feature loop
      - icon: "fas fa-file-word"
        content: "Add Annotations to Header/Footer of Microsoft Word Documents"
    
    more_feature:
      # more_feature_loop
      - title: "Easy Integration"
        content: "Integrating GroupDocs.Annotation Cloud SDK into your Node.js applications is very easy. No installation is ‎required on the server or client side. Just create an account at GroupDocs.Cloud to get App SID & ‎key. Following example shows how easy it is to import annotation information using Node.js:‎"

      # more_feature_loop
      - title: "Get Supported Document Formats - Node.js"
        content: |
          
          ```js
            // load the module
            var GroupDocs = require('groupdocs-annotation-cloud');
            
            // get your appSid and appKey at https://dashboard.groupdocs.cloud (free registration is required).
            var appSid = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX";
            var appKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
            
            // construct AnnotationApi
            var infoApi = GroupDocs.InfoApi.fromKeys(appSid, appKey);
            
            // retrieve supported file-formats
            infoApi.getSupportedFileFormats()
                .then(function (response) {
                    console.log("Supported file-formats:")
                    response.formats.forEach(function (format) {
                        console.log(format.fileFormat + " (" + format.extension + ")");
                    });
                })
                .catch(function (error) {
                    console.log("Error: " + error.message)
                });
          ```
      # more_feature_loop
      - title: "Support for Numerous Annotation Types"
        content: "Using GroupDocs.Annotation Cloud SDK for Node.js, you can work with diverse types of annotations. The ‎two basic types are; Text Annotations and Figure Annotations.‎

        While using text-based annotation, you can add text comments to selected text; highlight which text ‎should be replaced with what, hide confidential text using text redaction, highlight text with ‎strikethroughs/underlines, and add sticky notes with rich text.‎

        While working with figure annotations, you can add notes to an area highlighted with a rectangle (Area ‎Annotation), add notes to any point in the document (Point Annotation), hide confidential parts of an ‎image or text (Area Redaction), draw freehand lines and shapes (Polyline), arrows pointing to an ‎object (Pointer/Arrow), create text-based watermark overlays (Watermark), and measure the ‎distance between any objects in a document (Distance Annotation).‎"

      # more_feature_loop
      - title: "Easy Integration"
        content: "Integration of GroupDocs.Annotation Cloud SDK in to your C# or other .NET based applications is pretty easy and straight-forward. Simply create an account at GroupDocs.Cloud and get the App SID & App Key and you are good to go."

      # more_feature_loop
      - title: "Easy Customization"
        content: "GroupDocs.Annotation Cloud SDK for Node.js is 100% tested and out of the box running. The SDK is open ‎source and has an MIT license. You can use it, and even customize it for absolutely free of charge.‎"
      # more_feature_loop
      - title: "Interactive API Explorer"
        content: "Using our Swagger based API explorer; you can try out GroupDocs.Annotation Cloud SDK for Node.js ‎right away in your browser. This interactive API explorer gives you information about all the resources ‎that the API offers. You can also try your desired operation by interactively providing required ‎parameters.‎"
      

############################# Support ############################
support:
    enable: true

############################# Solutions ############################
solutions:
    enable: true
    title: "GroupDocs.Annotation Cloud Product Family also includes SDKs for other popular languages as listed below:"

    solution:
        # solution loop
        - img_alt: "GroupDocs.Annotation Cloud SDK for cURL"
          image: "/sdk/272x272/groupdocs_annotation-for-curl.webp"
          product: "GroupDocs.Annotation"
          platform: "cURL"
          link: "/annotation/curl/"

        # solution loop
        - img_alt: "GroupDocs.Annotation Cloud SDK for .NET"
          image: "/sdk/272x272/groupdocs_annotation-for-net.webp"
          product: "GroupDocs.Annotation"
          platform: ".NET"
          link: "/annotation/net/"

        # solution loop
        - img_alt: "GroupDocs.Annotation Cloud SDK for Java"
          image: "/sdk/272x272/groupdocs_annotation-for-java.webp"
          product: "GroupDocs.Annotation"
          platform: "Java"
          link: "/annotation/java/"

        # solution loop
        - img_alt: "GroupDocs.Annotation Cloud SDK for PHP"
          image: "/sdk/272x272/groupdocs_annotation-for-php.webp"
          product: "GroupDocs.Annotation"
          platform: "PHP"
          link: "/annotation/php/"

        # solution loop
        - img_alt: "GroupDocs.Annotation Cloud SDK for Python"
          image: "/sdk/272x272/groupdocs_annotation-for-python.webp"
          product: "GroupDocs.Annotation"
          platform: "Python"
          link: "/annotation/python/"

        # solution loop
        - img_alt: "GroupDocs.Annotation Cloud SDK for Ruby"
          image: "/sdk/272x272/groupdocs_annotation-for-ruby.webp"
          product: "GroupDocs.Annotation"
          platform: "Ruby"
          link: "/annotation/ruby/"

        # solution loop
        - img_alt: "GroupDocs.Annotation Cloud SDK for Node.js"
          image: "/sdk/272x272/groupdocs_annotation-for-node.webp"
          product: "GroupDocs.Annotation"
          platform: "Node.js"
          link: "/annotation/nodejs/"

        # solution loop
        - img_alt: "GroupDocs.Annotation Cloud SDK for Android"
          image: "/sdk/272x272/groupdocs_annotation-for-android.webp"
          product: "GroupDocs.Annotation"
          platform: "Android"
          link: "/annotation/android/"

############################# Back to top ###############################
back_to_top:
  enable: true
---