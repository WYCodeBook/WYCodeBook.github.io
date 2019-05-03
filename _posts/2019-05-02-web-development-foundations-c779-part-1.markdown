---
layout: post
title: "Web Development Foundations C779 - 1.Markup Language and Site Development Essentials"
date: "2019-05-02 19:54:40 -0700"
categories: WGU
---

Markup Language:

A series of commands used to format, organize and describe information on a Webpage.

Responsive Design:

- An approach to Web development that uses a series of techniques to make Webpages dynamic and accessible on all device screen sizes.
- Responsive design includes practices like defining sizes in percentages rather than absolute pixels, and checking device specifications to deliver one of multiple style sheets that best fit the user's needs.

Hypertext Markup Language (HTML):

- The traditional authoring language used to develop Webpages for many applications.
- HTML is standardized by an organization called the World Wide Web Consortium (W3C).
- HTML is the markup language that defines page structure, hyperlinks, graphics and more to enable pages to render in Web browsers and other devices.

Cascading Style Sheets (CSS):

- A technology that allows greater style definition and formatting control of HTML elements. Formatting can be placed within the HTML or called remotely from an external style sheet.
- Cascading style sheets is currently in its third version (CSS3)

Cloud Computing:

- Software, infrastructure and platform services that are hosted by a remote data center and provided to organizations or individuals over the Internet.
- These servers can now be located in the "cloud" (i.e., a remote data center that is accessed over the Internet).

Text Editor and Markup Language:

- You do not need to use a special editor application to create HTML. You can use a simple text editor.
- You should save it with the .htm or .html file name extension. Many operating systems and Web browsers are configured with Multipurpose Internet Mail Extensions (MIME) to automatically process files with these extensions.
- Multipurpose Internet Mail Extensions (MIME): A protocol that enables operating systems to map file name extensions to corresponding applications. Also used by applications to automatically process files downloaded from the Internet.

Graphical User Interface (GUI):

- A program that provides visual navigation with menus and screen icons, and performs automated functions when users click command buttons.
- Graphical user interface (GUI) markup editor applications place markup instructions into files for you; you do not need to know HTML to use GUI editors.
- Many GUI HTML editors still do not produce valid HTML.
- Commands are displayed on the graphical user interface as they will appear in a browser, thus the programs are often called WYSIWYG (What You See Is What You Get) editors.
- Some developers feel that using a GUI editor application saves time. Others feel that GUI editors create confused HTML code and do not provide true flexibility.
- Popular GUI HTML editors include Adobe Dreamweaver, Microsoft Expression Web, Mozilla SeaMonkey and Google Web Designer.

History of Markup Languages:

Standard Generalized Markup Language (SGML): A metalanguage used to create other languages, including HTML and XHTML.

- originally created by IBM and was standardized in 1986 by the International Organization for Standardization (ISO)
- a powerful markup language that describes documents by organizing concepts separately from their visual presentation.
- purpose was to describe only the information within a document, not the formatting of it.
- SGML essentially requires that you create, or define, your own document language rules. This set of language rules is called the Document Type Definition (DTD).
- Document Type Definition (DTD): A set of rules contained in a simple text file that defines the structure, syntax and vocabulary as it relates to tags and attributes for a corresponding document.

Hypertext Markup Language (HTML):

- Tim Berners-Lee of MIT invented Hypertext Markup Language (HTML) with colleagues from CERN (the European Particle Physics Laboratory) as a means of distributing non-linear text, called hypertext, to multiple points across the Internet.
- In HTML, one document links to another via pointers called hyperlinks.
- Hyperlinks are embedded instructions within a text file that call another location in the file or a separate file when the link is accessed, usually by a click of a mouse.
- HTML does not allow you to define a DTD and has fewer language elements than SGML.
- The latest version of HTML, called HTML5, is not based on SGML and DTD is no longer required.

HTML 3.2 vs. HTML 4.01

- HTML 3.2 is an older but functional HTML standard.
- The HTML 4.01 (released in 1999) contained many improvements from HTML 3.2, most notably Cascading Style Sheets (CSS).
- HTML 4.01 supported multiple spoken languages.
- HTML 4.01 also allowed you to create ambitious tables and forms, as well as incorporate scripting languages.

Note: The W3C regulates the development of CSS3 standards.

HTML 4.01 Distinct Variants / Flavors

1. HTML 4.01 Transitional — allowed developers to insert formatting using either CSS or traditional layout instructions (e.g., HTML font, color and phrase elements).
2. HTML 4.01 Strict — required the exclusive use of CSS when defining layout instructions. Deprecated tags were not allowed and generated errors.
3. HTML 4.01 Frameset — required for pages that used HTML frames, which placed Webpages inside each other to create separate panes in the browser window.

Note: You specify the flavor of HTML by using a document type (<!DOCTYPE>) declaration.

Extensible Markup Language (XML):

- A markup language that describes document content instead of adding structure or formatting to document content. A simplified version of SGML.
- Businesses use XML because it allows data to be interchanged with all types of applications.
- XML is often used with intranets and extranets because these systems tend to focus mostly on sophisticated personal and business transactions.
- XML documents can be formatted into print documents, Web documents, PDF documents, comma-separated values (CSV), Braille, text-to-speech and many other formats.
- XML is not used to format Webpages, but to describe the data from which Webpages are created.

Note: The W3C governs the development of XML.

Extensible Hypertext Markup Language (XHTML):

- a medium that would merge the HTML and XML into a markup language called Extensible Hypertext Markup Language (XHTML).
- XHTML could not completely depart from HTML, nor could it be patterned completely after XML. XHTML documents are not required to render correctly in standard clients, but will have little if any difficulty.
- XHTML extends HTML by allowing the convergence of HTML documents with XML structure, creating forward-compatibility for documents.

Note: When you use XML, the term Uniform Resource Identifier (URI) is preferred over the standard HTML term Uniform Resource Locator (URL).

HTML5:

- HTML5 is the latest version of HTML under development by the W3C.
- Introduces the '<video>' element, which is designed to eliminate the need to install third-party plug-ins (such as those for Adobe Flash or Microsoft Silverlight).
- Adds the '<audio>' element, which allows pages to seamlessly add audio files for events such as podcasts.
- Establishes ways to enable drag-and-drop capability for Webpages without using third-party add-ons.
- Gives developers more native tools such as download progress indicators, image captioning options and form validation tools to use on a page.
- Provides developers with a native option for offline storage, and enables applications to run as expected even without network connectivity.
- Allows developers to retrieve the geographical location information for a client-side device, called geolocation. Examples include using the Global Positioning System (GPS) of a mobile device to determine the device's location, which allows Web services to be provided based on the client's location.

Markup code validation: It is possible to validate all markup code automatically. Many validators exist, but the most authoritative is the W3C Markup Validation Service (https://validator.w3.org/).

Creating universal markup code is important for several reasons:

- Your pages will be ensured to render in future versions of most browsers.
- Your pages will be more scalable. This means that as you add more sophisticated content, make pages searchable or use the content in ways you have not yet imagined, you can still use markup you created without having to revise the code extensively.
- Your pages will be more accessible to disabled users. You will be able to more easily make your pages compliant so that your site is available to the widest possible audience and does not present a liability to your organization.

Note: Consistent use of an HTML standard — such as HTML5, for example — can improve your page's ability to rank higher in a search engine results page.

Note - HTML5 family or Web Development Trifecta:

- HTML5: Markup language used for structuring and presenting Webpage content
- Cascading Style Sheets (CSS3):	Style sheet language that provides the formatting and "look" of a Webpage or document written in a markup language
- JavaScript: Scripting language that provides dynamic, interactive capabilities to Webpages

Project management and the Web development project cycle:

- Create and document an initial Website plan.
- Obtain relevant input from stakeholders.
- Communicate the Website plan.
- Consider technical and non-technical concerns.
- Develop the site.
- Publish the site.
- Manage the site.

Note: Part of the management cycle is optimizing pages so that they rank highly in search engine results pages.

The Americans with Disabilities Act (ADA) was enacted in 1990 to protect the civil rights of disabled people.

- Ensuring that all images have text-based descriptions so that sight-impaired visitors can access sites through screen-reader technology.
- Providing text-based alternatives to all non-text content (e.g., Java applets).
- Providing forms that are easily read by screen-reading technology.

Note: Video is not ADA-compliant because sight-impaired visitors cannot see it. Video with audio but no alternative text support is a problem because hearing-impaired visitors cannot hear it.

Web Content Accessibility Guidelines (WCAG): The Web Content Accessibility Guidelines (WCAG) are part of a series of web accessibility guidelines published by the Web Accessibility Initiative (WAI) of the World Wide Web Consortium (W3C), the main international standards organization for the Internet.

- The WAI has developed the Web Content Accessibility Guidelines (WCAG) to provide a universal set of standards promoting accessibility.
- According to the WAI, the Web's full potential can only be realized by "promoting a high degree of usability for people with disabilities."
- The WAI works with worldwide organizations in five main areas: technology, guidelines, tools, education and outreach, and research and development.

Note: The European Union and Australia have mostly adopted the WCAG standards.

WAI concerns and standards:

- User agent accessibility — A user agent is any device used to view a Webpage. The most common user agent is a Web browser. Additional user agents include mobile device applications, such as smartphones and tablets. The W3C User Agent Accessibility Guidelines document is available at www.w3.org/TR/UAAG20.
- WCAG checklist — A checklist for the accessibility guidelines detailed in the WCAG is available at https://www.w3.org/TR/2006/WD-WCAG20-20060427/appendixB.html.
- Accessibility for developers — The W3C also addresses ways to ensure that development tools can be used by disabled people. For more information, read the W3C Authoring Tool Accessibility Guidelines at https://www.w3.org/TR/ATAG20/.

Section 508 of the Rehabilitation Act:

- On June 21, 2001, the U.S. government implemented Section 508 of the Rehabilitation Act: Electronic and Information Technology Accessibility Standards.
- Section 508 requires that Federal agencies provide accommodations users with disabilities for all electronic and information technology developed, procured, maintained or used by federal agencies.
- Section 508 is based on the Priority 1 and 2 checkpoints of the W3C's WAI Web Content Accessibility Guidelines 1.0.
- The chief purpose of Section 508 is to ensure that disabled individuals have a comparable level of access to information.

Section 508 includes the following standards for Websites:

- All non-text elements must have a text-based equivalent.
- If using multimedia, all equivalent information must be properly synchronized with the multimedia so that disabled persons are not at a disadvantage.
- Information must be equally available in color and without color.
Documents must be made available without requiring an associated style sheet.
- Text descriptions must be made available for all image maps.
- Client-side image maps should not be used because they cannot be properly presented to visually impaired users.
- If using tables for data, you must identify all row and column headers.
- If a table has two or more rows or columns, you must use row and column headers.
- Sites that use frames must have titles that easily enable alternative browsers to navigate through each frame.
- If necessary, a separate text-only site should be made available to ensure access.
- When scripting technology is used to enable a site feature (e.g., a form), a plaintext alternative must be available that allows an assistant application to read the feature.

Note: Partial color blindness is much more widespread than commonly realized. If your target audience is the entire world, read about color blindness to determine which color combinations are most easily read by the largest number of people. For information, color deficiency simulations and links to color-blindness tests, visit www.visibone.com/colorblind.

General Webpage accessibility considerations

Addressing visual challenges

- Text readability — Make sure that fonts used are the correct size.
- Text support for images — All images must be described in text using special HTML code.
- Screen-reader support — Ensure that all pages and page elements can be rendered by audio screen readers.

Addressing audio challenges

- Alternative audio support — If you include audio content on a page, make sure that a text-based equivalent is readily available for hearing-impaired users.
- Alternative speech input — If your site includes the ability for speech input, make sure that an equivalent keyboard entry mechanism is available.
- Text support for audio elements — Make sure that any audio elements are clearly marked with alternative text so that readers can obtain the information.

Addressing cognitive and technical challenges

- Page content that flashes, flickers or strobes — Such content may cause problems for those with neurological disorders.
- Alternative navigation — Navigation aids should be provided to help those with lower cognitive skills.
- Audio support — Audio transcriptions of text-based content may help users with reading disabilities such as dyslexia.
- Low-resolution alternatives — Design Webpages so that they do not require large, expensive screen resolutions, or provide low-resolution alternatives.

Creating and documenting an initial Website plan

- A statement discussing the purpose and intended audience for the site. This statement may evolve over time, but it is important to begin with this statement to remind everyone involved why the site is being developed and to steer all efforts in the proper direction.
- A rough outline of the pages needed, including:
  1.  The default page (e.g., index.html), also called the home page.
  2.  Sections of the site (e.g., products, sales, international, contacts).
  3.  An estimate of the technologies required (e.g., databases, Web servers, search capability, indexes).

Wireframing: The process of developing an outline for a Web presence. Wireframes usually focus on representing a Website's layout. Multiple wireframes can make up a storyboard.

- Determining the purpose and objective of the Website. Is this an e-commerce Website? An informational Website? A company intranet?
- Identifying all stakeholders for the site.
- Outlining the basic steps of the development process.
- Identifying steps for managing the project.
- Outlining site navigation.
- Identifying the technologies that are invoked with each user request.

Wireframing software can include:

- Gliffy (www.gliffy.com)
- Mockingbird (https://gomockingbird.com/home)
- HotGloo (www.hotgloo.com)

Determining the audience and message

- Customer representatives — Organizations often have important customers attend meetings and provide input. Customer representatives can teach you about the various types of messages that appeal most to potential customers. For example, some may want to focus on the value of a particular product, regardless of cost. In other instances, customers may help you focus on a message that shows your products to be inexpensive. Once you have surveyed customers to determine what the market wants, you can begin to craft Webpages that clearly convey your company's message to its intended customers.

- Suppliers — If you are planning for large sales as a result of your Web effort, make sure that your product suppliers are ready for this. Otherwise, you could damage the company's reputation by making promises that cannot be kept. Even though a Web authoring team works mostly on creating markup pages, your Website's ability to communicate with the public means that such business concerns are essential for the overall success of the project.

- Shareholders— If your organization is publicly owned, you may need to obtain input from shareholders about the look and feel of the site.

Validating design issues

- Message — Deliver a coherent message for each page. Information that is not relevant or otherwise distracts readers from a well-conceived central idea should be placed on another page or eliminated.
- Fonts — If specifying fonts, make sure that you use common ones so that browsers do not have difficulty rendering them. Use proper sizes; small fonts are difficult to read.
- Images — Make sure that all images used on a page contribute to either the page's navigability or its message.
- Color — Take time to consider color combinations so that your pages are as attractive and readable as possible.
