## Links

Links in technical documentation direct users to other titles in the same document, to other adjacent documents, or to external sites. This section describes the recommended specifications for using links in technical documents written in Markdown.

Examples of link formats in Markdown:

- Links to other titles in the same document: `[Product Architecture] (#product-architecture)`
- Links to other adjacent documents: `[Product Architecture] (.. /docs/architecture.md)`
- Links to external sites: `[Contributor Guide] (https://docs.microsoft.com/zh-cn/contribute/)`

### Description of Links

The content in brackets `[]` in a Markdown link is the descriptive text for the link. The description of the link must comply with the following specifications.

- The link description must summarize the general content of the linked document or page, which is good for Search Engine Optimisation. For example, the link description could be the title of the linked page.

    - Incorrect Examples:

        - For details, see `[trouble-shooting.md] (trouble-shooting.md)`
        - For details, please click `[here] (trouble-shooting.md)`

    - Correct Examples:

        - For more details on the above configuration items, see the relevant `configuration items in [Feature Configuration Set] (#feature-config-set)`.
        - See the `Troubleshooting Documentation (trouble-shooting.md)` for more information.

- Link descriptions of the same type should be as of the same style as possible. For example, it is not advisable to appear multiple times in the same document with different descriptions of “see for details”, “for details”, “for more information”, and “see for more information” that express the same meaning.

### Path of the link

The content in parentheses `()` in a Markdown link is the path of the link. The path of the link must comply with the following specifications.

- **If you link to another adjacent document, and the linked document is long, it is recommended to link to an anchor point**. Linking to an anchor means to link to a certain title in the document. Markdown supports adding “#title-names” to the filename in the link path to link to a specific title of the file.

    - Example: `[Configuration File] (trouble-shooting.md#config-file)` links to the `trouble-shooting.md` file under the “Configuration File” heading.

- The paths of links should be styled as consistently as possible. For example, you should use relative or absolute paths consistently when linking to non-external sites; mixing relative and absolute paths is not recommended.

- It is recommended to reduce the number of times users are redirected to external sites because pages on the external site might become stale and affect the user experience.

    > Meaning of external site: A website's documentation contains a link to website B. If website B does not have the same domain name or server as website A, then the link to website B is an external site for the documentation of website A. For example, cloud.google.com is an internal site relative to support.google.com, while cloud.google.com is an external site relative to kubernetes.io.

- **If you must link users to an external site, it is recommended that you add a clear label after the link to remind the user that the link will go to an external site. **

    > Due to the different terms of use and privacy policies of different websites, users who use the current site generally default to accepting the legal provisions of the current site. Before leaving the current site, the website maintainer is responsible for reminding the user that the current link is to an external site. If the user has a problem after jumping out, it is not the responsibility of the current site.

    - Example 1: If the front-end capabilities are sufficient, you can add a generic link icon effect after the link, such as a [list of contributors](https://github.com/yikeke/zh-style-guide/graphs/contributors).

    - Example 2: In Markdown, you can simply add information such as `“Click to go to an external site”` or `“Click to go to XXX site”` after the link path, such as `[link description] (the path of the link is “hint to external link”)`, you can achieve the effect of a hint when the mouse hovers over the hyperlink under normal rendering.
