---
layout: default
title: Rich Snippets Installation
description: magento snippet module installation
keywords: >
    magento quick view extension, magento rich snippet extension, magento
    google rich snippets extension, google rich snippets magento extension, google
    rich snippets tool
category: Rich Snippets
---

### Fresh Magento Installation

1.  Copy RichSnippets folder content to your store root;
2.  Go to `System>Configuration>Templates Master>RichSnippets` set `"Enabled"`;
3.  Fill needed data;
4.  Select format type
    -   Choose **"JSON Format"** for invisible block with your store snippets;
    -   Choose **"Microdata Format"** for visible block:

        ![Microdata Format](http://i.imgur.com/IjEbpz3.png)

        * If you use `TM_EasyTabs` extension it will appear in the bottom of **"Review"** Tab;
        * If you use default product page layout it will appear in the bottom of **"Additional Information"** block;

### Installation in Argento 1.6.2 version or lower or upgrading from previous Rich Snippets versions

1.  Go to your theme `view.phtml` file (i.e. *app/design/frontend/argento/default/template/catalog/product/view.phtml* )
2.  **REMOVE** following lines:

    ```html
    <div itemscope itemtype="http://schema.org/Product">
    ```

    ```php
    <!-- Rich snippets block -->
        <?php echo $this->getLayout()
             ->createBlock('richsnippets/product')
             ->setTemplate('tm/richsnippets/richsnippets_view.phtml')
             ->toHtml() ?>
    <!-- Rich snippets block -->
    </div>
    ```
3.  Find following code snippets and **REMOVE**:
    - `itemprop="name"`
    - `itemprop="description"`

4.  Or **RESTORE** your original theme **view.phtml** if no other changes were made;
5.  Copy **Rich Snippets 2.0** folder content to your store root;
6.  Go to `System>Configuration>TemplatesMaster>RichSnippets` set `"Enabled"`;
7.  Fill needed data;
8.  Select format type

    -   Choose "JSON Format" for invisible block with your store snippets
    -   Choose "Microdata Format" for visible block:

        ![Microdata Format](http://i.imgur.com/IjEbpz3.png)

        * If you use TM_EasyTabs extension it will appear in the bottom of "Review"
          Tab;
        * If you use default product page layout it will appear in the bottom of
          "Additional Information" block;

### Testing your site with Google Rich Snippets testing tool

1.  Open [Google Rich Snippets testing tool](https://developers.google.com/structured-data/testing-tool/);
2.  Insert your page source code or URL in proper fields and click **Check**;
3.  If everything is OK you will get similar results:

    ![All good Results](http://image.prntscr.com/image/49b886988de548cdb8ce4f164400e0e1.png)

4.  Wait when Snippets will appear in Google search results

#### After you install an extension you can go to:

* [Support](https://swissuplabs.com/contacts/)
* [Forum](https://swissuplabs.com/magento-forum/)