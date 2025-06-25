# General Best Practices in Digital Accessibility 

## Don't depend on formatting for conveying meaning

Here are some general rules:
- Do not use color, shape, or symbol _alone_ to denote meaning
- [Contrast](https://webaim.org/resources/contrastchecker) between foreground (e.g., text) and background colors must be sufficient:
    - Unless text is decorative, insignificant within the context, or is part of a logo or brand name
    - Between **non-bold text** and background, at least 4.5:1 if font size is smaller than 18 points, and 3:1 if larger
    - Between **bold text** and background, at least 4.5:1 if font size is smaller than 14 points, and 3:1 if larger
    - Between a non-text visual and its adjacent color(s), at least 3:1
- In terms of typography and text
    - Choose typefaces or fonts that are simple and easy to read. Use a limited number of typefaces, fonts, and font variations
    - Where possible, prefer font sizes 14 pt or bigger, but no smaller than 12 pt
    - Avoid justified text
    - User can apply the following customizations without loss of content or functionality:
        - Increase text size to up to 200%
        - Set line spacing to up to 1.5 times the font size
        - Set spacing following paragraphs to at least 2 times the font size (**Note**: where possible, “chunk” and separate blocks of contents with white space as a best practice)
        - Set letter spacing (tracking) to at least 0.12 times the font size
        - Set word spacing to at least 0.16 times the font size
- Avoid animations and transitions that are not essential to content or functionality.
- **Do not use a visual that flashes more than 3 times in a second**

**Relevant WCAG 2.1 Success Criteria**: [1.3.3](https://www.w3.org/TR/WCAG21/#sensory-characteristics), [1.4.1](https://www.w3.org/TR/WCAG21/#use-of-color), [1.4.3](https://www.w3.org/TR/WCAG21/#use-of-color), [1.4.4](https://www.w3.org/TR/WCAG21/#resize-text), [1.4.8](https://www.w3.org/TR/WCAG21/#visual-presentation), [1.4.10](https://www.w3.org/TR/WCAG21/#reflow), [1.4.11](https://www.w3.org/TR/WCAG21/#non-text-contrast), [1.4.12](https://www.w3.org/TR/WCAG21/#text-spacing), [2.3.1](https://www.w3.org/TR/WCAG21/#three-flashes-or-below-threshold)

### Why is this helpful?

The visual capabilities of sighted users may vary greatly, including in acuity, clarity, field of view, presence of obstructions, and ability to tell between colors. In addition, some users suffer from seizure disorders that are triggered by visual stimuli. The styling choices that we make can make a difference in if and how well our content is visually perceivable.

---
## Use headings to structure document content 

In rich content editors, such as the ones used by Canvas, H5P, or even Word, you can generally use headings to denote its structure.

Headings should describe topic or purpose. They should also be hierarchical; the following is an example of how you would use them in a book:

- Part I (Heading Level 1)
    - Chapter 1 (Heading Level 2)
        - Section (Heading Level 3)
            - Subsection (Heading Level 4)
        - Section (Heading Level 3)
    - Chapter 2 (Heading Level 2)

**Relevant WCAG 2.1 Success Criteria**: [1.3.1](https://www.w3.org/TR/WCAG21/#info-and-relationships), [2.4.6](https://www.w3.org/TR/WCAG21/#headings-and-labels), [2.4.10](https://www.w3.org/TR/WCAG21/#section-headings)

### Why is this helpful?

Rich content editors typically style heading levels differently (e.g., heading level 1 is bigger and bolder than heading level 2, and so on), which helps visually break up a document for sighted users. Similarly, screen readers announce heading hierarchy for its users. Further, headings in a document can be used for other purposes, such as generating table of contents and providing a way to “jump” to a specific place in the document.

### Further enhancements

Embedded webpages become a part of the flow of the page that they are embedded on. Where possible, the top heading level in an embedded webpage should be set appropriately as to not breaking the heading flow of its parent page.

For example, if a webpage is embedded in a section of a page with Heading Level 3, the top heading level in the webpage should not exceed Heading Level 3.

This is not always possible; however, the embedded webpage itself should still have a logical heading structure.

---
## Use built-in lists 

An easy way to tell if you’re using a built-in list is by using your mouse to highlight it – you are using a built-in list if the bullets themselves can’t be selected / highlighted.

**Relevant WCAG 2.1 Success Criteria**: [1.3.1](https://www.w3.org/TR/WCAG21/#info-and-relationships)

### ## Why is this helpful?

Items in a built-in list are semantically linked together, and screen readers can identify and navigate the list items as such (i.e., “List with 3 items”).

---
## Write descriptive links 

In general, your links should be descriptive enough that they are meaningful if by themselves without the original context.

Here are some examples with underlined text indicating links:

- **Do**: <u>Here is an article on the multimedia learning theory</u>
- **Avoid**: We have an article on the multimedia learning theory. <u>Click here</u>
- **Avoid**: Here is an article on the multimedia learning theory (www.abcdf.edu/learning/2015/12345.html)

In addition, links that refer to the same destination/page or functionality should be identified consistently; for example, “Course Syllabus” for all links that lead to the Syllabus page in a CarmenCanvas course.

**Relevant WCAG 2.1 Success Criteria**: [1.3.1](https://www.w3.org/TR/WCAG21/#info-and-relationships), [3.2.4](https://www.w3.org/TR/WCAG21/#consistent-identification)

### Why is this helpful?

Links are indicated and read by screen readers; terseness and contextual cues help making them easier to identify and less of an annoyance (e.g., “Here is an, link, article on the multimedia learning theory”)

---
## Use built-in tables 

Tables are a good way to present data that might be too complicated to be adequately described in text. 

When used for data, tables should have a programmatic caption, designated header cells, and scopes defined on the header cells. 

When used for layout, tables should NOT have any programmatic semantics. 

**Relevant WCAG 2.1 Success Criteria**: [1.3.1](https://www.w3.org/TR/WCAG21/#info-and-relationships)

### Why is this helpful?

When property constructed with metadata, including as captions, header cells, and header scoping, tables can programmatically provide to screen reader users information about how the data is structured (e.g. relationships), which would otherwise only be available visually to sighted users. Avoid complex tables (e.g., merged cells).

Also, built-in tables are not as susceptible to being deformed by user-defined styling (e.g., window width, font size, zoom level). 

---
## Provide text alternatives for images and figures 

Visuals, such as images, figures, and charts, are helpful for explaining complex concepts. 

Write text descriptions for visuals where applicable. You can provide this description either:
- Via the text placed immediately before or after the visual, which is useful when it is lengthy; or
- By providing “Alt/Alternative Text”, which can be read to a screen reader user

Note that images of text are **NOT** readable by screen readers.

**Relevant WCAG 2.1 Success Criteria**: [1.1.1](https://www.w3.org/TR/WCAG21/#non-text-content), [1.4.5](https://www.w3.org/TR/WCAG21/#images-of-text)

### Why is this helpful?

Text descriptions help preserve the benefits of your visuals when they can’t be loaded, or when they are being used by screen reader users.

### Do all visuals need alt text?

Not all visuals need alt text – they are referred to as “decorative”. The [World Wide Web Consortium (W3C)](https://www.w3.org) provides an [alt decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/).

### What should I write for alt text?

[WebAIM](https://webaim.org) provides the following guidelines for alt text:

- Accurate and equivalent
- Succinct
- NOT redundant (when considered with surrounding text)
- DOES NOT provide information that a screen reader already provides, such as “image of…” or “graphic of…”
- If the associated visual performs an action (e.g., a button), describe the action

---
## Provide text alternatives for math and scientific notations 

Math/scientific notations written in plain text (e.g., “cos(x^3)”) are read verbatim by screen readers, which lack important context. Screen readers support math notations written in MathML.

Alternatively, generate math and scientific notations as images, and provide appropriate alternative text. [WIRIS](https://teaching.resources.osu.edu/toolsets/carmencanvas/guides/carmen-integrations/wiris), the recommended solution for working in Carmen, takes this approach. 

**Relevant WCAG 2.1 Success Criteria**: [1.1.1](https://www.w3.org/TR/WCAG21/#non-text-content), [1.3.1](https://www.w3.org/TR/WCAG21/#info-and-relationships), [1.4.5](https://www.w3.org/TR/WCAG21/#images-of-text)

---
## Provide text alternatives for video and audio clips 

Multimedia is helpful for explaining complex concepts, and can provide nuances (e.g., visual cues, tonal inflections) that other formats, such as text, may not indicate.

Multimedia, even when provided with accessibility in mind, can be distracting to users if audio elements of more than 3 seconds are automatically played in the background. Provide a mechanism to pause or stop the audio, or a mechanism to control audio volume independently from the overall system volume level.

**Relevant WCAG 2.1 Success Criteria**: [1.2.1](https://www.w3.org/TR/WCAG21/#audio-only-and-video-only-prerecorded), [1.2.2](https://www.w3.org/TR/WCAG21/#captions-prerecorded), [1.2.3](https://www.w3.org/TR/WCAG21/#audio-description-or-media-alternative-prerecorded), [1.2.4](https://www.w3.org/TR/WCAG21/#captions-live), [1.2.5](https://www.w3.org/TR/WCAG21/#audio-description-prerecorded), [1.2.6](https://www.w3.org/TR/WCAG21/#sign-language-prerecorded), [1.2.7](https://www.w3.org/TR/WCAG21/#extended-audio-description-prerecorded), [1.2.8](https://www.w3.org/TR/WCAG21/#media-alternative-prerecorded), [1.2.9](https://www.w3.org/TR/WCAG21/#audio-only-live)

## Why is this helpful?

A general rule of thumb of digital accessibility is that text alternatives must be provided for visuals and multimedia. Text can be helpful for users who are deaf or hard of hearing. Text can also be programmatically converted into formats to fit different needs, including audio for users who are blind or visually impaired, and braille for users who are deaf and blind.

For multimedia, some common forms of text alternatives include synchronized caption, transcripts, and audio description (for important visual elements not already described in the audio track). Captions must include transcription of spoken text, speaker identification, and text-equivalents of non-verbal audio (i.e. sound effects).

---
## Place elements of a document in an order they are meant to be read

This concept is generally referred to as “Reading Order”.

In general, for PDFs to be screen reader accessible: 1) text must be selectable and searchable (as opposed to [scanned image, which are not accessible](https://ohiostate.pressbooks.pub/otdidlssmirc/chapter/accessibility-practice-provide-text-alternatives-for-visuals/)); 2) document elements must be accurately tagged with appropriate tag element types; and 3) document elements must have accurate reading order. PDF forms have additional requirements.

**Relevant WCAG 2.1 Success Criteria**: [1.3.1](https://www.w3.org/TR/WCAG21/#info-and-relationships), [1.3.2](https://www.w3.org/TR/WCAG21/#meaningful-sequence)

### Why is this helpful?

Some individuals with visual impairments depend on screen readers, which turns visual content, such as documents, into speech. Sometimes the order in which the elements of a document are visually presented differs from how they are programmatically structured – in other words, such document makes sense to sighted users, but may not for screen reader users. This programmatic order is referred to as “Reading Order”.

---
## Form fields must be named, labeled, and placed in an order they are meant to be completed 

For the purpose of this guide, “form” refers to a PDF form that can be filled out and saved locally on a user’s device. The same concepts can be applied to other common form creation tools, such as Qualtrics and Microsoft Forms.

For a PDF form to be fillable and accessible, it must 1) contain form fields inserted in Acrobat (vs. simply blank space from the originating document); 2) be tagged and have an accurate reading order.

In addition, the form fields themselves must 1) provide descriptive tooltips, which may match text label(s) intended for it; 2) have appropriate types, names and option values; 3) perform error validation and provide helpful error messages, where applicable; 4) be tagged; and 5) have a reasonable tab order.

For more information, see WebAIM’s “[Accessible Forms in Acrobat](https://webaim.org/techniques/acrobat/forms)“.

**Relevant WCAG 2.1 Success Criteria**: [1.3.5](https://www.w3.org/TR/WCAG21/#identify-input-purpose), [2.4.3](https://www.w3.org/TR/WCAG21/#focus-order), [2.5.3](https://www.w3.org/TR/WCAG21/#label-in-name), [3.3.1](https://www.w3.org/TR/WCAG21/#error-identification), [3.3.2](https://www.w3.org/TR/WCAG21/#labels-or-instructions), [3.3.3](https://www.w3.org/TR/WCAG21/#error-suggestion), [4.1.2](https://www.w3.org/TR/WCAG21/#name-role-value)

### Why is this helpful?

“Tab Order” describes the order in which actionable elements in a document, such as links, buttons, and form fields, are focused (thus can be acted upon) when hitting the Tab key on the keyboard. This is generally ensured by a document also having the correct reading order. This is important to keyboard-only users as it is how they navigate between actionable elements.